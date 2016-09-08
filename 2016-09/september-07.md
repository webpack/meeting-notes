## August 31 ([discuss](https://github.com/webpack/meeting-notes/pull/13))

### Attendees

* [Tobias Koppers](http://github.com/sokra)
* [Sean Larkin](http://github.com/thelarkinn)
* [Johannes Ewald](http://github.com/jhnns)
* [Juho Vepsäläinen](http://github.com/bebraw)


### Agenda

#### Documentation Updates
* Juho: Migrated a significant grouping of issues labeled `question` or `documentation` from [webpack/webpack](github.com/webpack/webpack) over to the [new docs page](github.com/webpack/webpack.js.org).

* PR's are now in for adding helpful documentation linters and plugins
	* proselint: will help with grammar and has settings for rules etc.
	
	* [#96](https://github.com/webpack/webpack.js.org/pull/96)

	* ESLINT module for codeblocks for markdown documents. This will ensure that our code examples are consistent across documents etc. [MERGED #97](https://github.com/webpack/webpack.js.org/pull/97)

	* Juho also suggested we look into `alex` which works with proselint on spelling and linting specific words based on topic (offensive, abbreviations, etc.)

	* Don't want linting too strict, just enough to provide, autoformatting, and eliminate the number of round of reviews for PR's.

* The topic of Cont. Deployment came up for our documentation. We veiw some other pages and it apeard Codeship is a popular option as well as Travis but requires more work. An issue will be created in the docs repo. 

#### Publication Updates
* Upon feedback, we discovered that Housing.com's engineering team had published an excellent article on medium about their success's with webpack. Sean suggested that we open up the option for authors who are interested, to post success stories and awesome information under our publication (after review). The team decided this would be fine since we have been slacking on our medium publication as of late. 

#### Domain
* We discussed between `webpack.js.org` and `webpack.github.io`. After we did the research we decided that we would setup `webpack.js.org`. Tobias is going to tackle this a bit later today. 

#### Analytics 
* Sean asked whether or not we have page analyitcs on our docs site currently. Tobias gave access to all the analytic data. Sean also brought up the idea of having webpack the tool ask if users would let us submit analyitcs data. Tabeled discussion as its a severe nice-to-have.

#### Logo
* Johannes had prepared some simple mock ups for a new logo design. We discussed a few color options, and that we could poll the community however, we want to iterate on the design that we feel expresses our goals, etc.

#### Issues/Defects 
**[#1792](https://github.com/webpack/webpack/issues/1729)**: 
	* This issue was brought up because it appears that our `node` target has been functioning this way for over a year with not one report until now. Tobias: "webpack should be identical to node in the `node` target". 
	
	* By using `module` like this, webpack's runtime would take a significant hit. (`try-finally` bails out the V8 compiler [and its called for every `require()` call] )
	* We will have to investigate the `node.js` repo and see if there is anyone coming across this issue already with useful knowledge. Otherwise we will create an edge-case target so that this can be used the proper way. We will discuss this more in detail next meeting. 

**[#250](https://github.com/webpack/webpack/issues/250#issuecomment-199602293)**: 
	* Johannes raised this issue because it is notable that some scaled builds take long to finish (even if it is 2-3 minutes). Johannes mentioned [`HappyPack`](https://github.com/amireh/happypack) is a common package that allows you to multithread the loader process. However there are struggles with the way that "hacky" loaders work that make `HappyPack` impossible for `awesome-typescript-loader` and `ts-loader` to implement together. 
	* Sean describes this "hackyness" is when a loader accesses `compiler` properties from `this` such as `this._compiler` to execute plugin based functionality. Needs to be deprecated.
	* Tobias mentions that maybe we can add functionality to the loader API to allow this to work. Sean explained that the reason these TS loaders need plugin access is because it needs to defer typechecking until the `compilation` is finished. 
	* Tobias mentions that deferred execution could be a feature we need to add to the loader API. Could also be useful for image sprites, etc. 
	* Johannes brings up that this is the same problem to `extract-text-plugin` (when you need to apply a plugin and a loader together).
	* Tobias states that this could fix a great deal of "hackyness" from `extract-text-plugin` and move it to a loader. 
	* Sean suggested that the deferred execution be expressed by unwrapping a promise. (
	The loader function itself would return the promise. ) Would be minimal additional effort and easy for developers to understand.
	* Tobias mentioned that tool that would be moved and use the new deferred execution API [(doesn't exist yet but suggested idea) `image-sprite-loader` and the `seperate-css-loader`] would need to include an `invalidate` method to issue recompilation from the callback. It would also need to include the following: 	
		* errors/warnings
		* invalidating => recompilation w/ new data
		* emitting files
		* access to the current chunk info (edited)
	* additionally noted it would fall after optimization and before id creation (in the compilation step)
	* This would also allow ts-loader and awesome-typescript-loader to execute typechecking in the resolve promise. (allowing tools like HappyPack to execute loaders parallel/multithreaded)
	* Johannes mentions that it would be important that we get feedback from loader authors to see if this would help solve some of their issues (including HappyPack).
	* Tobias described, (once implementing this feature [based upon the comments in the linked issue]) that a `disk-cache-loader` would look similar to having the following.
		* pithing phase (this is a pitching loader)
		* check disk cache for an entry
		* if there is an entry:
		* hash all content of entry.dependencies
		* compare hash with entry
		* if equal:
		   * return entry.source and entry.dependencies as result
		* continue loader execution
		normal phase:
		* store dependencies, hash of dependencies and source in disk cache (edited)
		* alternativly it could use loader-runner to run the remaining loaders. This would allow to cache more data: emitted files, errors, warnings. This would not be possible in the normal loader chain.
	* Issues will be created for each of these missing features. (Sean).
### Takeaways  
* Documentation

-----------
Please feel free to discuss these notes in the [corresponding pull request](https://github.com/webpack/meeting-notes/pull/13).

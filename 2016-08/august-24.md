## August 24 ([discuss](https://github.com/webpack/meeting-notes/pull/11))

### Attendees

* [Sean Larkin](http://github.com/thelarkinn)
* [Tobias Koppers](http://github.com/sokra)


#### Attendee Notes:
Johannes is in Iceland at JSConf Iceland (Good luck!), and Juho was unable to make the meeting today. 

### Agenda

#### Documentation Updates

* We were able to reach [Marco Pai](https://github.com/MarcoPai), however the offer he kindly extended to us for puchase of  webpack.io was too steep. We may consider keeping the existing domain, as the traffic is extremely high. We decided to talk about this after documentation has been a little bit more fleshed out. 

* We have had some more pull requests for documentation, however on the current pace we are at, it is most unlikely that we will not be able to release the beta tag from webpack 2 just yet because we have not fullfilled our [milestone/plan of action](https://github.com/webpack/webpack.io/issues?q=is%3Aopen+is%3Aissue+milestone%3A%22Webpack+2+-+Documentation+MVP%22). We are working on getting the site deployed, so that it is easier for people to see and use the new documentation page. Contributions should be as easy as getting a github link for the document you are looking at and then commiting the changes, and submitting a PR. 

#### Reported Issues

**Tree Shaking / Optimization**  
* We discussed briefly our disappointment that [UglifyJS2](https://github.com/mishoo/UglifyJS2/issues/1261) is not willing to work on a solution to to remove side-affects from transpiled unused ES6 exported classes transpiled to ES5 (by both Typescript and Babel). [#2867](https://github.com/webpack/webpack/issues/2867). 

* We decided that this is not a responsibility of *webpack*, however we see the need for a very strong general purpose tool that needs to be developed. Tobias suggested that we (along with the community) build a tool that handles the following: 
   
  * Anyone could use it, and we would leverage it in a plugin like UglifyJSPlugin
  * Complex side effect analysis to figure out it if the exported declaration is sideeffect-free, and not used somewhere else. 
  * Reading the AST, create a dependency graph of variables and references, Have some common templates for optimization, figure out what is unused, write the new AST. 
  * Cover all the edge cases: `eval`, `with`, global scope, `arguments`, conditionals
  * Program, Flow Analysis
  * It would be a general purpose optimization not specific to webpack.

* After we integrate Rollup features into webpack and then potentially usability changes (post 2.x release). We hope this will be a tool collaboratively developed in parallel by many interested parties (including ourselves) in this endeavor as it mutually benefits the entire javascript community.

**Rollup / Module Inlining**
* Because of the UglifyJS2 issue and results, It was appropriate to bring up the next steps in development after 2.x which is adding the module inlining, and what incremental steps we can take in development to start working on this. Webpack currently does not have plugin hooks for combining modules (a key feature of Rollup/Module Inlining). Tobias said this would be one of the first easier steps to make towards this feature. It could also allow people to work on implementations themselves if they wanted to. Second step will be using the same "variable deconflictor" that rollup uses to help make conflicts in variable names trivial. 

###Takeaways  
* **Documentation:** We need our milestone completed. Completing this goal is crucial for the community. 

-----------
Please feel free to discuss these notes in the [corresponding pull request](https://github.com/webpack/meeting-notes/pull/11).

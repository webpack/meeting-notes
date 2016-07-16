## July 15 ([discuss](https://github.com/webpack/meeting-notes/pull/5))

### Attendees

* [Johannes Ewald](http://github.com/jhnns)
* [Sean Larkin](http://github.com/thelarkinn)
* [Juho Vepsäläinen](http://github.com/bebraw)
* [Jesus Rodriguez](https://github.com/foxandxss)
* [Tobias Koppers](https://github.com/sokra)

#### Attendees Notes

* Jesus joined us today for the Google hangout. Jesus is working directly with Juho for documentation on webpack/webpack.io and his involvement is pertinent.

### Agenda

#### Medium and Publications

* We are have great response from our Medium publications still but we are tweaking the time and dates that we want to release. Juho said that we can try monday instead of saturday morning (CST) to release the publication. Johannes suggested Friday daytime, however we decided in the end to publish this Monday, and then continue to play with the date/time.

* Tobias offered to write this weeks publication article which will be an informative look into the AgressiveSplitPlugin. This will go out on Monday and will need to be reviewed by the team. 

#### Typescript Typings

* Sean brought up that there has been multiple responses from individuals to not only bring typings to webpack 2.x, but also include official typings into the repository. Sean mentioned that the benefits could allow people to use typescript in their configurations and have automatic type validation. Tobias asked if we would have these tested incase changes are made. Sean said that we could write tests that allow the types to test against the webpack compiler and configuration and plugin api & that it would be a huge benefit for users and developers on core. A typings file would simply be added to the repository and a `'typings'` field added to the package.json. Everyone agreed to this as long as it is tested and integrated into the CI process. Sean mentioned he has one or two people already offering to assist him with this and will now look into this even further. 

#### Documentation

* Stubs for learning resources continue to pour into the github. 

* Sean has offered to take on some of the Plugin API documentation when he gets around to it after his angular-cli webpack integration work. Also asked if Tobias would be willing to write the high level overview documentation for the Resolver instance. It is currently the least documented Plugin API feature and it would be great to have Tobias write it so that no stones are unturned about its use. 

* The `antwar` [branch](https://github.com/webpack/webpack.io/tree/antwar) which contains most of Juho's work is nearing its point of completion. Juho states that a PR will be coming within the next week or so with all the content changes. 

#### Slack

* Sean recapped that he finally set up and sent out slack to the core team members. The team decided that we would try it out, as well as invite plugin and loader authors in hopes of specifically communicating with them more efficently. 

#### Core Loaders and Plugins

* Juho has created a document with initial sorting and assignment for loaders and plugins. Sean mentioned that he will go through this list and add anyone else that remains. Once this list is approved we will send to Tobias to extend invitations to the organization and repos.

#### CSS Loader & CSS Modules 

* Johannes brought up that there are still a number of performance related issues in regards to `css-loader` and inquired whether or not it would be possible to isolate the css-modules code from the loader. Tobias said that the changes he had made which were thought to increase performance were not as good as promised. Johannes asked if we could instead have two separate loaders so that people who do not want to use css-modules can simply use a faster lightweight css-loader option instead. Tobias said it may be possible and would look into it.

### Takeaways
* Finalize vetting people for core loaders and plugins (Sean)
  * Clean up Pull Requests (all)
* Review Medium Article (all)
* Finish article for publication on HTTP2 & Webpack.
* Look into separate loader for CSS vs CSS-Modules (Tobias/Johannes)
* Start gathering a full team to work on webpack typings. 


-----------
Please feel free to discuss these notes in the [corresponding pull request](https://github.com/webpack/meeting-notes/pull/5).

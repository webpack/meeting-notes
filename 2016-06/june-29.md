## June 29 ([discuss](https://github.com/webpack/meeting-notes/pulls/1))

### Attendees

* [Tobias Koppers](http://github.com/sokra)
* [Johannes Ewald](http://github.com/jhnns)
* [Sean Larkin](http://github.com/thelarkinn)
* [Juho Vepsäläinen](http://github.com/bebraw)

### Agenda

#### Repo Management Tools

* Discussed briefly using Github management tools to help:
  * Move issues between repos:
  * Apply Issues to multiple repos: 
  * Track and coordinate milestones across repos:
  
#### Documentation

* Tobias worked on an [outline](https://github.com/webpack/webpack.io/commit/18b7f14d686b76775d1b5de763423d121bc28f0b) that could serve as a foundation for webpack/webpack.io. 
* Had one or two voluneers express interest in working on documentation however we will want to have a handful of folks working on documentation. (Because there is a lot to document).
* Suggestions were made to create individual issues for each of the "topics or features" for webpack so that we can easily track our progress. 
* Sean is still looking for a company who specializes in content creation etc. to help donate their efforts if possible.
* We will start to tag issues in github that we have answered/found useful for people with the `documentation` tag so that we can address them in the future documentation

#### Releasing Webpack 2.x Official

* Sean has created a filter of [current reported issues](https://github.com/webpack/webpack/issues?q=is%3Aopen+is%3Aissue+label%3Abug+label%3Awebpack-2+sort%3Acreated-asc+label%3A%22in+planning%22) that Tobias is going to look through to see if it has been already fixed, or if it is by design/not a bug, etc. 
* We agreed that a 2.x RC/Official Release milestone will be created that will assist us in tracking what remains. This will propose somewhat of a challenege because there is webpack/webpack-dev-server and other repo's to ensure are up to date to any breaking changes. 
* Also working on PR Issues, support for problems from @gaearon and @gdi2290 (Strong representatives from the Angular and React communities).
* In the end Documentation for [webpack/webpack.io](http://github.com/webpack/webpack.io) will be the **critical blocker**. Otherwise, only easy/small features/bugs remain.
* Backporting the --env `function` style webpack config definition so that transition is easier for users can use the feature if desired going from webpack 1.x to webpack 2.x. 

#### Releasing After Webpack 2.x Official

* Adding an InlinePlugin (name TBD) that will support RollUp style inlining of modules for ES6 tree shaking capabilities. But requires core changes and should happen after 2.x release. 
* 

#### Public awareness

* In addition to adding the meeting-notes as public Tobias brought up the idea of a Medium publication that all of the core team memebers can post on. The 'voice' of webpack tailored by the community's needs and wants. The Content will contain: 
  * Looking for maintainers for some repos
  * Webpack 2 release plan
  * Documentation plan
  * Slack
  * Sponsor/Donations plan
  * Team members
  * Thanks to loader authors
  * Ask what people expect from a webpack blog
* We want people to know that webpack 2.x not only represents a change in the code, but also dev community involvement, transparency, and support. #Webpack <3 #Developers

### Takeaways

* Backport --env
* Create a medium publication (tobias/sean)
* Create a blog post (tobias/sean)
* Find some more people to invite to maintain the loaders and plugins or decide to depricate unused ones: (all)
  * karma-webpack
  * coffee-loader
  * component-webpack-plugin
  * grunt-webpack
  * mocha-loader
  * html-loader
  * compression-webpack-plugin
  * i18n-webpack-plugin
  * transform-loader
  * jshint-loader
  * json5-loader
  * coffee-redux-loader
  * coverjs-loader
* Work on Standardized Ts loader/plugins if authors are willing CC @jbrantly&@s-panferov (Sean)
* Create 2.0 Typings team to work with documentation team and changes to accuratley be reflected in the typedefs (Sean) 

### Common Questions

1. How does one do target webpack builds? 
Using tools like [parallel-webpack](http://tech.trivago.com/2015/12/15/parallel-webpack/). There is a specific section on targeted builds. 

2. How does LoaderOptionsPlugin replace UglifyJsPlugin for minification. 
The LoaderOptionsPlugin delegates the minification and optimization to the loader itself. Therefore if the loader doesn't implement the properties (for 2.x) then nothing will happen. https://gist.github.com/sokra/27b24881210b56bbaff7#loader-options--minimize 

Please feel free to discuss these notes in the [corresponding issue](https://github.com/webpack/meeting-notes/pulls/1).
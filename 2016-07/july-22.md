## July 22 ([discuss](https://github.com/webpack/meeting-notes/pull/6))

### Attendees

* [Tobias Koppers](https://github.com/sokra)
* [Sean Larkin](http://github.com/thelarkinn)
* [Juho Vepsäläinen](http://github.com/bebraw)
* [Spencer Stark](https://github.com/spencerstark) 
* [Guy Bedford](https://github.com/guybedford)

#### Attendee Notes:
Guy Bedford was kind enough to join us to help tackle integration of Webpack w/ the Loader Spec and/or SystemJS.
Spencer was in attendance to take meeting notes. 

### Agenda

#### Documentation Updates
* Juho is currently working on documentation, all is going well. He's getting ready to submit a pull request with his current works with the intent to merge soon. After this grooming and reviewing issues will take place. 
* There will be another blog post with regards to documentation and the process coming soon. 

#### Core Loaders and Plugins
* We all agreed on the following list of repository team leads:
  * JSON5-loader: **gdi2290**
  * HTML-loader: **hemanth**
  * Mocha-loader: **tricoder42**
  * Transform-loader: **minwe**
  * JShint-loader: **kostasmanionis**
  * I18n-webpack-plugin: **ecutdavid**
  * Grunt-webpack **danez**
  * Karma-webpack: **mikaak**
  * ESlint-loader: (Obsolete)?
  * Component-webpack-plugin (deprecated)
    * Tobias thinks we should consider deprecating and leaving this plugin alone. 
  * Compression-webpack-plugin
    * Team lead => (?) 

#### Initial tasks for teams 
	
* Mimic issue templates / types from webpack/webpack 
* This will be some of the first “Pilot PR’s” for these teams once created
* Review old PRs in repos, start to implement support for webpack 2.0 breaking changes
* Continue to monitor and support once established
* Add testing 

#### SystemJS
* SystemJS is pretty well documented and well flushed out and positioned well for integrations
* Challenges:
  * Static loader, dynamic bundler?
  * a library that's usable in system js?
  * Private v. public modules
  * External modules with a systemJS call to load it.

* Thoughts:
  * Would need to be a normal output file with a systemjs suffix on it?
  * If you have a `System.import` with some module name as an identifier, you’ll want to know which module to get with the dynamic loader
  * You need some sort of mapper to a public registry? (From chunk ID's to names)
  * Guy suggested the concept of public modules, public module loader vs webpack.
  * Tobias mentioned that this has been done already before for another plugin (`DllPlugin`) and that we could resuse a lot of the functionality
  * Most modules need to be loaded, but not all. 
  * You’re plucking some modules out and exposing them (to the registry) and these ones would then be webpacked?.

* Would this be a plugin?
  * Might be better as a library?
  * Yes, it would be, and potentially expose the entry points and the needed 'public modules'. 
  * Would be a libraryTarget setting. IE: `libraryTarget: 'systemjs'`
  * Probably an underlying plugin will be written

###Takeaways  

* Send out official invites for core team (Tobias)
* Create issue for Guy/Tobias to work on for SystemJs/Webpack integration (Sean)
* Continue documentation effort. Clean up github issues with labels and more organization (Juho)

-----------
Please feel free to discuss these notes in the [corresponding issue](https://github.com/webpack/meeting-notes/pull/6).

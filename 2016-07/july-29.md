## July 29 ([discuss](https://github.com/webpack/meeting-notes/pull/7))

### Attendees

* [Tobias Koppers](https://github.com/sokra)
* [Sean Larkin](http://github.com/thelarkinn)
* [Juho Vepsäläinen](http://github.com/bebraw)
* [Johannes Ewald](http://github.com/jhnns)
* [Jesus Rodriguez](https://github.com/foxandxss)
* [Spencer Stark](https://github.com/spencerstark)  


### Agenda

#### Documentation Updates

* Juho working on documentation, which is going well. His time was stretched a little thin this week and he didn't get as far as he wanted to. 

* Jesus hasn't been as available as he would like, but is working on documentation as his time permits. 

* Want to know the progress on the documentation?

    * Progress on documentation can be found in the [Readme](https://github.com/webpack/webpack.io#content-progress)

* We are in the process of discussing Domain names and have set a milestone for next weeks meeting, more on this in takeaways. 

#### Configuration

* With regards to [Usability Discussion](https://github.com/webpack/webpack/issues/2797)

* Johannes spoke to the difficulty of setting up a configuration file. 

    * If people are having a hard time understanding and setting up the configuration, we need to cater to the set up process and provide information and tools to help them get set up and going easier. 

    * Strive for simplicity.

    * With Webpack 2 we hope to simplify configuration. A config can be as simple as entry and output. 

* There are different approaches we can take to simplify the configuration for people new to Webpack.

    * Validation

        * We could come up with a validation system to make sure that the webpack.config is correct and valid. 

    * IDE Support

        * We would want to brain storm on this further. 

    * What about a UI for configuration?

        * This could potentially help with those who haven’t used Webpack before to get going for the first time. 

        * This could certainly make it easier for beginners. 

* There is certainly room to remove the complexity

#### Overview of loader teams work

*  What are the thoughts about the loader teams?

    * We're extremely happy with how they’re coming along. 

* The way the HTML Loader was laid out was very notable. 

#### SystemJS

* Guy Bedford has been kind enough to investigate [SystemJS (Registry) Target for Loader Spec](https://github.com/webpack/webpack/issues/2810) for Webpack. 

    * Sean wants to spend time and use the plugin to understand it better and will follow up with implementation details. 

###Takeaways  

* Sean

    * Start list for possible domain names for discussion next meeting.

    * Communicate and promote the documentation process. 

* Johannes

    * Create a list of configuration options we can simplify for discussion next meeting.

-----------
Please feel free to discuss these notes in the [corresponding issue](https://github.com/webpack/meeting-notes/pull/7).

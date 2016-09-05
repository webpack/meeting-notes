## August 31 ([discuss](https://github.com/webpack/meeting-notes/pull/12))

### Attendees

* [Tobias Koppers](http://github.com/sokra)
* [Sean Larkin](http://github.com/thelarkinn)
* [Johannes Ewald](http://github.com/jhnns)
* [Juho Vepsäläinen](http://github.com/bebraw)


### Agenda

#### Documentation Updates
* Multiple PR's have been merged, including [#77](https://github.com/webpack/webpack.io/pull/77) by [@pksjce](https://github.com/pksjce) which increased our [milestone](https://github.com/webpack/webpack.io/milestone/1) completion to 30%!!

* Sean inquired we should create additional incentive for users to help write documentation. The following ideas were considered: 
  
  * Add contributors recognition on created pages (that they have 'touched').

  * Some sort of T-shirt, swag, etc.

* Sean mentioned he was working on the finishing touches to [#81](https://github.com/webpack/webpack.io/pull/81). This will help shape a "First-time user journey."

* Some features are still missing from the docs page that we should have before release: 

  * Ability to sort articles (for sidebar and flow). [#93](https://github.com/webpack/webpack.io/issues/93)

  * Ability to tie relavant articles (like wikipedia's md). [#94](https://github.com/webpack/webpack.io/issues/94)

  * Per-doc contrib generation [#95](https://github.com/webpack/webpack.io/issues/95)

#### Scope Collapsing/Module Inlining

* Tobias spent a bit of time working on a tool that will both assist in scope collapsing/module inlining as well as serve for Analyzing scope, high-level compression and minification. We haven't released it yet but could be coming soon in a separate public repo. Like we mentioned in last meeting, it would be good to have multiple members of the community help us approach this tool as an all around solution. Once we finish tackling webpack 2 defects and documentation, we can revisit this. 

#### Logo

* With new docs and design around the corner Johannes wanted to know if we could revisit the design of the logo, and iterate over some ideas. All were for this. 

* We will hold off on looking into t-shirts until the logo has been overhauled.

#### Domain

* We discussed between `webpack.js.org` and `webpack.github.io` briefly, but it was tabled for next week. The continuing discussion on this is due to the implications that a domain change may have on traffic.

### Takeaways  
* Documentation!
* Create github issues for new docs features (Sean).
* Research webpack.js.org and webpack.github.io for webpage. 

-----------
Please feel free to discuss these notes in the [corresponding pull request](https://github.com/webpack/meeting-notes/pull/12).

## July 29 ([discuss](https://github.com/webpack/meeting-notes/pull/8d))

### Attendees

* [Sean Larkin](http://github.com/thelarkinn)
* [Juho Vepsäläinen](http://github.com/bebraw)
* [Johannes Ewald](http://github.com/jhnns)
* [Jesus Rodriguez](https://github.com/foxandxss)

#### Attendee Notes:
Tobias is going to be on vacation for a couple weeks and thus wasn't present for this meeting.

### Agenda

#### Documentation Updates

* Sean has [merged](https://github.com/webpack/webpack.io/pull/59) our first [new documentation](https://github.com/webpack/webpack.io/blob/develop/content/concepts/index.md) into webpack/webpack.io!!!! Share it around, and provide feedback. It is still in a beta state as there is some link cleanups. But he wanted to provide a great introduction to people who haven't already had one. 

* We are still on the hunt for the `webpack.io` domain name. We see its registered to a gentleman in China, and would love any Mandarin speakers to help us draft an email to reach out to him for domain purchase as the first few emails have been unsuccessful!! [Marco Pai](https://github.com/MarcoPai) has some slight activity on github. So we aren't giving up hope just yet.

* Currently the `webpack/webpack.io` is a statically generated site, so Juho is going to be working to add React and JS for Dynamic usage in other portions of the page. 

* Documentation Structure has been finalized!!!! Priority number one is now creating the content and merging it into develop! The styling for the page is still a work in progress, however that is our last priority before we "ship the docs". 

* For future we may have Johannes with the help of other UI Designers to create personas that help us and contributors create appropriate language for documentation. Agreed that it was a very-nice-to-have but also a great addition if we ever had time. 

* Would love to have folks work on a ShemaStore schema for the webpack configuration. This we could use to autogenerate some documentation like the API: Configuration page. Also could provide IDE support for people almost out of the box. Need to look into how to do this when we tackle that documentation. 

* It was brought up that we need to create a feasible action plan that we can share with the Dan Abramov's, Kent Dodd's, and Patrick Stapleton's of the JS community to pass along and promote. It is in everyones best interest to work together to create documentation and having a strategy to accomplish this is vital. We spent time listing out the immediate MVP documents that would the team agreed could allow us to life the webpack 2.x beta status. 

* Juho created a [Github Milestone for all these tasks that we can give to people](https://github.com/webpack/webpack.io/issues?q=is%3Aopen+is%3Aissue+milestone%3A%22Webpack+2+-+Documentation+MVP%22)!!!! Barring any major or breaking changes from popular community loaders or plugins (as well as the core loaders and plugins), once this is finished, we believe this is our 'go-ahead' to lift the beta status. We all agreed that although this wouldn't contain all of the documentation we aspired to tackle, that this would give the (first time) users _that need it the most_, the opportunity to have a _far more_ augmented learning experience than what is available. 

* Everyone also agreed that we could technically accomplish this by the end of August. **Yes people, it's getting more than real, this is an estimated timeline of webpack 2.x being out of beta!** :champagne: :heart_eyes: :champagne:. If all goes well and we meet our deadline, then we can lay out our next milestone for more advanced "revisions" of our existing documentation migrated over to the `webpack/webpack.io` repo.

* **We will want/need lots of help!!!** So please share the link of the milestone above. The milestone will also include general guidelines for how to author one of these docs. And once we have a collection of people we can meet weekly via hangout, etc. to track and manage the Milestone goals, etc. There is also a [getting started page](https://github.com/webpack/webpack.io/blob/develop/content/get-started.md) we have referenced on the repo as well for those worried about contributing. It doesn't have to be perfect the first time around. 

#### Publication

* Sean admitted he has slacked a little bit on getting a new article for our publication, but wants to make it a priority to announce that the angular-cli and react-create-app are both powered by webpack now. 

* Its a huge milestone of integration for us. Including Laravel and Rails:Middleman and Grails new asset Pipline. The list of webpack users is seeming to continue to increase and the learning and constructive criticism continues to grow. This _is the tool you made and helped customize_ in the end, so every person, framework, library, boilerplate, MVC, that uses webpack is another win for you and the webpack team. 

#### Sourcemaps

* We have had a bunch of reports of [sourcemap issues](https://github.com/webpack/webpack/issues/2145) brought to Sean's attention. He's going to attempt to continue and connect with the ChromeDevTools team to see what we can do here, or needs to be done to help fix this.

###Takeaways  

* Sean:

    * Obtain domain

    * Ping Marco Pai on github as well

    * Publication

    * Communicate Action Plan for Docs

    * Add Writers Guide on Readme.md for webpack.io. (https://github.com/webpack/webpack.io/blob/develop/content/writers-guide.md#article-structure)


* Juho:

    * Add React Dynamic to AntwarJs.

* The Community (You Reading This): 

    * Spread the news about our [milestone/plan of action](https://github.com/webpack/webpack.io/issues?q=is%3Aopen+is%3Aissue+milestone%3A%22Webpack+2+-+Documentation+MVP%22) and help get the community together to bring a kick-ass learning experience for webpack users!!! Promote, share, contribute. Juho and Sean have promised to help revise and check any and all PR's that come in as a top priority if they will help close an issue on our Milestone. 

    * We want you to tackle the issues listed in that link, and then join us in our [gitter doc chat](https://gitter.im/webpack/docs). This is where we will collaborate any efforts for documentation. Everyone is welcome!!! Thank you so much! 

-----------
Please feel free to discuss these notes in the [corresponding issue](https://github.com/webpack/meeting-notes/pull/8).

# Backbone.js at Boston Front End Development Meetup

This is an HTML slide deck.

* Press "h" for help, or use the arrow keys to navigate.
* Press "p" for presenter notes, where you'll find a bunch of links, especially towards the end.

---
# Web apps shifting client-side

# Presenter Notes

* These days, some web apps have more code on the client than on the server.
* Who is seeing these trends?  What are you doing about it?
* How much JS?

    * Airbrake: Almost 0
    * Copycopter: 30%
    * Trajectory 41%
    * IoraHealth: 62%

* Hands up: Back end, front end, javascript, js MVC/MVVM frameworks 

---
# Goals of this shift

# Presenter Notes

* Improve UX through responsiveness
* First: Reduce server-side loads
* Then: Reduce AJAX calls
* Break that down: Background AJAX or No AJAX

---
# Frameworks

# Presenter Notes

* Where do frameworks come from?
* Landscape (defining features) -> path-least-resistance -> impl -> arch -> tech dividends/debt
* Server: Req/response (CGI, EHTML) -> procedural, high duplication, low modularity/encapsulation ( -> testability)
* Client: Async ($) -> Deeply nested callbacks (if-like), Stateful (DOM) -> app data stored in the DOM, AGAIN high dupe, low modularity/encapsulation/testability
* Patterns for organization.  MVC is one.  Good for GUI.
* MVC over HTTP is often stateless.  Some state maintained with session
* CS-MVC in GUI is stateful.  THIS IS OKAY!

---
# But which framework?

* SproutCore 2.0
* Knockout.js
* JavaScriptMVC
* Spine.js
* Backbone.js
* (And then Angular, Coherent, PureMVC-js, AFrameJS, ...)

# Presenter Notes

* Backbone: JavaScript-y, small, readable, intended for modification, extracted
* Spine.js: Very similar.  Even smaller.  Coffee.  Fully async, client rules.
* SC2: Similar, larger.  Less doc.  Declarative bindings, computed properties.
* JavaScriptMVC: Larger, older, generators, dep mgmt, builds, testing, jQuery-based-and-like, JSON/REST transport
* Knockout: MVVM.  (MS history: WPF, Silverlight.) Declarative bindings, computed properties.

---
# Compare frameworks

* [http://addyosmani.github.com/todomvc](http://addyosmani.github.com/todomvc)

---
# Example

* [http://backbonechat.herokuapp.com/](http://backbonechat.herokuapp.com/)

# Presenter Notes

* Use the app
* Point out URLs changing
* Point out view update

---
# Code dive

* History
* Router
* View
* Model
* Collection

# Presenter Notes

* (illustrate moving parts as you go)
* History - Handles hashchange, pushstate, BB.history.start()
* Router - read fragment, dispatch to action
* View - Takes model data, presents in DOM.  Binds to DOM events, triggers app logic.  1:1 `el`, `this.$`, `events`, `$.delegate`, templating
* Model - Conversions, computed properties, validations, access control, events change/change:attr,destroy,error
* Collection - Ordered set of models.  URL, fetch(), reset(json), _.methods, comparator, events reset/add/remove/all model events

---
# Peek under the hood

* Sync
* Underscore
* $

# Presenter Notes

* Sync - Encapsulation of persistence. Default `$.ajax` to RESTful JSON API.  Designed for override, global or per-class.
* Underscore -  FP functions (select, reduce), bind, template, deep comparator isEqual, clone, tap
* $ - jQuery || Zepto

---
# Books on JavaScript

* [JavaScript: The Good Parts](http://shop.oreilly.com/product/9780596517748.do) by Douglas Crockford
* [JavaScript Web Applications](http://shop.oreilly.com/product/0636920018421.do) by Alex MacCaw (Spine.js author)
* [Test-Driven JavaScript Development](http://tddjs.com/) by Christian Johansen
* [JavaScript Patterns](http://shop.oreilly.com/product/9780596806767.do) by Stoyan Stefanov
* [JavaScript: The Definitive Guide](http://shop.oreilly.com/product/9780596805531.do) by David Flanagan

---
# Backbone.js reference materials

* [Official Backbone docs](http://documentcloud.github.com/backbone/)
* [Annotated source code](http://documentcloud.github.com/backbone/docs/backbone.html)
* [Underscore docs](http://documentcloud.github.com/underscore/) and [source](http://documentcloud.github.com/underscore/docs/underscore.html)
* [Backbone Google Group](https://groups.google.com/group/backbonejs)

---
# Backbone.js learning materials

* [thoughtbot Backbone on Rails eBook](http://workshops.thoughtbot.com/backbone-js-on-rails)
* [Peepcode episodes on Backbone](http://peepcode.com/products/backbone-js)
* [Recipes with Backbone](http://recipeswithbackbone.com/)
* [Backbone.js live chat audio and notes](http://workshops.thoughtbot.com/pages/backbone-js-on-rails-qa-live-chat-1)

---
# Bonus round

* pushState
* localStorage
* WebSockets
* Testing

# Presenter Notes
* pushState
    * What does it look like? http://pjax.heroku.com/
    * How does it work? https://developer.mozilla.org/en/DOM/Manipulating_the_browser_history
* localStorage
    * http://documentcloud.github.com/backbone/docs/backbone-localstorage.html
* WebSockets
    * Nothing specifically interesting, but modularity helps
* Testing
    * [Jasmine](http://pivotal.github.com/jasmine/) goodies!  Get these.
    * Spy/stub/mock, even your HTTP, with [sinon.js](http://sinonjs.org/)
    * If you're looking for factory_girl.js, it's called [Rosie](https://github.com/bkeepers/rosie)
    * [guard-jasmine](https://github.com/netzpirat/guard-jasmine) autotest your Jasmine with headless webkit ([phantomjs](http://www.phantomjs.org/))
    * Get started with James Newbery's excellent blog posts on [testing Backbone with Jasmine](http://tinnedfruit.com/2011/03/03/testing-backbone-apps-with-jasmine-sinon.html)
    * Check out his [examples on GitHub](https://github.com/froots/backbone-jasmine-examples)

---
# Thanks!

* [http://jayunit.net](http://jayunit.net)
* [View slides online](http://jayunit.net/backbone-front-end-presentation)
* [View slides source on GitHub](http://github.com/jasonm/backbone-front-end-presentation/tree/gh-pages)

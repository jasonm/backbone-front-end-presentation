# Backbone.js

This is an HTML slide deck.

* Press "h" for help, or use the arrow keys to navigate.
* Press "p" for presenter notes, where you'll find a bunch of links, especially towards the end.

# Presenter Notes

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
# Organize your JavaScript

# Presenter Notes

* Where do frameworks come from?
* Paradigm -> path-least-resistance -> implementation -> architecture -> technical debt
* Server: Req/response (CGI, EHTML) -> procedural & tag soup *SP.
* Client: Async ($) -> Deeply nested callbacks (if-like), Stateful (DOM) -> app data stored in the DOM.
* Patterns for organization.  MVC is one.  Good for GUI.
* MVC over HTTP is often stateless.  Some state maintained with session
* CS-MVC in GUI is stateful.  THIS IS OKAY!

---
# But which framework?

* SproutCore 2.0
* Knockout.js
* Batman.js
* JavaScriptMVC
* Spine.js
* Backbone.js
* Angular, Coherent, PureMVC-js, AFrameJS, TrimPath Junction,...

# Presenter Notes

* [Decision Fatigue NY Times Mag article](http://www.nytimes.com/2011/08/21/magazine/do-you-suffer-from-decision-fatigue.html)
* SC2: Similar, larger.  Less doc.  Declarative bindings, even in templates.
* Knockout: MVVM.  WCF, Silverlight.
* Batman: Node server, share models, data-bind templates
* JavaScriptMVC: Larger, older, generators, dep mgmt, builds, testing, jQuery-based-and-like, JSON/REST transport
* Spine.js: Very similar.  Even smaller.  Coffee.  Fully async, client rules.
* Backbone: Small, readable, intended for modification, extracted from DocumentCloud

---
# SproutCore 2.0 Example: NOTES

---
# Knockout.js Example: NOTES

---
# JavaScriptMVC Example: NOTES

---
# Spine.js Example: NOTES

---
# Backbone.js Example: NOTES

---
# Request dive (illustrate moving parts as you go)

* History
* Router
* View
* Model
* Collection

# Presenter Notes

* History - Handles hashchange, pushstate, BB.history.start()
* Router - read fragment, dispatch to action
* View - Takes model data, presents in DOM.  Binds to DOM events, triggers app logic.  1:1 `el`, `this.$`, `events`, `$.delegate`, templating
* Model - Conversions, computed properties, validations, access control, events change/change:attr,destroy,error
* Collection - Ordered set of models.  URL, fetch(), reset(json), _.methods, comparator, events reset/add/remove/all model events
* Sync - Encapsulation of persistence. Default `$.ajax` to RESTful JSON API.  Designed for override, global or per-class.
* Underscore -  FP (select, reduce), bind, template, deep isEqual, clone, tap
* $ - jQuery || Zepto

---
# Peek under the hood

* Sync
* Underscore
* $
* pushState

---
# Resources

---
# Get your code on

* [Todo App example](http://documentcloud.github.com/backbone/#examples-todos)
* [James Newbery's jasmine examples](https://github.com/froots/backbone-jasmine-examples/tree/master/public/javascripts)

---
# Further reading: Books on JavaScript

* [JavaScript: The Good Parts](http://shop.oreilly.com/product/9780596517748.do) by Douglas Crockford
* [JavaScript Web Applications](http://shop.oreilly.com/product/0636920018421.do) by Alex MacCaw (Spine.js author)
* [Test-Driven JavaScript Development](http://tddjs.com/) by Christian Johansen
* [JavaScript Patterns](http://shop.oreilly.com/product/9780596806767.do) by Stoyan Stefanov
* [JavaScript: The Definitive Guide](http://shop.oreilly.com/product/9780596805531.do) by David Flanagan

---
# Further reading: Online resources

* [Backbone on Rails eBook](http://workshops.thoughtbot.com/backbone-js-on-rails?utm_source=jm-talk)
* [Official Backbone docs](http://documentcloud.github.com/backbone/)
* [Annotated source code](http://documentcloud.github.com/backbone/docs/backbone.html)
* [Underscore docs](http://documentcloud.github.com/underscore/) and [source](http://documentcloud.github.com/underscore/docs/underscore.html)
* [Backbone Google Group](https://groups.google.com/group/backbonejs)
* [Peepcode episodes on Backbone](http://peepcode.com/products/backbone-js)

---
# Recap

* Client-side frameworks
* Moving parts of Backbone
* Example
* Code dive
* Bonus topics
* Resources

---
# Thanks!

* Me:
    * [jason.p.morrison@gmail.com](mailto:jason.p.morrison@gmail.com)
    * [http://twitter.com/jayunit](http://twitter.com/jayunit)
    * [http://jayunit.net](http://jayunit.net)
* Slides:
    * [View slides online](http://jayunit.net/backbone-js-on-rails-talk)
    * [View slides source on GitHub](http://github.com/jasonm/backbone-js-on-rails-talk)
* Code:
    * [View chat app source on GitHub](http://github.com/jasonm/chat_app)

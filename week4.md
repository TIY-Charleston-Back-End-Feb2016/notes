## Week 4 - Web apps

### Day 1

* Review assignment (libgdx - minicraft)
* Exercise (parse string, remove duplicate words, build new string)
* Review language features
  * Anonymous classes
    * We made one in the BrowserAndroid project
    * They let you extend a class and instantiate it all at once
    * Open the Zoo project and add alligator to the switch statement as an anonymous class
    * Create an AnonymousClassExample file
      * Extend `Reptile` in a separate class
      * Extend `Reptile` in an anonymous class
  * Anonymous functions (aka lambdas)
    * Create an AnonymousFunctionExample file
      * Run code in a separate method
      * Run code in a `Runnable`
      * Run code in an anonymous function
* HTTP
  * GET vs POST requests
* Create [HelloSpark](https://github.com/TIY-Charleston-Back-End-Feb2016/HelloSpark)
  * Create a new project and use the command line template
  * Project Structure -> Libraries -> Add [Spark](http://sparkjava.com/)
    * `com.sparkjava:spark-core:2.3`
  * Project Structure -> Modules -> New Folder...
    * Call it "resources" and mark it as such
  * Project Structure -> Libraries -> Add the Mustache library
    * `com.sparkjava:spark-template-mustache:2.3`
  * Create `resources/templates/index.html` and a GET route
  * Create `resources/templates/account.html` and a GET route
  * Add create account form to `index.html`
  * Create a POST route that saves the username into an object
  * Display the name on the account page

### Day 2

* Review assignment (spark - microblog)
* Review mustache
  * `String name;`
    * Welcome, {{name}}!
  * `ArrayList<String> names;`
    * {{#names}} {{.}} {{/names}}
  * `Message msg;`
    * {{#message}} {{text}} by {{username}} {{/message}}
  * `ArrayList<Message> messages;`
    * {{#messages}} {{text}} by {{username}} {{/messages}}
  * Conditional (truthy)
    * {{#name}}Welcome, {{name}}!{{/name}}
  * Conditional (falsey)
    * {{^name}}Please login.{{/name}}
* Add multi-user support to HelloSpark
  * Store users in `HashMap<String, User>`
* Cookies
  * The `Session` works by storing a cookie with a session ID
  * Cookies are small pieces of data sent from a web server
  * Browsers send them back each time they talk to the server afterwards
* Create [GameTracker](https://github.com/TIY-Charleston-Back-End-Feb2016/GameTracker)
  * Add the Spark and Mustache libraries
  * Create `resources/templates`
  * Create `resources/templates/home.html`
  * Create `/` route
  * Create `resources/templates/login.html`
  * Create `/login` route
  * Create `Game` and the `/create-game` route
  * Add games to the `home.html` template

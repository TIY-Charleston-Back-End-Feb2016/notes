## Week 3 - Graphical programs

### Day 1

* Review assignment (file I/O continued - countries)
* Forum
  * Refactor code into separate methods
* HelloWorld
  * Create `HashMap` that maps destination addresses to lists of `Email` objects
  * Word frequency in a sentence into a `HashMap<String, Integer>`
* Review last week's concepts
  * String formatting
  * Extending a class
  * Reading and writing files
  * Parsing and serializing JSON
  * Debugging and testing
* Interfaces
  * Sort an `ArrayList<String>` in JREPL using `Collections.sort`
  * In the HelloWorld project, sort `ArrayList<Person>` by implementing `Comparable`
  * Definition
    * A list of one or more methods that a class must have
    * Allows code to call methods on objects even if they don't know what those objects are
    * Used all the time in Java itself as well as libraries/frameworks

### Day 2

* Review assignment (review - people)
* Install [Scene Builder](http://www.oracle.com/technetwork/java/javase/downloads/javafxscenebuilder-1x-archive-2199384.html)
* Create a project
  * New Project -> JavaFX template
  * Run blank project
  * Look at the three files you start with
  * Edit Main.java to set the title and window size
  * Edit sample.fxml via Scene Builder
    * Make all buttons set min size to USE_PREF_SIZE
  * Edit Controller.java
    * Implement `Initializable`
    * Implement action/keyboard methods
    * Bring in controls using `@FXML`
* Create a [to-do desktop app](../projects/ToDoDesktop)
  * Create an `ObservableList`
  * Set the `ListView` to use it
  * Wire up the "Add", "Toggle", and "Remove" buttons
* Create a [web browser desktop app](../projects/BrowserDesktop)
  * Wire up the "Go" button
  * Allow hitting enter in URL textfield
  * Implement `ChangeListener` to update the URL textfield
  * Wire up the back and forward buttons

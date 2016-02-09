## Week 2 - Console programs

### Day 1

* Review assignment (dynamic data structures - ATM)
* Review
  * Arrays and classes
  * Methods
  * Control flow (if, while, for, throw)
  * ArrayLists and HashMaps
* Create a [ToDo](https://github.com/TIY-Charleston-Back-End-Feb2016/ToDo) project
* Jar files
  * File -> Project Structure...
  * Click "Artifacts" and then the plus button
  * JAR -> From modules with dependencies...
  * Choose the main class and click OK
  * Build -> Build Artifacts...

### Day 2

* Review assignment (review - inventory)
* HelloWorld project
  * Create `PersonFinder.java`
  * Start with some `Person` objects
  * Add them to an `ArrayList<Person>`
  * Search an `ArrayList<Person>` for someone with a particular name
* Use `System.out.printf` in the ToDo project
* Create a [Zoo project](../projects/Zoo)
  * Animal
    * Mammal
      * Dog
      * Human
    * Reptile
      * Alligator
      * Turtle
    * Bird
      * Hawk
      * Parrot
  * Add fields and init them in constructors to demonstrate inheriting fields
  * Override `toString` to demonstrate inheriting methods
* Text adventure
  * Use `System.out.printf` when possible
  * Add health and damage to `Player`
  * Create a `Player` constructor
  * Create an `Enemy` class
  * Create a `Character` class that they extend
  * Create a `battle` method in `Character`

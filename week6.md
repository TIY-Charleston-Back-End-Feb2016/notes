## Week 6 - Spring

### Day 1

* Create [HelloSpring](../projects/HelloSpring)
  * Create project from template
    * Go to [Spring Initializr](https://start.spring.io/)
    * Choose "Gradle Project"
    * Group is `com.theironyard` and artifact is `HelloSpring`
    * Click "Switch to the full version"
    * Check the following options:
      * Web
      * Mustache
      * DevTools
    * Download and unzip the project
    * Import into IntelliJ
    * Choose "Import project from external model" and select Gradle
    * Click Next and Finish
  * MVC
    * Model (SQL)
    * View (HTML)
    * Controller (Java)
  * Create `/person` route that returns HTML
    * `src/main/resources/templates/person.html`
    * `src/main/java/com/theironyard/HelloSpringController.java`
    * Add arguments for name, city and age, and use `@RequestParam` to set default values
  * Create `/person.json` route that returns JSON
    * `src/main/java/com/theironyard/Person.java`
    * `src/main/java/com/theironyard/HelloSpringJsonController.java`
    * Add arguments for name, city, and age, and use `@RequestParam` to set default values
  * Create `/` route that returns HTML
    * `src/main/resources/templates/home.html`
    * Add `home` method to `HelloSpringController`
    * Add `login` method to `HelloSpringController`
* Build JAR file
  * Click the Gradle tab on the right edge of the window
  * HelloSpring -> Tasks -> build -> build
  * It will be in `build/libs`

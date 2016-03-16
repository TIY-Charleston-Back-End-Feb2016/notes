## Week 7 - Spring

### Day 1

* Time
  * Old way: `java.util.Date` and `java.util.Calendar`
  * New way: `java.time.LocalDate` and `java.time.LocalDateTime`
  * Advantages of `java.time`
    * Sane API
    * Immutable
    * Supports ISO-8601
  * Create [CalendarSpring](https://github.com/TIY-Charleston-Back-End-Feb2016/CalendarSpring)
* Add paging support to the "Purchases" assignment
  * Change `CrudRepository` to `PagingAndSortingRepository`, and add `Pageable pageable` to the custom method
  * Make the `/` route take an `int page` that defaults to `"0"`
  * Create a `PageRequest` object and pass it into the query methods
  * Add `nextPage` to the model and add the "Next" link to `home.html`
  * Add `page` to the model and add the `page` param to the filter links
  * Add `category` to the model and add the `category` param to the "Next" link
  * Make custom methods return `Page<Purchase>` and use the return value to selectively show the "Next" link

### Day 2

* Topics
  * JSON API + AJAX
  * Uploading files
* Install [JSONView](https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc?hl=en) chrome extension
* Create [IronGram](../projects/IronGram)
  * Create project from template with the following options
    * Web
    * DevTools
    * JPA
    * H2
    * PostgreSQL
  * Create initial server-side code
    * Modify `application.properties`
      * `spring.datasource.url=jdbc:h2:./main`
      * `spring.jpa.generate-ddl=true`
      * `spring.jpa.hibernate.ddl-auto=none`
    * Create `IronGramController` with `@RestController`
    * Create `User` with `username` and `password`
    * Create `Photo` with `sender`, `recipient`, and `filename`
    * Create `UserRepository` and `PhotoRepository`
    * Copy `PasswordStorage.java` into project
    * In the controller, add the repositories and create the `/login`, `/logout`, and `/user` routes
  * Create public folder
    * Download [jQuery](http://jquery.com/download/) and move it into `public`
    * Create `public/index.html` with jquery included
    * Create login, logout, and upload forms
    * Create `main.js` and include it after jquery
    * In `main.js`, use `$.get("/user", getUser)` and conditionally show the forms based on the return data
  * Create upload route
    * In the controller, create the `/upload` route with a `MultipartFile` as the file argument
      * Read username from session and throw exception if null
      * Check content type and throw exception if it doesn't start with "image"
      * Use `File.createTempFile` and `FileOutputStream` to write to disk
      * Create `Photo` object
      * Throw exception if recipient is null
  * Show photos
    * Create `/photos` route
    * Add `$.get("/photos", getPhotos)` to `main.js`
    * Add a `setInterval` to `main.js` that gets the photos every 3 seconds

### Day 3

* Fork [AngularSpring](https://github.com/TIY-Charleston-Back-End-Feb2016/AngularSpring)
  * JS frameworks behave differently than standard HTML queries
    * They encode parameters with JSON rather than URL encoding
    * They sometimes use path variables to request a specific id
    * All routes pertaining to a given entity have the same name
  * Add the necessary routes to make the app work
* Create [AnonUpload](https://github.com/TIY-Charleston-Back-End-Feb2016/AnonUpload)
  * Create project structure
    * Create project from template with the following options
      * Web
      * DevTools
      * JPA
      * H2
      * PostgreSQL
  * Create client-side code
    * Create `public`
    * Create `public/index.html` and `public/main.js`
    * Copy jquery into `public`
  * Create server-side code
    * Modify `application.properties`
      * `spring.datasource.url=jdbc:h2:./main`
      * `spring.jpa.generate-ddl=true`
      * `spring.jpa.hibernate.ddl-auto=none`
    * Create `AnonFile`
    * Create `AnonFileRepository`
    * Create `AnonUploadController` with `@RestController`
    * Create a `/files` route
    * Create an `/upload` route

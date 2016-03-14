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

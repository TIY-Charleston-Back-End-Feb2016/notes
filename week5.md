## Week 5 - Databases

### Day 1

* Review assignment (spark - crud)
* Saving data to the disk
  * Serialize to JSON vs using a database
  * JSON files can't be updated incrementally
    * You must continuously serialize the entire `HashMap` and overwrite the file
  * Databases let you read/write small portions of the entire data at a time
* Relational databases
  * Organize information into tables with rows and columns
  * Use a language called SQL (Structured Query Language)
    * Developed by IBM in the 70s
  * Most common commands
    * `CREATE TABLE`
    * `INSERT`
    * `SELECT`
    * `UPDATE`
    * `DELETE`
  * Most common data types
    * `VARCHAR`
    * `BOOLEAN`
    * `INT`
    * `DOUBLE`
  * Player example
    * `CREATE TABLE players (name VARCHAR, is_alive BOOLEAN, score INT, health DOUBLE)`
* Embedded vs external databases (SQLite/H2 vs MySQL/PostgreSQL)
* Create [HelloDatabase](https://github.com/TIY-Charleston-Back-End-Feb2016/HelloDatabase)
  * Download and add [H2](http://www.h2database.com/html/main.html) JAR file to project
  * Work with the database directly (by running the JAR file from the Terminal tab)
    * Use `jdbc:h2:./main` as the JDBC URL
    * Make the user name blank
  * Work with the database from Java (by writing code in `Main.java`)
    * Create a `Connection`
      * `Connection conn = DriverManager.getConnection("jdbc:h2:./main")`
    * Create a `Statement`
    * When creating a table, you should use `CREATE TABLE IF NOT EXISTS`
    * When selecting, use the `executeQuery` method, loop over the `ResultSet`, and print each column
    * Update and delete before the select statement
    * Run `DROP TABLE players` at the end
    * Demonstrate injecting values into query after the `DELETE` statement
      * The bad way: `String.format("INSERT INTO players VALUES ('%s', true, 10, 90.5)", inputName)`
        * SQL injection: `', true, 0, 0); DROP TABLE players; --`
      * The good way: `PreparedStatement`
  * For both methods, execute the following commands
    * `CREATE TABLE players (name VARCHAR, is_alive BOOLEAN, score INT, health DOUBLE)`
    * `INSERT INTO players VALUES ('Alice', true, 10, 90.5)`
    * `INSERT INTO players VALUES ('Bob', true, 9, 95)`
    * `SELECT * FROM players`
    * `SELECT * FROM players WHERE name = 'Bob'`
    * `SELECT * FROM players WHERE health > 0`
    * `UPDATE players SET score=20 WHERE name='Alice'`
    * `SELECT * FROM players`
    * `DELETE FROM players WHERE name='Alice'`
    * `SELECT * FROM players`

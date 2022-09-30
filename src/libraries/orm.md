# ORM

**The gist**: build a library that makes it easy to read and create data in a database from objects in your code.

ORM stands for Object-Relational Mapping, and it's usually the glue between your application code and the database. So instead of writing SQL directly, `SELECT * FROM users WHERE email='foo@example.com' LIMIT 1`, and instantiating an object with that data, you'd use the ORM to do that. It might look something like `User.find_by(email: "foo@example.com")`, which would return an instance of the `User` class.

ORMs are great for a variety of reasons:

- Generally a friendlier API than the database underneath
- Can help protect your application from running harmful queries
- You can craft queries in the language you're working in
- Easier to mock and stub when testing

What database you use is up to. [SQLite](https://www.sqlite.org/index.html) is a small, portable SQL database that is great for developing against.

## Specs

- Ability to find a record by ID or a given table column
- Create an object or struct in the language that you can then work with
- Ability to update a database record
- Ability to delete a database record

## Concepts

- API design
- Databases

## Extra Credit

- Support additional queries
- Support advanced queries like multiple `WHERE` clauses
- Try to make your ORM usable with a different flavor of SQL and see if it works

## Examples

- [sequel](https://github.com/jeremyevans/sequel) — Ruby ORM
- [activerecord](https://github.com/rails/rails/tree/main/activerecord) — Rails ORM
- [prisma](https://www.prisma.io) — Node.js ORM
- [sqlalchemy](https://www.sqlalchemy.org) — Python ORM
- [diesel](https://diesel.rs) — Rust ORM
- [gorm](https://gorm.io) — Go ORM

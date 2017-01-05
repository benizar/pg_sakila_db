# pg_sakila_db

- [Introduction](#introduction)
  - [Postgres xtensions](#postgres-extensions)
  - [Contributing](#contributing)
- [Getting started](#getting-started)
  - [Install the extension](#install-the-extension)
  - [Dependencies](#dependencies)
- [Related projects](#relatedprojects)
- [TODOs](#todos)



# Introduction

PostgreSQL extension for deploying a port of the Sakila example database.


## Postgres Extensions

PostgreSQL is an object-relational database management system (ORDBMS) with an emphasis on extensibility and standards-compliance [[source](https://en.wikipedia.org/wiki/PostgreSQL)].

Apart from the PostgreSQL official documentation you can check the [PostgreSQL Extension Network](http://pgxn.org/) for additional information about extensions.


## Contributing

- Send a pull request with your awesome features and bug fixes
- Help users resolve their [issues](../../issues?q=is%3Aopen+is%3Aissue).



# Getting started

## Install the extension

To build pg_adm:

    make
    make install
    make installcheck

If you encounter an error such as:

    ERROR:  must be owner of database regression

You need to run the test suite using a super user, such as the default "postgres" super user:

    make installcheck PGUSER=postgres

If that doesn't work, for testing purposes you also can do:

    sudo -u postgres createuser -s $USER

Once the extension is installed, you can add it to a database. If you're running PostgreSQL 9.1.0 or greater, it's a simple as connecting to a database as a super user and running:

    CREATE EXTENSION pg_sakila_db;


## Dependencies

The `pg_sakila_db` extension depends on other postgres extensions. See the `pg_sakila_db.control` file.



# Related projects

- http://www.postgresqltutorial.com/ (Initial database is available here).
- http://pgfoundry.org/projects/dbsamples/
- https://github.com/devrimgunduz/pagila


# TODOs:

More data could be inserted for working with: 

- Spatial objects (PostGIS)
- Table partitioning
- Full text search
- Jsonb
- Etc




# Linux Server Configuration

This project is my attempt at completing the Linux Server Configuration project.  The application running on the web server presents a catalog of movie posters, searchable by Year, Genre, and Director.

Anyone can browse the catalog, but add/edit/delete functions are limited to those who log into the
app via Google Accounts.

Summary of configurations made:
* Root access disabled
* Grader account created on server and allowed sudo access
* Password access disabled
* SSH allowed on port 2200
* UFW enabled, allowing access on 2200 (ssh), 80 (http), and 123 (ntp)
* Postgresql installed and "poster" db created
* "www-data" role allowed to read/write to/from db for postgres account
* Apache installed with mod_wsgi and configured to serve myapp.wsgi on port 80
* Catalog project installed
* Folder permissions modified to allow add/delete to /static/img folder


### Usage


* The instance can be found at 18.237.111.102.  
* The ssh port is configured to 2200
* The web application can be found at stickandburn.com.


## Built With

* [Flask](http://flask.pocoo.org/) - The web framework used
* [SQLAlchemy](https://www.sqlalchemy.org/) - Sql toolkit and ORM
* [Python](https://www.python.org/) - Server code
* [Postgresql](https://www.postgresql.org/) - Database server
* [Apache](https://httpd.apache.org/) - Web server

## Authors

* **Bijan Marashi** - [bm6410](https://github.com/bm6410)

## Acknowledgments

* Thanks to Udacity for various bits of sample code
* Hero image photographed by Rob Laughter
* I would be nowhere at all without [Stack Overflow](stackoverflow.com)
* Thanks to [PurpleBooth](https://gist.github.com/PurpleBooth) for the README.md template
* This [post](http://flask.pocoo.org/docs/1.0/deploying/mod_wsgi/) helped me get mod_wsgi working


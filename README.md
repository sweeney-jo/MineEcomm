# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
* 

To get Heoku up and running:
In Gemfile
specify what version of ruby (2.4.0) using,
then set db for development and test to sqlite3
also set heroku production to postgress
lastly add the rails 12factor job for heroku
save Gemfile.

open datbase.yml (config)
becasue using postgress for production you can delete everything from production on
save datbase.yml
open terminal and run $bundle install --without production
this installs all gems in the gem file,
we run bundle install without production cause when you push to heroku, heroku bundle installs automatically

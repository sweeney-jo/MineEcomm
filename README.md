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

$git status
$git add .
$git commit - m "cooment"
etc.

pushing App to heroku
$ heroku login
-email
-password

create app in heroku

$ heroku apps:create mine-eccom

push the app to heroku

$ git push heroku master
generates website address which can be altered
https://mine-ecomm.herokuapp.com/ 
site is now working locally on c9 and also remotely on heroku

To push to github
create new repository in github

sets git origin to this url (can type origin instead of full url, set-url for windows otherwise add)

$git remote set-url origin https://github.com/sweeney-jo/MineEcomm.git


push repository to github
$git push -u origin master
-github username sweeney-jo
-password college01//password does not show up, enter it and press enter

add bootstrap gem to the gem file
save file
Gemfile tells rails what gems the app needs // to have all gems and dependency you need

 $bundle install
 
 local rail server needs to be restartd whenever new gem is added to the rails project
 
 $rails s -b $IP -p $PORT
 
 add CSS
 create bootstrap_custom.css.scss  /scss extends css funtionality
 in bootstrap_custom.css.scss 
 @import 'bootstrap';
 save file

Create home page html in home.html.erb
contents of the home.html.erb are rendered to the yield tag
home.html.erb only contains code that is within body tag
update git from this point

add javscript
-application.js
line 12 //= require bootstrap
save file

push to github

$git push origin master

push to heroku 
$git push heroku master 


add Stripe GemFile
-gem 'stripe', :git => 'https://github.com/stripe/stripe-ruby'

$bundle install
this installs all gems in the gem file,

copy stripe view to home.ntml.erb from https://stripe.com/docs/checkout/rails

copy route- resources :charges

copy test publish key from strpe api keys 
paste into data key = from copied vuew code inhime.html.erb

add charges_controller code
add sekret key

config/initializers save file strip.rb 
paste in congig code

 Figaro to securely configure App
 gem 'figaro
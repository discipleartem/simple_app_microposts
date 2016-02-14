== README

Building demo blog by railstutorial.ru   Chapter 10-11 (microposts)

http://railstutorial.ru/chapters/4_0/user-microposts#top

* Ruby version 2.1.2

* Rails version 4.2.4

* Ubuntu 14.04

* Database postgres


* Features:

-add countdown 140 simbols at assets/javascripts/static_pages.js (renamed from .coffee) and views/shared/_micropost_form.html add span.countdown
(http://jberczel.github.io/hartl-solutions-ch10/#step7)

- fix custom.scss by myself

* Bugs:

- fix bug at sample_data.rake (rake db:populate) - http://stackoverflow.com/questions/23749612/wrong-number-of-arguments-1-for-0-hartl-chapter-10-bundle-exec-rake-dbpopul


* Deployment from http://railstutorial.ru/chapters/4_0/a-demo-app#top

- default admin user is "admin@railstutorial.org" and "example@railstutorial.org"
                                            with password: "foobar"
      to change - look at lib/tasks/sample_data.rake
      need to reset db -> rake db:reset
      and do ->           rake db:populate  for gem 'faker' to fill a db with data

- find a admin user at rails console -> User.where(:admin => true)

- do ->   rake assets:precompile    for working styles
          git add .
          git commit -am 'deploy heroku'

- git push heroku master
- heroku run rake db:migrate --app gentle-refuge-13368
- heroku run rake db:populate --app gentle-refuge-13368   --> fill db


App at production - https://gentle-refuge-13368.herokuapp.com


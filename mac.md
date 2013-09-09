##Mac OSx##

Alright ,let's get you set-up with a web development environment on your mac.

__How to read this document:__

Everything that has a ">" in front of it is a command you need to run in your terminal.

Open the terminal by pressing command and then the spacebar. In the search box type terminal and open it.

__What you need:__

###Xcode###

You  most likeSearch in your applications and upgrade to the latest version, alternatively:
--> Get it from itunes: https://itunes.apple.com/us/app/xcode/id497799835?mt=12

*RVM
Install RVM and the latest versions of Ruby and Rails
> $ \curl -L https://get.rvm.io | bash -s stable --rails

Install a new default gemset so that you can use the Rails 3.2.13 version instead of Rails 4.0

--> http://strandcode.com/2013/07/11/ruby-version-manager-rvm-overview-for-rails-newbs/

*Homebrew

> ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"

*Postgres

> Lion and up come with this database installed, so you can check in the terminal with:
> psql --version

That said, we probably want to use the latest version of Postgres to develop applications. In the command line enter:

> brew install postgresql

--> Read through the output after the installation. Two things are important.

First, create the database by running the following in:
> initdb /usr/local/var/postgres

Then start the database by running the following:

> pg_ctl -D /usr/local/var/postgres -l /usr/local/var/postgres/server.log start

Tip: save that last line on a sticky note or in an email as a quick reference to re-start Postgres after you restart your computer later down the line.

--> the first 1:30 min of this video also give good instructions (don't worry about anything that happens after the 1:30 min mark): http://railscasts.com/episodes/342-migrating-to-postgresql



OTHER SOFTWARE AND ACCOUNTS YOU NEED:

*Sublime 

--> go to sublimetext.com and install the text editor: http://www.sublimetext.com/2

To get some handy shortcuts:

Make "subl ." work in terminal
--> https://gist.github.com/olivierlacan/1195304

*Git
Create and account on Github.com and create a new repository.

If you prefer to use a little graphical interface program:
--> http://mac.github.com/

*Heroku

Set-up a Heroku account on:  https://www.heroku.com/

*Amazon S3

We need an amazon developer account for some image storage space (this will cost you nothing):

--> http://aws.amazon.com/ Sign-up and create an account. Anything we'll do over the weekend will cost you nothing, so don't worry about your credit card being charged.
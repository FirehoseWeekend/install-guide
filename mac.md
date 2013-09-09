#Mac OSx#

Alright, let's get you set-up with a web development environment on your mac. We'll be using Ruby on Rails for the weekend.

__How to read this document:__

Everything that is in a little box is a command you need to run in your terminal. For example, if you see a box like the one below copy that line and paste it in your terminal:

> copy everything in here an paste it into the terminal

__Open the terminal__ by pressing command and then the spacebar. In the search box type terminal and open it by clicking on it.

##Stuff you need##

###Xcode###

You  most likely already have a version of Xcode on your maching. Search in your applications folder to double check, but it's best if you upgrade to the latest version:
--> Get it from itunes: https://itunes.apple.com/us/app/xcode/id497799835?mt=12


###RVM###
Why: It will help you manage all the different versions of Ruby and Rails and make your life easy. So get this one right, since it's kind of important.

Install RVM and the latest versions of Ruby and Rails (this next line goes into the terminal, remember):
> \curl -L https://get.rvm.io | bash -s stable --rails

Now we probably have Rails 4.0 installed. Check with:

> rails -v

Rails 4.0 is the latest version of Rails, which changed a few things on how a project is run. Since a lot more online help is available for Rails previous verion (3.2.13), we're going to use that version of Rails. Doing so will help you a lot when building any application after this weekend...especially if you're troubleshooting error messages (believe me I've been there).

Let's get you on Rails 3.2.13:

Install a new default gemset so that you can use the Rails 3.2.13 version instead of Rails 4.0

--> http://strandcode.com/2013/07/11/ruby-version-manager-rvm-overview-for-rails-newbs/

###Homebrew###

> ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"


###Git###
We'll be using Git and Github to do version control. Think of this a place where you story all your work in the cloud so you can share it with other people, save different revisions and do all kind of cool things. It's used by a lot of developers and by using it too, you're in the know.



###Postgres###
Why? This is our database that we'll be using to store our data in. 


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



##OTHER SOFTWARE AND ACCOUNTS YOU NEED:##

###Sublime###
Why? Sublime Text 2 is a great texteditor that has all the great features and is easy to use; plus we can use it for free. If you have another text editor that you prefer, no need to switch.

--> go to sublimetext.com and install the text editor: http://www.sublimetext.com/2

To get some handy shortcuts:

Make "subl ." work in terminal
--> https://gist.github.com/olivierlacan/1195304


###Github###
Create and account on www.Github.com and create a new repository.

If you prefer to use a little graphical interface program:
--> http://mac.github.com/

###Heroku###

Set-up a Heroku account on:  https://www.heroku.com/

###Amazon AWS services###

We need an amazon developer account for some image storage space on Amazons S3 service (this will cost you nothing):

--> http://aws.amazon.com/ Sign-up and create an account. Anything we'll do over the weekend will cost you nothing, so don't worry about your credit card being charged.


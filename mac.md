#Mac OSx#

Alright, let's get you set-up with a web development environment on your mac. This is going to be a bit of a process so reserve a few hours going through everything in this document. We'll be using Ruby on Rails for the weekend and have plenty of time during Friday night to help you with all your questions. 

Remember, setting everything up is one of the most difficult steps, so be patient with yourself and remember we're all feeling the same web developer pain/frustration from time to time. It's the same when riding a bike for the first time - falling will hurt, but with enough training it soon feels like magic!

If you have any trouble please leave a comment below this document so others can see your question and the solution as well. If all else fails, feel free to email me at marco@firehoseweekend.com and I do my best to get back to you in a flash.


__How to read this document:__

Everything that is in a little box is a command you need to run in your terminal. For example, if you see a box like the one below copy that line and paste it in your terminal:

``` 
copy everything in here an paste it into the terminal
```

__Open the terminal__ by pressing command and then the spacebar. In the search box type terminal and open it by clicking on it.

##Stuff you need##

###Xcode###

You  most likely already have a version of Xcode on your maching. Search in your applications folder to double check, but it's best if you upgrade to the latest version:
--> Get it from itunes: https://itunes.apple.com/us/app/xcode/id497799835?mt=12


###RVM###
Why: It will help you manage all the different versions of Ruby and Rails and make your life easy. So get this one right, since it's kind of important.

Install RVM and the latest versions of Ruby and Rails (this next line goes into the terminal, remember):

```
 \curl -L https://get.rvm.io | bash -s stable --rails
```

Now we probably have Rails 4.0 installed. Check with:

```
 rails -v
```

FYI: Rails 4.0 is the latest version of Rails, which changed a few things on how a project is run. Since a lot more online help is available for Rails previous verion (3.2.13), we're going to use that version of Rails. Doing so will help you a lot when building any application after this weekend...especially if you're troubleshooting error messages (believe me I've been there).

Let's get you set-up with Rails 3.2.13.

Install a new default gemset so that you can use the Rails 3.2.13 version instead of Rails 4.0

```
rvm gemset create Ruby1.9_Rails3.2.13
```
```
rvm gemset use Ruby1.9_Rails3.2.13 
```

Add the gems with:

```
gem install Ruby -v 1.9.3p448
```
```
gem install Rails -v 3.2.13
```
Now if you type:

```
ruby -v
```
you should get: Ruby 1.9.3

And if you type:
```
Rails -v
```
You should get: Rails 3.2.13

High five you're all set :)

--> For the super-motivated, more info can also be found here: http://strandcode.com/2013/07/11/ruby-version-manager-rvm-overview-for-rails-newbs/

###Homebrew###
Why? with homebrew you can install a lot of programs with a single command line. It will save you a lot of time.

```
 ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"
```

###Git###
We'll be using Git and Github to do version control. Think of this a place where you story all your work in the cloud so you can share it with other people, save different revisions and do all kind of cool things. It's used by a lot of developers and by using it too, you're in the know.



###Postgres###
Why? This is our database that we'll be using to store our data in. 

Lion and up come with this database installed, so you can check in the terminal with:
```
 psql --version
```

That said, we probably want to use the latest version of Postgres to develop applications. In the command line enter:

```
brew install postgresql
```

--> Read through the output after the installation. Two things are important.

First, create the database by running the following in:
```
initdb /usr/local/var/postgres
```

Then start the database by running the following:

```
 pg_ctl -D /usr/local/var/postgres -l /usr/local/var/postgres/server.log start
```

Tip: save that last line on a sticky note or in an email as a quick reference to re-start Postgres after you restart your computer later down the line.

--> the first 1:30 min of this video also give good, albeit high-speed, instructions (don't worry about anything that happens after the 1:30 min mark): http://railscasts.com/episodes/342-migrating-to-postgresql


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

GCC
====

Install [GCC](https://github.com/kennethreitz/osx-gcc-installer/downloads) 

Download the version that matches your version of Mac.  In the top menu click the apple, and then "About this Mac".  If it says Version `10.6.x` download the 10.6 version.  Otherwise download the 10.7-v2 file (use this one even if you're running a version beyond 10.7).

Run this file

###Homebrew###
Why? with homebrew you can install a lot of programs with a single command line. It will save you a lot of time.

```
 ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"
```

###Git###
We'll be using Git and Github to do version control. Think of this a place where you story all your work in the cloud so you can share it with other people, save different revisions and do all kind of cool things. It's used by a lot of developers and by using it too, you're in the know.

If you __need a break from the command line__ you can use the visual installer for git here:
http://git-scm.com/downloads

If you want to keep going with the command line type:

```
brew update
```
```
brew install git
```

We will set-up git so it connects to your github after you have your github account set up. If you don't know what that means right now, don't worry, just remember we have to come back to here and do a few more lines to make everything work.



### libksba ###

```
brew install libksba
```


###rbenv###
Why: It will help you manage all the different versions of Ruby and Rails and make your life easy. So get this one right, since it's kind of important.

Install rbenv and the latest versions of Ruby and Rails (this next line goes into the terminal, remember):



```
git clone https://github.com/sstephenson/rbenv.git ~/.rbenv
```


```
 echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile
```

```
echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
```


```
git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build
```

__Now open a new terminal window by pressing COMMAND+T__

```
rbenv install 2.0.0-p353
```


Now let's get you the rails version we're using for the weekend. Add the gems with:

```
gem install rails -v 4.0.0
```

```
rbenv rehash
```

And if you type:

```
rails -v
```

You should get: Rails 4.

Now open a new tab in the terminal (Command+t) and type in:

```
rails -v
```

Still shows "Rails 4.0? --> High five you're all set :)



###Postgres###
Why? This is our database that we'll be using to store our data in. 

Download and run the [installer](http://www.enterprisedb.com/products-services-training/pgdownload#osx)


Create a database user
---------------------


```
createuser -s -r postgres -h localhost
psql postgres
\password postgres
```

Then enter the password (and password confirmation) of: `password`.


The Postgres Rubygem
-----------

You need to install the Postgres gem.  There are one of two ways that will work for you.


**If you have installed XCode (outside this particular guide, but if you have been hacking with it on a different project: ** you need to install postgres with the proper paths setup.  To determine if you have XCode installed hit Cmd+[Space] and type 'XCode'  if you see XCode listed under Applications, this means this is for you [see this](http://i.imgur.com/VGLrHxO.png).  Otherwise skip to the other way.

```
ARCHFLAGS="-arch x86_64" gem install pg -- --with-pg-config=/Library/PostgreSQL/9.3/bin/pg_config
```

If you have not installed XCode (you did not do the above) run the following command to install the Postgres Rubygem

```
gem install pg
```


###Awesome! You're all done here!###

__--> Now get your software and accounts set-up [here](https://github.com/FirehoseWeekend/install-guide)__


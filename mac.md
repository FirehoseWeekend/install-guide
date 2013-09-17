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

###XCode###

You  most likely already have a version of Xcode on your maching. Search in your applications folder to double check, but it's best if you upgrade to the latest version:
--> Get it from itunes: https://itunes.apple.com/us/app/xcode/id497799835?mt=12

--> Read Step 1 of this tutorial for any trouble with XCode: http://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/


###XCode Command Line Tools###

Once you install XCode, you need to install the command line integration.  

* Press Command+[Space] to launch spotlight in the top right window
* Type `xcode` and press enter
* In the menu bar click `XCode>Preferences`
* Press the downloads tab in the top bar of the dialog (See [this](http://i.imgur.com/V0MnjNS.png) picture for a screenshot of this and the next step)
* Press the `Install` next to the "Command Line Tools" listing


###RVM###
Why: It will help you manage all the different versions of Ruby and Rails and make your life easy. So get this one right, since it's kind of important.

Install RVM and the latest versions of Ruby and Rails (this next line goes into the terminal, remember):

```
 \curl -L https://get.rvm.io | bash -s stable
```

Now, let's get you set-up with Rails 3.2.14.

Install a new default gemset so that you can use the Rails 3.2.14 version.

```
rvm gemset create firehose
```

Now let's make this gemset the default gemset. First run

```
rvm list
```
You should see a whole bunch of stuff and something like this:
```
ruby-2.0.0-p247 [ x86_64 ]
```
You need the "ruby-2.0.0-p247" part (or whatever your version is).

Now let's make your gemset the default. __Make sure you use your version of ruby from above__!!!

```
rvm use ruby-2.0.0-p247@firehose --default
```


Now let's get you the rails version we're using for the weekend. Add the gems with:

```
gem install rails -v 3.2.14

```

And if you type:
```
rails -v
```
You should get: Rails 3.2.14.

Now open a new tab in the terminal (Command+t) and type in:

```
rails -v
```

Still shows "Rails 3.2.14? --> High five you're all set :)

--> For the super-motivated, more info can also be found here: http://strandcode.com/2013/07/11/ruby-version-manager-rvm-overview-for-rails-newbs/

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

**THIS IS IMPORTANT**: After running that command look at the output of the command.  If you see an error that looks like this: `FATAL:  could not create shared memory segment`, you'll need to do some work.  If the output looks all successful you can continue to the section on `Start Up the Database`.

```
sudo /Applications/Xcode.app/Contents/MacOS/Xcode /etc/sysctl.conf
```

_When you start typing a message box will pop up. Click on the `Unlock` button._

In the file that opens up change the line that starts with: `kern.sysv.shmall`. To be `kern.sysv.shmall=65536`.  Change the line that starts with `kern.sysv.shmmax` to be: `kern.sysv.shmmax=16777216`

Hit command+s to save the file, and then command+q to quit.  Restart your machine.

When it comes back up verify it worked properly and when you run `sysctl kern.sysv.shmmax` it prints 16777216 and when you run `sysctl kern.sysv.shmall` it prints 65536.

After that run:

```
initdb /usr/local/var/postgres
```

again and make sure the `FATAL` error does not happen.

Start Up the Database
---------------------


Then start the database by running the following:

```
 pg_ctl -D /usr/local/var/postgres -l /usr/local/var/postgres/server.log start
```

Tip: save that last line on a sticky note or in an email as a quick reference to re-start Postgres after you restart your computer later down the line.

--> the first 1:30 min of this video also give good, albeit high-speed, instructions (don't worry about anything that happens after the 1:30 min mark): http://railscasts.com/episodes/342-migrating-to-postgresql


Create a database user
---------------------


```
createuser -s -r postgres
sudo -u postgres psql postgres
\password postgres
```

Then enter the password (and password confirmation) of: `password`.

###Awesome! You're all done here!###

__--> Now get your software and accounts set-up [here](https://github.com/FirehoseWeekend/install-guide)__


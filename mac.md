#Mac OSx#

__How to read this document:__

Everything that is in a little box is a command you need to run in your terminal. For example, if you see a box like the one below copy that line and paste it in your terminal:

``` 
copy everything in here an paste it into the terminal
```

__Open the terminal__ by pressing command and then the spacebar. In the search box type terminal and open it by clicking on it.

##Stuff you need##

###Homebrew###
Why? with homebrew you can install a lot of programs with a single command line. It will save you a lot of time.

```
ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"
```

###Git###


```
brew update
```
```
brew install git
```


### libksba ###

```
brew install libksba
```


###rbenv###

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

Now setup the default version of ruby

```
rbenv global 2.0.0-p353
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

Still shows "Rails 4.0? High five you're all set :)



###Postgres###

Download and run the [installer](http://www.enterprisedb.com/products-services-training/pgdownload#osx), and follow the directions when going through the installer.  It's important to follow the direction exactly as described below.

####Run the Installer####

* If you get the application was blocked, make it unblocked.  To do this ask ken or marco how.

* **Install Directory**: Leave this the default (/Library/PostgreSQL/9.3), and press Next >.
* **Data Directory**: Leave this the default (/Library/PostgreSQL/9.3/data), and press Next >.
* **When prompted for a password (and password confirmation) enter `password` for both.  **This is important.  Use the password of `password`.  This matters later**
* **Port**: Leave this the default `5432`.
* **Locale**: Leave the [Default locale] set and press Next >.
* Press Next > again.
* When prompted about *Stack Builder* after the install, uncheck the box, then press Finish.


####Setup and Test The Postgres Installation####

* Open the terminal and run this command:

```
echo -e "\nsource /Library/PostgreSQL/9.3/pg_env.sh" >> ~/.bash_profile && source ~/.bash_profile
```

* In the terminal run this command.  You will be prompted for a password.

```
psql --username postgres -h localhost --password
```

**When prompted for a password enter `password`**, and you should be prompted with something that looks like:

```
psql (9.3.2)
Type "help" for help.

postgres=# 
```

Press **CTRL+D** to change the `postgres=#` into the `$`.


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

### Sublime Text Editor

Now we're ready to install the text editor we'll be coding in:


**Enable Unsigned Developer Applications**

* Press command+[space] and type "System Preferences"
* Click Security and Privacy
* Press the lock button & enter your password
* Make sure the `Allow applications downloaded from:` is set to `Anywhere`[^](http://i.imgur.com/0HEcfmt.png).

**Install Sublime**

* Go to [Sublime Text Editor Download Page](http://www.sublimetext.com/2), and click on the OSX link.
* When the *.dmg file finishes downloading double click it
* Drag the "Sublime Text 2" icon into the "Applications" icon that is present in the popup[^](http://i.imgur.com/DuTTT71.png).

```
ln -s /Applications/Sublime\ Text\ 2.app/Contents/SharedSupport/bin/subl /usr/local/bin/sublime
open ~/.bash_profile
```

Add the following line to the bottom and save the file:

```
export PATH="/usr/bin/local:$PATH"
```

Now if you type `sublime` in the terminal, the sublime text editor should be launched.


### Accounts

Now follow the guide [here](https://github.com/FirehoseWeekend/install-guide/blob/master/accounts.md) to setup your web development accounts.



Additional Info
======

database.yml
------

We'll go over what this means Saturday.

This installer will install postgresql in such a way that you'll need to adjust your database.yml file to look like this in each of the three sections (development, test, production).  Also be sure to adjust the database section.  _NOTE: indentation is super important - make sure they line up and rather than copy & pasting this, type this in)_:

```
development:
  adapter: postgresql
  encoding: unicode
  database: YOUR_APPLICATION_NAME_HERE_development
  pool: 5
  username: postgres
  password: password
  host: localhost
```


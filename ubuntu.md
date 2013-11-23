Ubuntu Environment Install Guide
===================

Step 1 - Launch Terminal
----------

* Press the dash-home button on the sidebar [^](http://i.imgur.com/6Y16pS1.jpg).
* Begin typing the work `terminal` and then press the terminal icon [^](http://i.imgur.com/xU4rZSW.png).

Step 2 - Configure the Terminal
---------------

* Right click in the terminal window so a menu pops up
* In the menu click `Profiles>Profile Preferences` [^](http://i.imgur.com/RwbAyOK.png)
* Click the `Title and Command` tab.  (See [this](http://i.imgur.com/iioFIpF.png) screenshot for this and the next step)
* Check the `Run command as login shell` box
* Click the close button

Step 3 - Run a Series of Terminal Commands
-----------

_NOTE: Anything in the format below should be typed into the terminal application exactly as presented._

```
This indicates text that should be entered into terminal
```

* Install Curl

```
sudo apt-get install curl
```

* Install rvm

```
curl -L https://get.rvm.io | bash -s stable
source ~/.bash_profile
rvm install 2.0.0
rvm use 2.0.0
rvm gemset use 2.0.0@firehose --default --create
```

* Install git

```
sudo apt-get install git-core
```

* Install Rails

```
gem install rails -v 4.0.1
```

* Install Postgres

```
sudo apt-get install postgresql postgresql-contrib libpq-dev
```


** Configure Postgres User Account **

```
sudo -u postgres psql postgres
\password postgres
```

When prompted for a password (and a confirmation) enter: `password`.

Press ctrl+d to close the postgres console.

* Install NodeJS

```
sudo apt-get install node
```


** Install Nokogiri RubyGem **

Nokogiri is a rubygem that we need and it requires certain packages to be installed.  To install those packages and make sure the gem can be installed run these commands:

```
sudo apt-get install ruby1.8-dev ruby1.8 ri1.8 rdoc1.8 irb1.8 libreadline-ruby1.8 libruby1.8 libopenssl-ruby libxslt-dev libxml2-dev libxslt1-dev libxml2-dev
gem install nokogiri
```

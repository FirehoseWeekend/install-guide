Ubuntu Environment Install Guide
===================

Step 1 - Launch Terminal
----------

* Press the dash-home button on the sidebar [^](http://i.imgur.com/6Y16pS1.jpg).
* Begin typing the work `terminal` and then press the terminal icon [^](http://i.imgur.com/xU4rZSW.png).

Step 2 - Run a Series of Terminal Commands
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
```

* Install git

```
sudo apt-get install git-core
```

* Install Rails

```
gem install rails -v 3.2.14
```

* Install Postgres

```
sudo apt-get install postgresql
```

* Install NodeJS

```
sudo apt-get install node
```

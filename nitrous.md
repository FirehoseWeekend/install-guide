Web Development Setup with Nitrous
==================

This will run you through the steps to configure your web development environment using the nitrous.io install process.


Step 1: Create accounts if you haven't already
--------

**Note:** These websites may ask you if you want to also download the software programs to go along with the accounts (The Heroku ToolBelt, GitHub for Windows, or GitHub for Mac).  We won't be using these programs so you won't need to download them.

### Part A

First go to [GitHub.com](http://github.com) and create an account.

### Part B

Then go to [Heroku.com](http://Heroku.com) and create an account there as well.

Step 2: Create a Nitrous.io Account & Environment
-----------------

### Part A

First go to [Nitrous.io](https://www.nitrous.io/) and create an account.

### Part B

Check your email and confirm your account by clicking the link that is
emails to you in the nitrous sign up flow.

### Part C

Click the Green "Open Dashboard" button

http://monosnap.com/image/gyeffOLKJiWsVRpouBVKqNMWrnR29K


### Part D

Create a ruby-on rails box.

* Make sure the "Ruby/Rails" logo is colored:

http://take.ms/E4LVI

* For name enter "Firehose"
* For region enter "US West"
* Leave "Download a GitHub repo" blank
* Press the orange "Create Box" button.

http://take.ms/Wny00

### Part E

Wait a few moments until you see "firehose is running" with a green icon on the page the gets displayed:

http://take.ms/ddcKG

### Part F

Press the orange "Next" button:

http://take.ms/O2y8m

### Part G

Scroll to the bottom of the page and press the orange "Okay, Take Me to my Box!" button:

http://take.ms/JI7TP

Then your coding environment will load up in the browser.


Install your database


Step 3 - Install Your Database
-------

### Part A

Click the bottom part of the window, where you see the dollar sign:

http://monosnap.com/image/sATBzBzvU3LE5POYxla4oWaBoyRLDh

### Part B

Type this (or copy & paste it), exactly like this right after the dollar
sign:

```
parts install postgresql
```

Once you get the dollar sign displayed again continue to Part C
(make sure there are no error messages).

### Part C

Type this (or copy & paste it), exactly like this right after the dollar
sign:

```
parts start postgresql
```

Once you get the dollar sign displayed again continue to the next step
(make sure there are no error messages).



Step 4: Accounts
------------

First a little about passwords: Read all of this
------------------

Sometimes you will be prompted for a password (your computer login password, user account, etc.) when you're installing programs using the terminal window.  When you start typing the password, it will look like it nothing has been typed (eg. nothing will display on the screen as type).  That's totally fine. Your password is being entered, just not shown to you. So keep typing and press enter when you're done typing.  In case you type your password wrong it will prompt you to type in your password again.  Why? So nobody can look over your shoulder and see your password or know how many characters your password has.


#### Configure Heroku with SSH Keys

In the window with the dollar sign, run this command (this will prompt
you for your **heroku email address** and password.  When it prompts you for
that, enter that here):

```
heroku login
```

Make sure it displays: "Authentication successful.", and when you
see that go onto the next command to run:

```
heroku keys:add
```
 
#### Configure Github with SSH Keys

In the window with the dollar sign, run this command.

**NOTE:** this will take a while (it hung for 18 minutes for me so hang in there and wait until it says "Successfully installed nokogiri-1.6.1")

```
gem install nokogiri                                                                                            
```

In the window with the dollar sign, run this command.


```
gem install github_api
```


In the window with the dollar sign, run this command (this will prompt
you for your **GitHub username** and password (note, this isn't your GitHub email address).  When it prompts you for
that, enter that here):

```
curl "https://raw.githubusercontent.com/FirehoseWeekend/install-guide/master/nitrous_github.rb" > ~/.firehose-github.rb && ruby ~/.firehose-github.rb
```

Then adjust these to have your name and email address inside the double quotes:

```
git config --global user.email "you@example.com"
```
```
git config --global user.name "Your Name"
```

##Amazon AWS services##

_We need an amazon developer account for some image storage space on Amazons S3 service (this will cost you nothing)_

* Sign-up and create an account for [Amazon Web Services](http://aws.amazon.com/). Anything we'll do over the weekend will cost you nothing, so don't worry about your credit card being charged.

 
Step 7: Test - Ask Marco and Ken for help
---------
 
We'll run by make sure your machine is up to snuf.


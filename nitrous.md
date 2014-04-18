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

![open-dashboard](http://i.imgur.com/oNINElt.png)


### Part D

Create a ruby-on rails box.

* Make sure the "Ruby/Rails" logo is colored:

![rails-is-selected](http://i.imgur.com/LYLHXg3.png)

* For name enter "Firehose"
* For region enter "US West"
* Leave "Download a GitHub repo" blank
* Press the orange "Create Box" button.

![push-create-box](http://i.imgur.com/KPMhIct.png)

### Part E

Wait a few moments until you see "firehose is running" with a green icon on the page the gets displayed:

![firehose-is-running](http://i.imgur.com/8xaMPmi.png)

### Part F

Press the orange "Next" button:

![press-next](http://i.imgur.com/HynaHgL.png)

### Part G

Scroll to the bottom of the page and press the orange "Okay, Take Me to my Box!" button:

![ok-takeme-to-my-box](http://i.imgur.com/MYp1hIk.png)

Then your coding environment will load up in the browser.


Install your database


Step 3: Install Your Database
-------

### Part A

Click the bottom part of the window, where you see the dollar sign:

![click-in-the-terminal](http://i.imgur.com/jdhKdV8.png)

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

**NOTE:** this will take a while (it hung for ~18 minutes for me so hang in there and wait until it says "Successfully installed nokogiri-1.6.1")

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
curl "https://raw.githubusercontent.com/FirehoseWeekend/install-guide/master/nitrous_github_action.rb" > ~/.firehose-github.rb && ruby ~/.firehose-github.rb
```

If you see it say "ok!" continue to the next step.

### Setup git

Then adjust these to have your name and email address inside the double quotes:

```
git config --global user.email "you@example.com"
```
```
git config --global user.name "Your Name"
```

 
Step 5: Have your machine checked
---------
 
Put your hand up and ask for Marco and Ken to help you out and test that your web development environment is properly setup.



Additional Info
----------

Information about how the database is setup is located [here](nitrous-database.md) - Marco & Ken will go over what this means later in the workshop.

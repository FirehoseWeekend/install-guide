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



Step 6: Accounts
------------

#### Configure Heroku with SSH Keys
 
This will prompt you for your heroku username and password.  Enter that here.

```
heroku login
```
```
heroku keys:add
```
 
#### Configure Github with SSH Keys
 
```
curl "https://raw2.github.com/kenmazaika/firehose-vagrant/master/github-key.rb" > ~/.firehose-github.rb && ruby ~/.firehose-github.rb
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

 
Step 7: Test
---------
 
 In the web development terminal window,  where it says `[Web Dev]` in blue, run this, _important note: after you run `rails s` it won't give you the prompt to continue to enter commands. This is by design, so move onto the next step even if it looks like it's just hanging_:

```
cd /vagrant/src/firehose-test-app
```
```
rails s
```


Open a web browser on your windows machine and go to: [http://127.0.0.1:3030](http://127.0.0.1:3030)

If you want to return to a window where you can enter commands in web development terminal window, go into it and hold CTRL+C.  This will stop your webpage from working, but allow you to enter new commands.



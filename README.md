Firehose Weekend Environment Install Guide
---------------

There are a few different options you have to install your web development environment.

### [Vagrant Install](https://github.com/kenmazaika/firehose-vagrant)

**Supports**: _Windows, Mac OS_

This will setup your web development environment using a tool called Vagrant.  

**In short**: this method will allow you to run with a pre-installed web development environment once you install a couple of programs.  Once you're up and running all you'll need to do is run a few commands to be ready for web development.

If you're curious to learn more, you can read up on the nitty-gritty details about Vagrant [here](http://www.vagrantup.com/) (entirely optional).

**This process is the fastest, and the easiest**.

### [Boxen Install](http://github.com/kenmazaika/firehose-boxen)

**Supports**: _Mac OS 10.8 and Mac OS 10.9_

This will setup your web development environment using a tool called Boxen.  

**A note about verions**: Unfortunately the seamless process only works with 10.8 or 10.9 Macs (Mountain Lion or Mavericks).  To check what OS X version you're running, go to the top-left menu and click on the Apple icon.  Then click "About this Mac".  Under OS X, it will show you the version.  This may or may not work with versions of Mac 10.7 and below, that already have XCode Command Line tools installed.  Installing XCode command line tools on these macs however will take around 3 gigabytes of packages, and you're probably better off just upgrading to your latest operating system instead.

**In short**: this method will automatically run your machine through the install process.  It's a lot like the manual process, but instead of actually running through a lot of the steps, there is a program, called boxen, that will run through many of the steps for you.

If you're curious to learn more, you read up on the nitty-gritty details about Boxen [here](http://boxen.github.com/), or the tool Puppet that allows boxen to work [here](http://puppetlabs.com/puppet/what-is-puppet) (entirely optional).

**This process is a little longer than the vagrant process, and a little bit harder**.


### [Manual Process](manual.md)
**Supports**: _Windows, Mac OS, and Ubuntu_  

**In short**: you can manually install all the programs that you'll need to on your machine.

This will give you fine grained control since you'll be installing everything by hand.  This should be used as a fall-back if either the Vagrant or Boxen installs are not possible.

**This process is the hardest to complete, and will take the longest**.

<br /><br />

---------------------------------------

### A Quick Rundown of the Tools (optional read for the curious)

You'll be installing the same tools, regardless of the method of installation you use.  We'll be going over the details of all these tools over the course, but if you want a quick primer, here's what's getting loaded on your machine.  Keep in mind, the goal of Install Night isn't get understand the details of the packages you're installing, just getting your machine into a state where you are ready to start writing code right away.

#### Software Installed

* **Ruby**:  This will allow you to run ruby code, and is needed to build ruby on rails applications
* **rbenv**:  This is a tool that will help us run ruby, and also will allow us to run multiple versions of ruby on the same machine.
* **PostgreSQL**:  This will be a place where we can store and change user generated data in our web application
* **Sublime Text Editor**:  This will allow us to 
* **SSH Keys**:  These are a lot like passwords that will live on your computer.  These passwords will allow your computer to talk to different web services out there.

#### Accounts Setup)

* **GitHub**: this will be a place where we can backup and collaborate on our code
* **Heroku** will make it possible to put our application live on the internet
* **Amazon Web Services**: we'll be storing images on S3, it's a lot like DropBox, except designed to be used by web-apps rather than people.



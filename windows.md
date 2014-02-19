Windows Environment Install Guide
===================

In order to have a well supported environment, with a large community if you are running a Windows machine, we encourage you to setup a linux Virtual Machine on your computer.  This guide will run you through how to setup the virtual environment.


Step 1 - Install VirtualBox
-------------
* Download and install the latest version of [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
* Launch the VirtualBox application.



Step 2 - Create a Virtual Environment
------------
* Press the _New_ button[^](http://i.imgur.com/ILPgFTk.png).  
* Enter `Firehose Rails Env` for the name, `Linux` for the type, and `Ubuntu` for the version and press the continue button in the bottom right[^](http://i.imgur.com/xnN2eDJ.png). 
* Enter `1024` mb for the Memory Size and press the continue button [^](http://i.imgur.com/UOopcQ0.png).
* Press the _Create_ button[^](http://i.imgur.com/kWI3QsU.png).
* Press _Continue_ at the hard drive creation dialog[^](http://i.imgur.com/smSASxl.png).
* Press _Continue_ at the storage page[^](http://i.imgur.com/zY9pgzh.png).
* Press the _Create_ button on the location size dialog[^](http://i.imgur.com/bJSaNGq.png).


Step 3 - Install and Configure Ubuntu on the Virtual Environment
-------------
* Download Ubuntu 12.04 LTS or copy the file from a local harddrive.  You can download it [here](http://www.ubuntu.com/download/desktop) as the 32-bit option [^](http://i.imgur.com/jY9aLmh.png).
* Click the _Not Now_ link[^](http://i.imgur.com/86ezhPg.png).
* In VirtualBox, press the _Start_ button[^](http://i.imgur.com/wTNjoWM.png).
* Press the _Select File_ button on the Select start-up disk dialog[^](http://i.imgur.com/HT29BD0.jpg).
* Select the ubuntu iso file you just obtained and press the open button[^](http://i.imgur.com/lWlMSOq.jpg).
* Press the _Start_ button[^](http://i.imgur.com/U9boNKt.jpg).
* Wait while a number of screens load
* Press _Install Ubuntu_[^](http://i.imgur.com/RdZWa6b.jpg).
* Check the _Install this third-party software_ box, and press continue [^](http://i.imgur.com/se6mPVs.png).
* Press continue on the Erase disk and install Ubuntu dialog[^](http://i.imgur.com/AJG7N0U.jpg).
* Press _Install Now_[^](http://i.imgur.com/P9xvhGz.jpg).
* Press _Continue_[^](http://i.imgur.com/b7K1U89.jpg).
* Press _Continue_[^](http://i.imgur.com/R2CLzu2.jpg).
* Enter your desired user profile information[^](http://i.imgur.com/oxHLbj1.jpg).
* Wait for the install to complete
* Press _Restart Now_[^](http://i.imgur.com/3pXtmQw.png).
* Press _ENTER_[^](http://i.imgur.com/Njfw5tr.png).
* When the machine restarts in VirtualBox select Devises > Install Guest Additions[^](http://i.imgur.com/HBMMlWQ.jpg).
* Press enter, supply password if requested, and then restart your virtual environment.

Step 4 - Install Linux Packages
-------------
Now that you have Ubuntu running in a virtual environment, you can follow the guide for [Ubuntu Environment Install Guide](ubuntu.md) inside this virtual environment that is setup.






Additional Info
======


Does VirtualBox fail to launch ubuntu?
------------

**ONLY READ THIS IF YOU'RE GETTING ERRORS**

* In a small number of cases, you may need to either use [VirtualBox 3.1.8](http://download.virtualbox.org/virtualbox/3.1.8/VirtualBox-3.1.8-61349-Win.exe) rather than latest one, or make some changes to your BIOS to allow you to use the latest version.  In these cases you'll need to first completely uninstall VirtualBox and then install the old version.  __You'll only want to do this if you're sure the latest version isn't going to work for you__.

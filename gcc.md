Install Web Development Environment Without XCode
========

__Please read through each sentence before you act on it or anything before it__.  Since you're not installing this on a standard install, you'll need to be extra dilligent about installing this!


Step 1 (Install the GCC toolkit - these are the parts of XCode you need):
-------
* Determine what version of OSx you're running.  To do this click on the Apple Button in the top left corner of the menu bar and press "About this Mac".  A dialog box should pop up and tell you, you are using OSX 10.x.y.  Remember this version.
* Download and run the GCC compiler from [here](https://github.com/kennethreitz/osx-gcc-installer/downloads).  Go under 'downloads' to find it. Make sure the version of the installer you grab matches the version of OSx you saw in the previous step. 
* In the standard install guide skip ahead to the __Homebrew__ section and follow that step.
* Install libksba by running the following command:

```
brew install libksba
```

* Install git by runing the following command:

```
brew install git
```

Next Step
---------

If you're running 10.7.x you can go back to the previous install guide and continue by starting the section that is labeled "RVM".  If you're running 10.6.x, you'll need to go to Step 2 in the below section.

Step 2 (Install Ruby through rbenv instead of RVM)
--------

__Only do this if you're running 10.6x__

* Install [rbenv](https://github.com/sstephenson/rbenv) (Instead of RVM)
* Install [ruby-build](https://github.com/sstephenson/ruby-build)
* Install ruby 2.0.0

```
rbenv install 2.0.0-p247
```

Now skip ahead to the part in the docs where it says "Now let's get you the rails version we're using".

After running "gem install rails -v [version number]" you'll need to run `rbenv rehash`.

Skip installing git, and homebrew for the docs that exist, because we've already done that.




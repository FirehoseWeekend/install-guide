Sublime Text Editor
===================

Why? Sublime Text 2 is a great texteditor that has all the great features and is easy to use; plus we can use it for free. If you have another text editor that you prefer, no need to switch.

Mac Guide
---------

** Enable Unsigned Developer Applications **

* Press command+[space] and type "System Preferences"
* Click Security and Privacy
* Press the lock button & enter your password
* Make sure the `Allow applications downloaded from:` is set to `Anywhere`[^](http://i.imgur.com/0HEcfmt.png).

** Install Sublime **

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



Ubuntu Guide
-------------

```
sudo add-apt-repository ppa:webupd8team/sublime-text-2
sudo apt-get update
sudo apt-get install sublime-text
sudo ln -s /usr/bin/subl /usr/bin/sublime
```

Now if you type `sublime` in the terminal, it should launch your sublime text editor.


###Github###

* Create and account on [github.com](http://www.github.com) and create a new repository.
* Setup your SSH key and connect it to GitHub
  * On a Mac follow [these](https://github.com/FirehoseWeekend/install-guide/blob/new-version/mac-ssh.md) steps
  * Otherwise follow the Ubuntu steps in your virtual environment [here](https://help.github.com/articles/generating-ssh-keys#platform-linux)

###Heroku###

* Set-up a Heroku account on:  [heroku.com](https://www.heroku.com/)
* Install the heroku tool kit, by running the installer you get [here](https://toolbelt.heroku.com/) 

* Add your SSH key to your account by doing the following:
  * Log into heroku.com
  * Click `Dashboard` in the top right
  * Click on the ninja guy in the top right corner, to expand a menu
  * Click on `Account` that pops up.
  * Click on the `Add new SSH key...` textbox that you see
  * Go into the terminal run this command to output your SSH key to the screen `cat ~/.ssh/id_rsa.pub`
  * Copy everything from `ssh-rsa` to your email address.  Make sure to copy this whole thing (including the `ssh-rsa` and your email address).
  * Paste it into the `Add new SSH key...` textbox on the heroku.com website
  * Press the `Add Key` button.
  * Green text should pop up at the top telling you it did that successfully.

###Amazon AWS services###

_We need an amazon developer account for some image storage space on Amazons S3 service (this will cost you nothing)_

* Sign-up and create an account for [Amazon Web Services](http://aws.amazon.com/). Anything we'll do over the weekend will cost you nothing, so don't worry about your credit card being charged.

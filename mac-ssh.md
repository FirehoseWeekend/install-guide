Step 1 - Check for SSH Keys
------------


Run the following command to check for an SSH key:

```
ls ~/.ssh
```

If you see "No such file or directory" go to step 2.  If you see "id_rsa" in the output, jump to step 3 (you already have an SSH key - basically a password file - on your machine)

Step 2 - Generate SSH Key
------------

**MAKE SURE TO CHANGE THE EMAIL ADDRESS IN THE BELOW STEP TO BE YOUR ACTUAL EMAIL ADDRESS**

```
ssh-keygen -t rsa -C "your_email@example.com"
```

**THIS WILL PROMPT YOU THAT**

`Enter file in which to save the key (/Users/you/.ssh/id_rsa):`

**LEAVE THIS BLANK AND PRESS THE ENTER KEY**

Then it will prompt you:

`Enter passphrase (empty for no passphrase):` **LEAVE THIS BLANK AND PRESS ENTER**.  Then it will prompt you for:

`Enter same passphrase again:` **ALSO LEAVE THIS BLANK**


```
ssh-add ~/.ssh/id_rsa
```

Step 3 - Add your SSH key to GitHub
-------------------


Run the following code to copy the key to your clipboard.

```
pbcopy < ~/.ssh/id_rsa.pub
```


1. Go to your [Account Settings](https://github.com/settings) in GitHub.com
2. Click [SSH Keys](https://github.com/settings/ssh) in the left sidebar
3. Click "Add SSH key"
4. Paste your key into the "Key" field.  This text should start with `ssh-rsa` and end with your email address. 
5. Click "Add key"
6. Confirm the action by entering your GitHub password.

Step 4 - Test everything out
--------

To make sure everything is working you'll now SSH to GitHub. When you do this, you will be asked to authenticate this action using your password, which for this purpose is the passphrase you created earlier. Don't change the `git@github.com` part. That's supposed to be there.

```
ssh -T git@github.com
# Attempts to ssh to github
```

You may see this warning:

```
The authenticity of host 'github.com (207.97.227.239)' can't be established.
# RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48.
# Are you sure you want to continue connecting (yes/no)?
```


Don't worry, this is supposed to happen. Verify that the fingerprint matches the one here and type "yes".

```
Hi username! You've successfully authenticated, but GitHub does not
# provide shell access.
```

If that username is correct, you've successfully set up your SSH key. Don't worry about the shell access thing, you don't want that anyway.



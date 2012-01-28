drsync
=======
Syncs a remote Drupal site to your local instance via ```rsync``` and ```ssh```. Uses password authentication -- password is saved locally but encrypted. This script is meant to be used on unfortunate servers without ```ssh``` key authentication support.

Installation/Update
-------------------
Run these commands:

```
curl https://raw.github.com/jtse/drsync/master/drsync > drsync
chmod 755 drsync
sudo mv drsync /usr/local/bin
```

Usage/Configuration
-------------------
Go to your project folder and run:

```
drsync
```

Or to SSH into the sync host: 

```
drsync ssh
```

Advanced Usage
--------------
Review the generated ```.drsync``` file.

Requirements
------------
The following commands must be present on both the remote and local machine:

```
drush
bash
ssh
rsync
openssl (for local password encryption/decryption)
```

Of course, you need a running instance of Drupal.

Limitations
-----------
* Does not support ```ssh``` key authentication -- you should be using ```drush rsync``` if key authentication is available.
* Does not support multisite (TODO) -- only syncs default/files

Security
--------
The security is only a notch better than storing your passwords in plain-text files.

The passwords are encrypted as follows:

* Passwords are saved into individual files in $HOME/.drsync/pass 
* Password filenames are a hash of the working directory, ssh user, and ssh host
* Passwords are encrypted with the decryption key as a hash of the working directory and current user name

Essentially, a cracker with knowledge of openssl encrypt/decrypt commands can steal your passwords if he or she has access to your $HOME/.drsync directory AND the directories of your Drupal projects.

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

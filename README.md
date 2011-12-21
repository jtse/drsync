drsync
=======
Syncs remote to local Drupal site via ```rsync``` and ```ssh```. Uses password authentication -- password is saved locally but encrypted. Script is meant to be used on servers without ```ssh``` key authentication.

Installation/Update
-------------------
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
The following must be present on both the remote and local machine:

```
drush
bash
ssh
rsync
```

Limitations
-----------
* Does not support ssh key authentication -- only password authentication. Use ```drush rsync``` if you need key support.
* Does not support multisite (TODO) -- only syncs default/files

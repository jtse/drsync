drsync
=======
Drupal remote sync script. Bash script for synchronizing remote Drupal to local Drupal instances. The script builds upon the shoulders of giants such as ssh, rsync, and drush to efficiently synchronizes Drupal database and files.

Installation/Update
--------------------
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
* Does not support ssh key authentication (TODO) -- only password authentication
* Does not support multisite (TODO) -- only syncs default/files

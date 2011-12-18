drsync
=======
Drupal remote sync script. Bash script that synchronizes a remote Drupal instance to a local Drupal instance. The script builds upon the shoulders of giants such as ssh, rsync, and drush to efficiently synchronize between Drupal instances.

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

drsync
=======
Drupal remote sync script. Bash script for synchronizing a remote Drupal to local Drupal instances.

Installation/Update
--------------------
```
curl https://raw.github.com/jtse/drsync/master/drsync > drsync
chmod 755 drsync
sudo mv drsync /usr/local/bin

```

Usage
-----
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


drsync
=======
Drupal sync scripts. Bash scripts for synchronizing a remote-to-local Drupal instances.

Installation/Update
--------------------
```
curl https://raw.github.com/jtse/drsync/master/drsync > drsync
chmod 755 drsync
sudo mv drsync /usr/local/bin

```

Usage
------
Go to your project folder and run
```
drsync
```

Requirements
------------
The following commands must be present on both the remote and local machine
```
drush
bash
ssh
rsync
```

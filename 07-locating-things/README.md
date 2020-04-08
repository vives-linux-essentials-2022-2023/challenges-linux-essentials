# Chapter 07 - Locating Things

Document all the commands and their output on your system. If the output is too long take a couple of lines and add `...` at the end.

## Locate

Install the `locate` command and update the index database.

Now locate the following files on your system:

* `sudoers.dist`
* the configuration file `ssh_config`
* `auth.log`

## Whereis

**What is the location of the man-pages of `python`?**

**Where are the binaries of `find` located?**

## Which

What is the location of the following commands for the current user:

* `passwd`
* `locate`
* `code`
* `fdisk`

## Find

Make sure to redirect the `permission denied` errors to `/dev/null` for all searches unless specified otherwise.

**Find the file `boot.log`.**

**Find the files `.bashrc`.**

**Do a system-wide search for files that contain the keyword `secret`.**

**Search for files that end with the extension `.conf` and contain a filename with the keyword `system` in the `/etc` directory.**

**What option can we use on `find` the make sure the current user can read the file? Don't use the `-perm` option. There is a better option. Give a nice example.**

**Find all log files in `/var/log` that were modified in the last 24 hours. Make sure to only include files and not directories. Now extend the command to perform a long listing human readable `ls` for each file.**

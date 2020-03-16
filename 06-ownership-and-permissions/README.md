# Chapter 06 - Ownership and Permissions

Make sure to document all your commands here. Provide prove using screenshots or terminal output or alike.

Unless specified otherwise, all commands should be executed in a terminal session logged in with your own user account.

Make sure to create a snapshot of your virtual machine before starting these challenges. If you mess up something serious you can always roll back to this snapshot.

## Sudo

Open a terminal session with your current user. Execute the `id` command. Explain the output. To what groups does your user belong?

Next execute the `id` command prefixed with `sudo`. What is the difference between both commands. What is happening here?

## New User Davy

Create a user account for `davy`. Place a screenshot of the process here.

Now open a terminal and switch to the user account using the command `su davy`. Take a screenshot of the terminal.

Create a file called `i_am_legend` inside of the home dir of `davy` using the `davy` session using the command `sudo touch ~/i_am_legend`. Why is this not working?

`exit` the current shell of `davy`.

Add the user account `davy` to the group `sudo`. Now repeat the process. Is it working now? Take a screenshot.

`exit` the current shell of `davy`.

Now switch to the superuser using `sudo su`.

Now execute the `su davy` command from the superuser session. Take a screenshot of the terminal. Why do we not need to provide the password of `davy`?

## Auth.log

What does the file `/log/var/auth.log` track? Provide an example that shows entries being added to the log after you executed the commands. Provide some screenshots.

## Basic Permissions

### Editable Text Configuration

Who is the owner of the `/etc` directory on the system?

What are the permissions on this directory? Why can you list the content of this directory? Explain the permissions.

### Davy's Secrets

Create a file called `davys_secrets.txt` inside of the `tmp` directory. Add some content to the file using nano.

What are the current permissions and who is the owner of the file?

Change the owner to `davy`. Can you still read / change the content of the file?

What command would you need to lock everyone except davy out of the file? Make sure to test it.

### Sudo created files

Create a file called `my_root.txt` inside of the `/tmp` directory using the command `sudo touch /tmp/my_root.txt`.

Who can access the file and what permissions does it have. Who is the owner of the file?

Change the permissions of the file to `640`. What has changed? Do you still have access to the file?

### Recursive

Create a directory called `/tmp/arts/colors` and add three files to it: `red`, `green` and `blue`.

Next create a directory `/tmp/arts/musical_notes` and add three files to it: `do`, `re` and `mi`.

Who is the owner of the files and directories? You can list all of them at once using the `-R` option for `ls`.

Now change the owner of the directory `/tmp/arts` and all of it included files to `davy` using the recursive option of `chown`.

Damn we made a small mistake. The goal was actually to make `root` owner of all the files and dirs and set the group to `davy`. Fix the mistake.

### Developers group

Search the man-pages on how to create a new group on the system.

Now add a group `devs` to the system. What is the `GID` of this group?

Add yourself and `davy` to this group.

Now add a directory `projects` to the root of the file system, so `/projects`.

Now set the owner of the directory to `root` and set the group to `devs`. Give both `root` and `devs` permissions to:

* traverse the directory
* create files in it
* read the files in it

The rest of the world should not be able to access this directory.

Now add a subdirectory for `davy` and a subdirectory for yourself. Set the owners accordingly. Next change the permissions of the directories so:

* davy has read and traverse permissions on your directory but no write permissions
* you have read and traverse permissions on davy's directory, but no write permissions

Test everything by using login sessions of each user.

# Chapter 06 - Ownership and Permissions

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

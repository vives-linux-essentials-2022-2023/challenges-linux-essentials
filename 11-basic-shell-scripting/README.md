# Chapter 11 - Basic Shell Scripting

Solve the challenges by creating small bash scripts. Place the bash scripts here for every challenge. Make sure to add some comments and explain how they work.

## Log the Date

Create a script that output the `date` every 10 seconds. Use the `sleep` command to wait between calls to the `date` command.

## Available Memory

Output the available system memory together with the current date in the following format:

```text
[Thu 14 May 2020 11:12:55 AM CEST] MemAvailable:   28439572 kB
```

The available memory can be found in the file `/proc/meminfo`. Use the `grep` tool to filter out the line with `MemAvailable`.

## Fetch GitHub Details

Use the `curl` tool to fetch the information of a user on GitHub at the api [https://api.github.com/users/<username>](https://api.github.com/users/<username>) (where `<username>` should be replaced with the github username) and display it to the user.

Create a script that takes in the username as an argument on the command line.

Example on how to call the script:

```bash
./github bioboost
```

### Fetching Github Keys

Create a script that fetches the public SSH keys of a user on GitHub and displays them in the terminal. This can be accomplished by using the `curl` tool to access the endpoint [http://github.com/<username>.keys](http://github.com/<username>.keys), where `<username>` is an existing github username.

Take in the username via the command line arguments. If none is provided request it from the user using the `read` command.

Example via command line:

```bash
./githubkeys bioboost
```

or via the `read` command:

```bash
./githubkeys
Please enter GitHub username: BioBoost
Fetching Keys
...
```

### Cloning Repo

Create a script that uses `git` to clone some repository (for example the one of this course) in the current directory. If the repository already exists locally, then pull the latests changes in `master`.

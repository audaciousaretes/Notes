# Intro to Terminal

```sh
# make a directory
$ mkdir <directory-name>

# move into a directory
$ cd <directory-name>

# list the contents of a directory
$ ls <directory-name>

# the symbol for the current directory is a dot
$ ls . # this lists the contents of the current directory

# the symbol for the parent directory is ..
$ cd .. # this moves up a directory

# See the current directory
$ pwd
```

## Intro to Git/Github

        * Homebrew
        * Git
        * Github

## Git Commands

#### Creating a repository on your computer
This creates a git repository in the current directory.

```sh
git init
```

#### Adding files to the staging area

To see the current status of your directory and repository:

```sh
$ git status
```

To add a single file to be tracked

```sh
$ git add filename.extension
```

To track *all* files. You can do this by adding the current directory.

```sh
$ git add .
```

#### Checking the status again, and do this often
```sh
$ git status
```

#### Committing files
Now that you have files in the staging area, you can save a snapshot of the staging area using a commit.

```sh
$ git commit -m "Message"
```

#### Ignore Certain Files

Want to ignore a specific file, create a `.gitignore` file and add any files to it you want to ignore. Ah'hem ... I'm looking at you `.DS_Store`.

# Resources
* [Try Git](https://try.github.io/levels/1/challenges/1)
* [Git Manual](http://git-scm.com/doc)

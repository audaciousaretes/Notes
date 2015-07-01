# Setting Up Your Development Environment

As an engineer, you'll have a toolset that you use on a daily basis and that toolset is made up of a few different types of tools:

- Operating System (OS X Yosemite)
- Editor (Atom)
- Browser (many browsers)
- Command Line Interface (Terminal.app)
- Package Managers (npm, homebrew)
- Languages (HTML, CSS, Javascript, Node.js)

In this session we'll setup Atom, learn a little about the command line and

## Install OS X Yosemite

It will help for us all to be on the same version of OS X for debugging and consistency purposes. If your Mac isn't on OS X Yosemite, please follow these instructions **when you get home** and let it install outside of class. Hit me up on slack if you run into trouble.

1. You’ll need to sign in to the Mac App Store with you Apple ID. If you don’t have one, sign up here.
1. Download the Yosemite upgrade from the Apple Store: download here.
1. Double-click “Install OS X Yosemite” to begin installation.

**WARNING**: The OS X upgrade can take a bit of time to complete and will require a restart. Plan on doing this in the evening.

## Install Atom

> Atom is a free text editor packed with lots of cool features and syntax highlighting (for reading your code more easily).

1. Download Atom from the Atom website.
1. Unzip the downloaded file by double-clicking on it. (It may be unzipped for you already, depending on how you downloaded it.)
1. Move the Atom application into your Applications folder.
1. Run Atom.
1. Once Atom has started, click the Atom menu and run “Install Shell Commands.”

Click on "Atom", "Preferences", "Packages" and in the search bar, type "autocomplete". Please disable all autocomplete packages. When you get to the point that you feel comfortable with the content at the end of the cohort, feel free to turn it back on, but the whole purpose of this class is to learn the languages we're using, where autocomplete for code may hinder you from growth.

## Install Google Chrome

Download [Google Chrome](https://www.google.com/intl/en/chrome/browser/)

## Install XCode Command Line Tools

1. Go to the [Apple Developer Downloads site](https://developer.apple.com/downloads/).
1. You will have to register.
1. Look for “Command Line Tools (OS X 10.10) for Xcode - Xcode 6.2” and download them.
1. Once downloaded, open the downloaded file by double-clicking on it. This should bring up a new window with a file that ends in .pkg. Double-click it and follow all the prompts.

## Install Node.js

> Node.js is a runtime environment for server-side applications, so you can use Javascript to create utilities and run applications. You can also write Javascript directly in your terminal using Node.js.

1. Download the Universal Mac OS X Installer: [Node v0.12.5](https://nodejs.org/dist/v0.12.5/node-v0.12.5.pkg)
1. Open the installer (the file tat ends in .pkg) and follow all the prompts.
1. When complete, open Terminal.app and type `node -v`. It should output `v0.12.5`.

### NPM

> NPM stands for Node Package Manager and is the javascript package manager we'll be using in class.

NPM comes bundled with Node.js, so inside of Terminal.app you should be able to type `npm -v` in the terminal and it will output a version number. If this is not the case, please let me know.

## Install Homebrew

> Homebrew is our other package manager that we'll managing software.

1. Open up Terminal.app. If you have any trouble here, go through the command-line prework.
1. Run `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` and follow all the prompts.
1. Run `brew doctor`
1. Run `brew install readline git`

## Setup SSH keys

> SSH keys are a way for two computers to communicate with each other securely without having to ask a user for their username and password.

Create an SSH key (do not give it a password when it asks for one)
Run `ssh-keygen` in your terminal.

## Setup a Github.com account

> We'll be using git heavily for version control as well as submitting homework assignments. github.com is a free platform that hosts your git version controlled codebases.

Create an account on [github.com](http://www.github.com) and follow Step 4 for adding your SSH key to your Github account. Let me know your username via slack.

## Learning the Command Line
`pwd` [present working directory] - to see the full path of what directory you're working out of
`ls` - Lists the files and directories in your present working directory
`cd` [change directory] - this command followed by an argument of what directory you want to change into changes your present working directory

## Bonus Material
[Introduction to the Command Line](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line)
[Learn the CLI (Terminal) The Hard Way](http://cli.learncodethehardway.org/book/)

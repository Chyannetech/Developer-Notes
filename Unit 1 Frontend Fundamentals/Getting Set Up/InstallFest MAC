For the first phase of "install-fest", we'll install or verify the installation of the following tools on our machines:

Slack
Zoom
Homebrew
Xcode
VS Code
Git / Github / Github Enterprise
Global Gitignore
Spectacle - (optional)
Imgur - (optional)


Slack
We'll use slack to communicate throughout the course.
By the time you are reading this, you should have received an invite to the relevant channels via e-mail.
Although you can login via the web browser, downloading / installing the app is highly recommended.

Zoom
Download the Zoom client and install it.

Homebrew
Homebrew is a package manager that we will use to install various command line tools in our class.

Open up terminal, and paste the following command to install Homebrew. You might be prompted to install XCode Command Line Tools during the install process. 

ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

If you are prompted to install the XCode CLI, say yes and your homebrew installation will continue.

After the installation process, run the command brew doctor. If any warnings or errors are displayed, we will need to resolve them before proceeding with the rest of the install fest.

Lastly, make sure to run brew updateto make sure you have the latest lists of available software.

Xcode
We do not use Xcode in class but some other applications that we do use require some Xcode libraries. Normally, all you need is the Xcode CLI which should have already been installed when you installed Homebrew. If it didn't get installed, you can use this command:

xcode-select --install
If you need to, you can install Xcode through the App Store. (You probably don't need to.)

Visual Studio Code
Text editors are a personal choice. One of the most popular open source text editors these days, for good reason, is Visual Studio Code.

Note: VS Code's keyboard shortcuts are different than the shortcuts used by the Sublime or Atom editors. If you already know Sublime's shortcuts and don't want to learn those of VS Code, it's possible to configure VS Code to use Sublime's.

Download and install VS Code from https://code.visualstudio.com/.

Important: Be sure that VS Code is in your Mac's Applicationsfolder.




Add Ability to Launch VS Code by typing code
Launch VS Code using spotlight (command + space- then start typing vs cuntil you see the app, then press enter).
Type shift + command + Pto open the command palette.
Start typing shell commandand when you the
Shell Command: Install 'code' command in PATHcommand - click it!
Quit VS Code and Terminal.
Relaunch Terminal
You should now be able to open a folder to edit by typing code .
Check this link for troubleshooting if you run into issues.



Git
Git is the version control software we will be using - it's extremely popular.

You should have already installed Git as instructed to complete the pre-work.

If it's not installed, we can use Homebrew to install it:

brew install git



Github
Github provides a way to host Git repos in the cloud. It enables collaboration and is wildly popular.

You should have already opened a personal Github account, however, you need to have a General Assembly Github Enterprise account as well.
You can get one by signing up here: https://git.generalassemb.ly/join




Configuring a Global git ignore
Everyone should have a global git ignore file so that you don’t have to worry about making the appropriate entries in a project’s git ignore.

First, create the file: touch ~/.gitignore_global

Next, configure git to use this file: git config --global core.excludesfile ~/.gitignore_global

Finally, lets put some good stuff in there:

# This is a list of rules for ignoring files in every Git repositories on your computer.
# See https://help.github.com/articles/ignoring-files

# Compiled source #
###################
*.class
*.com
*.dll
*.exe
*.o
*.so

# Packages #
############
# it's better to unpack these files and commit the raw source
# git has its own built in compression methods
*.7z
*.dmg
*.gz
*.iso
*.jar
*.rar
*.tar
*.zip

# Logs and databases #
######################
*.log

# OS generated files #
######################
._*
.DS_Store
.DS_Store?
.Spotlight-V100
.Trashes
ehthumbs.db
Thumbs.db

# Testing #
###########
.rspec
capybara-*.html
coverage
pickle-email-*.html
rerun.txt
spec/reports
spec/tmp
test/tmp
test/version_tmp

# node #
########
node_modules

# Rails #
#########
**.orig
*.rbc
*.sassc
.project
.rvmrc
.sass-cache
/.bundle
/db/*.sqlite3
/log/*
/public/system/*
/tmp/*
/vendor/bundle


# Ruby #
########
*.gem
*.rbc
.bundle
.config
.yardoc
_yardoc
doc/
InstalledFiles
lib/bundler/man
pkg
rdoc
tmp

# for a library or gem, you might want to ignore these files since the code is
# intended to run in multiple environments; otherwise, check them in:
# Gemfile.lock
# .ruby-version
# .ruby-gemset

# CTags #
#########
tags

# Env #
#######
.env

# Python #
#######
*.pyc
__pycache__/


Optional Installs
Some of these options below might not work properly on your machine depending on how old or new your computer is, so use at your own risk. However, the tradeoff is that these tools offer powerful conveniences


Installing Imgur
Create an account on imgur.com and install mac2imgur to ease uploading screenshots and other images from your computer to your imgur account.


Installing Spectacle
Install Spectacle for resizing windows.

This free "productivity" tool is invaluable when it comes to minimizing the time spent sizing windows using the mouse.


Spectacle's Basic Default Hotkeys
Here are the most popular hotkeys:

Make window full-size — opt + cmd + F
Move to the left half — opt + cmd + ←
Move to the right half — opt + cmd + →
Move to the top half — opt + cmd + ↑
Move to the bottom half — opt + cmd + ↓
Pressing the same hotkey will size the window by thirds!

You can find more info about Spectacle here.

Install a Markdown Editor
For editing and viewing Markdown, use VS Code or a dedicated markdown editor such as MacDown.

Resources for Markdown
https://guides.github.com/features/mastering-markdown/
https://www.markdownguide.org/basic-syntax/
https://markdowntutorial.com/
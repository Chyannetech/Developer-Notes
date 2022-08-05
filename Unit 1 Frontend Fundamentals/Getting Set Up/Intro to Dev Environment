Learning Objectives
Students will be able to:

Be more productive by using the keyboard vs. the mouse

Use the Terminal Command Line Interface (CLI) to navigate and manipulate the filesystem

Use the VS Code text editor to open and edit files




Being More Productive by using the Keyboard vs. the Mouse



Launching Apps with Spotlight
Developers avoid using the mouse whenever possible

Developers are more productive when their hands are on the keyboard

Open applications using Spotlight instead of the mouse by:

Pressing cmd+spaceto open Spotlight
Start typing the name of the app until the app is highlighted
Press enterto open the app!



Switching Between Applications
Quickly switch between running applications by pressing cmd+tab

If a minimized applications does not display after tabbing to it with cmd+tab:

Continue to hold down cmdand release tab
Press optionthen release cmd



Switching Between Instances of an Application
You can switch between multiple windows of the same application using cmd+` (that's a back-tick character, which is above the tabkey)

Note that it's best to minimize how many windows/applications you have open when developing to make switching between applications quicker and minimize distractions to the job at hand




Uploading Screenshots and Images to imgur.com

Why Upload Images?
Often you will need to share images with others or use them in your applications, notes, readme files, etc

Unfortunately, if an image exists only on your computer, you lose the ability to use it anywhere but on your computer

The solution is to upload images to a cloud service...



Imgur
One of the most popular image hosting services on the Internet is Imgur.

Go there now and open a free account

Although you can upload images using Imgur's web interface, but there's a better way...




Upload Tools for Imgur
Click this link to go to a page of different tools you can use to conveniently upload images to imgur from your computer




Screenshots
The following keyboard shortcuts can be used to take screenshots of your screen:
Whole screen: shift-cmd-3
Part of your screen: shift-cmd-4
A certain window: shift-cmd-4, then spacebarto toggle window mode


Using Spectacle to
Move and Size Windows

What is Spectacle?
Spectacle is a free utility that resizes and snaps into position app windows

If you don't see the "spectacles" in your menubar, launch Spectacle using Spotlight

When running, Spectacle will listen to the keyboard for certain key combinations (hotkeys) and will resize/position the active application accordingly...




Using the Terminal
Command Line Interface

What is Terminal?
Terminal is the developers' choice for entering commands and navigating the filesystem

Terminal is also known as a shell. The default shell in Mac OS X is Bash. You will find the terms terminal and bash often used interchangeably

Go ahead and open Terminal (remember - use Spotlight!)




Command Line Basics
Before we get started with this section, it might be helpful to ensure we are all using the same shell configuration.

That said, here are some screenshots to show how your instructor has set up their shell:

Now that we've reviewed shell config, here are the basic command tasks we'll try out:

Change directories (folders)
List a directory's contents
Create a directory
Create a file
Move files and directories
Copy files and directories
Rename files and directories
Delete files & directories
Command history & clearing the window


Change Directories
We use the cdcommand to change directories

Let's change to the home directory of the logged in user:
$ cd ~
Here are a few common shortcut characters used when navigating the filesystem:

~The logged in user's home directory
/The root (top-level) directory on the harddrive
.The current directory
..The parent directory of the current directory
The pwdcommand "prints" the current (working) directory



List a Directory's Contents
Use the lscommand to display a concise list

lsdoes not display hidden files by default, adding the -aoption will show them

treeis a nice utility for displaying a graphical representation of a directory and its nested directories.
Install it by typing brew install tree



Create a Directory
Use the mkdircommand to create directories

Let's create a drawersdirectory inside of the home directory:

$ mkdir ~/drawers
Note that you don't have to specify the full path if we are already in the home directory



Using Tab Auto-Completion
Change to the home directory

Now let's change to our newly created drawersdirectory, however, only type cd d,
then press tabwhich will auto-complete directory name(s)

You can cycle between matching directory names by continuing to press tab



Creating Files
We use the touchcommand to create empty files

Let's move to the drawersdirectory and create a directory named socks. Here is how we can create the directory and change to it using a single command:

$ mkdir socks && cd socks
Now let's create a dress.socksfile:

$ touch dress.socks


Practice Creating Directories and Files
Create this directory: ~/drawers/pjs

Create two files in the new pjsfolder named warm.pjsand favorite.socks



Moving Files
Okay, so we have a messy drawers/pjs, let's move our favorite.socksfile out of the pjsfolder and into the drawers/socksfolder where it belongs!

Here's how we can do the move regardless of which directory we're currently in by using absolute paths:

$ mv ~/drawers/pjs/favorite.socks ~/drawers/socks/
Be sure to use tab-completion!

Note that you have the option to use absolute and/or relative paths.



Moving Directories
Moving directories is just as easy using the same mvcommand

Try it out:

Create a ~/shortsdirectory
Move the newly created shortsdirectory into the drawersdirectory


Renaming Files
Guess what - there's no dedicated bash command to rename files and directories!

Don't panic! The mvcommand is very flexible!

Here's how we can rename the warm.pjsfile to summer.pjsfrom anywhere:

$ mv ~/drawers/pjs/warm.pjs ~/drawers/pjs/summer.pjs
Of course, you can actually move and rename simultaneously!



Deleting Files
We use the rmcommand to delete both files and directories

Let's first use it to delete the dress.socksfile. Here's one way:

$ cd ~/drawers/socks && rm dress.socks
Using the *wildcard character, it's possible to delete and move multiple files. For example, typing *.sockswould match all files with an extension of .socks...



Deleting Directories
Deleting directories is almost the same as deleting files except you must use the -roption, which runs the rmcommand "recursively" to delete a directory and it's contents.

To delete the pjsfolder we could use this command:

$ rm -r ~/drawers/pjs


Moving Multiple Files
To demonstrate moving multiple files, re-create the dress.socksfile we just deleted from the socksdirectory

Now let's move all of the .socksfiles out of the socksfolder into our home folder. The following command assumes we're inside the socksfolder:

$ mv *.socks ~
Now, without changing directories, return the socks files back to where they belong



Copying Files & Directories
Use the cpcommand to copy files and directories

Here's how we can copy all .js files:

$ cp *.js ~/dest-folder
And entire directories by adding the -Roption:

$ cp -R ./sample-code ~/dest-folder


Command History & Clearing the Window
Pressing the up and down arrows in Terminal will cycle through previously entered commands. This can be a huge time saver!

If you'd like to clear the Terminal window, simply press cmd+k



Using VS Code to Open and Edit Files

What is VS Code?
VS Code is a popular open-source text-editor maintained by Microsoft

It's very customizable and capable

VS Code's functionality can be extended using extensions, however, most useful features are built-in

To try it out, let's use VS Code to open and edit a file...



Add VS Code to $PATH
We want to be able to type in code .in Terminal and have VS Code open the current directory for editing

First, open VS Code's Command Palette by pressing ⇧⌘P

Next, type "shell command" and select the Shell Command: Install 'code' command in PATHcommand

Restart Terminal for the new $PATH to take effect

For the above to work, VS Code must be installed in the Applications folder





Going Forward
Today, we have only scratched the surface of tools such as Terminal and VS Code

Rest assured that throughout your time in SEIR, we will help you to get to know these tools much better!


Install a Markdown Editor
For editing and viewing Markdown, use VS Code or a dedicated markdown editor such as MacDown.

Resources for Markdown
https://guides.github.com/features/mastering-markdown/
https://www.markdownguide.org/basic-syntax/
https://markdowntutorial.com/
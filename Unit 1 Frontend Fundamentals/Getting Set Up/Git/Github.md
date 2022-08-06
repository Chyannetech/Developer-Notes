Setup Instructions

https://generalassembly.zoom.us/rec/share/DyllEgQeyvNoguKc0O-MzJjh_hecAxGD4GruuopH2ywLCBOJ07eqoWRkwoVXLOZd.fYZ9-MUXeu1eA7OB?startTime=1613504867000 


Create a folder in your Desktop or any other designated location on your machine; you can name it git-github-and-terminal
Initialize a gitrepo inside that folder with the command git init
Create a repository on git.generalassemb.ly- Your Github Enterprise Account
Add your remote from githubto your local repo with the following command: git remote add origin https://www.git.generalassemb.ly/YOURUSERNAME/git-github-and-terminal.git
Create a file called README.mdinside your git-github-and-terminalfolder
Write your answers to the questions below in your README.mdfile
Commit your work at each point when directed (remember to git add .and then git commit -m "your commit message")



Git & Github - Questions
Refer back to the notes from today and/or use the internet and google-futo find the answers to the questions below:

Answer the following questions

What command do you use to setup a git repository inside of your folder?
What command do you use to ask git to start tracking a file?
What command do you use to ask git to move your file from the staging area to the repository?



Terminal Practice

Episode X: A New Terminal
A long time ago in a Unix environment far, far away, young Jedi padawans who knew only of desktop software were seduced by the dark side of the Force to enter… The Terminal.

Follow the instructions below using all the console commands introduced in Fundamentals, class, or that you find on your own.



Setup
Open the Terminal app

Inside your homework folder, git-github-and-terminal, create another folder called: galaxy-far-far-away

Then create a file inside galaxy-far-far-awaycalled commands.txt

Paste the answer to each numbered question (i.e. the command(s) that accomplished the task) in commands.txtonce you get it to work

Remember, you can learn about any Unix command by typing manand then the command name. E.g., man ls. Type Qto get out of the Manual page ("man page") viewer



Part I: Set the Scene
Complete all work inside the galaxy-far-far-awayfolder.

Create a directory called death_star, and make the following files inside of it: darth_vader.txt, princess_leia.txt, storm_trooper.txt

In galaxy-far-far-away, make a directory named tatooineand create the following files in it: luke.txt, ben_kenobi.txt

Inside of tatooinemake a directory called millenium_falcon, and in it create: han_solo.txt, chewbaca.txt


Part II: mv- rename
You can rename a file using the mvcommand.

Rename ben_kenobi.txtto obi_wan.txt

Part II: cp- copy
You can copy a file from one location to another using the cpcommand. (man cpfor more info)

Directories can be sibling (parrell to each other) or can be parents (the folder that contains the folder you are in)
Copy storm_trooper.txtfrom death_starto tatooine

Part IV: mv- move
You can use the mvcommand to move files from one location to another. mvcan be used for renaming, moving, or both. Run man mvto see the options—remember hit the Qkey to get out of the manual page viewer.

Move luke.txtand obi_wan.txtto the millenium_falcon

Move millenium_falconout of tatooineand into galaxy-far-far-away

Move millenium_falconinto death_star

Move princess_leia.txtinto the millenium_falcon


Part V: rm- remove
BE CAREFUL WITH rm!!! THERE IS NO "TRASH" IN THE UNIX CLI. WHEN YOU DELETE SOMETHING IT IS GONE FOREVER!!!

You can use rmto delete a file.

Delete obi_wan.txt.

Part VI: all together
In galaxy-far-far-away, make a directory called yavin_4

Move the millenium_falconout of the death_starand into yavin_4

Make a directory in yavin_4called x_wing

Move princess_leia.txtto yavin_4and luke.txtto x_wing

Move the millenium_falconand x_wingout of yavin_4and into galaxy-far-far-away

In death_star, create directories for tie_fighter_1, tie_fighter_2and tie_fighter_3

Move darth_vader.txtinto tie_fighter_1

Make a copy of storm_trooper.txtin both tie_fighter_2and tie_fighter_3

Move all of the tie_fightersout of the death_starand into galaxy-far-far-away


Part VII: rm -r: remove directories and everything they contain
BE CAREFUL WITH rm -rTHERE IS NO TRASH CAN IN THE UNIX CLI. WHEN YOU DELETE SOMETHING IT IS GONE FOREVER

Before you hit enter, make sure are deleting the right thing, or you could accidentally delete the contents of your computer (it has happened).

This command will not typically ask you if you "really want to delete." It will just delete.

Remove tie_fighter_2and tie_fighter_3

Part VIII:
Touch a file in x_wingcalled the_force.txt

Destroy the death_starand anyone inside of it

Return x_wingand the millenium_falconto yavin_4

Celebrate. You've reached the end of this homework :)

Commit and push your updated code:
"Add" your changes (prepare them to be "committed"):

$ git add -A
"Commit" your changes—any time you make a commit, you can always restore the files in the repo to that point:

$ git commit -m "Completed homework"
"Push" your commits to github:

$ git push origin master
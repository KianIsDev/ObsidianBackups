# Attention
This is a smal project i have been working on for my own entertainment. It *should* be applicable by anyone who finds themselves in a similar situation, but keep in mind that this is "just" a hobby project to help my study productivity.
I can't confirm if it will work on other types of Linux machines, but i at least know that it works on mine :D
That said, i am incerdibly proud of how it turned out, and i would love any and all feedback!

# Who is this for?
- You use **Obsidian**.
- You use an Ubuntu-based **Linux** machine and a seperate Windows machine with **WSL** (Windows Subsystem for Linux) on it.
  - *Alternatively* two(or more) Ubuntu-based Linux machines that you want to sync between.

# Why i did it
I recently switched to Linux Mint on my home computer, while still using Windows on my School computer with a WSL for Ubuntu.
The proplem then became, that i didnt have a reliable way of syncing my Obsidian notes between the two computers. Erarlier i had used Google Drive to automatically upload and download the notes, but this solution works poorly on a linux machine.
So thats why i went with github.
There are other tools that links github and Obsidian, but the setup was somewhat of a hassle, and it didnt seem to do exactly the things i wanted it to, so i made my own :D

# Getting started
You should consider making a **private** copy of this repository and host it on your own account. While forking the project does come with some benefits, it sadly can't (to my knowledge) hide the private notes that this project is aimed at backing up.
So for your own safety, i recommend making your own **private** copy of this project.

## Make a private copy
1) ``git clone`` this repository.
2) ``cd`` into the repository.
3) Go to [GitHub](https://github.com/new) and make a new **private** repository.
4) ``git push --mirror`` into your new repository.
5) Now you should be able to see all the same files inside your own repository.
6) Clone this new repository instead of mine, on your various machines.

## Run the script
The file named **BackUpObsidian** is the bash script that takes care of all the syncing to GitHub. It also has the *optional* capability of opening Obsidian for you. So instead of opening obsidian manually, just run this script and you should be taken straight to Obsidian. This also has the added benefit of terminating the backup process once you close out of Obsidian!

Simply *double-click* the script in a file manager, or use ``bash BackUpObsidian`` inside the terminal.

## First launch
On your first launch, you will be greeted with a prompt, asking you to provide the command that opens Obsidian.
simply follow the instructions for either Linux or WSL.
This information will be stored in a file called **obsidian.path**. If you want to change this command in the future, simply edit the file or delete it and you will be prompted once you run the script again.




# Helpful tips
## Use an Alias

Create an [alias](https://askubuntu.com/questions/17536/how-do-i-create-a-permanent-bash-alias) to quickly run the program from a terminal.
I made one that looks like this, for the WSL terminal:

``alias obsidiantool='cd /mnt/c/Users/Kian/Documents/ObsidianBackups/; bash BackUpObsidian'``


## WSL and file management on Windows

Preferably you want to save the program and all the notes in the Windows file system. Obsidian won't be able to open the files if you save them inside the WSL envionment.
You should instead ``cd`` to a directory inside the ``/mnt/c/`` where the Windows filesystem resides, and clone the git repository there.

(*Note that this is because i have installed the Windows version of the Obsidian application. It will behave differently, if you install Obsidian through WSL itself*)

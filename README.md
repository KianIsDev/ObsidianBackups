# Attention
This is a smal project i have been working on for my own entertainment. It should be applicable by anyone who finds themselves in the same situation, but keep in mind that this is "just" a hobby project to help my study productivity.
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

# Helpful tips
## Use an Alias

Create an [alias](https://askubuntu.com/questions/17536/how-do-i-create-a-permanent-bash-alias) to quickly run the program from a terminal.
I made one that looks like this, for the WSL terminal:

``alias obsidiantool='cd /mnt/c/Users/Kian/Documents/ObsidianBackups/; bash BackUpObsidian'``


## WSL and file management on Windows

Preferably you want to save the program and all the notes in the Windows file system. Obsidian won't be able to open the files if you save them inside the WSL envionment.
You should instead ``cd`` to a directory inside the ``/mnt/c/`` where the Windows filesystem resides, and clone the git repository there.
(Note that this is because i have installed the Windows version of the **Obsidian** application. It will behave differently, if you install Obsidian through WSL itself)

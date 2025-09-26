# OverTheWire-Bandit-Level-2-README.md
This is an over-the-wire lab to capture hidden passwords using the Linux command lines

# Bandit Level 1-2
**Platform:** OverTheWire (Bandit)  
**Date:** 2025-09-24  
**Difficulty:** Beginner 
**Objective:** The goal of this level is to find the password for the next level (level 2-3). It is in a file called -

## Steps
1. SSH into the server (details not shared here).  
2. Checked files with `ls` (ls is a command to list the file(s)). A weird file named - is present.
3. Tried reading the file using `cat` (cat is a command to read the file(s) but didn't open it.
4. Googled what kind of file "-" is, and I found out it's a special kind of file
5. After research, I then used the prefix "./" in the file, and it finally opened, and the required password for the next level was retrieved.

## Screenshots
- errors and capture.png (logged in, errors and proof (redacted))   

## Lessons
- I learnt that reading any file named"-" directly with cat won't output anything, as the terminal will see it as a stdin command.
- I learnt that you must first disambiguate such files in 3 ways: Use ./ in front of it, Use -- to tell the command “stop parsing options”, or Quote it (it may still need -- depending on command) 

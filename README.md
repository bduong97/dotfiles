# Introduction
This repo will be where I store my dot files, such as .bashrc, .bash_profile and other configuration files for programs so that
they are under version control and easily transferable between different systems.

# Disclaimer
If you are on Windows and using Git Bash, note that trying to create a symbolic link using bash did not work for me; It would create a copy of the file instead of linking
to the actual file as intended. To get around this, I created a symbolic link from the command prompt using `mklink`, which worked. Note that you have to make sure
that your user account has symbolic link privilege (check *local security policy -> local policies -> user rights assignment -> Create Symbolic Links*)

# Setup
If you'd like to try it yourself, here is the process:
1. Create some directory (*~/GitStuff/myDirectory/*), `cd` into it, and input `git init`
2. Add your remote repo with `git remote add origin [repo URL here]`
3. Move your configuration/settings file into this repo. For example, with .bashrc, you can input `mv ~/.bashrc ~/GitStuff/myDirectory/.bashrc`
4. Create a *sym link* where the original settings file was located and point it to your file in the git directory. Example: `ln -s ~/GitStuff/myDirectory/.bashrc ~/.bashrc`
5. Commit and push to remote repo. You can then add your remote repo on other machines and pull from it in order to keep your settings files accurate

# Disclaimer
You will have to create the sym link pointing to your settings files for each machine that you use.

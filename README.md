# Introduction
This repo will be where I store my dot files, such as .bashrc, .bash_profile and other configuration files for programs so that
they are under version control and easily transferable between different systems.

# Setup
If you'd like to try it yourself, here is the process:
1. Create some directory (*~/GitStuff/myDirectory/*), `cd` into it, and input `git init`
2. Add your remote repo with `git remote add origin [repo URL here]`
3. Move your configuration/settings file into this repo. For example, with .bashrc, you can input `mv ~/.bashrc ~/GitStuff/myDirectory/.bashrc`
4. Create a *sym link* where the original settings file was located and point it to your file in the git directory. Example: `ln -s ~/GitStuff/myDirectory/.bashrc ~/.bashrc`
5. Commit and push to remote repo. You can then add your remote repo on other machines and pull from it in order to keep your settings files accurate

# Disclaimer
You will have to create the sym link pointing to your settings files for each machine that you use.

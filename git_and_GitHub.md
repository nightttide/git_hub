# Install
on linux you need to run `apt-get update` then run `apt-get install git`
TIP: Most linux systems come with git pre-insalled

On windows you can download this [this program](https://gitforwindows.org/)
, it will emulate a linux terminal environment

# Basic usage (aka not editing the repos)
## Cloning a repository

Make a copy of a remote repository on your system

```
git clone https://github.com/WillKopil/webAvatars
```

to update that repository simply run this within the directory in was cloned

```
git pull
```

# Set up

## Setup git user

`git config --global user.name "Mona Lisa"`

`git config --global user.email "your_email@example.com"`

## setting up GitHub account

Create a public and private ssh key, the name id_rsa is good

`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

Now take the content of the .pub file and paste them on GitHub in settings

Verify the key by running

 `ssh -T git@github.com`

The output should say your authenticated but do not have access to the shell

# Using git for your projects

## Starting a local repository

Navigate to folder where you want to create a repo and run

`git init`

TIP: in the terminal environment you can see what folder you are in by running `pwd` 
To change to the desired directory run `cd path/to/your/dir`
Now you can see what files in in said directory with the `ls` command

## Staging files for a commit

From the repos directory run

`git add filename`

## Check status of repository
You can see what files have been added to the repo and what has changed with

 `git status`
 
 ## Commit changes to repository

`git commit`

To commit with a message run

`git commit -m "your message here"`


## Adding a remote repository

`git remote add origin "http://github.com/user/repo"`

To see the current remote repo 

`git remote -v`

## Pushing to remote repository

`git push -f origin master`

For GitHub

```
git branch -M main
git push -u origin main
```

## Changing the default text editor

`git config --global core.editor "C:\path\to\editor.exe"`

You can also check what the current editor is with

`git config ???global core.editor`

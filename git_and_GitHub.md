# Install
on linux you need to run `apt-get update` then run `apt-get install git`
TIP: Most linux systems come with git pre-insalled

On windows you can download this [this program](https://gitforwindows.org/)
, it will emulate a linux terminal environment

# Configuration

## First-time Setup
You will need to perform some basic configuration before using Git for the first time.

```
git config --global user.name "Mona Lisa"
git config --global user.email "your_email@example.com"
git config --global init.defaultBranch main
```

## Default Editor

Optionally, you may also want to set your default text editor.

```
git config --global core.editor "C:\path\to\editor.exe"
```

Verify your currently-set editor with:
```
git config –-global core.editor
```

## GitHub

In order to push your commits to GitHub, you will need to generate an SSH key and upload it to your GitHub account.

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

You will be prompted for a file name, which by default will be id_rsa. After generating your key, find id_rsa.pub and view the contents in a text editor.

Next, on GitHub browse to Settings -> SSH and GPG Keys, and click "New SSH Key". Give the key any title you like, and enter the contents of id_rsa.pub, and save.

You can now verify the key is correctly set up by running:

```
ssh -T git@github.com
```

If everything is configured correctly, you should see a message stating that you've successfully authenticated.

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

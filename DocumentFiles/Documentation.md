# Documentation of How To
## Contents
- [Usefull Commands](#Usefull-Commands)
- [Vim Navigation](#Vim-Navigation)
- [Push Help](#Pushing)
  - [Push Permision Error](#Permission-Error)
  - [Push Rejected Error](#Rejected-Error)
- [Tagging](#Tagging)
- [Ssh key](#ssh-key-creation)
- [Markdown](#Markdown)
- [Misc](#Misc)
## Usefull Commands

`cd` Change directory 

`git status` gives you a summary of what you have edited

`git log` shows you a summary of all the commits that have been done

`git branch` shows a list of all branches including which one your in

`git branch name` creates a branch with that name

`ls` shows the files in current directory

`git stash` allows you to update the repository without geting rid of your changes

## Vim navigation

`i` Insert, edit document

`w` Save

`:wq` Allows you save your documents and quit

`:wq!` Quit without saving

`Esc` Access the comand line for vim

`:help` Help page `:q` to exit help page

  
## Pushing
Once you have edited all the files you want go ahead and do this.
```
git add .
git commit -m <commit message>
git push --set-upstream origin
```
### Permission Error
if you recive a message that looks like this:
```
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.
```
then try 
```
chmod 600 /your/key/location/on/computer
```
### Rejected Error
if you recive a message that looks like this:
```
 ! [rejected]        PracticeMerging -> PracticeMerging (fetch first)
error: failed to push some refs to 'github.com:Awsome-O-clocks/CS-3300.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
then your push is conflicting with your current version try:
```
git pull origin
```
Now you can run your push command

## Tagging

When your ready to tag a version heres how. First your going to want to find the commit ID run
```
git log  --pretty=oneline
```
This will show you all the commits you've done look for the one that has the message you are looking for and note the first 5 or so characters of 
the Commit ID.
Next run the commands
```
git tag -a <label your tag> -m <add a description here> <commit ID>
git push origin --tags
```
If you want to check the tags curently saved run
```
git tag
```

## Ssh Key Creation

I recomend fallowing this guide.

[ssh creation](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

After step three go to this page and follows these instuctiions.

[Add ssh to account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

## Markdown

If your writing or editing this document then your more than welcome to look at the 'code' for this page.
You can also look at this [Markdown help page](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

But if your looking for a short and fast cheat sheet.
```
# BIG
## medium
### smaller

tripple pike: ``` opens a code block and closes with ```
a single pike: ` opens a code line and closes with `

[text](Link)
[text](# heading)

```

# Misc
A team member never recived the invation to the organization, after being added as a colaborator.
They eventualy descovered that the invatation was under the organizations tab in their github.

> [!NOTE]
> You can check your organizations in the organizations Tab.

![The oganizations tab is in the righthand menu](https://github.com/Awsome-O-clocks/CS-3300/assets/98062325/98d60864-889d-485e-9343-3230a4a0d295)


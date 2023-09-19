# Documentation of How To
## Contents
- [Usefull Commands](#Usefull-Commands)
- [Vim Navigation](#Vim-Navigation)
- [Push Help](#Pushing)
  - [Push Permision Error](#Permission-Error)
  - [Push Rejected Error](#Rejected-Error)
- [Stashing](#Stashing)
- [Tagging](#Tagging)
- [Ssh key](#ssh-key-creation)
- [Markdown](#Markdown)
- [Misc](#Misc)

## Usefull Commands

`git clone` pulls the entire repository down for EVIL >:). Makes a compleate copy. 
This is not the same as forking which creates a copy of the repository. (More to come on Fork) 

`cd` Change directory 

`git status` gives you a summary of what you have edited

`git log` shows you a summary of all the commits that have been done

`git branch` shows a list of all branches including which one your in

`git branch name` creates a branch with that name

`ls` shows the files in current directory

`git stash` allows you to update the repository without geting rid of your changes.

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

## Stashing

To stash your current work run `git stash` Then you can run `git stash list` this will show you all your active stashes.

```
stash@{0}: WIP on master: 9fd72D12 File Added
```

That first part is important if you want to veiw the changes you made.
Run `git stash show -p stash@{#}` 
> [!IMPORTANT]
> replace the # with what ever number you want to view.

Now you can pull the repository from here.
Now if you want to push the stash to the origin.

Fallow the push procedures as normal.


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

For Powershell Setup:

Windows has built-in OpenSSH into it since 2018
Open up terminal or PowerShell and run the following command

`ssh-keygen -t ed25519`

Using ed 25519 because GitHub recommends it you then will be prompted
for the key's name and where you want to save it.

Next will prompt for a passphrase the output should look like the following if done right:

![ssh-key gen](/Documentation-Developement/DocumentFiles/images/ssh-key-output.avif)



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

Issues with GE02:

Matthew:

Didn't know that he had to restart the virtual environment before visiting the local host link on port 8000. When he realized that, he started the virtual environment every time he returned to the GE02 assignment and was able to access the link.

Ray:

Visual studio command line wasn't working. Corrected the issue by researching online and going to the UCCS Math Center. 

Under "Devind URI Path and Views" in GE02 document, didn't get the right screenshot on question 8. Fixed the problem by going back and making sure all the HTML files had the correct syntax. Found a bracket in the wrong place, which fixed the screenshot.

Intial push to GitHub was difficult and had to look up the correct commands.

> [!NOTE]
> You can check your organizations in the organizations Tab.

![The oganizations tab is in the righthand menu](https://github.com/Awsome-O-clocks/CS-3300/assets/98062325/98d60864-889d-485e-9343-3230a4a0d295)


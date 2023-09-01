# Documentation of how to solve seen issues
## Contents
- [Push Help](#Pushing)
- [Push Permision Error](#Permission-Error)
- [Push Rejected Error](#Rejected-Error)
  
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Habitant morbi tristique senectus
 et netus et malesuada fames ac. In eu mi bibendum neque. Dolor morbi non arcu risus quis varius quam. In pellentesque massa placerat duis ultricies. Id consectetu
r purus ut faucibus pulvinar elementum. Tellus id interdum velit laoreet id donec. Id interdum velit laoreet id donec ultrices. Aliquam ultrices sagittis orci a sce
lerisque purus semper. Velit aliquet sagittis id consectetur purus ut faucibus pulvinar elementum. Donec adipiscing tristique risus nec feugiat in fermentum posuere
 urna. Facilisi nullam vehicula ipsum a. Ac tortor vitae purus faucibus ornare suspendisse. Felis imperdiet proin fermentum leo vel orci porta. Nunc consequat inter
dum varius sit amet. Id faucibus nisl tincidunt eget nullam non nisi est. Tincidunt eget nullam non nisi est. Amet justo donec enim diam vulputate ut pharetra. Turp
is tincidunt id aliquet risus feugiat in ante. Eros donec ac odio tempor orci dapibus ultrices.


Aenean sed adipiscing diam donec adipiscing tristique risus nec feugiat. Tortor aliquam nulla facilisi cras fermentum odio eu. Donec adipiscing tristique risus 
nec. Tempus egestas sed sed risus pretium. Cursus vitae congue mauris rhoncus aenean vel elit scelerisque mauris. Leo duis ut diam quam nulla. Sem et tortor cons
equat id. Commodo viverra maecenas accumsan lacus vel facilisis volutpat est velit. Ut pharetra sit amet aliquam. Sagittis orci a scelerisque purus semper eget d
uis. Sit amet facilisis magna etiam. Vitae turpis massa sed elementum. Quis eleifend quam adipiscing vitae. Nisl nunc mi ipsum faucibus.


### Pushing
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



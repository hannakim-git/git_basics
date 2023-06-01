# Git basics :

Basic set of instructions to practice and learn basic to intermediate application of git in your project.

What is git? *Software which allows you to manage and keep track of your development in the project.*

## Getting Started :

How to use this repo ?
- Fork it on your github account. 

and follow the following instructions :

### Create a new branch :
```bash

git checkout -b test_v1
```
Note : `-b` means creating a new branch.

### Add your changes :
Check this repo and you'll find `example/` folder.

I have already added sample python file `example/add.py` which adds two value. Now, create a new file in your preferred language and write a function to calculate the sum of two integers. 

git add is an alternative way of saying "code in this file is written, i'll put it in a stash folder before shipping it" 

```bash

git add example/"writefilenamehere"
```

for example : `git add example/add_csharp.cs `

you can add multiple files also like :
```bash

git add example/add_csharp.cs 
git add example/add_rust.rs
git add example/add_go.go 
```

They all will be stashed in the same folder before being shipped.

if you have created alot of new files then adding a file one by one can be little annoying. so you can just add all the files to the stash folder by saying
```bash
git add .
```


### Commit your changes made to git :

git commit is an alternative way of saying "file which were in this stash folders are ready to be shipped." so all of the files that were in the stash folder will be given a packed under a message and shipped, they'll be tracked by the git from now.

```bash

git commit -m "Add CSharp example"
```

now if you type
```bash
git log 
```
output will be like 
```bash
commit b74787e256c681776c30c6e22cf18adde6a93b22 (HEAD -> master)
Author: hiteshhedwig <hitesh.kumar61@yahoo.com>
Date:   Thu Jun 1 12:41:07 2023 +0530

    add example code
```

this commit ID `b74787e256c681776c30c6e22cf18adde6a93b22` will be tracked by git further. 

why this is helpful ? the changes you made in `N` number of files. will be saved under the commit ID incase there is something went wrong, you can open the commit and check what was the issue. This gets crucial when high number of people are working on a single project. 

in simple words, code saved was shipped with commit ID `b7478..`



### But If you forgot to add one more file to the commit :

One simple solution is to add the left over file and commit it. 

Other way would be to revert the previous commit and add the file and create a commit again.

Revert the previous commit :
```bash
git reset HEAD~
```

Add all the relevant files now.

```bash
git add .
```
Now, commit it.

```bash
git commit -m "add example code"
```
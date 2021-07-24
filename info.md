## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Starter pack](#starter-pack)

## General info
This is main source of git cheetsheet^manual. 

## Technologies
git basic commands:
configure new repository, connect to branch, switch branch, push, pull and more...
	
### Starter pack
Here come some notes how to use git and stuff like that 

```
git config --global user.name "Sam Smith" 	### Configure the author name and email address to be used with your commits.  ---> Tell git who you are
git config --global user.email sam@example.com	### Note that Git strips some characters (for example trailing periods) from user.name.

git init 					### Create new local repository
git clone /path/to/repository			### Create a working copy of a local repository:
git clone username@host:/path/to/repository	### For a remote server, use:
git add <filename>				### Add files to git

git commit -m "Commit message"			### Commit changes to head (but not yet to the remote repository):
git commit -a					### Commit any files you've added with git add, and also commit any files you've changed since then:
git push origin master				### Send changes to the master branch of your remote repository:
git status					### List the files you've changed and those you still need to add or commit:
git remote add origin <server>			### If you haven't connected your local repository to a remote server, add the server to be able to push to it:
git remote -v					### List all currently configured remote repositories:

git checkout -b <branchname>			### Create a new branch and switch to it:
git checkout <branchname>			### Switch from one branch to another:
git branch					### List all the branches in your repo, and also tell you what branch you're currently in:	
git branch -d <branchname>			### Delete the feature branch:
git push origin <branchname>			### Push the branch to your remote repository, so others can use it:	
git push --all origin				### Push all branches to your remote repository:	
git push origin :<branchname>			### Delete a branch on your remote repository:	

git pull					### Fetch and merge changes on the remote server to your working directory:
git merge <branchname>				### To merge a different branch into your active branch:
git diff					### View all the merge conflicts:
git diff --base <filename>			### View the conflicts against the base file:
git diff <sourcebranch> <targetbranch>		### Preview changes, before merging:
git add <filename>				### After you have manually resolved any conflicts, you mark the changed file:
git tag 1.0.0 <commitID>			### You can use tagging to mark a significant changeset, such as a release:
git log						### CommitId is the leading characters of the changeset ID, up to 10, but must be unique. Get the ID using:
git push --tags origin				### Push all tags to remote repository:

git checkout -- <filename>			### If you mess up, you can replace the changes in your working tree with the last content in head:
						### Changes already added to the index, as well as new files, will be kept.
git fetch origin				### Instead, to drop all your local changes and commits,
git reset --hard origin/master			### fetch the latest history from the server and point your local master branch at it, do this:
git grep "foo()"				### Search the working directory for foo():

```

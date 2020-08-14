---

---

# Git and Github

## Terminology

**Git** - version control software that you use at the command line to keep track of edits to your scientific codes over time.

**GitHub** - an online repository hosting service where you can archive your scientific codes online. You can [create a free personal Github account](https://github.com/join) where you can archive your scientific codes into different “repositories” within your account. If you keep your Github repos up to date, it also allows you (and collaborators) to access your codes from anywhere.

**repository (repo)** - A directory or storage space where your projects can live. A repo can be a local folder on your laptop/HPC system (local repo) or it can be a storage space on GitHub (online/remote repo). Inside a repo is where you keep your code files, text files, etc. Generally, each of your local repos is also associated with an online Github repo called a "remote" repo.

**clone** - the process of copying an entire existing Github repo to your computer (copying to a local repo)

**fork** - the process of copying an entire existing Github repo to your own Github account (copying to an online repo)

**branch** - each branch in a repo is an isolated space where you can work/develop your codes without affecting the work saved in other branches. Each repository has one default branch called Master (soon to be renamed Main) and can have multiple other branches. A new branch is always created from an existing branch. The following example is one way to use branches effectively. If you have a functioning code on the Master branch and you want to experiment with code changes without affecting your functioning code on Master, you can create a new branch called Dev, for example. You could then make changes to your code on the Dev branch which would be entirely separate from your code on the Master branch. If you like your changes, you could incorporate them into your code on the Master branch by merging the Dev branch into the Master branch. 

**commit** - the process of saving a "snapshot" or versions of your files. Similar to saving a file that's been edited, a commit records your changes to one or more files on a branch. Git assigns each commit a unique ID that indentifies the specific changes, when the changes were made, and who created the changes. When you make a commit, you also attached a short description of the changes you made. It's wise to group similar edits together and include them in a single commit and also to commit your changes every so often so that you have a good number of "snapshots" available to you in case you break your code and need to look back to earlier versions. For example, you could code all day and do one commit at the end of the day and have one snapshot/version of your code, but it may be more useful to commit more often that way you will have multiple snapshots of your work throughout the day that you could revert back to if necessary. 

**stage** - the process of "telling Git" which edited files should be included in each commit that you make. Just because you change a file in your repo does not mean that it will be automatically included in your repo snapshot when you commit. You must first "stage" the edited files so that Git knows how to make the snapshot.

**pull** - the process of updating your local repo to include changes made to the remote (online) repo. You "pull" down any edits from the online repo and merge them into your local repo. 

**push** - the process of updating your online remote repo with the changes you have made to your local repo. You "push" up any edits from your local repo and merge them into your online remote repo.

**pull request** - the process of requesting that changes you have made to your repo branch be incorportated into someone else's version of the repo. For example, you fork (copy) someone's existing Github repo to a repo on your own Github account and you then make changes to some of the files. If you want the original repo that you copied from to incorporate your changes into their repo, then you would make a pull request. It is called a pull request because you are requesting that someone else pulls and merges your edits into their online repo.

**merge** - the process of combining multiple sequences of commits into one unified history. Most often used to incorporate changes from one branch into another. A merge happens when you pull, push, and pull request.


## Using Git & Github to Archive and Version Your Codes

### A Workflow Starting From Github

This example workflow demonstrates how to:
  - copy an existing Github repo to your own Github account,
  - make a local copy of your Github repo on your computer (in this case your Ceres account)
  - make changes to the repo files locally, 
  - push your local repo changes to your Github repo, and 
  - have your repo edits incorporated back into the online repo that you originally copied from on Github. 


Step 1: Fork a Github repo (on Github, copy an existing Github repo to your own Github account)
a. Login to [Github](https://github.com/) with your username and password.
b. Find the Github repo that you want to copy. Let's copy the repo called "Spoon-Knife" on Kerrie Geil's Github page.
  - In the black Github search bar at the top left where it says "Search or jump to", type kerriegeil, and select the dropdown list option that says search kerriegeil All Github.
  - On the bottom of the resulting menu click Users, then click Kerrie Geil on the right to see all the public repos on her account.
  - Click on the Spoon-Knife repo. You should be here: https://github.com/kerriegeil/Spoon-Knife.
c. Click Fork on the top right of the repo page and then click on your github username when you are asked where to fork to. You have now copied the repo to your own account. Notice the URL you are at- it should be github.com/yourusername/reponame


Step 2: create a local repo on Ceres from your Github repo (git clone)
a. SSH into your Ceres account from a terminal/command line. See the [Ceres Quick Start Guide](https://scinet.usda.gov/guide/quickstart#accessing-scinet) for instructions.
b. Navigate to the location on Ceres where you want to copy the repo. It's small so putting it in your home directory is fine (~/home/username).
c. Go back to Github to get the URL of your Github repo. On your repo page, click the green Code button to find the repo address. It should be in the form https://github.com/username/reponame.git
d. Back at the command line type the following to make a local copy of your Github repo
```git clone paste_or_type_the_repo_URL```


Step 3: make changes to your local repo and make multiple commits to create a series of "snapshots" of your changes (make edits, git add, git commit -m "message")
a. create some new text files using your name as the file name
```touch yourname1.txt yourname2.txt yourname3.txt```
to see the files you just created
```ls```
b. check the status of your edits. The changed files should appear as untracked files
```git status```
c. stage the edits before committing. You are "telling Git" what files you want to include in a future commit.
```git add yourname1.txt```
```git add yourname2.txt yourname3.txt```
d. check the status of your edits. The changed files should now appear as changes to be committed
``git status```
e. commit the edits to include them in a snapshot of your updated local repo
```git commit -m "create new text files"```
f. check the status of your edits again. The changed files should no longer appear. If you've committed all your changes you should see "nothing to commit, working directory clean" 
```git status```
g. Let's do it again. Edit the file hi-my-name-is.txt to include your name
```nano hi-my-name-is.txt```
Type your name, then hit Ctl+O then enter to write, Ctl+X to exit
h. Stage your edits
```git add hi-my-name-is.txt```
f. another commit
```git commit -m "update with my name"```
g. check the status of the changes, working directory should now be clean meaning all changes have been committed to an updated "snapshot"
```git status```


Step 4: Push your local changes up to your remote repo on your Github account
a. if you want to double check what remote repo(s) is/are associated with your local repo, at the command line type
```git remote -v```
you should see that your remote repo is called "origin" for short and that the URL to the remote repo is https://github.com/yourusername/reponame.git, the same URL we used when we cloned the repo to your local computer
b. push your local changes to your remote repo on your Github account with
```git push origin```
c. Go back to your repo on Github and refresh the page. You should see your new files appear now on Github


Step 5: Make a pull request to the original repo (request that your changes be incorporated into the original repo)
a. To add your repo changes into the original repo at kerriegeil/Spoon-Knife navigate back to that original repo page
b. Now submit a pull request. You are requesting that kerriegeil incorporate ("pull") your edits into her repo
  - click the Pull Requests tab
  - click the green New Pull Request button
  - click the link near the top that says "compare across forks"
  - ensure the base repository is kerriegeil/Spoon-Knife and the base branch is Master (left side of the arrow)
  - ensure that the head repository is yourusername/Spoon-Knife and the compare branch is Master (right side of the arrow)
  - click the green Create Pull Request button. The fate of your pull request now lies with the owner of the original repo

Additional workflow tips:

If you are collaborating with someone on Github it is good practice to pull down any changes from the main repo to your local repo every time you begin working on your local repo. This way you can avoid merge conflicts later. If you have the remote repo that you are collaborating on set to "origin" you can simply type the following to fetch and merge remote changes to your local repo:
```git pull```

There are two ways to see every available snapshot of your repo (history of commits). On Github in your repo, click the commits link located right under the green Code button. From the command line:
```git log``
We won't cover how to revert your repo to a previous commit in this tutorial but you should know that commit number you see on Github commits or in the git log output at the command line is what you need to access an earlier version of your repo.




### A Workflow Starting From the Command Line
Sometimes you'll want to start a brand new local repo right from the command line and then push your local repo up to Github. Here's how to do it.

Step 1: Initialize a new local git repository
a. Create a new local directory where you want your new local repo to live and navigate into it
```mkdir my_new_repo```
```cd my_new_repo```
b. Initialize a new local git repository
```git init```

Step 2: Edit away!
adding content to your local repo is the exact same process as Step 3 in the previous workflow

Step 3: create a remote repo on Github and push your local repo up to your Github repo
a. login to your Github account
b. navigate to your repositories page, click the green New button
c. give your new Github repo the same name my_new_repo
d. you can skip the section about creating a readme, license, gitignore because you'll be importing an existing repo
e. follow the instructions to push an existing repo from the command line
  - ```git remote add origin https://github.com/yourusername/my_new_repo.git```
  - ``git push origin```
f. refresh your Github repo page, you should see all your local files now in your Github repo





# Conda
terminology
conda, packages, environment, specfile, yml

## Accessing Conda on Ceres
### From the Module System
### User Install

## Conda Environments
create
install
view packages
change env
view envs
export env to spec file

## 

# Containers (Docker and Singularity)
terminology
image, container, Docker, DockerHub dockerfile, Singularity

## Accessing an Existing Docker Image

## Running a Container on Ceres
singularity runs docker images  

## Creating a New Docker Image from an Existing Image
dockerhub
dockerfile
getting it on Ceres


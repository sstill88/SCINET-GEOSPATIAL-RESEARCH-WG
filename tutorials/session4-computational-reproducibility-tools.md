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

**staging** - the process of "telling Git" which edited files should be included in each commit that you make. Just because you change a file in your repo does not mean that it will be automatically included in your repo snapshot when you commit. You must first "stage" the edited files so that Git knows how to make the snapshot.

**pull** - the process of updating your local repo to include changes made to the remote (online) repo. You "pull" down any edits from the online repo and merge them into your local repo. 

**push** - the process of updating your online remote repo with the changes you have made to your local repo. You "push" up any edits from your local repo and merge them into your online remote repo.

**pull request** - the process of requesting that changes you have made to your repo branch be incorportated into someone else's version of the repo. For example, you fork (copy) someone's existing Github repo to a repo on your own Github account and you then make changes to some of the files. If you want the original repo that you copied from to incorporate your changes into their repo, then you would make a pull request. It is called a pull request because you are requesting that someone else pulls and merges your edits into their online repo.

**merge** - the process of combining multiple sequences of commits into one unified history. Most often used to incorporate changes from one branch into another. A merge happens when you pull, push, and pull request.


## Using Git & Github to Archive and Version Your Codes
### A Workflow Starting From Github
copy existing repo to SCINet account
make changes in a series of commits
push repo online
pull request

git pull to update local repo before working every time
show how to access all the code versions
ASK ROWAN IF HE HAS A GOOD VERSION NAMING/SAVING METHOD

### A Workflow Starting From the Command Line
git init
push to repo online...


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


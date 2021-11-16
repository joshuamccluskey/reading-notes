# Revisions and the Cloud
## Read 03
### Joshua McCluskey

#### Version Control:
A system to track, revisit, record, compare, and changes. 

#### Local version control
Version on your computer

#### Centralized Version Control 
A single server storing all chanded in a Centralized Version Control System facilitates collaboration in a team

#### Distrubuted Version Control
Address single point of failure of the CVS single server and DVCS advantage facilitates back ups and stored in more than one location.

#### Git
- DVCS takes snapshots each time saving a project
- Local operations changes made save on local disk
- Tracking chaning always detects file corruption or info loss
- States
  - Commited: Data stored on local database
  - Modified: File changed but not saved/comitted
  - Staged: Fags file's changed version to be committed in the next snapshot

#### Git History
- Open source software project Linux kernel
- Bitkeeper a DVCS in 2002
- Linus Travolds begins creating Git
- Non linear development with multiple branches

#### MAC
Go to terminal and type `git` install if not found

#### Windows
[For Git Download](http://git-scm.com/download/win)

#### Linux
#### For Fedora:

    $ sudo yum intall git
    
#### For Ubuntu

    $ sudo apt-get intall git


#### Customize Git

```
git config --global user.name "Name Name"

git config --global user.email "email@email.com"

```

#### To confirm:

```
git config --global user.name (should return Name Name)

git config --global user.email (should return email@email.com)

```

#### Default text editor:

Configure for your default text editor example below emacs

    $ git config --global core.editor emacs

#### Check git settings

    $ git config --list
    
#### Git Help...Get it...haha

```
git help command

git command --help

man git-command

```

#### Settigng up Git Repository (Repo)

1. Go to target projects repository `$ cd test (cd = change directory)`
2. Use git init `$ git init`
3. Track and excute inital commit `$ git add *.c` next `$ git add LICENSE` next `$ git commit -m “any message here”`

#### Cloning

Go to GitHub and click green button top right of repo youo want to clone and copy and paste url. Ex: `$ git clone https://github.com/test`


Clone to different directory `$ git clone https://github.com/test mydirectory`

#### Local Repo

Working Directory -> Index -> Index -> Head

Working Directory: Acutal files location

Index: Area for staging

Head: Point to current commit

Tracked: Modified, unmodified, or stages

Untracked: not last snapshot and not in staging area


#### Life Cycle of File

- Git flags file modified
- You stage modified file
- commit staged modified file

#### Check Status

    $ git status
    
    
#### Tracking and Staging New File

Single File: `git add filename`

All Files: `$ git add *`


#### Committing a File

    $ git commit -m “made change x,y,z”
    
#### Committing all changes

    $ git commit -a
    
#### Pushing Changes

    $ git push origin master
 
 #### Pushes from local *master* branch to remote repo *origin*
 
 Not Sure of Committing then Stash
 Stash it and revist with apply
 
     git stash
     
     git stash apply
 
#### Seeing Your Remotes

    git remote
    
    
#### View all remote

    git remote -v
    
[<== BACK](README.md)

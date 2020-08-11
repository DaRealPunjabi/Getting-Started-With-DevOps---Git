# Create a remote, empty repository on Github

1. Login to your Github account.

2. At the top right of any Github page, you should see a '+' icon. Click that, then select 'New Repository'.

3. Complete the basic details - With the name only

> Repository name : Ideally meaningful name that will match your local repository **hello-world-app** <br />
> Description (optional) : **LEAVE** blank <br /> 
> Public : **KEEP** selected <br /> 
> Initialize this repository with a README : **KEEP** unselected <br /> 

4. Click 'Create Repository'. **This will show a new page with instructions to create a new local repository from the command line**


# Create a local repository

1. Open the terminal and create a project directory
```
  mkdir hello-world-app
  cd hello-world-app
```

2. Create a new local repository
```
  git init
```

Initialized empty Git repository in /Users/darealpunjabi/Projects/workspace/**hello-world-app**/.git/

3. Create a README.md for the project
```
  echo "# Getting started with my first app" >> README.md
```

4. Checking the status of our repository
```
  git status
```

> On branch master <br /> 
> No commits yet <br /> 
> Untracked files: <br /> 
> (use "git add <file>..." to include in what will be committed) <br /> 
> &nbsp;&nbsp;&nbsp;&nbsp;**README.md** <br /> 
> nothing added to commit but untracked files present (use "git add" to track) <br /> 

Untracked files are any files in your working directory that were not in your last snapshot and are not in your staging area.
https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository

5. Tracking new files
```
  git add README.md
    or
  git add .              # To stage all new/modified file
```

6. Checking the status of our repository
```
  git status
```

> On branch master <br /> 
> No commits yet <br />
> Changes to be committed: <br />
> (use "git rm --cached <file>..." to unstage) <br />
> &nbsp;&nbsp;&nbsp;&nbsp;new file:   **README.md** <br />

Staged files are under the “Changes to be committed” heading. If you commit at this point, the version of the file at the time you ran git add is what will be in the subsequent historical snapshot

7. Ignorining files
```
  echo .DS_Store >> .gitignore
```

"Desktop Services Store" is a hidden file that contains attributes of a folder. Navigating to a folder using the "Finder" on Mac generates a .DS_Store file. Setting up a .gitignore file for the new repository at the start avoid committing files that are not wanted in the Git repository.

7. Committing the changes
```
  git commit -m "first commit"
```


> [master (root-commit) 0daf9f8] first commit <br />
> 1 file changed, 1 insertion(+) <br />
> create mode 100644 README.md <br />

A commit records the snapshot of the staging area. These points “safe” versions of a project that can reverted if required.

8. Show commit logs
```
  git log
```

> Date:   Tue Aug 11 12:14:33 2020 +0100 <br />
> first commit <br />

This command is used to view commit history of the repository current branch.


9. Link local **Git** repository to remote **Github** repository
```
  git remote add origin https://github.com/DaRealPunjabi/**hello-world-app**.git
```

Specifying origin indicates the **origin** will be hosted on remote **Github**.

10.  Push the changes to Github
```
  git push -u origin master
```
> Enumerating objects: 7, done. <br />
> Counting objects: 100% (7/7), done. <br />
> Delta compression using up to 4 threads <br />
> Compressing objects: 100% (6/6), done. <br />
> Writing objects: 100% (7/7), 2.61 KiB | 2.61 MiB/s, done. <br />
> Total 7 (delta 0), reused 0 (delta 0)<br />
> To https://github.com/DaRealPunjabi/Getting-Started-With-DevOps---Git.git <br />
> &nbsp;&nbsp;&nbsp;&nbsp;* [new branch]      master -> master <br />
> Branch 'master' set up to track remote branch 'master' from 'origin'.<br />

This will push the changes to the master branch.


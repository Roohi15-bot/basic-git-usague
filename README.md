# basic-git-usague
-Git is the version control system(vcs) github uses and it is a distributed version control system
-git is the open source and free to use for small and large projects
-Github meanwhile is where people can share and collaborate on the files they have created 
git is used for-history tracking
               -branching and merging
               -collaboration
               -reverting
               -backup and recovery

##git init (initializing repositories)
-A repository (or "repo") is where Git stores all the files and the history of changes for your project. 
-The git init command creates a new, empty repository in a directoThe git init command creates a new, empty repository in a directory.
--------------------------------------steps--------------------------------------------------------------------
1)Open a terminal: Open your command-line tool.
2)Navigate to your project folder: Use the cd command to go to the directory where you want to create your project (e.g., cd /Users/yourname/myproject).
3)Initialize the repository: Type:
git init
and press Enter.
4)Verify: Git will create a hidden folder named .git inside your project directory. This folder contains all the repository's information.

##git add (adding changes to staging):-
1)When you make changes to files in your project, Git needs to know which changes you want to include in the next snapshot (commit).
2)The git add command moves these changes from your working directory to the staging area (also called the index).
3)The staging area is like a preparation zone for your next commit.
---------------------------------------------------------steps-------------------------------------------------
1)Modify files: Make some changes to the files in your project.
2)Add specific files: To add a specific file, use:
git add <filename>
(e.g., git add myFile.txt).
3)Add all changes: To add all changed files in the current directory and its subdirectories, use:
git add .
4)Verify: Use git status to see which files are staged. They will be listed in green.

##git commit (committing changes)
-A commit is a snapshot of your changes at a specific point in time. 
-The git commit command takes the changes from the staging area and saves them as a new commit in the repository's history. 
-You must include a message with each commit to describe the changes you made.
---------------------------------------------------steps------------------------------------------------------
1)Stage your changes: Use git add to add the changes you want to commit.
2)Commit the changes: Type:
git commit -m "Your descriptive commit message"
and press Enter. Replace "Your descriptive commit message" with a clear description of your changes (e.g., "Fixed a bug in the login function", "Added new styling to the header").
3)Verify: Use git log to see the commit history. Your new commit will be listed.

##git reset (unstaging changes)
-The git reset command is a powerful tool that can be used to undo changes in Git. 
-When talking about unstaging changes, git reset removes files from the staging area, but it leaves the actual file modifications in your working directory.
-----------------------------------------------------steps-----------------------------------------------------
1)Stage files: Use git add <file> to add changes to the staging area.
2)Unstage a file: To unstage a specific file, use:
git reset <file>
(e.g., git reset myFile.txt).
3)Verify: Use git status to check the status of your files. The file will no longer be listed as staged, but your changes will still be in the file.

##gitignore file usage
Sometimes, there are files in your project that you don't want Git to track (e.g., temporary files, log files, files containing sensitive information).
The gitignore file is a special file that tells Git which files or patterns of files to ignore.
--------------------------------------steps--------------------------------------------------------------------
1)Create a .gitignore file: In the root directory of your Git repository, create a new file named .gitignore (without any file extension).
2)Add patterns: Open the .gitignore file in a text editor and add patterns for the files you want to ignore. Each pattern should be on a new line.
*.log
temp/
config.js
*.log: Ignore all files with the .log extension.
temp/: Ignore the temp directory and everything inside it.
config.js: Ignore a specific file named config.js
3)Save the file: Save the .gitignore file.
4)Verify: Git will now ignore the files that match the patterns in your .gitignore file. They won't show up in git status as untracked files.

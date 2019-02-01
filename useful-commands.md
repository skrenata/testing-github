# Useful git commands

Some of these are likely to be innacurate / wrong, as I'm still learning.

Note to future self: "commit" is basically a synonym for "update" in git jargon.

### git status
Checks the status of the current directory. It tells you what stuff has been changed, marked for tracking and so on.

### git clone https://github.com/[path]
Clones a repository from GitHub into the current directory.

### git pull https://github.com/[path]
Gets most recent info from GitHub from the target repository to the current directory.

### git add [filename] (or .)
Adds (all) files to the local git index (preparation before doing a commit). You'd do this after editing any stuff locally, in order to later update them to GitHub.

### git rm [filename]
Removes files from local git index (preparation before doing a commit).

### git commit -m "short message describing changes" [filename1 filename2] (or -a)
Updates and stores the current index (see add / rm above), together with a log message. Use option -a commits all files in the directory.

### git push origin [branch]
This will update the specified [branch] in your original GitHub directory, using the current index (usually after a commit). It will ask for your GitHub login / password.  
- If you're happy with all the changes you made locally, you can merge this directly to the master branch. 
- If you're still testing things, you might want to create a separate branch to keep track of changes until you're sure all is well.

### git branch
Lists all existing branches, highlighting in which one you're working at the moment.

### git branch [branchName]
Create a new branch.

## git checkout [branchName]
Switches to a different branch.

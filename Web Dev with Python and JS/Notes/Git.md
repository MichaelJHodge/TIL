Notes

Git: A version control tool in order to maintain different versions and organize code. 
- Git can keep track of changes made to code, synchronize code between different people, test changes to code without losing the original, and revert back to old versions of code.
- GitHub is a website that stores Git repositories on the internet to facilitate the collaboration that Git allows for. A repository is simply a place to keep track of code and all the changes to code.

GIT COMMANDS:

- git clone <url> : take a repository stored on a server (like GitHub) and downloads it
- git add <filename(s)> : add files to the staging area to be included in the next commit
- git commit -m "message" : take a snapshot of the repository and save it with a message about the changes
- git commit -am <filename(s)> "message" : add files and commit changes all in one
- git status : print what is currently going on with the repository
- git push : push any local changes (commits) to a remote server
- git pull : pull any remote changes from a remote server to a local computer
- git log : print a history of all the commits that have been made
- git reflog : print a list of all the different references to commits
- git reset --hard <commit> : reset the repository to a given commit
- git reset --hard origin/master : reset the repository to its original state (e.g. the version cloned from GitHub)


‘Branching’ is a feature of Git that allows a project to move in multiple different directions simultaneously. There is one master branch that is always usable, but any number of new branches can be created to develop new features. Once ready, these branches can then be merged back into master.

When working in a Git repository, HEAD refers to the current branch being worked on. When a different branch is ‘checked out’, the HEAD changes to indicate the new working branch.


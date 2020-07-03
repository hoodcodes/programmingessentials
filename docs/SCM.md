##### Source Control Management



<ins>Git<ins>

Becoming a Git Ninja

Git - A distributed version control system. 

Benefits:
You can get a full copy of a repo downloaded locally, work with it offline, having full history of all code changes, and make new branches, commits, and merges locally.  
Other ‘peers’ can do the same.  When you are ready to push your changes up to the remote (origin) repo, you can push a new branch, submit a pull request, and have changes merged at that time.  
You can pull down branches (unmerged) which have been pushed up by other peers.  



Branching 
Branching allows you to work on code in isolation with others
Branches are intended to be merged eventually
Branches have a traceable history to their parents

Branching Patterns
75 pages  by the ALM Rangers:  https://vsardata.blob.core.windows.net/projects/TFS%20Version%20Control%20Part%201%20-%20Branching%20Strategies.pdf 


.gitignore


practice of committing OFTEN.  Every significant change to code.  


Cherry Picking


Reverting    


Pull Requests   








Visual Studio Code integration with GitHub
associate your identity with Git and authenticate with GitHub
Create and set your username (can be anything)
git config --global user.name "Christopher Hood"
Then verify your username was set correctly:
git config --global user.name
Set your commit email address:
git config --global user.email git@cshood.com
Then verify your commit email address as set correctly:
git config --global user.email
cache your github password:
git config --global credential.helper wincred


view your remote branches:
git remove -v

Setting upstream remote:
git remote add upstream <git path>
example:git remote add upstream  https://github.com/cshood/mslearn-tailspin-spacegame-web.git




Tricks:

start making changes and you are in the wrong branch:
git stash  (stash the changes)
git co -b <new branch name>  OR  git checkout <existing branch name>
git stash apply  (apply the stashed changes to the intended branch




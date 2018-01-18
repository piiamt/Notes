We looked at a few things, and tried a few things:


1 We investigated how GIT works, and what it is doing.  We talked a little about why it works that way.

2 We set up account and installed the pieces of software on our computers that are needed to work with GIT.
  * Create an account on GitHub
  
  * Windows
    Install GitBash.  Durring the install, select the option that doesn't change the cmd window, and select notepad++ as the editor (install it from the link on that part of hte gitbash installer)
    
  * Mac OSX
    Install the Git tools.
    
3 We walked through multiple tasks on Git
  1 GitHub interaction
  * On GitHub, we gained access to a repo (IntroToGit)
  * We cloned this to our account.
  * We added a file with our name and the extension .md
  * We committed this to the cloned repo in our account.
  * We created a pull request to have the change pulled from our cloned repo to the original repo on the class account.
  2 when something doesn't work
  * We added a line to a file that already existed in the repo.
  * We commited our chagne to the repo on our account.
  * We attempted to create a pull request to the class repo, however someone had made a change between when we checked this file out, and now.
  * Thus there was a conflict that we needed to resolve.
  * Resolving this on GITHub through it's text editor may take two attepts to take effect.
  3 working iwth local files
  * We cloned the repo on our account to the computer hard drive (Note this is the first Git step that we are doing that has changes on our local computer.)
  * We made changes.
  * We looked at the status of things with: git status
  * We added the files with: git add -A
  * We again checked the status.
  * We committed the changes to the repo on the machine we were working on with: git commit
  * This brought up a text editor to add a comment that describes our change.
    * Note: that the text needs to be on the first line.
    * Also: if you are in notepad++, you can type in your comment, save, and then close the window.  If you selected a different editor, you make the change, save and quit to finish this step.
  * We once again looked at git staus to see what it said.
  * We also looked at git log to see that our commit was known by Git.
    * Note: type the letter 'q' to exit the log.
  * We then went and looked at our repo on GitHub, and noticed that our change was not there.
  * We pushed our changes up to our repo with the command: git push origin master
    * This is saying that we want to push our commited changes to the repo named origin, and it's branch named master.
  * We once again checked on our repo on GitHub to see that now the change was there.
  * We now could create a pull request to have that change be pulled into the class repo if we wanted.

You probably want to review the **Git Basics** book at some point but just to have the
essentials so you can be using git to update your homework assignments here's
some easy steps. (This assumes you are comfortable using the shell on your machine. Snippets starting with `$` are shell commands. Also assumes you have a github account, and git installed locally.) I have also linked to the github docs, honestly you are probably better off following their directions in the future instead of mine.


# Easy github directions:

+ [Initialize new repository](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/creating-a-new-repository) from your github account
+ [clone the repository](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/cloning-a-repository) to your machine
+ [add files to the repository](https://docs.github.com/en/free-pro-team@latest/github/managing-files-in-a-repository/adding-a-file-to-a-repository-using-the-command-line)
+ [make your first local commit](https://github.com/git-guides/git-commit)
+ [push your commit to github](https://docs.github.com/en/free-pro-team@latest/github/using-git/pushing-commits-to-a-remote-repository)

## Initialize new repository
Can be done locally but this is the order I do it in:

Sign into your GitHub account use the plus sign in the upper right hand corner of the page to select new repository. You can make a seperate repository for each course in **Launch School**. Use the option to intialize with a readme. Make your repository public.

## Clone the repository to your machine
+ In your shell on your machine navigate to where you want your new repo to live. I keep all my Launch School stuff in Documents/ls_files.
+ From your new github repository use the green `Code` button copy the HTTPS url from the dropdown dialouge box. 
+ Use the command `git clone` pasting in the URL. (ctrl+shift+v to paste in shell)
```
$ git clone https://github.com/username/repo_name.git
```

+ In your shell type `ls` to show the new directory containing your repo is there. Navigate into your repository directory using `cd`. Type your new favorite command `git status` to see whats going on with your repo.

## Add files to the repository
+ Your repo only has a README so far, copy/move all your directories/files to this directory. You should have a seperate directory for each lesson of the course.
+ Type `git status` you'll now see that git lists what you have saved in the directory as untracked files. You now need to add these files to be tracked by git.
+ You can individually add files using `git add filename.rb`, or in this case it's easier to just add everything all at once using
```
$ git add -A
```
+ Use `git status` again to see that everything is now staged for commit.
add

## Make first local commit
+ Now you will make a commit, saving the status of all our tracked files
+ The most potentially confusing part of this step as a begginer is adding a commit message. By default the command `git commit` opens your shell's default text editor which might be Vim, this can be really confusing if you have never used Vim before. We will avoid this by using the `-m` flagg to add our message without a text editor.
+ ```git commit -m "Initial dump of already complete files" ```
+ A good commit message should help you know what changes were added to the repository for this commit. If you are adding homework problems say something like `"finnished easy2 exercises"`. If you are making slower progress on a larger program explain what features or refactoring you did.
+ Try `git status` again see that there are no files to track, everything was included in your last commit but there is a new message to look at
```
Your branch is one commit ahead of 'origin/master' by 1 commit
```
+ Now you need to push this commit to github to get your remote repository up to date with your local repository.

## Push your commit to github
+ You can check the *name* of the remote repo git is set to using `git remote`.
+ Since you initialized this repo on github this is already setup. Otherwise you would need to use `git remote set-url <name> <newurl>` 
+ `git config --get remote.origin.url` will show you the url you used to clone this repository from github in the first place.
+ This step is pretty straight forward use the command `git push <remote name>`. github will prompt you for credentials to securely push to your repository.
``` $ git push origin
Username for 'https://github.com': <username>
Password for 'https://devinbremmeyr@github.com': *****
```
+ If you don't want to have to type in these credentials every time you can set up *SSH* instead. It's not that hard just look for a guide in the github docs.
+ Use `git status` to see that your local branch is up to date with 'origin/master'.
+ Go to your github account and see all your files are now present in the repository on github, *great success*

## Now what?
+ as you work type `git status` once and while to see if you are keeping things up to date.
+ keep commiting: The whole point of version control is having saved versions of your work so you can roll things back to a working state. The goal is to incorporate git into your workflow and have good commit hygine.
+ google is your friend! If you forget a command or how to do a step there are lots of guides out there to help.
+ You can also use `git --help` or for a specific command e.g. `git add --help`
+ When you start a new course, make a new repository to orgainize your code on github.

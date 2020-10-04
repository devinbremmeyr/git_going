You probably want to review how git works at some point but just to have the
essentials so you can be using git to update your homework assignments here's
some easy steps. (This assumes you are comfortable using the shell on your machine. Snippets starting with `$` are shell commands.)


# Easy github directions:

+ [Initialize new repository](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/creating-a-new-repository) from your github account
+ [clone the repository](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/cloning-a-repository) to your machine
+ add files to the repository
+ make your first local commit
+ push your commit to github

## Initialize new repository
Can be done locally but this is the order I do it in:

Sign into your GitHub account use the plus sign in the upper right hand corner of the page to select new repository. Use the option to intialize with a readme.

## Clone the repository to your machine
+ In your shell on your machine navigate to where you want your new repo to live. I keep all my Launch School stuff in Documents/ls_files.
+ From your new github repository use the green `Code` button copy the HTTPS url from the dropdown dialouge box. 
+ Use the command `git clone` pasting in the URL. (ctrl+shift+v to paste in shell)
```$ git clone https://github.com/username/repo_name.git
```

+ In your shell type `ls` to show the new directory containing your repo is there. Navigate into your repository directory using `cd`. Type your new favorite command `git status` to see whats going on with your repo.

## Add files to the repository
+ Your repo only has a README so far, copy/move all your directories/files to this directory. You should have a seperate directory for each lesson of the course.
+ Type git status you'll now see that git lists what you have saved in the directory as untracked files. You now need to add these files to be tracked by git.
+ You can individually add files using `git add filename.rb`, or in this case it's easier to just add everything all at once using
```
$ git add -A
```
+ Use `git status` again to see that everything is now staged for commit.
add 
## Make first local commit

## Push your commit to github

## Now what?
git status
keep commiting
google is your friend!

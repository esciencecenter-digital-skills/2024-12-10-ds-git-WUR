![](https://i.imgur.com/iywjz8s.png)


# Collaborative Document

2024-12-10 ds-git-WUR

Find this collaborate document: tinyurl.com/git-wur-2024


## Teaching material

[Version control with Git](https://swcarpentry.github.io/git-novice/), developed by [the Carpentries Community](https://carpentries.org/)
 

## 👮Code of Conduct

Participants are expected to follow these guidelines:
* Use welcoming and inclusive language.
* Be respectful of different viewpoints and experiences.
* Gracefully accept constructive criticism.
* Focus on what is best for the community.
* Show courtesy and respect towards other community members.
 
## ⚖️ License

All content is publicly available under the Creative Commons Attribution License: [creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/).

## 🙋Getting help

To ask a question, just raise your hand.

If you need help from a helper, place a green post-it note on your laptop lid. A helper will come to assist you as soon as possible.

## 🖥 Workshop website

🛠 Setup

Please check the "Setup" section of the registration page: [link](https://www.wur.nl/en/library/students/courses-and-demos-students/courses-and-demos-display/get-into-git-one-day-workshop-on-collaboration-with-git.htm)


## 👩‍🏫👩‍💻🎓 Instructors & Helpers

Ou Ku, Johan Hidding, Louis Henry
  

## 👩‍💻👩‍💼👨‍🔬🧑‍🔬🧑‍🚀🧙‍♂️🔧 Roll Call
Name/ pronouns (optional) / job, role / social media (twitter, github, ...) / background or interests (optional) / city


## Put .git repository outside (Teams)directory
Git puts a .git directory in the directory where you want version control. This is not handy in a onedrive directory (as all files in the .git may start synchronizing). 
If you want the .git directory somewhere else, use:

`git init --separate-git-dir c:\wherever\yourNameOfChoice.git`

Or:

`git clone git@git.wur.nl:yourBeautiful/Project.git --separate-git-dir C:\whereverYouWant\yourNameOfChoice.git`

Instead of a .git directory a .git file will be made. This file has a reference to the place where you have the .git

[Reference](https://rakhesh.com/coding/how-to-move-separate-the-git-folder-out-of-your-working-tree/)

## Troubleshooting: `ssh -T git@git.wur.nl` not working
```
ssh-keygen
```
Accept creating a key, then copy the path of the key and do:
```
cat PATH.pub
```
This should print your public key. Copy the text. They connect to the WUR gitlab, go to your profile (click on the avatar, profile preferences, keys) and click `add new key`. Paste the text of your piublic key there. Now try again the `ssh -T`


## 🗓️ Agenda
Morning
|  Time | Topic                                    |
| -----:|:---------------------------------------- |
| 09:30 | Welcome and icebreaker                   |
| 09:45 | Introduction to Git, setting up Git      |
| 10:45 | Coffee break                             |
| 11:00 | Creating a repository, tracking changes. |
| 11:50 | Coffee break                             |
| 12:00 | Exploring history, ignoring things       |
| 12:45 | Lunch                                    |

Afternoon
|  Time | Topic                                    |
| -----:|:---------------------------------------- |
| 13:45 | Remotes in GitLab                        |
| 14:45 | Coffee break                              |
| 15:00 | Collaboration with Git and GitLab        |
| 16:45 | Wrap-up                                  |
| 17:00 | END                                      |


## 🎓 Certificate of attendance
If you attend the full workshop you can request a certificate of attendance by emailing to training@esciencecenter.nl.

## 🔧 Exercises

### Exercise: Places to Create Git Repositories
Along with tracking information about recipes (the project we have already created), You would also like to track information about desserts specifically. You created a desserts project inside the recipes project with the following sequence of commands:


```shell=
$ cd recipes      # go into recipes directory, which is already a Git repository
$ ls -a           # ensure the .git subdirectory is still present in the recipes directory
$ mkdir desserts # make a sub-directory recipes/desserts
$ cd desserts    # go into desserts subdirectory
$ git init        # make the desserts subdirectory a Git repository
$ ls -a           # ensure the .git subdirectory is present indicating we have created a new Git repository
```

Is the git init command, run inside the desserts subdirectory, required for tracking files stored in the desserts subdirectory?

### Exercise: Committing Changes to Git
Which command(s) below would save the changes of myfile.txt to my local Git repository? (no need to execute the commands in your terminal)

```shell=
   $ git commit -m "my recent changes"
```

```shell=
   $ git init myfile.txt
   $ git commit -m "my recent changes"
```

```shell=
   $ git add myfile.txt
   $ git commit -m "my recent changes"
```

```shell=
   $ git commit -m myfile.txt "my recent changes"
```


- 1
- 2
- 3 :+1: :+1: :+1: :+1: :+1: :+1: :+1: :+1: :+1: :+1: :+1: :+1: :+1: :+1: :+1: :+1:
- 4 :+1:
- 5 
(good luck =)

### Exercise: Committing Multiple Files

The staging area can hold changes from any number of files that you want to commit as a single snapshot.

Add some text to guacamole.md noting the rough price of the ingredients.
Create a new file groceries.md with a list of products and their prices for different markets.
Add changes from both files to the staging area, and commit those changes.

:8ball: we will have chaos again


## Recovering Older Versions of a File
Jennifer has made changes to the Python script that she has been working on for weeks, and the modifications she made this morning “broke” the script and it no longer runs. She has spent ~ 1hr trying to fix it, with no luck…

Luckily, she has been keeping track of her project’s versions using Git! Which commands below will let her recover the last committed version of her Python script called data_cruncher.py?

- 1 `$ git restore`

- 2 `$ git restore data_cruncher.py`

- 3 `$ git restore -s HEAD~1 data_cruncher.py`

- 4 `$ git restore -s <unique ID of last commit> data_cruncher.py`

- 5 Both 2 and 4

1. :broken_heart:
2. :+1: :+1:
3. :+1: :+1: :+1:+1:+1 **[]**:+1:
4. 
5. :+1: :+1:   :+1:  :+1: :+1: :+1: :+1::+1::+1::+1::+1::+1: :+1: :+1: :+1:
6. 
    
    
## 🧠 Collaborative Notes

### Cheat sheet (command line)
(things after the # character are just notes - the command line does not execute them)
 Commands: 

- `pwd` **p**rints **w**orking **d**irectory, tells you where you are in your file system
- `ls`: **l**i**s**t current directory, shows all the files and directories that are there.
- `cd [DIR]`: **c**hanges working **d**irectory to DIR. Similar to when you double click on a directory in the file explorer 
- `mkdir [DIR]`: **m**a**k**es a **dir**ectory of the name DIR. This directory will be a perfectly normal directory as if you had clicked 'new' in your graphics user interface file explorer.
- `cat FILE`: prints out the content of a file on the screen

Other:

- `..`: parent directory. For instance `ls .. lists all files/directories in the parent directory of the current working directory
- `.` : current directory. `ls .` does the same thing as `ls`
- `~` : home directory
- `-` : previous working directory


### Cheat sheet (Git commands)


- git init: makes the current directory a Git repository
- git config --global parameter value: changes the parameter to a value in your configuration. Parameters we have seen are user.name user.mail and init.defaultbranch 
- git --version: shows the current version of Git you are running
- git status: shows the state of your Git repository, with files that have been modified since last commit, files that are in the staging area.
- git diff: shows the list of **tracked** files that are different from their committed state, and what the changes are.
- git log: see the history of commits.
Now the commands to add files:
- git add YOURFILE: moves YOURFILE to the staging area, where you can group all the changes you want to bundle into one **commit**.
- git commit -m "Your commit message": takes all the changes that are in the staging area, and make them part of your Git history.


### Welcome [Ou]

Step 1: Open the command line programme on your computer, for instance Git Bash. Command line will be explained in a next lesson, but this is a way to interact with your computer, similar to the Graphic User Interface you are used to.

Step 2: Type
```
git --version
```
and press ENTER. This should give you a message telling you which version your Git is on.

The relevant URL for the workshop is [this](tinyurl.com/git-wur-2024). If what you see looks like gibberish, make sure to click on the Eye icon on the top left of the page. The `gibberish` is Markdown language.

Markdown language uses # to mark different levels of titles, and * to start an itemisation. 


###  Introduction to Git, setting up Git [Johan]

Back to command line software ('terminal').

- Step 1: You need to configure Git before using it, adding your name and email address so that changes can be attributed to you.
```
git config --global user.name "Your Human-Readable Name"
#Press enter
git config --global user.email "YourEmailAddress"
#Press enter
```

Notes: do not put a space between `--` and `global`
Notes: do not forget the quote marks around your name and the email address

- Step 2: You now can check your git configuration

```
git config list
```

- Step 3: config line endings

On Windows:
```
git config --global core.autocrlf true
```

On Lunix/Mac

```
git config --global core.autocrlf input
```

- Step 4: You also can choose your favourite text editor that Git will use using (for Nano as an example):

```
git config --global core.editor 'nano -w'
```


Notes: every command in command line tends to have a `man` page
```
man git
man nano
```
give you information about git and nano

Questions asked:
- no man on Windows;
- how to quit nano. Answer: Ctrl+X
- how to quit man. Answer: type `q`
- what to do when you have several values for a given git config field.

- Step 5: Rename the default main branch with:

```
git config --global init.defaultBranch main
```

### Creating a repository, tracking changes [Ou]

A side point about command line: it is not to torture ourselves with bad-looking graphics and arid syntax. It allows -for the course at least- to know better what Git is doing 'under the hood'.

Question: How do we make sure that Git is working on the local drive, not on the cloud.
*Answer*
```
cd ~
pwd
```
What is the path you see? Is it `/c/something`?
If it is, try:

```
cd /c/
```

Tip: `cd -` goes to the previous folder you were in.

To create a directory named recipes under the current directory, do:

```
mkdir recipes
```

Then let's go there:
```
cd recipes
```
Check you're there
```
pwd
```
pwd: *p*rint *w*orking *d*irectory

Now we need to make Git understand that this will be a Git directory:
```
git init
```

Tip: tap the TAB key to autocomplete a command. Tap it twice quickly to show the list of possible autocompletions.

Now we need to actually start using Git for our changes.
Firstly, tell Git to get the changes to `guacamole.md` into account
```
git add guacamole.md
```
Now the state of guacamole.md at the time of the command typing has been added to the **staging area**. It is still not saved into the project, because all your changes in the staging area now need to be **committed**:

```
git commit -m "Your commit message"
```

And now your changes are safe, and part of the git history:
```
git log

```
will show your commit with its message.

Attempt 1:
- edit the guacamole.md file to add some ingredients;
- `git status`
- `git commit -m "Added ingredients to the guacamole"`
- `git log` to see the history of commits.

It seems that our commit never made it, why? This is because we did not **stage** the changes (we did not tell Git we wanted to bundle those changes into a commit). So rather, do now:
- `git add guacamole.md`
- `git status`: now guacamole.md is in the staged area
- `git commit -m "Added ingredients to the guacamole"`
- `git log` to see the history of commits. Now your commit is there.

Note: you need to create the file to add it with `git add`

### Exploring History, ignoring things [Johan]

How to add your current staged changes to the latest commit **IF YOU HAVE NOT PUSHED YET**:
```
git commit --amend
```

How to change a file back to its state in a given commit?
- get the commit identifier with `git log`
- `git restore -s IDENTIFIER YOURFILE`

How to track changes to one file with `git log`:
```
git log --patch YOURFILE
```


### Remotes in GitLab [Ou]

```
git remote add origin git@git.wur.nl:ku_o/recipes.git
git add .
git commit -m "Initial commit"
git push --set-upstream origin main
```

### Collaborate with GitLab

Go to the home directory

```
cd ~
```

Clone the project Johan just create

```
git clone git@git.wur.nl:hidding_j/temperature-conversion-tool.git
```

A repository `temperature-conversion-tool` will be cloned to your home directory.

Get into the newly cloned repo:

```
cd temperature-conversion-tool
```

create a file `conversion.py` and add it to git history
```
nano conversion.py
```

add the following content to the file
```python=
def convert(t):
    return t * 9/5 + 32

```

add, commit and push the file

```
git add conversion.py
git commit -m "add a conversion file"
git push
```

an `.gitignore` file is added to ignore files

```
nano .gitignore
```

```
__pycache__
*.dat
```

Louis created [an issue](https://git.wur.nl/hidding_j/temperature-conversion-tool/-/issues/?sort=created_date&state=closed&first_page_size=20) in Johan's repository, indicating some improvement/fix


Johan created a new branch refering the issue number 1

```
git switch -c 1-explicit-conversion
```

Then, Johan changed the function name in `conversion.py` to `celcius_to_farenheit`, also added some comments. Then he staged this file and committed this.

```
git add conversion.py
git commit -m "rename the function to celcius_to_farenheit and added some comments"
git push
```

Louis now looks into [the changes Johan made](https://git.wur.nl/hidding_j/temperature-conversion-tool/-/merge_requests/1) on GitLab, and judge if this is a good implementation. This is a code reviewing of a Merge Request. 

Johan created a [new issue](https://git.wur.nl/hidding_j/temperature-conversion-tool/-/issues/2), asking for a new feature to covert Farenheit back to Celcius. 

```
git switch -c 2-add-farenheit-to-celcius
```

Louis then added another function to `conversion.py`.

Then Louis push the changes to remote

```
git add conversion.py
git commit -m "add function farenheit to celcius"
git push
```

Then Johan starts to review Louis's implementation as a [Merge Request](https://git.wur.nl/hidding_j/temperature-conversion-tool/-/merge_requests/2)


### Work in pairs, try to follow the workflow

```
cd ~
```

1. PERSON A: Create an issue in the repository
1. PERSON B: Clone this repository to your system
1. PERSON B: Create a new branch
1. PERSON B: Make the changes requested in the issue
1. PERSON B: Push the changes to the remote repository on GitHub
1. PERSON B: Submit a Pull Request, refer to the issue (e.g. “Closes #1”)
1. PERSON A: Review the Pull Request
1. PERSON B: Address the comments
1. PERSON A: Approve the Pull Request
1. PERSON B: Merge the Pull Request


## 📚 Resources

[Helpfull video](https://youtu.be/dQw4w9WgXcQ?si=iZ5v2C8oJJypZaBI)
[Post workshop survey](https://www.surveymonkey.com/r/CFHV62J)
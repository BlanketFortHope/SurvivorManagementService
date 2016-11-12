---
title: Getting Started with GitHub
type: index
weight: 0
---

This discussion will be an introduction to GitHub. We will discuss how GitHub should be used, what its purpose is and delve into its features.

<!-- _A brief handout will be provided with examples of each covered topic to serve as a cheat sheet for early use._ -->

## Outline

* Recommended Prerequisites
*	What is Git?
  * What's a repository?
	*	Version Control
*	What is GitHub
	*	Project Management
*	Documentation
*	Getting Started
	* Using git-scm command line
		* Opening a new terminal
		* Navigating to the repository directory
		* Running Git Commands
*	Common Git Tasks
	* Configuration
	* Global vs. Local vs. System
	* Identifying yourself
	* Create aliases
	* Confirming Configuration
	* Initializing Your Repository
		* Create a Repository from Scratch
		* Clone a Repository
	* Modifying, Adding and Removing files
		* File State
	* Committing
		* Status
	* Merge Requests
		* pull Requests
		* push Requests
		* Addressing issues with Commit messages
	*	Advanced Git Features
		* Branching
		* Forking
		* GitFlow
		* Webhooks
*	GitHub Project Features
	* Markdown
		* README Markdown File
	* Updates and Notifications
		* Stars
		* Watching Projects
	* Issue Tracker
	* Wiki
	* GitHub Pages


## Recommended Prerequisites
A laptop with git-scm installed on it if you’d like to follow along.

To install, proceed to the following [git-scm download link](https://git-scm.com/downloads) and download the correct version for your operating system.  Once downloaded, open the file, click "Run," and follow the installation prompts.  (Note: in order to follow along with this tutorial, Git must be included in your path.  If you used the default values provided by the installer, this will be done automatically)

## What is Git

Git is a lightweight, open source, version control system that has been widely adopted by the developer community. It is very sophisticated in how it does it job, but is not that difficult to take advantage. There is a lot of Git magic taking place behind the scenes, so to speak, but for our purposes here we will accept and trust that magic so that we can get to using Git and the associated tools we will discuss quickly. If you have further interest or as you get into more complicated use of Git and the tools, there is plenty of information available that will let you behind the curtain and understand the magic.

### What's a repository?
Commonly referred to a "repo", a repository is a collection of related files, most often source code, usually associated to the same project or product. This is an important concept to understand with Git, because most management occurs at the repo level.

### Version Control

Simply put, version control is a means of tracking the all of changes made to a project over time.  This could include changes to source code, configuration files, or even training documentation like the one you are reading now.  Proper version control provides teams with the ability to detect exactly what changes were made to cause a break in the code and allows the code to be easily reset to a previous working version. Version Control Systems like Git are also commonly referred to as Source Control Management or SCM.

Git is has a particularly lightweight and easy to use SCM.  In addition to meeting the requirements of a proper version control system listed above, git also has some more advanced features, such as parallel branching, forking, distributed version control (to be covered in greater detail later in the training). It is important to understand that Git differs from many traditional SCMs in that it is a Distributed Version Control System (DVCS), which means that clients don't just check out the latest version of files, but actually mirror the whole repository. This also results in most operations being performed locally on the client.

## What is GitHub

GitHub is a Git hosting website that started out to provide a centralized "cloud based" Git service and has become an integral part of the open source and global technology communities. GitHub has expanded exponentially as a product and company and now in addition to providing the free hosting service also provides locally installed or dedicated cloud versions along with training and support.

Github provides a visual interface on top of Git and the stored repositories and adds, and continues to expand on, features and functionality that enhances teams usage of Git for their projects. Several of those features are covered in this training.

### Project Management

GitHub's ability to track the progress of all work being completed within a project, makes it an ideal solution for project management.  While it's default web interface allows for some project management capabilities, it's not really sufficient as a robust project management tool.  This is not a problem however, because of Git's open source nature and easy extensibility.  With it's widespread adoption, Git has spurred the creation of numerous project management extensions have been created and has been integrated into many existing project management suites (such as the Atlassian suite currently being used by Blackstone)

## Documentation

There are now numerous sources of information on Git, GitHub, and related products/projects. Some key resources are:
* [Pro Git](https://progit2.s3.amazonaws.com/en/2016-03-22-f3531/progit-en.1084.pdf) a book written by people involved in GitHub from early days
* [GitHub Guides](https://guides.github.com/)
* The git-scm also installs a local guide that is used in help requests (`git help <command`) and can be referenced stand-alone.

## Getting Started

Now that you know what Git is all about, we'll begin actually learning how to actually use it. This will be an introduction to Git's powerful capabilities and as such will not go into depth of everything you can and would do with Git. The basic assumption is that you are working with a remote Git server/repository and are working from a master branch (these terms will make more sense as we progress).

### Using git-scm command line
While several GUIs have been created to help facilitate the use of Git for non-developers, the best way to learn and understand Git is by using it through your operating system's terminal. We will come back to the default gui provided with git-scm

Terminal commands are different between Windows based systems and Unix based systems (Mac & Linux) each operating system, and learning to use them is better left for another post... or several.  Luckily for us, the git commands are operating system agnostic, so all we need to do is get you to the correct directory.

#### Opening a new terminal

If you are an experienced user, and prefer to use your own shell, feel free to do so.  If you don't know what that means, have no fear, just do the following based on your operating system:

* **Windows**
	* **Git Bash Shell**
		1. Click on the Start menu
		2. Navigate to and expand the Git menu group
		3. Select the Git Bash item to open the windows
		4. You can also open the Git Shell from a file explorer window by right clicking the folder and left clicking Git Bash
		4. This shell behaves like a Linux (bash) command shell ("ls" lists files, etc.)
	* **Command Shell**
		1. Click on the Start menu
		2. Type `cmd` into the search bar
		3. Hit enter or select "cmd" from the list of programs
		4. There is also an option on the git start menu to launch a command shell. Both behave like a Windows command shell ("dir" list files, etc.)
* **Mac**
	1. Open a file explorer by clicking on the finder icon in the dock
	2. On the left most column, select `Applications` > `Utilities`
	3. Inside the Utilities folder, open the `Terminal` application
* **Linux** - There are several different distributions of Linux and different ways of accessing their terminals.  The methods below should work on most distributions, but probably not all.  If you are using Linux, you most likely already know how to access your terminal anyway.
	1. Hit `Ctrl` + `Alt` + `T` simultaneously
	2. Navigate to `Applications` > `Accessories` and open the `Terminal` application

Once you have the terminal open, you can determine what version of git you have by typing: `git --version` and pressing enter.  If this returns an error (and you didn't make a typo), Git was not properly installed or was not added to your Operating Systems PATH.  In either case, the simplest remedy is to repeat the steps in the [Recommended Prerequisites](##Recommended-Prerequisites) section.

#### Navigating to the repository directory
Now we must navigate into the directory (aka folder) where we want to create our Git repository using the terminal.  As mentioned previously, the commands used in each OS's terminal are different.  Lucky for us, the command for changing directories is the same throughout.

Use what ever means you are most comfortable with to navigate to the directory you would like your Git repository to reside.  Once there copy the absolute path to that location - It should start with `C:\` (Windows) or `/` (Linux/Mac).  This is the path to your repository.

Now navigate to this directory in your terminal using the following command, replacing `<repository path>` with the absolute path to your repository:

`cd <repository path>`

For Example:
* (Windows) - `cd C:\Users\NickJonas\Documents\AmazingRepo`
* (Mac/Linux) - `cd /Users/NickJonas/Documents/AmazingRepo`

**Note:** The cd in the command above stands for "Change Directory"

#### Running Git Commands
Now that we have our terminal open and are in the correct directory, we can start interacting with Git.  To run Git inside the terminal, you type `git` followed by the command you would like to execute (ex. `git init`).  Simply `git` with no command after it, the terminal will return a list of available Git commands to use.  Go ahead and give it a try!

In the next section, we will review a list of common Git commands, explain what they do, and when to use them.

## Common Git Tasks

### Configuration
First things first.  Git is all about collaborating, but we want the version on our machine to be all about us!  To do that we need to edit a configuration file to let it know our preferences.  This file will let us do things such as identify ourselves when checking in code and create shorthand versions of commands we use on a regular basis. You can edit the configuration using the git command line with the **config** command ("git config ...").

#### Global vs. Local vs. System
Okay, so in reality, there's more than one configuration file.  In fact there are three different levels of configuration files.  If you want to know more check out the bullets below, but otherwise you can feel free to skip this subsection.

* **Local** - The settings in the local configuration file only apply to a single repository (the repository in which it resides).  This configuration file is used to define attributes that are unique between repositories . For example, you may manage several repositories from your account and would like to associate yourself with different emails for each.  This will be the level of configuration file used in this tutorial.
* **Global** - The settings in the global configuration file apply to all of the repositories under your user account on a given computer.  That may sound a little confusing, but here's what I mean:
	* If you share the computer (or server) with other people who log in with their own account, it will not affect their git configuration. They will have their own global configuration file associated to their accounts
	* This will not affect the configuration of Git on other computers you use.  If you use multiple computers, you will need to set this configuration file on each.
* **System** As you may have guessed, the settings in the system configurations file apply to all of the accounts on a computer (or all virtual machines on a server).  Unless you are a systems administrator you probably won't use this file.

You can specify the level of configuration to edit using the git config command line with parameters global, local, and system ("git config --global ...").

**Note:** If a setting is present in multiple levels, the lowest level's value will be in effect.

#### Identifying yourself
You can use the configuration file to identify yourself to Git.  This allows Git identify who committed each change.
From the command line these commands will set your identifying information:
	git config --global user.name "John Doe"
	git config --global user.email johndoe@example.com

#### Create aliases

This is more common as you are likely using Git a tool for collaboration

#### Confirming Configuration

To display your current configuration you can simply run the config command with the --list option:
	git config --list
Or specify a specific key you want to see:
	git config user.name
Any key defined in multiple levels will display multiple times and the last one listed will be the one in effect. You can also display keys just for a level with the same options when setting them (--global etc.)

### Initializing Your Repository
In order to use git, you first need a repository.  --define repository here--

#### Create a repository from Scratch
If you need to create a new repository from scratch you can use the following command:

`git init <path of repository>`

This will initialize (create) a git repository in the directory identified by the "target path".  If this directory does not already exist, Git will create it.  If you omit the path of the repository, it will create a repository in your current directory.

#### Clone a repository
It's much more likely that you will want to contribute to an existing repository rather than create one from scratch (Git is a collaboration tool after all!).  To do this, you use the following command

`git clone <source repository> <target path>`

This will create a repository at the "target path" and copy all of the contents from the source repository to  your local machine at the defined path.  If you omit the path of the repository it will create the repository in your current directory. You now have a complete copy of the repository on your local machine.

### Making changes
#### File State
The files in your local copy will be tracked by Git as you let Git know what and when you want to do with them. The state of any file is basically untracked, unmodified, modified, or staged, as shown in this diagram:

![imgGFS][img Git File State]

You will tell Git what files to track and when to stage files you have tracked and then modified to be ready to be committed back to the repository (branch effectively).

#### Modifying, Adding and Removing files
You now can start contributing to the project by changing the contents of your local repository. You can edit existing files, delete existing files, and modify existing files. You need to tell Git about the changes you are making using the git add command. The less risky way to do this is to run a git add command for each file you add or modify, such as

`git add <path of file relative to current directory>/mynewfile.txt`

If you want to rename or delete a file you can use the mv (move) or rm (remove) commands such as

`git mv <path of file relative to current directory>/theoldfile.txt mynewfile.txt`
`git rm <path of file relative to current directory>/thebadfile.txt`

Technically, Git can recognize some changes to the repo without these specific commands, or you run wildcard commands like `git add *`, but it is a good practice at least as you start out to be very explicit with Git.  Note that git add always adds just the current contents of a file; further changes to the same file will be ignored unless you run git add on the file again.

### Committing
When you are content with the changes you have made and are ready to commit to them, you can do so with the commit command. This is how you tell Git that you want these changes in your local copy to become part of the master repository. You add a comment with the commit that briefly describes what you are submitting. The git command will act against everything that has been added with the add and other commands. The format of the command in it's simple form is:

`git commit -m "comment on changes"`

If you prefer, you can leave the -m option off and Git will open your default editor where you can provide the comments and when you exit the editor will execute the commit.

#### Status
When you want to know where things stand with your changes before committing them, you can use some commands to ask Git what the state currently is. The `git status` command will show you the files that would be committed and other information. The `git diff` command will show you more details on the actual changes (with no parameter it is the diff between your local changes and the original version, with the --cached parameter it will show between your changes and the "head" or currently committed version).

### Merge Requests
#### pull Requests
When you have cloned an existing repository from a central source like github or otherwise associated your repository with that instance, you have to keep it in sync with other changes that occurring while you are working on it. In the simple flow, you would issue a `git pull` command which will take all other committed changes from the source and merge them into your local copy. Technically this runs a `git fetch` and a `git merge origin/master` commands. You do this before committing your changes in so that you become aware of any conflicts right away.

#### push Requests
When you are ready to commit your changes back to the central source to be shared by other people or prepared for deployment you send them to the source with a push command. In its simple form and without going into the deeper topic of branching, this command will push your version of the repository to the source version of the same repository and on the master branch.

`git push origin master`

#### Addressing Commit and Merge issues
Git has a very sophisticated and intelligent merging capability. It will attempt to combine multiple changes to the same files in the way they should be. However, it will not do this in dangerous ways resulting in bad results. Instead it will alert you to the specific conflicts and give you the ability to select what changes should be applied.

The potentially odd part of this is that Git will save a modified version of the file with comments that describe the conflict. You can edit the file to resolve the conflicts and take the steps to add and commit it again. An example of a conflicted file is here:

	`<<<<<<< HEAD:file.txt
	Hello world
	=======
	Goodbye
	>>>>>>> 77976da35a11db4580b80ae27e8d65caf5208086:file.txt
	All you need to do is edit the files to resolve the conflicts, and then

	$ git add file.txt
	$ git commit`


## Advanced Git Features
### Branching
One of the most powerful capabilities of Git and what differentiates it from other SCMs is it's ability to support numerous branches and merges. Branching strategies and commands are an advanced topic, so for now it is important to understand that this is possible and what a branch represents in simple form. A branch is a snapshot of a the repository contents at a point in time that can be modified separately without affecting the original until desired. At the point that it is desired to join the changes together with the original (which has possibly changed itself since the snapshot) the branch can be merged back. Depending on the location and complexities of the changes, this merging can happen automatically and intelligently or may need some manual assistance to ensure the correct end state is achieved.

### Forking
Forking is another method of making a separate copy of the repository contents for separate modification. Forking, however, is usually intended to take the repository down a different path that may never be merged back with the original. It can be, but the merging usually requires more manual editing as decisions must be made as to what differences are to be moved to the new version. Forking is very commonly done when working with Open Source projects that provide a basis for what is needed, but require modifications to meet the specific requirements and those modifications may not be desired in the original project.

### GitFlow
GitFlow is a term that refers to the branching strategy that a project determines to best fit its needs. A basic example is that there is a master branch where all changes come back to, a develop branch where new development occurs, and a release or staging branch where new changes come through to be validated before going back to master. Steps along the GitFlow allow for the vetting of and approval of changes to provide a system of checks and balances that help ensure the quality and integrity of the project. There are some standard documented GitFlows such as this one: [GitFlow Example](http://nvie.com/posts/a-successful-git-branching-model/)


## GitHub Project Features
### Markdown
Github recognizes a file with an extension of md and formatted with a standardized Markdown language and converts it into a web html. This document is written with markdown. The syntax to create basic, but nicely formatted documents is straightforward. Refer to this or other links for more information on the syntax and usage:
[Markdown Syntax Reference Example](https://help.github.com/articles/basic-writing-and-formatting-syntax/)

#### README Markdown File
 When a file is located in a repository such at the root folder of a project with the name README.md, it will be displayed in Github along with the folder directory and other information. It is a defacto standard to include such a file at the top of a project to describe the project and provide a consumer with the information they need if they want to use the contents of the project.

### Updates and Notifications
#### Watching Projects
GitHub will notify you by email about changes to a project/repository including changes in your access levels. You can control these notifications from the interface by indicating if you want to "watch" the repository or not, including if you want to be told when you are "mentioned".

#### Stars
You can "star" a repository in the GitHub interface. Starring a repository allows you to keep track of projects that you find interesting, even if you aren't associated with the project.
When you star a repository, you're actually performing two distinct actions:
* Creating a bookmark for easier access
* Showing appreciation to the repository maintainer for their work

Many of GitHub's repository rankings depend on the number of stars a repository has. For example, repositories can be sorted and searched based on their star count. In addition, the Explore page shows you popular repositories based on the number of stars they have.

### Issue Tracker
GitHub also includes basic project management tools based on an Agile and Kanban methodologies that can be used by a team collaborating on the project. You can create a project, create issues and assign them to the project on a Kanban board, create milestones likes Sprints and associate issues to them. You can also assign labels to issues to be used in grouping and searching.

### Wiki
Github will allow you to create and manage a wiki (information sharing/collaboration space) related to your project. Since people will be in GitHub reqularly while working on the project, having a location right there for discussions and information sharing can be a valuable tool.

### Webhooks
Webhooks provide a way for notifications to be delivered to an external web server whenever certain actions occur on a repository or organization. They are commonly used to trigger automatic processes like project builds when new changes are pushed.

### GitHub Pages
Github Pages allows you to have some web page content associated to your repository or organization.

## Graphical Tools
### Git GUI
The install of the git-scm includes a GUI tool that can be used to execute the Git functions. It is fairly straightforward once your understand the basics that you learned here about repositories, file states, and GitFlow.  You can visually see the state of your repository and request the same actions as you would with the shell commands. To access the Git Gui:
1. Click on the Start menu
2. Navigate to and expand the Git menu group
3. Select the Git Bash item to open the windows

### GitHub Desktop
The GitHub people have also provided a graphical tool that you can install and run locally that will allow you to view and take actions against your repository in a visual way. It does not provide any real support for the functionality that GitHub extends from Git, but adds links to bring you to the repository in GitHub and to other tools like a Git Shell. This is the link to get the install for  [GitHub Desktop](https://desktop.github.com/)

## Possible Additional Sections
### TLS Keys



[img Git File State]:img/GitFileState.png "Git File State"

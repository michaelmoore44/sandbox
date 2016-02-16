To install git, Google for "download git windows" and download git for windows.
Run the downloaded file to install git on your computer. Be sure to pay close
attention to where git is installed on your computer. This will be important 
because when you install source tree, you will need to make sure that 
Source tree is able to find your installation of git. When you install Source
Tree, it will ask if you want to install a standalone version of git. I usually
point it to my already installed instance of git.


To create a new repository:
Go to your account page on github.com
click the repositories tab
click the new button (usually in the upper right hand corner)
give your repository a name, and a description if you feel it is necessary
now click create repository

To clone this new repository (get the repository on your computer):
go to your projects directory on the pc you intend to clone this new repository
create a folder to hold the previously created repository. I typically give this
	folder the same name as the repository or the project.
If you have git installed, you should be able to right click and select
	git bash here. This will open a git command terminal where you can enter
        the commands in the following steps to clone the repository.
Before cloning the repository, copy the URL for the repository to the clipboard.
	With GitHub, you can usually do this on the main page of the repository.
Now in your terminal enter the following command:
	git clone --recursive https://github.com/michaelmoore44/sandbox.git
You should now have a functioning repository.

from here you could pick up with source tree by pointing to this repository.

For now I will continue with the command line.

To get the command line pointed to our working directory, type the command below:
	cd sandbox

for the purpose of introducing git, I have added these instructions as a text
	file to the repository folder named getting_started_with_git.md. I saved this
	file in the sandbox directory at the same level as the .git folder. In my
	case, it would be stored in the following directory:

	C:\projects\sandbox\sandbox

Now to see what the repository looks like type the command below:

	git status

At this point, the status command tells me that I have one untracked file. To
	get the file ready to be committed to the repository, it must be staged. To
	stage the file enter the command below:

	git add

Entering the status command should tell you that you have one new file. To
	commit this file to your local repository, enter the command below:

	git commit

Your default text editor should now open with instructions for entering a
	commit message. enter the message save and exit.

Your file has now been added to your version of the repository that is local to
	your computer. The file now needs to be added to the remote version of your
	repository(the one stored on github). To do this, type the command below:

	git push -u origin master

To see a log of your local repository you can now type the command below:

	git log

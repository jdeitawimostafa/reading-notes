# revesion and the cloud
what is Git?
* Snapshots
* Local Operations
* Tracking Changes
* Loss of Data
***
## Cloning 
You can also create a copy of an existing Git repository from a particular server by using the clone command with a repository’s URL:

$ git clone https://github.com/test
By cloning the file, you have copied all versions of all files for a project. This command leads to the creation of a directory called “test,” with an initialized .git directory inside it, which has copies of all versions of all files for the specified project. The command also automatically checks out — or retrieves for editing — a copy of the newest version of the project.

To clone a repository into a directory with another name of your choosing, use the following command format:

$ git clone https://github.com/test mydirectory
The command above makes a copy of the target repository in a directory named “mydirectory.”
*** 
### Tracking and Staging a New File
Single File
Track one file only by using the following format:
git add filename
Track all files in a repository by using the following command:
 git add . 
After using these commands, files are tracked and staged for committing.
After adding a new file called EXAMPLE, you would see information regarding changes to be committed when using the git status command:
git status
On branch master
Changes to be committed:
  (use "git reset HEAD ..." to unstage)
new file: EXAMPLE
This information tells us that there are changes to be committed and that the file has been staged.
Committing a File
After staging one or multiple files, you should commit the changes and record what you did within the commit message:
$ git commit -m “made change x,y,z”
*This step has committed changes for the file or files (you can have one commit message for multiple files, if applicable) to the HEAD.
Committing All Changes
$ git commit -a
*This command commits a snapshot of all modifications to tracked files in the working directory.
Pushing Changes
Next, you would push changes to a remote repository. We will discuss remote repositories in more depth in the next section. For now, we will look at a general overview of pushing changes to remotes.
Example:
git push origin main 
then it ask you to enter your username and password in github . 

#### thanks for reading . 

***Git: Basic Overview & Notes***


---What is it?---
A fundamental technology employed by many software devs providing version control throughout the production process. An important note to make is that Git is run locally. There are 3rd party service providers with a common purpose (i.e. GitHub, a cloud-based application) that work with Git, but they are not the same thing as Git.


---Version Control---
Often there are multiple developers collaborating on the same code base, concurrently working on making additions or revisions to the code as features are added or improved. This results in multiple versions of the same code existing, which can become problematic when attempting to sort out the changes. Furthermore, issues can arise if an update creates a bug in the program that is difficult to locate.
  Git creates offers solutions to these issues by creating save points in a project's files. Once changes are made, Git assists in merging versions so the code base remains the same for everyone. Additionally, if hard-to-fix bugs arise, it allows the code to be rolled back to a prior, functional version.


---Staging and Committing---
This version control functionality is achieved in 2 phases. When code has been modified, or files are being added or deleted, the changes need to be submitted to a staging area where they can be reviewed and tested. These modifications haven't yet been saved to the code base yet, so if additional changes are required, they can be made without affecting any other copies or versions of the code.
   After reviewing and accepting the changes in staging, the next phase is Committing the update to the origin master file. This saves the changes, and requires a brief message describing the changes and/or purose of commit.


---Fundamental Git Commands---
These commands can be used on the command line or in shell. A new project folder will need to be created and the directory changed so the prompt corresponds with the correct location.

-Creating new project: git init

This allows Git to begin tracking changes to the project. A new hidden .git folder is created in the current directory. This folder rarely needs to be accessed unless advanced settings are being implemented.

-Checking Git status: git status

Requests information about current status. This will provide branch information and if there are any commits.

-Adding files to project: git add <fileName.extension>

When a new file is added to the current directory, git will recognize the file provide feedback of an "Untracked file" that can be committed. Using the git add command allows files to be put into the staging area.
   After using git add, an additional git status command will demonstrate the file is now waiting for commit.
   As a shortcut to typing multiple file names, all files in the staging area can be committed at one time via git add -A (the latter -A is a flag saying all files to be added; in some instances developers may use git add . but this require the project to be in root directory to ensure all changes are selected).

-Saving changes to project: git commit -m "<Include message text here.>"

At this point, git commit can be used to update the code with the staged modifications. The -m followed by a message in quotes is required for the commit to be successful.

-Checking commit history: git log

Running this command will provide a readout of commit dates, messages, and authors, along with a unique ID for the commit known as a "commit hash" which can be used later to reference a particular commit, if needed.

-Switching betwen versions: git checkout <commit hash/ID>

Entering checkout allows a prior version to be viewed, which will likely come with a "detached HEAD" message indicating the state is inactive. As such, changes may be made and committed, otherewise discarded without affecting other branches. Additionally, a new branch may be made via git checkout -b <new-branch-name>


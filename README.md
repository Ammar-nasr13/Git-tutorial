## What is Git ?

- It is a local repository that stores all our projects.
- Version Control System. ( VCS ) => This means that when you create a new repository and save your project files in it, it tracks all the changes that will occur to the project files and saves every change that will be made in a separate version, and you can return to any version at any time.
- Work as a team => Each programmer works on his own copy separately without affecting the others, and then all these copies are merged together.

## 📌 By using git you can do the following:

- 📝 **Track changes** Any changes to a file are recorded (who made them, when, what was the change).
- 🔙 **Rollback** If something goes wrong, roll back to a clean version of the code.
- 🤝 **Teamwork** Each programmer works on their own version, and then you merge the changes together.
- 🌐 **Distributed** Every device has a full copy of the project, and you don't always need an internet connection.


## How to Install git in your PC ?

- click here to [Download Git](https://git-scm.com/downloads)
- choose your operating system to downloading ( Windows - macOS - Linux/Unix)
- install Git after downloading.
- **Note** => click here to [Download Git Book](https://github.com/progit/progit2/releases/download/2.1.448/progit.pdf)

## How create New Repostory in Git and store project in it ?

- Open Terminal or Cmd.
- You must make sure that you are inside the project folder.
- **git init** => Initialized empty Git repository in path ..... => write in cmd dir /a:h to show hidden .git folder. <br>

 ➡️ **.git**

- *Note* => Any git repository you create contains a .git file.
- An empty Git repository in which the project is stored later.
- It contains several files responsible for: <br>
  1- All data related to the repository. <br> <br>
  2- Tracking changes, rolling back to older versions, and working on different branches.

- **git status** => Used to know the current status of the project (repository).
- Current branch.
- Files in Staging Area (ready to commit).
- Untracked files.
- Files that have been modified but not added.
- **Note** => **git status -s** => M or A هذا الامر يقوم باظهار الملف وبجانبه حرف يدل علي حاله الملف هل هو   <br>

- **git add** => **git add file name or git add or git add folder name** . => It is used to add new files or changes to the index file (staging area). These files are then ready to be saved and released.

- **git commit -m "message"** => Used to commit changes from a Staging Area to the Git database (inside the .git/objects folder).
- Each commit represents a snapshot of the project at a particular moment in time. => version

## How to update Repostory (project files) in Git ?

- if you change files in project. This change will appear in the project's git repository, but we need to update that change in the project's git repository.
- to show This change  appeared in the project's git repository => write **git status**
- To update changes in Repostory => using **git add .** - **git commit -m "message update"**  


<div align=center>
<img src="https://github.com/Ammar-nasr13/files/blob/master/images/unnamed.png" height=350>
</div>

## Repostory History in Git .

- After you git commit  => this commad save all changes in Repostory History.
- Every commit you make is saved in a separate version.
- Each commit (version) is saved as a contract next to each other.
  

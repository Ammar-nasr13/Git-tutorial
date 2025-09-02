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

- **Note** => To show all command in git write.
```commands
git --help
```

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

 ```commands
# إضافة ملف معين

git add filename.txt

# إضافة جميع الملفات المعدلة

git add .

# إضافة جميع الملفات بما فيها المحذوفة

git add -A

# إضافة ملفات interactively

git add -p
```

- **git commit -m "message"** => Used to commit changes from a Staging Area to the Git database (inside the .git/objects folder).
- Each commit represents a snapshot of the project at a particular moment in time. => version

```commands
#  مع رسالة commit

git commit -m "وصف التغييرات"

# إضافة الملفات المعدلة و commit مباشرة

git commit -am "وصف التغييرات"

# تعديل آخر commit

git commit --amend
```

## How to update Repostory (project files) in Git ?

- if you change files in project. This change will appear in the project's git repository, but we need to update that change in the project's git repository.
- to show This change  appeared in the project's git repository => write **git status**
- To update changes in Repository => using **git add .** - **git commit -m "message update"**  


<div align=center>
 <img src="https://github.com/Ammar-nasr13/files/blob/master/images/image2.png" height=350>
</div>

## Repostory History in Git .

- After you git commit  => this commad save all changes in Repository History.
- Every commit you make is saved in a separate version.
- Each commit (version) is saved as a contract next to each other.

  
<div align=center>
 <img src="https://github.com/Ammar-nasr13/files/blob/master/images/image1.png" width=600 height=300>
</div>

- To show **Repostory History** using **git log**

```command
git log
```
- this command show => ( commit id - message - date of change - author )
- To exit command write => q

- git log -p or git show => مع التغيرات  commits عرض سجل الـ   

```command
git log -p  or git show

git log -p filename  // specific file

git log --graph

git show commit_hash
```
- git log --oneline => عرض ملخص للسجل    

```command
git log --oneline
```

- **git show**
 ```commands
# عرض آخر commit

git show

# عرض commit محدد

git show commit_hash


# عرض التغيرات في ملف ضمن commit محدد

git show commit_hash:filename
```

- **git blame**

```comands

# عرض من عدل كل سطر في الملف

git blame filename

# مع تفاصيل الـ commit

git blame -c filename


# لعرض سطور محددة (مثلاً من 10 إلى 20)

git blame -L 10,20 filename

```

## Delete commands in git ?

- It deletes files permanently.

``` command
git rm filename
```

- It deletes the folder permanently.

``` command
git rm -r folder_name/
```

- Delete the file from the git repository but it is not deleted permanently and becomes *UnTracked* => move file from *Staged* to *UnTracked*

``` command
git rm --cached filename
```

- Deletes all files ending with *.log*.

 ``` command
  git rm *.log
```

## Compare changes in Git ?

- Using **git diff** => It displays the changes and compares these changes.

-  **git diff** => modifted ومعمول لها  staging اي انها ليست في مرحلة tracked هو يقوم بتوضيح التغيرات ومقارنة الملفات الموجودة في

``` command
git diff
```

- git diff --staged => staging مقارنة التغيرات في الملفات المضافة لل

```command
git diff --staged
git diff --cached
 ```

- git diff filename => مقارنة تغيرات ملف معين

```command
git diff filename
```

- git diff commit_hash => مقارنه التغيرات في اصدار معين

```command
git diff commit_hash
```

- git diff commit1_hash commit2_hash => مقارنة التغيرات بين اصدارين

```command
git diff commit1_hash commit2_hash
```
 
## .gitignore file in any project.

-  **.gitignore** =>  يتجاهلها وميتتبعهاش في اي عملية تحدث في المشروع git هو عبارة عن ملف يتم وضع بداخلة جميع الملفات والمجلدات اللي انا عايز
-  **.gitignore** => API الهدف من ذلك هو حماية الملفات التي تمثل بيانات هامة حماية قواعد البيانات حماية <br>

➡️ **How to create this file and Rules Used in it**

- Create directory => Name of directory must be *.gitignore*
- Put all files and directories Which is ignored in *.gitignore* <br>

➡️ **Rules Used in it**

- عشان نعمل تعليق داخل هذا الملف بنكتب # وهو نستخدمه لوضع عنوان اعلي الملف او المجلد.
- عشان اخلي ملف او مجلد في حالة تجاهل من  قبل git قم باضافة اسم الملف او المجلد .
- استخدام الرمز * ثم ياتي بعده امتداد مثلا log. هذا يعني انه سوف يتجاهل كل الملفات التي تنتهي بهذا الامتداد .
- علامة التعجب قبل الملفات والمجلدات معناها لا تقم بتجاهل هذه الملفات او المجلدات وهذه شئ استثنائي .<br>

- **Note** ⤵️

```comands
# التحقق من الملفات المتجاهلة
git status --ignored

# التحقق من قواعد gitignore النشطة
git check-ignore -v <filename>
```

➡️ **Convert Tracked Files to .gitignore**

- To convert Tracked Files to .gitignore using command ⤵️

```comand
git rm --cached filename

git rm --staged filename

write filename in .gitignore
```
<br>

- **Note** => To put any files or directories in .gitignore must theses UnTracked.

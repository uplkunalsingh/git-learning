# Getting Started with GIT

## 1.  Check Git Version 

```
git --version

```

## 2. Create Project 

```
mkdir my-project
cd my-project
git init 

```
Creates all files for git management(mostly hidden)
.gitignore => we will discuss it 

## 3. Create your first file in project

```
touch index.html

```

## 4. Add Content to your file

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>

```

## 5. Check Status of your project with 

```
git status

```

Gives 

```
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

```

### 6. Lets Add the file to Staging Area 

Before Add lets Understand Commiting and Staging in git

Staging and Committing the code
Committing is the process in which the code is added to the local repository. Before committing the code, it has to be in the staging area. The staging area is there to keep track of all the files which are to be committed.


```

git add index.html
// For multiple files use
git add * or git add .

```

Gives 

```

On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html

```

### 7. Lets Commit our first Change

```
git commit -m "Added My First File"

[main (root-commit) d65203e] Added My First File
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 index.html

```

### 8. Check Status Again 

```

$ git status
On branch main
nothing to commit, working tree clean

```

### 9. Lets CHeck Our History of Commit (Snapshot of Changes)

```
$ git log 
commit d65203e3ff14385d13308039cf6783185e0a007f (HEAD -> main)
Author: singhkunal2050 <singhkunal2050@gmail.com>
Date:   Thu Feb 17 15:11:20 2022 +0530

    Added My First File

```

### 10. Lets do some more changes and see the log again

```
$ touch style.css
$ git add style.css     
$ git commit -m "Added Style File"

```

```
$ git log
commit 43b7e02cf63064f447d704d1838af4992c39d5ca (HEAD -> main)
Author: singhkunal2050 <singhkunal2050@gmail.com>
Date:   Thu Feb 17 15:15:07 2022 +0530

    Added Style File

commit d65203e3ff14385d13308039cf6783185e0a007f
Author: singhkunal2050 <singhkunal2050@gmail.com>
Date:   Thu Feb 17 15:11:20 2022 +0530

    Added My First File

```




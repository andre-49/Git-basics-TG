# BUNDLE 1 

## EXERCISE 1 

``````
andre@beBop ~/Cyphers  
╰─➤  mkdir git_basics 
andre@beBop ~/Cyphers  
╰─➤  cd git_basics 
andre@beBop ~/Cyphers/git_basics  
╰─➤  git init         
Initialized empty Git repository in /home/andre/Cyphers/git_basics/.git/
andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  touch textFile.txt                                                                                                         130 ↵
╭─andre@beBop ~/Cyphers/git_basics  ‹main*› 
╰─➤  git branch -M master
╭─andre@beBop ~/Cyphers/git_basics  ‹master*› 
╰─➤  git branch -M main   
╭─andre@beBop ~/Cyphers/git_basics  ‹main*› 
╰─➤  git add .                                                                                                                    1 ↵
╭─andre@beBop ~/Cyphers/git_basics  ‹main*› 
╰─➤  git commit -m "first commit"      
[main (root-commit) 64ec0dd] first commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 textFile.txt
 ╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git remote add origin git@github.com:andre-49/Git-basics-TG.git                                                      
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git push -u origin main                                        
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 213 bytes | 213.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To github.com:andre-49/Git-basics-TG.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git checkout -b dev         
Switched to a new branch 'dev'
╭─andre@beBop ~/Cyphers/git_basics  ‹dev› 
╰─➤  git checkout -b test
Switched to a new branch 'test'
╭─andre@beBop ~/Cyphers/git_basics  ‹test› 
╰─➤  git checkout dev    
Switched to branch 'dev'
╭─andre@beBop ~/Cyphers/git_basics  ‹dev› 
╰─➤  git branch        
* dev
  main
  test
╭─andre@beBop ~/Cyphers/git_basics  ‹dev› 
╰─➤  git branch -D test                                                                                                         129 ↵
Deleted branch test (was 64ec0dd).
╭─andre@beBop ~/Cyphers/git_basics  ‹dev› 
╰─➤  git branch        
* dev
  main
╭─andre@beBop ~/Cyphers/git_basics  ‹dev› 
╰─➤  git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤

``````
## EXERCISE 2

``````
╭─andre@beBop ~/Cyphers/git_basics  ‹dev› 
╰─➤  v home.html       
╭─andre@beBop ~/Cyphers/git_basics  ‹dev*› 
╰─➤  git stash push -um "untracked home file"
Saved working directory and index state On dev: untracked home file
╭─andre@beBop ~/Cyphers/git_basics  ‹dev› 
╰─➤  git stash list                          
stash@{0}: On dev: untracked home file
╭─andre@beBop ~/Cyphers/git_basics  ‹dev› 
╰─➤  v about.html
╭─andre@beBop ~/Cyphers/git_basics  ‹dev*› 
╰─➤  git stash push -um "untracked about file"
Saved working directory and index state On dev: untracked about file
╭─andre@beBop ~/Cyphers/git_basics  ‹dev› 
╰─➤  v team.html 
╭─andre@beBop ~/Cyphers/git_basics  ‹dev*› 
╰─➤  git stash push -um "untracked team file" 
Saved working directory and index state On dev: untracked team file
╭─andre@beBop ~/Cyphers/git_basics  ‹dev› 
╰─➤  git stash pop stash@\{1\} 
Already up to date.
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	about.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{1} (18f7b89b6f987ae3539b615d59a965c34e5e182c)
╭─andre@beBop ~/Cyphers/git_basics  ‹dev*› 
╰─➤  git stash pop stash@\{1\} 
Already up to date.
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	about.html
	home.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{1} (686d325344fa07e272e26932df759efbc994077f)
╭─andre@beBop ~/Cyphers/git_basics  ‹dev*› 
╰─➤  git add .                
╭─andre@beBop ~/Cyphers/git_basics  ‹dev*› 
╰─➤  git commit -m "adding home, about files on dev"
[dev db111c0] adding home, about files on dev
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
╭─andre@beBop ~/Cyphers/git_basics  ‹dev› 
╰─➤  git push                                       
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 558 bytes | 558.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To github.com:andre-49/Git-basics-TG.git
   0ac8ce7..db111c0  dev -> dev
╭─andre@beBop ~/Cyphers/git_basics  ‹dev› 
╰─➤  git stash pop            
Already up to date.
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	team.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped refs/stash@{0} (56952d85c9e80d3e4f46d523403534354a826b32)
╭─andre@beBop ~/Cyphers/git_basics  ‹dev*› 
╰─➤  git reset --hard                                         
HEAD is now at db111c0 adding home, about files on dev
╭─andre@beBop ~/Cyphers/git_basics  ‹dev*› 
╰─➤  ls
 about.html   home.html  󰂺 README.md   team.html   textFile.txt
╭─andre@beBop ~/Cyphers/git_basics  ‹dev*› 
╰─➤  rm team.html
``````
# BUNDLE 2

## EXERCISE 1

```
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git checkout -b ft/bundle-2
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  v services.html
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git add .
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git commit -m "Services page"
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git push -u origin ft/bundle-2

```
## EXERCISE 2

```
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/bundle-2› 
╰─➤  git switch main               
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git pull                      
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 898 bytes | 898.00 KiB/s, done.
From github.com:andre-49/Git-basics-TG
   d43fc64..5329d0d  main       -> origin/main
Updating d43fc64..5329d0d
Fast-forward
 services.html | 12 ++++++++++++
 1 file changed, 12 insertions(+)
 create mode 100644 services.html
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  ls
󰂺 README.md   services.html   textFile.txt
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git checkout -b ft/service-redesign           
Switched to a new branch 'ft/service-redesign'
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/service-redesign› 
╰─➤  v services.html
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/service-redesign*› 
╰─➤  git commit -am "updating services page"
[ft/service-redesign 6e70358] updating services page
 1 file changed, 1 insertion(+)
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/service-redesign› 
╰─➤  git push -u origin ft/service-redesign  
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 399 bytes | 399.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/andre-49/Git-basics-TG/pull/new/ft/service-redesign
remote: 
To github.com:andre-49/Git-basics-TG.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/service-redesign› 
╰─➤  git switch main                       
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  v services.html
╭─andre@beBop ~/Cyphers/git_basics  ‹main*› 
╰─➤  git commit -am "updating services page on main"
[main 2625104] updating services page on main
 1 file changed, 1 insertion(+), 1 deletion(-)
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git push                                       
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 402 bytes | 402.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:andre-49/Git-basics-TG.git
   5329d0d..2625104  main -> main
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git checkout ft/service-redesign               
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/service-redesign› 
╰─➤  git diff main
diff --git a/services.html b/services.html
index 5e49bcf..d79b1ab 100644
--- a/services.html
+++ b/services.html
@@ -7,6 +7,7 @@
         <link href="css/style.css" rel="stylesheet">
     </head>
     <body>
-        <h1>Services page here!</h1> 
+        <h1>This is a services page</h1>
+    
     </body>
 </html>
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/service-redesign› 
╰─➤  git merge main 
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/service-redesign*› 
╰─➤  git diff main                                                                       1 ↵
diff --git a/services.html b/services.html
index 5e49bcf..dc07e3f 100644
--- a/services.html
+++ b/services.html
@@ -7,6 +7,11 @@
         <link href="css/style.css" rel="stylesheet">
     </head>
     <body>
+<<<<<<< HEAD
+        <h1>This is a services page</h1>
+    
+=======
         <h1>Services page here!</h1> 
+>>>>>>> main
     </body>
 </html>
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/service-redesign*› 
╰─➤  v services.html
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/service-redesign*› 
╰─➤  git commit -am "merging from main with conflicts"
[ft/service-redesign 9a8ffae] merging from main with conflicts
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/service-redesign› 
╰─➤  git push                                         
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 441 bytes | 441.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:andre-49/Git-basics-TG.git
   6e70358..9a8ffae  ft/service-redesign -> ft/service-redesign
``````
# BUNDLE 3

## EXERCISE 1

```
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git checkout -b ft/team-page                 
Switched to a new branch 'ft/team-page'
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/team-page› 
╰─➤  v team.html
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/team-page*› 
╰─➤  git add .                   
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/team-page*› 
╰─➤  git commit -m "Team page on ft/team-page"
[ft/team-page 5c266e7] Team page on ft/team-page
 1 file changed, 13 insertions(+)
 create mode 100644 team.html
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/team-page› 
╰─➤  git push -u origin ft/team-page          
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 472 bytes | 472.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/andre-49/Git-basics-TG/pull/new/ft/team-page
remote: 
To github.com:andre-49/Git-basics-TG.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/team-page› 
╰─➤  git branch                     
  dev
  ft/bundle-2
  ft/service-redesign
* ft/team-page
  main
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/team-page› 
╰─➤  git switch main                          
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git checkout -b ft/contact-page          
Switched to a new branch 'ft/contact-page'
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/contact-page› 
╰─➤  git switch ft/team-page        
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/team-page› 
╰─➤  git log                
commit 5c266e7ac4fb6ad623ae705b0ddeca11b359b2f8 (HEAD -> ft/t
eam-page, origin/ft/team-page)
Author: andre <andy49miguel@gmail.com>
Date:   Sun Mar 2 10:13:13 2025 +0200

    Team page on ft/team-page

commit 7710010cdab3b918be38582938dbc6d971935589 (origin/main, 
origin/HEAD, main, ft/contact-page)
Author: andre <andy49miguel@gmail.com>
Date:   Sun Mar 2 10:05:21 2025 +0200

    readme update after bundle 2

commit 262510424fe2c5d244c5b826ca676689f06482a4
Author: andre <andy49miguel@gmail.com>
Date:   Sun Mar 2 09:47:38 2025 +0200

    updating services page on main

commit 5329d0d60ff792139509ff4e42acfafd77d1e25d
Merge: d43fc64 6f53fa0
Author: Andy Miguel Songa <andy49miguel@gmail.com>
Date:   Sun Mar 2 09:35:03 2025 +0200

    Merge pull request #1 from andre-49/ft/bundle-2
    
    Services page

╭─andre@beBop ~/Cyphers/git_basics  ‹ft/team-page› 
╰─➤  git switch ft/contact-page 
Switched to branch 'ft/contact-page'
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/contact-page› 
╰─➤  git cherry-pick 
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/contact-page› 
╰─➤  git cherry-pick 5c266e7ac4fb6ad623ae705b0ddeca11b359b2f8                          130 ↵
[ft/contact-page 8a76788] Team page on ft/team-page
 Date: Sun Mar 2 10:13:13 2025 +0200
 1 file changed, 13 insertions(+)
 create mode 100644 team.html
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/contact-page› 
╰─➤  ls
󰂺 README.md   services.html   team.html   textFile.txt
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/contact-page› 
╰─➤  v contact.html
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/contact-page*› 
╰─➤  git add .                                               
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/contact-page*› 
╰─➤  git commit -m "Contact page"                            
[ft/contact-page 514c8a4] Contact page
 1 file changed, 12 insertions(+)
 create mode 100644 contact.html
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/contact-page› 
╰─➤  git push -u origin ft/contact-page 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 825 bytes | 825.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), done.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/andre-49/Git-basics-TG/pull/new/ft/contact-page
remote: 
To github.com:andre-49/Git-basics-TG.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/contact-page› 
╰─➤  git checkout -b ft/faq-page                             
Switched to a new branch 'ft/faq-page'
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/faq-page› 
╰─➤  v faq.html    
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/faq-page*› 
╰─➤  git add .                  
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/faq-page*› 
╰─➤  git commit -m "Faq page"          
[ft/faq-page aacc2c9] Faq page
 1 file changed, 1 insertion(+)
 create mode 100644 faq.html
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/faq-page› 
╰─➤  git push -u origin ft/faq-page    
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 306 bytes | 306.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/andre-49/Git-basics-TG/pull/new/ft/faq-page
remote: 
To github.com:andre-49/Git-basics-TG.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/faq-page› 
╰─➤  git revert5 c266e7ac4fb6ad623ae705b0ddeca11b359b2f8 
git: 'revert5' is not a git command. See 'git --help'.

The most similar command is
	revert
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/faq-page› 
╰─➤  git revert 5c266e7ac4fb6ad623ae705b0ddeca11b359b2f8                                 1 ↵
[ft/faq-page 9385288] Revert "Team page on ft/team-page"
 1 file changed, 13 deletions(-)
 delete mode 100644 team.html
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/faq-page› 
╰─➤  ls
 contact.html   faq.html  󰂺 README.md   services.html   textFile.txt
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/faq-page› 
╰─➤  git push                      
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 281 bytes | 281.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:andre-49/Git-basics-TG.git
   aacc2c9..9385288  ft/faq-page -> ft/faq-page
```

## EXERCISE 2

```
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/faq-page› 
╰─➤  git checkout -b ft/home-page-redesign   
Switched to a new branch 'ft/home-page-redesign'
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/home-page-redesign› 
╰─➤  git switch main                      
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  v home.html
╭─andre@beBop ~/Cyphers/git_basics  ‹main*› 
╰─➤  git commit -am "home page on main"           
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	home.html

nothing added to commit but untracked files present (use "git add" to track)
╭─andre@beBop ~/Cyphers/git_basics  ‹main*› 
╰─➤  git add .                                                                           1 ↵
╭─andre@beBop ~/Cyphers/git_basics  ‹main*› 
╰─➤  git commit -am "home page on main"
[main 8f6b31f] home page on main
 1 file changed, 12 insertions(+)
 create mode 100644 home.html
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git push                          
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 523 bytes | 523.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To github.com:andre-49/Git-basics-TG.git
   7710010..8f6b31f  main -> main
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git switch ft/home-page-redesign 
Switched to branch 'ft/home-page-redesign'
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/home-page-redesign› 
╰─➤  git rebase main                 
Successfully rebased and updated refs/heads/ft/home-page-redesign.
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/home-page-redesign› 
╰─➤  v home.html
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/home-page-redesign*› 
╰─➤  git commit -am "home page update" 
[ft/home-page-redesign 0136fc8] home page update
 1 file changed, 1 insertion(+)
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/home-page-redesign› 
╰─➤  git push -u origin ft/home-page-redesign 
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 8 threads
Compressing objects: 100% (13/13), done.
Writing objects: 100% (14/14), 1.59 KiB | 812.00 KiB/s, done.
Total 14 (delta 6), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (6/6), done.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/andre-49/Git-basics-TG/pull/new/ft/home-page-redesign
remote: 
To github.com:andre-49/Git-basics-TG.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.
```

# BUNDLE 4

## EXERCISE 1

```
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git remote add git-copy git@github.com:andre-49/Bundle-4.git   
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git remote                                                  
git-copy
origin
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  v home.html 
╭─andre@beBop ~/Cyphers/git_basics  ‹main*› 
╰─➤  git commit -am "updated home page"             
[main ff7b0c1] updated home page
 1 file changed, 1 insertion(+)
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git push -u git-copy main                      
Enumerating objects: 42, done.
Counting objects: 100% (42/42), done.
Delta compression using up to 8 threads
Compressing objects: 100% (40/40), done.
Writing objects: 100% (42/42), 8.00 KiB | 4.00 MiB/s, done.
Total 42 (delta 16), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (16/16), done.
To github.com:andre-49/Bundle-4.git
 * [new branch]      main -> main
branch 'main' set up to track 'git-copy/main'.
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git push                 
Everything up-to-date
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git push origin main     
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 331 bytes | 331.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:andre-49/Git-basics-TG.git
   c74faf5..ff7b0c1  main -> main
```

## EXERCISE 2

```
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git checkout -b ft/footer            
Switched to a new branch 'ft/footer'
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/footer› 
╰─➤  v footer.html 
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/footer*› 
╰─➤  git add .                
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/footer*› 
╰─➤  git commit -m "Footer"            
[ft/footer 12a22ab] Footer
 1 file changed, 15 insertions(+)
 create mode 100644 footer.html
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/footer› 
╰─➤  v footer.html
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/footer*› 
╰─➤  git commit -am "updated footer"   
[ft/footer cec0162] updated footer
 1 file changed, 1 insertion(+)
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/footer› 
╰─➤  git push -u origin ft/footer            
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 704 bytes | 704.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/andre-49/Git-basics-TG/pull/new/ft/footer
remote: 
To github.com:andre-49/Git-basics-TG.git
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/footer› 
╰─➤  git switch main             
Switched to branch 'main'
Your branch is up to date with 'git-copy/main'.
╭─andre@beBop ~/Cyphers/git_basics  ‹main› 
╰─➤  git checkout -b ft/squashing       
Switched to a new branch 'ft/squashing'
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/squashing› 
╰─➤  git merge --squash ft/footer
Updating ff7b0c1..cec0162
Fast-forward
Squash commit -- not updating HEAD
 footer.html | 16 ++++++++++++++++
 1 file changed, 16 insertions(+)
 create mode 100644 footer.html
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/squashing*› 
╰─➤  git commit -m "footer changes squashing"
[ft/squashing f1ca8d9] footer changes squashing
 1 file changed, 16 insertions(+)
 create mode 100644 footer.html
╭─andre@beBop ~/Cyphers/git_basics  ‹ft/squashing› 
╰─➤  git push -u origin ft/squashing         
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 469 bytes | 469.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/andre-49/Git-basics-TG/pull/new/ft/squashing
remote: 
To github.com:andre-49/Git-basics-TG.git
 * [new branch]      ft/squashing -> ft/squashing
branch 'ft/squashing' set up to track 'origin/ft/squashing'.
```

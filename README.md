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

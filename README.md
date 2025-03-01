# BUNDLE 1 
## EXERCISE 1 
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

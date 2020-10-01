# GIT Notes

##what is verison control

  keeps track of changes
  
   version 1 and, verison 2 , veriscon 3
   
   Version Control System (VCS)
   Source Code managment tools (SCM)
   
   
   file name ex(budget_v4.xls, public_ comments_final.txt)
   
   example of programms that have verison control 
   adobe
    
    
##Source code control System (Sccs)
    
   stored original version and sets of changes
  
 
## Revision Control System (RCS)

 stores the lasted file 
 
  
## Concurrent Versions System (CVS)
 1986- 1990: open  source 
 multiple files, entire project
 multi- user

## Apach subverison (SVN)
 
 2000: open source
 track text and images 
 track filie changes collectively
 
 
## BitKeeper Scm
 
distrivuted verison control paid verison

 community Verison free
 
 
##  Git 

open- source
Distributed verison control 


   different user maintain their own repositories 
   no central Repository
   change sets can be exhange between repositories
   no single master repository
   many working  changes sets
   each with their own combination of changes sets
   imagine changes to a document as sets A,B,C,D,E,F
   
   * repo 1: A,B,C,D,E,F
   * repo 2: A,B,C,D
   * repo 3: A,B,E,F

  * we could move the repository around 
    
  * faster

  * no network acces required 
  
  * no single Failure point 
   
    * Encourages participation and forking of projects
    * Developers can work independently 
    * submit changes set for inclusion or rejection
    * submit changes set for inclusions or rejection
    
  no need to communicate with a central Server
     
   
   
compatible with Linux,macOS, and windows 
faster than other Scms (100 times)
Explosion in popularity 



installing get on mac 
pre installed a version of git 
installer 


 check git by typing this in terminal

      git --version
      git help
      brew intstall git 
 
 
 
 configuration 
 
  /etc/gitconfig
  program file\Git\etc\gitconfig
  
  
  user 
  ~/.gitconfig
  $HOME\.gitconfig
  
  documents - setting 
  
  or store set by
  
  Project
   
    my_project/.git/config

System
	
	git config --system

User
	
	git config --global

Project

	 git config
	
	 git config --global user.name "paul man"
	 git config --global user.email "email@newSchool.edu"
	 
configure your name globally
and email with 
		
	git config --list
	
gives a list of you configurations

look at  single configuration by looking it up

		 git config user.name 
		 git config
		 
chose your editor
	
		git config --global core.editor " "
		
		git config --global color.ui true


## git auto completion

got to github find the the git repo to 
find autocomplete repo
save the folder user directory
 	 
 	 mv git -completion.bash
 	 mv git -completion.bash mv git -completion.bash
 	 
 	 
in bash profile 
add

	 if[-f ~/.git-completion.bash];then
	 	source ~/.git-completion.bash
	 fi
	 	  


## Git Help


to get useful command lines
	 
	 	git help
get understanding of a command

	 	
	 	git help log
same
	
		git -log
		
		
     
## Start git on a project

what go to document  or make the document 
	
	git init
	cd Documents/
	ls
	cd "document name"/
	ls (checks the folder)
	git init
	ls -la
 
 it has started
  inside the git file
  
  	
 	ls -la .git
 	
 then can configure   or  information about the  the file you u just git 
 the project
 
 	.git/config
 	

track some changes


update and add the changes
then  commit to changes 

 * less then 50 characters on the message
  	
  		git add.
  		git commit -m "intital commit"
  	
  	

# how to view commit

 make sure your in the git folder
 
 /Users$/"usernames"/Documents/First_git_project
 grep is searching for globally experiession 
  
  	 git log
  	
  	 git help log
  	 
  	"gives how to use log"
  	 
  give last 5 logs 
  	 	
  	 	git log -n 5
  	 
  all commits since 
  		 
  		 git log --since=2019-01-01
  	 
  all commits until
   		
   		git log --until=
  		 
  by name 	 
		
		git log -- author="name"
	 
by message 
	
		 git log --grep="init"  	
  	
  	
# Trees
  
  repo: working
  
  repo: staging index : working 

## workflow
  
  git add -a to staging index from working 
  git commit-a from staging to repo1
  
## Hash vaules (sha-1)
  
   * git generates a checksum for each  changeet
   * check sum algorithms convert data into a simple number
   * same data always equals same checksum
   * data integrity is fundamental
   * example: 5c115e8bd540c113cd

### head pointer

 tracking the  where at in the  repo to record and  fast forward and rewind
 
 it's a pointer
  
  sha 
  
  	master                  
  		5c15e8- 38e73D- a614b15 
 	 <br>  head


 	.git/Head    	
 		
 	 cat  .git/refs/head/master
 	 
 	 git log
 	 
 	
will show where the head


## Add files to git 
 	 
 let's you know the status 
 	 
 	 git status
 
 if untrack shows up git knows nothing 
     
     git add ."add alls"
 	 
 	 git add second_file.txt 
 	 	
add one file can add mutlpy files 
 	 
 	 git add second_file.txt third_file.txt 

 
  
### view  the changes 
 	
 	in the folder compares the 
 	 	 			 
 	 	git diff
 	 	
 	 	
###  deletle files 

  techiques to deleting files 
  delete file from the folder 
  peremantly remove can still access to  from old repo

     git status  
     git rm "filename"
     git rm "filename2.txt"
    
    
## git rename file 


rename in the the folder 

	 git status
        git add primay_file.tct
        git rm "file name"
       
 second  techquine     
 
 	git mv second_file.txt  secondary_file.txt
 	git status 

moving and remaning
 	
 	git mv third_file.txt first_folder/third_file.txt
 	git status
  
    
###view documents edit
 with 
 	
 	git status
 and 
 	git  diff
 	
### git commit  stage shortcut

 git commit -a
 git commit --all
 
    					 
  
  	                            	                                         
## git show

	 git show grab some code 
from

	 git log  
 	 git diff  1c16945 .. 9bcff6ef6
 	 git diff  1c16945 .. 9bcff6ef6 --color-words
 	 
 	 
## multlie line 

 this will promtp you editor 
 
 	 git commit -a
 	 
write and close

### small atomic commits


##undo changes
git status will tell what document change
git diff show what was change
	
	git status
 	git diff
 	git status 
 	git checkout -- index.html
 	git status" work tree is clean"
 	
 	
### Unstage file 

	 git status
	 git add name* "astrick will card character"
	 
	 to unstage 
	 git reset HEAD "tour.html"
	 
	 check
	 
### amend comitts


add changes to a change

 	git  add"name"
 	git commit --amend m""
	 

###  getting old files

 	git log
 	git show sha num
 	git checkout sha -- "name of file"
 	git diff --stage	 
 	 
 	 git rest head "name"
 	 
### revert commit

 		git revert "sha "
 
 untracked files
 
  	git clean 
  	git clean -n
  	 git clean -f
  	 
  ingrone file
   to ingore all files name  somelike
   
    log/*.txt
    folder/file/
    
    
    
   track  empty
   
   create new file
     .gitkeep
    

 	
     

# GitHub 
  
* login in to github make a new repo
* name it  and name the folder on your repo the same thing

copy the link  beneath the the title ""

go to terminal

	 git remote add origin [web address]
	 
	 git push origin master
	 
	
 if the repo was dowload from git it is already gitted
 if not go to the folder
  
  	git init
  	git status
	git add remote origin "address"
	git remote -v
	  
 to push do the add status and commit 
 then you can push to pull  to the master
 
 so you can add or download it 
  
# remote stuff 

git remote shows
   
    git remote -v
 
will show you the remote origin 
 
    cat .git/config
    
# remote stuff 

 remove remote 
   	
   		git remote rm "name"
 


shows the  
 	
 	git branch 
 	
 
local master to remote
	
	git push -u origin
	
 shows are remote branches
 
	git branch -r

 shows all branches
  	
  	git branch -a

# How do i create remote a branch in terminal

	git clone "url" name
	

#remote branch tracking 


 shows whats in the folder to show the branches

	cat .git/config

helps with commands 

	git help branch

this a new branch 

	 git branch non_tracking
 
  this  
  
	 git push origin non_tracking 

this will add a branch

u opition is for tracking
what is tracking 

	git branch -u origin/non_tracking  non_tracking 
	
to untrack

	git branch --unset -upstream non_tracking
	

# Push Changes to Remote

 view changes
 	
 	git status
 
 commit 
  
  	git commit -am "sum message"
  
this local
this is the  the last 5 commits
in online 

	git log --oneline -5

 to view the remote
 	
								(name)
		git log --oneline -5 origin/master

can look master and or the  remote branch

view the difference 
	
	git diff master..origin/master
	
push to the remote

	git push origin master
	
or
	
	git push

to view the 

	git log -- oneline -5 origin/master


# Fecthing changes

which branch do i want fetch

 log to view changes
	
		git log --oneline -5 name

check with the remote server if you haven't a in min 

	git fetch origin
or
	git fetch
	

fetch in the morining 
fetch  before you push 
fetch before you go offline 
fetch often

this brings down whats new  fetch just checks 
nothing changes

# Merge fetch changes

 you can merge  remote branchs but you can not checkout 
 
 
 	
 	git log - oneline -5 origin/master

	
you can get the difference 
	
	git  diff origin/master..master
	
merge with local

	git fetch
	
	git merge origin/master
	
git fetch and then git merge

shortcut

	git pull


# check out remote branches

shows the branch
	
	git branch 

shows other branchs 
	
	git branch -r
	
makes new branch 

	git branch "non_tracking origin"/"non_tracking"
		

delete the branch 
	
	git branch -d non_tracking 

	git checkout -b "non_tracking origin"/"non tracking"
	
you do this because you cann't check out a remote but you can branch to you local and checkout those pulls
	
	

# push local changes to remote

pushing when fail the head is behind you fetch and merge

 	git fetch 	
 	git merge
 	git	 push 
 	
# Delete a remote
		
for feature branches
when a feature is done
	
	git branch

shows all 

	git branch -r
	
this deletes a branch 
the for the git remote not the git  


 	git push origin :non_tracking
	

 ### second wa
 
 git push origin --delete branch name
 
	 git push origin --delete "non_tracking" pit


	
	
	
	






	





 
 


    
  
 
	 
	 




# steps followed

# download git and install on your computer

https://kbroman.org/github_tutorial/pages/first_time.html

https://git-scm.com/downloads


# set and configure account on git

git config --global user.name humaasif

git config --global user.email hasif@yoda.bsd.uchicago.edu

help: https://kbroman.org/github_tutorial/pages/first_time.html

# color output in terminal

git config --global color.ui true

# editor

git config --global core.editor vim

# How can I see how Git is configured?

git config --list

git config --list --local

git config --list --global

# To change a configuration value for all of your projects on a particular computer, run the command:

git config --global setting value (setting could be user.name, user.email)

git config --global user.name humaasif

# check git status

git status

 # generate key for github
 
ssh-keygen -t rsa -C hasif@yoda.bsd.uchicago.edu

# i copied the keys in ~/.ssh/
githubKeys     githubKeys.pub

cp githubKeys* ~/.ssh/
mv githubKeys id_rsa
mv githubKeys.pub id_rsa.pub

# check if git working fine 

ssh -T git@github.com

Hi Humaasif! You've successfully authenticated, but GitHub does not provide shell access.

# go to github in browser and create a new repository by clicking new

https://github.com/Humaasif?tab=repositories

 choose repository name ThresholdPaperScript and description as Save all scripts used in GWAS-Paper Elliot group
 # link of this repository
 https://github.com/Humaasif/ThresholdPaperScript
 
 # click tick Initialize this repository with a README
 
 # Make sure you have set git remote URL correctly. 
 
 git remote -v
 
 output : origin	https://github.com/Humaasif/ThresholdPaperScript (fetch)
 # clone repository by typing this in terminal 
 
 git clone https://github.com/Humaasif/ThresholdPaperScript
 
 This command will generate ThresholdPaperScript on Macbook
 # copy filles you want to upload in this folder
 cp  Effective_test_63categories.txt ThresholdPaperScript/
 # Now add files in git staging area
 you must be in ThresholdPaperScript folder to give git add command 
 
 git add Effective_test_63categories.R 
 
 git add visualizecorrelationMatrix-Zongi.R 
 
 # check status (if the file is added or not)
 
 git status
output is :  new file:   Effective_test_63categories.R
 # Save changes in staging area
 
 git commit Effective_test_63categories.R -m "AnnotationCategories-LiandJiEffectiveTestScript"
 
 git commit visualizecorrelationMatrix-Zongi.R -m "visualizationScript"
 
# publish your local commits

git push

# so follow same steps to copy all scripts here.


# when i try to commit and push another file i got rejection so to solve that i did this

git add visualizecorrelationMatrix-Zongi.R 

git commit visualizecorrelationMatrix-Zongi.R -m "visualizationScript"
# Error when push command given

git push 
Error: To https://github.com/Humaasif/ThresholdPaperScript
 ! [rejected]        master -> master (fetch first)
 
# to get rid of error

git fetch origin master

git merge origin master

git push
 
 #  Extra stuff
 # go to macbook terminal in folder where i save scripts for zongi Li and ji effective number of tests and visualization of correlation matrix.
 
 mkdir corrScript-EffectiveNumberOfTest
 # in corrScript-EffectiveNumberOfTest download scripts from server
 scp labuser@128.135.75.151:/mnt/hgfs/Huma/BSNIP_FreeSurfer6/Nyholt-BSNIP_FreeSurfer6/visualizecorrelationMatrixBSNIP1_FS6phenos_CLEAN.R .
 
# long story short commands to add files from macbook to server

git clone https://github.com/Humaasif/ThresholdPaperScript

git add Biotypes-PhenotypesExtraction.R

git commit Biotypes-PhenotypesExtraction.R -m "add this file"

git fetch origin master

git merge origin master

git push


 # track the changes to the commit
 
 git status
 
 if any file is not added in staging area it will be red and display ""nothing added to commit but untracked files present (use "git add" to track)" and a file name in red it mean its not uploaded

#to upload 

git add . (this . will push the file to staging area)

#git status now will be Your branch is up-to-date with 'origin/master'. and file will be green

git commit Effective_test_63categories.txt -m "forgetto upload"

git status

#now will display "nothing to commit, working tree clean"

git push
 
 #command to see list of files that are in the repository, but whose history Git is not currently tracking.
 
git clean -n

#how can i remove these files whose history Git is not currently tracking

git clean -f

Use this command carefully: git clean only works on untracked files, so by definition, their history has not been saved. If you delete them with git clean -f, they're gone for good.
 
 git status
 
 output:
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean





























# Test
Trying how github work

# transfer folder on laptop

git clone https://github.com/Humaasif/Test.git
# to check status
git status
# to add things in staging area
git add grocery list
# to save things in staging area

git commit -m " I am adding grocery list"


git push 

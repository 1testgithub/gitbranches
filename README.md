# gitbranches
1. add files interactive mode:

   git add -i 


2. create a new branch off master branch 

git checkout -b R324b master

3. check branches :

git branch -v

# when no Remote branch for currently LOCAL new branch.  need to do the following
git push --set-upstream origin R324b


* create a new local branch off the remote R324b branch as the following.

git checkout -b R324b-branch origin/R324b



# cherry-pick (whatsever in Master's laest check-in, which can be for R324c branch;  note the changes only for myself,  because others are updating master as well)

* (cherry pick)  http://stackoverflow.com/questions/4024095/push-a-commit-in-two-branches-with-git

1. first find out the 'hash' for the changes checked in Master branch which are not in R324b branch 

git checkout master

git branch -v

   showing ....   
                * master       d7703d7 Added a co

2. now go back to the NEW branch  R324b-branch

git checkout R324b-branch

git cherry-pick d7703d7 


3. Now, push the local NEW branch (R324b-branch) to REMOTE branch (R324b) 

it push origin R324b-branch:R324b






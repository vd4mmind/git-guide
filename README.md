````
# git-guide
## Private git repo for the laboratories

## enter the repo which needs to be pushed to the private git repo and synced to your local machine
### git the folders in the local MAC of the R projects in gitlab 
### initiliaze the git move to folder where you want to
cd /Users/vdas/Documents/Test_lab_projects/Tania_Project_2017/scripts/OC_ORG_MONO_2017

git init

git add .

git commit -a

## vim opens so write initial commit

##add remote server

git remote add gitlab https://gitlab.com/vdas1987/Tania_bulk_OC.git

git push -u gitlab master


### before closing the day to day activity of a project in R just commit and push the project from Rstudio tab which will push it to the remote gitalb in master




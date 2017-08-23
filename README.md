````
# git-guide
## Private git repo for the laboratories

## enter the repo which needs to be pushed to the private git repo and synced to your local machine
cd /path/scripts
git init
git add .
git status
git commit -a ## git all
git remote -v

## go to the corresponding project in the gitLab , name it and copy the link and then use it here, adding git of the HPC to the gitLab repo of the IEO

git remote add OvaCa_RNASeq https://git.ieo.eu/vdas/OvaCa_RNASeq.git
git remote -v

## status
# OvaCa_RNASeq	https://git.ieo.eu/vdas/OvaCa_RNASeq.git (fetch) 
# OvaCa_RNASeq	https://git.ieo.eu/vdas/OvaCa_RNASeq.git (push)

git push OvaCa_RNASeq
# HEAD     master
git push OvaCa_RNASeq master

### Now syncing the same git from your gitLab private repo to your local workstation

## create a dir for all code repo and sub project dir inside of them

mkdir source ## one time

git clone https://git.ieo.eu/vdas/OvaCa_RNASeq.git ## clones the OvaCa_RNASeq repo from the gitLab to your local workstation

cd OvaCa_RNASeq # enter the git repo

git remote -v
#origin	https://git.ieo.eu/vdas/OvaCa_RNASeq.git (fetch)
# origin	https://git.ieo.eu/vdas/OvaCa_RNASeq.git (push)

# create a branch that can be used shared or used for enhancement and developments and all changes will be made on this and not the master node of the git repo 

git branch testDev1

git status

## switching to the branch

git checkout testDev1

git status

## make some random change to see if it works 

vi foo.txt

git commit -a

git add .
git commit -a
# [testDev1 1a4fdff] first test

git push

git remote -v
#origin	https://git.ieo.eu/vdas/OvaCa_RNASeq.git (fetch)
#origin	https://git.ieo.eu/vdas/OvaCa_RNASeq.git (push)

git push origin testDev1 ## pushes and creates the new branch that was made in the local workstation in to the project repo of the gitLab of IEO private
```



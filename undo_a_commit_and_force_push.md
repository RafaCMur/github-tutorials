# How to undo a commit

## Step 1
git reset --soft HEAD~1

## Step 2: Update the branch with the content of master
git pull origin master

## Step 3: Do the commit

## Step 4: See actual branch where I am
git branch  // The one with the asterisk

## Step 5: (may not be needed)
git push origin <my-branch> --force-with-lease

### BE CAREFUL: IT SHOULD BE <MY-BRANCH> NOT MASTER WHEN YOU DO THE PUSH --force-with-lease
### We use --force-with-lease because it prevents accidentally overwriting our teammates' work.

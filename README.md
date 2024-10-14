# Clone repository
git clone https://github.com/devops-intellipaat/merge-conflict.git
cd merge-conflict

# Fetch all branches
git fetch --all

# Update Feature1 with master (apply security patch)
git checkout Feature1
git merge master
# Resolve conflicts (if any), then:
git add main.c
git commit

# Update Feature2 with master (apply security patch)
git checkout Feature2
git merge master
# Resolve conflicts (if any), then:
git add main.c
git commit

# Merge Feature1 into master
git checkout master
git merge Feature1
# Resolve conflicts (if any), then:
git add main.c
git commit

# Merge Feature2 into master
git merge Feature2
# Resolve conflicts (if any), then:
git add main.c
git commit

# Push all branches to GitHub
git remote add personal https://github.com/MukulChauhann/new_repo2.git

git push personal master
git push personal Feature1
git push personal Feature2

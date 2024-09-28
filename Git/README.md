# Git Interview Questions

## Table of Contents

1. <a href="#1">What is a git repository?</a>  
2. <a href="#2">What does git clone do?</a>  
3. <a href="#3">What does the command git config do?</a>  
4. <a href="#4">Can you explain head in terms of git and also tell the number of heads that can be present in a repository?</a>  
5. <a href="#5">What is a conflict?</a>  
6. <a href="#6">What is the functionality of git ls-tree?</a>  
7. <a href="#7">What does git status command do?</a>  
8. <a href="#8">Define “Index”.</a>  
9. <a href="#9">What does git add command do?</a>  
10. <a href="#10">What is a version control system (VCS)?</a>  

11. <a href="#11">What has to be run to squash multiple commits (last N) into a single commit?</a>  
12. <a href="#12">How would you recover a branch that has already pushed changes in the central repository but has been accidentally deleted from every team member’s local machines?</a>  
13. <a href="#13">Can you tell something about git reflog?</a>  
14. <a href="#14">What consists of a commit object?</a>  
15. <a href="#15">Explain the levels in git config and how can you configure values using them?</a>  
16. <a href="#16">What is a detached HEAD and what causes this and how to avoid this?</a>  
17. <a href="#17">What does git annotate command do?</a>  
18. <a href="#18">What is the difference between git stash apply vs git stash pop command?</a>  
19. <a href="#19">What do the git diff and git status commands do?</a>  
20. <a href="#20">Why is it considered to be easy to work on Git?</a>  
21. <a href="#21">How will you create a git repository?</a>  
22. <a href="#22">Tell me something about git stash?</a>  
23. <a href="#23">What is the command used to delete a branch?</a>  
24. <a href="#24">What differentiates between the commands git remote and git clone?</a>  
25. <a href="#25">What does git stash apply command do?</a>  
26. <a href="#26">Differentiate between git pull and git fetch.</a>  
27. <a href="#27">Can you give differences between “pull request” and “branch”?</a>  
28. <a href="#28">Why do we not call git “pull request” as “push request”?</a>  
29. <a href="#29">Can you tell the difference between Git and GitHub?</a>  

30. <a href="#30">How will you resolve conflict in Git?</a>  
31. <a href="#31">What command helps us know the list of branches merged to master?</a>  
32. <a href="#32">What is best advisable step in cases of broken commit: Create an additional commit OR amend an existing commit?</a>  
33. <a href="#33">How to revert a bad commit which is already pushed?</a>  
34. <a href="#34">What is the functionality of “git cherry-pick” command?</a>  
35. <a href="#35">Explain steps involved in removing a file from git index without removing from the local file system?</a>  
36. <a href="#36">What are the factors involved in considering which command to choose among: git merge and git rebase?</a>  
37. <a href="#37">How do you find a commit which broke something after a merge operation?</a>  
38. <a href="#38">What are the functionalities of git reset --mixed and git merge --abort?</a>  
39. <a href="#39">Can you tell the differences between git revert and git reset?</a>  

## Solutions

### <a id="1">1. What is a git repository?</a>
A Git repository is a storage space where your project files and the entire history of changes are tracked. It can exist locally on your machine or on a remote server.

### <a id="2">2. What does git clone do?</a>
The `git clone` command creates a copy of an existing Git repository. It duplicates all files, commit history, and branches from the original repository.

### <a id="3">3. What does the command git config do?</a>
The `git config` command is used to configure Git settings. It can set user information, enable color output, and control other options at the repository or global level.

### <a id="4">4. Can you explain head in terms of git and also tell the number of heads that can be present in a repository?</a>
In Git, `HEAD` refers to the currently checked-out commit. Typically, a repository has one HEAD, but you can have multiple branches, each with its own HEAD.

### <a id="5">5. What is a conflict?</a>
A conflict occurs when two branches have changes to the same line in a file or when one branch deletes a file that another branch modifies. Git requires manual resolution in these cases.

### <a id="6">6. What is the functionality of git ls-tree?</a>
The `git ls-tree` command displays the contents of a tree object, showing the files and directories in a specific commit.

### <a id="7">7. What does git status command do?</a>
The `git status` command shows the current state of the working directory and staging area, indicating which changes are staged, unstaged, or untracked.

### <a id="8">8. Define “Index”.</a>
The index, also known as the staging area, is a temporary area where changes are held before being committed to the repository.

### <a id="9">9. What does git add command do?</a>
The `git add` command stages changes in the working directory for the next commit, moving them to the index.

### <a id="10">10. What is a version control system (VCS)?</a>
A Version Control System (VCS) is software that helps track changes to files and coordinate work among multiple people, allowing for historical access and versioning.

...

### <a id="39">39. Can you tell the differences between git revert and git reset?</a>
`git revert` creates a new commit that undoes changes from a previous commit, preserving history. `git reset`, on the other hand, changes the current branch to a specific state, which can potentially lose history.

# Begin with creating a repo from github first
1. create a repo in github, say HelloGit

2. checkout the project from github to your PC with the
following command:
   git clone https://github.com/github_username/HelloGit.git

3. create new files

4. git add files

5. git commit -m "your message". If commit modified files,
the -a option should be used, namely, git commit -am "your message"

6. git push origin master or other branches


# Adding an existing project to GitHub using the command line
1. Create a new repo in github

2. Change the current working directory to the local project in PC

3. Initialize the local directory as a Git repository
   git init
   
4. Add the files in your new local repository. This stages them for the first commit.
   git add .

5. Commit the files that you've staged in your local repository.
   git commit -m "first commit"

6. Add the URL for the remote repository where your local repository will be pushed
   git remote add origin remote_repo_URL
   
7. Push the changes in your local repository to GitHub
   git push -u origin master
   
   
# Keep the forked repo update with the original repo (called "upstream")

1. Add the remote, call it "upstream":

git remote add upstream https://github.com/whoever/whatever.git

2. Fetch all the branches of that remote into remote-tracking branches, such as upstream/master:

git fetch upstream

3. Make sure that you're on your master branch:

git checkout master

4. Rewrite your master branch so that any commits of yours that aren't already in upstream/master are replayed on top of that other branch:

git rebase upstream/master

5. If you don't want to rewrite the history of your master branch, then you should replace the last command with

git merge upstream/master

6. Force the push in order to push it to your own forked repository on GitHub:

git push -f origin master

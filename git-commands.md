# Git Commands

## Create & Clonning Repositories.
* **git Init** >> Initialize local git repository.
* **git clone [url]** >> create local copy of remote repository.

## Inspect & Make Changes
* **git status** > Check current status of ongoing working branch.
* **git add [file]** > Snapshots the file in preparation for versioning.
* **git add -a** > Snapshots all new or modified files in preparation for versioning.
* **git commit -m "[descriptive message]"** > Records file snapshots permanently in version history
* **git show [commit]** > Outputs metadata and content changes of the specified commit
* **git log** > Lists version history for the current branch
* **git log --follow [file]** > Lists version history for a file, including renames
* **git reset [commit]** > Undoes all commits after [commit], preserving changes locally
* **git reset --hard [commit]** > Discards all history and changes back to the specified commit

## Branches
* **git branch** > lists local branches.
* **git branch -r** > lists remote branches.
* **git branch -a** > lists all local and remote branches.
* **git branch [branch-name]** > Creates a new branch.
* **git checkout [branch-name]** > Switches to the specified branch and updates the working directory.
* **git merge [branch]** > Combines the specified branch’s history into the current branch. This is usually done in pull requests,
but is an important Git operation.
* **git branch -d [branch-name]** > Deletes the specified branch.
* **git push -u origin [branch-name]** > push local branch to remote.

## Tagging
* **git tag** > Listing the existing tags.
* **git tag -l [tag-name]** > see specific "tag-name" series.
* **git tag [tag-name]** > create lightweight tag. it’s just a pointer to a specific commit.
* **git tag -a [tag name]** > create annotated  tag. It stored as full objects in the Git database. optionally can add **-m "my tag descpription"** command.
* **git tag -a [tag-name] [commit]** > create annotated tag at specific **commit**. Usefull when want to label a version at specific commit.
* **git show [tag-name]** > Outputs tag information.
* **git push origin [tag-name]** > By default, the **git push** command doesn’t transfer tags to remote servers. You will have to explicitly push tags after you have created them.
* **git push origin --tags** > push all tags to remote repository.
* **git tag -d [tag-name]** > delete tag on local repository.
* **git push origin --delete [tag-name]** > delete tag on remote repository.
* **git checkout [tag-name]** > to view files on this [tag-name]. Caution, any further commits on this will be point nowhere. better use **git checkout -b version2 [tag-name]** to make changes.
* **git fetch --tags** > This will fetch all remote tags. Optionally can use '--all' keyword.
* **$ git checkout $tag -b latest** > to checkout the latest git tag. where $ tag=$(git describe --tags `git rev-list --tags --max-count=1`) need to apply first. Apply '$ echo $tag' to view latest tag.

## Synchronize Changes
* **git fetch** > Downloads all history from the remote tracking branches.
* **git merge** > Combines remote tracking branch into current local branch.
* **git push** > Uploads all local branch commits to GitHub.
* **git pull** > Updates your current local working branch with all new commits from the corresponding remote branch on GitHub.
 **git pull** is a combination of **git fetch** and **git merge**.
* **git reset HEAD -- path/to/file** > unstage specific file
* **git reset HEAD --** > unstage all changes
 
## Configure 
* **git config --global user.name "[name]"** > Sets the name you want attached to your commit transactions.
* **git config --global user.email "[email address]"** > Sets the email you want attached to your commit transactions.
* **git config --global color.ui auto** > Enables helpful colorization of command line output.
* **.gitgnore** > put excluded file list in this file. See [github.com/github/gitignore](https://github.com/github/gitignore).

## Commits
* **git log** > printing commit message logs. Enter q to exit form log mode.

## Remote repository
* **git config --get remote.origin.url** > display cuurent remote url.
* **git remote add origin https://github.com/user/repo.git** > adding remote repository.
* **git remote set-url origin https://github.com/USERNAME/REPOSITORY.git** > Changing a remote repository's URL.
* **git remote rename origin destination** > Change remote name from 'origin' to 'destination'.
* **git remote rm destination** > Remove remote. example here removing 'destination'. Note: It does not delete the remote repository from the server. It simply removes the remote and its references from your local repository.
* **git remote -v** > Verify remote for the changes made.
 

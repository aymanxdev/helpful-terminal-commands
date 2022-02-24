# Useful Terminal Commands ⌨️ 

Homebrew

Displays installed brews in sorted form

```
brew list --formula | xargs -n1 -P8 -I {} \
    sh -c "brew info {} | egrep '[0-9]* files, ' | sed 's/^.*[0-9]* files, \(.*\)).*$/{} \1/'" | \
    sort -h -r -k2 - | column -t
```

## Git commands 

| Command   | Description  |
| ------------- | ------------- |
|`git commit -a -m` | to commit message after git `git add` however `-a ` doesn't track new files. |
|`git add .`| adds everything in the current directory. If `-A` added i.e `git add -A` will add everything in the repo and not only that directory.|
|`git revert` |allows reverting to changes to be undone if passed the commit hash ID. It won't delete the commit but rather undo the changes.| 
|`git revert HEAD` |undo the most recent commit|
|`git reflog`| to log all the commits in a list|
|`git log --graph --decorate --oneline`| create a better visual representation for the commits logs.| 
|`git log -S "part of the code `| it searches for changes in the repo, in case wanna find which commit created it.| 
|`git stash`| put all the new changes in separate place and brings it back with this command `git stash pop` *only locally*|
|`git branch -vv`| list all the branches |
|`git remote update --prune`| updates git with the lates branches and delete the ones that are no longer exist
|`git branch -vv awk /: gone ]/ {print $1} `|print out branches that are delete| .|
|`git bisect start`| start a binary search|  
|`git bisect bad`| assumes the recent commit is bad.| 
|`git bisect good`| pass commit `hash id` this is the good commit that will compare both bad and good to search for the bug.|  
|`git config --global alias.ac '!git add -A && git commit -m'`|To create a short cut for adding and commiting changes, use this  this will create an easy and short way to commit changes with only one command `git ac"update to commit"`|

## SSH Commands
`pbcopy < ~/.ssh/"enter here id_rsa file name".pub` copies the SSH public key
more about how SSH works internally, watch this excellent [video](https://youtu.be/ORcvSkgdA58)


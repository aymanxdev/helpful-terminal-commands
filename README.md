# Helpful Terminal Commands ⌨️ 

Homebrew

Displays installed brews in sorted form

```
brew list --formula | xargs -n1 -P8 -I {} \
    sh -c "brew info {} | egrep '[0-9]* files, ' | sed 's/^.*[0-9]* files, \(.*\)).*$/{} \1/'" | \
    sort -h -r -k2 - | column -t
```

## Git commands 

`git commit -a -m` to commit message after git `git add` however `-a ` doesn't track new files. 

`git add .` adds everything in the current directory. If `-A` added i.e `git add -A` will add everything in the repo and not only that directory 

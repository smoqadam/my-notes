# Git

**Stash list**  
`git stash list`  
**output:** 

`stash@{0}: ...  
stash@{1}: ...  
stash@{2}: ...`

**Stash only one file**

`git stash show stash@{1}:<filename> > <newfilename>`

#### Save modified files as a zip file

```text
cp $(git ls-files --modified) ../modified-files
```

```text
zip modified-files.zip $(git ls-files --modified)
```


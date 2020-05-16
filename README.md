# git

### Connect Remote Repo To Local Repository.
```
git remote add origin remote_repo_url
```

### git remote url for pull, push
```
git remote -v
```

### push to master/branch
```
git push origin master/branch
```

### git configuration file
```
git config –global user.name “myname”

git config --global user.email "abc@gmail.com"
```
### Getting rid of files already added/committed to git repository and then add them to your .gitignore; (these files will still be present in your repository index)
1. Remove everything tracked by git
```git
git rm -r --cached .
```
* rm is the remove command
* -r will allow recursive removal
* -–cached will only remove files from the index. Your files will still be there.
* The . indicates that all files will be untracked. You can untrack a specific file with git rm --cached foo.txt

* **Caution : The rm command can be unforgiving. If you wish to try what it does beforehand, add the -n or --dry-run flag to test things out **

2. Add everything again
```
git add .
```

3. Commit
```
git commit -m "message here"
```

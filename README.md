## Git Commands


Version number for BASH (Bourne Again Shell) that is running on the platform.
> echo $BASH_VERSION
------
Installed git vesion
> git --version
------

Connect `remote` repo to `local` repository.
> git remote add origin <remote_repo_url>


Git remote url for pull, push
> git remote -v


### Push to master/branch
```
git push origin master/branch
```

Git configuration file

> git config –global user.name “myname”

> git config --global user.email "abc@gmail.com"

Getting rid of files already added/committed to git repository and then add them to your .gitignore; (these files will still be present in your repository index)
```
1. Remove everything tracked by git
git rm -r --cached .

rm is the remove command
-r will allow recursive removal
-–cached will only remove files from the index. Your files will still be there.
The . indicates that all files will be untracked. You can untrack a specific file with git rm --cached foo.txt

Caution : The rm command can be unforgiving. If you wish to try what it does beforehand, add the -n or --dry-run flag to test things out 

2. Add everything again
git add .


3. Commit
git commit -m "message here"
```

The “fatal: refusing to merge unrelated histories” Git error

> git pull origin master --allow-unrelated-histories


Find all the files `tracked` by Git
```
git ls-tree -r <branch_name> --name-only
Example:
git ls-tree -r master --name-only
```

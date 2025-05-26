# Git Instructions
## For those who haven't used git before :)

Git is a giant framework, but to simplify greatly, these are the commands you will be using:

Go to a directory on your desktop where you want to store the project files locally. Open a terminal window and navigate there, and enter this command:
```
git remote add origin https://github.com/sophiatsoukalas/threaded.git
```

To retrieve data from the git repository (either for the first time, or to download changes):
```
git pull origin main
```

To upload new changes:
```
git add <name of files, or '.' for all changed files>
git commit -m "<message to be tagged to the commit>"
git push origin main
```

As an example, let's say I made changes to README.md, and I want to upload those changes. I would run:
```
git add README.md
git commit -m "Added author names to README.md"
git push origin main
```

If I made changes to a whole bunch of files and want to upload all of those changes, I would do:
```
git add .
git commit -m "various updates"
git push origin main
```

Let's say you want to work on a new feature, but don't want to alter the existing code that already works. You would create a new _branch_, go to that branch, and develop on there:
```
git branch <new branch name>
git checkout <new branch name>
blah blah blah git push, git pull, whatever
```

## Commands/options that are useful to have, but you should almost never use:

The `-f` option: e.g. `git push origin main -f`. This flag *forces* changes. It will ignore any backtalk git tries to give, and might fuck shit up if used incorrectly. Do not use this unless you know what the fuck you're doing
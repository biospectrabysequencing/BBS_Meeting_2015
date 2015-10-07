Customising your .gitconfig
===========================

Useful Aliases
--------------

This is a collection of aliases that have so far proven useful to at least one person. If there are 
additions to add, the rules are, alphabetical, include an explanation and the command to execute.

e.g. 

### co

Shorthand for checkout.

```
git config --global alias.co checkout
```

If you have an alias that you are using and wish to augment it, or simply recall the options or details
then git can inform you from the command line.

```bash
$ git alog --help
`git alog' is aliased to `log --graph --oneline --decorate'
```

## Simple Aliases
These are generally similar to Subversion short commands

### br

Shorthand for *branch*
```
git config --global alias.br branch
```

### ci

Shorthand for *commit*
```
git config --global alias.ci commit
```

### co

Shorthand for *checkout*
```
git config --global alias.co checkout
```

### df

Shorthand for *diff*
```
git config --global alias.df diff
```

### lg

Shorthand for *log -p*
```
git config --global alias.lg 'log -p'
```

### lsm

Shorthand for *ls-files -m*, which lists modified files
```
git config --global alias.lsm 'ls-files -m'
```

### rb

Shorthand for *rebase*
```
git config --global alias.rb rebase
```

### st

Shorthand for status
```
git config --global alias.st status
```

### who

Shorthand for *shortlog -s --*, which summarises the contributors
```
git config --global alias.who 'shortlog -s --'
```

## Logging Aliases

The standard git log is a little verbose and difficult to interpret the history 
in a meaningful way. Saving typing and configuring these will aid understanding 
of history directly from the command line.

### alog

Shorthand for *log --graph --oneline --decorate*, which displays branches, head
locations and coloured output for terminals that support it.

```
git config --global alias.alog 'log --graph --oneline --decorate'
```

### flog

Shorthand for *log --name-only --pretty=format:'%Cred%h%Creset - %s %C(bold blue)<%an>%Creset'*, 
which displays the files that were touched in each commit.

```
git config --global alias.flog "log --name-only --pretty=format:'%Cred%h%Creset - %s %C(bold blue)<%an>%Creset'"
```

### plog

Shorthand for a really pretty logging format, similar to alog, but including 
more information, such as contributor and age of commit.
```
git config --global alias.plog "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative"
```

## Merging Aliases

### moff

Shorthand for *merge --no-ff --log*, which stops the updating of head pointer 
and forces a merge commit, even when fast-forward is possible.  The log generates
a log message based on the oneline commit messages of the merge. 

Using moff in a [git-svn workflow](using_git_svn.md) ensures reading and writing 
to a subversion repository while locally managing content with git - "Nice one bruva"

```
git config --global alias.moff 'merge --no-ff --log'
```

### drymerge

Shorthand for the best way to achieve a dry run of a merge - possibly from upstream.
This can be important for preparing yourself for conflicts and resolution of them.
```
git config --global alias.drymerge "!f() { git merge-tree $(git merge-base $2 $1) $1 $2; }; f"
```
Usage:
```
## fetching and merge rather than pull
$ git fetch upstream master

## this will tell you likely sources of conflicts - 3-way merge may still save you
$ git drymerge master upstream/master | grep -A3 'changed in both'
```

## Diff Aliases

Common uses for git diff.

### changes

Shorthand for showing changes similar to lsm, but with a status change.
```
git config --global alias.changes 'diff --name-status -r'
```

### dstat

Shorthand for diff statistics
```
git config --global alias.dstat 'diff --stat -r'
```

### sdf

Shorthand for diff the stage, helpfully s, d & f are adjacent on 
the keyboard, this can be a frequent command...
```
git config --global alias.sdf 'diff --cached'
```

## Stash Aliases

Common uses of the stash.

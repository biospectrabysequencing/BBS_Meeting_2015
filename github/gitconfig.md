gitconfig
=========

Directly from ```man git-config```

The git configuration file contains a number of variables that affect the git command's behavior. The .git/config file in each repository is used to store the configuration for that
repository, and $HOME/.gitconfig is used to store a per-user configuration as fallback values for the .git/config file. The file /etc/gitconfig can be used to store a system-wide 
default configuration.

The configuration variables are used by both the git plumbing and the porcelains. The variables are divided into sections, wherein the fully qualified variable name of the variable
itself is the last dot-separated segment and the section name is everything before the last dot. The variable names are case-insensitive and only alphanumeric characters are allowed.
Some variables may appear multiple times.


## Proxy server configuration

You may need to set up a stanza to traverse a proxy server


```bash
[http]
        proxy = http://[PROXY_ADDRESS]:8080
[https]
        proxy = https://[PROXY_ADDRESS]:8080
```

A [Google search](http://lmgtfy.com/?q=git+through+proxy) can provide additional information.

## colours
Tuning the colours that the console displays during various `git` commands can really add to the experience making the human parsing of text displayed easier. The following text can be added to your `~/.gitconfig`.

```ini
[color]
        ui = true

[color "branch"]
        current = yellow reverse
        local   = yellow
        remote  = green

[color "diff"]
        meta       = yellow bold
        frag       = magenta bold
        old        = red bold
        new        = green bold
        whitespace = red reverse
#       ^
# Highlight whitespace in diffs

[color "status"]
        added     = yellow
        changed   = green
        untracked = cyan
```

...or if you prefer running commands
```bash
git config color.ui true
git config color.branch.current 'yellow reverse'
git config color.branch.local yellow
git config color.branch.remote green 
git config color.diff.meta 'yellow bold'
git config color.diff.frag 'magenta bold'
git config color.diff.old 'red bold'
git config color.diff.new 'green bold'
git config color.diff.whitespace 'red reverse'
git config color.status.added yellow
git config color.status.changed green
git config color.status.untracked cyan
```

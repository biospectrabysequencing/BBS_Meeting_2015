Github gists
============

What is a gist?

[Gists](http://gist.github.com) are a way to document and share code snippets. They are accessible from the link a the top middle of any github page.
You can think of a gist as a cut down github repository, each gist can be public or private (https, and large shasum url) and contain one or many files of content. 

By specifying the filetype of a file as `[FILENAME].md`, automatically sets the filetype as markdown for document rendering.
 
You can only have a master branch, however you can fork an upstream gist url that has been shared with you, clone your origin fork, make changes locally, 
and push those changes back into your fork. Only the owner of an upstream gist repository can merge changes from a fork back into the upstream repository.


Private gist example
--------------------

This ia a (not so) private gist example [3d546ecf98c54d930709](https://gist.github.com/mdavy86/3d546ecf98c54d930709).

So we could clone this gist, in this case user [mdavy86](https://github.com/mdavy86) is the owner of the origin remote;

```
git clone git@gist.github.com:e0bf757fd6c05852c02c.git
```


Set up remotes;

```bash
git remote -v
kiwiroy git@gist.github.com:f15b7e1e22f4fcf6ff1d.git (fetch)
kiwiroy git@gist.github.com:f15b7e1e22f4fcf6ff1d.git (push)
origin  git@gist.github.com:3d546ecf98c54d930709.git (fetch)
origin  git@gist.github.com:3d546ecf98c54d930709.git (push)
```

Make some changes locally, the git alog illustrates that any branching is of the master branch when synchronizing forks.


```bash
git alog | head -n15
* 7dad2f6 (HEAD, origin/master, origin/HEAD, master) README, document()
* 505483e simplify Makefile, consistency
* 8997532 new knitr call, help added, defaults ordering etc
* e25adfa malformed authors@R using person()
* e8c7c75 bug fix, simplify ex fun
* 1a091ca clean
* 60ab2e6 options
*   4a2570b Merge branch 'master' of gist.github.com:f15b7e1e22f4fcf6ff1d
|\
| * ae86672 devtools options
| * 512b39f getopt
| * 4a245a5 git-ize this
* | 6f94139 getopt dependency
|/
* 33724f7 rm auto gen content
```

and push them back to the repository;


```bash
## From local machine
git push origin master
```

Organizing your gists
---------------------

Use [gistbox](http://www.gistboxapp.com) as a mechanism to share and organize your gists with collaborators.


See also
--------

* https://help.github.com/articles/about-gists
* http://www.labnol.org/internet/github-gist-tutorial/28499
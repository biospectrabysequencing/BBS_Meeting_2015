github 101
==========

## Rationale

Using github is essential for collaboration in [biospectrbysequencing](https://github.com/biospectrabysequencing) 
for the following reasons;

* Contributors are cross-company and cross site.
* Promotes Reproducible research
* Audit trail promotes a contribution model
* Leverage open source bioinformatics community e.g. github projects [samtools](https://github.com/samtools/samtools), [bcftools](https://github.com/samtools/bcftools), [vcftools](https://github.com/vcftools/vcftools), [freebayes](https://github.com/ekg/freebayes) etc...
* [5x increase in contributions](https://www.youtube.com/watch?v=U8GBXvdmHT4&t=47m00s)

[![online](http://img.youtube.com/vi/U8GBXvdmHT4/0.jpg)](https://www.youtube.com/watch?v=U8GBXvdmHT4&t=47m00s))


## Training material

We can leverage training material in the public domain

* [Atlassian github tutorials](https://www.atlassian.com/git/tutorials)
* [github help](https://help.github.com)
* [Software caprentry](https://software-carpentry.org)
 + [git novice](https://github.com/swcarpentry/git-novice)


## github setup

Your [.gitconfig](gitconfig.md) file needs to be configured for your user account and traverse company firewalls 

## Setting up aliases
 
See [useful aliases](userful_aliases.md) to save on typing


## Syncing repositories

forks and clones of repositories can get out of sync, how can we tell easily?
[Shasums](https://en.wikipedia.org/wiki/Sha1sum) are used as a [globally unique identifier](https://en.wikipedia.org/wiki/Globally_unique_identifier)
for each commit which contains changs to one or more files.

We can use the [network graph](https://github.com/biospectrabysequencing/BBS_Meeting_2015/network) to see commits in a repository. It illustrates
the mast branch (in black) of the [upstream]() repository, and the position of any forks of the upstream repostiory  and branches that contributors are working on.

Searching for code
==================


An important task is searching for code by `filename`, or underlying `text` within files potentially
across multiple repositories, for example all code which contains the text `samtools sort` for all 
repositories. In the github saerch box type

* [user:biospectrabysequencing tassel](https://github.com/search?utf8=%E2%9C%93&q=user%3Abiospectrabysequencing+tassel&type=Code&ref=searchresults)

We can then identify what code type we are interested in and subset accordingly. Say we are only interest in `shell` code, then we can click on the Language type link
filter for only that type of code

* [user:biospectrabysequencing langauge:Shell tassel](https://github.com/search?l=bash&q=user%3Abiospectrabysequencing+tassel&ref=searchresults&type=Code&utf8=%E2%9C%93)

See [Advanced search GUI](https://github.com/search/advanced) for constructing more complicated search criteria.


## Considerations for code search

This is covered in [Searching code](https://help.github.com/articles/searching-code)
    
* Only the *default branch* is considered. In most cases, this will be the `master` branch.
* Only files smaller than 384 KB are searchable.
* You must always include at least one search term when searching source code. For example, searching for `language:go` is not valid, while `amazing language:go` is.
* At most, search results can show two fragments from the same file, but there may be more results within the file.
* You can't use the following wildcard characters as part of your search query: `. , : ; / \ ` ' " = * ! ? # $ & + ^ | ~ < > ( ) { } [ ].` The search will simply ignore these symbols.


See also
--------

* [Searching code](https://help.github.com/articles/searching-code)
* [Searching github](https://help.github.com/articles/searching-github)
* [Search syntax](https://help.github.com/articles/search-syntax)
* [Advanced search](https://help.github.com/articles/advanced-search)
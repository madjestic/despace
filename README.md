A small utility to replace spaces in a file-name with '_'
                i.e. $ foo bar -> $ foo_bar
Author: 		    Vladimir Lopatin
Maintainer: 		Vladimir Lopatin
Created: 		    Thu Dec 26 03:41:06 CET 2013
Version: 	      0.1.0
Package-Requires:   	(mv)
Last-Updated:       	Mon Apr 14 21:49:31 CEST 2014
By:	                  Vladimir Lopatin
Keywords:             utility, rename files
Compatibility:        all 


Example:
> $ touch "foo bar"
> $ ./despace ./"foo bar"
> $ ls
> > foo_bar
 

Code:

> despace() {
>     if [ -e "$1" ]
>     then 
> 	str="$1"
> 	mv "$1" ${str// /_}
>     fi
> }

> despace "$1"
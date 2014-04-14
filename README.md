### A small utility to replace spaces in a file-name with '_' 


Example:

```bash
$ touch "foo bar"
$ ./despace ./"foo bar"
$ ls
> foo_bar
```

Code:

```bash
despace() {
    if [ -e "$1" ]
    then 
	str="$1"
	mv "$1" ${str// /_}
    fi
}

despace "$1"
```
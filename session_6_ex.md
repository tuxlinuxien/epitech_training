# Session 6

## PART 1

### List of functions required

```
int my_putstring(char *)
int my_putchar(int)
int my_putnumber(int)
```

### List of allowed functions from the standard lib

* write

### Files required

* `$HOME/work/my_put/my_put.c`
* `$HOME/work/my_put/my_put.h`

### Important

* if your project directory contains more or less than 2 files than the ones required => 0/20
* if your project contains a main function or main.c => 0/20
* if your lib generates warnings => 0/20

## PART 2

you will have to write a program called *my_cat* that takes an infinite numbers
of files as arguments.
Same as the command *cat* which display files into your terminal, you will have to write a
similar program that takes files as arguments and display them into the terminal on
`STDOUT`.

If no file is provided as argument, *my_cat* will have to read from `STDIN` and display the output
on `STDOUT`.

If I provide the parameter `-e`, all the carriage returns (`\n`) should be printed as `$`

### Example

```
$> echo "my file 1" > file1.txt
$> echo "my file 2" > file2.txt
$> my_cat file1.txt file2.txt
my file 1
my file 2
my_cat -e file1.txt file2.txt
my file 1$
my file 2$
$> my_cat file1.txt nofile.txt
my file 1
An error has occurred while opening nofile.txt.
$> echo "this is a line" | my_cat
this is a line
$> echo "this is a line" | cat file1.txt
my file 1
$>
```


### Directory required

* `$HOME/work/my_cat/`
* `$HOME/work/my_cat/main.c`

This directory will have to contains a file main.c at the root. You can however
add as many C and Header file as your want.

### List of allowed functions from the standard lib

* open
* read
* write
* close

### Compile

you need to compile your program with gcc and add the following arguments

```
-W -Wall -Werror
```

### Important

* If a file provided as argument does not exist or doesn’t have read permission, you need to
display `An error has occurred while opening <filename>.` on `STDERR`. where `<filename>` is
the name of a file.

* Using printf, putchar, getchar will lead to 0 / 20. You need to code those functions by
yourself and prefix them with `my_`

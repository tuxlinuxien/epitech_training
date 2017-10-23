# Session 5

## PART 1

### List of functions required

```
int my_putstring(char *)
int my_putchar(int c)
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
Same as the command cat which display files into your terminal, you will have to write a
similar program that takes files as arguments and display them into the terminal on
STDOUT.

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

* If a file provided as argument does not exists or doesn’t have read permission, you need to
display `An error has occurred while opening <filename>.` on STDERR. where <filename> is
the name of a file.

* Using printf, putchar, getchar will lead to 0 / 20. You need to code those functions by
yourself and prefix them with `my_`

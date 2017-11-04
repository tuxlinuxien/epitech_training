# Session 7

## PART 1

### List of functions and structure required

```c
typedef struct  List
{
    struct List *next;
    struct List *prev;
    int         val;
}               List;

List *push_front_item(List *,int)
List *push_back_item(List *, int)
int list_size(List *)
void free_list(List *)
```

* `List *push_front_item(List *,int)`
    * takes list item pointer as argument and an integer then returns the item
    created. If your list doesn't have any item, then `NULL` will be provided.
    The new item will be added at the front of the list.
* `List *push_back_item(List *, int)`
    * takes list item pointer as argument and an integer then returns the item
    created. If your list doesn't have any item, then `NULL` will be provided.
    The new item will be added at the end of the list.

### Example

```c

/*
** Header you need for your test.
*/

void display_list_from_beginning(List *list)
{
    // This is just a test function that displays the items from the beginning.
}

int main()
{
    List *my_list = NULL;
    my_list = push_front_item(NULL, 1);
    my_list = push_front_item(my_list, 2);
    my_list = push_back_item(my_list, 3);
    my_list = push_back_item(my_list, 4);
    display_list_from_beginning(my_list);
    printf("items = %d\n", list_size(NULL))
    printf("items = %d\n", list_size(my_list))
    free_list(my_list)
    return 0
}

// After we compile it an run our program
2
1
3
4
items = 0
items = 4
```



### List of allowed functions from the standard lib

* malloc
* free

### Files required

* `$HOME/work/my_list/list.c`
* `$HOME/work/my_list/list.h`

### Important

* if your project directory contains more or less than 2 files than the ones required => 0/20
* if your project contains a main function or main.c => 0/20
* if your lib generates warnings => 0/20

## PART 2

You will have to write a program called *my_ls* that lists the files and directory
of the current working directory. The output will be written on `STDOUT` and errors on
`STDERR`.

If an argument is provided, you will have to display the content of the directory passed in argument.

The output will be in alphabetical order.

### Example

```
$ ls
a.out  Desktop	Documents  Downloads  main.c  Music  Pictures  Public  snap  Templates	Torrent  Videos  work
$ my_ls
a.out  Desktop	Documents  Downloads  main.c  Music  Pictures  Public  snap  Templates	Torrent  Videos  work
$> mkdir my_dir && chmod a-rx my_dir
$ ls my_dir
ls: cannot open directory 'my_dir': Permission denied
$ my_ls my_dir
ls: cannot open directory 'my_dir': Permission denied
$

```


### Directory required

* `$HOME/work/my_ls/`
* `$HOME/work/my_ls/main.c`

This directory will have to contains a file main.c at the root. You can however
add as many C and Header file as your want.

### List of allowed functions from the standard lib

* opendir
* readdir
* closedir
* malloc
* free
* write


### Compile

you need to compile your program with gcc and add the following arguments

```
-W -Wall -Werror
```

# Import for Part 1 and Part 2

* `for` loop, `else if` and `switch` are strictly forbidden and will lead to 0 / 20.
* macro are forbidden (-5 per macro).
* Using printf, putchar, getchar will lead to 0 / 20. You need to code those functions by yourself and prefix them with `my_`
* If I see any commented code in the part 1 or part 2, it will lead to 0 / 20.

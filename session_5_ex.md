# Session 5

## List of functions required

```c
char    *my_stpcpy(char *dest, const char *src);
char    *my_strcat(char *dest, const char *src);
int     my_strcmp(const char *s1, const char *s2);
int     my_strlen(const char *s);
int     my_strcasecmp(const char *s1, const char *s2);
```

## Files required

* `my_string.c`
* `my_string.h`

## Test

```c
#include <stdio.h>
#include "my_string.h"

int     main()
{
    char *str1;
    char *str2;

    str1 = "hello";
    str2 = "world";

    printf("%d\n", my_strlen(str1)); 
    printf("%d\n", my_strlen(str2)); 

    return 0;
}
```

then

```
$> gcc -W -Wall -Werror main.c my_string.c -I./
```

## Important

* if your project directory contains more or less than 2 files than the ones required => 0/20
* if your project contains a main function or main.c => 0/20
* if your lib generates warnings => 0/20

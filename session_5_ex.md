# Session 5

## List of functions required

```c
char    *stpcpy(char *dest, const char *src);
char    *strcat(char *dest, const char *src);
int     strcmp(const char *s1, const char *s2);
size_t  strlen(const char *s);
int     strcasecmp(const char *s1, const char *s2);
```

## Files required

* `my_string.c`
* `my_string.h`

## Test

```c
#include <stdio,h>
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
$> gcc main.c my_string.c -I./
```

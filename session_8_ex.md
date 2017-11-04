# Session 8

## List of allowed functions from the standard lib

* malloc
* free
* write

## Binary name

`my_calc`

## Files required

* `$HOME/work/infinite_calculator/main.c`
* `$HOME/work/infinite_calculator/build.sh`

You can for sure create as many c and header files as you want.

## Compile

you need to compile your program with **gcc** and the following arguments:

```
-W -Wall -Werror
```

The project have to be compiled like:

```
cd $HOME/work/infinite_calculator/ && sh ./build.sh

```

The generated binary should be **my_calc**

## Description

As you already know, numbers like integers or floats have a minimum and a
maximum value (cf session_4.pdf slide 7). The goal of this exercise is to build an
infinite calculator that will print the output on **STDOUT**.

You will have to support the following operators:

* add as `+`
* sub as `-`
* mul as `*`

Example:

```
$> ./my_calc add 123 111
234
$> ./my_calc add 123 -1
122
$> ./my_calc sub 123 111
12
$> ./my_calc sub 123 -111
234
$> ./my_calc mul 1 0
0
$> ./my_calc mul -1 0
0
$> ./my_calc mul 1 10
10
$> ./my_calc mul 10 10
100
./my_calc add 4353254325432534534253425432535324534253534 34537897896573296479843658439659325698435983568439659384659543265983659843563
34537897896573296479843658439659330051690309000974193638084975801308194097097
./my_calc mul 10 10 10
invalid command.
./my_calc mul 10
invalid command.
./my_calc mul
invalid command.
./my_calc mil 10 10
invalid command.
./my_calc mul z 9
invalid command.
```

If an argument is not valid, you will have to print on **STDERR** the following
message

```
invalid command.
```

**For this exercise, you only have to support integers like** *(ex :-1 or 99)*

## Important

* if your program generates warnings => 0/20
* `for` loop, `else if` and `switch` are strictly forbidden => 0 / 20.
* macro are forbidden (-5 per macro).
* If I see any comment or commented code => 0 / 20.
* No more than 5 functions per C file => -1 per extra function.
* No more than 30 lines per function => -1 per extra line.
* If you allocate memory (by using **malloc**), you need to free it => -5 per memory leak
* only *.c, *.h, directories, build.sh or my_calc are allowed during your presentation => -1 per invalid file
* Any abnormal program termination *(ex: SIGSEV/SegFault/Segmentation Fault)* => 0/20

Example of a valid 30 lines function:

```
void    toto(void)
{
// line 1
// line 2
// line 3
// line 4
// line 5
// line 6
// line 7
// line 8
// line 9
// line 10
// line 11
// line 12
// line 13
// line 14
// line 15
// line 16
// line 17
// line 18
// line 19
// line 20
// line 21
// line 22
// line 23
// line 24
// line 25
// line 26
// line 27
}
```

## Code

### Functions

Valid

```c
void toto()
{
    // your code here
}
```

Invalid

```c
void toto() {
    // your code here
}
```

### Indentation

Valid

```c
void toto()
{
    int i = 0;

    i++;
    if (i == 0)
        do_something();
    else
        do_other_thing();
}
```

Invalid

```c
void toto()
{
    int i = 0;
    i++;
    if (i == 0)
    do_something();
    else
    do_other_thing();
}
```

### Block statement

Valid

```c
if (i == 0)
    do_something();
else
    do_other_thing();

// OR

if (i == 0)
{
    do_step_1();
    do_step_2();
}
else
{
    do_step_3();
}

// OR

while (i > 0)
{
    do_something();
}

// OR

while (i > 0)
    do_something();
```

Invalid

```c
if (toto)
    do_something();
else {
    do_something_1();
    do_something_2();
}

// OR

if (toto) {
    do_something();
} else {
    do_something_1();
    do_something_2();
}

// OR

if (toto) {
    do_something();
}
else {
    do_something_1();
    do_something_2();
}
```

## Score

Your project will be scored based on:

* the quality of your code (40%)
    * good function declaration
    * good indentation
    * syntax
* functionalities
    * add (20%)
    * sub (20%)
    * mul (20%)

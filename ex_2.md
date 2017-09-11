# Exercices

## mydbsh

You will have to write a shell script that can store data as a key value storage (ex: Redis).

```sh
$> ./mydbsh v1 val1
$> ./mydbsh v2 val2
$> ./mydbsh r1 rval1
$> ./mydbsh show
v1 val1
v2 val2
r1 rval1
$> ./mydbsh show v1
val1
$> ./mydbsh show-any v*
v1 val1
v2 val2
$> ./mydbsh show-any r*
r1 rval1
$> ./mydbsh del v1
$> ./mydbsh show
v2 val2
r1 rval1
$> ./mydbsh v1 val1_update
$> ./mydbsh show v1
val1_update
$> ./mydbsh flush # this will flush all the data of your database
$> ./mydbsh show
```

The program should exit after every operation and outputs should be alphabetically ordered.

## Hints

Look for **pipe** and **redirection** to:

* save data into a file
* read a file
* filter

## Useful command

* grep
* sort
* uniq
* man

## Errors

Each parameter should be checked. If a wrong command is provided, you should display the folloing message

`Invalid input`


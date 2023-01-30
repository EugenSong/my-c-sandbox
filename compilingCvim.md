Writing and Compiling "Hello World" Program in C - Using Vim
=

### 1) 


```c
#include <stdlib.h>
#include <stdio.h>

int
main()
{
    printf("Hello World!\n");
    return EXIT_SUCCESS;
} 
```

### 2) Save and exit file by 
```ESC ---> :wq ```

### 3) Compile using the following format 
-  want program to be called "hello-world", specify using -o flag 

``` gcc -std=c99 hello-world.c -o hello-world ```

### 4) No output will be seen. The heirarchy looks like so.

``` ~/hello-world/
└── hello-world.c
└── hello-world
```

### 5) Run the following command, exactly.
- note the ./ ; have to intentionally tell shell to look in the *current directory*

``` ./hello-world ```

### Output

```
$./hello-world
Hello World! 
```

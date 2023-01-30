Heap Memory
-
A region of memory that is set aside for dynamic allocation at runtime.
Memory can be allocated and deallocated using the malloc() and free() functions (or calloc() for arrays).
Heap memory continues to exist until it is explicitly deallocated.

Examples:

```c
int* ptr = (int*) malloc(sizeof(int)); // dynamically allocate memory for an int

*ptr = 5; // store the value 5 at the memory location pointed to by ptr

printf("%d", *ptr); // prints 5

free(ptr); // release the memory

```

```c
int* arr = (int*) calloc(10, sizeof(int)); 

for(int i = 0; i < 10; i++) {
    arr[i] = i*2;
}

for(int i = 0; i < 10; i++) {
    printf("%d\n", arr[i]);
}

free(arr);
```

Stack Memory
-
A region of memory that is used for storing local variables and function call frames.
Memory is automatically deallocated when the function that created it returns.
The size of the stack is usually fixed and relatively small.

Dynamic Allocated Memory
-
Memory that is allocated during runtime as opposed to being pre-allocated at compile time.
It can be allocated either in heap or stack, but most of the time it refers to heap memory.
Examples of dynamic allocated memory are the examples provided for heap memory.

-
In summary, Heap memory and stack memory are two different ways in which the memory is managed by the operating system, while dynamic allocated memory refers to the process of allocating memory during the runtime, which can happen either in heap or stack memory.
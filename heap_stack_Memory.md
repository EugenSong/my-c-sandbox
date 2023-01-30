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



Stack Memory vs Heap Memory (Key!)
-

Imagine you're playing a game where you have a toy box. The toy box is like the computer's memory.

When you play with certain toys, like blocks or action figures, you use them for a short time and then put them back in the toy box. These are like the local variables in a program - they're used for a specific purpose and then they're done with. The toy box takes care of cleaning them up and putting them back in the right place. This is like the stack memory in a computer.

But sometimes you have a toy that you want to keep for a long time, like a stuffed animal or a puzzle. You don't want to put it back in the toy box right away, because you want to play with it later. So you keep it out of the toy box and put it somewhere else, like on your bed or in a closet. This is like the heap memory in a computer - you can allocate memory and keep it around as long as you need it.

And that's the difference between local variables and dynamically allocated memory. Local variables are like the toys you play with for a short time and put back in the toy box, while dynamically allocated memory is like the toys you want to keep for a long time and put somewhere else.

-
In summary, Heap memory and stack memory are two different ways in which the memory is managed by the operating system, while dynamic allocated memory refers to the process of allocating memory during the runtime, which can happen either in heap or stack memory.
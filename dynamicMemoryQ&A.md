Dynamic Memory Q&A
=
-
So what sort of variables are labeled as dynamically allocated memory? Variables like global variables?
-

Dynamically allocated memory is memory that is allocated at runtime, rather than at compile-time. Global variables are allocated at compile-time, when the program is first loaded into memory. Therefore, global variables are not considered as dynamically allocated memory.

Dynamically allocated memory typically refers to memory that is allocated and deallocated during the program's execution, using functions like malloc() and free() in C. This is different from stack memory, which is automatically allocated and deallocated as functions are called and returned, and from global variables, which are allocated at the start of the program and remain in memory until the program exits.

A global variable can be considered as a fixed size memory, which is preallocated at the beginning of the program, while a dynamically allocated memory can be considered as a memory that can be allocated or deallocated during the program execution based on the program needs.

So to cement my understanding, dynamically allocated memory are variables that are allocated in my code which prompts the operating system to create space or find space on the computer and which I have to free later on?
-

Yes, that's correct! When you use functions like malloc() or calloc() in C, you are requesting a specific amount of memory from the operating system. The operating system then finds a suitable location in memory for that block of memory and returns a pointer to it. This pointer can be used to access the memory just like any other variable.

It's important to keep in mind that this memory is not automatically deallocated like stack memory is. Once the memory is allocated, it remains allocated until your program explicitly releases it using the free() function. If you do not release the memory, your program will eventually run out of memory and may crash.

So in summary, dynamically allocated memory are variables that are allocated in your code, which prompts the operating system to create space or find space on the computer, and which you have to free later on by using function like free() to prevent memory leaks and make sure that the operating system can use that memory again.

Is it possible to include dynamically allocated memory variables in a function which should use stack memory right? So then are those variables automatically freed or do I have to also free that space?
-

Yes, it is possible to include dynamically allocated memory variables in a function that should use stack memory. When a function is called, the operating system creates a new stack frame for that function, which includes space for local variables, function arguments, and return address. This space is automatically allocated and deallocated as the function is called and returned.

When you include a dynamically allocated memory variable in a function, the pointer to that memory is stored in the stack frame just like any other local variable. However, the actual memory being pointed to is not part of the stack, it is part of the heap.

When the function returns, the stack frame is automatically deallocated, but the dynamically allocated memory remains allocated. This is called a memory leak.

Therefore, when you use dynamically allocated memory inside a function, it's important to make sure that you free it before the function returns. This can be done by calling free() on the pointer, or using smart pointers like std::unique_ptr in C++.

It's worth noting that if you're using a language like C++, and you're using objects with destructors, the destructor of the object is automatically called when the object goes out of scope, so the memory allocated by the object is automatically freed, but if you're using C, you have to manually release the memory using the free() function.

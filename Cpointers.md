Pointers in C
-

```c
char mychar, mychar2;		// init vars, 'mychar' and 'mychar2'


mychar = 'C'; 				// assign a value 'C' at var,'mychar'


char* mypointer;			// create a char pointer 'mypointer'


mypointer = &mychar;	// assign address of 'mychar' to value of 
							pointer, 'mypointer'... 
							pointers only contain addresses


char* mypointer2 = mypointer; // create char ptr, 'mypointer2' 
								and assign value of 'mypointer', an 
								address to it


mypointer2 = &mychar2; 		// reassign 'mypointer2s' value, an address
									to address of 'mychar2' 


*mypointer2 = *mypointer;	// "DEREFERENCE" 'mypointer2' , aka give
								the value of whatever var lies at 
								address found at 'mypointer2's value , 
								the value that lies at 'mypointer' 

```

Notes on Dereference (&) / Pointer (*)
-

```c

& - give me the address

* - 1) go to the address (open the address box and look what's inside
		aka dereference)
		[ int package = *mailbox ] 
  - 2) create a pointer var that holds an address 
  		[char *ptr ... create a char pointer named ptr]

```
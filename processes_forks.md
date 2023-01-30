Processes
=

How to start a new process - *fork()*
-
Process A ---------->

|---- fork() -----> Process B ------------>


**Process A and B are nearly identical copies, both running the same code.**

- Each process has its own pid. 
- Each process returns a different value from fork(). 

- Process B has the same **file descriptor, same variables**


Returns (**pid_t** data type) :

-1 - failure
 
 1. -1 to the parent process ; 
 2. no child process is created
 3. errno is set

0 - success 
	
1. 0 is returned in the child process
2. pid of the child is returned in the parent

How to create 3 processes
-
```c
int main(int argc, char* argv[]) {
	int id = fork();
	if (id != 0) {
		fork();
	}
	print("Hello world"); 
	return 0;
}

```
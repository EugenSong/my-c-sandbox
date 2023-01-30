Structs in C
-

```c
typedef struct { 		// required keywords
string name;			// properties
string number;
} Person; 				// datatype Name

or 

struct Person {
string name;
string number;
};


```

Example
-
```c
int main(void) {

Person people[2];

people[0].name = "Brian";
people[1].number = "12345671";
}


```
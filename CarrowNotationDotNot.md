C Arrow Notation (Shorthand for Dot Notation)
-

Dot notation is used to access struct members. Arrow notation is a shorthand:

```c
(*mystruct_pointer).member == mystruct_pointer->member
```

The main reason for this is because the . operator has higher precedence than the * dereference operator, so you'd have to write a lot of (*a).(*b).(*c) instead of a->b->c


ref: [C Language documentation - operator member access](https://en.cppreference.com/w/c/language/operator_member_access)
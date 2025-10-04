# Stack-in-cpp

Aim: To study the concept of Stack in C++ and implement operations like push, pop, and display.

Tools: VS Code.

## Theory

Stack is a fundamental linear data structure that follows the Last In First Out (LIFO) principle. It is one of the most important and widely used data structures in computer science, serving as the foundation for many algorithms and system-level operations. 

* The last element inserted is the first one to be removed.
  
* It has two main operations:
  1. Push – add an element to the top of the stack.
  2. Pop – remove the top element from the stack.
     
* Can be implemented using arrays or linked lists.
  
* Requires a pointer/index (top) to keep track of the top element.

## Stack Implementation Approaches:

```
class Stack {
private:
    int arr[MAXSIZE];  // Array-based implementation
    int top;           // Index of top element
public:
    Stack() : top(-1) {}  // Initialize empty stack
    
    void push(int data) {
        if (top < MAXSIZE - 1) {
            arr[++top] = data;
        } else {
            cout << "Stack Overflow" << endl;
        }
    }
    
    void pop() {
        if (top >= 0) {
            top--;
        } else {
            cout << "Stack Underflow" << endl;
        }
    }
};
```

## Types of Stack Implementations:

* Array-based Stack: Fixed size, fast access, memory efficient.
  
* Linked List Stack: Dynamic size, flexible memory allocation.

* Template Stack: Generic implementation for any data type.

* STL Stack: Standard library implementation using containers.

## Applications of Stack:

* Function Call Management: Managing function calls and returns

* Expression Evaluation: Infix to postfix conversion, arithmetic expressions

* Syntax Parsing: Compiler design, bracket matching, syntax analysis

* Memory Management: Stack memory allocation for local variables

  
## Program: Stack Implementation Using Array

## Logic:

A Stack class is created with an array to store elements and an integer top to track the top position.push() adds a new element at the top of the stack.
pop() removes the top element. display() traverses and prints all stack elements. Overflow and underflow conditions are handled using checks on top.

## Algorithm:

1. Start

2. Define a class Stack with array and top index.

3. Initialize top = -1 (empty stack).

4. Push Operation:

5. Check if top >= MAX-1 → Overflow

6. Else increment top and insert value

7. Pop Operation:

8. Check if top < 0 → Underflow

9. Else remove element and decrement top

10. Display Operation:

11. Traverse array from 0 to top and print elements

12. In main(), perform multiple push and pop operations.

13. End

## Conclusion

Stacks are simple and useful for tasks like expression evaluation, function call tracking, and undo operations. Using arrays, we can efficiently implement stack operations while handling overflow and underflow conditions.

# Question: Write an algorithm to implement stack using an array.
---
# Answer:
## Algorithm to Implement Stack Using Array

### Definition

A **Stack** is a linear data structure that follows **LIFO (Last In First Out)** principle.

---

## Data Structure Declaration

```
STACK[MAX]
TOP = -1
```

Where:

* `MAX` → Maximum size of stack
* `TOP` → Index of top element
* `TOP = -1` means stack is empty

---

# 1️⃣ Algorithm for isEmpty()

### Condition:

Stack is empty when `TOP = -1`

```
Algorithm isEmpty()

Step 1: If TOP = -1
            Return TRUE
Step 2: Else
            Return FALSE
```

---

# 2️⃣ Algorithm for isFull()

### Condition:

Stack is full when `TOP = MAX - 1`

```
Algorithm isFull()

Step 1: If TOP = MAX - 1
            Return TRUE
Step 2: Else
            Return FALSE
```

---

# 3️⃣ Algorithm for PUSH(STACK, ITEM)

```
Step 1: If isFull()
            Print "Stack Overflow"
            Exit
Step 2: TOP = TOP + 1
Step 3: STACK[TOP] = ITEM
Step 4: Exit
```

---

# 4️⃣ Algorithm for POP(STACK)

```
Step 1: If isEmpty()
            Print "Stack Underflow"
            Exit
Step 2: ITEM = STACK[TOP]
Step 3: TOP = TOP - 1
Step 4: Return ITEM
```

---

# 5️⃣ Algorithm for PEEK()

```
Step 1: If isEmpty()
            Print "Stack is Empty"
            Exit
Step 2: Return STACK[TOP]
```

---

# Question: Draw the Stack Structure for each case when
the following operations are performed on an
empty stack.
1. PUSH A, B, C, D, E, F
2. POP two letters
3. PUSH G
4. POP one letter
5. POP four letters
6. POP one letter
7. PUSH 1,J
8. POP one letter

# Answer:
This is a **stack tracing question**.
We must show the stack structure after **each operation**, starting from an empty stack.

Stack follows **LIFO (Last In First Out)**.

Initial condition:

```
TOP = -1
Stack = Empty
```

---

# Step-by-Step Stack Structure

---

## 1️⃣ PUSH A, B, C, D, E, F

After pushing in order:

```
Top → F
       E
       D
       C
       B
       A
```

(Stack from bottom to top: A B C D E F)

---

## 2️⃣ POP two letters

Pop F and E.

```
Top → D
       C
       B
       A
```

(Stack: A B C D)

---

## 3️⃣ PUSH G

```
Top → G
       D
       C
       B
       A
```

(Stack: A B C D G)

---

## 4️⃣ POP one letter

Pop G.

```
Top → D
       C
       B
       A
```

(Stack: A B C D)

---

## 5️⃣ POP four letters

Pop D, C, B, A.

Stack becomes empty.

```
Stack = Empty
TOP = -1
```

---

## 6️⃣ POP one letter

Stack is already empty.

Result:

```
Stack Underflow
Stack remains Empty
```

---

## 7️⃣ PUSH I, J

Push I first, then J.

```
Top → J
       I
```

(Stack: I J)

---

## 8️⃣ POP one letter

Pop J.

```
Top → I
```

(Stack: I)

---

# Final Stack Content

```
Top → I
```

---

# Qestion: Discuss the application of stack

# Answer:
# Applications of Stack

A **Stack** is a linear data structure that follows the **LIFO (Last In First Out)** principle. It is widely used in computer science for managing data in a specific order.

---

## 1️⃣ Expression Evaluation

Stacks are used to:

* Evaluate **Postfix expressions**
* Evaluate **Prefix expressions**
* Convert **Infix to Postfix/Prefix**

Example:
Postfix: `AB+` → A + B

Compilers use stack to evaluate mathematical expressions.

---

## 2️⃣ Parenthesis Checking

Stack is used to check whether parentheses are balanced.

Example:

* `(A + B)` → Valid
* `(A + B` → Invalid

Algorithm pushes opening brackets and pops when closing bracket is found.

Used in:

* Compilers
* Syntax checking

---

## 3️⃣ Function Calls (Recursion)

Stack is used to manage **function calls**.

When a function is called:

* Its address and local variables are pushed into **Call Stack**
* When function ends, it is popped

Example:
Recursive factorial program uses stack internally.

---

## 4️⃣ Undo and Redo Operations

Used in:

* Text editors (MS Word)
* Paint software

Undo operation:

* Last action is pushed into stack
* When undo is pressed → last action is popped

---

## 5️⃣ Backtracking

Used in:

* Maze solving
* Depth First Search (DFS)
* Puzzle solving

Stack helps to return to previous state when path fails.

---

## 6️⃣ Reversing Data

Stack can reverse:

* Strings
* Numbers
* Lists

Example:
Input: ABCD
Output: DCBA

Push all characters, then pop them.

---

## 7️⃣ Syntax Parsing

Compilers use stack for:

* Parsing programming languages
* Checking syntax errors

---

# Conclusion

Stack is an important data structure used in:

* Expression evaluation
* Recursion
* Parenthesis checking
* Undo/Redo operations
* Backtracking

Because of its **LIFO property**, it is very useful in many real-world applications.

---

# Question: Describe the stack as an Abstract Data Type (ADT), including its operations and properties.

# Answer:
# Stack as an Abstract Data Type (ADT)

## 1️⃣ What is an Abstract Data Type (ADT)?

An **Abstract Data Type (ADT)** is a logical description of a data structure that defines:

* The data
* The operations on the data
* Without specifying how it is implemented

It focuses on **what operations are performed**, not **how they are implemented**.

---

## 2️⃣ Stack as an ADT

A **Stack ADT** is a linear data structure that follows the
**LIFO (Last In First Out)** principle.

In Stack ADT:

* Insertion and deletion happen only at one end called **TOP**.
* The internal implementation (array or linked list) is hidden.

---

# 3️⃣ Operations of Stack ADT

### 1. push(x)

* Inserts element `x` at the top of the stack.
* Condition: Stack should not be full.

### 2. pop()

* Removes and returns the top element.
* Condition: Stack should not be empty.

### 3. peek() / top()

* Returns the top element without removing it.

### 4. isEmpty()

* Returns TRUE if stack is empty.

### 5. isFull()

* Returns TRUE if stack is full (in array implementation).

---

# 4️⃣ Properties of Stack ADT

1. **LIFO Principle**

   * Last inserted element is removed first.

2. **Restricted Access**

   * Elements can be accessed only from the top.

3. **Single End Operation**

   * All operations occur at one end (TOP).

4. **Dynamic or Static Implementation**

   * Can be implemented using:

     * Array (Static)
     * Linked List (Dynamic)

5. **Overflow and Underflow**

   * Overflow → When stack is full
   * Underflow → When stack is empty

---

# 5️⃣ Formal Representation of Stack ADT

A Stack ADT can be represented as:

```
Stack S

Operations:
Create(S)
Push(S, x)
Pop(S)
Peek(S)
IsEmpty(S)
IsFull(S)
```

---

# 6️⃣ Advantages of Stack ADT

* Simple to implement
* Efficient (O(1) operations)
* Useful in recursion, expression evaluation, parsing

---

# Conclusion

Stack as an ADT defines a collection of elements with LIFO behavior and a set of operations such as push, pop, and peek. It hides implementation details and focuses only on behavior and functionality.

---

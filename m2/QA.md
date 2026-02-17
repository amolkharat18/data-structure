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
---


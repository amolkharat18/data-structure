# Write an algorithm to implement stack using an array.
---

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


---


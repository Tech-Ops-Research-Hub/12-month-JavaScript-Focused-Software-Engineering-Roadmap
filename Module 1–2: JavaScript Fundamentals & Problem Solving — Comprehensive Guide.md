# **Module 1–2: JavaScript Fundamentals & Problem Solving (Full Detailed Curriculum)**

**Goal:** Build absolute mastery of JavaScript basics, computational thinking, and problem-solving foundations before touching frameworks or complex systems.

---

# **Module 1: Core JavaScript Fundamentals**

## **1. Core JavaScript Concepts (First Principles Breakdown)**

### **1.1 Variables**

A variable is a *named storage location* in memory that holds a value.
JavaScript provides **let**, **const**, and **var**, but modern JS uses:

* **let** → value can change
* **const** → value cannot be reassigned
* **var** → outdated; avoid due to unexpected behavior

Example:

```javascript
let score = 10;
const country = "Kenya";
```

---

### **1.2 Data Types**

Data types describe the kind of value stored.

#### **Primitive Types (copied by value)**

* **Number** → integers or decimals
* **String** → text
* **Boolean** → true or false
* **Undefined** → declared but no value
* **Null** → intentional “empty” value
* **Symbol** → unique identifiers
* **BigInt** → very large integers

Example:

```javascript
let name = "Amina";
let age = 24;
let isAdmin = false;
let data = null;
```

#### **Reference Types (copied by reference)**

* Object
* Array
* Function

Example:

```javascript
let user = { name: "Amina", age: 24 };
let items = [1, 2, 3];
let greet = () => {};
```

---

### **1.3 Operators**

Operators instruct the computer to perform actions.

#### **Arithmetic**

`+`, `-`, `*`, `/`, `%`, `**`

#### **Comparison**

`==`, `===`, `!=`, `!==`, `>`, `<`

#### **Logical**

`&&`, `||`, `!`

#### **Assignment**

`=`, `+=`, `-=`, etc.

Example:

```javascript
let a = 5;
let b = 10;
let c = a + b;  // 15
```

---

### **1.4 Conditionals**

Control flow based on conditions.

Example:

```javascript
if (age >= 18) {
  console.log("Adult");
} else {
  console.log("Minor");
}
```

---

### **1.5 Loops**

Repeat a block of code.

#### **Common loops**

* `for`
* `while`
* `do…while`
* `for…of`
* `for…in`

Example:

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

---

### **1.6 Functions**

A function is a reusable block of code.

Example:

```javascript
function add(a, b) {
  return a + b;
}
```

---

### **1.7 Recursion**

A function calling itself to solve a smaller version of the same problem.

Example:

```javascript
function countdown(n) {
  if (n === 0) return;
  console.log(n);
  countdown(n - 1);
}
```

---

### **1.8 Scope**

Scope defines where variables are accessible.

* **Global scope** → everywhere
* **Function scope** → inside a function
* **Block scope** → inside `{ }`, applies to `let` and `const`

---

### **1.9 Closures**

A closure occurs when a function remembers variables from its parent scope even after the parent function finishes.

Example:

```javascript
function counter() {
  let count = 0;
  return function () {
    count++;
    return count;
  };
}

let c = counter();
c(); // 1
c(); // 2
```

---

# **Module 2: ES6+ Features, Debugging & Problem Solving**

## **2. ES6+ Features (Modern JavaScript)**

### **2.1 Arrow Functions**

Shorter syntax for functions.

```javascript
const add = (a, b) => a + b;
```

### **2.2 Template Literals**

String formatting using backticks.

```javascript
let name = "Amina";
console.log(`Hello, ${name}`);
```

### **2.3 Destructuring**

Extract values from arrays or objects.

```javascript
const person = { name: "Anna", age: 22 };
const { name, age } = person;
```

### **2.4 Modules**

Split code across files.

```javascript
// add.js
export function add(a, b) { return a + b; }

// main.js
import { add } from "./add.js";
```

### **2.5 Default Parameters**

Set fallback values.

```javascript
function greet(name = "Guest") {
  return `Hello ${name}`;
}
```

---

# **3. Programming Practices**

### **3.1 Debugging**

Using:

* `console.log()`
* breakpoints in browser DevTools
* stepping through code

### **3.2 Console Usage**

Inspect values during execution.

```javascript
console.log({ a, b, message: "Debug info" });
```

### **3.3 Error Handling**

Avoid crashes using `try…catch`.

```javascript
try {
  let result = riskyOperation();
} catch (error) {
  console.error("Something went wrong:", error);
}
```

---

# **4. Basic Algorithms**

### **4.1 Sorting Algorithms**

#### **Bubble Sort (compare neighbors)**

```javascript
function bubbleSort(arr) {
  for (let i = 0; i < arr.length; i++) {
    for (let j = 0; j < arr.length - 1; j++) {
      if (arr[j] > arr[j + 1]) {
        [arr[j], arr[j + 1]] = [arr[j + 1], arr[j]];
      }
    }
  }
  return arr;
}
```

#### **Insertion Sort**

Good for nearly sorted lists.

#### **Selection Sort**

Find minimum each time.

### **4.2 Searching Algorithms**

#### **Linear Search**

Check each element one by one.

#### **Binary Search**

Repeatedly divide sorted array.

---

# **5. Data Structures**

### **5.1 Arrays**

Ordered list of elements.

```javascript
let arr = [10, 20, 30];
```

### **5.2 Stack (LIFO)**

Last-In, First-Out.

Operations:

* `push`
* `pop`

Example:

```javascript
let stack = [];
stack.push(1);
stack.push(2);
stack.pop();
```

### **5.3 Queue (FIFO)**

First-In, First-Out.

```javascript
let queue = [];
queue.push(1);
queue.push(2);
queue.shift();
```

---

# **6. Git & GitHub Basics**

### **6.1 Git Concepts**

* Repository
* Commit
* Branch
* Merge
* Pull Request

### **6.2 Commands**

```bash
git init
git add .
git commit -m "Initial commit"
git branch feature-x
git checkout feature-x
git push
```

### **6.3 Workflow**

1. Create repo
2. Create new branch
3. Make changes
4. Commit
5. Push
6. Open Pull Request

---

# **7. Mini Project: CLI JavaScript Utility**

Choose one:

### **Option 1: CLI Calculator**

Requirements:

* add, subtract, multiply, divide
* error handling for invalid inputs
* interactive prompts (using Node.js `readline`)

### **Option 2: CLI To-Do List**

Features:

* add task
* remove task
* list tasks
* mark task completed
* save tasks to file

### **Option 3: Simple Expense Tracker**

* track expenses
* sum totals
* display categories

---

## 💻 Functions in TypeScript: Your First Steps

Welcome to one of the most fundamental concepts in programming: **functions**\! Functions are like miniature programs or recipes that you write once and can use many times. They allow you to bundle a series of steps (instructions) together, give them a name, and execute them whenever you need to perform a specific task. This is key for making your code organized, reusable, and easy to understand.

-----

### 1\. What is a Function?

Imagine you have a task, like "Calculate the area of a rectangle." You could write the instructions (multiply length by width) every time you need it. Or, you could create a **function** named `calculateArea`. Now, whenever you need the area, you just "call" that function.

In programming terms, a function:

  * **Takes Input:** It can accept data, called **parameters** or **arguments**, that it needs to perform its job.
  * **Does Work:** It contains the instructions (the code block) to process the input.
  * **Returns Output:** It can optionally produce a result, called the **return value**.

-----

### 2\. Basic Function Syntax in TypeScript

TypeScript is built on JavaScript, so the basic function structure is the same. TypeScript just adds **type safety**, which is incredibly helpful for catching errors early\!

#### The Structure:

```typescript
function functionName(parameter1: Type1, parameter2: Type2): ReturnType {
  // Code to execute goes here
  return result; // Optional: send a value back
}
```

#### Example 1: A Simple Greeting Function

Let's create a function that greets a user by name.

```typescript
function greet(name: string): string {
  return "Hello, " + name + "!";
}

// Calling the function
const message = greet("Alice");
console.log(message); // Output: Hello, Alice!
```

| Component | Description |
| :--- | :--- |
| `function` | The keyword that tells TypeScript/JavaScript you're defining a function. |
| `greet` | The **name** of the function. |
| `(name: string)` | The **parameter list**. We specify that the function expects one input, which must be a `string`, and we're calling it `name` inside the function. |
| `: string` | The **return type**. This tells the user (and the TypeScript compiler) that the function is guaranteed to return a `string` value. |
| `return` | The keyword that specifies the value the function sends back as its result. |

-----

### 3\. Functions with No Return Value (`void`)

Sometimes a function performs an action but doesn't need to return a value. For example, a function whose sole job is to print something to the console.

In TypeScript, you specify this using the `void` return type.

#### Example 2: Just Printing

```typescript
function logMessage(message: string): void {
  console.log("LOG:", message);
  // No return statement needed
}

logMessage("System startup successful."); // Output: LOG: System startup successful.
const result = logMessage("Test");
console.log(result); // Output: undefined (because it returns nothing)
```

> **🔑 Key Concept:** `void` means the function will not return a meaningful value. If you omit the return type and the function doesn't return anything, TypeScript often infers it as `void`.

-----

### 4\. Optional and Default Parameters

What if a parameter is not always required? TypeScript offers two ways to handle this.

#### A. Optional Parameters (`?`)

You can make a parameter optional by adding a question mark (`?`) after its name.

```typescript
function buildName(firstName: string, lastName?: string): string {
  if (lastName) {
    return firstName + " " + lastName;
  }
  return firstName;
}

console.log(buildName("Alice", "Smith")); // Output: Alice Smith
console.log(buildName("Bob"));          // Output: Bob
```

#### B. Default Parameters (`=`)

You can provide a default value for a parameter. If the user doesn't pass a value for that parameter, the default value will be used instead.

```typescript
function power(base: number, exponent: number = 2): number {
  return base ** exponent;
}

console.log(power(5, 3)); // Output: 125 (5 * 5 * 5)
console.log(power(5));    // Output: 25 (uses the default exponent: 5 * 5)
```

-----

### 5\. Arrow Functions (The Modern Way)

The previous examples use the traditional `function` keyword. A more modern and often preferred way to write functions in JavaScript and TypeScript is using **arrow functions**. They are more concise, especially for simple, one-line functions.

#### Traditional Function:

```typescript
function add(a: number, b: number): number {
  return a + b;
}
```

#### Arrow Function Equivalent:

```typescript
const add = (a: number, b: number): number => {
  return a + b;
};

// Even shorter for one-line return (implicit return):
const subtract = (a: number, b: number): number => a - b; 

console.log(subtract(10, 3)); // Output: 7
```

In the arrow function syntax:

  * The `function` keyword is replaced by the arrow `=>`.
  * The function is often assigned to a constant variable (like `add`).

Arrow functions are very common in modern TypeScript code, and you'll see them everywhere\!

-----

### 💡 Practice Challenge

Try to write a function called `isEven` that takes one parameter, a `number`, and returns a `boolean` (true or false) indicating if the number is even.

\<details\>
\<summary\>Click for Solution\</summary\>

```typescript
function isEven(num: number): boolean {
  return num % 2 === 0;
}

// Or as an arrow function:
const isEvenArrow = (num: number): boolean => num % 2 === 0;

console.log(isEven(4)); // true
console.log(isEven(7)); // false
```

\</details\>

This concludes the chapter on functions\! Mastering this topic is the key to writing effective and maintainable programs.

-----

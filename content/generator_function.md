
# 📜 JavaScript Generator Functions: Managing Flow and State

Generator functions in JavaScript are a powerful feature introduced in ECMAScript 2015 (ES6). They allow a function's execution to be paused and resumed, fundamentally changing how asynchronous and iterative code is written.

-----

## 1\. The Core Concept: Pausing and Resuming (Beginner)

A standard function executes from start to finish. A **generator function** can stop mid-execution, return a value, and then resume precisely where it left off later.

### Defining a Generator (`function*`)

A generator function is defined using an asterisk (`*`) after the `function` keyword:

```javascript
function* simpleGenerator() {
  console.log("Start");
  yield 1; // Execution pauses here
  console.log("Paused at 1, resuming...");
  yield 2; // Execution pauses here again
  console.log("Paused at 2, finished.");
  return 3; // The final value
}
```

### The Generator Object and `.next()`

When you call a generator function, it **does not run immediately**. Instead, it returns a special **Generator Object** (which is an iterator). To start or resume the generator, you call the **`.next()`** method on this object.

```javascript
const gen = simpleGenerator();

// 1. Start: Runs to the first 'yield'
console.log(gen.next()); 
// Output: Start
//         { value: 1, done: false }

// 2. Resume: Runs from the first 'yield' to the second 'yield'
console.log(gen.next()); 
// Output: Paused at 1, resuming...
//         { value: 2, done: false }

// 3. Finish: Runs from the second 'yield' to the 'return' statement
console.log(gen.next()); 
// Output: Paused at 2, finished.
//         { value: 3, done: true } // 'done: true' signifies completion

// 4. Exhausted: Generator is finished
console.log(gen.next()); 
// Output: { value: undefined, done: true } 
```

### Automatic Iteration with `for...of`

The most common way to consume a generator is using the `for...of` loop, which automatically calls `.next()` until the result's `done` property is `true`.

```javascript
for (const value of simpleGenerator()) {
  console.log(`Received: ${value}`);
}
// Output: Received: 1
//         Received: 2
// (Note: The final 'return 3' value is ignored by 'for...of')
```

-----

## 2\. Advanced Control Flow: Delegation and Co-Routines (Advanced)

Generators become truly powerful when used for composition and two-way communication.

### A. Delegation with `yield*`

The **`yield*`** operator allows one generator to delegate its control to another iterable (like another generator, an array, or a string). This is excellent for **composition** and keeping logic modular.

```javascript
function* countUp(limit) {
    for (let i = 1; i <= limit; i++) {
        yield i;
    }
}

function* mainReporter() {
    yield "--- Start Count ---";
    // Delegate control to the 'countUp' generator
    yield* countUp(3); 
    yield "--- Count Finished ---";
}

// Sequence yielded: "--- Start Count ---", 1, 2, 3, "--- Count Finished ---"
for (const item of mainReporter()) {
    console.log(item);
}
```

### B. Bi-Directional Communication (Co-Routines)

Unlike standard functions, generators can **receive** values while they are paused, turning them into **co-routines**.

The value you pass into `gen.next(value)` is assigned as the **result** of the `yield` expression *inside* the generator.

```javascript
function* calculator() {
  let sum = 0;
  
  // 1. First call to .next() starts the generator and runs to here.
  //    The result of this first yield (the input) is always undefined initially.
  let input = yield `Start sum is ${sum}`; 
  
  while (input !== 0) {
    sum += input;
    // 2. Pauses here and returns the current sum.
    //    When resumed, 'input' receives the value passed into gen.next(value).
    input = yield `Current sum: ${sum}`; 
  }
  
  return sum;
}

const calc = calculator();

// 1. Start the generator
console.log(calc.next().value); // Output: Start sum is 0

// 2. Send 10 into the generator
console.log(calc.next(10).value); // Output: Current sum: 10 (sum = 10)

// 3. Send 5 into the generator
console.log(calc.next(5).value);  // Output: Current sum: 15 (sum = 15)

// 4. Send 0 to exit the loop and return the final value
console.log(calc.next(0));      
// Output: { value: 15, done: true }
```

### C. Error and Cleanup Methods

You can control a running generator's state from the outside using these advanced methods:

  * **`gen.throw(error)`**: Injects an error into the generator at its current paused location. This causes the generator to throw the error as if it happened during execution, allowing the generator's internal `try...catch` blocks to handle it.
  * **`gen.return(value)`**: Forces the generator to complete immediately. The final value passed in becomes the value of the last result object.

<!-- end list -->

```javascript
function* cleanupGen() {
  try {
    yield 1;
    yield 2;
  } catch (e) {
    console.error("Generator caught external error!");
  } finally {
    console.log("Generator cleanup complete.");
  }
}

const cgen = cleanupGen();
cgen.next(); // Yields 1

// Force the generator to terminate:
cgen.return();
// Output: Generator cleanup complete.
//         { value: 'Finished', done: true }
```

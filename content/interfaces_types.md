# 📘 Chapter: Mastering Interfaces and Types in TypeScript

TypeScript's defining feature is its **static type system**, which allows you to describe the shape of objects, functions, and data, helping catch errors before your code even runs. The two main tools for defining these shapes are **Interfaces** and **Type Aliases**.

-----

## 🚀 1 The Basics: Describing Data Structures

The most fundamental use of both `interface` and `type` is to define the structure of an object.

### 🍎 1.1 Interfaces (`interface`)

An `interface` is a contract that an object must follow. It traditionally defines the shape of an object.

```typescript
interface Person {
  firstName: string;
  lastName: string;
  age: number;
}

// An object that adheres to the contract
const user: Person = {
  firstName: "Alice",
  lastName: "Johnson",
  age: 30,
};

// Error: Property 'age' is missing
// const invalidUser: Person = { firstName: "Bob", lastName: "Smith" };
```

### 🍇 1.2 Type Aliases (`type`)

A `type` alias is simply a new name for any type—it can be an object type, a primitive, or a complex union.

```typescript
// 1. Alias for a primitive type
type UserID = string;

// 2. Alias for an object structure
type Point = {
  x: number;
  y: number;
};

const myPoint: Point = { x: 10, y: 20 };
const id: UserID = "abc-123";
```

-----

## ✨ 2 Key Features: Modifiers and Flexibility

Both interfaces and types allow you to define object properties with more flexibility.

### ❓ 2.1 Optional Properties

You can mark a property as optional by adding a question mark (`?`) after the property name. This means an object *may* have the property, but is not required to.

```typescript
interface Book {
  title: string;
  author: string;
  // year is optional
  year?: number;
}

const modernBook: Book = { title: "TS Handbook", author: "Dev" }; // Valid
const oldBook: Book = { title: "Classic", author: "Anon", year: 1800 }; // Also valid
```

### 🔒 2.2 Readonly Properties

You can ensure a property cannot be changed after the object is first created by using the `readonly` keyword.

```typescript
type Config = {
  readonly apiKey: string;
  debugMode: boolean;
};

const appConfig: Config = {
  apiKey: "12345",
  debugMode: true,
};

// appConfig.apiKey = "67890"; // Error: Cannot assign to 'apiKey' because it is a read-only property.
appConfig.debugMode = false; // Valid
```

### 🏷️ 2.3 Index Signatures (Flexible Keys)

Sometimes, you don't know the exact names of all properties in advance, but you know their keys (e.g., they are all strings) and their corresponding values (e.g., they are all numbers). This is common for dictionary-like objects.

```typescript
interface PriceList {
  // Key (property name) must be a string, value must be a number
  [key: string]: number;
}

const inventoryPrices: PriceList = {
  apple: 1.0,
  banana: 0.5,
  // 3: 5.0, // Error: Key is treated as a string, but the value must be a number (and it is, so this is valid)
  "three-pack": 5.0,
};

const price = inventoryPrices.apple; // price is number
```

-----

## 🧩 3 Advanced Types: Composing Complex Shapes

This is where the power of type aliases really shines, allowing you to combine existing types in complex ways.

### 🤝 3.1 Union Types (`|`)

A **Union Type** allows a variable to be one of several types. The vertical bar (`|`) signifies "or."

```typescript
// A variable can hold either a string OR a number
type StringOrNumber = string | number;

let idValue: StringOrNumber = 101;
idValue = "A101"; // Valid

// A variable can only be one of these three specific string values
type Direction = "up" | "down" | "left" | "right";

let move: Direction = "up";
// move = "forward"; // Error: Type '"forward"' is not assignable to type 'Direction'.
```

### 🕸️ 3.2 Intersection Types (`&`)

An **Intersection Type** combines multiple types into one. The new type has **all** the properties of the combined types. The ampersand (`&`) signifies "and."

```typescript
interface Name {
  name: string;
}

interface Age {
  age: number;
}

// The Employee type must have BOTH a 'name' and an 'age' property.
type Employee = Name & Age;

const fullTime: Employee = { name: "Carol", age: 45 };
```

### 🔑 3.3 Type Lookups (Indexed Access Types)

You can use the `typeof` operator and bracket notation (`[]`) to extract the type of a property from another type.

```typescript
interface User {
  id: number;
  name: string;
  settings: {
    theme: 'dark' | 'light';
    notifications: boolean;
  }
}

// Extracts the type of the 'settings' property:
type UserSettings = User['settings']; 
// UserSettings is now: { theme: 'dark' | 'light'; notifications: boolean; }

// Extracts the union type of the possible keys of the User object:
type UserKeys = keyof User; // 'id' | 'name' | 'settings'
```

-----

## 🔁 4 Interface vs. Type: When to Use Which

The line between `interface` and `type` has blurred over time, but there are still key differences that guide professional usage.

| Feature | `interface` | `type` |
| :--- | :--- | :--- |
| **Object Shape** | Yes, primary use. | Yes. |
| **Primitives/Unions/Tuples** | No. | Yes, can name any type. |
| **Declaration Merging** | Yes, can be defined multiple times and they merge. | No. |
| **Extending/Implementing** | Use `extends` (more natural for object hierarchy). | Use `&` (intersection) for object composition. |

### 1\. Declaration Merging (Interfaces Win)

If you declare the same interface twice, TypeScript will merge them into a single, combined interface. This is very useful in large codebases or when working with third-party libraries (e.g., adding custom properties to an existing library interface).

```typescript
// First declaration
interface Box {
  width: number;
}

// Second declaration (later in a different file)
interface Box {
  height: number;
}

// The resulting Box interface has BOTH width and height.
const myBox: Box = { width: 10, height: 20 };
```

### 2\. Unions and Primitives (Types Win)

If you need to define a non-object type (like a union, a primitive alias, or a tuple), you *must* use a `type` alias.

```typescript
// Union: type
type Status = "success" | "error";

// Tuple: type
type RgbColor = [number, number, number];

// Primitive Alias: type
type Name = string;
```

> **📚 General Rule of Thumb:** Use **`interface`** when defining the shape of an object that will be implemented or extended. Use **`type`** when defining anything else, especially for unions, intersections, and aliases for primitives or complex conditional types.

-----

## 🔧 5 Utility Types (Advanced)

TypeScript provides built-in "Utility Types" to perform common type transformations. These are excellent examples of advanced type manipulation.

### 🤏 5.1 `Partial<T>`

Makes all properties of an interface/type `T` optional.

```typescript
interface UserData {
  id: number;
  name: string;
  email: string;
}

// All properties in UpdateData are now optional: id?, name?, email?
type UpdateData = Partial<UserData>;

const update: UpdateData = { email: "new@example.com" }; // Valid to only include one property
```

### 🚫 5.2 `Omit<T, K>`

Creates a type by picking all properties from `T` and then removing a set of keys `K`.

```typescript
// The original UserData is defined above

// Removes 'id' and 'email' properties from UserData
type UserDetails = Omit<UserData, 'id' | 'email'>;

/*
UserDetails is now: {
  name: string;
}
*/
```

### ⛏️ 5.3 `Pick<T, K>`

Creates a type by picking only a set of properties `K` from an interface/type `T`.

```typescript
// The original UserData is defined above

// Only picks 'id' and 'name' properties from UserData
type UserSummary = Pick<UserData, 'id' | 'name'>;

/*
UserSummary is now: {
  id: number;
  name: string;
}
*/
```

By mastering these concepts, you can write TypeScript code that is not only type-safe but also clean, composable, and maintainable, regardless of the complexity of your application.

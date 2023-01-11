---
title: FewV minutes of Types in Typescript.
publishdate: 2022-12-30T08:11:12-07:00
author: Vishakha Sawra
draft: false
description: Let us understand the different types used in Typescript
tags:
  - typescript

youtube: ux59GUKLxGs
---

## >> Types in TypeScript

1. When creating a variable, there are two main ways TypeScript assigns a type:

2. Explicit and Implicit.

## >> Explicit

3. Explicit - It means defining the type of a variable, Wether it is a string, number, or boolean.

```ts
let firstName: string = "John";
let myAge: number = 30;
```

## >> Implicit

4. Implicit - It maens TypeScript will have to guess the type based on the assigned value.

```ts
let lastName = "Doe";
let age = 30;
```

5. This is called as infer, where TS have to guess the type of value

6. Implicit type assignment are shorter and are faster to type.

7. Now where we can get the error.

**ERROR: TypeScript will throw an error if data types do not match.**

Example

8. Error for Explicit type:

```ts
let firstName: string = "John"; // type string
firstName = 33; // re-assigning the value to a different type
// Type 'number' is not assignable to type 'string'.
```

Here we defined the type of firstName to be a **string** and then if we try to re-assign it's type, TypeScript will throw an error.

9. Error for Implicit type:

```ts
let lastName = "Doe"; // inferred to type string
lastName = 33; // re-assigning the value to a different type
// Type 'number' is not assignable to type 'string'.
```

Here TypeScript already guessed the type of lastName to be a **string** and then if we try to re-assign it's type, TypeScript will throw an error.

## >> Special Types

10. There are special type which are used in TypeScript and they are
    **_Any, Unknown, never, null, undefined_**

## >> Any Type

1. Any type disable the type checking.

2. It is mostly not used in practice.

```ts
let hobbies: any[] = ["Cooking", "Sports", 5, true];
```

**Console:**

```
["Cooking", "Sports", 5, true]
```

## >> Unknown Type

1. Unknown is safer alternative to **any**.

2. Unknown is best used when we don't know the type of data being typed.

```ts
let myHobbies: unknown[] = ["Cooking", "Sports", 5, true];
```

**Console:**

```
["Cooking", "Sports", 5, true]
```

## >> Never, Undefined, Null Types

1. Never, Undefined, Null are not used in practice.

2. They don't hold much meaning in TypeScript.

```ts
// Never
let a: never = true; //never returns a value

// Undefined
let b: undefined = undefined;

// Null
let c: null = null;
```

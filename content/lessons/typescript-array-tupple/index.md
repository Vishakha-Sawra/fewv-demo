---
title: FewV minutes of Arrays and Tupple in Typescript.
publishdate: 2023-01-10T08:11:12-07:00
author: Vishakha Sawra
draft: false
description: Let us understand Arrays and Tupple in Typescript
tags:
  - typescript

youtube: RZA4_Uhn1Lc
---

## >> Arrays in TypeScript

1. For Arrays in TypeScript, We have a specific syntax for typing out an array.

2. And that is as follows

```ts
const names: string[] = ["John", "Jane", "Mary"];

const ages: number[] = [25, 30, 27];
```

Console:

```
["John", "Jane", "Mary"]

[25, 30, 27]
```

3. **names** is a variable which has a type of **string** and the square brackets means the variable **names** is an array containing various values like _John_, _Jane_, _Mary_.

4. Similarly, **ages** is a variable which has a type of **number** and the square brackets means the variable **ages** is an array containing various values like 25, 30, 27.

5. Now if we want to add a value in **names** or **ages** we can do it with **push** property.

```ts
names.push("Bob");

ages.push(10);
```

Console:

```
["John", "Jane", "Mary", "Bob"]

[25, 30, 27, 10]
```

## >> Readonly Arrays in TypeScript

6. Now what if we want arrays to remain unchanged, for this we have **readonly** keyword, which will prevent array from being changed.

7. It is typed as

```ts
// Readonly array
const books: readonly string[] = ["Harry Potter", "Lord of the Rings"];
```

8. And now if we try to add another book in **books** variable, TypeScript will throw an error.

```ts
books.push("Almond"); //error => Property 'push' does not exist on type 'readonly string[]'
```

## >> Type infer Arrays

9. TypeScript can also infer(guess) the type of an array based on it's value.

```ts
// Array type inference
let myFavBooks = ["Harry Potter", "Lord of the Rings"];
// TypeScript infered the type of myFavBooks to string.
```

10. But what if we by mistakenly we change the type of **myFavBooks**, TS will throw error.

```ts
myFavBooks.push(21);
//error => Argument of type 'number' is not assignable to parameter of type 'string'.
```

11. Which means we cannot use any other type than what is already infered by TS at first.

---

## >> Tuple in TypeScript.

1. A tuple is a typed array with a fixed length and fixed types for each index.

2. To define a tuple, we have to specify the type of each element that is in the array.

```ts
let ourTuple: [string, number];
ourTuple = ["John", 25];
```

Console:

```
["John", 25]
```

3. But we add an extra value, we will get error

```ts
let ourTuple: [string, number];
ourTuple = ["John", 25, true];
// error => Type '[string, number, boolean]' is not assignable to type '[string, number]'.
// Source has 3 element(s) but target allows only 2.
```

---

# Generic Function Arguments

### Problem

https://typehero.dev/challenge/generic-function-arguments

#

### Problem Description

In TypeScript, functions often need to pass generic type arguments for flexibility in handling different data types. For example, a function might need to return an object with a specific type for its properties. The syntax `<T,>` helps distinguish between generic functions and JSX, resolving ambiguity in the TypeScript compiler. This challenge involves creating an identity function (`const identity = undefined;`) that returns its input unchanged and a more complex `mapArray` function (`const mapArray = (arr, fn) => arr.map(fn);`) to demonstrate practical use of generics.


#

### Solution

```ts
const identity = <T>(val:T) => val;

const mapArray = <T,C>(arr: T[], fn:(val: T) => C) => arr.map(fn);
```



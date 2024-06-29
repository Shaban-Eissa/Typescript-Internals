# Concat

### Problem

https://typehero.dev/challenge/concat

#

### Problem Description

Implement the JavaScript Array.concat function in the type system. A type takes the two arguments. The output should be a new array that includes inputs in ltr order

For example:
```ts
type Result = Concat<[1], [2]> // expected to be [1, 2]
```

#

### Solution

```ts
type Concat<T extends readonly any[], U extends readonly any[]> = [...T , ...U]; 
```



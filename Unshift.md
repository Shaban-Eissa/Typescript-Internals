# Unshift

### Problem

https://typehero.dev/challenge/unshift

#

### Problem Description

Implement the type version of Array.unshift

For example:
```ts
type Result = Unshift<[1, 2], 0> // [0, 1, 2,]
```

#

### Solution

```ts
type Unshift<T, U> = T extends any[] ? [U, ...T] : never;
```



# Reverse

### Problem

https://typehero.dev/challenge/reverse

#

### Problem Description

Implement the type version of Array.reverse

For example:
```ts
type a = Reverse<['a', 'b']> // ['b', 'a']
type b = Reverse<['a', 'b', 'c']> // ['c', 'b', 'a']
```

#

### Solution

```ts
type Reverse<T extends any[]> = T extends [infer F, ...infer R] ? [...Reverse<R>, F] : [];
```



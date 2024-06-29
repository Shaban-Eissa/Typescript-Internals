# Filter

### Problem

https://typehero.dev/challenge/filter

#

### Problem Description

Implement the type Filter<T, Predicate> takes an Array T, primitive type or union primitive type Predicate and returns an Array include the elements of Predicate.

#

### Solution

```ts
type Filter<T extends any[], P> = T extends [infer F, ...infer R]
  ? F extends P
    ? [F, ...Filter<R, P>]
    : Filter<R, P>
  : [];
```



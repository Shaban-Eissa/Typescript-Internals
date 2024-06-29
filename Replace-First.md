# Replace First

### Problem

https://typehero.dev/challenge/replace-first

#

### Problem Description

Implement the type ReplaceFirst<T, S, R> which will replace the first occurrence of S in a tuple T with R. If no such S exists in T, the result should be T.

#

### Solution

```ts
type ReplaceFirst<T extends readonly unknown[], S, R> = T extends [
  infer F,
  ...infer Rest
]
  ? F extends S
    ? [R, ...Rest]
    : [F, ...ReplaceFirst<Rest, S, R>]
  : [];
```



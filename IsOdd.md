# IsOdd

### Problem

https://typehero.dev/challenge/isodd

#

### Problem Description

return true is a number is odd

#

### Solution

```ts
type IsOdd<T extends number> = `${T}` extends `${string}${1 | 3 | 5 | 7 | 9}`
  ? true
  : false;
```



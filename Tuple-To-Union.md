# Tuple to Union

### Problem

https://typehero.dev/challenge/tuple-to-union

#

### Problem Description

Implement a generic TupleToUnion<T> which covers the values of a tuple to its values union.

For example : 
```ts
type Arr = ['1', '2', '3']

type Test = TupleToUnion<Arr> // expected to be '1' | '2' | '3'
```


#

### Solution

```ts
type TupleToUnion<T extends any[]> = T[number];
```



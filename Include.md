# Includes

### Problem

https://typehero.dev/challenge/includes

#

### Problem Description

Implement the JavaScript Array.includes function in the type system. A type takes the two arguments. The output should be a boolean true or false.

For example:
```ts
type isPillarMen = Includes<['Kars', 'Esidisi', 'Wamuu', 'Santana'], 'Dio'> // expected to be `false`
```

#

### Solution

```ts
type Equal<X, Y> = (<T>() => T extends X ? 1 : 2) extends <T>() => T extends Y
  ? 1
  : 2
  ? true
  : false;

type Includes<T extends readonly any[], U> = T extends [
  infer First,
  ...infer Rest
]
  ? Equal<U, First> extends true
    ? true
    : Includes<Rest, U>
  : false;
```



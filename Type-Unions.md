# Type Unions

### Problem

https://typehero.dev/challenge/type-unions

#

### Problem Description

Type unions in TypeScript help prevent errors by distinguishing between different units. Unions are created using a pipe (|) to combine multiple type aliases, enabling functions to handle each unit appropriately. Unions are unordered, unique, and can include the never type, representing an empty union. This makes the code safer and more reliable by enforcing correct usage of types.


#

### Solution

```ts
// Part 1: Meters
type Meters = {
  unit: 'meters';
  value: number;
};

type Miles = {
  unit: 'miles';
  value: number;
};

type Feet = {
  unit: 'feet',
  value: number
}

type Distance = Meters | Miles | Feet;

/////////////////////////////////////////////////
// Part 2: position
type Position = 'left' | 'center' | 'right' | 'top' | 'topLeft' | 'topRight' |'bottom' | 'bottomLeft' | 'bottomRight' ;
```



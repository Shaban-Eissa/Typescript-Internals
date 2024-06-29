# Omit

### Problem

https://typehero.dev/challenge/omit

#

### Problem Description

Implement the built-in Omit<T, K> generic without using it.

Constructs a type by picking all properties from T and then removing K

For example : 
```ts
interface Todo {
  title: string
  description: string
  completed: boolean
}

type TodoPreview = MyOmit<Todo, 'description' | 'title'>

const todo: TodoPreview = {
  completed: false,
}
```

#

### Solution

```ts
type MyOmit<T, K extends keyof T> = {
  [P in Exclude<keyof T, K>]: T[P];
};
```



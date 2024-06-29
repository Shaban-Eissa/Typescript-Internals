# Awaited

### Problem

https://typehero.dev/challenge/awaited

#

### Problem Description

If we have a type which is a wrapped type like Promise, how we can get the type which is inside the wrapped type?

For example: if we have Promise<ExampleType> how to get ExampleType?


```ts
type ExampleType = Promise<string>

type Result = MyAwaited<ExampleType> // string
```

#

### Solution

```ts
type MyAwaited<T extends PromiseLike<any>> = T extends PromiseLike<infer Inner> 
  ? Inner extends PromiseLike<any> 
		? MyAwaited<Inner> 
		: Inner
	: never;
```



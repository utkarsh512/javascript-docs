# Learning JavaScript

In this repository, I will be listing core constructs in JavaScript and creating analogies with C++ and Python.

## General Tips

* Always use `let` keyword or `const` keyword to declare variables, don't ever use `var` keyword.
* Refer to [Moziila Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) for references.

## What are `const` and `let` keywords?

`const` and `let` keywords are use to declare variables in JavaScript.

* Variables declared using `const` in JavaScript are similar constant pointers in C++. As in C++, we cannot change the pointer value for a constant pointer, but can modify the pointee, similarly in JavaScript, variables declared as `const` cannot be initialized again, but the internal object can be changed.

```javascript
// [JavaScript]
const arr = [1, 2, 3, 4];
arr.push(7);     // Pointee can be modified
arr = [2, 3, 4]; // Error: Cannot initialize it again
```

```cpp
// [C++ equivalent]
int a = 2, b = 3;
int * const p = &a;
*p = 7;         // Pointee can be modifed
p = &b;         // Error: Cannot change pointee of a constant pointer
```

* Variables declared using `let` in JavaScript are similar to:
  *  non-const pointers in C++
  *  variables in Python

## Mutable and Immutable types

The concepts of mutability and immutability of types in JavaScript is similar to that of Python, i.e., built-in types like integer, string, etc. are immutable, but arrays, objects, etc. are mutable.

## Iterating over an array

### Using index-based approach

```javascript
// [JavaScript]
const arr = [1, 2, 3, 4, 5];
for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}
```

### Using for/of loop

```javascript
// [JavaScript]
const arr = [1, 2, 3, 4, 5, 6];
for (const x of arr) {
  console.log(x);
}
```

```cpp
// [C++ equivalent]
std::vector<int> v = {1, 2, 3, 4, 5, 6};
for (auto x : v) {
  std::cout << x << std::endl;
}

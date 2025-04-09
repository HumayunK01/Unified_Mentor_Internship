# JavaScript Closures Demo

This project demonstrates the concept of closures in JavaScript through a practical example. Closures are a fundamental concept in JavaScript that allows functions to maintain access to variables from their outer scope even after the outer function has finished executing.

## What is a Closure?

A closure is a function that has access to its own scope, the outer function's variables, and global variables, even after the outer function has returned. This is possible because the inner function maintains a reference to its outer scope.

## Code Explanation

```javascript
function clickCounter() {
  let count = 0;  // 'count' is scoped to this function

  // Return an inner function that "closes over" the 'count' variable
  return function() {
    count++;
    document.getElementById('countDisplay').textContent = `Button clicked ${count} times.`;
  };
}

const counter = clickCounter();  // counter now remembers 'count'
```

### Key Components:

1. **Outer Function (`clickCounter`)**:
   - Creates a local variable `count`
   - Returns an inner function

2. **Inner Function**:
   - Has access to the `count` variable
   - Increments the count
   - Updates the display

3. **Closure Creation**:
   - `const counter = clickCounter()` creates a closure
   - The returned function maintains access to `count`

## How It Works

1. When `clickCounter()` is called, it:
   - Creates a new scope with `count = 0`
   - Returns the inner function
   - The inner function "closes over" the `count` variable

2. Each time the button is clicked:
   - The closure function is executed
   - It has access to the same `count` variable
   - The count is incremented and displayed

## Benefits of Closures

1. **Data Privacy**: Variables in the outer function are not accessible from outside
2. **State Maintenance**: The closure maintains state between function calls
3. **Module Pattern**: Enables the creation of modules with private variables

## Practical Applications

Closures are commonly used for:
- Event handlers
- Callback functions
- Module patterns
- Data privacy
- Function factories

## Resources

- [MDN Web Docs - Closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)
- [JavaScript.info - Closures](https://javascript.info/closure)
- [W3Schools - JavaScript Closures](https://www.w3schools.com/js/js_function_closures.asp)

## How to Test

1. Open `index.html` in a web browser
2. Click the "Click Me" button multiple times
3. Observe how the counter maintains its state between clicks 
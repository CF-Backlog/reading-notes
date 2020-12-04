## The Call Stack

### What is a call stack?
  > a mechanism for an interpreter (such as JS) to keep track of its place in a script which calls multiple functions

### What are call stacks used for?
  > function invocations

### How do call stacks work?
  > Last In, First Out Principle (LIFO)
    - the last function that gets pushed into the stack is the first to come out when the function is returned
  > Temporary Storage
    - when a function is called, the function is pushed into the call stack to form a *stack frame*
  > Manage function calls
    - maintains a record of the position of each stack frame
    - allows JS to be synchronous

## Stackoverflow

## JavaScript Error Messages

> Types of error messages are:
  > Reference errors: tried to use a variable that is not yet declared. A simple fix is declaring the variables before any declaration is made. For example:
    <!-- ```js
    let foo;
    foo = 'Hello';
    ``` -->
  > Syntax errors: come from misplaced quotes, semi-colons, parentheses, etc.
  > Range errors: when an object being manipulated that has length is given an invalid length (like negative).
  > Type errors: show up when types are incompatible (numbers, strings, etc).
> The easiest way to debug your JS is `console.log`
> You can use the Chrome Developer Tools using `cmd+o`. To choose a file to debug, click the line and refresh the page.
> You can also create a breakpoint with a `debugger` statement where you want to break.

> The call stack is given by the **red** part of an error message. The article explains how to use the debugger to analyze the call stack:

> Paired with breakpoints it is easier to create a code execution in scenarios 
> like this by taking into account the call stack which is available, for example, 
> in chrome developer tools “sources” tab.
> Naming functions makes the call stack easier to navigate.
>`console.trace()` prints out the current call stack trace.
>You can handle errors by using `try` and `catch`. For example:

  <!-- ```js
  (function testing(){
    function add(a, b) {
      try {
        var result = a + b
        return result.split('')
      } catch (error) {
        console.error('add went wrong ->', error)
        return [] // default value
      }
    }
    var stringResult = add("1", "2")
    var numberResult = add(1, 2)
  })()
  ``` -->

> Because JS is not compiled, your errors happen at runtime. That means you can only see what's wrong after it is running.
> You can use tools like quokka, eslint, and TypeScript to detect errors faster.

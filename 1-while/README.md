# Part I: While

Before getting started, make sure that you have a JavaScript console open (like <a href="http://www.repl.it/languages/javascript" target="_blank">repl.it</a>), so you can complete these exercises.

## Exercises

### Basic Requirements

1. **Summation to `n`:** Let's implement the function `sum` that takes a single
   parameter `n`, and computes the sum of all integers up to `n` starting from
   `0`, *e.g.*:

   ```js
   function sum(n) {
     // TODO: your code here
   }
   sum(3); // => 6
   sum(4); // => 10
   sum(5); // => 15
   ```

2. **Factorial of `n`:** The factorial of `n` is the *product* of all the
   integers preceding `n`, starting with `1`, *e.g.*:

   ```js
   function factorial(n) {
     // TODO: your code here
   }
   factorial(3); // => 6
   factorial(4); // => 24
   factorial(5); // => 120
   ```

3. **Repeating a String `n` Times:** Let's write a function called
   `repeatString` that takes two parameters: a string `str`, which is the string
   to be repeated, and `count` -- a number representing how many times the
   string `s` should be repeated, *e.g.*

   ```js
   function repeatString(str, count) {
     // TODO: your code here
   }
   repeatString('dog', 0); // => ''
   repeatString('dog', 1); // => 'dog'
   repeatString('dog', 2); // => 'dogdog'
   repeatString('dog', 3); // => 'dogdogdog'
   ```

   Your task is to implement the `repeatString` function using a `while` loop.

### More Practice

1. Modify your `sum` function from the **Basic Requirements** section to accept
   *two* parameters, `start` and `end`: `sum` should now compute the sum of the
   numbers from `start` to `end`, *e.g.*

   ```js
   function sum(start, end) {
     // TODO: your code here
   }
   sum(2, 7); // => 2 + 3 + 4 + 5 + 6 + 7 => 27
   sum(3, 5); // => 3 + 4 + 5 => 12
   ```

   + What happens if `start` is larger than `end`? Modify `sum` to check for this
     case and, when found, swap the `start` and `end` arguments.

2. Let's pretend for a moment that JavaScript does not have the addition
   operator `+` -- instead, it comes with two functions called `inc` and `dec`
   that perform *increment* and *decrement* respectively:

   ```js
   // ignore the fact that inc makes use of +
   function inc(x) {
     return x + 1;
   }

   function dec(x) {
     return x - 1;
   }
   ```

   Your task is to write a function called `add` that takes two numbers as
   parameters, `x` and `y`, and adds them together. The catch is that you can
   *only* use `inc` and `dec` to accomplish this.

3. Write a function called `isEven` that, given a number `n` as a parameter,
   returns `true` if that number is *even*, and `false` otherwise; however, you
   need to do this **without using the `%` operator.**

4. Write a function called `multiply` that accepts two numbers as parameters,
   and multiplies them together -- but without using the `*` operator; instead,
   you'll need to use repeated addition.

### Advanced

1. **Compute the `n`th Fibonacci Number:** The fibonacci numbers are represented by the
   following sequence:

   ```js
   // fib(n): 1 1 2 3 5 8 13 21
   //         | | | | | |  |  |
   //      n: 0 1 2 3 4 5  6  7
   ```

   That is, `fib(0)` is 1, `fib(1)` is 1, `fib(2)` is 2, `fib(3)` is 3, `fib(4)`
   is 5, etc.

   Notice that each fibonacci number can be computed by adding the **previous
   two** fibonacci numbers, with the exception of the first two: `fib(0)` and
   `fib(1)`. More succinctly,

   + `fib(0)` is `1`
   + `fib(1)` is `1`
   + `fib(n)` is `fib(n - 1) + fib(n - 2)`

   Write a function called `fib` that accepts a number `n` as a parameter and
   computes the `n`th fibonacci number using the above rules.

2. By now you should have worked with the `length` property of strings, *e.g.*
   `"hello".length`. Your task is to write a function called `stringLength` that
   accepts a string as a parameter and computes the length of that string;
   however, as you may have guessed, you are not allowed to use the `length`
   property of the string!

   Instead, you'll need to make use of the string method called `slice`. To
   get an idea of how `slice` works, try the following at a console:

   ```js
   "hello".slice(0);
   "hello".slice(1);
   "".slice(1);
   ```

   For our purposes, we can consider `slice` as taking one argument -- the
   **index** to begin slicing from, and returns a new string starting from that
   index onwards.

   **Indices** are *positions* of characters within strings, and they always
   begin counting from 0, *e.g.*:

   ```js
   // "h e l l o" (spaces added for clarity)
   //  | | | | |
   //  0 1 2 3 4
   ```

   The `"h"` character has index (position) `0` in the string `"hello"`, `"e"`
   has index `1`, `l` has index `2`, etc.

3. The "modulo" operator (`%`) computes the *remainder* after dividing its left
   operand by its right one, *e.g.*

   ```js
   5 % 2; // => 1
   8 % 10; // => 8
   7 % 5; // => 2
   ```

   Write a function called `modulo` that works like the `%` operator, but
   without using it.

4. Write a function called `countChars` that accepts two parameters: a `string`
   and a `character`. This function should return a number representing the
   number of times that the `character` appears in `string`. To access the
   *first* element of a string, you can use the following syntax:

   ```js
   // access the element at index 0
   "hello"[0]; // => "h"
   "dog"[0]; // => "d"
   ```

   **HINT:** You'll also need to make use of the `slice` method as shown above
   in the exercise on computing the length of a string.

5. Implement a function called `indexOf` that accepts two paramters: a `string`
   and a `character`, and returns the *first* index of `character` in the
   `string`. You'll need to make use of the techniques for accessing the *first*
   element of a string and the *rest* of the string (`slice`) as before.

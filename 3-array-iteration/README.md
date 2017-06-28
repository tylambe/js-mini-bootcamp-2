# Part III: Array Iteration

Before getting started, make sure that you have a JavaScript console open (like <a href="http://www.repl.it/languages/javascript" target="_blank">repl.it</a>), so you can complete these exercises.

## Exercises

Try to write *all* of the exercises using **both** the `for` loop *and* `while`
loop.

### Basic Requirements


1. Write a function `sum` that computes the sum of the numbers in an array.

2. Write a function `max` that accepts an array of numbers and returns the
   *largest* number in the array.

3. Try the following at a console:

  ```js
  "the quick brown fox jumped over the lazy dog".split(" ");
  "Hello, world!".split("")
  "1,2,3,4,5,6".split(",")
  ```

  What is returned by `split` (You can read more about it
  [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)),
  and how does it work?

  Use `split` to write a function `longestWord` that takes a string as an
  argument and returns the longest word.

4. Write a function `remove` that accepts an *array* and an *element*, and
   returns an array with all ocurrences of *element* removed.

   ```js
   function remove(array, element) {
     // your code here
   }
   remove([1, 3, 6, 2, 3], 3); // => [1, 6, 2]
   ```

5. Write a function `evens` that accepts an array as an argument, and returns
   an array consisting of all of the *even* numbers in that array.

### More Practice

1. Write a function called `average` that takes an array of numbers as a
   parameter and returns the *average* of those numbers.

2. Write a function called `min` that finds the *smallest* number in an array of
   numbers.

3. Write a function `shortestWord` that works like `longestWord`, but returns
   the *shortest* word instead.

4. Write a function `countChar` that takes two arguments: any string, and a
   *character* (string of one letter), and returns the number of times that the
   character occurs in the string.

5. Write a function `evenLengthWords` that takes an array of *strings* as an
   argument, and returns an array of just the words that have an even length.

### Advanced

1. Read about the `join` method on
   [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join)
   and use it to implement a function that accepts a string as an argument and
   returns that string *reversed*.

2. Write a function `keep` that "keeps" certain elements in an array. The
   function will need to take *two* arguments, an array, and something else --
   the second argument will be what is used to determine which elements to keep.

   You should be able to use this function to write `evens`, `evenLengthWords`,
   a hypothetical `odds` function, or `oddLengthWords` *without changing the
   `keep` function*.

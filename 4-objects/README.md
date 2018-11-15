# Part IV: Objects

Before getting started, make sure that you have a JavaScript console open (like <a href="http://www.repl.it/languages/javascript" target="_blank">repl.it</a>), so you can complete these exercises.

## Exercises

### Basic Requirements

#### Syntax & Style

Fix the syntax & style issues with the three objects below:

```js
{firstName "Josh", lastname: "Lehman" }
{a: 1, b:2 c: 3 d 4}
{
    animal: "dog"
    noise: "bark",
        age: 3,
  type "Labrador"
     color: "Yellow",
}
```

#### Creating Objects

1.  Create an object that represents *you*. It should contain your first name,
    last name, age and hometown.

2.  Add three more key/value pairs to your object that represent other attributes
    of yourself. Ideas include (but are not limited to):
    - Favorite TV Shows/Movies/Sports/Activities etc.
    - Occupation
    - Date of Birth
    - Pets (number of pets, names of pets, etc.)

    **HINT:** You can just modify the object that you created before.

3.  The values in an object can be objects themselves, and in fact, this is a
    very common pattern. For example, consider the following object that
    represents a computer:

    ```js
    var computer = {
      brand: "Apple",
      year: 2014,
      model: "MacBook Pro",
      size: "15-inch",
      specs: {
        processor: "2.3GHz Intel Core i7",
        memory: "16 GB 1600 MHz DDR3",
        graphics: "Intel Iris Pro 1536 MB"
      }
    }
    ```

    You should notice that the `specs` key in the `computer` object is an object
    itself! We could access information about the processor using dot-notation
    like so:

    ```js
    computer.specs.processor; // => "2.3GHz Intel Core i7"
    ```

    Change your object to have a `name` key, the value of which is an *object*
    &#x2013; this object should have `first`, `last` and `middle` keys
    containing your first, last, and middle names respectively (make sure to
    *remove* the `firstName` and `lastName` keys that you added before). You
    should be able to access your *last name* afterwards like so (assuming your
    object is called `you`):

    ```js
    you.name.last; // => YOUR LAST NAME
    ```

4.  Look up your favorite movie on IMDB, and make an object that represents some
    aspects of that movie, *e.g.*:
    - Title
    - Director
    - Year released
    - Rating
    - Actors

    **HINT:** Most movies have multiple actors. What data-structure do we use to
    represent a collection of similar things?

#### Creating New Key/Value Pairs

**Perform these exercises in a console!**

1. Create a new empty object in your console called `obj` like this:

   ```js
   var obj = {};
   ```

2. Add a new key/value pair to the object `obj` by *assigning* a new value to a
   new key like so:

   ```js
   obj.hello = "world";
   obj["number"] = 25;
   ```

3. Now, check the value of `obj` in the console and ensure that it has the two
   key/value pairs added above. This is how we create new key/value pairs in
   existing objects.

4. In the console, add a `favoriteColor`
   key/value pair to the object that represents you.

#### Accessing Values by Key

1.  Fix the attempts to access values in the `person` object:

    ```js
    var key = "name";
    var person = {
        name: "Alyssa P. Hacker",
        age: 26,
        hometown: "somewhere"
    };
    person[age]; // => 26
    person.key; // => "Alyssa P. Hacker"
    ```

2. Write a function `fullName` that takes a person object as an argument, and
   returns that person's full name as a string. By *person object*, we mean an
   object that has the structure of the object you created to represent
   yourself above, for example:

   ```js
   var alyssa = {
     name: {
       first: "Alyssa",
       middle: "P.",
       last: "Hacker"
     },
     age: 26
   };

   function fullName(person) {
     // TODO: your code here
   }

   fullName(alyssa); // => "Alyssa P. Hacker"
   ```

3. What happens if you pass a person object to `fullName` that doesn't have a
   middle name?

   ```js
   fullName({name: {first: "John", last: "Doe"}}); // => "John Doe"
   ```

   Your `fullName` function should work correctly regardless of whether or not
   the person has a middle name -- if it doesn't produce the output shown above
   when given the object `{name: {first: "John", last: "Doe"}}`, fix it so that
   it does.

4. We often deal with **arrays of objects**; below is an example of an array of
   objects, where each object represents a *person*:

   ```js
   var people = [
     {name: {first: "Alyssa", middle: "P.", last: "Hacker"}, age: 26},
     {name: {first: "Ben", last: "Bitdiddle"}, age: 34},
     {name: {first: "Eva", middle: "Lu", last: "Ator"}, age: 40},
     {name: {first: "Lem", middle: "E.", last: "Tweakit"}, age: 45},
     {name: {first: "Louis", last: "Reasoner"}, age: 21}
   ];
   ```

   1. Add the object representing yourself to this array of people (if your
      `name` key does not have the same "shape" as the ones above, make sure you
      change it to look like these).
   2. Write a function that, when passed an array of *people* (person objects) as
      an argument, returns an array of their **full names**. Can you make use of
      your `fullName` function here?
   3. Write a function that finds the average age of the `people` array.
   4. Write a function that, when given *people* and an *age* as arguments,
      returns an array of just the people that are older than the specified age.

#### Iterating over Keys & Values

1. The following object has a number of key/value pairs that need to be removed:

   ```js
   var dirtyObject = {
     _fht: 192492,
     name: "Alyssa P. Hacker",
     age: 26,
     _byz: 939205,
     _ttrs: 510852
   }
   function clean(obj) {
     // ...
   }
   clean(dirtyObject); // => {name: "Alyssa P. Hacker", age: 26}
   ```

   The function `clean` should accept an object as an argument and return a new
   object that has all of the key/value pairs of its parameter except for those
   that begin with `_`.

2. Write a function `removeOddValues` that takes an object as an argument and
   returns an object with all key/value pairs removed for which the value holds
   an *odd number*. You'll need to use the \`typeof\` operator to first check that
   the values are numbers:

   ```js
   typeof "Hello"
   typeof 3
   ```

### More Practice

1. Look around at various physical objects in the room, or think about
   activities that you enjoy. How would you represent this *things* as objects?
   Practice creating objects to represent different things. Some ideas include:

   - Your favorite drink
   - A recipe
   - Sports or hobbies
   - Your car/bike/hoverboard/vehicle-like thing
   - Literally anything

2. Write a function `countWords` that, when given a string as an argument,
   returns an *object* where *keys* are the words in the string, and *values*
   are the number of occurrences of that word within the string:

   ```js
   function countWords(s) {
   // ...
   }
   countWords("hello hello"); // => {"hello": 2}
   countWords("Hello hello"); // => {"Hello": 1, "hello": 1}
   countWords("The quick brown"); // => {"The": 1, "quick": 1, "brown": 1}
   ```

   **HINT:** You will want to make use of the string method `split`. Try
   `\"Hello hello".split(" ")` at a console to see how it works.

   - Modify `countWords` to be *case insensitive* by using the following string
     method (experiment at a console with it to learn its behavior):

   ```js
   "HElLo".toLowerCase(); // => ???
   ```

3. Write a function `countCharacters` that, when given a string as an argument,
   returns an object containing counts of the ocurrences of each *character* in
   the string.

   ```js
   function countCharacters(s) {
     // ...
   }
   countCharacters("hello"); // => {"h": 1, "e": 1, "l": 2, "o": 1}
   ```

   **HINT:** You will want to make use of the string method `split`. Try
   `\"hello".split("")` at a console to see how it works.

4. Write a function `select` that accepts two arguments: an object and an
   array. The **array** should contain names of keys that will be *selected* from
   the object:

   ```js
   function select(obj, keys) {
     // ...
   }
   select({a: 1, b: 2, c: 3}, ["a"]); // => {a: 1}
   select({a: 1, b: 2, c: 3}, ["a", "c"]); // => {a: 1, c: 3}
   select({a: 1, b: 2, c: 3}, ["a", "c", "d"]); // => {a: 1, c: 3}
   ```

5. Write a function `extends` that accepts two objects as arguments, and
   *extends* all of the key/value pairs of the second one to the first one.

   ```js
   function extend(obj1, obj2) {
     // ...
   }
   extend({a: 1}, {b: 2}); // => {a: 1, b: 2}
   extend({a: 1, c: 3}, {b: 2, c: 4}); // => {a: 1, b: 2, c: 4}
   ```

### Advanced

1. The function `Object.keys` returns an array of an object's *keys*. Experiment
   with it at the console like this:

   ```js
   Object.keys({a: 1, b: 2});
   ```

   Using this property, write versions of the above functions using repetition
   through function invocation (*i.e.* recursion)

2. The function `JSON.stringify` turns arbitrary JavaScript data structures
   (arrays and objects) into strings. Try it out in a console like this:

   ```js
   JSON.stringify({a: 1, b: 2, c: ["dog", "cat", "zebra"], d: true});
   JSON.stringify([5, 7, 2, 4, 0, 20]);
   var people = [
      {name: {first: "Alyssa", middle: "P.", last: "Hacker"}, age: 26},
      {name: {first: "Ben", last: "Bitdiddle"}, age: 34},
      {name: {first: "Eva", middle: "Lu", last: "Ator"}, age: 40},
      {name: {first: "Lem", middle: "E.", last: "Tweakit"}, age: 45},
      {name: {first: "Louis", last: "Reasoner"}, age: 21}
   ];
   JSON.stringify(people);
   ```

   Write a function `stringify` that works *exactly* like `JSON.stringify`.

   **HINT:** This will be much easier to accomplish with repetition through
   function invocation than with iteration.

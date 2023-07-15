## Javascript Review and Practice

## type conversion and string concatenation in JavaScript. 

1. Sum an integer and a string representation of an integer.
2. Sum a floating-point number and a string representation of a floating-point number.
3. Concatenate two strings.

Here is how to approach each one:

1. To sum the integer and the string representation of an integer, we first need to convert the string to an integer. We can use the built-in JavaScript function `parseInt()` for this purpose. `parseInt()` takes a string as an argument and returns its integer representation.

2. To sum a floating-point number and a string representation of a floating-point number, we'll use the `parseFloat()` function, which is similar to `parseInt()`, but it's used for floating-point numbers (numbers with decimal points).

3. To concatenate the two strings, we can simply use the `+` operator. This operator, when used with strings, joins them together.

Now, let's fill in the missing parts of your code:

```javascript
function performOperation(secondInteger, secondDecimal, secondString) {
    // Declare a variable named 'firstInteger' and initialize with integer value 4.
    const firstInteger = 4;
    
    // Declare a variable named 'firstDecimal' and initialize with floating-point value 4.0.
    const firstDecimal = 4.0;
    
    // Declare a variable named 'firstString' and initialize with the string "HackerRank".
    const firstString = 'HackerRank ';
    
    // Write code that uses console.log to print the sum of the 'firstInteger' and 'secondInteger' (converted to a Number type) on a new line.
    console.log(firstInteger + parseInt(secondInteger));
    
    // Write code that uses console.log to print the sum of 'firstDecimal' and 'secondDecimal' (converted to a Number type) on a new line.
    console.log(firstDecimal + parseFloat(secondDecimal));
    
    // Write code that uses console.log to print the concatenation of 'firstString' and 'secondString' on a new line. The variable 'firstString' must be printed first.
    console.log(firstString + secondString);
}
```

Now, when `performOperation()` is called with the second set of values, it will print the desired outputs. It's important to note that JavaScript has dynamic typing, which means that a variable can be of any type and can be changed. However, when performing operations, we need to make sure that the types are compatible or explicitly convert them to a compatible type, as we did in this problem.

## Vowels and Consonants
implement a function that prints all vowels in a given string first, each on a new line, in the order they appear in the string, and then does the same for consonants. 

**This is a great opportunity to understand control flow in JavaScript with loops and conditional statements. Here's how you could implement this function:**

```javascript
function vowelsAndConsonants(s) {
    let vowels = 'aeiou';
    let consonants = '';

    for(let i = 0; i < s.length; i++) {
        if(vowels.includes(s[i]))
            console.log(s[i]);
        else
            consonants += s[i];
    }

    for(let i = 0; i < consonants.length; i++)
        console.log(consonants[i]);
}

```

Here's a step-by-step breakdown of the code:

1. Define the vowels in a string for comparison.

2. Initialize an empty string `consonants` to hold the consonants in `s`.

3. Loop over each character in the input string `s`. If a character is included in the `vowels` string, we immediately print it out. If not, we add it to the `consonants` string.

4. After handling all the vowels, loop over the `consonants` string and print each character.

Remember, strings in JavaScript are iterable, like arrays. The `includes()` method checks if the string contains a certain character, returning `true` if it does, `false` otherwise. The `+=` operator is used to concatenate strings.

Lastly, it's important to note that we use `let` to declare variables in modern JavaScript, as `var` has some peculiarities that can lead to unexpected results. The variable `i` needs to be declared and initialized within the loop.

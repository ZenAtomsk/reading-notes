## HTML Lists, CSS Boxes, JS control Flow

### HTML Lists
- There are 3 types of HTML lists:
    1. ordered
    2. unordered
    3. definition
- ordered lists use numbers.
- unordered lists use bullets.
- definition lists are used to define terminology.
- lists can be nested inside one another.

#### Definition lists

the definition list is created with the ***\<dl>*** element and usually consists of a series of terms and their definitions.

Inside the \<dl> you will usually see pairs of ***\<dt>*** and ***\<dd>*** elements.

***\<dt>*** is used to contain the term being defined (the definition term).

***\<dd>*** is used to contain the definistion.

### CSS Boxes

- CSS treats each HTML element as if it has its own box

- you can use CSS to control the dimensions of a box.

- you can also control the borders, margins and padding for each box with CSS.

- it is possible to hide elements using the display and visibility properties.

- block-level boxes can be made into inline boxes, and inline boxes made into block-level boxes.

- legibility can be improved by controlling the width of boxes containing text and the leading.

- CSS3 has introduced the ability to creat iage borders and rounded borders.

### Basic JavaScript Instructions

- A script is made up of a series of statements. Each statement is like a step in a recipe.

- Scripts contain very precise instructions. for example, you might specify that a value must be remembered before creating a calculation using that value.

- variables are used to temporarily store pieces of information used in the script.

- arrays are special types of variables that store more than one piece of related information

- JavaScript distinguishes between numbers (0-9), strings (text), and Boolean values.

- Expressions evaluate into a single value.

- Expressions rely on operators to calculate a value.

### Decisions and loops

- Switch statements allow you to compare a value against possible outcomes (and also provides a default option if none match).

- data types can be coerced from one type to another

- all values evaluate to either truthy or falsy.

- There are three types of loop (each repeats a set of statements);
    1. for
    2. while
    3. do...while

#### Switch Statements

A switch statement starts with a variable called the switch value. Each case indicates a possible value for this variable and the code that should run if the bariable matches that value.

| IF...ELSE | VS | Switch |
| --- | ---| --- |
| there is no need to provide an else option (you can just use if statement) | | You have a default option that is run if none of the cases match.
| with a series of if statements, they are all checked even if a match has been found (so it performs more slowly than switch) | | if a match is found, that code is run; then the break statement stops the rest of the switch statement running (providing better performance than multiple ***if*** statements).

### Loops

Loops check a condition. if it returns true, a code block will run. Then the condition will be checked again and if it still returns true, the code block will run again. It repeats until the condition returns false. There are three common types of loops
1. For
    - if you need to run code a specific number of times, use a for loop (most common loop).
2. While
    - If you do not know how many times the code should run, you can use a while loop.
3. Do While
    -The do...while loop is very similar to the while loop, but has one key difference: it will always run the statements inside the curly braces at least once, even if the condition evaluates to false.

### Loops Counters

a ***for*** loop uses a counter as a condition This instructs the code to run a specified number of times.

Example:

---

>**for (var i = 0; i < 10; i++) { <br />
>    document.write(i); <br />
> }**

Here the condition is made up of three statements:


1. Initialization
    - Create a variable and set it to 0. This variable is commonly called ***i***, and it acts as the counter
    >var i = 0;
    >

    - the variable is only created the first time the loop is run.
    - you will sometimes see this variable declared before the condition.
        >var i; <br />
        for (i = 0; i < 10; i++) { <br />
            code goes here <br />
        }
        >

2. Condition
    - the loop should continue to run until the counter reaches a specified number
    >i < 10;

    - the value of **i** was initially set to **0**, so in this case the loop will run 10 times before stopping.

    - The condition may also use a variable that holds a number. If a variale called **rounds** held the number of rounds in a test and the loop ran once for each round, the condition would be:
    >var rounds = 3; <br />
    >i < (rounds);

3. Update
    - every time the loop has run the statements in the curly braces, it adds one to the counter.

    >***i++***

    - one is added to the counter using the increment (++) operator
    - another way of reading this is that it says, "take the varialbe i, and add one using the ++ operator."
    - it is also possible for loops to count downwards using the decrement operator (--)

### Key loop concepts

Here are three points to consider when working with loops.

1. Keywords <br />
you will commonly see these two keywords used with loops:
    - Break <br />
    This keyword causes the termination of the loop and tells the interpreter to go onto the next statement of code outside of the loop.
    - continue <br />
    this keyword tells the interpreter to stop the current iteration and then update and check the condition again. (if it is true, the code runs again.)

2. Loops & Arrays <br />
    - loops are very helpful when dealing with arrays if you want to run the same code for each item in the array. you might want to write the value of each item stored in an array into the page.
    - you may not know how many items will be in an array when writing a script, but, when the code runs, it can check the total number of items in a loop. that figure can then be used in the counter to control how many times a set of statements is run.
    - once the loop has run the right number of times, the loop stops.

3. Performance issues
    - it is important to remember that when a browser comes across JavaScript, it will stop doing anything else until it has processed that script.
    - if your loop is dealilng with only a small number of items, this will not be an issue. if, however, your loop contains a lot of items, it can make the page slower to load
    - if the condition never returns fals, you get what is commonly referred to as an **infinite loop**. The code will not stop running until your browser runs out of memory (breaking your script).
    - any variable you can define outside of the loop and that does not change within the loop should be defined outside of it. If it were declared inside the loop, it would be recalculated every time the loop ran, needlessly using resources.
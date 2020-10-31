- [Growth Mindset](https://zenatomsk.github.io/reading-notes/)
- [Learning Markdown](https://zenatomsk.github.io/reading-notes/01-learning-markdown) 
- [The Coder's Computer](https://zenatomsk.github.io/reading-notes/02-the-coders-computer)
- [Terminal revision and the cloud....or the matrix](https://zenatomsk.github.io/reading-notes/03-revisions-and-the-cloud)
- [Html-the structure](https://zenatomsk.github.io/reading-notes/04-structure-with-html)
- [Where do you want it and what color?](https://zenatomsk.github.io/reading-notes/05-design-with-css)
- [Let's make it do stuff and things](https://zenatomsk.github.io/reading-notes/06a-dynamic-with-javascript)
- [Computer architecture and logic](https://zenatomsk.github.io/reading-notes/06b-computer-architecture-and-logic)
- [You need coffee for all this Java..Script](https://zenatomsk.github.io/reading-notes/07-programming-with-js)
- [Answer how I want you to answer, or this loop will never close](https:zenatomsk.github.io/reading-notes/08-operators-and-loops)

## **New Vocabulary**

1. loop - Check a condition. If it returns true, a code block will run. Then the condition will be checked again and if it still returns true, the code block will run again. It repeats until the condition returns false. There are three common loop types

2. while - If you do not know how many times the code should run, you can use a ***while*** loop. Here the condition can be something other than a counter, and the code will continue to loop for as long as the condition is true.

3. for - If you need to run code a specific number of times, use a for loop. (it is the most common loop.) In a for loop, the condition is usally a counter which is used to tell how many times the loop should run

4. condition - the loop should continue to run until the counter reaches a specified number.
    
    >i<10;
    
    - the value of ***i*** was initially set to 0, so in this case the loop will run 10 times before stopping.
    
    - the condition may also use a variable that holds a number. If a variable called **rounds** held the number of rounds in a test and the loop ran once for each round, the condition would be:
        >var rounds = 3

        >**i** < (rounds);

5. increment -  increase by 1
6. decrement - decrease by 1 

## Operators and Loops

Loops check a condition. If it returns true, a code block will run. Then the condition will be checked again and if it still returns true, the code block will run again. It repeats until the condition returns false. There are three common loop types

**== is equal to.** This operator compares two values (numbers, strings, or Booleans) to see if they are the same. ('Hello' == 'Goodbye' returns false because they are not the same string. 'Hello' == 'Hello' returns true because they are the same string.)

**=== Strict equal to.** This operator compares two values to check that both the data type and value are the same. ('3' === 3 is false. '3' === '3' is true)

**!= is not equal to**

**!== strict not equal to**

**> greater than**

**>= greater than or equal to**

**< less than**

**<= less than or equal to**

**&& logical and** This operator tests more than one condition ((2 < 5) && (3 >= 2)) returns *true*. both expressions must be true to result in *true* for the operator.

**|| Logical or** this operator tests at least one condition ((2 < 5) || (2 < 1)) returns true. If either expressions is *true*, the result will be *true* for the operator.

**! Logical not** this operator takes a single Boolean value and inverts it. !(2 < 1) returns true. this reverses the state of an expression. If it was false (without the ! before it) it would return true. If the statement was true, it would return false. !true returns false and !false returns true.
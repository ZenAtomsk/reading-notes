## **JS Debugging**

### Error handling and debugging

- If you understand execution contexts (which have two stages) and stacks, you are more likely to find the error in your code.

- Debugging is the process of finding errors. It involves a process of deduction

- The console helps narrow down the area in which the error is located, so you can try to find the exact error.

- The console helps narrow down the area in which the error is located, so you can try to find the exact error.

- JavaScript has 7 different types of errors. Each creates its own error object, which can tell you its line number and gives a description of the error.

- If you know that you may get an error, you can handle it gracefully using the ***try, catch, finally*** statements. Use them to give your users helpful feedback.

### The Stack

The JavaScript interpreter processes one line of code at a time. When a statement needs data from another function, it **stacks** (or piles) the new function on top of the current task.

When a statement has to call soe other code in order to do its job, the new task goes to the tp of the pile of things to do.

Once the new task has been performed, the interpreter can go back to the task in hand

>&nbsp; &nbsp; &nbsp;  3      <br />
>&nbsp; &nbsp;  2 2 2    <br />
>&nbsp; 1 1 1 1 1  

---

### **TRY, CATCH, FINALLY**

If you know your code might fail, use try, catch, and finally. <br />
Each one is given its own code block.

>***try {***  
> *try to execute this code* <br />
>***} catch (exception) {*** <br />
> *if there is an exception, run this code* <br />
>***} finally { ***<br />
> *this always gets executed* <br />
>***}***

**TRY**
- First, you specify the code that you thin might throw an exception within the try block

- If an exception occurs in this section of code, control is automatically passed to the corresponding catch block.

- The try clause must be used in this type of error handling code, and it should always have either a catch , finally, or both.

- If you use a continue, break, or return keyword inside a try, it will go to the finally option.

**CATCH**
- If the try code block throws an exception, catch steps in with an alternative set of code.

- it has one parameter: the error object. Although it is optional, you are not handling the error if you do not catch an error.

- The ability to catch an error can be very helpful if there is an issue on a live website.

- It lets you tell users that something has gone wrong (rather than not informing them why the site stopped working).

**FINALLY**
- The contents of the finally code block will run either way - whether the try block succeeded or failed.

- It even runs if a return keyword is used in the try or catch block. It is sometimes used to clean up after the previous two clauses.

- These methods are similar to the .done(), .fail(), and .always() methods in jQuery.

- You can nest checks inside each other (place another try inside a catch), but be aware that it can affect performance of a script.
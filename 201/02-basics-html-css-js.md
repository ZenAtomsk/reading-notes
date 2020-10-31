# **Basics of HTML, CSS and JS**
---

## ***Text***
- HTML elements are used to describe the structure of the page (e.g. headings, subheadings, paragraphs).
- They also provide sematic information (e.g. where emphasis should be placed, the definition of any acronyms used, when given text is a quottion).

### Headings

HTML has six "levels" of headings:

***\<h1>*** is used for main headings

***\<h2>*** is used for subheadings

if there are further sections under the subheadings then the ***\<h3>*** element is used, and so on

---

### Paragraphs

***\<p>*** to start

***\</p>*** to end

A browser will show each paragraph on a new line with some space between it and any subsequent paragraphs.

---

### Bold and Italic

***\<b>*** by enclosing words in the \<b> \</b> we can make characters appear bold.

***\<i>*** by enclosing words in the \<i> \</i> we can make characters appear italic.

---

### Superscript & Subscript

the ***\<sup>*** element is used to contain characters that should be superscript such as the suffixes of dates or mathematical concepts like raising a number to a power such as 2<sup>2</sup>.

the ***\<sub>*** element is used to contain characters that should be subscript. It is commonly used with foot notes or chemical formulas such as H<sub>2</sub>O.

---

### White Space

In order to make code easier to read, web page authors often add extra spaces or start some elements on new lines.

When the browser comes across two or more spaces next to each other, it only displays on space. Similarly if it comes across a lin break, it treats that as a single space too. This is known as ***white space collapsing***.

### Line Breaks & Horizontal Rules

***\<br />*** used if you want to add a line break inside the middle <br /> of <br /> a <br /> paragraph.

***\<hr />*** to create a break between themes - such as a change of topic in a book or a new scene in a play - you can add a horizontal rule between sections.

><p>Cartoons are simple</p> 
><hr />
><p>Anime can have very mature themes not intended for children</p>

---

## Semantic Markup

There are some text elements that are not intended to affect the structure of your web pages, but they do add extra information to the pages.

### Strong and Emphasis

***\<strong>*** element indicates that its content has strong importance <strong>Beware!!!</strong>

***\<em>*** element <em>indicates</em> emphasis that <em>subtly</em> changes the <em>meaning</em> of a sentence.

### Quotations

***\<blockquote>*** element is used for longer quotes that take up an entire paragraph. the ***\<p>*** element is still used inside the \<blockquote> element.

***\<q>*** element is used for shorter quotes that sit within a paragraph. Browsers are supposed to put quotes around the \<q> element. However internet explorer does not

### Abbreviations & Acronyms

***\<abbr>*** can be used if you use an <abbr title='abbreviation'>abbr</abbr> or an acronym.

### Citations & Definitions

***\<cite>*** used when referencing a piece of work such as a book, film or research paper

***<dfn>\<dfn></dfn>*** is used the first time you explain some new terminology (academic concept or some jargon) in a document, it is known as the defining instance of it

### Author Details

***\<address>*** has a specific use: to contain contact details for the author of the page
    <address>
        <p><a href="mailto:ricardo.b3788@gmail.com">
            ricardo.b3788@gmail.com</a></p>
        <p>16501 NE 33rd CT YY101, Redmond. </p>
    </address>

### Changes to content

***\<ins> and \<del>*** can be used to show content that has been <ins>inserted</ins> or <del>deleted<del>.

***\<s>*** indicates something that is no longer accurate or relevant (but should not be deleted)

Price:
<p><s>$999</s></p>
<p>now only $998!!!! Can you believe my generosity?!</p>

---

## Introducing CSS

- CSS treats each HTML element as if it appears inside its own box and uses rules to indicate how that element should look.
- rules are made up of selectors (that specify elements the rule applies to) and declarations (that indicate what these elements should look like).
- Different types of selectors allow you to target your rules at different elements.
- Declarations are made up of two parts
    1. the properties of the element that you want to change
    2. the values of those properties.
    > for example, the font-family property sets the choice of font, and the value arial specifies Arial as the preferred typeface.
- CSS rules usually appear in a separate document, although they may appear within an HTML page.

## Basic JavaScript Instructions

- A script is made up of a series of statements. Each statement is like a step in a recipe.

- Scripts contain very precise instructions. for example, you might specify that a value must be remembered before creating a calculation using that value.

- variables are used to temporarily store pieces of information used in the script.

- arrays are special types of variables that store more than one piece of related information

- JavaScript distinguishes between numbers (0-9), strings (text), and Boolean values.

- Expressions evaluate into a single value.

- Expressions rely on operators to calculate a value.


### Rules for naming variables
1. the name must begin with a leter, dollar sign, or an underscore. it must not start with a number.
2. the name can contain letters, numbers, dollar sign, or an underscore. you must not use a dash or a period in a variable name.
3. you cannot use keywords or reserved words. Keywords are special words that tell the interpreter to do something. For example, ***var*** is a keyword used to declare a variable.
4. all variable are case sensitive, so score and Score would be different variable names, but it is bad practice to create two variables that have the same name using different cases.
5. use a name that describes the kind of information that the variable stores.
6. if your vairable name is made up of more than one word, use camelCase.

### Arrays

An array is a special type of variable. It doesn't just store one value; it stores a list of values.

you should consider using an array whenever you are working with a list or a set of values that are related to each other.

arrays are especially helpful when you do not know how many items a list will contain.

#### Creating an array

you creat an array and give it a name just like you would any other variable. The values are assigned to the array inside a pair of square brackets, and each value is separated by a comma. 

The values in the array do not need to be the same data type, so you can store  string, a number and a Boolean all in the same array.

The technique for creating an array is known as an array literal. It is usually the preferred method for creating an array. You can also write each value on a separate line:

>Colors = ['white', <br />
>          'black', <br />
>          'custom']

Values in an array are accessed as if they are in a numbered list. It is important to know that the numbering of this list starts at zero (not one).

Numbering items in an array
- each item in an array is automatically given a number called an index. This can be used to access specific items in the array.

var colors;
colors = ['white', <br />
    'black', <br />
    'custom'];

Confusingly, index values start at 0, so the folowing table shows items from the array and their corresponding index values:

| Index | Value |
--- | --- |
| 0 | 'white' |
| 1 | 'black' |
| 2 | 'custom' |

Accessing items in an array
- to retrieve the third item on the list, the array name is specified along with the index nuber in square brackets.

> var itemThree; <br />
> itemThree = colors[2]

## Decisions and loops

- Conditional statements allow your code to make decisions about what to do next

- Comparison operators are used to compare two operands.

- Logical operators allow you to combine more than one set of comparison operators.

- if..else statements allow you to run one set of code if a condition is true, and another if it is false.
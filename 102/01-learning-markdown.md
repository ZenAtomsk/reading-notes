
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


# These are my reading notes

## Markdown is a lightweight and easy-to-use syntax for styling all forms of writing on the GitHub platform.
- Markdown is a way to style text on the web to control the display of the document; formatting words as bold or italic, adding images, and creating lists.
- Markdown is just regular text with a few non-alphabetic characters thrown in, like # or *

## Examples: 

### Text: It's very easy to make some words **bold** and other words *italic* with Markdown. You can even [link to Google!](http://google.com)

### Lists: Sometimes you want numbered lists:

1. One
2. Two
3. Three

Sometimes you want bullet points:

* Start a line with a star
* Profit!

Alternatively,

- Dashes work just as well
- And if you have sub points, put two spaces before the dash or star:
  - Like this
  - And this
  
Images: If you want to embed images, this is how you do it:
  
  -exclamation symbol[title] followed by the link in parenthases
  
![Image of Yaktocat](image of an awesome cat thing) (this image is broken on purpose, the cat picture was huuuuuge)

### Headers and quotes: # Structured documents

Sometimes it's useful to have different levels of headings to structure your documents. Start lines with a `#` to create headings. Multiple `##` in a row denote smaller heading sizes.

#### This is a fourth-tier heading
##### This is a fifth-tier heading

You can use one `#` all the way up to `######` six for different heading sizes.

If you'd like to quote someone, use the > character before the line:

> Coffee. The finest organic suspension ever devised... I beat the Borg with it.
> - Captain Janeway

## Code: There are many different ways to style code with GitHub's markdown. If you have inline code blocks, wrap them in backticks: ` var example = true `.  If you've got a longer block of code, you can indent with four spaces:

    if (isAwesome){
      return true
    }

GitHub also supports something called code fencing, which allows for multiple lines without indentation:

```
if (isAwesome){
  return true
}
```

And if you'd like to use syntax highlighting, include the language:

```javascript
if (isAwesome){
  return true
}
```

## Extras: GitHub supports many extras in Markdown that help you reference and link to people. If you ever want to direct a comment at someone, you can prefix their name with an @ symbol: Hey @kneath — love your sweater!

But I have to admit, tasks lists are my favorite:

- [x] This is a complete item
- [ ]  This is an incomplete item

When you include a task list in the first comment of an Issue, you will see a helpful progress bar in your list of issues. It works in Pull Requests, too!

And, of course emoji!

## Markdown syntax can be searched in search engines for shortcuts or cheet sheets.

## GitHub.com uses its own version of the Markdown syntax that provides an additional set of useful features, many of which make it easier to work with content on GitHub.com.

## Types of syntax
- headers
- emphasis
- lists (unordered/ordered)
- images
- links
- blockquotes
- inline code

## GitHub uses its own version of Markdown syntax for additional features

1.**Syntax highlighting**
  - you can also indent your code by four spaces

2.**Task Lists**
    - [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
    - [x] list syntax required (any unordered or ordered list supported)
    - [x] this is a complete item
    - [ ] this is an incomplete item
- **if you include a task list in the first comment of an issue, you will get a progress indicator in you issue list**3. 

3.**Tables**
- you can creat tables by assembling a list of words and dividing them with hypens - (for the first row), and then separating each column with a pipe | :

**Year** | **Number of succesfull graduates**
------------ | -------------
1908 | 2
2020 | 200

4.**SHA references** (is a cryptographic hash function which takes an input and produces a 160-bit (20-byte) hash value known as a message digest – typically rendered as a hexadecimal number, 40 digits long)
- any reference to a commit's SHA-1 hash will be automatically converted into a link to that commit on GitHub.

16c999e8c71134401a78d4d46435517b2271d6ac
mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac

5.**Issue references within a repository**
- Any number that refers to an Issue or Pull Request will be automatically converted into a link.

#1
mojombo#1
mojombo/github-flavored-markdown#1

6.**Username @mentions**
- Typing an @ symbol, followed by a username, will notify that person to come and view the comment. This is called an “@mention”, because you’re mentioning the individual. You can also @mention teams within an organization.

7.**Automatic linking for URLs** 
- Any URL (like http://www.github.com/) will be automatically converted into a clickable link.
- you can also use [] to title your link, making it clickable with the link directly after using ()

8.**Strikethrough**
- any word wrapped with two tildes ~~experience~~ will be crossed out
- ~~any word wrapped with two tildes will be crossed out~~

9.**Emoji**
- Github supports emoji.
You can add emoji to your writing by typing :EMOJICODE:.
@octocat :+1: This PR looks great - it's ready to merge! :shipit:



Also great document for more reading https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax#using-emoji
[Awesome Document](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax#using-emoji)

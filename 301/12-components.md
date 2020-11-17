# **COMPONENTS**

- [EJS Partials](https://medium.com/@henslejoseph/ejs-partials-f6f102cb7433)
- [Video-Intro to EJS-Partials](https://www.youtube.com/watch?v=3_xEEH4fTEk&t=0s&index=7&list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt)

## **PARTIALS**

Partials come in handy when you want to reuse the same HTML across multiple views. Think of partials as functions, they make large websites easier to maintain as you don’t have to go and change a piece of text in every page it appears in. Instead, you define that reusable bundle of code in a file and include it wherever you need it.

- in a new "views/partials" file create the partial html
- to include the partial file in another ejs use <%-include(PARTIAL_FILE_NAME)%>
- partials are native to ejs, so easy to put in
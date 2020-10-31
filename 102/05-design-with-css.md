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

## New Vocabulary

- **CSS** *Cascading Style Sheets* - a simple mechanism for adding style (e.g., fonts, colors, spacing) to Web documents.
- **RGB** - Values for red, green, and blue are expressed as numbers between 0 and 255
- **HSL** - *Hue/Saturation/Lightness* - alternative way to specify colors using Hue represented as a color circle where the angle represents the color. Saturation is the amount of gray in a color. Saturation is represented as a percentage. 100%  is full saturation and 0% is a shade of gray. Lightness is the amount of white or black in a color. Lightness is represented as a percentage (Sometimes referred to as *luminosity*).
- **Hex codes** - Hex values represent values for red, green, and blue in hexadecimal code.
- **Layout** - 
- **Rule** - If the two selectors are identical, the latter of the two will take precedence.
- **Declarations** - indicate how the elements referred to in the selector should be styled. Declarations are split into two parts (a property and a value), and are separated by a colon
- **Selector** - indicate which element the rule applies to. The same rule can apply to more than one element if you separate the element names with commas.
- **Property** - indicate the aspects of the element you want to change. For example, color, font, width, height and border. 
- **Values** - specify the settings you want to use for the chosen properties. For example, if you want to specify a color property then the value is the color you want the text in these elements to be
- **Curly braces** - Declaration block

classes have periods .classname
IDs have numbers #idname

# Reading notes

## Summary of Color

- color not only brings your site to life, but aslo helpsconvey the mood and evokes reactions.
- there are three ways to specify colors in S+CSS. RGB values, hex codes, and color names.
- color pickers can help you find the color you want.
- it is important to ensure that there is enough contrast between any text and the background color (otherwise peopls will not be able to read your content).
- CSS3 has introduced an extra value for RGB colors to indicatee opacity. It is known as RGBA.
- CSS3 also allows you to specify colors as HSL values, with an optional opacity value. It is known as HSLA.

### Foreground color

the color porperty allows you to specify the color of text inside an element. you can spicify any color in CSS in on of three ways:
1. **RGB Values** These express colors in terms of how much red, green and blue are used to make it up. For example: rgb(100,100,90)
2. **Hex codes** These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. For exampl: #ee3e80
3. **Color names** There are 147 predefined color names that are recognized by browsers. For example: DarkCyan

*CSS3 has also introduced another way to specify colors called HSLA*

*the use of comments can help you to understand a CSS file (and organise it, by splitting a long document into sections). to make notes use /* (note) */

### Background color

CSS treats each HTML element as if it appears in a box, and the background-color property sets the color of the background for that box. 

You can specify you choice of background color in the same three ways.

If you do not specify a background color, then the background is transparent.

By default, most browser windows have a white background, but users can set a color for their windows.

### Understanding color

Every color on a computer screen is created by mixing amounts of rgb. Use the color picker to choose.

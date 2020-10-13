## **Chart.js, Canvas**

---

### **Charts**

Easily create stunning animated charts
  - Line chart
  - Pie chart
  - Bar chart

Can be used to animate.

---

### **Canvas**

A \<canvas> looks like the \<img> element, with the only clear difference being that it doesn't have the src and alt attributes. 

The \<canvas> element has only two attributes, width and height. These are both optional and can also be set using DOM properties. When no width and height attributes are specified, the canvas will initially be 300 pixels wide and 150 pixels high. The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout size: if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted.

>Note: If your renderings seem distorted, try specifying your width and height attributes explicitly in the \<canvas> attributes, and not using CSS.

The id attribute isn't specific to the \<canvas> element but is one of the global HTML attributes which can be applied to any HTML element (like class for instance). It is always a good idea to supply an id because this makes it much easier to identify it in a script

The \<canvas> element can be styled just like any normal image (margin, border, background…). These rules, however, don't affect the actual drawing on the canvas.

#### **Fallback content**

The \<canvas> element differs from an \<img> tag in that, like for \<video>, \<audio>, or \<picture> elements, it is easy to define some fallback content, to be displayed in older browsers not supporting it, like versions of Internet Explorer earlier than version 9 or textual browsers. You should always provide fallback content to be displayed by those browsers.

Providing fallback content is very straightforward: just insert the alternate content inside the \<canvas> element. Browsers that don't support \<canvas> will ignore the container and render the fallback content inside it. Browsers that do support \<canvas> will ignore the content inside the container, and just render the canvas normally.

>Requires closing \</canvas> tag.

---

### **Drawing Text**

The canvas rendering context provides two methods to render text:

  1. fillText(text, x, y [, maxWidth])
    
      - Fills a given text at the given (x,y) position. Optionally with a maximum   width to draw.
  
  2. strokeText(text, x, y [, maxWidth])
      - Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

#### **Styling Text**

1. font = value 
    - The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.

2. textAlign = value
    - Text alignment setting. Possible values: start, end, left, right or center. The default value is start.

3. textBaseline = value
    - Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.

4. direction = value
    - Directionality. Possible values: ltr, rtl, inherit. The default value is inherit

### **Advanced text measuremets**

measureText()

  - Returns a TextMetrics object containing the width, in pixels, that the specified text will be when drawn in the current text style.

--- 

### **Applying styles and Colors**

#### **Colors**

Up until now we have only seen methods of the drawing context. If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.

1. fillStyle = color
    - Sets the style used when filling shapes.

2. strokeStyle = color
    - Sets the style for shapes' outlines

color is a string representing a CSS <color>, a gradient object, or a pattern object. We'll look at gradient and pattern objects later. By default, the stroke and fill color are set to black

#### **Transparency**

In addition to drawing opaque shapes to the canvas, we can also draw semi-transparent (or translucent) shapes. This is done by either setting the globalAlpha property or by assigning a semi-transparent color to the stroke and/or fill style.

- globalAlpha = transparencyValue
    - Applies the specified transparency value to all future shapes drawn on the canvas. The value must be between 0.0 (fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default.

#### **Line styles**

1. lineWidth = value
    - Sets the width of lines drawn in the future.

2. lineCap = type
    - Sets the appearance of the ends of lines.

3. lineJoin = type
    - Sets the appearance of the "corners" where lines meet.

4. miterLimit = value
    - Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.

5. getLineDash()
    - Returns the current line dash pattern array containing an even number of non-negative numbers.

6. setLineDash(segments)
    - Sets the current line dash pattern.

7. lineDashOffset = value
    - Specifies where to start a dash array on a line.

Gradients, patterns, shadows and Canvas fill also available.
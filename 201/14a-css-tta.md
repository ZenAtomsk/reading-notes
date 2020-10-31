## **CSS Transforms, Transitions, and Animations**

[Transform Everything.](learn.shayhowe.com/advanced-html-css/css-transforms/)

[Animate Everything](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)

### ***Transforms***

The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

#### **Transform Syntax**

The actual syntax for the transform property is quite simple, including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.

    div {
      -webkit-transform: scale(1.5);
        -moz-transform: scale(1.5);
          -o-transform: scale(1.5);
            transform: scale(1.5);
    }

the transform property includes multiple vendor prefixes to gain the best support across all browsers. The un-prefixed declaration comes last to overwrite the prefixed versions, should a browser fully support the transform property.

vendor prefixes are strongly encouraged for any code in a production environment.

#### **2D Transforms**

Two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes.

**2D Rotate**

The rotate value provides the ability to rotate an element from 0 to 360 degrees. Using a positive value will rotate an element clockwise, and using a negative value will rotate the element counterclockwise. The default point of rotation is the center of the element, 50% 50%, both horizontally and vertically.

    HTML:
    1 <figure class="box-1">Box 1</figure>
    2 <figure class="box-2">Box 2</figure>
    3
      
    CSS: 
    1 .box-1 {
    2   transform: rotate(20deg);
    3 }
    4 .box-2 {
    5   transform: rotate(-55deg);
    6 }

**2D Scale**

Using the scale value within the transform property allows you to change the appeared size of an element. The default scale value is 1, therefore any value between .99 and .01 makes an element appear smaller while any value greater than or equal to 1.01 makes an element appear larger.

    HTML:
    1 <figure class="box-1">Box 1</figure>
    2 <figure class="box-2">Box 2</figure>
    3
      
    CSS: 
    1 .box-1 {
    2   transform: scale(.75);
    3 }
    4 .box-2 {
    5   transform: scale(1.25);
    6 }

It is possible to scale only the height or width of an element using the scaleX and scaleY values. The scaleX value will scale the width of an element while the scaleY value will scale the height of an element. To scale both the height and width of an element but at different sizes, the x and y axis values may be set simultaneously. To do so, use the scale transform declaring the x axis value first, followed by a comma, and then the y axis value.

    HTML:
    1 <figure class="box-1">Box 1</figure>
    2 <figure class="box-2">Box 2</figure>
    3 <figure class="box-3">Box 3</figure>
      
    CSS: 
    1 .box-1 {
    2   transform: scaleX(.5);
    3 }
    4 .box-2 {
    5   transform: scaleY(1.15);
    6 }
    7 .box-3 {
    8   transform: scale(.5, 1.15);
    9 }

**2D Translate**

The translate value works a bit like that of relative positioning, pushing and pulling an element in different directions without interrupting the normal flow of the document. Using the translateX value will change the position of an element on the horizontal axis while using the translateY value will change the position of an element on the vertical axis.

As with the scale value, to set both the x and y axis values at once, use the translate value and declare the x axis value first, followed by a comma, and then the y axis value.

The distance values used within the translate value may be any general length measurement, most commonly pixels or percentages. Positive values will push an element down and to the right of its default position while negative values will pull an element up and to the left of its default position.

    HTML:
    1 <figure class="box-1">Box 1</figure>
    2 <figure class="box-2">Box 2</figure>
    3 <figure class="box-3">Box 3</figure>
      
    CSS: 
    1 .box-1 {
    2   transform: translateX(-10px);
    3 }
    4 .box-2 {
    5   transform: translateY(25%);
    6 }
    7 .box-3 {
    8   transform: translate(-10px, 25%);
    9 }    

**2D Skew**

The last transform value in the group, skew, is used to distort elements on the horizontal axis, vertical axis, or both. The syntax is very similar to that of the scale and translate values. Using the skewX value distorts an element on the horizontal axis while the skewY value distorts an element on the vertical axis. To distort an element on both axes the skew value is used, declaring the x axis value first, followed by a comma, and then the y axis value.%p

The distance calculation of the skew value is measured in units of degrees. Length measurements, such as pixels or percentages, do not apply here.

    HTML:
    1 <figure class="box-1">Box 1</figure>
    2 <figure class="box-2">Box 2</figure>
    3 <figure class="box-3">Box 3</figure>
      
    CSS: 
    1 .box-1 {
    2   transform: skewX(5deg);
    3 }
    4 .box-2 {
    5   transform: skewY(-20deg);
    6 }
    7 .box-3 {
    8   transform: skew(5deg, -20deg);
    9 }  

**Combining Transforms**

It is common for multiple transforms to be used at once, rotating and scaling the size of an element at the same time for example. In this event multiple transforms can be combined together. To combine transforms, list the transform values within the transform property one after the other without the use of commas.

Using multiple transform declarations will not work, as each declaration will overwrite the one above it. The behavior in that case would be the same as if you were to set the height of an element numerous times.

A lot more. [Transform Everything.](learn.shayhowe.com/advanced-html-css/css-transforms/)

---

### **Transitions & Animations**

One evolution with CSS3 was the ability to write behaviors for transitions and animations. Front end developers have been asking for the ability to design these interactions within HTML and CSS, without the use of JavaScript or Flash, for years. Now their wish has come true.

With CSS3 transitions you have the potential to alter the appearance and behavior of an element whenever a state change occurs, such as when it is hovered over, focused on, active, or targeted.

Animations within CSS3 allow the appearance and behavior of an element to be altered in multiple keyframes. Transitions provide a change from one state to another, while animations can set multiple points of transition upon different keyframes.

#### **Transitions**

For a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target pseudo-classes.

There are four transition related properties in total, including transition-property, transition-duration, transition-timing-function, and transition-delay.

Declaring every transition property individually can become quite intensive, especially with vendor prefixes. Fortunately there is a shorthand property, transition, capable of supporting all of these different properties and values. Using the transition value alone, you can set every transition value in the order of transition-property, transition-duration, transition-timing-function, and lastly transition-delay. Do not use commas with these values unless you are identifying numerous transitions.

To set numerous transitions at once, set each individual group of transition values, then use a comma to separate each additional group of transition values.

    1 .box {
    2   background: #2db34a;
    3   border-radius: 6px;
    4  transition: background .2s linear, border-radius 1s ease-in 1s;
    5 }
    6 .box:hover {
    7   color: #ff7b29;
    8   border-radius: 50%;
    9 }
    10

  --- 

  ### Animations

Transitions do a great job of building out visual interactions from one state to another, and are perfect for these kinds of single state changes. However, when more control is required, transitions need to have multiple states. In return, this is where animations pick up where transitions leave off.


[Animate Everything](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)
  
---




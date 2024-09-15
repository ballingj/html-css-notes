METADATA
Language:: CSS
Sub-concepts:: Improved Styling with CSS

Summary:: The CSS _box model_ is a box that wraps around an HTML element and controls the design and layout.  We control the spacing of elements by adjusting the content's height, width, margin, border & padding.


---

![[Box-model.png]]
> The CSS _box model_ is a box that wraps around an HTML element and controls the design and layout. 

### The properties of Box-model: width, height, padding, _border_, and _margin_. 

1. `width` and `height`: The width and height of the content area.
2. `padding`: The amount of space between the content area and the border.
3. `border`: The thickness and style of the border surrounding the content area and padding.
4. `margin`: The amount of space between the border and the outside edge of the element.

### 1/ Height and Width

An element’s content has two dimensions: a height and a width. By default, the dimensions of an HTML box are set to hold the raw contents of the box.

The CSS `height` and `width` properties can be used to modify these default dimensions.

```css
p {  height: 80px;  width: 240px;}
```

### 2/ Padding

The space between the contents of a box and the borders of a box is known as _padding_. Padding is like the space between a picture and the frame surrounding it. In CSS, you can modify this space with the `padding` property.

```css
p.content-header {
	border: 3px solid coral;
	padding: 10px;
}
```

If you want to be more specific about the amount of padding on each side of a box’s content, you can use the following properties:

- `padding-top`
- `padding-right`
- `padding-bottom`
- `padding-left`

Each property affects the padding on only one side of the box’s content, giving you more flexibility in customization.  You can specify these properties in a few different ways:
###### 4 Values
In the example above, the four values `6px 11px 4px 9px` correspond to the amount of padding on each side, in a clockwise rotation. In order, it specifies the padding-top value (`6px`), the padding-right value (`11px`), the padding-bottom value (`4px`), and the padding-left value (`9px`) of the content.
```css
p.content-header {
	padding: 6px 11px 4px 9px;
}
```

###### 3 Values
If the left and right sides of the content can be equal, the padding shorthand property allows for 3 values to be specified. The first value sets the padding-top value (`5px`), the second value sets the padding-left and padding-right values (`10px`), and the third value sets the padding-bottom value (`20px`).
```css
p.content-header {
	padding: 5px 10px 20px;
}
```

###### 2 Values
And finally, if the top and bottom sides can be equal, and the left and right sides can be equal, you can specify 2 values. The first value sets the padding-top and padding-bottom values (`5px`), and the second value sets the padding-left and padding-right values (`10px`).
```css
p.content-header {
	padding: 5px 10px;
}
```

And finally, if the top and bottom sides can be equal, and the left and right sides can be equal, you can specify 2 values. The first value sets the padding-top and padding-bottom values (`5px`), and the second value sets the padding-left and padding-right values (`10px`).

### 3/ Borders

A _border_ is a line that surrounds an element, like a frame around a painting. Borders can be set with a specific `width`, `style`, and `color`:

- `width`—The thickness of the border. A border’s thickness can be set in pixels or with one of the following keywords: `thin`, `medium`, or `thick`.
- `style`—The design of the border. Web browsers can render any of [10 different styles](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style#Values). Some of these styles include: `none`, `dotted`, and `solid`.
- `color`—The color of the border. Web browsers can render colors using a few different formats, including [140 built-in color keywords](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value).

```css
p {
border: 3px solid coral;
}
```

##### Border Radius

Ever since we revealed the borders of boxes, you may have noticed that the borders highlight the true shape of an element’s box: square. Thanks to CSS, a border doesn’t have to be square.

You can modify the corners of an element’s border box with the `border-radius` property.

```css
div.container {
	border: 3px solid blue;
	border-radius: 5px;
}
```

You can create a border that is a perfect circle by first creating an element with the same width and height, and then setting the radius equal to half the width of the box, which is 50%.

```css
div.container {
	height: 60px;
	width: 60px;
	border: 3px solid blue;
	border-radius: 50%;
}
```

### 4/ Margins

Margin refers to the space directly outside of the box. The `margin` property is used to specify the size of this space.
```css
p {  border: 1px solid aquamarine;  margin: 20px;}
```
If you want to be even more specific about the amount of margin on each side of a box, you can use the following properties:

- `margin-top`
- `margin-right`
- `margin-bottom`
- `margin-left`

Each property affects the margin on only one side of the box, providing more flexibility in customization.

```css
p { 
	border: 3px solid DarkSlateGrey;
	margin-right: 15px;}
```

Similar to padding shorthand, _margin shorthand_ lets you specify all of the `margin` properties as values on a single line: you can specify these properties in a few different ways:

###### 4 Values
In the example below, the four values `6px 10px 5px 12px` correspond to the thickness of the margin on each side, in a clockwise rotation. In order, it specifies the margin-top value (`6px`), the margin-right value (`10px`), the margin-bottom value (`5px`), and the margin-left value (`12px`) of the content.
```css
p {  
	margin: 6px 10px 5px 12px;
}
```

###### 3 Values
If the left and right sides of the content can be equal, the margin shorthand property allows for 3 values to be specified. The first value sets the margin-top value (`5px`), the second value sets the margin-left and margin-right values (`12px`), and the third value sets the margin-bottom value (`4px`).
```css
p {  margin: 5px 12px 4px;}
```

###### 2 Values
And finally, if the top and bottom sides can be equal, and the left and right sides can be equal, you can specify 2 values. The first value sets the margin-top and margin-bottom values (`20px`), and the second value sets the margin-left and margin-right values (`10px`).
```css
p {  margin: 20px 10px;}
```


## The property `box-sizing` of CSS _box model

In CSS, the `box-sizing` property controls the type of box model the browser should use when interpreting a web page.  The default value of this property is `content-box`. This is the same box model that is affected by border thickness and padding.

- The property `box-sizing` controls which aspect of the box is determined by the `height` and `width` properties. 
- The default value of this property is `content-box`, which renders the actual size of the element including the content box; but not the paddings and borders.

### `box-sizing: content-box;`
![[content-box.png]]


The value `border-box` of the `box-sizing` property for an element corresponds directly to the element’s total rendered size, including padding and border with the `height` and `width` properties.

The default value of the `box-sizing` property is `content-box`. The value `border-box` is recommended when it is necessary to resize the `padding` and `border` but not just the content. For instance, the value `border-box` calculates an element’s `height` as follows: `height = content height + padding + border`.
```css
#box-example {
  box-sizing: border-box;
}
```
### `box-sizing: border-box`
![[border-box.png]]


### CSS Margin Collapse

CSS _margin collapse_ occurs when the top and bottom margins of blocks are combined into a single margin equal to the largest individual block margin.

Margin collapse only occurs with vertical margins, not for horizontal margins.
```css
/* The vertical margins will collapse to 30 pixels
instead of adding to 50 pixels. */

.block-one {
  margin: 20px;
}

.block-two {
  margin: 30px;
}
```

### CSS `auto` keyword

The value `auto` can be used with the property `margin` to horizontally center an element within its container. The `margin` property will take the width of the element and will split the rest of the space equally between the left and right margins.
```css
div {
  margin: auto;
}
```

### Dealing with `overflow`

If content is too large for its container, the CSS `overflow` property will determine how the browser handles the problem.

By default, it will be set to `visible` and the content will take up extra space. It can also be set to `hidden`, or to `scroll`, which will make the overflowing content accessible via scroll bars within the original container.
```css
small-block {
  overflow: scroll;
}
```

### Height and Width Maximums/Minimums

The CSS `min-width` and `min-height` properties can be used to set a minimum width and minimum height of an element’s box. CSS `max-width` and `max-height` properties can be used to set maximum widths and heights for element boxes.
```css
/* Any element with class "column" will be at most 200 pixels wide, despite the width property value of 500 pixels. */
.column {
  max-width: 200px;
  width: 500px;
}
```

### The `visibility` Property

The CSS `visibility` property is used to render `hidden` objects invisible to the user, without removing them from the page. This ensures that the page structure and organization remain unchanged.
```css
.invisible-elements {
  visibility: hidden;
}
```


## Key Concepts:

- The box model comprises a set of properties used to create space around and between HTML elements.
- The height and width of a content area can be set in pixels or percentages.
- Borders surround the content area and padding of an element. The color, style, and thickness of a border can be set with CSS properties.
- Padding is the space between the content area and the border. It can be set in pixels or percent.
- Margin is the amount of spacing outside of an element’s border.
- Horizontal margins add, so the total space between the borders of adjacent elements is equal to the sum of the right margin of one element and the left margin of the adjacent element.
- Vertical margins collapse, so the space between vertically adjacent elements is equal to the larger margin.
- `margin: 0 auto` horizontally centers an element inside of its parent content area, if it has a width.
- The `overflow` property can be set to `display`, `hidden`, or `scroll`, and dictates how HTML will render content that overflows its parent’s content area.
- The `visibility` property can hide or show elements.
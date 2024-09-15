METADATA
Language:: CSS
Sub-concepts:: Improved Styling with CSS

Summary:: control the positioning of elements on a web page.


---
# Display and Position

five properties for adjusting the position of HTML elements in the browser:

- `position`
- `display`
- `z-index`
- `float`
- `clear`

## Position
Positioning in CSS provides designers and developers options for positioning HTML elements on a web page. The CSS `position` can be set to `static`, `relative`, `absolute` or `fixed`.   The default position of an element can be changed by setting its `position` property.  The `position` property can also take a fifth value:

- `static` - the default value (it does not need to be specified)
- `relative`
- `absolute`
- `fixed`
- `sticky`

### CSS `position: relative`

One way to modify the default position of an element is by setting its `position` property to `relative`.

This value allows you to position an element _relative_ to its default static position on the web page.

```css
.green-box {
	background-color: green;
	position: relative;
}
```

Although the code in the example above instructs the browser to expect a relative positioning of the `.green-box` element, it does not specify where the `.green-box` element should be positioned on the page. This is done by accompanying the `position` declaration with one or more of the following _offset properties_ that will move the element away from its default static position:

- `top` - moves the element down from the top.
- `bottom` - moves the element up from the bottom.
- `left` - moves the element away from the left side (to the right).
- `right` - moves the element away from the right side (to the left).

You can specify values in pixels, ems, or percentages, among others, to dial in exactly how far you need the element to move. It’s also important to note that offset properties will not work if the element’s `position` property is the default `static`.

```css
.green-box {
	background-color: green;
	position: relative;
	top: 50px;
	left: 120px;
}
```

In the example above, the element of `green-box` class will be moved down 50 pixels, and to the right 120 pixels, from its default static position.  Offsetting the relative element will not affect the positioning of other elements.

### CSS `position: absolute`

The value `absolute` for the CSS property `position` enables an element to ignore sibling elements and instead be positioned relative to its closest parent element that is positioned with `relative` or `absolute`. The `absolute` value removes an element entirely from the document flow. By using the positioning attributes `top`, `left`, `bottom` and `right`, an element can be positioned anywhere as expected.
```css
.element {
  position: absolute;
}
```

### CSS `position: fixed` 

When the CSS position has a value of `fixed`, it is set/pinned to a specific spot on a page. The fixed element stays the same regardless of scrolling. The navigation bar is a great example of an element that is often set to `position: fixed;`, enabling the user to scroll through the web page and still access the navigation bar.
```css
#navbar {
  position: fixed;
}
```
We can _fix_ an element to a specific position on the page (regardless of user scrolling) by setting its position to `fixed`, and accompanying it with the familiar offset properties `top`, `bottom`, `left`, and `right`.
```css
#navbar {
	position: fixed;
	top: 0px;
	left: 0px;
}
```

### CSS `position: sticky` 
The `sticky` value is another position value that keeps an element in the document flow as the user scrolls, but _sticks_ to a specified position as the page is scrolled further. This is done by using the `sticky` value along with the familiar offset properties, as well as one new one.

```css
.box-bottom {
	background-color: darkgreen;
	position: sticky;
	top: 240px;}
```
In the example above, the `.box-bottom` will remain in its relative position, and scroll as usual. When it reaches 240 pixels from the top, it will stick to that position until it reaches the bottom of its parent container where it will “unstick” and rejoin the flow of the document.

## CSS `z-index` property

The CSS `z-index` property specifies how far back or how far forward an element will appear on a web page when it overlaps other elements.

The `z-index` property uses integer values, which can be positive or negative values. The element with the highest `z-index` value will be at the foreground, while the element with the lowest `z-index` value will be at the back.
```css
/*`element1` will overlap `element2`*/

.element1 {
  position: absolute;
  z-index: 1;
}

.element2 {
  position: absolute;
  z-index: -1;
}
```


## CSS `display` property

The CSS `display` property determines the type of render block for an element. The most common values for this property are `block`, `inline`, and `inline-block`.
#### _Block_
take up the full width of their container with line breaks before and after, and can have their height and width manually adjusted.
### _Inline_
take up as little space as possible, flow horizontally, and cannot have their width or height manually adjusted.
### _Inline-block_ 
can appear next to each other, and can have their width and height manually adjusted.

```css
.container1 {
  display: block;
}

.container2 {
  display: inline;
}

.container3 {
  display: inline-block;
}
```


### CSS `float` property

The CSS `float` property determines how far left or how far right an element should float within its parent element. The value `left` floats an element to the left side of its container and the value `right` floats an element to the right side of its container. 
>For the property `float`, the `width` of the container or the `width` of the floated element must be specified; otherwise, the floated element will assume the full width of its containing element.
```css
/*The width of the container must be specified*/
.container {
	width: 400px;
}
/* The content will float to the left side of the container. */
.left-box {
	width: 100px;
	float: left;
}

/* The content will float to the right side of the container. */
.right-box {
	width: 100px;
	float: right;
}
```

### The CSS `clear` property

The CSS `clear` property specifies how an element should behave when it bumps into another element within the same containing element. The `clear` is usually used in combination with elements having the CSS `float` property. This determines on which sides floating elements are allowed to float.
```css
/*This determines that no other elements within the same containing element are allowed to float on the left side of this element.*/

.element {
  clear: left;
}

/*This determines that no other elements within the same containing element are allowed to float on the right side of this element.*/
.element {
  clear: right;
}

/*This determines that no elements within the same containing element are allowed to float on either side of this element.*/
.element {
  clear: both;
}

/*This determines that other elements within the same containing element are allowed to float on both side of this element.*/

.element {
  clear: none;
}
```

### Key Concepts

- The `position` property allows you to specify the position of an element.
- When set to `relative`, an element’s position is relative to its default position on the page.
- When set to `absolute`, an element’s position is relative to its closest positioned parent element. It can be pinned to any part of the web page, but the element will still move with the rest of the document when the page is scrolled.
- When set to `fixed`, an element’s position can be pinned to any part of the web page. The element will remain in view no matter what.
- When set to `sticky`, an element can stick to a defined offset position when the user scrolls its parent container.
- The `z-index` of an element specifies how far back or how far forward an element appears on the page when it overlaps other elements.
- The `display` property allows you to control how an element flows vertically and horizontally in a document.
- `inline` elements take up as little space as possible, and they cannot have manually adjusted `width` or `height`.
- `block` elements take up the width of their container and can have manually adjusted `height`s.
- `inline-block` elements can have set `width` and `height`, but they can also appear next to each other and do not take up their entire container width.
- The `float` property can move elements as far left or as far right as possible on a web page.
- You can clear an element’s left or right side (or both) using the `clear` property.

When combined with an understanding of the box model, positioning can create visually appealing web pages. So far, we’ve focused on adding content in the form of text to a web page. 

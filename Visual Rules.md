METADATA
Language:: CSS
Sub-concepts:: Improved Styling with CSS

Summary:: CSS-declarations, font-size, color, background-color, 

---
# Visual Rules

### CSS declarations

In CSS, a _declaration_ is the key-value pair of a CSS property and its value. CSS declarations are used to set style properties and construct rules to apply to individual or groups of elements. The property name and value are separated by a colon, and the entire declaration must be terminated by a semi-colon.

```css
/* 
CSS declaration format:
property-name: value;
*/

/* CSS declarations */
text-align: center;
color: purple;
width: 100px;
```

### Font Size

The `font-size` CSS property is used to set text sizes. Font size values can be many different units or types such as pixels.
```css
font-size: 30px;
```

### Background Color

The `background-color` CSS property controls the background color of elements.
```css
background-color: blue;
```

### `!important` Rule

The CSS `!important` rule is used on declarations to override any other declarations for a property and ignore selector specificity. `!important` rules will ensure that a specific declaration always applies to the matched elements. However, generally it is good to avoid using `!important` as bad practice.
```css
#column-one {
  width: 200px !important;
}

.post-title {
  color: blue !important;
}
```

### Opacity

The `opacity` CSS property can be used to control the transparency of an element. The value of this property ranges from `0` (transparent) to `1` (opaque).
```css
opacity: 0.5;
```

### Font Weight

The `font-weight` CSS property can be used to set the weight (boldness) of text. The provided value can be a keyword such as `bold` or `normal`.
```css
font-weight: bold;
```

### Text Align

The `text-align` CSS property can be used to set the text alignment of inline contents. This property can be set to these values: `left`, `right`, or `center`.
```css
text-align: right;
```

### CSS Rule Sets

A CSS rule set contains one or more selectors and one or more declarations. The selector(s), which in this example is `h1`, points to an HTML element. The declaration(s), which in this example are `color: blue` and `text-align: center` style the element with a property and value. The rule set is the main building block of a CSS sheet.
```css
h1 {
  color: blue;
  text-align: center;
}
```

### Setting foreground text color in CSS

Using the `color` property, foreground text color of an element can be set in CSS. The value can be a valid color name supported in CSS like `green` or `blue`. Also, 3 digit or 6 digit color code like `#22f` or `#2a2aff` can be used to set the color.
```css
p {
  color : #2a2aff ;
}

span {
  color : green ;
}
```

### Resource URLs

In CSS, the `url()` function is used to wrap resource URLs. These can be applied to several properties such as the `background-image`.
```css
background-image: url("../resources/image.png");
```

### Background Image

The `background-image` CSS property sets the background image of an element. An image URL should be provided in the syntax `url("moon.jpg")` as the value of the property.
```css
background-image: url("nyan-cat.gif");
```

### Font Family

The `font-family` CSS property is used to specify the typeface in a rule set. Fonts must be available to the browser to display correctly, either on the computer or linked as a web font. If a font value is not available, browsers will display their default font. When using a multi-word font name, it is best practice to wrap them in quotes.
```css
h2 {
  font-family: Verdana;
}

#page-title {
  font-family: "Courier New";
}
```

### Color Name Keywords

Color name keywords can be used to set color property values for elements in CSS.
```css
h1 {
  color: aqua;
}

li {
  color: khaki;
}
```

### Key Concepts

- The `font-family` property defines the typeface of an element.
- `font-size` controls the size of text displayed.
- `font-weight` defines how thin or thick text is displayed.
- The `text-align` property places text in the left, right, or center of its parent container.
- Text can have two different color attributes: `color` and `background-color`. `color` defines the color of the text, while `background-color` defines the color behind the text.
- CSS can make an element transparent with the `opacity` property.
- CSS can also set the background of an element to an image with the `background-image` property.
- The `!important` flag will override any style, however it should almost never be used, as it is extremely difficult to override.
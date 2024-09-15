METADATA
Language:: CSS
Sub-concepts:: Improved Styling with CSS

Summary:: The Art of arranging text on web pages


---
# Typography

_typography_ is the art of arranging text on a page.
- How to style and transform fonts.
- How to lay text out on a page.
- and how to add external fonts to your web pages.

### CSS `font-family` Property
You may remember from the [[Visual Rules]] notes that the font of an element can be changed using the `font-family` property.

```css
h1 { 
	font-family: Arial;
}
```
##### Fallback Fonts and Font Stacks

Web safe fonts are good _fallback fonts_ that can be used if your preferred font is not available.

```css
h1 {
	font-family: Caslon, Georgia, 'Times New Roman', serif;
}
```
> `serif` and `sans-serif` are also keyword values that can be added as a final fallback font if nothing else in the font stack is available.
##### Serif and Sans-Serif
![[serif-sans-serif.png]]

### CSS `font-weight` Property
The CSS `font-weight` property declares how thick or thin should be the characters of a text. 

The `font-weight` property can take any one of these keyword values:
- `bold`: Bold font weight.
- `normal`: Normal font weight. This is the default value.
- `lighter`: One font weight lighter than the element’s parent value.
- `bolder`: One font weight bolder than the element’s parent value

Numerical values can be used with this property to set the thickness of the text. The ==numeric scale range of this property is from 100 to 900 and accepts only multiples of 100==. The default value is `normal` while the default numerical value is `400`. Any value less than `400` will have text appear lighter than the default while any numerical value greater than the `400` will appear bolder.

In the given example, all the `<p>` elements will appear in a bolder font.
```css
/* Sets the text as bolder. */
.left-section { 
	font-weight: 700;
}

.right-section {
	font-weight: bold;
}
```

### CSS `font-style` property

The CSS `font-style` property determines the font style in which text will appear.

It accepts `italic` as a value to set the font style to italic.
```css
.text {
  font-style: italic;
}
```

### CSS `text-transform` property

Text can also be styled to appear in either all uppercase or lowercase with the `text-transform` property.

```css
h1 {
	text-transform: uppercase;
}
```

### Text Layout

You’ve learned how text can be defined by font family, weight, style, and transformations. Now you’ll learn about some ways text can be displayed or laid out within the element’s container.

##### Letter Spacing

The `letter-spacing` property is used to set the horizontal spacing between the individual characters in an element. It’s not common to set the spacing between letters, but it can sometimes help the readability of certain fonts or styles. The `letter-spacing` property takes length values in units, such as `2px` or `0.5em`.

```css
p {  letter-spacing: 2px;}
```
> In the example above, each character in the paragraph element will be separated by 2 pixels.


##### Word Spacing

You can set the space between words with the `word-spacing` property. It’s also not common to increase the spacing between words, but it may help enhance the readability of bolded or enlarged text. The `word-spacing` property also takes length values in units, such as `3px` or `0.2em`.

```css
h1 {
	word-spacing: 0.3em;
}
```
> In the example above, the word spacing is set to `0.3em`. For word spacing, using `em` values are recommended because the spacing can be set based on the size of the font.

### The CSS `line-height` property

The CSS `line-height` property declares the vertical spacing between lines of text. It accepts both unitless numbers as a ratio (eg. `2`) and numbers specified by unit as values (eg. `12px`) but it does not accept negative numbers. A unitless number is an absolute value that will compute the line height as a ratio to the font size and a unit number can be any valid CSS unit (eg. pixels, percents, ems, rems, etc.). To set the `line-height` of the `<p>` elements to `10px`, the given CSS declaration can be used.
```css
p {
	/* line-height: 10px; */  
	line-height: 1.4;
}
```
> Generally, the unitless value such as `1.4` is preferred since it is responsive based on the current font size. In other words, if the `line-height` is specified by a unitless number, changing the font size will automatically readjust the line height.

##### Text Alignment

The `text-align` property, which you may already be familiar with from the [[Visual Rules]], aligns text to its parent element.

```css
h1 {
	text-align: right;
}
```

### CSS _@font-face_ rule

The CSS _@font-face_ rule allows external fonts or font files to be imported directly into stylesheets.  The location of the font file must be specified in the CSS rule so that the files can be loaded from that location. This rule also allows locally hosted fonts to be added using a relative file path instead of a web URL.
```css
@font-face {
  font-family: 'Glegoo';
  src: url('../fonts/Glegoo-Regular.ttf') format('truetype');
}
```

#### multiple font-faces
```css
@font-face {
	font-family: 'MyParagraphFont';
	src: url('fonts/Roboto.woff2') format('woff2'),
	     url('fonts/Roboto.woff') format('woff'),
	     url('fonts/Roboto.ttf') format('truetype');
}
```

### CSS _Linking fonts_

_Linking fonts_ allow user to use web fonts in the document. They can be imported in an HTML document by using the `<link>` tag. Once the web font URL is placed within the `href` attribute, the imported font can then be used in CSS declaration.
```html
<head>
  <link href="https://fonts.googleapis.com/css?family=Droid%20Serif" rel="stylesheet">
</head>
```

## Key Concepts:
- _Typography_ is the art of arranging text on a page.
- Text can appear bold or thin with the `font-weight` property.
- Text can appear in italics with the `font-style` property.
- The vertical spacing between lines of text can be modified with the `line-height` property.
- _Serif_ fonts have extra details on the ends of each letter. _Sans-Serif_ fonts do not.
- _Fallback fonts_ are used when a certain font is not installed on a user’s computer.
- The `word-spacing` property changes how far apart individual words are.
- The `letter-spacing` property changes how far apart individual letters are.
- The `text-align` property changes the horizontal alignment of text.
- Google Fonts provides free fonts that can be used in an HTML file with the `<link>` tag or the `@font-face` property.
- Local fonts can be added to a document with the `@font-face` property and the path to the font’s source.
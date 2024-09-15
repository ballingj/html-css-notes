METADATA
Language:: CSS
Sub-concepts:: Improved Styling with CSS

Summary:: Setting the foreground and background colors in CSS


---
# CSS Colors
Colors in CSS can be described in three different ways:

- _Named colors_ — English words that describe colors, also called _keyword colors_
- _RGB_ — numeric values that describe a mix of red, green, and blue
- _HSL_ — numeric values that describe a mix of hue, saturation, and lightness

Color can affect the following design aspects:
- `color` - this property styles an element’s foreground color.
- `background-color` - this property styles an element’s background color.

```css
h1 {
	color: red;
	background-color: blue;}
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
>There are more than 140 named colors, which you can review [here on MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/named-color).

### CSS Hexadecimal Colors

CSS colors can be represented in _hexadecimal_ (or _hex_) notation. Hexadecimal digits can represent sixteen different values using `0`-`9` and `a`-`f`.

Hexadecimal colors are composed of 6 characters–each group of two represents a value between 0 and 255 for red, green, or blue. For example `#ff0000` is all red, no green, and no blue.

When both characters of all three colors are repeated, hex colors can be abbreviated to only three values, so `#0000ff` could also be represented as `#00f`.
```css
.red {
  color: #ff0000;
}

.short-blue {
  color: #00f;
}
```
[Here](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value) is a list of many different colors and their hex values.
 declared with the _HSL_ color system using `hsl()` syntax. This syntax contains three values: _hue_ (the color value itself), _saturation_ (intensity), and _lightness_.

Hue values range from 0 to 360 while saturation and lightness values are represented as percentages.
```css
.light-blue {
  background-color: hsl(200, 70%, 50%);
}
```

### CSS rgb() Colors

CSS colors can be declared with _RGB colors_ using `rgb()` syntax.

`rgb()` should be supplied with three values representing red, green, and blue. These values range can from 0 to 255.
```css
.hot-pink {
  color: rgb(249, 2, 171);
}

.green {
  color: rgb(0, 255, 0);
}
```


### CSS HSL Colors

CSS colors can be declared with the _HSL_ color system using `hsl()` syntax. This syntax contains three values: _hue_ (the color value itself), _saturation_ (intensity), and _lightness_.

Hue values range from 0 to 360 while saturation and lightness values are represented as percentages.
```css
.light-blue {
  background-color: hsl(200, 70%, 50%);
}
```

_Hue_ is the first number. It refers to an angle on a color wheel. Red is 0 degrees, Green is 120 degrees, Blue is 240 degrees, and then back to Red at 360. You can see an example of a color wheel below.
![[hsl-wheel.png]]
_Saturation_ refers to the intensity or purity of the color. The saturation increases towards 100% as the color becomes richer. The saturation decreases towards 0% as the color becomes grayer.

_Lightness_ refers to how light or dark the color is. Halfway, or 50%, is normal lightness. Imagine a sliding dimmer on a light switch that starts halfway. Sliding the dimmer up towards 100% makes the color lighter, closer to white. Sliding the dimmer down towards 0% makes the color darker, closer to black.
### CSS Color Alpha Values

_Alpha values_ determine the transparency of colors in CSS. Alpha values can be set for both RGB and HSL colors by using `rgba()` and `hsla()` and providing a fourth value representing alpha. Alpha values can range between `0.0` (totally transparent) and `1.0` (totally opaque).

The CSS `transparent` value can also be used to create a fully transparent element.
```css
.midground {
  background-color: rgba(0, 255, 0, 0.5);
}

.foreground {
  background-color: hsla(34, 100%, 50%, 0.1);
}

.transparent {
  color: transparent;
}
```

### Key Concepts:
There are four ways to represent color in CSS:

- Named colors—there are more than 140 named colors, which you can review [here on MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/named-color).
- Hexadecimal or hex colors
    - Hexadecimal is a number system that has sixteen digits, 0 to 9 followed by “A” to “F”.
    - Hex values always begin with `#` and specify values of red, blue, and green using hexadecimal numbers such as `#23F41A`.
    - Six-digit hex values with duplicate values for each RGB value can be shorted to three digits.
- RGB
    - RGB colors use the `rgb()` syntax with one value for red, one value for blue and one value for green.
    - RGB values range from 0 to 255 and look like this: `rgb(7, 210, 50)`.
- HSL
    - HSL stands for hue (the color itself), saturation (the intensity of the color), and lightness (how light or dark a color is).
    - Hue ranges from 0 to 360 and saturation and lightness are both represented as percentages like this: `hsl(200, 20%, 50%)`.
- You can add opacity to color in RGB and HSL by adding a fourth value, `a`, which is represented as a percentage.


METADATA
Language:: Design
Sub-concepts:: Web Design Colors

Summary:: Learn about Color Theory


---
# Color Theory

```css
p {  color: hsla(34, 100%, 50%, 0.1); /* HSLA*/}
```

When thinking like a designer, HSLA is the preferred syntax for setting colors. Why?

- The CSS color keywords only give us a few options.
- Hex Codes and RGB values cannot be intuitively adjusted. For example, you get feedback on your design that one color needs to be a little brighter, that does not translate to intuitive changes within Hexadecimal codes or RGB values.
- HSLA is the most semantic system of setting colors with CSS.

Let’s review what each value means:

- The “pure” color is set with the Hue. This is expressed as the angle in degrees around the color wheel.
- Saturation refers to the intensity or purity of that hue. Colors with full saturation (100%) are the color itself, colors with no saturation (0%) are completely grayscale.
- Lightness refers to the lightness of the color. 0% is black, 100% is white.
- A, or alpha, refers to the opacity. 0% is fully transparent, 100% is fully opaque.

Using values that have semantic meaning gives the designer more direct control over the color scheme, and more direct ability to manage contrast and create related color schemes.

![[HSL color-wheel.png]]

### Warm Colors
All colors have a warmth value assigned to them, which can be classified as warm or cool.

Warm colors range between red and yellow, which include various versions of those colors in addition to orange. This also comprises colors such as brown and tan. These are considered to be “warm” colors in that they evoke a sense of warmth. For instance, fire is associated with warmth, and it typically burns between the spectrum of reds and yellows. Warm colors can also promote a feeling of aggression and are considered bold.

In the `style.css` file, we’ve created a layout consisting of five blocks. Let’s explore warm colors by creating a spectrum of them within the browser.

**Note:** We’ll be using HSL color properties to adjust our colors. You can refer to [this list of HSL color codes](http://www.december.com/html/spec/colorhsl.html) if you want to discover more.

###### Instructions
1. In the `style.css` file, update the hue of the `.first-color` class to a value between 0 and 8.
2. Next, update the hue of the `.second-color` class to a value between 8 and 15.
3. Change the value of the hue of the `.third-color` class to a number between 15 and 30.
4. Make the `.fourth-color` hue a value between 30 and 45.
5. Finally, change the `.fifth-color` hue a value between 45 and 60.

```html
<!DOCTYPE html>
<html>
<head>
  <link rel='stylesheet' type='text/css' href='styles.css'>
</head>
<body>
  <section class="first-color">First Color</section>
  <section class="second-color">Second Color</section>
  <section class="third-color">Third Color</section>
  <section class="fourth-color">Fourth Color</section>
  <section class="fifth-color">Fifth Color</section>
</body>
</html>
```

```css
body {
  background-color: #fdfdfd;
  margin:0;
  padding: 0;
  overflow: hidden;
}
section {
  width: 100%;
  display: block;
  height: 18vh;
  padding: 1vh;
  font-size: 22px;
  border-style: solid;
  border-width: 0px 0px 1px 0px;
}

.first-color {
  background-color: hsla(5, 100%, 50%, 1);
}
.second-color {
  background-color: hsla(12, 100%, 50%, 1);
}
.third-color {
  background-color: hsla(22, 100%, 50%, 1);
}
.fourth-color {
  background-color: hsla(37, 100%, 50%, 1);
}
.fifth-color {
  background-color: hsla(52, 100%, 50%, 1);
}
```

![[warm-colors.png]]
### Cool Colors
On the other side of the color wheel in contrast to warm colors, there are colors that are considered to be “cool”. These colors range between blue, purple and green. Most gray colors fall into the cool category as well.

Cool colors are given this designation because of their calming, soothing nature. They’re often associated with winter climates or water.

As we did before, let’s update our colors to create a spectrum of cool colors.

###### Instructions
1. In the `style.css` file, update the background color of the `.first-color` class to feature a hue between 260 and 280.
2. Change the background color of the `.second-color` class to feature a hue between 240 and 260.
3. Next, make the background color of the `.third-color` class have a hue ranging between 190 and 240.
4. Update the hue value of the background color of the `.fourth-color` class between 170 and 190.
5. Finally, change the hue value of the background color for the `.fifth-color` class between 140 and 160.

```css
body {
  background-color: #fdfdfd;
  margin:0;
  padding: 0;
  overflow: hidden;
}
section {
  width: 100%;
  display: block;
  height: 18vh;
  padding: 1vh;
  font-size: 22px;
  border-style: solid;
  border-width: 0px 0px 1px 0px;
}

.first-color {
  background-color: hsla(270, 100%, 50%, 1);
}
.second-color {
  background-color: hsla(250, 100%, 50%, 1);
}
.third-color {
  background-color: hsla(215, 100%, 50%, 1);
}
.fourth-color {
  background-color: hsla(180, 100%, 50%, 1);
}
.fifth-color {
  background-color: hsla(150, 100%, 50%, 1);
}

```

![[cool-colors.png]]

### Tints and Shades
You can also increase and decrease the lightness of a color, resulting in tints and shades of a hue, respectively.

Tints occur when white is applied to a color, adding or increasing the lightness of a hue.

Shades are created when black is added to a color, which decreases the lightness of a hue.

In HSLA, tints and shades are determined by the third number, which is L for lightness. This starts at 0% (black) and ranges to 100% (white).

Understanding how to use tints and shades of a color can help in creating a wider range of colors you could apply to your websites.

In this exercise, we’ll keep the hue consistent (blue), and we will vary the lightness value to create increasingly lighter shades.

###### Instructions
1. Change the lightness of the `.second-color` class background color within the range of `35%` and `45%` to create a slightly lighter shade of blue.
2. Update the lightness of the `.third-color` class background color within the range of `45%` and `55%`.
3. Make the lightness of the `.fourth-color` fall within the range of `55%` and `65%`.
4. Finally, change the lightness of the `.fifth-color` fall within the range of `65%` and `75%`.

```css
body {
  background-color: #fdfdfd;
  margin:0;
  padding: 0;
  overflow: hidden;
}
section {
  width: 100%;
  display: block;
  height: 18vh;
  padding: 1vh;
  font-size: 22px;
  border-style: solid;
  border-width: 0px 0px 1px 0px;
}

.first-color {
  background-color: hsla(240, 100%, 30%, 1);
}
.second-color {
  background-color: hsla(240, 100%, 40%, 1);
}
.third-color {
  background-color: hsla(240, 100%, 50%, 1);
}
.fourth-color {
  background-color: hsla(240, 100%, 60%, 1);
}
.fifth-color {
  background-color: hsla(240, 100%, 70%, 1);
}
```

![[tints-shades.png]]

### Color Contrast

Color contrast plays a major role in design as well. Colors opposite of each other on the color wheel tend to have a higher contrast. Colors that fall next to each other have a lower contrast to one another.

When applying color to your designs, it’s vital to ensure contrast levels provide clarity to the users for the elements on your page. For instance, you wouldn’t want to use a light color on a white background or a detailed background. It’s essential to try and increase the contrast of your designs in order to promote ease of use and legibility.

This is also the reason why you often see dark gray or black text on a white background. The high contrast between the two colors provides the best ability for users to read the information without any difficulty.

Before we begin to add color to our website, let’s add contrast to the text elements to ensure the readability of our content is ideal.

### Color Schemes

Now that you’ve learned some basic color theory, let’s explore how you can select and apply color to your designs.

As a designer, it’s vital to understand how properly harmonizing colors will enable you to create elegant and usable designs. The color wheel comes in handy when deciding which colors might fit with one another, and using it can allow you to create a variety of color schemes.

Color schemes (or color palettes) are the result of pairing two or more colors together. The colors you select can make or break your design, however, knowing your options will put you in a better place to determine what is best for moving forward.

When deciding which colors to use in your design, there are four different color schemes to consider:

- [[Monochromatic]]
- [[Complementary]]
- [[Analogous]]
- [[Triadic]]

Each of these can work to your advantage depending on how you want your designs to display. Let’s explore each type of color scheme and apply it to our site to see how they differ.

![[color schemes.png]]


### Color Psychology

Even though we’ve explored multiple possibilities in terms of selecting color schemes, when it comes down to choosing the right combinations, a designer must determine the “feel” of their website.

Every color has a different context and meaning, and color psychology can impact how people perceive a design and relate to the colors used. Choosing the right colors can help nonverbally communicate the context and emotion of a product or service.

![[Color Psychology.png]]

Each color has a specific meaning (both positive and negative), which can evoke emotions from a user. For instance, here’s a list of words often associated with colors:

- **Red:** Passionate, energetic, angry
- **Orange:** Optimistic, playful, fun
- **Yellow:** Welcoming, intellectual, impatient
- **Green:** Prosperous, balanced, growing
- **Blue:** Peaceful, loyal, cold
- **Purple:** Imaginative, royal, spiritual
- **Gray:** Unemotional, compromising
- **White:** Innocent, pure
- **Black:** Luxurious, powerful

It’s also important to note that color associations may vary from other parts of the world as well. However, when selecting colors, be sure to choose ones that help reinforce the overall message and tone of the website!


### Best Practices

Now that we’ve talked through how to choose the proper colors for your designs, there are some best practices to consider as well.

**Use neon colors sparingly.** While the use of neon colors can feel hip, they are often hard on a user’s eyes.

**Avoid vibrating colors.** Vibrating colors result from pairing two colors with high saturation together that may be complementary to one another. It creates a glowing or moving effect, which also can be hard on one’s eyes.

For example, the red and green pairing that is common with Christmas cards is very glaring when presented on a screen. See the example below to notice how intense and distracting this pairing feels.

![[color-contrasts.png]]

**Use backdrops to separate vibrating colors.** In the example, the white backdrop behind the green card reduces the space where the contrasting colors (red and green) are directly next to each other, but the overall effect is still too intense for most websites.

**Avoid color combinations with insufficient contrast**, including:

- Bright colors on top of bright colors
- Light colors on top of light colors
- Dark colors on top of dark colors

Even if there’s enough contrast in these pairings for the different colors to be legible, they likely won’t create enough contrast to attract the user’s attention.

Remember that **most users skim websites!** They are not reading every word and checking every menu—you need to guide the user to the most important content with good color choices.



### Color Theory Review

Congratulations! You gained some knowledge on color theory and how to select colors to use within your websites.

Remember, the keys to choosing the right colors for your projects are:

- Using the color wheel as a basis for selecting colors
- Using a color scheme approach that promotes harmony
- Using colors that fit the context and emotion you are trying to display to users
- Using contrast to enhance the legibility of elements on the page
- Using shades and tints of a color to create flexibility
- Avoiding combinations that can cause issues for users

Following these guidelines allow you to create more elegant, engaging and beautiful websites!
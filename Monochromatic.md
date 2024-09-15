### Monochromatic Designs

The most basic color scheme possible utilizes a single color with varying shades and tints to create a monochromatic palette.
![[Monochromatic.svg]]


Each color in the scheme is derived from the base color. While all elements within the design may feel similar, you can help eliminate the monotonous feeling with high contrast. This means when you are selecting a monochromatic color scheme, it’s important to select a much lighter and much darker shade of the main color.

These monochromatic color schemes are beneficial in that they provide an organized impression when applied to your designs. The use of a single color can provide an immediate sense of harmony.

Monochromatic schemes can also consist of black and white, with varying shades of gray, as you see in our current site. However, let’s enhance it by selecting a different base color and applying a monochromatic color scheme to our website!

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Codecademy | Celestial Color Theory</title>

  <!-- Meta -->
  <meta charset="utf-8">
  <meta content="IE=edge,chrome=1" http-equiv="X-UA-Compatible">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1 user-scalable=no">

  <!-- Fonts -->
  <link href="https://fonts.googleapis.com/css?family=Barlow+Condensed:700|Barlow:400,700" rel="stylesheet">

  <!-- CSS -->
  <link rel='stylesheet' type='text/css' href='styles.css'>
</head>
<body>
  <!-- Site Header -->
  <header role="banner" aria-label="site navigation" class="site-header">
    <!-- Site Navigation -->
    <nav role="navigation" class="site-navigation">
      <ul class="site-header-left">
        <li>
          <img src="https://content.codecademy.com/programs/ui-design/color-theory-lesson/color-theory-logo.svg" alt="Celestial" />
        </li>
      </ul>
      <ul class="site-header-right">
        <li>
          <a href="#">About</a>
        </li>
        <li>
          <a href="#" class="button button-primary">Download Now</a>
        </li>
      </ul>
    </nav>
  </header>
  <!-- Site Main Content -->
  <main role="main">
    <!-- Main Content Header -->
    <section role="region" aria-label="page-hero-title" class="page-hero-header">
      <div class="container">
        <div class="page-hero-header-left">
          <h1 id="page-hero-title">Look up in the sky</h1>
          <p>All-new app so you can see deeper and further into space than ever before</p>
          <a href="#" class="button button-primary">Download Now</a>
        </div>
        <div class="page-hero-header-right">
          <div class="img-container">
            <img src="https://content.codecademy.com/programs/ui-design/color-theory-lesson/color-theory-screen-1.png" alt="application interface" />
          </div>
        </div>
      </div>
    </section>
    <!-- Main Content Benefits -->
    <section role="region" class="main-content-benefits">
      <div class="container">
        <ul class="clearfix">
          <li class="item">
            <div class="item-image"></div>
            <h2>Step I</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer at nunc id ligula sollicitudin finibus eget id leo.</p>
          </li>
          <li class="item">
            <div class="item-image"></div>
            <h2>Step II</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer at nunc id ligula sollicitudin finibus eget id leo.</p>
          </li>
          <li class="item">
            <div class="item-image"></div>
            <h2>Step III</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer at nunc id ligula sollicitudin finibus eget id leo.</p>
          </li>
        </ul>
      </div>
    </section>
    <!-- Main Content Info -->
    <section role="region" class="main-content-info">
      <div class="mobile-show main-content-info-left">
        <img class="mobile-show" src="https://content.codecademy.com/programs/ui-design/color-theory-lesson/color-theory-image-1.jpg" alt="Nebula"/>
      </div>
      <div class="container">
        <div class="main-content-info-right">
          <h2>Pictures of the Sky</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer at nunc id ligula sollicitudin finibus eget id leo.</p>
          <a href="#" class="button button-primary">Download Now</a>
        </div>
      </div>
    </section>
    <!-- Main Content CTA -->
    <section role="region" class="main-content-cta">
      <div class="container">
        <div class="main-content-cta-left">
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer at nunc id ligula sollicitudin finibus eget id leo.</p>
        </div>
        <div class="main-content-cta-right">
          <div class="cta-container">
            <input type="email" placeholder="Email Address" />
            <button type="submit" class="button button-secondary">Subscribe</button>
          </div>
        </div>
      </div>
    </section>
  </main>


  <!-- Site Footer -->
  <footer role="contentinfo" class="footer clearfix">
    <!-- Site Footer Nav -->
    <nav role="navigation" class="footer-navigation">
      <ul class="footer-left">
        <li>
          Copyright &copy; 2017. Celestial. All Rights Reserved.
        </li>
      </ul>
      <ul class="footer-right">
        <li>
          <a href="#">Home</a>
        </li>
        <li>
          <a href="#">About</a>
        </li>
        <li>
          <a href="#">Download Now</a>
        </li>
      </ul>
    </nav>
  </footer>
</body>
</html>

```

##### Instructions:
1. Notice the insufficient contrast around the gray links and buttons. Because this gray is a medium tint, neither white or black shows up on top of it with enough contrast.

	Let’s change it to a nice, dark navy blue!
	
	In `styles.css`, change the color of the `<a>` tag to `#0D1C32`.
	
	This will change the “About” link (at the top of the page) and the links in the footer to a dark navy blue (you might need to scroll to notice these changes).

1. Let’s make the same change to the buttons on the site. 
	Change the background color of the `.button-primary` class to the same dark navy blue (`#0D1C32`).

3. Let’s update the background color of the `.footer` to follow our blue monochromatic color scheme.
	Because there are dark navy blue links within the footer, let’s use a light periwinkle blue. Use the hex code`#ECF3FF`.

4. The main buttons on this site are prompting the user to download the application. But there’s a second type of button, which prompts the user to subscribe. We should use a different shade of blue to differentiate this button from the others.
	
	Change the background color of the `.button-secondary` class to `#627FB0`, which is a slate blue.

5. Let’s use this slate blue as an accent color elsewhere. The “page hero” is a design term that refers to the banner (image, often paired with text and a background) that is placed front and center on the page.
   
   Change the background color within the `.page-hero-header` class to use the slate blue (`#627FB0`).

6. Make the background color of the `.main-content-benefits` class `#F5F9FF`. This will be the lightest shade of blue that we use, which will improve the legibility of the text in front of it.

7. The text in front of that very light blue can be the dark navy color that we use elsewhere on the site. Notice that we are re-using the same shades of blue in different elements, to create harmony, while still ensuring contrast.

	Update the color of the `.main-content-benefits h2` to `#0D1C32`.

8. Update the background color of the `.main-content-cta` section to the same color (`#0D1C32`). This is the background color that surrounds the call-to-action for the user to subscribe.

9. It’s often helpful to give distinct sections of content their own background color, to create visual groupings that convey how information is grouped.

	Change the `.main-content-info` class background color to `#627FB0`.

```css
/* Site Stylesheet
  1. Global Styles
  2. Typography Styles
  3. Structure Styles
  4. Module Styles
  5. Component Styles
  6. Page Styles
======================================== */

/* 1. Global Styles
======================================== */
* {
  box-sizing: border-box;
}

html {
  margin: 0 auto;
  overflow-x: hidden;
  width: 100%;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0 auto;
  overflow-x: hidden;
  width: 100%;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  color: #999999;
}
.clearfix::after {
  content: " ";
  clear: both;
  display: table;
}
.float-right {
  float: right;
}

/* 2. Typography Styles
======================================== */
h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: 'Barlow Condensed', Helvetica, sans-serif;
  font-weight: 700;
  line-height: 1.25;
  margin-bottom: 15px;
  transition: font-size 0.25s ease;
  text-transform: uppercase;
}

h1 {
  font-size: calc(100px / 1.25);
  line-height: 0.85;
}
h2 {
  font-size: calc(65px / 1.25);
  margin-top: 10px;
  line-height: 0.85;
}
@media(min-width: 1024px) {
  h1 {
    font-size: 100px;
  }
  h2 {
    font-size: 60px;
  }
}
p {
  font-family: 'Barlow', Georgia, serif;
  font-size: 16px;
  line-height: 23px;
  margin: 0 0 15px;
}
a {
  font-family: 'Barlow', Helvetica, sans-serif;
  font-size: 16px;
  color: #0D1C32;
}
ul {
  padding: 0;
  margin: 0;
}
li {
  font-family: 'Barlow', Helvetica, sans-serif;
  font-size: 16px;
  line-height: 23px;
  list-style: none;
}
img {
  width: 100%;
}

/* 3. Structure Styles
======================================== */
.container {
  margin: 0 auto;
  max-width: 1280px;
  padding: 0 15px;
}
.container:before, .container:after {
  content: " ";
  display: table;
  clear: both;
}
.mobile-hide {
  display: none;
}
.mobile-show {
  display: block;
}
@media(min-width: 720px) {
  .mobile-hide {
    display: block;
  }

  .mobile-show {
    display: none;
  }
}
/* 4. Modules Styles
======================================== */

/* Site Navigation */
.site-header {
  background-color: #FFFFFF;
  padding: 30px 15px;
}
.site-navigation {
  margin: 0 auto;
  max-width: 1280px;
}
.site-header-left,
.footer-left {
  display: inline-block;
}
.site-header-left li {
  line-height: 0;
}
.site-header-right,
.footer-right {
  display: inline-block;
  float: right;
}
.site-header-right li,
.footer-right li {
  display: inline;
}
.site-header-right li a {
  text-decoration: none;
  margin-left: 20px;
}

/* Site Footer */
.footer {
  background-color: #ECF3FF;
  padding: 30px;
}
.footer-navigation {
  margin: 0 auto;
  max-width: 1280px;
}
.footer-right {
  float: none;
  margin-top: 15px;
}

@media(min-width: 720px) {
  .footer-right {
    float: right;
    margin-top: 0;
  }
}
.footer li {
  line-height: 0;
}
.footer li a {
  text-decoration: none;
  margin-left: 20px;
}

/* 5. Component Styles
======================================== */
button {
  border: none;
}
button:hover {
  cursor: pointer;
}
.button {
  border-radius: 100px;
  display: inline-block;
  font-family: 'Barlow', Helvetica, sans-serif;
  font-size: 16px;
  text-transform: uppercase;
  line-height: normal;
  padding: 15px 30px;
  text-align: center;
  text-decoration: none;
  transition: opacity 0.5s ease;
}
.button:hover {
  opacity: 0.75;
}
.button-primary {
  background-color: #0D1C32;
  color: #FFFFFF;
}
.button-secondary {
  background-color: #627FB0;
  color: #FFFFFF;
}
input {
  border-radius: 100px;
  margin-bottom: 15px;
  padding: 10px;
  border: none;
  box-shadow: none;
  transition: border-color 0.5s ease;
  width: 100%;
}

/* 6. Page Styles
======================================== */
.page-hero-header {
  background-color: #627FB0; 
  background-image: url('images/saturn-background.svg');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  max-height: 600px;
  overflow: hidden;
}
.page-hero-header-left, .page-hero-header-right {
  width: 100%;
  text-align: center;
  display: block;
}
.page-hero-header-left {
  padding: 0px 40px;
  color: #FFFFFF;
}
.main-content-benefits {
  padding: 80px 0;
  background-color: #F5F9FF;
}
.main-content-benefits h2 {
  color: #0D1C32;
}
.main-content-info {
  background-color: #627FB0;
  text-align: center;
}
.main-content-info-left {
  max-height: 300px;
  width: 100%;
  overflow: hidden;
}
.main-content-info-right {
  padding: 60px;
  color: #FFFFFF;
  width: 100%;
}
.main-content-cta-left, .main-content-cta-right {
  width: 100%;
  padding: 0 30px;
  text-align: center;
}
.main-content-cta {
  background-color: #0D1C32;
  color: #FFFFFF;
  padding: 80px 0;
}
.cta-container {
  position: relative;
}
.cta-container input {
  width: 100%;
  padding: 23px 30px;
  font-size: 1em;
}
.cta-container button {
  position: absolute;
  right: 10px;
  top: 7px;
  -webkit-appearance: none;
  -moz-appearance: none;
  border: none;
}

/* Items */
.item {
  margin-bottom: 30px;
  width: 100%;
  padding: 0 2%;
  text-align: center;
}
.item .item-image {
  background: #FFFFFF;
  box-shadow: 0 5px 20px 0 rgba(0,0,0,0.05);
  border-radius: 10px;
  width: 100%;
  height: 250px;
}
@media(min-width: 720px) {
  .page-hero-header-left, .page-hero-header-right {
    width: 50%;
    text-align: left;
    display: inline-block;
    float: left;
  }
  .page-hero-header-left {
    padding: 80px;
  }
  .page-hero-header-left p {
    font-size: 24px;
    line-height: 28px;
    margin: 0 0 20px;
  }
  .main-content-info {
    background-image: url('images/space-image.jpg');
    background-repeat: no-repeat;
    background-position: center left;
    background-size:50%;
    text-align: left;
  }
  .main-content-info-right {
    padding: 80px;
    width: 50%;
    float: right;
    display: inline-block;
  }
  .main-content-cta-left, .main-content-cta-right {
    width: 50%;
    float: left;
    display: inline-block;
    padding: 0 30px;
    text-align: left;
  }
  .item {
    float: left;
    margin-bottom: 0;
    width: calc(95%/3);
  }

  .item:not(:last-child) {
    margin-right: 2.5%;
  }
}
```


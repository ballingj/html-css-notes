METADATA
Language:: Design
Sub-concepts:: Web Design Colors

Summary:: 


---
# Color for UI

## ### Introduction

When diving deeper into the use of color in web design, there’s more to creating a usable experience than just selecting beautiful, harmonious colors.

While aesthetics can enhance the display of your website, an important part of being a designer is ensuring your audience understands how to interact with your product and make effective decisions to solve their goals.

As you continue to grow as a designer, you’ll begin to look at a site holistically through the eyes of a user. More importantly, when it comes to color, applying the right hues to actions and messaging that the user will perceive and act on will be a powerful tool to improve the UI of your site.

In this lesson, we’ll explore

- How to use contrast to imply hierarchy on a page and draw a user’s attention
- How to establish brand and accent colors and then how to properly apply them
- What states are necessary for buttons and forms
- How to properly provide feedback on error, success and warning messages
- How to use neutral colors to effectively communicate your content
- Why whitespace is important to the usability and aesthetic quality of your designs
- How to ensure your website is usable for all individuals

We will be applying the knowledge you learn during this lesson to update the wireframe to your right.

Please note that the browser view of the website has been scaled to fit the viewport’s size. If you expand your browser view the site will change based on the viewing area.

### Contrast Constraints

Contrast is a great way to differentiate elements on a page. However, by doing so to all elements, it can cause a cognitive overload for users. When there are a lot of competing elements, everything is vying for their attention, which can lead to nothing being dominant on the page.

When thinking about and applying contrast to a page through the use of color, it’s important to limit the overall amount of contrast. This helps you as the designer to highlight only the most important parts of the page—the actions you want the users to focus on and take.

Having a neutral background (any color with low lightness or saturation) is a good base, because it allows you to add high contrast to the parts of the site where you want to direct a user’s attention.

Similarly, a dark background with light colored text can be a reasonable alternative, depending on the assets like image or video, that you are displaying on the site.

On the other hand, a medium background is a little bit more tricky because it can be hard to create enough contrast and allow for clear visibility.

##### Instructions:   (See starter HTML/CSS files below this page)
1.  Let’s start off by addressing the background color of the header and hero section. A hero is a section placed prominently on a web page like a banner.

	First, we will start by applying a background color to the navigation that helps bring our links into focus.
	
	In the **styles.css** file, find the CSS selector `.site-header` and replace the property `background-color` from `#EBEBEB` to `#34474F`.
	
	You can find this selector in section 4 which is called `Modules Styles.`
	
2. Now let’s blend that navigation color into the background of our hero section.
	
	In the **styles.css** file, find the CSS selector `.site-main-background` and replace the property `background-color` from `#EBEBEB` to `#34474F`.
	
	This selector can be found in section 6 which is called `Page Styles.`
	
3. Moving right along. As you can see now, the hero heading and hero paragraph text is very hard to read. We want to make sure we maximize our contrast here. Especially since this text introduces users to our page’s core responsibility.

	In the **styles.css** file, find the CSS selector group
	
	```
	.site-main-header h1,.site-main-header p { }
	```
	
	and replace the property `color` from `#2A2A2A` to `#FFFFFF`.
	
4.  Lastly, we need to adjust our navigation link text so it is legible.

	In the **styles.css** file, find the CSS selector `.site-nav-link` and replace the property `color` from `#959595` to `#FFFFFF`.
	
	To find this selector navigate back up to section 4, `Modules Styles.`

### Brand Color

Each company, whether it be an internet startup, a sports team, or a multinational clothing label, has a defined brand color. For instance, Facebook has its iconic blue, as does Twitter, while Coca-Cola features red as its primary color.

Just think about all of the brands you know and love and colors you associate with them. There’s even a site, called [BrandColors](https://brandcolors.net/), dedicated to showing those for various companies.

When working on a design, it’s essential to select and apply a brand color. This is a hue that should dominate your color palette. This brand color will account for roughly 60% of the color used on your site, and helps build a bridge between your product and the user’s recognition of it.

##### Instructions
1.  Now that we have an idea of brand colors and how they can really bring our site to life, let’s integrate some of this brand’s colors into our site.
	
	In the **styles.css** file, find the CSS selector `.site-nav-link-active` and replace the property `color` from `#2A2A2A` to `#FF6600`.
	
	This selector is at the bottom of section 4, `Modules Styles`, right before the footer styles.

### Accent Colors

While brand colors typically dominate the makeup of a web site, accent colors are equally important. These supplementary hues provide small pops of color within your designs and can be used to draw the user’s attention.

For instance, if you’ve selected a color scheme, one (or more) of the colors from your palette would be used as an accent color. This would allow you to apply these accent colors in various parts of your design to help the user decipher calls-to-action, which are an important part of guiding the user to achieve their goal.

### Buttons

Buttons are one type of element where accent colors can be used effectively. As these provide ways for the user to navigate, submit a form, or move onto the next task, the color of a button can determine a lot in the user’s eyes.

In addition to selecting the right color for your buttons, there are different states a button has as the user interacts with them. These different states provide a visible signal to the user that an interaction is or is not possible. Two common states used are the **hover state** and the **disabled state**.

The hover state typically features a shade or tint of the accent color used for the buttons. This helps a user comprehend that something is happening as they scroll over top of an action.

As a designer, you must also consider how to communicate to your users that a button has been disabled and is no longer actionable. The disabled state implies that the button cannot be clicked, either because it’s not an active button or the user must complete steps prior to the button activating.

A good example is a user sign-in form. We can disable the button for signing in until the user has provided us a username or email and a valid password.

##### Instructions
1.  When designing web sites, web applications or mobile applications, designers tend to use a lot of buttons to call attention to actions they want their users to take. To keep these actions users take consistent, naming your buttons properly in your CSS is important.
	
	In this example, the page actions are our primary buttons. While the buttons that appear in our navigation and footer are our secondary buttons.
	
	In the **styles.css** file, find the CSS selector `.button-primary` and replace the property `background-color` from `#959595` to `#00CF63`.
	
	This selector can be found in section 5, `Component Styles.`

2.  In the **styles.css** file, find the CSS selector `.button-secondary` and replace the property `background-color` from `#2A2A2A` to `#FFAA00`.

	This selector can be found in section 5, `Component Styles.`

### Forms

Form inputs are another type of component that use color to indicate an action to a user. Similar to buttons, form inputs have certain states.

There is the default state, which is how the user views the inputs when they first arrive at a page.

The second state is the selected, or active, state. These provide the user with a visual cue that they have highlighted the field and have the ability to type within it. This is typically achieved by using a border color or a box shadow effect.

If the input field is unable to be edited or typed within, there should be a disabled state as well. This should render much like the disabled button, in that it is grayed out.

Inputs also have other colors that indicate success and failure. These are called semantic colors.

##### Instructions
1.  To ensure our users know what form element they are filling out, we are going to add some color to our hover state and active state. To do so we will use a CSS pseudo-selector.
	
	In the **styles.css** file, find the selectors
	
	```
	input:active, input:focus,textarea:active, textarea:focus {}
	```
	
	and change the `border` property from `1px solid #CCCCCC` to `1px solid #42A5F5`

### Semantic Colors

In addition to your brand and accent colors, you have to remember to provide additional indications to the user when something goes right or wrong.

People make mistakes. We’re all human. So when designing user input elements, you must understand that errors will arise. When this happens, users should be alerted to understand where they went wrong. A common design pattern color used for this indicator is red.

Red is also used to provide more emphasis for delete buttons. If the user wishes or is required to delete something, it should be abundantly clear that the delete action is different from a normal action.

On the other hand, when a user achieves their goal without issue or does something right, you should reward them! A good way to do that is through the use of green as a success message. Green is also often used for actions that entice the user to submit, move forward, or go.

Not all errors are caused by the user. Sometimes, the code just breaks! If an error occurs on the website and we need to notify the user, we should consider selecting a color that indicates the issue level and one that does not conflict with our action colors. A typical color for these warning situations is yellow.

The visual feedback you provide users with when they interact with your interface is incredibly important. It can help alleviate pain points some users might experience.
##### Instructions
1.  Now we need to show our users they made an error. One way to do this is to keep an active border state on the input that was not filled out correctly.
	
	In the **styles.css** file, find the selectors `.input-error` and change the `border-color` property value from `#F2F3F5` to `#FC472E`.

2.  Since we already established the color that represents an error, we will apply that to our alert. But since we know color shouldn’t be the only thing to communicate an error to our users, note the alert icon we placed inside of the alert component.
	
	In the **styles.css** file, find the selectors `.alert-error` and change the `background-color` property value from `#CCCCCC` to `#FC472E`.
	
	You can find this selector in section 5, `Component Styles`.

### Default Colors

Next, let’s discuss default or structural colors. Almost every site you design will incorporate black, white, and shades of gray in some way. These default colors are used often as the color for text within your designs, as they provide plenty of contrast for reading and can fit into many other different color schemes.

When selecting the color of your text, it’s important to ensure the contrast is high enough for the text to be legible. However, too much contrast can also be an issue.

Pure black on white can be hard on the user’s eyes because of the stark contrast. Using a darker gray for text on a white background, or white text on a dark gray background, helps soften the feel while still providing clear enough contrast to be legible without issue.

![[DefaultColors.png]]

### Neutral Colors

It’s important to consider how contrast will also be affected when using different colors for backgrounds and text.

Neutral colors, or hues with low lightness and/or saturation, make for good base colors as it allows you to add flourishes to the parts of the site where you want to direct the user’s attention.

For example, similar to using a dark gray with white text, you can use a darker shade of a color with light colored text. Using a medium shade or tint of a color can be difficult to achieve the same result, as the contrast is lower.

### Whitespace

Space is an important aspect of creating balanced and harmonious layouts in web design. As a designer, it’s important to understand how space can enhance as well as hurt your designs.

Whitespace, or negative space, refers to the emptiness between elements. It’s not necessarily white in color, even though, that is sometimes the case.

For example, you will notice that [Google](http://www.google.com) embraces whitespace on its landing page. It focuses the user’s attention solely on the primary action, which is searching for content.

Too much whitespace can negatively impact the flow of your site. By including too much spacing in-between elements, it can cause issues for users trying to navigate seamlessly through the content.

As a designer, don’t fear using space to enhance the usability of your site and prioritize the most important content.

##### Instructions
1.  Our site is starting to come together. But it is a little tight. Let’s add some white space to different parts of the site’s interface. One way to add some nice space between elements on a page is by applying the property of padding to elements.
	
	Remember, padding is the space inside of an element, while margin is the space around the element.
	
	In the **styles.css** file, find the CSS selector `.site-main` and update the `padding` property values from `0 15px` to `60px 15px`.
	
	This selector can be found in section 6, `Page Styles.`

2.  In the **styles.css** file, find the CSS selector `.site-main-header` and update the `margin-bottom` property values from `0` to `60px`.
	
	This selector can be found in section 6, `Page Styles.`

3.  In the **styles.css** file, find the CSS selector `.location-details li` and update the `margin-top` property values from `0` to `15px`.
	
	This selector can be found in section 6, `Page Styles.`

4.  In the **styles.css** file, find the CSS selector group

```
.site-nav-left li:not(:last-child),.site-nav-right li:not(:last-child),.site-nav-mobile li:not(:last-child) {}
```
	
 and update the `margin-right` property values from `5px` to `45px`.
	
 This selector can be found in section 4, `Modules Styles.`

### Accessibility

Making sure that the colors you choose for your UI components are accessible is a really important aspect of visual design.

Using contrasting colors will help users that need assistance understand and differentiate the content you have designed.

However, many users can experience different types of color blindness:

- **red-green**, where users have a difficult time differentiating between the red and green colors.
- **blue-yellow**, where the blues tend to appear greener
- **monochromatic**, when users can’t see color at all.

To make your sites more accessible, try pairing another indicator along with color to convey information. Earlier, we mentioned using green as a success indicator and red as an error alert indicator. Consider using a label indicator such as a green check for success and a red “x” for error to ensure the user has a full understanding of the message.

If you are having trouble deciding on an accessible color palette you can visit [Color Safe](http://colorsafe.co/) which creates accessible color palettes for your site or app based on Web Content Accessibility Guidelines (WCAG).

Already decided on colors? You can go to [WebAIM Color Contrast Checker](https://webaim.org/resources/contrastchecker/) to test how your selected colors work with web usability.

As you can see in our example, we placed an icon next to the alert message to provide an additional visual cue for the user.

### Iterations

As a Visual UI designer, aesthetics are important to the overall user experience. However, if usability and aesthetics conflict, it’s always best to err on the side of usability.

Testing and iteration are essential parts of the user-centered design process. Test early and test often is the motto of designers! No amount of design knowledge can replace putting your designs in front of users to gain appropriate and helpful feedback.

As some users are different from others, gaining a better understanding of who you are building for will help in ensuring the color choices work. So it’s important to understand that while you may fall in love with that shade of blue, you should be prepared to change your color choices based on the feedback you receive.

![[define-develop-test-research-loop.png]]

### Review

Congratulations! You gained some knowledge on using color for UI design and how to ensure your websites are usable while remaining aesthetically pleasing.

Remember, the keys to designing for UI:

- Select a dominant brand color and supporting accent colors
- Use contrast to define sections and differentiate actions
- Use semantic colors for error and success messages
- Incorporate default colors for text and backgrounds where needed
- Neutral colors can provide good contrast
- Keep users in mind when selecting color

Following these guidelines allow you to create more elegant, engaging and beautiful websites!

### Starter html
```html
%% starter html %%
<!DOCTYPE html>
  <html lang="en">
  <head>
    <title>Codecademy | Color For UI</title>

    <!-- Meta -->
    <meta charset="utf-8">
    <meta content="IE=edge,chrome=1" http-equiv="X-UA-Compatible">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1 user-scalable=no">

    <!-- CSS -->
    <link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/meyer-reset/2.0/reset.min.css">
    <link rel="stylesheet" type="text/css" href="styles.css">

    <!-- Fonts -->
    <link href="https://fonts.googleapis.com/css?family=Roboto:400,700" rel="stylesheet">
  </head>
  <body>
    <!-- Site Wide Header -->
    <header role="banner" aria-label="site-wide-navigation" class="site-header">
      <div class="container">
        <nav role="navigation" aria-label="navigation" class="site-header-nav">
          <ul class="site-nav-left">
            <li>
              <a href="#">
                <img src="https://content.codecademy.com/programs/ui-design/color-ui/logo.svg" alt="Citrus" class="logo" />
              </a>
            </li>
            <li>
              <a href="#" class="site-nav-link">About</a>
            </li>
            <li>
              <a href="#" class="site-nav-link-active">Contact Us</a>
            </li>
          </ul>
          <ul class="site-nav-right">
            <li>
              <a href="#" class="site-nav-link" aria-label="site-wide-search-button" role="button">
                <img src="https://content.codecademy.com/programs/ui-design/color-ui/icon-search.svg" alt="Search" />
              </a>
            </li>
            <li>
              <a href="#" class="button button-secondary button-small site-nav-link">Login</a>
            </li>
          </ul>
        </nav>
      </div>
    </header>
    <!-- Site Main Content -->
    <main role="main" class="site-main">
      <header aria-labelledby="page-title" class="clearfix site-main-header">
        <div class="container">
          <h1 id="page-title">Contact Our Team</h1>
          <p class="col-1-2">We are standing by for your questions, comments or concerns. If there is anything we can do, please reach out and let us know.</p>
        </div>
      </header>
      <section role="region" aria-label="contact-form" class="site-main-section">
        <div class="container">
          <div class="card contact-form-container">
            <div class="clearfix">
              <div class="col-1-2">
                <figure class="alert alert-error">
                  <div class="alert-content">
                    <img src="https://content.codecademy.com/programs/ui-design/color-ui/icon-help.svg" alt="Help indicator" />
                    <p>Looks like you forgot to add your name!</p>
                  </div>
                </figure>
                <h2 class="section-header">Leave A Message</h2>
                <form role="form" class="clearfix">
                  <label>Your Name</label>
                  <input type="text" placeholder="Full Name" class="input-error" />
                  <label>Your Email</label>
                  <input type="email" placeholder="Email Address" />
                  <label>Select Contact Reason</label>
                  <select>
                    <option selected disabled>Please Select One</option>
                    <option>Customer Service Question</option>
                    <option>Billing Question</option>
                    <option>Website Question</option>
                  </select>
                  <label>Issue Details</label>
                  <textarea placeholder="Provide as much detail as you can so we can address your issue."></textarea>
                  <input type="submit" value="Submit Message" class="button button-primary float-right" />
                </form>
              </div>
              <div class="col-1-2">
                <p><b>Our Location</b></p>
                <img src="https://content.codecademy.com/programs/ui-design/color-ui/map.jpg" alt="Office Location" />
                <ul class="location-details">
                  <li><b>Address:</b> 233 S Wacker Dr, Chicago, IL 60606</li>
                  <li><b>Phone:</b> (123) 456-7890</li>
                  <li><b>Email:</b> support@citrusmail.com</li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </section>
      <div class="site-main-background" arai-hidden="true"></div>
    </main>
    <!-- Site Wide Footer -->
    <footer role="contentinfo" class="footer">
      <div class="container">
        <nav role="navigation" class="clearfix">
          <ul class="col-1-4 footer-section">
            <li>
              <img src="https://content.codecademy.com/programs/ui-design/color-ui/logo.svg" alt="Citrus" class="logo" />
            </li>
            <li>
              <p><smalL>All Rights Reserved | &copy; <time>2017</time></smalL></p>
            </li>
          </ul>
          <div class="col-1-4 footer-section" aria-labelledby="product-pages">
            <p id="product-pages"><b>About</b></p>
            <ul>
              <li>
                <a href="#">Features</a>
              </li>
              <li>
                <a href="#">Pricing</a>
              </li>
              <li>
                <a href="#">Schedule Demo</a>
              </li>
            </ul>
          </div>
          <div class="col-1-4 footer-section" aria-labelledby="support-pages">
            <p id="support-pages"><b>Support</b></p>
            <ul>
              <li>
                <a href="#">FAQ</a>
              </li>
              <li>
                <a href="#">Documentation</a>
              </li>
              <li>
                <a href="#">API Status</a>
              </li>
            </ul>
          </div>
          <div class="col-1-4 footer-section" arai-labelledby="social-links">
            <p id="support-pages"><b>Stay Up To Date</b></p>
            <form>
              <input type="email" placeholder="Your emaill address" class="footer-email-input">
              <input type="submit" value="Submit" class="button button-secondary footer-email-button"/>
            </form>
          </div>
        </nav>
      </div>
    </footer>
  </body>
</html>
```
### Starter CSS
```css
/* starter css */

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
  height: 100%;
  margin: 0 auto;
  overflow-x: hidden;
  width: 100%;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}

body {
  height: 100%;
  margin: 0 auto;
  overflow-x: hidden;
  width: 100%;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
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
  color: #414546;
  font-family: 'Roboto', Helvetica, sans-serif;
  font-weight: 700;
  transition: font-size 0.25s ease;
}

h1 {
  font-size: calc(64px / 1.5);
  line-height: 1.25;
}

h2 {
  font-size: calc(64px / 1.5);
}

h3 {
  font-size: calc(45px / 1.5);
}

h4 {
  font-size: calc(23px / 1.5);
}

@media(min-width: 720px) {
  h1 {
    font-size: calc(64px / 1.25);
  }

  h2 {
    font-size: calc(45px / 1.25);
  }

  h3 {
    font-size: calc(32px / 1.25);
  }

  h4 {
    font-size: calc(23px / 1.25);
  }
}

@media(min-width: 1024px) {
  h1 {
    font-size: 64px;
  }

  h2 {
    font-size: 45px;
  }

  h3 {
    font-size: 32px;
  }

  h4 {
    font-size: 23px;
  }
}

p {
  color: #414546;
  font-family: 'Roboto', Georgia, serif;
  font-size: 16px;
  line-height: 23px;
  margin: 0 0 15px;
}

a {
  color: #42A5F5;
  font-family: 'Roboto', Helvetica, sans-serif;
  font-size: 16px;
  line-height: 23px;
}

li {
  color: #414546;
  font-family: 'Roboto', Helvetica, sans-serif;
  font-size: 16px;
  line-height: 23px;
  list-style: none;
}

label {
  color: #414546;
  display: block;
  font-family: 'Roboto', Helvetica, sans-serif;
  font-size: 12px;
  font-weight: 700;
  line-height: 18px;
  margin-bottom: 5px;
}

img {
  width: 100%;
}

b,
strong {
  font-weight: 700;
}

small {
  font-size: 12px;
  line-height: 1.25;
}

/* 3. Structure Styles
======================================== */
.container {
  margin: 0 auto;
  max-width: 1160px;
  padding: 0 15px;
}

.divider {
  border: none;
  border-bottom: 1px solid #F2F3F5;
  clear: both;
  width: 100%;
}

@media(min-width: 720px) {
  .col-1-2 {
    float: left;
    width: calc(97.5%/2);
  }

  .col-1-2:not(:last-child) {
    margin-right: 2.5%;
  }

  .col-1-3 {
    float: left;
    width: calc(95%/3);
  }

  .col-1-3:not(:last-child) {
    margin-right: 2.5%;
  }

  .col-1-4 {
    float: left;
    width: calc(92.5%/4);
  }

  .col-1-4:not(:last-child) {
    margin-right: 2.5%;
  }
}

/* 4. Modules Styles
======================================== */

/* Site Navigation */
.site-header {
  background-color: #EBEBEB;
  padding: 30px 15px 0;
}

.site-header-nav {
  align-items: center;
  display: flex;
}

.site-nav-left,
.site-nav-right {
  align-items: center;
  display: flex;
}

.site-nav-right {
  float: right;
  margin-left: auto;
}

.site-nav-left li:not(:first-child),
.site-nav-right li {
  font-weight: 700;
  display: inline-block;
  line-height: 0;
}

.site-nav-mobile li {
  display: inline-block;
}

.site-nav-left li:not(:last-child),
.site-nav-right li:not(:last-child),
.site-nav-mobile li:not(:last-child) {
  margin-right: 5px;
}

.site-nav-left .logo {
  width: 120px;
}

.site-nav-link {
  color: #959595;
  text-decoration: none;
}

.site-nav-link-active {
  color: #2A2A2A;
  text-decoration: none;
}

/* Site Footer */
.footer {
  padding: 30px 30px 60px;
}

.footer-section {
  margin-bottom: 15px;
}

@media(min-width: 720px) {
  .footer-section {
    margin-bottom: 0;
  }
}

.footer .logo {
  margin-bottom: 5px;
  width: 100px;
}

.footer a  {
  color: #959595;
  text-decoration: none;
}

.footer p  {
  margin-bottom: 5px;
}

.footer-email-input {
  margin-right: 2.5%;
  width: 68% !important;
}

.footer-email-button {
  font-size: 12px !important;
  padding: 10px !important;
  width: 27.5% !important;
}

@media(min-width: 768px) {
  .footer-email-input {
    width: 57% !important;
  }

  .footer-email-button {
    width: 37.5% !important;
  }
}

/* 5. Component Styles
======================================== */
.alert {
  border-radius: 3px;
  margin-bottom: 15px;
  padding: 10px 15px;
  text-align: left;
}

.alert-content {
  align-items: center;
  display: flex;
}

.alert-error {
  background-color: #CCCCCC;
}

.alert img {
  display: inline-block;
  height: 15px;
  margin-right: 5px;
  width: 15px;
}

.alert p {
  color: #FFFFFF;
  display: inline-block;
  margin-bottom: 0;
}

.button {
  border-radius: 3px;
  color: #FFFFFF;
  display: inline-block;
  font-family: 'Roboto', Helvetica, sans-serif;
  font-size: 16px;
  font-weight: 700;
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
  background-color: #959595;
}

.button-secondary {
  background-color: #2A2A2A;
}

.button-full {
  width: 100%;
}

.button-small {
  font-size: 13px;
  padding: 10px 30px;
}

.card {
  background-color: #FFFFFF;
  border-radius: 10px;
  box-shadow: 0 0 40px 2px rgba(0, 0, 0, 0.1);
  padding: 30px 30px 15px;
}

.chip {
  display: flex;
  align-items: center;
}

.chip-img-container {
  border-radius: 30em;
  float: left;
  margin-right: 15px;
  overflow: hidden;
  height: 60px;
  width: 60px;
}

.chip-content-container {
  float: left;
}

.chip-content-title {
  margin-bottom: 0;
}
.chip-content-description {
  color: #8F9196;
  margin-bottom: 0;
}

input,
select,
textarea {
  background-color: #FFFFFF;
  border: 1px solid #F2F3F5;
  border-radius: 3px;
  box-shadow: inset 1px 1px 3px 0 rgba(189,191,192,0.10);
  height: 35px;
  margin-bottom: 15px;
  padding: 10px;
  transition: border-color 0.5s ease;
  width: 100%;
}

input[type="submit"] {
  cursor: pointer;
  height: auto;
  width: auto;
}

input:active,
input:focus,
textarea:active,
textarea:focus {
  border: 1px solid #CCCCCC;
  outline: none;
}

textarea {
  height: 100px;
}

.input-error {
  border-color: #F2F3F5;
}

/* 6. Page Styles
======================================== */
.site-main {
  padding: 0 15px;
  position: relative;
}

.site-main-background {
  background-color: #EBEBEB;
  height: 600px;
  display: block;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: -1;
}

.site-main-header {
  margin-bottom: 0;
}

.site-main-header h1,
.site-main-header p {
  color: #2A2A2A;
}

.section-header {
  font-size: 23px;
  line-height: 33px;
  margin-bottom: 15px;
}

.location-details li {
  display: block;
  margin-top: 0;
}

```

### Finished CSS
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
  height: 100%;
  margin: 0 auto;
  overflow-x: hidden;
  width: 100%;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}

body {
  height: 100%;
  margin: 0 auto;
  overflow-x: hidden;
  width: 100%;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
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
  color: #414546;
  font-family: 'Roboto', Helvetica, sans-serif;
  font-weight: 700;
  transition: font-size 0.25s ease;
}

h1 {
  font-size: calc(64px / 1.5);
  line-height: 1.25;
}

h2 {
  font-size: calc(64px / 1.5);
}

h3 {
  font-size: calc(45px / 1.5);
}

h4 {
  font-size: calc(23px / 1.5);
}

@media(min-width: 720px) {
  h1 {
    font-size: calc(64px / 1.25);
  }

  h2 {
    font-size: calc(45px / 1.25);
  }

  h3 {
    font-size: calc(32px / 1.25);
  }

  h4 {
    font-size: calc(23px / 1.25);
  }
}

@media(min-width: 1024px) {
  h1 {
    font-size: 64px;
  }

  h2 {
    font-size: 45px;
  }

  h3 {
    font-size: 32px;
  }

  h4 {
    font-size: 23px;
  }
}

p {
  color: #414546;
  font-family: 'Roboto', Georgia, serif;
  font-size: 16px;
  line-height: 23px;
  margin: 0 0 15px;
}

a {
  color: #42A5F5;
  font-family: 'Roboto', Helvetica, sans-serif;
  font-size: 16px;
  line-height: 23px;
}

li {
  color: #414546;
  font-family: 'Roboto', Helvetica, sans-serif;
  font-size: 16px;
  line-height: 23px;
  list-style: none;
}

label {
  color: #414546;
  display: block;
  font-family: 'Roboto', Helvetica, sans-serif;
  font-size: 12px;
  font-weight: 700;
  line-height: 18px;
  margin-bottom: 5px;
}

img {
  width: 100%;
}

b,
strong {
  font-weight: 700;
}

small {
  font-size: 12px;
  line-height: 1.25;
}

/* 3. Structure Styles
======================================== */
.container {
  margin: 0 auto;
  max-width: 1160px;
  padding: 0 15px;
}

.divider {
  border: none;
  border-bottom: 1px solid #F2F3F5;
  clear: both;
  width: 100%;
}

@media(min-width: 720px) {
  .col-1-2 {
    float: left;
    width: calc(97.5%/2);
  }

  .col-1-2:not(:last-child) {
    margin-right: 2.5%;
  }

  .col-1-3 {
    float: left;
    width: calc(95%/3);
  }

  .col-1-3:not(:last-child) {
    margin-right: 2.5%;
  }

  .col-1-4 {
    float: left;
    width: calc(92.5%/4);
  }

  .col-1-4:not(:last-child) {
    margin-right: 2.5%;
  }
}

/* 4. Modules Styles
======================================== */

/* Site Navigation */
.site-header {
  background-color: #34474F;
  padding: 30px 15px 0;
}

.site-header-nav {
  align-items: center;
  display: flex;
}

.site-nav-left,
.site-nav-right {
  align-items: center;
  display: flex;
}

.site-nav-right {
  float: right;
  margin-left: auto;
}

.site-nav-left li:not(:first-child),
.site-nav-right li {
  font-weight: 700;
  display: inline-block;
  line-height: 0;
}

.site-nav-mobile li {
  display: inline-block;
}

.site-nav-left li:not(:last-child),
.site-nav-right li:not(:last-child),
.site-nav-mobile li:not(:last-child) {
  margin-right: 45px;
}

.site-nav-left .logo {
  width: 120px;
}

.site-nav-link {
  color: #FFFFFF;
  text-decoration: none;
}

.site-nav-link-active {
  color: #FF6600;
  text-decoration: none;
}

/* Site Footer */
.footer {
  padding: 30px 30px 60px;
}

.footer-section {
  margin-bottom: 15px;
}

@media(min-width: 720px) {
  .footer-section {
    margin-bottom: 0;
  }
}

.footer .logo {
  margin-bottom: 5px;
  width: 100px;
}

.footer a  {
  color: #959595;
  text-decoration: none;
}

.footer p  {
  margin-bottom: 5px;
}

.footer-email-input {
  margin-right: 2.5%;
  width: 68% !important;
}

.footer-email-button {
  font-size: 12px !important;
  padding: 10px !important;
  width: 27.5% !important;
}

@media(min-width: 768px) {
  .footer-email-input {
    width: 57% !important;
  }

  .footer-email-button {
    width: 37.5% !important;
  }
}

/* 5. Component Styles
======================================== */
.alert {
  border-radius: 3px;
  margin-bottom: 15px;
  padding: 10px 15px;
  text-align: left;
}

.alert-content {
  align-items: center;
  display: flex;
}

.alert-error {
  background-color: #FC472E;
}

.alert img {
  display: inline-block;
  height: 15px;
  margin-right: 5px;
  width: 15px;
}

.alert p {
  color: #FFFFFF;
  display: inline-block;
  margin-bottom: 0;
}

.button {
  border-radius: 3px;
  color: #FFFFFF;
  display: inline-block;
  font-family: 'Roboto', Helvetica, sans-serif;
  font-size: 16px;
  font-weight: 700;
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
  background-color: #00CF63;
}

.button-secondary {
  background-color: #FFAA00;
}

.button-full {
  width: 100%;
}

.button-small {
  font-size: 13px;
  padding: 10px 30px;
}

.card {
  background-color: #FFFFFF;
  border-radius: 10px;
  box-shadow: 0 0 40px 2px rgba(0, 0, 0, 0.1);
  padding: 30px 30px 15px;
}

.chip {
  display: flex;
  align-items: center;
}

.chip-img-container {
  border-radius: 30em;
  float: left;
  margin-right: 15px;
  overflow: hidden;
  height: 60px;
  width: 60px;
}

.chip-content-container {
  float: left;
}

.chip-content-title {
  margin-bottom: 0;
}
.chip-content-description {
  color: #8F9196;
  margin-bottom: 0;
}

input,
select,
textarea {
  background-color: #FFFFFF;
  border: 1px solid #F2F3F5;
  border-radius: 3px;
  box-shadow: inset 1px 1px 3px 0 rgba(189,191,192,0.10);
  height: 35px;
  margin-bottom: 15px;
  padding: 10px;
  transition: border-color 0.5s ease;
  width: 100%;
}

input[type="submit"] {
  cursor: pointer;
  height: auto;
  width: auto;
}

input:active,
input:focus,
textarea:active,
textarea:focus {
  border: 1px solid #42A5F5;
  outline: none;
}

textarea {
  height: 100px;
}

.input-error {
  border-color: #FC472E;
}

/* 6. Page Styles
======================================== */
.site-main {
  padding: 60px 15px;
  position: relative;
}

.site-main-background {
  background-color: #34474F;
  height: 600px;
  display: block;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: -1;
}

.site-main-header {
  margin-bottom: 60px;
}

.site-main-header h1,
.site-main-header p {
  color: #FFFFFF;
}

.section-header {
  font-size: 23px;
  line-height: 33px;
  margin-bottom: 15px;
}

.location-details li {
  display: block;
  margin-top: 15px;
}
```
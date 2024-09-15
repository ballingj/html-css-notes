METADATA
Language:: CSS
Sub-concepts:: Improved Styling with CSS

Summary:: Styling Links and buttons as well as insights on purpose and useability of designing this interactive items.


---
 
# Links and Buttons
### Signifiers

In the field of user interface design, signifiers are indicators that offer clues about how to interact with new objects or situations.

### The User Agent Stylesheet

The user agent stylesheet is a set of default styles included in the browser for use on all web pages.

### Links and Button Behavior

Links and buttons should exhibit the same behavior across different browsers to consistently maintain the same experience for all users.

### Link States

In a browser, links have four main states:
- Normal (not clicked)
- Hover
- Active (clicked)
- Visited

These four states have associated [CSS pseudo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes): `:link`, `:hover`, `:active`, and `:visited`
The proper order of these rules is:

- `:link`
- `:visited`
- `:hover`
- `:active`
### Link Styles

Links should be styled in a different way from their surrounding text.
By default, links appear blue and underlined in contrast to the surrounding black text.

### Anchor Text

Anchor text is the text inside of a link and is descriptive of the linked resource.
It improves:

- Usability
- Accessibility
- Search engine optimization

### The ‘title’ Attribute

The `title` attribute can be provided to any HTML element.
This attribute is used for additional context or advisory text for clickable elements.

```CSS
<p>  <a href="https://www.codecademy.com" title="Codecademy is an online learning platform">Codecademy</a> is the best place to learn to code!</p>

```

### Tooltips

A tooltip is a descriptive box which contains the text of an element’s `title` attribute and appears near the user’s cursor.

### The `:hover` CSS Pseudo-Class

The CSS pseudo-class `:hover` is used to style an element when the mouse cursor hovers over it.
```css
a {
	color: blue;
}

a:hover {
	color: orange;
}
```

### The CSS `cursor` Property

The CSS `cursor` property is used to change the appearance of the mouse cursor when hovering over an element.
```css
a {  cursor: pointer;}
```

### Skeuomorphism

Skeuomorphism is the concept of replicating or imitating real-life counterparts with UI elements.

### Flat Design

_Flat design_ is an alternative approach to skeuomorphism that embraces the fact that computer interfaces do not necessarily need to model real-life interfaces. As users grow more familiar with digital displays and interfaces, designers have felt less need to model physical interactions and instead rely on other signifiers to indicate interactive elements. To generalize, flat design uses simplicity and lack of clutter for its UI elements.

### Button Skeuomorphic Styling
https://codepen.io/ballingj/pen/eYxwdXQ

A `<button>` element can incorporate skeuomorphic styling for a realistic 3D appearance.
When pressing the button, a texture change may occur to make the button appear to flatten and pop back up when released.

```css
button {
  height: 50px;
  width: 200px;
  cursor: pointer;
  font-weight: 600;
  font-size: 15px;
}

.skeuomorphic {
  border: 2px solid #0c960c;
  border-radius: 5px;
  color: #F8F8F8;
  box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.2), 0px -2px 2px rgba(255, 255, 255, 0.5) inset, 0 2px 2px rgba(255, 255, 255, 0.8) inset;
  background: linear-gradient(#1D1, #0ebc0e);
  text-shadow: 0 -2px #0c960c;
}

```
![[skeumorphic-btn.png]]

### Button Flat Styling
https://codepen.io/ballingj/pen/gOqNwyg
A `<button>` element can incorporate flat styling for a simple 2D effect.
When pressing the button, a color change may occur as a signifier that the button has been pressed.
```css
.flat {
  background-color: #1D1;
  color: #fff;
  border: 2px solid #12dd23;
  border-radius: 10px;
}

```
![[Flat-btn.png]]
### Button Hover State

A button can have a hover state that changes the appearance of a cursor when it is directly over the button.

```css
.skeuomorphic:hover {
  box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.1), 0px -2px 2px rgba(255, 255, 255, 0.25) inset, 0 2px 2px rgba(255, 255, 255, 0.4) inset;
  background: #0ebc0e;
  background: linear-gradient(#0ebc0e, #0c960c);
  border-color: #064f06;
}

.flat:hover {
  background-color: #0c960c;
  transition: background-color .15s, font-size .15s;
  font-size: 18px;
}
```

##### Mobile Device Hover State
The hover state of buttons and links do not apply to mobile devices due to the lack of a cursor. 

### Button Active State

A button has an active state when it is being pressed.  The styling goes away as soon as the button is no longer being pressed.

```css
.skeuomorphic:active {
  margin-top: 2px;
  margin-bottom: -2px;
  box-shadow: 0px 2px 2px rgba(63, 63, 63, 0.1), 0px -2px 2px rgba(255, 255, 255, 0.25) inset, 0 2px 2px rgba(255, 255, 255, 0.4) inset;
  background: #0c960c;
  background: linear-gradient(#0c960c, #0ebc0e);
}

.flat:active {
  border-color: #fff;
}
```


#### Key Concepts

improve usability:

1. Added styles to make links recognizable and distinguishable from ordinary text.
2. Added link styles that depend upon mouse interaction state, providing users with visual feedback for cursor hovering and mouse clicks.
3. Added additional context text with the HTML `title` attribute.
4. Styled buttons to be easily recognizable (in both skeuomorphic and flat design styles) using box shapes, border, hover, and active states.


Bonus Article:
# Affordances, Signifiers, and Clickability

This article covers the design concepts of affordances and signifiers as well as some of their applications in web design.

## Clickability

For users on the web, the mouse click is perhaps the most fundamental human-computer interaction. The web _became_ the web partially through the power of _hypertext_, or text in one document that links to other documents or resources. To this day, users navigate the web largely through mouse clicks (and finger taps on mobile and tablet devices).

## Affordances

Objects _afford_ the ability of users to interact with them in various ways. For instance, a bench affords a person the ability to sit on it, but if it is not affixed to the ground, it also affords the user the ability to turn it over, throw (if the user is physically able), or perform any number of other actions. Even though the designer was probably not designing the bench with throwing in mind as the primary user behavior, the object still affords this action. Potentials for interaction are collectively called the _affordances_ of an object.

## Signifiers

_Signifiers_ are aspects of an object that a designer uses to indicate potential and intended affordances of an object. For example, a teacup with no handle affords the ability to lift it and drink out of it. But designers and potters often add handles to _signify_ that users can and should lift up the object and take a sip. The handle is an example of a common _user experience pattern_.

## UX Patterns

User experience (UX) patterns establish reusable solutions to common problems. Handles are ubiquitous—they are used on objects of all shapes, sizes, and purposes to indicate that users can initiate an action by grabbing the handle with their hand(s).

## Affordances and Signifiers in Web Design

In computer interactions, the possible affordances of any computer are usually relatively limited. Consider a web application in a browser—a user can essentially click, execute key commands or type, and potentially execute touch events or voice commands. Because of the relatively limited range of affordances, using proper signifiers is especially important to direct users properly. Users can click anywhere on a page, but not every click will have a result. Often, websites and applications use a combination of visual feedback and common UX patterns to help solve this issue. In web browsers, one common example of visual feedback is the cursor image itself: it can demonstrate what behavior might be expected from a click: a pointing hand indicating that an interaction will occur, an i-beam shape indicating that text can be selected, a four-directional arrow showing that an element can be moved, and [many more cursor styles and interactions](https://developer.mozilla.org/en-US/docs/Web/CSS/cursor).

As stated above, the hovering, pointing hand cursor is a nearly universal pattern to indicate that an element or text is clickable. But users do not want to hover a cursor over every element to determine if it is clickable, and mobile devices do not even have the ability to hover a cursor! For this reason, designers also use signifiers to demonstrate elements that afford interaction. On the web, these signifiers come in the form of CSS styles that differentiate clickable from non-clickable elements. A ubiquitous example is the styling of hyperlinks—hyperlinks should be easily differentiated from other text in a block by different colors, underline styles, or font weights.

There is no universal “right answer” to the issues surrounding signifiers and affordances on the web, but web designers should always keep these ideas in mind while creating web designs and interfaces.

## Further Reading

- [Signifiers, Not Affordances](https://jnd.org/signifiers-not-affordances/) by Don Norman. This article discusses a bit of the history of thought around affordances and signifiers, and their importance in design.
- [UI Patterns.com](http://ui-patterns.com/) has many examples of solutions to common design patterns in web design.

Want to learn more? Check out our [courses on web design](https://www.codecademy.com/catalog/subject/web-design).
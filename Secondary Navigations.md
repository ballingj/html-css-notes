METADATA
Language:: CSS
Sub-concepts:: Improved Styling with CSS

Summary:: Notes and codes on Breadcrumbs


---
# Secondary Navigation 

#### What is primary vs secondary navigation?

- The primary navigation system typically contains the most important links and buttons that need to be displayed on every single page of the site.
- Secondary navigation, or breadcrumb navigation, usually consists of a clickable list of pages or attributes that led to the current page. It can help users understand the extent of the site and also where they are currently.

For example, a shopping site may have a breadcrumb trail leading to a pair of shoes like so: 
![[UI_breadcrumb.svg]]
##### Why do we call them breadcrumbs?

Think about the story of Hansel and Gretel, where the kids drop breadcrumbs as they walked in the woods so that they would be able to find their way back.

##### Benefit of using breadcrumbs

Breadcrumb navigation provides a lot of benefits for users that come to random pages in a website through direct links or search results. Even if they enter to a seemingly random page on our site, they already have an idea of where they are in the website. The breadcrumb also hints at the extent of the site. For the example above, users could safely assume the site had shoes for other categories, shoes in different styles, and shoes in more colors.

Breadcrumbs also provide a way for a user to quickly jump backward in their navigation of the site. For example, if a user wanted to browse another style of shoe, they could click directly on the “Shoes” page and navigate to their desired style. Without the breadcrumbs, they would likely need to click “back” twice in their browser or start their search over from the home page.

The decision to use breadcrumbs is a judgment call depending on the type, depth, and complexity of your site.

```HTML
<html>
<link rel="stylesheet" type="text/css" href="./styles.css">

<ul class="breadcrumb">
  <li>
    <a href="shopping">Shopping</a>
  </li>
  <li>
    <a href="fashion">Fashion</a>
  </li>
  <li>
    <a href="shoes">Shoes</a>
  </li>
  <li>
    <a href="flats">Flats</a>
  </li>
  <li>
    <a href="brown">Brown</a>
  </li>
</ul>

</html>
```

```css
.breadcrumb > li {
  display: inline;
}

.breadcrumb li+li::before {
  padding: 10px;
  content: ">"
}

.breadcrumb a {
  text-decoration: none;
}

.breadcrumb a:hover {
  color: red;
}
```

Result:
![[simple_breadcrumb.png]]

### Where do Breadcrumbs Lead

In the previous examples, if you clicked on any of the breadcrumbs, it wouldn’t take you to a new page. This is because we have set `href="#"`. With this value, a click on the link will cause the page to scroll to the top of the current page.

In a full site, these breadcrumbs would link to their respective pages. This is accomplished by setting the `href` property to the appropriate page.

Since breadcrumbs are typically relative to the current page, the breadcrumb list on each page needs to be different. However, as a user moves around the breadcrumb list, they should expect the breadcrumb style and list to stay consistent.

For example, if the breadcrumb list was:
`Fashion > Shoes > Flats > Brown`

and a user clicked on “Flats”, the breadcrumb list on that page should look like:
`Fashion > Shoes > Flats`

It would be confusing for a user if the categories or order of them changed like:
`Shoes > Shopping > Flats`

#### More Samples:
In the code below, we’ve included the page “Singapore Hotels”. 

The first step is to create an HTML unordered list within **index.html** below the jumbotron div. The list should have the class of `"breadcrumb"` and the list items should be “Asia”, “Singapore”, “Tourism”, and “Hotels”.

For now, set the breadcrumb items to link to `"#"`.
```html
<body>
    <div class="jumbotron">
      <h1>Hotels In Singapore</h1>
    </div>

<ul class="breadcrumb">
    <li>
      <a href="#">Asia</a>
    </li>
    <li>
      <a href="#">Singapore</a>
    </li>
    <li>
      <a href="#">Tourism</a>
    </li>
    <li>
      <a href="#">Hotels</a>
    </li>
  </ul>
```

Add CSS to **breadcrumb.css** to configure the display of the breadcrumbs. (We’ve already added a bit of CSS to remove some of the existing styling within **style.css**).

You can style the breadcrumbs how you like, but at a minimum, it should set the `.breadcrumb li` elements to `display: inline;` and you should use the `.breadcrumb li+li::before` selector to insert a “>” between the items.
```css
body{
    padding:0px;
    margin: 0px;
    background-color: #1E1E24;
    text-align: center;
}

.jumbotron{
    background-image:url(https://images.unsplash.com/photo-1444882158336-bcfbd9298309?dpr=1&auto=format&crop=entropy&fit=crop&w=1500&h=1000&q=80&cs=tinysrgb);
    height: 200px;
    background-position: bottom center;
}

h1{
    color:#ffffff;
    font-family: 'Ruda', sans-serif;
    font-size: 70px;
    font-weight: 900;
    margin: 0px;
    padding-top: 20px;
    text-align: center;
    text-transform: uppercase;

}.breadcrumb li {
  display: inline;
}

.breadcrumb li+li::before {
  content: ">";
  color: #fff;
}
```

![[breadcrumb-asian-hotels.png]]

The example below makes use of a couple of CSS tricks to create an arrow effect. We’re using the `::before` and `::after` pseudo-elements to add filled rectangles (with empty content) before and after each list item:
```css
.breadcrumb {
  text-align: left;
}
  
.breadcrumb li {
  float: left;
}
 
.breadcrumb a {
  color: #fff;
  background: darkcyan;
  text-decoration: none;
  position: relative;
  height: 30px;
  line-height: 30px;
  text-align: center;
  margin-right: 15px;
  padding: 0 5px;
}
  
.breadcrumb a::before,
.breadcrumb a::after {
  content: "";
  position: absolute;
  border-color: darkcyan;
  border-style: solid;
  border-width: 15px 5px;
}
  
.breadcrumb a::before {
  left: -10px;
  border-left-color: transparent;
}
  
.breadcrumb a::after {
  left: 100%;
  border-color: transparent;
  border-left-color: darkcyan;
}
  
.breadcrumb a:hover {
  background-color: blue;
}

.breadcrumb a:hover::before {
  border-color: blue;
  border-left-color: transparent;
}

.breadcrumb a:hover::after {
  border-left-color: blue;
}
```

![[breadcrumbs-arrowed.png]]
### Breadcrumb Types

There are three major types of breadcrumbs:
- Location
- Attribute
- Path

You’ve seen the first two types in our examples so far.

**Location** based breadcrumbs are based on where you are with respect to the navigation structure of the website. In our previous shoe shopping example, the first three `li` elements are location based. We are in the “shoes” section of the website, which is contained within the “fashion” section, which is contained within the “shopping” section.

**Attribute** based breadcrumbs are based on the attributes of the page or product that you are browsing. In our previous example, the final two `li` elements are attribute based. We are shopping for shoes that are “flats” and “brown”. Since the order of these attributes is not prescriptive, you’ll see some sites display these at the same level in the UI. If you want to allow users to remove attributes, provide an (x) button or similar to indicate they can be removed.

Finally, breadcrumbs can be based on a user’s unique **path** through the site. For example, if they landed on the home page, browsed to the about page and finally the registration page, their breadcrumb trail may look like:

`Home > About > Register`

Note that this breadcrumb trail will be different for each user and each visit. For even mildly complex sites, the number of steps will become large. To simplify the display, the beginning of the trail is often abbreviated:

`... > About > Register`

```html
<body>
    <div class="jumbotron">
      <h1>Hotels In Singapore</h1>
    </div>
    <ul class="breadcrumb">
      <li class="location"><a href="">...</a></li>
      <li class="location"><a href="">Hotels</a></li>
      <li class="attribute"><a href="">Pets</a></li>
      <li class="attribute"><a href="">Queen Bed</a></li>
    </ul>
```

```css
.breadcrumb {
  text-align: left;
}
.breadcrumb li {
  display: inline;
}
/* Modify the CSS to only put the “>” character between location based breadcrumbs. */
.breadcrumb li.location+li.location::before {
  color: gray;
  content: ">";
}
.breadcrumb a {
  display: inline;
}

/* Color the “attribute” anchor tags gray to indicate that they are different than the “location” ones. */
.attribute a {
  color: gray;
}
/* Add a “close” indication using the :after pseudoselector: */
.attribute a::after {
  content: " x";
  font-size: 8px;
  vertical-align: super;
}
```
### Breadcrumb Pitfalls

Sometimes it is not appropriate to use breadcrumbs as a means of secondary navigation within a website. Users expect breadcrumbs to behave a certain way and attempts to deviate from this may confuse them. Most users are expecting breadcrumbs to expose the hierarchy of the site or display attributes of the page they are on.

Path based breadcrumbs are unique to a user’s journey and are not commonly implemented. Only use this type of breadcrumbs if there is a compelling reason for it.

While breadcrumbs are common, it is not the primary way users will navigate a site. Don’t make the breadcrumbs the only navigation structure.

In general, the rule of not adding anything extraneous to the design applies here. If the site only contains a few pages or if the pages in the breadcrumbs are already available through primary navigation, there is little reason to include breadcrumbs in the design.



METADATA
Language:: Design
Sub-concepts:: Text Design

Summary:: 


---
# Text Designs

### Introduction: Why do we care about text design?

One of the most fundamental ways a user is going to interact with your website is going to be through reading text. Their experience with this text will play a large role in dictating what they read, how they feel, and how likely they are to stay on your site. While the way we read and write text for websites is somewhat different than how we might read and write text on other platforms, many of the same basic principles of typography apply.

The form of the text you choose is intimately connected to the purpose and function of your website. If you are designing an online marketplace, your use of text will be significantly different than it would be if you were designing an online blog.

#### What this lesson will cover:

In this lesson, you'll learn how to effectively design and format text for digital content. We’ll start by discussing how we can differentiate text, then we will cover some basic text design principles, and then go into the details of how the users will engage with the text and how you can utilize this for the benefit of your website (or other digital media).

Consider the recipe website to your right. What does the text design tell you about this page? What’s easy to read? What’s hard to read? How can we improve it? As you progress through this lesson you will make various small improvements to this page to improve its usability, legibility, and impact.
### Differentiating Text: HTML Headers

Accept it now, no user is ever going to read every sentence on your website. It’s your job as the designer to make sure the user can easily distinguish what they want to read and what they can skip. Differentiating important pieces of text, such as titles and subtitles, is an effective way of achieving this.

You can guide a user through your site by creating contrast with headings, subheading, and lists (ordered or unordered).

As a best practice, the following HTML elements are used to differentiate text into categories:

- `<h1>` — Used for titles.
    - You should only have one header this style per page.
- `<h2>` — Used for headings.
    - This should be to identify major sections you want the user to immediately be drawn towards.
- `<h3>` — Used for subheadings.
    - This should be used for smaller focal points, such as articles, that you want the user to notice when scanning the page.

  
These tags will create a **visual hierarchy** that is very clear and familiar to your user (and therefore very learnable), and it will also stop you from writing paragraph after paragraph. Use HTML tags to remind yourself to be concise, and break things into lists and headings whenever possible.

Make sure that headings are closer to the content that they are introducing than the content that they come after. They do not provide clear visual organization if they are equidistant from both settings.

### Differentiating Text: Fonts

Fonts also play a useful role in differentiating text when used sparingly. It is effective to have a different font for a page title, and perhaps a third font for certain subheaders. But be warned, if you differentiate each paragraph with a new font or have a different font for every level of header your page will quickly become muddled and hard to read.

It often works well to have most of your text in a serif font, and then create contrast with headings or subheadings in a sans-serif font, but this can vary based on how you’d like the page to be styled. The most important thing is that the fonts you have complement each other appropriately.

In addition to fonts and headers, you can contrast between different pieces of text in a number of ways:

- style
- size
- weight
- color

A good rule is that if you find yourself using more than three different fonts on one page, maybe it’s time to try fewer fonts but other sources of visual contrast with text.

### Whitespace

The whitespace on your page is just as important to the text design of your site as the text itself. Without proper spacing and balance, your text can be rendered virtually illegible.

A website is like a room, the user needs to be able to move through it easily. And just like a room, it is important to keep it tidy and free of clutter. This is the power of whitespace. Good whitespace allows you to increase the legibility of your text, helps prevent users from skimming over elements, and serves as an unintrusive boundary between different sections of the page, without actually being there.

It’s just like standing in line at the store. You don’t want to be breathing down the neck of the person in front of you, it’s not comfortable for anyone! It’s the same with text, you don’t want your title crowded out by your subheaders, and you don’t want that paragraph invading the personal space of the nearby image.

### Instructions

1. Our recipe site is severely lacking in whitespace and many of the elements feel very cramped together.
	
	Let’s add some whitespace to the header. Add `margin-bottom: 30px;` to `.site-main-header`.

1. That seems to have added some whitespace underneath our header, but it is still too close to the top navigation bar and the logo. The sides also feel a little cramped.

	We can adjust both of these whitespaces at once by changing the styling of `.site-main`.
	
	Add 30 pixels of vertical padding and 15 pixels of horizontal padding to `.site-main`.
	
1. There is little distinction between the Popular Recipes. Let’s try to add some using whitespace.
	
	In `.recipe-preview`, increase `margin-bottom` to 60 pixels.

### Text Readability

It should be a pleasant experience for users to read the text on your website. Here are some easy ways to accomplish this:

- Make sure that your text is big enough (over 16px).
- Have a strong contrast between the foreground and the background.
- Make sure there is enough space between lines and letters (remember, whitespace is king!)

  
How can we adjust whitespace within the text?

### Line Spacing

Line spacing, also known as _Leading_, refers to the distance between two lines of text. Adjusting this value has a huge impact on the legibility of your site.

![image showing 3 paragraphs, one with good leading, one with too much leading, and one with cramped leading](https://content.codecademy.com/courses/learn-text-design/text%20design%20diagram%20leading.svg)

### Tracking

Similar to kerning, a way to make your text more readable is to adjust the _tracking_ of the letters. _Tracking_ is the space between the letters **and** the words. If you have too little tracking, the words will appear cramped, so by increasing tracking slightly, you make your text significantly more legible.

![image showing 3 paragraphs, one with normal tracking, one positive tracking, and one with negative tracking](https://content.codecademy.com/courses/learn-text-design/text%20design%20diagram%20tracking.svg)

### Kerning

_Kerning_ is the space between two letters in the text. You typically will not need to worry about kerning because a well-designed typeface already has optimal kerning built in. It is most important when you want to adjust the kerning in a title or header to achieve the design you want.

![image shows the words Space Exploration twice, once with no kerning, and once with metric kerning](https://content.codecademy.com/courses/learn-text-design/text%20design%20diagram%20kerning.svg)

### Instructions

1.  The text on the site feels a little cramped and is hard to read.

	In `styles.css` increase the `line-height` of all `p` elements to `23px`.

2. All of the headers are very hard to read and the tracking of the letters seems way off.

	Find the cause of this in `styles.css` and change the `letter-spacing` value to `1px`.

3. The cook time and prep time information feels a little more clustered than we’d like. Let’s add a little bit of whitespace around them to improve their readability.

	In `styles.css` add 26 pixels of line height to `.recipe-info-item`.


### Text Navigability

It’s also important for a user to immediately know how to navigate your text. It should be clear what they can click, and where it will take them.

- Stick to conventions about showing what is clickable (generally, links should be blue and underlined). Underlining links is less common now than a few years ago. It’s optional, but a nice courtesy to colorblind users.
- Never use blue as a general accent color for text, because your users will probably try to click on it no matter what.
- Having text on navigation buttons is important. It removes all uncertainty about what each button does.

  
Sticking to these simple rules will allow users to easily navigate your page and makes them more likely to stick around and experience the actual content of your site.

Also, it is important to think about the ways the user’s eyes will travel across your text. This will impact the way they navigate the page. If you organize the text into columns, the user’s eyes will likely not travel across the entire screen, they will travel to the end of a column and then down. Similarly, if you have long line lengths, the user’s eyes will spend more time traveling from left to right. We’ll cover this further in the next exercise.

##### Instructions
1.  It’s hard to tell which pieces of text are buttons that can be clicked on.

Let’s add in a background color to text buttons that link out to recipes.

Add the following code to `styles.css`:

```
.button-primary {  background-color: #E9BE53;}
```

2. In `index.html`, add `button-primary` styling to all of the “View Recipe” buttons, as well as the “View Rest of the Recipe” button and the “Submit” input in the “Featured” section.

There are five instances of these buttons in `index.html`:
- 3 “View Recipe” buttons
- 1 “View Rest of the Recipe” button
- 1 “Submit” button

### Text Length, Columns, and Line Length

The way users consume text on the internet is different from traditional text. As you read in the [_How Users Scan_](https://www.codecademy.com/article/how-users-scan) article before this course (or perhaps didn’t read) users rarely read web pages, especially if there are large blocks of text.

Because of this, you want to make it as easy as possible for a user to read your text. You may be used to writing paragraphs with 5 sentences when you were in school, but that’s too long! The average internet paragraph is only 1-3 sentences. It’s actually better to avoid sentences and paragraphs whenever possible and use a list instead.

### Line Length

Line length has a larger impact than you would expect on the reader. Each time a reader gets to a new line the mind is slightly energized and encouraged (“Typographie”, E. Ruder). But if the line lengths are too short, then the reader will be constantly taken out of the flow of the content by the quick succession of line breaks.

[Studies](https://www.usability.gov/get-involved/blog/2006/08/line-length-and-onscreen-reading.html) have shown that while users read longer line lengths faster, they actually prefer shorter line lengths and that they provide a better user experience.

Hitting a happy medium is key to having engaging text content. The best bet is to aim to have columns that contain roughly 50-75 characters per line. This will allow the reader to have the sensation of making good progress through the text without being continually interrupted by the line breaks.

Consider the following paragraph. Is it more readable in columns or as a single block? What are the advantages and disadvantages of both?

![two paragraphs, one formatted as a single block, the other broken up into two columns.](https://content.codecademy.com/courses/learn-text-design/text%20design%20diagram%20paragraph.svg)

There are several ways you can achieve this as a text designer. You can break up the site into columns, which can be effective for something like a news site, or you can reduce the lengths of your lines and then align the shorter text properly so it doesn’t impair the design of the site. The choice you make should depend on the purpose of your site.

##### Instructions
1. User usage data on `not much Thyme` has shown that users are skipping over the “Featured” section and not clicking to the recipe. Take a look at the section. Why do you think this might be?

Reduce the amount of text in the featured recipe description by removing all three of the displayed steps in the `index.html` file.

2. Now that you’ve removed the steps from the “Featured” section, change the text on the button so it says “View Recipe”.

### What Content will the Users Notice and Remember?

What do you want your users to take away from the text on your website? Would you rather they remember a description of where a product was built or would you rather they remember the benefits the product will give them if they buy it.

Where do you want the user’s eyes to immediately focus when they open the page? Would you rather they be drawn to the navigation bar at the top, or do you want them to immediately focus on the articles that are featured on the homepage.

As the designer, these are questions you will have to answer. There are several tools you can use to highlight the most important content.

#### Primacy and Recency

People will notice and remember the first and last elements of a list or a page better than anything in the middle of the list/page. This is known as **Primacy and Recency** effects. You can utilize this neurological behavior when organizing the text on your site to make sure that users remember what you want them to remember.

#### Image Pairing

Users eyes are easily drawn to images quicker than they are to text. You can utilize this by pairing important text with images whenever appropriate.

This pairing can be accomplished by grouping with card designs (putting them in a div together with a shared background color). This is a great way of adding visual appeal to your text.

It may be confusing to hear about images in a lesson on text design, but you cannot solely focus on text when you design your page. It is important to create a balance between the image and the text. You want the image to be able to draw the users eye to a section of the page, but you don’t want it to completely overshadow the text, which is ultimately what you want the user to consume.

##### Instructions
1. We want people to sign up for the weekly recipe email, but the current page design hasn’t successfully gotten many people to sign up.

	Locate where the box to sign up for the email is on the site. Its element in the HTML is
	
	```
	<div class="footer-section footer-section-right" aria-labelledby="email-subscription">
	```
	
	Primacy and Recency tell us that users are more likely to notice this element if we move it to the beginning or end of the page.
	
	In `index.html`, move the entire `<div>` element for the email signup into the `Site Wide Footer` section, right after
	
	```
	<nav role="navigation" class="clearfix">
	```
### F-Shaped Skimming

Notice that even leading long form magazines like the New Yorker have very visual landing pages. Every article has a photo or sketch associated with it, and rarely more than a one sentence preview. Users are happy to click through to get to the content they want, and they would prefer this to a cluttered homepage.

Take it a step further, look at the Amazon.com homepage. There is almost no text, and absolutely no full sentences(no periods in sight!) even though some of the headings have both a subject and a verb. When people are figuring out where to go on your site, they are just skimming to find what they want (even if what they want is a news article or a short story). You need to write and format your text with this skimmer in mind.

Recall the article from the previous unit, [_How Users Scan_](https://www.codecademy.com/article/how-users-scan). Users will scan content on the left of the screen before the right of the screen, and the top of the screen before the bottom of the screen. Our eyes jump back to the left of the screen whenever we finish reading a line. This creates an F pattern that the user’s eye follows, and is thus known as _f-shaped skimming_.

**Side note:** This is only true for languages that are read left to right: reverse it if you are designing a site that will be read in a language that goes right to left like Hebrew or Arabic.

##### Instructions
1.  Let’s take a look at the alignment of our recipe site. Does it properly cater to f-shaped skimming behavior?

	Not quite, all of the text in the popular recipes is aligned to the right side of a screen and a user skimming the page will likely pass right over it.
	
	Find `.site-main-section` in `styles.css` and change the text alignment to `left`.
### Review: Text Design Best Practices

In this lesson, you have learned that the way you design your text can have a huge impact on a users experience when browsing your site. Poor text design can make your site incomprehensible, and good text design can engage a user, make them more likely to buy something, and make them want to come back to your site.

You’ve learned that:

- Differentiating text is essential, and there are several ways to do this:
    - Use `<h1>`, `<h2>`, and `<h3>` header elements
    - Use 2-3 well-paired fonts, but no more.
    - Adjust font style, size, weight, spacing, and color.
- Whitespace plays a big part in readability. Make sure all of your text elements have enough whitespace.
- Use standard convention for links and navigation buttons so users know what to expect.
- Use columns when necessary to keep line length at around 50-75 characters.
- Use colored cards to pair images with important text so users’ eyes are drawn towards it.
- Have the elements you want users to notice at the top of the page, or down the left-hand side because those are the areas of the page users will notice when skimming.

If you keep all of these tips in mind when you are designing the text on your site, you will have a much higher chance of getting users to read your content and navigate your site correctly.


# Review: Fundamentals of Web Design

In this unit, you learned about the best user interface (UI) design practices to implement in CSS.

Congratulations! The goal of this unit was to introduce the fundamentals of web design. You learned about the best user interface (UI) design practices that you can implement in CSS.

Having completed this unit, you are now able to:

- Understand what wireframing is
- Make wireframes and designs that account for different devices and screen sizes
- Understand best UI practices, such as color theory and text design

If you are interested in learning more about these topics, here are some additional resources:

- Resource: [Adobe Color](https://color.adobe.com/create/color-wheel)
- Resource: [Cloud Flare Design](https://color.cloudflare.design)
- Resource: [Google Font Pairings](https://heyreliable.com/ultimate-google-font-pairings/)

Learning is social. Whatever you’re working on, be sure to connect with the Codecademy community in the [forums](https://discuss.codecademy.com/). Remember to check in with the community regularly, including for things like asking for code reviews on your project work and providing code reviews to others in the [projects category](https://discuss.codecademy.com/c/project/1833), which can help to reinforce what you’ve learned.
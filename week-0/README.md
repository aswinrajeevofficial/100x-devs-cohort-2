# Week 0 Notes

Starters:

* Tags
* Attributes
* Inline Styles (bg color, fonts, etc)
* JS Basics (data types, loops, functions)

Main Course:

* External styles (classes, IDs)
* Flexbox
* Connecting JS to HTML (selectors, DOMs)
* Chrome Dev Tools

1. What are browsers? How do they render websites? What purpose do HTML/CSS/JS serve?

    A browser, when it gets some HTML, should be able to interpret it and render the file to view by the end user. Where does it get it the HTML file from? When you type www.google.com into a browser, the Google server located somewhere in the world returns back the HTML file that is interpreted and rendered by your browser. The browser knows from the different elements present in the file, where to render, and how to render them.

    Any website, should be encapsulated within these three languages and it is what is known by the internet. Most practical websites need only these three languages to run. Any fancy looking website, Instagram, Facebook, LinkedIn, etc, can be written in pure HTML/CSS/JS, without the use of any frameworks. 

2. How much of this do we actually use in the industry? HTML (very minimal), CSS (minimal), JS (heavy) 

    There were a lot of websites that used raw HTML/CSS and JS to build websites. But since 2010, after the creation of frameworks/libraries like React/Vue/Angular, the amount of HTML and CSS written to build websites have come down a lot.

## HTML

* Specifies the structure of your website (where to place what)
* **Tags** - Used to define the structure 
  * Popular tags in HTML are:

    ```html
    <html> <head> <title> <body> <div> <span> <h1> <h2> <h3> <h4> <h5> <h6> <p> <img> <a> <input> <button> <b> <i> <center>
    ```

  * `<html>` - This tag specifies that it is an HTML document. All other tags are placed inside this one. If you don't add it to an HTML file, the browser injects the <html> tag for you.
  * `<head>` - The head tag is used to enter some metadata information. This is also automatically added to the HTML file if you don't add it yourself.
  * `<body>` - The body tag houses all your content. This is also automatically added to the HTML file if you don't add it yourself. The above three tags are used to structurally differentiate your HTML file at a high level.
  * `<title>` - It is one of the metadata tags that's added to your <head> tag. Whatever is inside the title tag is rendered as the title in your browser's tab. 
  * `<div>` - One of the most common tags used. It takes up one whole width of the page. It is called a block element. You can put multiple divs inside one another. 
  * `<span>` - Takes only the space the content inside it requires. It is called an inline element.
  * `<h1> - <h6>` - Used for headings. `<h1>` is level 1 heading, largest size. `<h6>` is the smallest. Used to change font sizes without using CSS.
  * `<p>` - Used to add content inside paragraphs. Note that text inside a `<div>`, `<span>`, or without any tags appear the same as using the <p> tag.
  * `<img>` - Used to add images to your HTML document. Syntax: `<img src="zerodha-landing.png"></img>`
  * `<a>` - Used to add links to your website. When clicking on an `<a>` tag, it takes you to the website that's configured. Syntax: `<a href="https://www.google.com">Go to Google</a>`. This will render text as "Go to Google" on your HTML page and when clicking on it, it opens up Google homepage. 
    * What if you want to open it in a new tab? Use the following syntax: `<a href="https://www.google.com" target="_blank">Go to Google</a>`
  * `<b>` and `<i>` - Content inside these tags appear **Bold** or *Italic*. You can also use it together.
  * `<button>` - Used to add a button to your HTML page. You can add several attributes to the button tag to make it "do" something when clicked. If you hover over a button, the mouse changes its cursor.
  * `<input>` - Used to accept input from a user. Simple syntax: `<input placeholder="Username" type="text"></input>`
  * `<center>` - Used to center the contents that are put inside it.
* **Attributes** - They are extra info added to a tag. For instance, the `<img>` tag had the `src` attribute, the `<a>` tag had the `href` attribute. You can add multiple attributes to a tag and it helps in defining what the tag must do.

## CSS

### Styles

* Lets you add styles to your website. Change colors, font sizes, background colors. Another big thing that CSS lets you do is position different HTML elements on your website.
* How to add styles? `<h1>Hi there</h1>` Change this to `<h1 style="color:red, background:green;">Hi there</h1>`. You can use the background style to set images/gradients/colors etc. But if you use the background-color style, you can only set the background color.
* Styles are added inside the `style` attribute separated by a semi-colon (`;`).
* Common styling attributes:
  * `color` - Gives a color to your textual content
  * `background` - Gives a border to your element
  * `border-radius` - Gives a rounded edge to the element. Syntax: `border-radius: 10px;`
  * `border` - Gives a border to the element. Syntax: `border: 2px solid black;` Gives a 2 pixel wide border with a solid black color. You can replace solid with dotted and a few other variants. Border width appears in between padding and margin.
  * `padding` - Give space all around the element. Padding is used to add space between the content and the edges of the element.
  * `margin` - Gives space all around the element. Margin is used to add space between the edge of the element and the outside of it. For both padding and margin you can use `padding-left, padding-right, padding-top, padding-bottom, margin-left, margin-right, margin-top, margin-bottom` to give specific values to particular sides.
  * `box-shadow` - Lets you add some shadow to your HTML element. Syntax: `box-shadow:2px 10px 10px black;` The first attribute is to move from right or left. Positive values are to move the shadow to right. Negative values are to move it to the left. The second value is to move the shadow from top to bottom. Positive values move it to the bottom, negative values move it to the top. The third value is for the spread. The last value is the color.
  * `font-size` - Sets the font size of the content inside your HTML element. Syntax: `font-size: 100px;`

### Positioning

* `float` - Float the element to the direction specified relative to the parent element.
* The best way to position elements is by using Flexbox. Floating elements is the old way of doing it. 
* `display: flex;` - This tells your browser to display all children elements side by side even if they are block elements. This is used on the parent container to mark it as flexbox. To position the children elements we use the `justify-content` attribute.
* `justify-content` - It tells where to position the children elements inside the flexbox container. It has several values:
  * `flex-start` - Positions it at the beginning. It is the default value.
  * `flex-end` - Positions it at the end of the screen.
  * `center` - Positions it at the center
  * `space-between` - Positions elements equally.
  * `space-around`
  * `space-evenly`

## Zerodha Landing Exercise - HTML/CSS Only

I've added some more CSS styles that were not discussed during the lecture for some additional pixel perfection.

![Zerodha landing page done using HTML and CSS only.](./project-1-zerodha-landing.png)
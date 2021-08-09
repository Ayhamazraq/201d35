# Layout 
 
* The simplest and most popular way of creating layouts is using HTML < table> tag. These tables are arranged in columns and rows, so you can utilize these rows and columns in whatever way you like.
 
**Key ConCepts in positioning eLements:**
1. Bulding block: CSS treats each HTML element as if it is in its own box. This box will either be a block-levelbox or an inline box.
2. containing element: If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element. 
* containing ElEmEnts: If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.It is common to group a number of elements together inside a < div>(or other block-level) element. For example, you might group together all of the elements that form the header of a site (such as the logo and the main navigation). The < div> element that contains this group of elements is then referred to as the containing element.
 
![containing element](https://slideplayer.com/16646897/96/images/slide_2.jpg)
 
**Controlling the Positin of Elemet**
CSS has the following positioning schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning. You specify the positioning scheme using the positionproperty in CSS. You can also float elements using the float property.
 
* normal flowEvery: block-level element appears on a new line, causing each item to appear lower down the page than the previous one. Even if you specify the width of the boxes and there is space for two elements to sit side-by-side, they will not appear next to each other. This is the default behavior (unless you tell the browser to do something else).
* relative Positioning: This moves an element from the position it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been placed. This does not affect the position of surrounding elements; they stay in the position they would be in in normal flow.
* Absolute Positioning: This positions the element in relation to its containing element. It is taken out of normal flow, meaning that it does not affect the position of any surrounding elements (as they simply ignore the space it would have taken up). Absolutely positioned elements move as users scroll up and down the page.
 
* To indicate where a box should be positioned, you may also need to use box offset properties to tell the browser how far from the top or bottom and left or right it should be placed. (You will meet these when we introduce the positioning schemes on the following pages.)
 
**normaL flow, position:static**
* In normal flow, each block-level element sits on top of the next one. Since this is the default way in which browsers treat HTML elements, you do not need a CSS property to indicate that elements should appear in normal flow, but the syntax would be: position: static; 
 
```
<body>  <h1>The Evolution of the Bicycle</h1>  <p>In 1817 Baron von Drais invented a walking        machine that would help him get around the        royal gardens faster...</p></body>c
```
```
body{ width: 750px;  font-family: Arial, Verdana, sans-serif;  color: #665544;}h1 {  background-color: #efefef;  padding: 10px;}p {  width: 450px;}
```
 
* clearing floats:
 
![clear floats](https://i.stack.imgur.com/6s48p.png)
 
**screen sizes**
* Different visitors to your site will have different sized screens that show different amounts of information, so your design needs to be able to work on a range of different sized screens.
 
* screen resoLution: Resolution refers to the number of dots a screen shows per inch. Some devices have a higher resolution than desktop computers and most operating systems allow users to adjust the resolution of their screens.
 
* Because screen sizes and display resolutions vary so much, web designers often try to create pages of around 960-1000 pixels wide (since most users will be able to see designs this wide on their screens).
 
* you will find information in [Layout](https://www.w3schools.com/html/html_layout.asp).
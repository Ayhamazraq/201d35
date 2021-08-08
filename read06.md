# Understanding The Problem Domain Is The Hardest Part Of Programming
 * What is the hardest thing about writing code?
* There are many common answers to this question:
 1. Learning a new technology.
 2. Naming things.
 3. Testing your code.
 4. Debugging.
 5. Fixing bugs.
 6. Making software maintainable.

 **Why problem domains are hard?**
 * Have you ever tried to put together a jigsaw puzzle that didn’t have any picture on it?  How about one like this one, that has a very similar pattern repeated on it and is double-sided? The reason why puzzles like this one are so hard, is because you can’t really see what you are trying to build very clearly.  Normally when you put together a jigsaw puzzle you follow steps that might look something like this:
 1. Figure out what the major components of the picture are.
 2. Sort the pieces by color or component.
 3. Put together all the border pieces.
 4. Put together each component of the picture from the piles you created.
* This all breaks down when you don’t have a picture with clear components that you can identify. The same thing happens when writing code.  Writing code is a lot like putting together a jigsaw puzzle.  We put together code with the purpose of building components that we have taken out of the “bigger picture” of the problem domain. The big issue is that many problem domains are like a puzzle with a blurry picture or no picture at all.

**Programming is easy if you understand the problem domain**
* A long time ago, I worked for Hewlett Packard writing software for multi-function printers. Most of the work at the time was basic waterfall development.  There wasn’t much Agile happening there—at least at the time I was there. There was however something really interesting about the waterfall approach and the extreme amount of specification that was done before anything was built—it was very easy to write the code for a feature.

* What can you do about it?
* If understanding the problem domain is the hardest part of programming and you want to make programming easier, you can do one of two things: 
1. Make the problem domain easier.
2. Get better at understanding the problem domain.
* You can often make the problem domain easier by cutting out cases and narrowing your focus to a particular part of the problem. What I mean by this is that it is often beneficial to take a part of the problem and fully understand that part before expanding the problem domain.
* for more information please visit [Understanding the problem domain](https://simpleprogrammer.com/understanding-the-problem-domain-is-the-hardest-part-of-programming).

## Object Literals
**WHAT IS AN OBJECT?**
* WHAT IS AN OBJECT? Objects group together a set of variables and functions to create a model of a something you would recognize from the real world. In an object, variables and functions take on new names. IN AN OBJECT: VARIABLES BECOME KNOWN AS PROPERTIES If a variable is part of an object, it is called a property. Properties te ll us about the object, such as the name of a hotel or the number of rooms it has. Each individual hotel might have a different name and a different number of rooms. IN AN OBJECT: FUNCTIONS BECOME KNOWN AS METHODS If a function is part of an object, it is called a method. Methods represent tasks that are associated with the object. For example, you can check how many rooms are available by subtracting the number of booked rooms from t he total number of rooms.
**CREATING· OBJECTS USING LITERAL NOTATION**
* This example starts by creating an object using literal notation. This object is called hotel which represents a hotel called Quay with 40 rooms (25 of which have been booked). Next, the content of the page is updated with data from this object. It shows the name of the hotel by accessing the object's name property and the number of vacant rooms using the checkAvail ability() method.
```
var hotel  =  { name: 'Quay', rooms: 40, booked:  25, checkAvailability: function() { return this.rooms -this.booked; } } ; JAVASCRIPT var el Name = document. getElementByld('hotelName'); elName.textContent =hotel .name; var elRooms = document.getElementByid{'rooms'); elRooms.textContent = hotel.checkAvailability(); 
```
**CREATING MORE OBJECT LITERALS** 
* Here you can see another object. Again it is called hote 1, but this time the model represents a different hotel. For a moment, imagine that t his is a different page of the same travel website.

```
var hotel = { name: 'Park', rooms : 120, booked:  77, c03/js/ object- l iteral2.js checkAvailability:  function() { return this.rooms  -th i s.booked; } } ; var elName = document. getElementByid('hotelName'); elName. textContent =hotel.name; var elRooms = document. getElementByid(' r ooms'); e 1 Rooms. text Content = hote 1 . checkAvai l a  bility(); 
```

### Document Object Model
* The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is  in the browser window.
**THE DOM TREE IS A MODEL OF A WEB PAGE**
* As a browser loads a web page, it creates a model of t hat page. The model is called a DOM t ree, and it is stored in the browsers' memory. It consists of four main types of nodes.  
* THE DOCUMENT NODE: Above, you can see the HTML code for a shopping list, and on the right hand page is its DOM tree. Every element, attribute, and piece of text in the HTML is represented by its own DOM n ode. At the top of the tree a document node is added; it represents the entire page (and also corresponds to the document object, which you first met on p36). When you access any element, attribute, or text node, you navigate to it via the document node. It is the starting point for al l visits to the DOM tree. 
* ELEMENT NODES HTML elements describe the structure of an HTML page. (The < hl > -< h6> elements describe what parts are headings; the < p> tags indicate where paragraphs of text start and finish; and so on.) To access the DOM tree, you start by looking for elements. Once you find the element you want, then you can access its text and attribute nodes if you want to. This is why you start by learning methods that allow you to access element nodes, before learning to access and alter text or attributes.
* Each node is an object with methods and properties. Scripts access and update this DOM tree (not the source HTML file). Any changes made to the DOM tree are reflected in  the browser.
* DOM TREE:

![Dom tree](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/DOM-model.svg/1200px-DOM-model.svg.png)

* ATTRIBUTE NODES: attribute I text The opening tags of HTML elements can carry attributes and these are represented by attribute nodes in the DOM tree. 
* TEXT NODES: Once you have accessed an element node, you can then reach the text within t hat element. This is stored in its own text node.
**WORKING WITH THE DOM TREE**
* Accessing and updating the DOM tree involves two steps:
 1. Locate the node that represents the element you want to work with. 
 2. Use its text content, child elements, and attributes. 

 **SELECTING ELEMENTS USING ID ATTRIBUTES** 
 * HTML

 ```
 <hl id="header">List King<lhl> <h2>Buy groceries<lh2> <ul> <li id="one" class="hot"><em>fresh<lem> figs<lli> <li id="two" class="hot">pine nut s<lli> <li id="three" class="hot">honey<lli> <li id="four">balsamic vi negar<lli> </ul> 
 ```
 * JavaScript

 ```
 Select the element and store it in a  variable. var el = document.getElementByid('one'); II Change the value of the class attribute. el.className ='cool' ; 
 ```
 * EXAMPLE DOCUMENT OBJECT MODEL:

 ```
 var list Items = document.querySelectorAl l (' l i '); /!All <li>  elements //ADD A CLASS OF COOL TO ALL LIST ITEMS var i; for (i = 0; i  < listltems. length; i++) { listltems[i] .className = 'cool'; } //Counter variable // Loop through elements //Change class to cool //ADD NUMBER OF ITEMS IN THE LIST TO THE HEADING var heading= document. querySelector('h2'); // h2 element // h2 text var headingText = heading.firstChild.nodeValue; var totalltems = listitems.l ength; //No. of <li> elements + '</span>';// Content //Update h2 var newHeading = headingText + '<span>' + totalitems heading.textContent = newHeading; 
 ```
 **Summarization:**
 1. The browser represents the page using a DOM tree.
 2. DOM trees have four types of nodes: document nodes, element nodes, attribute nodes, and text nodes.
 3. You can select element nodes by their id or cl ass attributes, by tag name, or using CSS selector syntax.
 4. Whenever a DOM query can return more than one node, it will always return a Nadel i st. 
 5. From an element node, you can access and update its content using properties such as textContent and i nnerHTML or using DOM manipulation techniques.
 6. An element node can contain multiple text nodes and child elements that are siblings of each other.
 7. In older browsers, implementation of the DOM is inconsistent (and is a popular reason for using jQuery). 
 8. Browsers offer tools for viewing the DOM tree . 
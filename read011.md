# Images 
* Controlling the size and alignment of your images using CSS keeps rules that affect the presentation of your page in the CSS and out of the HTML markup.
* You can also achieve several interesting effects using background images. In this chapter you will learn how to:
1. Specify the size and alignment of an image using.
2. Add background images to boxes.
3. Create image rollovers in CSS.
 
* controllIng sIzes of Images In css:
![ImageSize](https://slideplayer.com/slide/15265880/92/images/3/CONTROLLING+SIZES+OF+IMAGES+USING+CSS.jpg)
 
* You can control the size of an image using the width and height properties in CSS, just like you can for any other box. Specifying image sizes helps pages to load more smoothly because the HTML and CSS code will often load before the images, and telling the browser how much space to leave for an image allows it to render the rest of the page without waiting for the image to download.
 
## aligning Images Using css 
* In the last chapter, you saw how the float property can be used to move an element to the left or the right of its containing block, allowing text to flow around it.Rather than using the < img>element's align attribute, web page authors are increasingly using the float property to align images. There are two ways that this is commonly achieved:
1. The float property is added to the class that was created to represent the size of the image (such as the small class in our example).
2.  New classes are created with names such as align-left or align-right to align the images to the left or right of the page. These class names are used in addition to classes that indicate the size of the image.
 
* background-position: 
* When an image is not being repeated, you can use the background-positionproperty to specify where in the browser window the background image should be placed. This property usually has a pair of values. The first represents the horizontal position and the second represents the vertical.
### Css3: gradIents background-image
* CSS3 is going to introduce the ability to specify a gradient for the background of a box. The gradient is created using the background-image property and, at the time of writing, different browsers required a different syntax.Since it is not supported by all browsers, it is possible to specify a background image for the box first (which would represent the gradient) and then provide the CSS alternatives for browsers that support gradients.
 
* example Images:
```
<!DOCTYPE html><html>  <head>      <title>Images</title>      <style type="text/css">   body {color: #665544;background-color: #d4d0c6;background-image: url("images/backdrop.gif");font-family: Georgia, "Times New Roman", serif;text-align: center;}.wrapper {width: 720px;margin: 0px auto;}.header {margin: 40px 0px 20px 0px;}.entry {width: 220px;float: left;margin: 10px;height: 198px;background-image: url("images/shadow.png");background-repeat: no-repeat;background-position: bottom;}figure {display: block;width: 202px;height: 170px;background-color: #e7e3d8;padding: 9px;text-align: left;}figure img {width: 200px;height: 150px;border: 1px solid #d6d6d6;}figcaption {background-image: url("images/icon.png");padding-left: 20px;background-repeat: no-repeat;}      </style>
``` 
* summary :
* You can specify the dimensions of images using CSS. XThis is very helpful when you use the same sized images on several pages of your site.Images can be aligned both horizontally and vertically Xusing CSS.You can use a background image behind the box Xcreated by any element on a page. 
 
### Practical information:
* To wrap up the book we are going to look at some practical information that will help you launch a successful site.
 
* There are entire books written about each of the topics covered in this chapter but I will introduce you to the key themes that each subject deals with and give you pointers for what you need to be considering. You will see:
1. The basics of search engine optimization.
2. Using analytics to understand how people are using your ●site after it has launched.
3. Putting your site on the web.
 
* search engine oPtimization (seo):
* SEO is a huge topic and several books have been written on the subject. The following pages will help you understand the key concepts so you can improve your website's visibility on search engines. 
1. the Basics: Search engine optimization (or SEO) is the practice of trying to help your site appear nearer the top of search engine results when people look for the topics that your website covers.
2. on-Page techniques: On-page techniques are the methods you can use on your web pages to improve their rating in search engines.
3. off-Page techniques: Getting other sites to link to you is just as important as on-page techniques. Search engines help determine how to rank your site by looking at the number of other sites that link to yours.
![seo](https://wordstream-files-prod.s3.amazonaws.com/s3fs-public/images/media/images/on-page-seo-versus-off-page-seo-visual.jpg)
Visit [Practical Information](https://www.oreilly.com/library/view/html-css/9781118206911/25_chapter-19.html).
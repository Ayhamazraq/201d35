

# Transforms
With CSS3 came new ways to position and alter elements. Now general layout techniques can be revisited with alternative ways to size, position, and change elements. All of these new techniques are made possible by the transform property.

The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

Within this lesson we’ll take a look at both two-dimensional and three-dimensional transforms. Generally speaking, browser support for the transform property isn’t great, but it is getting better every day. For the best support vendor prefixes are encouraged, however you may need to download the nightly version of Chrome to see all of these transforms in action.

# Transform Syntax.

The actual syntax for the transform property is quite simple, including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.

    div {
    -webkit-transform: scale(1.5);
        -moz-transform: scale(1.5);
        -o-transform: scale(1.5);
            transform: scale(1.5);
    }

  #  2D Rotate
The transform property accepts a handful of different values. The rotate value provides the ability to rotate an element from 0 to 360 degrees. Using a positive value will rotate an element clockwise, and using a negative value will rotate the element counterclockwise. The default point of rotation is the center of the element, 50% 50%, both horizontally and vertically. Later we will discuss how you can change this default point of rotation.

## HTML:
    <figure class="box-1">Box 1</figure>
    <figure class="box-2">Box 2</figure>

              
## CSS"
.box-1 {
  transform: rotate(20deg);
}
.box-2 {
  transform: rotate(-55deg);
}

              
# Rotate Demo

The gray box behind the rotated element symbolizes the original position of the element. Additionally, upon hover the box will rotate 360 degrees horizontally. As the lesson progresses, keep an eye out for the gray box within each demonstration as a reference to the element’s original position and the horizontal rotation to help demonstrate an elements alteration and depth.

# 2D Scale
Using the scale value within the transform property allows you to change the appeared size of an element. The default scale value is 1, therefore any value between .99 and .01 makes an element appear smaller while any value greater than or equal to 1.01 makes an element appear larger.

## HTML:
    <figure class="box-1">Box 1</figure>
    <figure class="box-2">Box 2</figure>

              
## CSS:
.box-1 {
  transform: scale(.75);
}
.box-2 {
  transform: scale(1.25);
}

# 2D Cube Demo
## HTML:
    <div class="cube">
    <figure class="side top">1</figure>
    <figure class="side left">2</figure>
    <figure class="side right">3</figure>
    </div>

                
## CSS:
    .cube {
    position: relative;
    }
    .side {
    height: 95px;
    position: absolute;
    width: 95px;
    }
    .top {
    background: #9acc53;
    transform: rotate(-45deg) skew(15deg, 15deg);
    }
    .left {
    background: #8ec63f;
    transform: rotate(15deg) skew(15deg, 15deg) translate(-50%, 100%);
    }
    .right {
    background: #80b239;
    transform: rotate(-15deg) skew(-15deg, -15deg) translate(50%, 100%);
    }

# Perspective
In order for three-dimensional transforms to work the elements need a perspective from which to transform. The perspective for each element can be thought of as a vanishing point, similar to that which can be seen in three-dimensional drawings.

The perspective of an element can be set in two different ways. One way includes using the perspective value within the transform property on individual elements, while the other includes using the perspective property on the parent element residing over child elements being transformed.

Using the perspective value within the transform property works great for transforming one element from a single, unique perspective. When you want to transform a group of elements all with the same perspective, or vanishing point, apply the perspective property to their parent element.

# 3D Rotate
So far we’ve discussed how to rotate an object either clockwise or counterclockwise on a flat plane. With three-dimensional transforms we can rotate an element around any axes. To do so, we use three new transform values, including rotateX, rotateY, and rotateZ.

Using the rotateX value allows you to rotate an element around the x axis, as if it were being bent in half horizontally. Using the rotateY value allows you to rotate an element around the y axis, as if it were being bent in half vertically. Lastly, using the rotateZ value allows an element to be rotated around the z axis.

As with the general rotate value before, positive values will rotate the element around its dedicated axis clockwise, while negative values will rotate the element counterclockwise.

## HTML:
    <figure class="box-1">Box 1</figure>
    <figure class="box-2">Box 2</figure>
    <figure class="box-3">Box 3</figure>

              
## CSS:
    .box-1 {
    transform: perspective(200px) rotateX(45deg);
    }
    .box-2 {
    transform: perspective(200px) rotateY(45deg);
    }
    .box-3 {
    transform: perspective(200px) rotateZ(45deg);
    }

   # 3D Scale
By using the scaleZ three-dimensional transform elements may be scaled on the z axis. This isn’t extremely exciting when no other three-dimensional transforms are in place, as there is nothing in particular to scale. In the demonstration below the elements are being scaled up and down on the z axis, however the rotateX value is added in order to see the behavior of the scaleZ value. When removing the rotateX in this case, the elements will appear to be unchanged.

## HTML:
    <figure class="box-1">Box 1</figure>
    <figure class="box-2">Box 2</figure>

              
## CSS:
    .box-1 {
    transform: perspective(200px) scaleZ(1.75) rotateX(45deg);
    }
    .box-2 {
    transform: perspective(200px) scaleZ(.25) rotateX(45deg);
    }

# Transitions & Animations
One evolution with CSS3 was the ability to write behaviors for transitions and animations. Front end developers have been asking for the ability to design these interactions within HTML and CSS, without the use of JavaScript or Flash, for years. Now their wish has come true.

With CSS3 transitions you have the potential to alter the appearance and behavior of an element whenever a state change occurs, such as when it is hovered over, focused on, active, or targeted.

Animations within CSS3 allow the appearance and behavior of an element to be altered in multiple keyframes. Transitions provide a change from one state to another, while animations can set multiple points of transition upon different keyframes.

# Transitions
As mentioned, for a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target pseudo-classes.

There are four transition related properties in total, including transition-property, transition-duration, transition-timing-function, and transition-delay. Not all of these are required to build a transition, with the first three are the most popular.

In the example below the box will change its background color over the course of 1 second in a linear fashion.

    .box {
    background: #2db34a;
    transition-property: background;
    transition-duration: 1s;
    transition-timing-function: linear;
    }
    .box:hover {
    background: #ff7b29;
    }

# Vendor Prefixes
The code above, as with the rest of the code samples in this lesson, are not vendor prefixed. This is intentionally un-prefixed in the interest of keeping the code snippet small and comprehensible. For the best support across all browsers, use vendor prefixes.

For reference, the prefixed version of the code above would look like the following.

    .box {
        background: #2db34a;
        -webkit-transition-property: background;
        -moz-transition-property: background;
            -o-transition-property: background;
                transition-property: background;
        -webkit-transition-duration: 1s;
        -moz-transition-duration: 1s;
            -o-transition-duration: 1s;
                transition-duration: 1s;
        -webkit-transition-timing-function: linear;
        -moz-transition-timing-function: linear;
            -o-transition-timing-function: linear;
                transition-timing-function: linear;
    }
    .box:hover {
    background: #ff7b29;
    }

#  Transition Duration
The duration in which a transition takes place is set using the transition-duration property. The value of this property can be set using general timing values, including seconds (s) and milliseconds (ms). These timing values may also come in fractional measurements, .2s for example.

When transitioning multiple properties you can set multiple durations, one for each property. As with the transition-property property value, multiple durations can be declared using comma separated values. The order of these values when identifying individual properties and durations does matter. For example, the first property identified within the transition-property property will match up with the first time identified within the transition-duration property, and so forth.

If multiple properties are being transitioned with only one duration value declared, that one value will be the duration of all the transitioned properties.


    .box {
    background: #2db34a;
    border-radius: 6px;
    transition-property: background, border-radius;
    transition-duration: .2s, 1s;
    transition-timing-function: linear;
    }
    .box:hover {
    background: #ff7b29;
    border-radius: 50%;
    }

#  Transition Delay
On top of declaring the transition property, duration, and timing function, you can also set a delay with the transition-delay property. The delay sets a time value, seconds or milliseconds, that determines how long a transition should be stalled before executing. As with all other transition properties, to delay numerous transitions, each delay can be declared as comma separated values.


    .box {
    background: #2db34a;
    border-radius: 6px
    transition-property: background, border-radius;
    transition-duration: .2s, 1s;
    transition-timing-function: linear, ease-in;
    transition-delay: 0s, 1s;
    }
    .box:hover {
    background: #ff7b29;
    border-radius: 50%;
    }

#  Transitional Button
## HTML:
    <button>Awesome Button</button>

                
## CSS:
    button {
    border: 0;
    background: #0087cc;
    border-radius: 4px;
    box-shadow: 0 5px 0 #006599;
    color: #fff;
    cursor: pointer;
    font: inherit;
    margin: 0;
    outline: 0;
    padding: 12px 20px;
    transition: all .1s linear;
    }
    button:active {
    box-shadow: 0 2px 0 #006599;
    transform: translateY(3px);
    }

# Card Flip
## HTML:
    <div class="card-container">
    <div class="card">
        <div class="side">...</div>
        <div class="side back">...</div>
    </div>
    </div>

                
## CSS:

    .card-container {
    height: 150px;
    perspective: 600;
    position: relative;
    width: 150px;
    }
    .card {
    height: 100%;
    position: absolute;
    transform-style: preserve-3d;
    transition: all 1s ease-in-out;
    width: 100%;
    }
    .card:hover {
    transform: rotateY(180deg);
    }
    .card .side {
    backface-visibility: hidden;
    height: 100%;
    position: absolute;
    width: 100%;
    }
    .card .back {
    transform: rotateY(180deg);
    }



 Just a couple of lines of code will give you an awesome transition effect that will excite your users, increase engagement and ultimately, when used well, increase your conversions. What’s more, these effects are hardware accelerated, and a progressive enhancement that you can use right now.

## Here are 8 really simple effects that will add life to your UI and smiles to your users’ faces.

# 1. Fade in
    .fade
    {
            opacity:0.5;
    }
    .fade:hover
    {
            opacity:1;
    }
   # 2. Change color.
    .color:hover
    {
            background:#53a7ea;
    }

   # 3. Grow & Shrink
    .grow:hover
    {
            -webkit-transform: scale(1.3);
            -ms-transform: scale(1.3);
            transform: scale(1.3);
    }
# 4. Rotate elements
    .rotate:hover
    {
            -webkit-transform: rotateZ(-30deg);
            -ms-transform: rotateZ(-30deg);
            transform: rotateZ(-30deg);
    }
# 5. Square to circle
    .circle:hover
    {
            border-radius:50%;
    }

# 6. 3D shadow
    .threed:hover
    {
            box-shadow:
                    1px 1px #53a7ea,
                    2px 2px #53a7ea,
                    3px 3px #53a7ea;
            -webkit-transform: translateX(-3px);
            transform: translateX(-3px);
    }
 # 8. Inset border


        .border:hover
    {
            box-shadow: inset 0 0 0 25px #53a7ea;
    }

![](https://www.pngitem.com/pimgs/m/254-2549750_index-of-assets-minimal-404-error-logo-svg.png)

    body {
    margin:0;
    font-family:sans-serif;
    color:#f25252;
    background:#f7f7f7;
    }
    h1 {
    font-size:11rem;
    position:absolute;
    transform:translate(-50%,-50%);
    margin:0;
    }
    h1:nth-of-type(1){
    animation: range 4s infinite;
    }
    h1:nth-of-type(2){
    left:50%;
    top:50%;
    animation: size 4s infinite;
    }
    h1:nth-of-type(3){
    animation: range2 4s infinite;
    }
    @keyframes range {
    0%  {left:42%;top:50%;font-size:11rem;}
    25% {left:50%;top:40%;font-size:4.5rem;}
    50% {left:58%;top:50%;font-size:11rem;}
    75% {left:50%;top:60%;font-size:4.5rem;}
    100%{left:42%;top:50%;font-size:11rem;}
    }
    @keyframes range2 {
    0%  {left:58%;top:50%;font-size:11rem;}
    25% {left:50%;top:60%;font-size:4.5rem;}
    50% {left:42%;top:50%;font-size:11rem;}
    75% {left:50%;top:40%;font-size:4.5rem;}
    100%{left:58%;top:50%;font-size:11rem;}
    }
    @keyframes size {
    0%  {font-size:11rem;}
    25% {font-size:26rem;}
    50% {font-size:11rem;}
    75% {font-size:26rem;}
    100%{font-size:11rem;}
    }



  ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAASwAAACoCAMAAABt9SM9AAAATlBMVEUpesv///8jeMoedsoTc8ne6fYOcshonNh+qdwAcMhJitGfv+W2zuqzzOqSt+I/hs+MsuDM3fHt9PvT4vNyotrm7/mrx+hPjtKFrt4ygM6dosh/AAAA3klEQVR4nO3XW27CMBAF0PgREzdQKK+0+99oP/gAIiVUqtSk0jkruLoajzxNAwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAL8UUy45x6Vj/AMx1beu3+7e93npKGsXa3Now02vrVl1vw13m7R0nhWLpQ+PPurSiVYsnp66CkfvcFIedRVOZelIq5UOo67C2c6aUtpRVzsra1K+PHd11dW08vhrCJeNrmbE4V5V22X7alY6H29DdR1qchm+kMrQfW6+qhv6R2JKZgoAAAAAAAAAAAAAAAAAAAAA4G99A0jdA8Q7yknRAAAAAElFTkSuQmCC)

    @keyframes balltransform {
        0% {
            border-radius:50%;
            height:100%;
            width:60%;
        }
        29% {
            height:100%;
            width:60%;
        }
        30% {
            height:50%;
            width:100%;
        }
        40% {
            height:80%;
            width:80%;
        }
        59% {
            height:100%;
            width:60%;
        }
        60% {
            height:50%;
            width:100%;
            border-radius:50%;
            transform:rotate(0);
        }
        100% {
            height:80%;
            width:80%;
            border-radius:0;
            transform: rotate(-180deg);
        }
    }

    @keyframes ballbounce {
        /* up */
        0% {
            top:-30%;
            animation-timing-function: ease-in;
        }
        /* floor */
        30% {
            top:80%;
            animation-timing-function: ease-out;
        }
        /* up */
        40% {
            top: 20%;
        }
        /* up */
        45% {
            top:17%;
            animation-timing-function: ease-in;
        }
        /* floor */
        60% {
            top:80%;
            animation-timing-function: ease-out;
        }
        /* up */
        75% {
            top:30%;
        }
        90% {
            top:25%;
            animation-timing-function: ease-in;
        }
        /* floor */
        100% {
            top:110%;
            animation-timing-function:ease-out;
        }
    }

    @keyframes scalemask {
        0% {
            mask-size:0%;
        }
        65% {
            mask-size:0%;
        }
        78%,100% {
            mask-size:300%;
        }
    }

    @keyframes scalemask2 {
        0% {
            -webkit-mask-size:0%;
        }
        83% {
            -webkit-mask-size:0%;
        }
        100% {
            -webkit-mask-size: 300%;
        }
    }

    * {
        box-sizing:border-box;
    }

    body {
        padding:0;
        margin: 0;
    }

    /* Ball -------------------- */
    .ball {
        width:5rem;
        height:5rem;
        left:50%;
        position:absolute;
        z-index:1;
        margin-left:-2.5rem;
        animation:ballbounce 4s 1s infinite;
        animation-fill-mode:both;
    }

    .ball:after {
        content:" ";
        color:#fff;
        display:block;
        margin:auto;
        border-radius:50%;
        background:#fff;
        width:100%;
        height:100%;
        animation: balltransform 4s 1s infinite;
    }

    /* Animation containers -------------------- */
    .animation {
        background:#297acb;
        height:100vh;
        width:100vw;
        position:relative;
        z-index:1;
    }

    .animation-2,
    .animation-3 {
        position:absolute;
        top:0;
        left:0;
        -webkit-mask-size:0;
        -webkit-mask-image:radial-gradient(circle closest-side,black 0%,black 90%,rgba(255,255,255,0) 92%);
        -webkit-mask-repeat:no-repeat;
        -webkit-mask-position:center center;
        animation-fill-mode:both;
    }

    .animation-2 {
        background:purple;
        animation:scalemask 4s 1s infinite;
    }

    .animation-3 {
        animation:scalemask2 4s 1s infinite;
    }

    .animation-2 .ball:after {
        background: #297acb;
    }

    
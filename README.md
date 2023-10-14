# flipbook
created flipbook using only html/css no third party resources 

Flipbook README
This is a simple flipbook project created using HTML and CSS. It consists of several pages that can be flipped through using checkboxes and CSS animations. Below, you'll find an overview of the project structure and how to use it.

Project Structure
The project structure includes the following files:

index.html: This is the main HTML file that defines the structure of the flipbook, including the cover, pages, and back cover.

style.css: This is the CSS file responsible for styling the flipbook. It includes styles for the cover, pages, animations, and more.

Images: The project includes various image files (e.g., pic2.0.jpg, pic12.0.jpg, cover pic.jpg) used as content within the flipbook.

How to Use
        To view the flipbook, follow these steps:
        
        Clone the repository to your local machine.
        
        Open the index.html file in a web browser of your choice.
        
        You will see the cover of the flipbook. To flip through the pages, click on the left or right corners of the pages. This will simulate turning the pages of a physical book.
        
        The flipbook includes several pages, each with different content and images.
        
        Enjoy flipping through the pages and reading the content!

Customization
If you want to customize the flipbook, you can do so by modifying the HTML and CSS files. Here are some customization options:

      Changing Content: You can replace the content of each page with your own text and images by modifying the HTML within the <div class="page"> elements.
      
      Styling: Feel free to modify the styles in the style.css file to change the colors, fonts, or animations used in the flipbook.
      
      Adding More Pages: If you want to add more pages to the flipbook, you can replicate the structure of existing pages by creating additional <div class="page"> elements in the HTML.

Credits
  Icons: This project uses icons from FontAwesome.

  Quote: A quote by William Shakespeare is included in one of the pages and quroa.

Author
This flipbook project was created by AISHWARYA MS.


html file consists of >>>>>>>>>>>>>>>>>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="flipbook">
    <title>flipbook</title> <!--added a title -->
    <link rel="stylesheet" href="style.css"> <!--linked to css file -->
    <script src="https://kit.fontawesome.com/1cad54f882.js"></script> <!--added icons -->

    <body>
<!--within the html> body, now creating a div with respective class, label with for and input with id that will help us understand and make styling easier for both programmers and views -->
                <input type="checkbox" id="checkbox-cover">
                <input type="checkbox" id="checkbox-page1">
                <input type="checkbox" id="checkbox-page2">
                <input type="checkbox" id="checkbox-page3">
                <div class="book">
                    <div class="cover">
                       <!--added a div  whose class= "cover"; It also has a label "checkbox-cover"-->
                        <label for="checkbox-cover"></label>
                    </div>
                    <!--created page 1 with id=page1 liked to the input type=checkbox id=checkbox-page1 -->
                    <div class="page" id="page1" >
                        <div class="front-page" style="background-color: white;"> <!-- added inline styling to page 1 with bg clr= white -->
                                
                            <p class="para"> Live a Little </p> <!-- added paragragh to page 1-->
                            <blockquote>So holy and so perfect is my love,
                                And I in such a poverty of grace,
                                That I shall think it a most plenteous crop
                                To glean the broken ears after the man
                                That the main harvest reaps; loose now and then
                                A scatt'red smile, and that I'll live upon.
                                —William Shakespeare</blockquote>  <!-- added paragragh and quote of William Shakespeare to page 1-->
                            <label class="prev" for="checkbox-page1"></label>
                        </div> 
                        <div class="back-page"> <!-- created a back page, opp to front page to have an img or content to page 2(backside of page 1) which can be viewed as we flip the page-->
                            <img src="./pic2.0.jpg" >     
                            <label class="next" for="checkbox-page1"><i class="fas fa-chevron-left"></i></label>
                        </div>
                    </div>
<!-- repated all the steps to page 3, 4, 5 , 6-->

                    <div class="page" id="page2" >
                        <div class="front-page" style="background-color: white;">
                            <p class="para"> Happiness</p>
                            <p> Happiness is not something outside <br>
                                It is an attitude you can provide <br>
                                Your happiness is not down the road <br>
                                And, it doesn't mean an easy load. <br><br>
                                
                                Happiness is found in you <br>
                                How you look at life and what you do <br>
                                You decide each day, you see <br>
                                How happy you will be?  <br></p> 
                            <label class="prev" for="checkbox-page2"></label>
                        </div> 
                        <div class="back-page">
                            <img src="./pic12.0.jpg">   
                            <label class="next" for="checkbox-page2"><i class="fas fa-chevron-left"></i></label>
                        </div>
                    </div>
                    <div class="page" id="page3" >
                        <div class="front-page" style="background-color: white;">
                            <p class="para"> HER </p>   
                            <p > Her smile is like the sky sparkling with diamonds. Happiness is in her soul to energize body's frame. She will forever be the same with her wondrous smile! Her smile uplifts the depressed soul and warms the cold heart. </p>
                            <label class="prev" for="checkbox-page3"></label>
                        </div> 
                        <div class="back-page">
                            <img src="./cover pic.jpg" >     
                            <label class="next" for="checkbox-page3"><i class="fas fa-chevron-left"></i></label>
                        </div>
                    </div>
                    <div class="page" id="page4" >
                        <div class="front-page" style="background-color: white;">
                                
                            <p class="para"> LIVE <br> LOVE <br> LAUGH </p>
                            <label class="prev" for="checkbox-page4"></label>
                        </div> 
                    </div>
                    <div class="back-cover"></div>
                </div>

      <!-- created the back of the book as back-cover in the above page, closed the body and html -->
    </body>
</html>


CSS File consists of >>>>>>>>>>>>>>>>>>>>

*{
margin: 0px;
padding: 0px;
}
/*created  css style sheet with padding and margin as =0px, The main reason this is used is because sometimes the browser will apply it's default margin/padding to elements, and in a case where you do not want there to be any margin or padding space around an element you will want to define that there is no margin or padding.*/
body {
	font-family: "Poppin", sans-serif;
	background-color: #e5e9ea;
	height: 100vh;
	display: flex;
	align-items: center;
	justify-content: center;
}/*styled the body of the web created with bg clr-white , specifying height and importantly making display to flex to justify and align them in center. Flexbox is a Layout Module, makes it easier to design flexible responsive layout structure without using float or positioning.*/

.book {
	width: 350px;
	height: 450px;
	position: relative;
	transition-duration: 1s;
	perspective: 1500;
} /* width, height is applied for customisation of certain properties over required items for desired changes. here postion is : relative. tarnsition are controlled using the shorthand transition property. This is the best way to configure transitions, as it makes it easier to avoid out of sync parameters, which can be very frustrating to have to spend lots of time debugging in CSS.*/
input {
	display: none; /*display CSS property sets whether an element is treated as a block or inline box and the layout used for its children, such as flow layout, grid or flex. when none of them are used, we use none*/
} /*adding css to cover and back cover with desired bg clr= yellow, adding shadow to add depth to the book and give visual effects, making it flex gives various opts for customisation*/
.cover, .back-cover {
	background-color: #dcc026;
	width: 100%;
	height: 100%;
	border-radius: 0 15px 15px 0;
	box-shadow: 0 0 5px rgb(108, 108, 108);
	display: flex;
	align-items: center;
	justify-content: center;
	transform-origin: center left;
}
.cover {
	position: absolute;
	z-index: 4; /*the z-index sets the z-order of a positioned element and its descendants or flex items. Overlapping elements with a larger z-index cover those with a smaller one.*/
	transition: transform 1s;
}
.cover label {
	width: 100%;
	height: 100%;
	cursor: pointer; /*cursor which looks as an arrow to pointer that allows users to interact through clicks */
}

.para{

/* text-align: center; */
display: flex;
justify-content: center;
align-items: center;
padding-top: 15%;
font-size: 40px;
}
.page {
	position: absolute;
	background-color: white;
	width: 330px;
	height: 435px;
	border-radius: 0 15px 15px 0;
	margin-top: 10px;
	transform-origin: left; /*tranform s and annimations are effective in css. here we use transform property lets you rotate, scale, skew, or translate an element. It modifies the coordinate space of the CSS visual formatting model.*/
	transform-style: preserve-3d; /*tells us on how nested elements are rendered in 3D space.*/
	transform: rotateY(10deg); /*A two-dimensional transformation is applied to an element through the 'transform' property. */
	transition-duration: 1.5s;/*Specifies how long the transition from the old value to the new value should take.*/
}

.front-page {
	position: absolute;
	width: 100%;
	height: 100%;
	backface-visibility: hidden;/*Determines whether or not the 'back' side of a transformed element is visible when facing the viewer. With an identity transform, the front side of an element faces the viewer.*/
	box-sizing: border-box;/*Specifies the behavior of the 'width' and 'height' properties.*/
	padding: 1rem;
    cursor: pointer;/*Allows control over cursor appearance in an element*/
    /* transition: transform 1s; */

}

.page img {
    margin-bottom: auto;/*the thickness of the margin area. If left is omitted, it is the same as right. If bottom is omitted it is the same as top, if right is omitted it is the same as top. Negative values for margin properties are allowed, but there may be implementation-specific limits..*/
	width: 100%;
	height: 100%;
	border-radius: 15px 0 0 15px;
}


.next, .prev {
	position: absolute;/*sets how an element is positioned */
	bottom: 1em;
	cursor: pointer;
}
.next {
	right: 1em;
}
.prev {
	left: 1em;
}

#page1 {
	z-index: 3;
}
#page2 {
	z-index: 2;
}
#page3 {
	z-index: 1;
}
#checkbox-cover:checked ~ .book {
	transform: translateX(200px);
}
#checkbox-cover:checked ~ .book .cover {
	transition: transform 1.5s, z-index 0.5s 0.5s;
	transform: rotateY(-180deg);
	z-index: 1;
}
#checkbox-cover:checked ~ .book .page {
	box-shadow: 0 0 3px rgb(99, 98, 98);
}
#checkbox-page1:checked ~ .book #page1 {
	transform: rotateY(-180deg);
	z-index: 2;
}
#checkbox-page2:checked ~ .book #page2 {
	transform: rotateY(-180deg);
	z-index: 2;
}
#checkbox-page3:checked ~ .book #page3 {
	transform: rotateY(-180deg);
	z-index: 2;
}



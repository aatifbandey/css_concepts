CSS Interview Questions

Ruleset
	
	It consist of a selector and declaration block
	h1 -> selector
	{
		// declaration block
	}

Padding vs Margin

	Padding is the inner space of the element
	Margin is the outer space of the element of the border.

Box Sizing 
	
	Its a property used to tell browser 
	https://www.w3schools.com/cssref/tryit.asp?filename=trycss3_box-sizing 

Psuedo elements

	Psuedo elements are used to design some parts of elements with a selector

	eg : h1::first-line{
			color : blue
		}

Psuedo Classes
	
	These are used to define a state of an element 
	eg a : hover{
		color: blue;
	}

Setting the viewport
	
	HTML5 introduced the concept of viewport by defined in <meta name="viewport"
	and device width and initial zoom level

What is negation (not) in css

	negation is used as not to apply css for that condition
	eg: p:not(.classy){
			color:red     // css will be applied everywhere accept elems whom class is classy
		}

Box Modal

	It has margin, padding, border, content

Inline and Block elements

	Block elements take full width and leave space before and after element
	Eg div h1

	Inline block elements take required width 
	eg : span

How to give a line break using span in CSS?
	
	<span style=” display: block” />

What is Background clip?
	
	It specifies to apply background for  which area of div
	Eg background-clip : padding-box or content-box
	https://www.w3schools.com/cssref/tryit.asp?filename=trycss3_background-clip

What is Background origin
	
	It defines from where the background image should start from
	Eg  #example1 {
		    background:url(img_flwr.gif);
		    background-repeat: no-repeat;
		    padding:35px;
		    background-origin: content-box;
		}
		https://www.w3schools.com/cssref/tryit.asp?filename=trycss3_background-origin

Add Multiple background

	backround-image :url('vv'), url('kk');


How to fit a potrait image in container
	
	width : 100%;
	height : auto;


Concept on Static | Relative | Absolute | Fixed

	Static
	Static is default position of every element in css.
	Z-index wont work for it


	Relative
	It is the most confused position. As it means its relative to itself
	Eg if you give postion:relative to a div and also provide left : 10px it will move 10 px
	from where it was.Also z-index works for this

	Absolute
	This position is dependent on its parent if you give top:10px and its parent is relative then it will move
	10px from parent div z-index works for this

	Fixed:
	This position is relative to viewport 

Difference b/w 
	
	@media (max-width:632px) vs @media screen and (max-width:632px) vs @media only screen and (max-width:632px)
	
	@media (max-width:632px)
	This one is saying for a window with a max-width of 632px that you want to apply these style and lesser width than 632px 

	@media screen and (max-width:632px)
	This one is saying for a device with a screen and a window with max-width of 632px apply the style. The difference is media type should be screen not print or other media type

	@media only screen and (max-width:632px)
	The keyword ‘only’ can also be used to hide style sheets from older user agents. User agents must process media queries starting with ‘only’ as if the ‘only’ keyword was not present

	For more ref : http://stackoverflow.com/questions/8549529/what-is-the-difference-between-screen-and-only-screen-in-media-queries


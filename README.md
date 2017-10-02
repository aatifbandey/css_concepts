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
	
	Its a property used to tell browser the space and it takes the height and if padding is given it doesnt increase
	the container height
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

Specificity 
	inline sytyle
	ID - 100
	Class
	Attributes
	Sudeo class

	Memorize how to measure specificity. “Start at 0, add 1000 for style attribute, add 100 for each ID, add 10 for each attribute, class or pseudo-class, add 1 for each element name or pseudo-element. So in
	body #content .data img:hover
	the specificity value would be 122 (0,1,2,2 or 0122): 100 for #content, 10 for .data, 10 for :hover, 1 for body and 1 for img.” [CSS Specificity]

	Important table for order specificity

	1	* { }	0
	2	li { }	1 (one element)
	3	li:first-line { }	2 (one element, one pseudo-element)
	4	ul li { }	2 (two elements)
	5	ul ol+li { }	3 (three elements)
	6	h1 + *[rel=up] { }	11 (one attribute, one element)
	7	ul ol li.red { }	13 (one class, three elements)
	8	li.red.level { }	21 (two classes, one element)
	9	style=””	1000 (one inline styling)
	10	p { }	1 (one HTML selector)
	11	div p { }	2 (two HTML selectors)
	12	.sith	10 (one class selector)
	13	div p.sith { }	12 (two HTML selectors and a class selector)
	14	#sith	100 (one id selector)
	15	body #darkside .sith p { }	112 (HTML selector, id selector, class selector, HTML selector; 1+100+10+1)



Semantic HTMl
	it represents the content of web page.
	Eg <h1> to <h6> are semantic tags
		<p> is a semantic tag
		<code>, <abbr>, <span> etc are semantic tags
	Why it is important ?

	Many visually impaired people rely on speech browsers to read pages back to them. These programs cannot interpret pages very well unless they are clearly explained.

	Search engines need to understand what your content is about in order to rank you properly on search engines. Semantic code tends to improve your placement on search engines

	Semantic code makes site updates easier because you can apply design style to headings across an entire site instead of on a per page basis.

	Features:

		No More Types for Scripts and Links
		<link rel="stylesheet" href="path/to/stylesheet.css" />  no need of type attribute
		<script src="path/to/script.js"></script>

		Email Inputs
		Placeholders
		Session storage
		Local Storage
		Semantic header and footer
		Autofocus attribute on inputs
		Required attribute on inputs
		Regular Expressions
			Thanks to the new "pattern" attribute, we can insert a regular expression directly into our markup
			<input pattern="[A-Za-z]{4,10}" >

		When to Use a <div> Now?
		if you find that you need to wrap a block of code within a wrapper element specifically for the purpose of positioning the content, a <div> makes perfect sense. However, if you're instead wrapping a new blog post, or, perhaps, a list of links in your footer, consider using the <article> and <nav> elements, respectively. They're more semantic


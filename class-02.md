# summarizing : 

## chapter 2 (text) : 

* there are markup to the text that
appears on your pages : 
1. structural markup such as : 
- headings : 

*html has six level of heading from h1 to h6 ( from the biggest to smallest),(we put it between tags)* . 

![headings](https://www.schudio.com/wp-content/uploads/2016/10/html-headings.png?x97747)

- paragraphs :

***To create a paragraph, surround
the words that make up the
paragraph with an opening p
tag and closing p tag***.

![paragraphs](https://ictacademy.com.ng/wp-content/uploads/2017/10/demo.png)


- bold text : 

**By enclosing words in the tags
b and b we can make characters appear bold**.

![bold](https://i.ytimg.com/vi/rmqyIN3KvA8/maxresdefault.jpg)

- italic text : 

*By enclosing words in the tags
i and i we can make characters appear italic* .

![italic](https://www.wikihow.com/images/a/a7/Italicize-Text-in-HTML-Step-6.jpg)

- Superscript & Subscrip :

sup : The sup element is used
to contain characters that
should be superscript such
as the suffixes of dates or
mathematical concepts like
raising a number to a power such
as 22 . 

sub : The sub element is used to
contain characters that should
be subscript. It is commonly
used with foot notes or chemical
formulas such as H20.

![supandsub scripts](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRvQeHVgtj1DvgNRyK4ZzePWo3cHnXXHw25Fw&usqp=CAU)

- line breaks and horizontal rules:

line breaks : 

the browser will automatically show each new paragraph or heading on a new line. But if you wanted to add a line break inside the middle of a paragraph you can use the line break tag br . 

horizontal rules : 

the browser will automatically show each new paragraph or heading on a new line. But if you wanted to add a line break inside the middle of a paragraph you can use the line break tag br .

2. semantic markup such as : 

- strong and emphasis : 

strong : The use of the strong
element indicates that its content has strong importance. For example, the words contained in this element might be said with strong emphasis. By default browsers will show the contents of a strong element in bold . 

emphasis : The em element indicates emphasis that subtly changes the meaning of a sentence.
By default browsers will show the contents of an em element in italic. 

- Quotations : 
The blockquote element is used for longer quotes that take up an entire paragraph. Note how the p element is still used inside the blockquote element. Browsers tend to indent the contents of the blockquote element, however you should not use this element just to indent a piece of text — rather you should achieve this effect using CSS .

* The q element is used for shorter quotes that sit within a paragraph. Browsers are supposed to put quotes around the q element, however Internet Explorer does not —therefore many people avoidusing the q element.


- Abbreviations & Acronyms : 

If you use an abbreviation or an acronym, then the abbr element can be used. A title attribute on the opening tag is used to specify the full term. 

- Citations & Definitions : 

cite :
 When you are referencing a piece of work such as a book, film or research paper, the
cite element can be used to indicate where the citation is from . 

definition :
 The first time you explain some new terminology (perhaps an academic concept or some
jargon) in a document, it is known as the defining instance of it. The dfn element is used to indicate the defining instance of a new term.

- Author Details : 

address : The address element has quite a specific use: to contain contact details for the author of the page. It can contain a physical address, but it does not have to. For
example, it may also contain a phone number or email address .

- changes to content : 

ins and del : The ins element can be used to show content that has been inserted into a document, while the del element can show text that has been deleted from it.

s : The s element indicates something that is no longer accurate or relevant (but that should not be deleted). Visually the content of an s element will usually be displayed with a line through the center . 

*** 

### chapter 10 (introducing css) : 

- what is css ? 
CSS stands for Cascading Style Sheets. CSS describes how HTML elements are to be displayed on screen, paper, or in other media. CSS saves a lot of work. It can control the layout of multiple web pages all at once. External stylesheets are stored in CSS files.

- how css works ? 
 The browser loads the HTML (e.g. receives it from the network) .
 It converts the HTML into a DOM (Document Object Model). The DOM represents the document in the computer's memory The DOM is explained in a bit more detail in the next section.
 The browser then fetches most of the resources that are linked to by the HTML document, such as embedded images  and videos ... and linked CSS! JavaScript is handled a bit later on in the process, and we won't talk about it
here to keep things simpler.
The browser parses the fetched CSS, and sorts the different rules by their selector types into different "buckets", e.g. element, class, ID, and so on. Based on the selectors it finds, it works out which rules should be applied to which nodes in the DOM, and attaches style to them as required (this intermediate step is called a render tree).
The render tree is laid out in the structure it should appear in after the rules have been applied to it.
The visual display of the page is shown on the screen (this stage is called painting) .


![circle](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_works/rendering.svg)

- css syntax and properties and values : 
this is a syntax of css . 


![syntax](https://www.w3schools.com/css/selector.gif)




- this is a properties of css : 

align-content : 	Specifies the alignment of flexible container's items within the flex container.
align-items : 	Specifies the default alignment for items within the flex container.
align-self :  	Specifies the alignment for selected items within the flex container.
animation :  	Specifies the keyframe-based animations.
animation-delay :	Specifies when the animation will start.
animation-direction :	Specifies whether the animation should play in reverse on alternate cycles or not.

- css values : 
1. integers and real numbers . 
2. lengths . 
3. units . 
4. percentage .
5. colors .

- Using External CSS : 
1. link : The link element can be used in an HTML document to tell the browser where to find the CSS file used to style the page. It is an empty element (meaning it does not need a closing tag), and it
lives inside the head element. It should use three attributes . 

2. href :This specifies the path to the CSS file (which is often placed in a folder called css or styles) . 

3. type : This attribute specifies the type of document being linked to. The value should be text/css.

4. rel :This specifies the relationship between the HTML page and the file it is linked to. The value should be stylesheet when linking to a CSS file . 

- Using Internal CSS : 

1. style: You can also include CSS rules within an HTML page by placing them inside a style element,
which usually sits inside the head element of the page. The style element should use the type attribute to indicate that the styles are specified in CSS. The value should be text/css.

- CSS selectors : 

*There are many different types
of CSS selector that allow you to
target rules to specific elements
in an HTML document such as* : 


![selectors](https://i.pinimg.com/originals/bc/97/96/bc97965579512f8a6d2303934f599c65.png)

*** 

#### chapter 2 (basic javascript instruction) : 

scripts : 

1. A script is a series of instructions that a computer can follow one-by-one. Each individual instruction or step is known as a statement. Statements should end with a semicolon.

2. You should write comments to explain what your code does. They help make your code easier to read and understand. This can help you and others who read your code. 

3. A script will have to temporarily store the bits of information it needs to do its job. It can store this
data in variables.


*So here are the 5 basic concepts of any programming language* :

1.Variables.

2.Control Structures.

3.Data Structures.

4.Syntax.

5.Tools.

**we can makes web pages more interactive with javascripts** :

- access content 
- modify content 
- program rules
- react to events

***you have to learn the basics of scripts and the concepts before you doing the tasks and designing such as*** :

- what is a scripts and how do i create a one ?
- how do computers fit in the world around them ?
- how do i write a script for a web page ?

*you can compare scripts through this concepts* :

- recipes
- handbooks
- manuals

**there is a steps for designing scripts** :

1. remove used bedding .
2.  wipe all surfaces .
4. vacum floors .


- expressions+operators :

![expressions](data:image/png;base64,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)

*there are two type of expressions :
- expressios that jus assign a value to a variable .

- expressions that use two or
more values to return a
single value . 

*Expressions rely on things called operators; they allow programmers to
create a single value from one or more values and there are four types of operators* :

- assignment operator .
- comparsion operators .
- string operators .
- arithmetic operators like :


![operators](https://2.bp.blogspot.com/-Aa3I3yOraos/W8LSLWl3Q5I/AAAAAAAAESw/RJugarKq2mQn0zb8BXB6cYHtKOjYXoAEgCLcBGAs/w1200-h630-p-k-no-nu/arithmatic-operators.PNG)

*** 

##### chapter 4 (decisions and loops) : 

- Like other languages, JavaScript also provides many decision making statements like if, else, etc . : 

1. if statement : if is used to check for a condition whether its true or not. Condition could be any expression that returns true or false. When condition satisfies then statements following if statement are executed.

2. else statement : else statements are used with if statements. When if condition gets fail then else statement is executed. 

*there are two components to a decision* : 
1. an expression is evaluated , which returns a value .
2. a conditional statement says what to do in a given situation . 

* comparison operators : 

![operators](data:image/png;base64,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)

- logical operators : 

![logical](https://www.devopsschool.com/blog/wp-content/uploads/2020/07/JavaScript-Logical-Operator.png)

###### thanks for reading . 

































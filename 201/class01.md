# explaining HTML & CSS
## what is HTML and CSS?
HTML is a marking language to structure the web page and CSS is to add colors and alignments to the structure.

** How Pages are Structured **

Think about the stories you read in a newspaper: for each story, there will be a headline, some text, and possibly some images. If the  article is a long piece, there may be subheadings that split the story into separate sections or quotes from those involved. Structure helps readers understand the stories in the newspaper.The structure is very similar when a news story is viewed online (although it may also feature audio or video). This is illustrated on the right with a copy of a newspaper alongside the corresponding article on its website.Now think about a very different type of document — an insurance form. Insurance forms often have headings for different sections, and each section contains a list of questions with areas for you to fill in details or checkboxes to tick. Again, the structure is very similar online.

![page structre in HTML](https://qatechhub.com/wp-content/uploads/2016/09/BasicHtmlStructure.png)

![HTML code snippet](https://i.stack.imgur.com/HldY2.png)

** CSS for Styling**

CSS is the language we use to style an HTML document.
CSS describes how HTML elements should be displayed.

**linking CSS file to HTML page**

Definition and Usage
The <link> tag defines the relationship between the current document and an external resource.

The <link> tag is most often used to link to external style sheets.

The <link> element is an empty element, it contains attributes only.

When a browser reads a style sheet, it will format the HTML document according to the information in the style sheet.

Three Ways to Insert CSS
There are three ways of inserting a style sheet:

1. External CSS
2. Internal CSS
3. Inline CSS

*how they work?*
Markup languages work in the same way as you just did when you labeled those content types, except they use code to do it -- specifically, they use HTML tags, also known as "elements." These tags have pretty intuitive names: Header tags, paragraph tags, image tags, and so on.

Every web page is made up of a bunch of these HTML tags denoting each type of content on the page. Each type of content on the page is "wrapped" in, i.e. surrounded by, HTML tags.

For example, the words you're reading right now are part of a paragraph. If I were coding this web page from scratch (instead of using the WYSIWG editor in HubSpot's CMS), I would have started this paragraph with an opening paragraph tag: <p>. The "tag" part is denoted by open brackets, and the letter "p" tells the computer that we're opening a paragraph instead of some other type of content.

Once a tag has been opened, all of the content that follows is assumed to be part of that tag until you "close" the tag. When the paragraph ends, I'd put a closing paragraph tag: </p>. Notice that closing tags look exactly the same as opening tags, except there is a forward slash after the left angle bracket. Here's an example:

<p>This is a paragraph.</p>

Using HTML, you can add headings, format paragraphs, control line breaks, make lists, emphasize text, create special characters, insert images, create links, build tables, control some styling, and much more.

To learn more about coding in HTML, I recommend checking out our guide to basic HTML, and using the free classes and resources on codecademy -- but for now, let's move on to CSS.

CSS
CSS stands for Cascading Style Sheets. This programming language dictates how the HTML elements of a website should actually appear on the frontend of the page.

HTML vs CSS
HTML provides the raw tools needed to structure content on a website. CSS, on the other hand, helps to style this content so it appears to the user the way it was intended to be seen. These languages are kept separate to ensure websites are built correctly before they're reformatted.


* JS for giving life to the page *

JavaScript is the world's most popWhy Study JavaScript?
JavaScript is one of the 3 languages all web developers must learn:

   1. HTML to define the content of web pages
   2. CSS to specify the layout of web pages
   3. JavaScript to program the behavior of web pagesular programming language.

JavaScript is the programming language of the Web.

JavaScript is easy to learn.

Why Study JavaScript?
JavaScript is one of the 3 languages all web developers must learn:

   1. HTML to define the content of web pages

   2. CSS to specify the layout of web pages

   3. JavaScript to program the behavior of web pages

![JS code snippet](https://res.cloudinary.com/practicaldev/image/fetch/s--LsnxYBWY--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/i/jxfae4q7i6kbewhxzmzh.png)

* how does JS function?

So, how does JS do everything it does? Where is it's best use? To understand how it works, when and where, first, we need to speak of its nature.

NATURE OF JAVASCRIPT:

JS is a single threaded and single concurrent programming language which means it can handle one task at a time or, in other words, a piece of code at a time. It’s an interpreted programming language, and like most scripting languages, it uses dynamic typing, where type safety is verified at the runtime. But how JS runtime handles tasks or executes asynchronous codes?

JavaScript is asynchronous by nature, meaning it is designed to ensure the non-blocking code execution. Non blocking code do not prevent the execution of another piece of code. This means that the server works in much the same way, waiting in a loop for a network request, and accepting more incoming requests while the first one is being handled. 

Asynchronous programming is great for a faster execution of programs but it is difficult to develop and most of the time you might end up with callback hell situations. So to avoid it you can modularise your code, use generators, promises, event-driven programming or Async.js.

![JS code snippet](https://res.cloudinary.com/practicaldev/image/fetch/s--LKutaB_j--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://pbs.twimg.com/media/EUaykCrUUAIMkUW.jpg)

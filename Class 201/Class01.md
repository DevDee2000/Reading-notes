# ***Skim Reads*** <hr>

&nbsp;

## <ins>**Clients and Servers**</ins>

- Clients are the typical web user's internet-connected devices (for example, your computer connected to your Wi-Fi, or your phone connected to your mobile network) and web-accessing software available on those devices (usually a web browser like Firefox or Chrome).

- Servers are computers that store webpages, sites, or apps. When a client device wants to access a webpage, a copy of the webpage is downloaded from the server onto the client machine to be displayed in the user's web browser.

&nbsp;

## <ins>The other parts of the toolbox</ins>

- Your internet connection: Allows you to send and receive data on the web. It's basically like the street between your house and the shop.


- TCP/IP: Transmission Control Protocol and Internet Protocol are communication protocols that define how data should travel across the internet. This is like the transport mechanisms that let you place an order, go to the shop, and buy your goods. In our example, this is like a car or a bike (or however else you might get around).


- DNS: Domain Name System is like an address book for websites. When you type a web address in your browser, the browser looks at the DNS to find the website's IP address before it can retrieve the website. The browser needs to find out which server the website lives on, so it can send HTTP messages to the right place (see below). This is like looking up the address of the shop so you can access it.


 - HTTP: Hypertext Transfer Protocol is an application protocol that defines a language for clients and servers to speak to each other. This is like the language you use to order your goods.


- Component files: A website is made up of many different files, which are like the different parts of the goods you buy from the shop. These files come in two main types:


>- Code files: Websites are built primarily from HTML, CSS, and JavaScript, though you'll meet other technologies a bit later.


>- Assets: This is a collective name for all the other stuff that makes up a website, such as images, music, video, Word documents, and PDFs.

&nbsp;

## <ins>**So what happens exactly?**</ins>

### When you type a web address into your browser (for our analogy that's like walking to the shop):

1.  The browser goes to the DNS server, and finds the real address of the server that the website lives on (you find the address of the shop).


2. The browser sends an HTTP request message to the server, asking it to send a copy of the website to the client (you go to the shop and order your goods). This message, and all other data sent between the client and the server, is sent across your internet connection using TCP/IP.


3. If the server approves the client's request, the server sends the client a "200 OK" message, which means "Of course you can look at that website! Here it is", and then starts sending the website's files to the browser as a series of small chunks called data packets (the shop gives you your goods, and you bring them back to your house).


4. The browser assembles the small chunks into a complete web page and displays it to you (the goods arrive at your door — new shiny stuff, awesome!).

&nbsp;

## <ins>**Order in which component files are parsed**</ins>

- When browsers send requests to servers for HTML files, those HTML files often contain < link> elements referencing external CSS stylesheets and < script> elements referencing external JavaScript scripts. It's important to know the order in which those files are parsed by the browser as the browser loads the page:


- The browser parses the HTML file first, and that leads to the browser recognizing any < link>-element references to external CSS stylesheets and any < script>-element references to scripts.

 
- As the browser parses the HTML, it sends requests back to the server for any CSS files it has found from < link> elements, and any JavaScript files it has found from < script> elements, and from those, then parses the CSS and JavaScript.
The browser generates an in-memory DOM tree from the parsed HTML, generates an in-memory CSSOM structure from the parsed CSS, and compiles and executes the parsed JavaScript.


- As the browser builds the DOM tree and applies the styles from the CSSOM tree and executes the JavaScript, a visual representation of the page is painted to the screen, and the user sees the page content and can begin to interact with it.

&nbsp;


## <ins>**DNS Explained**</ins>

- ### Real web addresses aren't the nice, memorable strings you type into your address bar to find your favorite websites. They are special numbers that look like this: 63.245.215.20.

- ### This is called an IP address, and it represents a unique location on the web. However, it's not very easy to remember, is it? That's why Domain Name Servers were invented. These are special servers that match up a web address you type into your browser (like "mozilla.org") to the website's real (IP) address.

- ## Websites can be reached directly via their IP addresses. You can use a DNS lookup tool to find the IP address of a website.

&nbsp;

## <ins>**Packets Explained**</ins>

- ### Earlier we used the term "packets" to describe the format in which the data is sent from server to client. What do we mean here? Basically, when data is sent across the web, it is sent in thousands of small chunks. There are multiple reasons why data is sent in small packets. They are sometimes dropped or corrupted, and it's easier to replace small chunks when this happens. Additionally, the packets can be routed along different paths, making the exchange faster and allowing many different users to download the same website at the same time. If each website was sent as a single big chunk, only one user could download it at a time, which obviously would make the web very inefficient and not much fun to use.

&nbsp;

# ***JavaScript Basics*** <hr>

## **What is JavaScript?**

### JavaScript itself is relatively compact, yet very flexible. Developers have written a variety of tools on top of the core JavaScript language, unlocking a vast amount of functionality with minimum effort. These include:

- Browser Application Programming Interfaces (APIs) built into web browsers, providing functionality such as dynamically creating HTML and setting CSS styles; collecting and manipulating a video stream from a user's webcam, or generating 3D graphics and audio samples.


- Third-party APIs that allow developers to incorporate functionality in sites from other content providers, such as Twitter or Facebook.


- Third-party frameworks and libraries that you can apply to HTML to accelerate the work of building sites and applications.

&nbsp;

## <ins>**Language basics crash course**</ins>

&nbsp;

### **Variables**

- Variables are containers that store values. You start by declaring a variable with the let keyword, followed by the name you give to the variable:

- A semicolon at the end of a line indicates where a statement ends. It is only required when you need to separate statements on a single line. However, some people believe it's good practice to have semicolons at the end of each statement. There are other rules for when you should and shouldn't use semicolons.

- You can name a variable nearly anything, but there are some restrictions. 

- JavaScript is case sensitive. This means myVariable is not the same as myvariable. If you have problems in your code, check the case!

- note that variables may hold values that have different data types:

![](/Screenshot%202023-03-01%20at%207.50.21%20PM.png)

### So why do we need variables? Variables are necessary to do anything interesting in programming. If values couldn't change, then you couldn't do anything dynamic, like personalize a greeting message or change an image displayed in an image gallery.

&nbsp;

## <ins>**Operators**</ins>

- An operator is a mathematical symbol that produces a result based on two values (or variables). In the following table, you can see some of the simplest operators, along with some examples to try in the JavaScript console.

![](/Screenshot%202023-03-01%20at%2011.04.55%20PM.png)



#### Question 1. Compose a short poem describing how HTTP sends data between computers.

A. Http it's an amazing thing
    it goes out for a copy
    and brings back the same thing.

&nbsp;

#### Question 2. Describe how HTML, CSS, and JS files are “parsed” in the browser.

A. The browser parses the HTML file first, and that leads to the browser recognizing any < link>-element references to external CSS stylesheets and any < script>-element references to scripts.

As the browser parses the HTML, it sends requests back to the server for any CSS files it has found from < link> elements, and any JavaScript files it has found from < script> elements, and from those, then parses the CSS and JavaScript.

The browser generates an in-memory DOM tree from the parsed HTML, generates an in-memory CSSOM structure from the parsed CSS, and compiles and executes the parsed JavaScript.

&nbsp;
#### Question 3. How can you find images to add to a Website?

A. Use google images or other sources online and copy the link to image and add it in your html.

&nbsp;

#### Question 4 How do you create a String vs a Number in JavaScript?

A. A string is enclosed in double or single quotations and numbers don't have them.

&nbsp; 

#### Question 5. What is a Variable and why are they important in JavaScript?

A. Variables are containers that store values. Variables are important because they allow us to be more creative with the design of a website and helps it to be more interactive.

&nbsp;

# ***Introduction to HTML*** <hr>


## <ins> ***What is HTML***</ins>

- HTML (HyperText Markup Language) is a markup language that tells web browsers how to structure the web pages you visit.

- HTML consists of a series of elements, which you use to enclose, wrap, or mark up different parts of content to make it appear or act in a certain way. The enclosing tags can make content into a hyperlink to connect to another page, italicize words, and so on. 

&nbsp;

## <ins>***Inline vs Block Elements***</ins>

- Block-level elements form a visible block on a page. A block-level element appears on a new line following the content that precedes it. Any content that follows a block-level element also appears on a new line. Block-level elements are usually structural elements on the page. For example, a block-level element might represent headings, paragraphs, lists, navigation menus, or footers. A block-level element wouldn't be nested inside an inline element, but it might be nested inside another block-level element.

- Inline elements are contained within block-level elements, and surround only small parts of the document's content (not entire paragraphs or groupings of content). An inline element will not cause a new line to appear in the document. It is typically used with text, for example an < a> element creates a hyperlink, and elements such as < em> or < strong> create emphasis.

&nbsp;

## <ins>***Void Elements***</ins>

- Not all elements follow the pattern of an opening tag, content, and a closing tag. Some elements consist of a single tag, which is typically used to insert/embed something in the document. Such elements are called void elements. For example, the < img> element embeds an image file onto a page:


&nbsp;


## <ins>***Atributes***</ins>

![](/Attribute%20example.png)

- Attributes contain extra information about the element that won't appear in the content. In this example, the class attribute is an identifying name used to target the element with style information.

An attribute should have: 

- A space between it and the element name. (For an element with more than one attribute, the attributes should be separated by spaces too.)

- The attribute name, followed by an equal sign.

- An attribute value, wrapped with opening and closing quote marks.

Here are a few common attributes.

- href:
This attribute's value specifies the web address for the link. For example: href="https://www.mozilla.org/".

- title:
The title attribute specifies extra information about the link, such as a description of the page that is being linked to. For example, title="The Mozilla homepage". This appears as a tooltip when a cursor hovers over the element.

- target:
The target attribute specifies the browsing context used to display the link. For example, target="_blank" will display the link in a new tab. If you want to display the linked content in the current tab, just omit this attribute.


&nbsp;

## Boolean Attributes

- Sometimes you will see attributes written without values. This is entirely acceptable. These are called Boolean attributes. Boolean attributes can only have one value, which is generally the same as the attribute name. For example, consider the disabled attribute, which you can assign to form input elements. (You use this to disable the form input elements so the user can't make entries. The disabled elements typically have a grayed-out appearance.) For example:

### Questions <hr>

Q1. What is an HTML attribute?

A. a property that contains extra information about the element that won't appear in the content.


Q2. Describe the Anatomy of an HTMl element.

A. 
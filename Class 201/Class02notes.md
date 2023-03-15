# Basics of HTML, CSS & JS <hr>

## <ins>The basics: headings and paragraphs</ins>

&nbsp;

- There are six heading elements: < h1>, < h2>, < h3>, < h4>, < h5>, and < h6>. Each element represents a different level of content in the document; < h1> represents the main heading, < h2> represents subheadings, < h3> represents sub-subheadings, and so on.

- Preferably, you should use a single < h1> per page—this is the top level heading, and all others sit below this in the hierarchy.

- Make sure you use the headings in the correct order in the hierarchy. Don't use < h3> elements to represent subheadings, followed by < h2> elements to represent sub-subheadings—that doesn't make sense and will lead to weird results.

- Of the six heading levels available, you should aim to use no more than three per page, unless you feel it is necessary. Documents with many levels (for example, a deep heading hierarchy) become unwieldy and difficult to navigate. On such occasions, it is advisable to spread the content over multiple pages if possible.

&nbsp;

## <ins>Why do we need Structure?</ins>

- To answer this question, let's take a look at [text-start.html](https://github.com/mdn/learning-area/blob/main/html/introduction-to-html/html-text-formatting/text-start.html)—the starting point of our running example for this article (a nice hummus recipe). You should save a copy of this file on your local machine, as you'll need it for the exercises later on. This document's body currently contains multiple pieces of content. They aren't marked up in any way, but they are separated with line breaks (Enter/Return pressed to go onto the next line).

- Users looking at a web page tend to scan quickly to find relevant content, often just reading the headings, to begin with. (We usually spend a very short time on a web page.) If they can't see anything useful within a few seconds, they'll likely get frustrated and go somewhere else.

- Search engines indexing your page consider the contents of headings as important keywords for influencing the page's search rankings. Without headings, your page will perform poorly in terms of SEO (Search Engine Optimization).

- Severely visually impaired people often don't read web pages; they listen to them instead. This is done with software called a screen reader. This software provides ways to get fast access to given text content. Among the various techniques used, they provide an outline of the document by reading out the headings, allowing their users to find the information they need quickly. If headings are not available, they will be forced to listen to the whole document read out loud.

- To style content with CSS, or make it do interesting things with JavaScript, you need to have elements wrapping the relevant content, so CSS/JavaScript can effectively target it.

&nbsp;
&nbsp;

# Advanced text formatting <hr>

## <ins>Description lists</ins>

- Description lists; The purpose of these lists is to mark up a set of items and their associated descriptions, such as terms and definitions, or questions and answers.

- Description lists use a different wrapper than the other list types — < dl>; in addition each term is wrapped in a < dt> (description term) element, and each description is wrapped in a < dd> (description definition) element.

![](/Screenshot%202023-02-21%20at%201.48.31%20PM.png)
![](/Screenshot%202023-02-21%20at%201.48.06%20PM.png)

### <ins>HTML Questions</ins>


Q. Why is it important to use semantic elements in our HTML?
&nbsp;

A.  Writing semantic HTML makes your code easier to understand, making the source code more readable for other developers.


&nbsp;

Q. How many levels of headings are there in HTML?

&nbsp;

- A. HTML defines six levels of headings.

&nbsp;

Q. What are some uses for the < sup> and < sub> elements?

&nbsp;

- A. to mark up typographical conventions with specific meanings

&nbsp; 

Q. When using the < abbr> element, what attribute must be added to provide the full expansion of the term?

&nbsp;

- A. The title attribute must be added to provide the full expansion of the term.

&nbsp;

### <ins> CSS Questions</ins>

Q. What are ways we can apply CSS to our HTML?

&nbsp;

- A. Inline - by using the style attribute inside HTML elements
Internal - by using a < style> element inside the < head> section.
External - by using a < link> element to link to an external CSS file.

&nbsp;

Q. Why should we avoid using inline styles?

&nbsp;

- A. it does not support (or it has really poor support) for CSS features


&nbsp;

Q. Review the block of code below and answer the following questions:

1. What is representing the selector?

2. Which components are the CSS declarations?


3. Which components are considered properties?

- A. h2 is representing the selector

  B. black and 5px are the components of the CSS declaration.

  C. Color and padding are considered to be the properties.


  ### <ins> JavaScript Questions</ins>

  -  Q. What data type is a sequence of text enclosed in single quote marks?

&nbsp;

    A. It is a string

&nbsp;

    Q.  List 4 types of JavaScript operators.
&nbsp;

    A. Arithmetic Operators, Comparison Operators, Assignment Operators, Conditional Operators.

&nbsp;

    Q. Describe a real world Problem you could solve with a Function.

&nbsp;

    A. You have a subscription service and you want your customer to enter certain fields of information that you need to know. you can create a function that will make them have to fill in certain input areas.

&nbsp;

    Q. An if statement checks a __ and if it evaluates to ___, then the code block will execute.

&nbsp;

    A. condition, True

&nbsp;

    Q. What is the use of an else if?

&nbsp;

    A. to add more choices or outcomes to your if else statement.

&nbsp;

    Q. List 3 different types of comparison operators.

&nbsp;

    A. less than (<), greater than (>), equal to(==)

&nbsp;

    Q. What is the difference between the logical operator && and ||?

&nbsp;

    A. the && operator only returns true when both of its operands are true (and false in all other cases), while the || operator only returns false when both of its operands are false (and true in all other cases)
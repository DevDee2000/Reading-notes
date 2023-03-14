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

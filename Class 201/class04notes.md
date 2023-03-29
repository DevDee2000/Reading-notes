# Readings: HTML Links, JS Functions, and Intro to CSS Layout <hr>


&nbsp;
&nbsp;

# ***Learn HTML***

## <ins>What is a hyperlink</ins>

- Hyperlinks are one of the most exciting innovations the Web has to offer. They've been a feature of the Web since the beginning, and are what makes the Web a web. Hyperlinks allow us to link documents to other documents or resources, link to specific parts of documents, or make apps available at a web address. Almost any web content can be converted to a link so that when clicked or otherwise activated the web browser goes to another web address (URL).

&nbsp;

## <ins> **Anatomy of a link** </ins>

- A basic link is created by wrapping the text or other content inside an < a > element and using the href attribute, also known as a Hypertext Reference, or target, that contains the web address.

## <ins>*Block level links*</ins>

- As mentioned before, almost any content can be made into a link, even [block-level elements](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started#block_versus_inline_elements). If you want to make a heading element a link then wrap it in an anchor (< a>) element as shown in the following code snippet:

![](/Screenshot%202023-02-24%20at%202.54.28%20PM.png)

## <ins>[***Adding supporting information with the title attribute***](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks#adding_supporting_information_with_the_title_attribute)</ins>

- Another attribute you may want to add to your links is title. The title contains additional information about the link, such as which kind of information the page contains, or things to be aware of on the website.

&nbsp;
&nbsp;

## [A quick primer on URLs and paths](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks#a_quick_primer_on_urls_and_paths)

- To fully understand link targets, you need to understand URLs and file paths. This section gives you the information you need to achieve this.

- A URL, or Uniform Resource Locator is a string of text that defines where something is located on the Web. For example, Mozilla's English homepage is located at https://www.mozilla.org/en-US/.

- URLs use paths to find files. Paths specify where the file you're interested in is located in the filesystem. Let's look at an example of a directory structure, see the [creating-hyperlinks](https://github.com/mdn/learning-area/tree/main/html/introduction-to-html/creating-hyperlinks) directory.

- The root of this directory structure is called creating-hyperlinks. When working locally with a website, you'll have one directory that contains the entire site. Inside the root, we have an index.html file and a contacts.html. In a real website, index.html would be our home page or landing page (a web page that serves as the entry point for a website or a particular section of a website.).

- There are also two directories inside our root — pdfs and projects. These each have a single file inside them — a PDF (project-brief.pdf) and an index.html file, respectively. Note that you can have two index.html files in one project, as long as they're in different filesystem locations. The second index.html would perhaps be the main landing page for project-related information.

- Same directory: If you wanted to include a hyperlink inside index.html (the top level index.html) pointing to contacts.html, you would specify the filename that you want to link to, because it's in the same directory as the current file. The URL you would use is contacts.html:

![](/Screenshot%202023-02-24%20at%205.47.01%20PM.png)

&nbsp;
&nbsp;

## <ins>***Link Best Practices***</ins>

### Use clear link wording

It's easy to throw links up on your page. That's not enough.We need to make our links accessible to all readers, regardless of their current context and which tools they prefer. For example:

- Screen reader users like jumping around from link to link on the page, and reading links out of context.


- Search engines use link text to index target files, so it is a good idea to include keywords in your link text to effectively describe what is being linked to.


- Visual readers skim over the page rather than reading every word, and their eyes will be drawn to page features that stand out, like links. They will find descriptive link text useful.

- Don't repeat the URL as part of the link text — URLs look ugly, and sound even uglier when a screen reader reads them out letter by letter.


- Don't say "link" or "links to" in the link text — it's just noise. Screen readers tell people there's a link. Visual users will also know there's a link, because links are generally styled in a different color and underlined (this convention generally shouldn't be broken, as users are used to it).


- Keep your link text as short as possible — this is helpful because screen readers need to interpret the entire link text.

- Minimize instances where multiple copies of the same text are linked to different places. This can cause problems for screen reader users, if there's a list of links out of context that are labeled "click here", "click here", "click here".

&nbsp;


# ***CSS Layout*** <hr>

- Elements on a webpage lay out in normal flow if you haven't applied any CSS to change the way they behave. And, as we began to discover, you can change how elements behave either by adjusting their position in normal flow or by removing them from it altogether. Starting with a solid, well-structured document that's readable in normal flow is the best way to begin any webpage. It ensures that your content is readable even if the user's using a very limited browser or a device such as a screen reader that reads out the content of the page. In addition, since normal flow is designed to make a readable document, by starting in this way you're working with the document rather than struggling against it as you make changes to the layout.

&nbsp;

Q. To create a basic link, we wrap text or other content inside what element?

&nbsp;

A. 
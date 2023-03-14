# Readings: ***Images, Color, Text*** <hr>

&nbsp;

## <ins>How do we put an image on a webpage?</ins>

- In order to put a simple image on a web page, we use the < img> element. This is a void element (meaning, it cannot have any child content and cannot have an end tag) that requires two attributes to be useful: src and alt. The src attribute contains a URL pointing to the image you want to embed in the page. As with the href attribute for < a> elements, the src attribute can be a relative URL or an absolute URL. Without a src attribute, an img element has no image to load.

&nbsp;

## <ins>Alternative text</ins>

- The next attribute we'll look at is alt. Its value is supposed to be a textual description of the image, for use in situations where the image cannot be seen/displayed or takes a long time to render because of a slow internet connection. For example, our above code could be modified like so:

- The easiest way to test your alt text is to purposely misspell your filename. If for example our image name was spelled dinosooooor.jpg, the browser wouldn't display the image, and would display the alt text instead:



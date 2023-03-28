# ***Debugging*** <hr>

&nbsp;

## <ins>*Troubleshooting Javascript*</ins>

&nbsp;

### **Types of error**

- Syntax errors: These are spelling errors in your code that actually cause the program not to run at all, or stop working part way through — you will usually be provided with some error messages too. These are usually okay to fix, as long as you are familiar with the right tools and know what the error messages mean!

- Logic errors: These are errors where the syntax is actually correct but the code is not what you intended it to be, meaning that program runs successfully but gives incorrect results. These are often harder to fix than syntax errors, as there usually isn't an error message to direct you to the source of the error.


### **Fixing syntax errors**

- This is a pretty easy error to track down, and the browser gives you several useful bits of information to help you out (the screenshot above is from Firefox, but other browsers provide similar information). From left to right, we've got:


A red "x" to indicate that this is an error.

An error message to indicate what's gone wrong: "TypeError: guessSubmit.addeventListener is not a function"


A "Learn More" link that links through to an MDN page that explains what this error means in greater detail.


The name of the JavaScript file, which links through to the Debugger tab of the developer tools. If you follow this link, you'll see the exact line where the error is highlighted.


The line number where the error is, and the character number in that line where the error is first seen.

## Notes Questions <hr> 

    Q. Name some key differences between a Syntax Error and a Logic Error.

&nbsp;

    A. Syntax errors occur when you misspell something in your code or for get a punctuation or an empty space, while Logic errors occur when your code is working but not doing what you want it to perform.

&nbsp;

    Q. List a few types of errors that you have encountered in past lab assignments and explain how you were able to correct them.

&nbsp;

    A. I have mostly encountered syntax errors cause I'm always typing too fast and tend to forget letters or semicolons and things of that nature. Thanks to the error messages in the console I was able to identify. 

&nbsp;

    Q. How will this topic continue to influence your long term goals?

&nbsp;

    A. It will give me the knowledge i need in order to correct my code when something is wrong with it.

&nbsp;

    Q. How would you describe the JavaScript Debugger tool and how it works to someone just starting out in software development?

&nbsp;

    A. That the debugger will soon become your best friend when you begin coding and can't figure out what's going wrong in your code. The debugger will help you to quickly identify what and where the problem is.

&nbsp;

    Q. Define what a breakpoint is.

&nbsp;

    A. A breakpoint is a pause in the execution of your code that helps you to find what it is that's preventing your code from running properly.

&nbsp;

    Q. What is the call stack?

&nbsp;

    A. The Call stack section shows you what code was executed to get to the current line.
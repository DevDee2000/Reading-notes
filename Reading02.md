# **Notes on Text Editors** <hr>

## ***What is a text editor?*** <hr>

- A text editor is a piece of software that you download and install on
your computer, or you access online through your web browser, that
allows you to write and manage text, especially the text that you write
to build a web site.

> It's a very important tool for aspiring web developers.


## ***Features to Look For In a Text Editor*** <hr>

- Code completion
- Syntax highlighting
- A nice variety of themes (can help to reduce eye strain and fatigue)
- The ability to choose from a healthy selection of extensions avaiable when you need them.

### **Code completion**: <ins>Code completion</ins> allows you to start typing, and the code completion feature will display possible suggestions based on what you originally typed

 * this will help to save time while typing code by providing a choice rather than typing out the full code and possibly encountering typos

 - Emmet is a shorthand language that can help you write your HTML and CSS more effciently and faster. Some text editors come with it built in and it can also be added via an extension.

 ### **Syntax highlighting**: <ins>Syntax highlighting</ins> is a feature that takes the text you type, and makes it more noticeable by colorizing the text.
&nbsp;



# Using The Software That Already Comes With Your Computer <hr>

- Every computer comes with it's own text editor. On Mac it's called Text Edit.


- Make sure that when you use the text editor that comes on
your computer, that you’re creating code in a plain text editor. You should not see options for making text bold, underlined, or italic.


- If you can make your text bold, underlined or italic, then you might need to change a setting somewhere. Please make sure you’re coding in plain text.


- Make sure that when you use the text editor that comes on your
computer, that you first create a folder on your computer somewhere
(maybe on your Desktop, for example) to store your entire website.
As you create new documents with the text editor that comes on your
computer, save those files in the appropriate folders or sub-folders
within the main website folder.


- Also, please make sure that when you’re saving your file, that they
have the appropriate extension at the end of the file names. For
example, your main HTML file should be called, “index.html.” Your
CSS file should be called something like “style.css.” The filename isn’t
as important as the extension (the “.html” and the “.css”).
&nbsp; 

# **Third Party Options** <hr>

### For the sake of the devices that I have I will only be taking notes on the third parties that are supported by Mac computers
&nbsp;

## **BB Edit** <hr>

- BB Edit is software that you purchase. But BB Edit comes with a 30-day free trial. After the 30 days is over, if you still want the free version, simply continue using BB Edit, and you’ll get the same features as you would have gotten in TextWrangler. If you want the full features in BB Edit, the full cost for a full license is $49.99. Find out more by clicking here [BB Edit link](https://www.barebones.com/products/textwrangler/)

## **Visual Studio Code** <hr>

- Visual Studio Code is a free text editor made by the folks at Microsoft. It is available for Windows computers, Mac computers and Linux computers. VS Code has the Emmet shorthand for HTML and CSS already built-in with no additional work from you at all. VS Code has everything: syntax highlighting, themes, extensions and code completion.

## **Atom** <hr>
- Atom is a free text editor that’s available for download for Windows
computers, Mac computers and Linux computers. Atom is brought to
you by the folks at GitHub . GitHub is a great service online where
you can host and review code, or you can post and get help with the
development of your own projects. Atom also ticks all the right boxes.
It has syntax highlighting, themes, extensions, the works!

&nbsp;
# ***Utilizing the Command Line*** <hr>

## **So what are they exactly?**

- A command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.

- The command line typically presents you with a prompt. As you type, it will be displayed after the prompt. Most of the time you will be issuing commands. Here is an example:

> ls -l /home/ryan
>>total 3
>>>drwxr-xr-x  2 ryan users 4096 Mar 23 13:34 bin
>>>>drwxr-xr-x 18 ryan users 4096 Feb 17 09:12 Documents
>>>>>drwxr-xr-x  2 ryan users 4096 May 05 17:25 public_html

&nbsp;

### Let's break it down: 
- Line 1 presents us with a prompt ( user@bash ). After that we entered a command ( ls ). Typically a command is always the first thing you type. After that we have what are referred to as command line arguments ( -l /home/ryan ). Important to note, these are separated by spaces (there must be a space between the command and the first command line argument also). The first command line argument ( -l ) is also referred to as an option. Options are typically used to modify the behaviour of the command. Options are usually listed before other arguments and typically start with a dash ( - ).

- Lines 2 - 5 are output from running the command. Most commands produce output and it will be listed straight under the issuing of the command. Other commands just perform their task and don't display any information unless there was an error.

- Line 6 presents us with a prompt again. After the command has run and the terminal is ready for you to enter another command the prompt will be displayed. If no prompt is displayed then the command may still be running (you will learn later how to deal with this).

- Your terminal probably won't have line numbers on it. I have just included them here to make it easier to refer to different parts of the material

## **The Shell Bash** <hr>

- Within a terminal you have what is known as a shell. This is a part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you. There are various shells available but the most common one is called bash which stands for Bourne again shell.

- If you would like to know which shell you are using you may use a command called echo to display a system variable stating your current shell. echo is a command which is used to display messages.

> user@bash: echo $SHELL

> /bin/bash

> user@bash:

As long as it prints something to the screen that ends in bash then all is good.

## **Shortcuts** <hr>

- The terminal may seem daunting but don't fret. Linux is full of shortcuts to help make your life easier. You'll be introduced to several of them throughout this tutorial. Take note of them as not only do they make your life easier, they often also save you from making silly mistakes such as typos.

- Here's your first shortcut. When you enter commands, they are actually stored in a history. You can traverse this history using the up and down arrow keys. So don't bother re-typing out commands you have previously entered, you can usually just hit the up arrow a few times. You can also edit these commands using the left and right arrow keys to move the cursor where you want.

&nbsp; 
## ***So where are we?*** <hr>

- The first command we are going to learn is **pwd** which stands for ***Print Working Directory***. (You'll find that a lot of commands in linux are named as an abbreviation of a word or words describing them. This makes it easier to remember them.) The command does just that. It tells you what your current or present working directory is.

- A lot of commands on the terminal will rely on you being in the right location. As you're moving around, it can be easy to lose track of where you are at. Make use of this command often so as to remind yourself where you presently are.
&nbsp; 

## What's in Our Current Location? <hr>

- It's one thing to know where we are. Next we'll want to know what is there. The command for this task is **ls**. It's short for list. 
- Where as pwd is just run by itself with no arguments, ls is a little more powerfful. We have run it here with no arguments in which case it will just do a plain listing of our current location. We can do more with ls however. Below is an outline of its usage:

ls [options] [location]

- In the above example, the square brackets ( [ ] ) mean that those items are optional, we may run the command with or without them.

![Alt text](Screenshot%202023-02-03%20at%202.21.37%20PM.png)

### Let's break it down:

- **Line 1** - We ran ls in it's most basic form. It listed the contents of our current directory.
- **Line 4** - We ran ls with a single command line option ( -l ) which indicates we are going to do a long listing. A long listing has the following:
    - First character indicates whether it is a normal file ( - ) or directory ( d )
    - Next 9 characters are permissions for the file or directory (we'll learn more about them in section 6).
    - The next field is the number of blocks (don't worry too much about this).
    - The next field is the owner of the file or directory (ryan in this case).
    - The next field is the group the file or directory belongs to (users in this case).
    - Following this is the file size.
    - Next up is the file modification time.
    - Finally we have the actual name of the file or directory.
- **Line 10** - We ran ls with a command line argument ( /etc ). When we do this it tells ls not to list our current directory but instead to list that directories contents.
- **Line 13** - We ran ls with both a command line option and argument. As such it did a long listing of the directory /etc.
- **Lines 12** and **18** just indicate that I have cut out some of the commands normal output for brevities sake. When you run the commands you will see a longer listing of files and directories.

&nbsp; 

# ***Paths*** <hr>

## **Absolute and Relative Paths**

- There are 2 types of paths we can use, absolute and relative. Whenever we refer to a file or directory we are using one of these paths. Whenever we refer to a file or directory, we can, in fact, use either type of path (either way, the system will still be directed to the same location).

- To begin with, we have to understand that the file system under linux is a hierarchical structure. At the very top of the structure is what's called the root directory. It is denoted by a single slash ( / ). It has subdirectories, they have subdirectories and so on. Files may reside in any of these directories.

- **Absolute Paths**: Absolute paths specify a location (file or directory) in relation to the root directory. You can identify them easily as they always begin with a forward slash ( / )

- **Relative Paths**: Relative paths specify a location (file or directory) in relation to where we currently are in the system. They will not begin with a slash.

&nbsp; 


![Alt text](Screenshot%202023-02-03%20at%203.44.57%20PM.png)

- Line 1 - We ran pwd just to verify where we currently are.
- Line 4 - We ran ls providing it with a relative path. Documents is a directory in our current location. This command could produce different results depending on where we are. If we had another user on the system, bob, and we ran the command when in their home directory then we would list the contents of their Documents directory instead.
- Line 7 - We ran ls providing it with an absolute path. This command will provide the same output regardless of our current location when we run it.

&nbsp;

## **More on Paths**

You'll find that a lot of stuff in Linux can be achieved in several different ways. Paths are no different. Here are some more building blocks you may use to help build your paths.

- ~ (tilde) - This is a shortcut for your home directory. eg, if your home directory is /home/ryan then you could refer to the directory Documents with the path /home/ryan/Documents or ~/Documents
- . (dot) - This is a reference to your current directory. eg in the example above we referred to Documents on line 4 with a relative path. It could also be written as ./Documents (Normally this extra bit is not required but in later sections we will see where it comes in handy).
- .. (dotdot)- This is a reference to the parent directory. You can use this several times in a path to keep going up the hierarchy. eg if you were in the path /home/ryan you could run the command ls ../../ and this would do a listing of the root directory.

So now you are probably starting to see that we can refer to a location in a variety of different ways. Some of you may be asking the question, which one should I use? The answer is that you can use any method you like to refer to a location. Whenever you refer to a file or directory on the command line you are actually referring to a path and your path can be constructed using any of these elements. The best approach is whichever is the most convenient for you. Here are some examples:

![Alt text](Screenshot%202023-02-03%20at%204.07.08%20PM.png)

After playing about with these on the command line yourself they will start to make a bit more sense. Make sure you understand how all of these elements of building a path work as you'll use all of them in future sections.

&nbsp; 

# Let's Move Around A Bit <hr>
In order to move around in the system we use a command called **cd** which stands for **Change Directory** It looks like this: 

- cd [location]

>Shortcut
>> If you run the command cd without any arguments then it will always take you back to your home directory.

&nbsp;

The command cd may be run without a location as we saw in the shortcut above but usually will be run with a single command line argument which is the location we would like to change into. The location is specified as a path and as such may be specified as either an absolute or relative path and using any of the path building blocks mentioned above.

![Alt text](Screenshot%202023-02-03%20at%204.14.18%20PM.png)

When you start typing a path (anywhere on the command line, you're not just limited to certain commands) you may hit the Tab key on your keyboard at any time which will invoke an auto complete action. If nothing happens then that means there are several possibilities. If you hit Tab again it will show you those possibilities. You may then continue typing and hit Tab again and it will again try to auto complete for you.

It's kinda hard to demonstrate here so it's probably best if you try it yourself. If you start typing cd /hTab/<beginning of your username>Tab you'll get a feel for how it works.

&nbsp;

&nbsp;


## Things I Want To Know More About <hr>
- One of the main things I would love to know more about and get in depth to is utilizing the terminal. It looks very complicated and intricate but I love a good challenge, and the terminal is a challenge that I want to master. 

- I also want to eventually explore the other text editors and see differences between each one of them.
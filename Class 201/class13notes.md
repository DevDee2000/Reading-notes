# ***Local Storage and How to use it on websites*** <hr>

&nbsp;

## <ins>Adding State to the web: the "Why" of local storage</ins>

- The main problem with HTTP as the main transport layer of the Web is that it is stateless. This means that when you use an application and then close it, its state will be reset the next time you open it. If you close an application on your desktop and re-open it, its most recent state is restored.

- This is why, as a developer, you need to store the state of your interface somewhere. Normally, this is done server-side, and you would check the user name to know which state to revert to. But what if you don’t want to force people to sign up?

- This is where local storage comes in. You would keep a key on the user’s computer and read it out when the user returns.

&nbsp;

## C is for Cookie. Is That Good Enough for me?

The classic way to do this is by using a cookie. A cookie is a text file hosted on the user’s computer and connected to the domain that your website runs on. You can store information in them, read them out and delete them. Cookies have a few limitations though:

- They add to the load of every document accessed on the domain.

- They allow up to only 4 KB of data storage.

- Because cookies have been used to spy on people’s surfing behavior, security-conscious people and companies turn them off or request to be asked every time whether a cookie should be set.

&nbsp;

## Using Local Storage in HTML5 Capable Browsers

- Using local storage in modern browsers is ridiculously easy. All you have to do is modify the localStorage object in JavaScript. You can do that directly or (and this is probably cleaner) use the setItem() and getItem() method:

![](/Screenshot%202023-03-21%20at%201.38.09%20PM.png)

- If you read out the favoriteflavor key, you will get back “vanilla”:

![](/Screenshot%202023-03-24%20at%2010.14.58%20AM.png)

To remove the item, you can use — can you guess? — the removeItem() method:

![](/Screenshot%202023-03-24%20at%2010.16.38%20AM.png)

&nbsp;


Q. Why would a developer use local storage for a web application?

&nbsp;

A. Because local storage allows developers to retrieve and store data in the browser without it expiring if the tab or window is closed.

&nbsp;

Q. What information should not be stored in local storage?

&nbsp;

A. Personal information such as social security numbers, banking information, etc

&nbsp;

Q. Local storage can store what type of data? How would you convert it to that type before storing?

&nbsp;

A. It can only store strings and in order to convert it to that before storing you would have to use the method Stringify.
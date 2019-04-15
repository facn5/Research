# Full-stack Architecture

Separation of Concerns (SoC)

Client-side vs. Server-side

Alternative back-end technologies

Writing for different environments



---




## Separation of Concerns (SoC)

### What is it?
SoC means separating a program into sections, so each handles a separate concern.

A program with good SoC is called a modular program

---


### What are the benefits?

SoC can take a bit more time to set up at first, but the resulting code is: 
* more readable, with less cognitive load.
* easier to maintain, reuse, and upgrade

This means saving time and money.


---



![spaghetti code](https://craftofcoding.files.wordpress.com/2013/10/pi_forspaghetti.jpg)


---



![old rich guy](https://i.pinimg.com/originals/20/49/27/204927c4fee53e783163b022690c9759.jpg)




---


### How do you do it?

Encapsulation (information hiding) inside a section of code.

Layered designs: presentation layer, business logic layer, data access layer, persistence layer.


---


## Decisions

Unless you are building a very simple app such as a page only using API calls with cURL, you will need server side.

This raises a choice: server-side or client-side for the various features?

The choice between client- or server- side is not always black-and-white.  It depends.  Some general guidelines:


---


## Quick Review

### Front-end or Client-side
* Usually smart phones, laptop, desktop.
* Browsers, HTML, CSS, JavaScript

### Back-end or Server-side
* A server computer.
* Also JS, plus Python, C#, PHP, SQL, etc.  Some crossover/exceptions.

Tech is very similar now, only the roles are different.  Client computer requests info from server which delivers/returns it.


---


## Server-side (Back-end)


* Database access
* Security and authentication
* Validation of user inputs
These can be duplicated, but not replaced, on Client-side
* Business logic*

ex: basic password validation on client-side, but secure authentication happens on server-side


---




## Client-side (Front-end)

* UI rendering*
* UI logic, changing the look
* Basic validation
* Business logic*


---



Business logic used to be all back-end, but with complex sites it may be handled more on the front-end.

Webpage rendering depending on the situation may be done more on the back-end or front-end.


---



## Client-side pros and cons

### Client-side pros
* Rich site interactions
* Fast website rendering after the initial load.
* Great for web applications.
* Robust selection of JavaScript libraries.

### Client-side cons:
* Low SEO if not implemented correctly.
* Initial load might require more time.
* Client-side code may be manipulated/insecure, or not run if not supported



---


## Server-side pros and cons

### Server-side pros
* Search engines can crawl the site for better SEO.
* The initial page load is faster.
* Great for static sites


---




### Server-side cons:
* Frequent server requests.
* An overall slow page rendering.
* Full page reloads.
* Non-rich site interactions.



---


## Client-side vs. server-side rendering:

Some trade-offs:  Server-side rendering of web pages may be better for SEO, as the content is present before you get to it.

Your website won't be able to load until ALL of the JS is downloaded to the browser, so it might be slow if the user has a slow connection or the page is very large.



---




## Client-side rendering of web pages 
This means getting a bare-bones HTML document, with a JS file that will render the rest of the site using the browser.  This is relatively new style that didn't become popular until JS libraries started using it, like React and Vue.

Clicking a JS link uses JS to load the content, rather than reloading the page.  Example:


## Example
```
<!DOCTYPE html>
 <html>
 <head>
   <meta charset="utf-8">
  <title>Example Website</title>
</head>
<body>
  <div id="root">
    <app></app>
  </div>
  <script src="https://vuejs.org"type="text/javascript"></script>
  <script src="location/of/app.js"type="text/javascript"></script>
</body>
</html>
```



---



## Advanced Considerations

* How long do you have to build it?

* Is slightly longer load time ok?

* Do you have time to build separate components? (SOA - service oriented approach)

* How skilled are you?


---


## Conclusion

Client-side can be more insecure and you can easily expose data.  

Server-side security is well-documented, and frameworks may also be more mature.  Building client-side inefficiently will result in poor UX anyway.  Each one affects the other


--- 

# Alternative back-end technologies

### Why Node.js

### The Pros:

---

#### One Environment

Using JavaScript on a web server as well as the browser reduces the impedance mismatch between the two programming environments which can communicate data structures via JSON that work the same on both sides of the equation. Duplicate form validation code can be shared between server and client, etc.

---

### Popularity and community

A lot of people already know JavaScript, even people who do not claim to be programmers. It is arguably the most popular programming language. So a popular language means a popular community. Big community means easy to get help or support if you
get stuck doing something.

---

### Easy to learn
Node is not something new. It’s just simple JavaScript. So the JavaScript developers don’t have to put much extra effort to learn Node, Also, there are many interactive tutorials available on GitHub which makes the learning experience more pleasant and fast.

---

### The Cons :

#### Not suitable for heavy computing apps
Node.js doesn’t provide scalability. One CPU is not going to be enough; the platform provides no ability to scale out to take advantage of the multiple cores commonly present in today’s server-class hardware.

---

### Callbacks
Every time using a callback end up with tons of nested callbacks.

---

### Alternative  technologies to Node.js

### ASP.NET Core
ASP. NET Core is the second most popular alternative, alot of people use and like this framework, it's an open source framework for building backend and web apps and services and IOT apps, it's one of the most used frameworks It seamlessly integrates with popular client-side frameworks and libraries


---

#### Vert.x
Eclipse Vert.x is event driven and non blocking. This means your app can handle a lot of concurrency using a small number of kernel threads. Vert.x lets your app scale with minimal hardware.

while Vert.x also provides non-blocking methods which run asynchronously, the thing with Node.js is that it also does the same, but It's also better than any other alternative.

---

### Why?
for the simple fact that you can write the same language for backend and front-end
if you're using node so you don't have to learn any new language
and you don't have to get used to it and this is why in my opinion
it's the best option to choose for now.

---

 ### Javascript in the Front End vs Back End
 
 Javascript is a programming language. It is not a backend, frontend,. It's just a programing language that can be used on both.
 
 ---
 
 ### There are two run time environment for this language.

First one is V8 which is installed on your browser like chrome to run the code in there which is basically running JS on the front end.

---

Second one is called Node which is designed to run the code on your operating system without a need of browser.

---

Even though it's the same programming language,Each environment, browser or OS has their own dependencies. You cannot run any code written in Javascript interchangeably on both environments.

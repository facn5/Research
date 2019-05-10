# Research day topics
Research day should be thought of as a [spike](http://www.extremeprogramming.org/rules/spike.html) to help with your end-of-week project

## Week 1 - Toolkit
### Command Line
* Customise your command line to make it pretty and useful (ie. git branch/branch status parser)
* Install using a package manager
* Create a "workshop", designed to walk the rest of your cohort through the steps (this doesn't need to be long - just one markdown file)
### Regular Expressions
* How to use regex
* (basic) pattern creation and repetitions
* (advanced) groups
* Find and use on-line tools such as regex101
* Create a code snippet using regex such as (for example) email validator:
 * us3r1@foundersandcoders.com
 * user must start with an alphabetical character;
 * user can contain also other characters (which ones?);
 * site and user are always separated by a snail/small duck/AT symbol (@);
 * site is always done with at least 3 alphabetical characters, a dot and at least 2 more alphabetical characters
### Accessibility
* Write an accessible navbar
* Write an accessible modal
* (Hint: think about semantic HTML, managing focus, adding key handlers, adding aria attributes)
* Refactor one of your team's websites (or one from the rest of your cohort if necessary) to reflect what you've learned
### CSS
* Responsive vs mobile-first design
* How to write CSS with BEM
* Refactor one of your team's websites to reflect what you've learned

## Week 2 - Testing
### Unit vs integration testing
* What is a unit test?
* What is an integration test?
* When would you use each kind of test?
### Technical spikes
* What are technical spikes?
* When and why would a spike be useful?
* How would you successfully spike on a topic?
* Give an example of how a spike could have helped with last week's projects.
### DOM manipulation
* How can you use JavaScript to create an HTML element and then add it to your webpage? How would you replace an existing element with it?
* How would you add a <li> element to the start of a <ul>?
* What is a JavaScript Event? What does event.preventDefault() do and why might you use it?
* What is a NodeList? How is it different from an Array?
* What are the security concerns around Element.innerHTML and what could you use instead?
### Test coverage
* What is test coverage?
* Why is test coverage useful?
* What are Istanbul and nyc?
* How would you use them to improve your testing?
* Use Istanbul/nyc to calculate your code coverage for the TDD workshop.
  
## Week 4 - Node Core Week 1
### Topic 1: Architecting
* Separation of concerns: What kind of tasks are normally handled in the back end, and which are more usually handled in the front end? Why?
* Client side vs server side: Some tasks – such as templating and validation – can be implemented on either the client or the server. What are the pros and cons of running code on the client, rather than the server (and vice versa)?
* Alternative back-end technologies: Which other technologies (programming languages and servers) might be used instead of Node on the back end? What are some of the pros and cons of using Node in your stack, rather than one of those alternatives?
* Writing for different environments: Why might you have to write JavaScript differently if it's going to run in the browser, rather than in Node? What tools can help bridge the gap?
### Topic 2: Engineering
* Modules: Why is it a good idea to modularise your code? What are require and module.exports? Why can't you use them in the browser? How might you modularise client-side code?
* Asyncronous functions: Why should you use asyncronous forms of functions wherever possible in Node? What are error-first callbacks, and why is it important to follow that pattern in your own code? Why should you avoid using throw in callbacks? When might you use the syncronous form of a function instead?
* Input/output (the fs and path modules): What kind of tasks does the fs module enable you to perform that you wouldn't be able to in the browser? What are some of the issues of working with paths when accessing a file system? How does the path module help, and why should you use it instead of manually writing file paths as strings?
* Working with URLs (the url and querystring modules): What is a urlObject and how is it structured? Why is it important to be able to turn JavaScript objects into querystrings and back again? Why is it a bad idea to build a query string manually from other strings (think about URL encoding and escape characters)?
### Topic 3: Packaging
* Dependencies: What is a dependency? Why might you want to use a dependency in your project, rather than writing the code from scratch? What have traditionally been some of the issues with managing dependencies?
* NPM: What is a package manager? How does it help with dependencies? What is package.json, and what does npm init do? How do you use an installed package in your code?
* npm install: What is the difference between installing a package globally, installing it as a dependency, or installing it as a development dependency? When would you use each? How would you do each in the command line? Why is it normally a bad idea to install a package globally?
* Package files: Where does NPM install packages? Why is it important to make sure that installed packages aren't included in your repositories? How do you prevent Git from including these files in your repository?
### Topic 4: Deploying
* Cloud platforms: What is PaaS? Why is it useful to be able to deploy your code to a cloud platform, rather than running it locally? What services are there that can provide you with a platform for your code? Heroku is a good start, but try to find some others. If you have time, try to deploy a simple server to Heroku as a demo.
* Environment variables: Why might some variables in your code need to change for different environments? Why is it a bad idea to include those variables in a public repository? What modules might you use to help manage environment variables? (Look at env2 from our neighbours at DWYL.) If you can, write some sample code to show how it works.
  
## Week 5 - Node Week 2
### Node Shell project
* Using the instructions here, create your own test output formatter (a test output formatter is a program that when you pipe the results of your tests into, will read the results of those tests and provide you with useful information about them e.g. tap-spec, tap-nyan)
* (Bonus) Publish your package to npm
### Continuous Integration
* Research what Continuous Integration is and what assurances it can provide when building an application.
* Create a basic Node project on Github that includes some tests with Tape, then sync your project with an online CI tool. 
* Add a new feature to your project, commit your changes, then check on your CI tool to ensure your tests are still passing and your project build is passing. A popular tool is Travis, this excellent tutorial will come in handy.
* (Bonus) after verifying the latest changes, display the build .svg file provided and display it at the top of your projects' README.md file.
### Streams and Buffers
* Research what streams and buffers are in Node, how are they used in conjunction?
* Create a file streamFile.js, so that when a user runs the command node streamFile.js bigtextfile.txt, it streams the contents of the file to the users terminal.
* Need a big file? How about a book.
* To start with, you could hardcode the file path bigtextfile.txt into the js file instead of passing it as a command-line argument.
* (Bonus) Allow an additional argument to be provided in the command to specify a time interval of how often a chunk of text from the file is streamed to the terminal. E.G node streamFile.js bigtextfile.txt 1s
### Make a request from the server
* Research what npm modules are available to make a request from a node server to another server (equivalent of XMLHttpRequest for the server).
* Using a module of your choice, create a node server which makes a request to an online API (it's up to you what one you'd like to use, I'd recommend either Unsplash.it, Guardian, Tesco, or Recipe Puppy), then serve the response when a client requests the home ('/') route of your server.
* (Bonus), when the server receives the API response, instead of serving the response at the home route, make another GET request to a different API, then combine that response with the original response and serve it to the home route.
  
## Week 6 - PostgreSQL
### Schemas and relationships
* What is a schema and why/when would you need one?
* What are primary keys and why do we need them?
* Create a visual representation of a mock schema for a database about Founders & Coders, using as many different kinds of relationship as you can. Explain the logic behind it.
### Database setup and maintenance
* What is a build script and why do you need one? (think ahead to how this might come in useful when working on a project this week)
* What is database migration?
* Create a build script for a simple database (one or two tables only), which you can run locally. Check that it works for you and everyone on your team
### Script injections / safety issues
* What is a script injection and how do these happen?
* How would you prevent script injections?
* Prepare a short demonstration of good (and bad?) practices, including some sample code

## Week 7 - Authentication
### HTTP vs HTTPS
* How does HTTPS work? What are TLS/SSL certificates?
* Why is this important to implement in your projects?
* Demo how to generate certificates and use them in a node project
### Stateless vs stateful authentication
* What is session based authentication (stateful) vs token based authentication (stateless)?
* Draw flow diagrams to show the steps involved in each process
* What are the advantages and disadvantages of each?
### Web storage
* What are local storage and session storage and what is the difference between the two?
* Why would you use cookies vs local/session storage?
* Demo a simple usage of localStorage and sessionStorage
### Attacks
* What are the following types of attack?
* Man In The Middle (MITM)
* Cross Site Scripting (XSS)
* Cross Site Request Forgery (CSRF)
* How can you defend against each of them?

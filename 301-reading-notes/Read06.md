# What Is Node.js?

Node.js is a runtime environment* for executing JavaScript code, and it is built on the Chrome V8 engine. It is asynchronous, which means that it does not have to wait for one process to complete before starting another one. Like V8, Node.js is free and open-source. Unlike V8, it does not have built-in sandboxing.
(Those familiar with JavaScript will note the '.js' file extension; however, this is purely an aesthetic choice for the runtime environment's name to indicate its association with JavaScript and does not mean that Node.js is a JavaScript file.)
The Node.js runtime is: the software stack responsible for installing your web service's code and its dependencies and running your service.And it environment is the software environment in which code is executed.

# Node Is Built on Google Chrome’s V8 JavaScript Engine:

## The V8 engine is :
the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers, including Brave, Opera, and Vivaldi. It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute.
However, when we say that Node is built on the V8 engine, we don’t mean that Node programs are executed in a browser. They aren’t. Rather, the creator of Node (Ryan Dahl) took the V8 engine and enhanced it with various features, such as a file system API, an HTTP library, and a number of operating system–related utility methods.
This means that Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.

## What is npm?

NPM is a package manager for Node. js packages, or modules if you like. www.npmjs.com hosts thousands of free packages to download and use. The NPM program is installed on your computer when you install Node.js. NPM is already ready to run on your computer!

## Installing a Package Globally:

In the terminal ,type the following:
npm install -g jshint
This will install the jshint package globally on your system.

## Installing a Package Locally:
We can also install packages locally to a project, as opposed to globally, on our system. Create a test folder and open a terminal in that directory. Next type this:
npm init -y

This will create and auto-populate a package.json file in the same folder. Next, use npm to install the lodash package and save it as a project dependency:
npm install lodash --save

# What Is Node.js Used For?

Node. js is primarily used for non-blocking, event-driven servers, due to its single-threaded nature. It's used for traditional web sites and back-end API services, but was designed with real-time, push-based architectures in mind.
And if you want to start developing apps with any modern JavaScript framework (for example, React or Angular), you’ll be expected to have a working knowledge of Node and npm (or maybe Yarn). This isn’t because you need a Node back end to run these frameworks. You don’t. Rather, it’s because these frameworks (and many, many related packages) are all available via npm and rely on Node to create a sensible development environment in which they can run.

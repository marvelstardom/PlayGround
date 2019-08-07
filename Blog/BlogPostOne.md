---
title: Blog Post One
---

# VUE JS

REACT
React is a javascript library that is used to build user interfaces.
It was created by facebook in instagram
JSX(Javascript and XML)- Allows us to use html syntax and allows us to programme.
ReactDOM - It takes a list of html and displays it as a target.

Download Reactmin, react-dom-min, browser-min.

A Component is one of the main building block of React. Thry're just a part of your website. An entire app in react is made up of components. A comp is a react class. Whenever you make a component, make sure you return only one parent div.
In order to make a comp name appear more than once, create a div in the reactDOM.render() and paste the comp name as many times as you want it to appear.
Every single compo can only return one parent element.

Properties allows you to customize your own components.

All what components do is that they basically return some html.
We display props using curly braces{}.
     
```A Prop is an html attribute that we can pass in to customize our comp in pretty awesome ways.```

Children Property is just any data that is in between the opening tag and closing tag.

Chrome Web Store Extensions-> React-Detector
React Developer Tools
To open developer tools on a web, windows- ctrl+shift+j

DOM is the structure of html that makes up a webpage. React made updating the DOM by making use of DOM Diffing. DD compare rendered content with the new ui changes. React optimizes this by making only the minimal changes necessary. DD compares javascripts objects and it is faster than writing to or reading from the dom. Whenever we use getelementbyid, we are reading from the dom. when we change classes, contents, we are writing to the dom.

Backbone is a framework or library. In backbone, we render the same data over and over again even when the changes haven't happened everywhere. 
This re-rendering slows down our app a lot. 
With React, only the minimak changes would be rendered, this is really efficient.

run npm init to generate our project.
Enter a name, version and description, entry point: index.js, skip test command, enter author and also a lincense.
Package.json describes our project as well as dependendies.
Next: install babel cli- npm install --save-dev babel-cli.

flag: --out-file.

WEBPACK: this is a module bundler that helps us to create static files and automates processes that need to happen before your files go into production. Wbpack will run several commands to create a bundle file. BABEL packages scripts, dependencies together into one file i.e one request.

test: /\.js$/ : any files that have a .js extension. 

STATE
States can change.
Whenever something is going to stay the same, use properties... Whenever it's going to change, use states.

"onClick, onChange" an example of an event handler.


<!-- <vue-disqus shortname="PlayGround" :identifier="$page.post.title"></vue-disqus> -->

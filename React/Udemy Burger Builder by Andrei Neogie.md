## Background
React can be used with any tech stack which is rendered by any browser (mobile, Android & iOS, desktop browser) so long as the tech stack incorporates javascript. 

## Keywords
Virtual DOM. The browser touches the DOM elements. I.e. renders a virtual DOM.
‘State’ is like a javascript object which stores the data of the app.
Props. 
‘Components’ are built with JSX (HTML-like syntax with Javascript). Component is a self-contained piece of code that returns some visual UI.
Component tree


## There is 1 way data flow in React.
React library is like a function which accepts Components & state, and renders a ‘virtual DOM’ which is a Javascript rendering of DOM(-like) objects. This gives the browser a blueprint of how it should update the DOM.  


As soon as state changes, React reacts to the change - it combines the new state (new data) with existing components & rerenders the DOM. I.e. state trickles down. State can live in different components. The state can not move up to parent components, only down to child components. 


## Create React App
I think it puts in the 2 React javascript libraries, and enables your react code to be read/compiled to create the virtualDOM which is rendered by the browser. I.e. create-react-ap installs the react library into your solution/project, & gets the virtual DOM ready for you to use as the interface/UI/frontend/DOM of the solution/project/application. creat-react-app is a comfortable environment to learn React & also build a single page application. 

Download Visual Studio Code
Download git bash (& if you like, you can access git bash terminal from the Visual Studio Code terminal).
Download node package manager
Download npm

Inside the git bash terminal, type the following to see what version I have installed.
node -v    
npm -v   

yarn & npm are pretty much substitute package managers. Not to be confused with YAML 


npx create-react-app monsters-rolodex
cd monsters-rolodex  
npm start

npm install -g cowsay
cowsay hello 
npm list -g cowsay
npm uninstall -g cowsay


If I look at the package.json file, inside my monsters-rolodex, I can see there are 3 testing libraries, which may be useful, we will look at it later, and also, any other libraries.

src folder is the entry point for my react app. It is where npm start goes and looks as soon as I run the app. The src folder is where I save the UI views etc. 


## index.js 
index.js is the place where the react app looks first. When index.js is first created, it by default, contains the following imports for useful libraries -  
import React from ‘react’;    is the engine which helps allow the app to have functions etc.
import ReactDOM from ‘react-dom’;    is tool which specifies that the React engine should create the virtual DOM for a web-browser apps. (i.e. instead of ReactDOM, we might import ReactNative for native mobile apps). 
import ‘./index.css’;
import App from ‘./App’;
import reportWebVitals from ‘./reportWebVitals’;


ReactDOM.render(
<React.StrictMode>     
	<App />
</React.StrictMode>,
document.getElementById(‘root’)
);

<React.StrictMode></React.StrictMode> means whatever is inside the strict mode tags will be checked for old deprecated code & you will be given warnings that you are not developing with the latest syntax. E.g. some functions might be deprecated or not supported in the newest version of React.


The index.html file is inside the public folder & this has the app’s entry point i.e. has the ‘root’ div element. <div id=’root’></div>

## Some random info about React
All React components live inside the ReactDOM.render(); function & you can have sibling plain old HTML elements outside that ReactDOM.render() function too, which will display on the page outside of the React elements.

React is very, very fast because all the front-end code is saved to the HTML, js, and css files which are served to the client & it’s very fast. When you host the app in production somewhere, you can actually serve users/clients the build version of the app, which is more optimized i.e. white text is gone. See the build version by going to the build folder > index.html

Sometimes, some browsers can not understand React, so the ‘react build’ library/package also uses ‘babel’ & ‘webpack’ under the hood to convert the React syntax to plain, old-school javascript. Thus, the built version of my app can be rendered by all these different browsers, because the ‘react build’ library/package takes care of this. Webpack modularizes/chunks up the javascript files of my React app, and just sends appropriate chunks when the user needs it i.e. the javascript related the the Homepage, when the user wants the home page, and the js related to some other page, when the user needs the other page.

React with redux versus React with hooks. I believe redux was the old way, and hooks are the new way. Classes (i.e. class components) are an old way too. Hooks is too React-specific whereas classes are ubiquitous throughout programming languages & some old React libraries only use classes. The oldest, plainest way is functional components rather than class components. So, I think in terms of oldest to newer/higher-order React syntax, we have:
1. Functional components
2. Class Components
3. Redux
4. Hooks 


## Class Components

To write class components, we need to import the component library from react i.e. at the top of the js file which is going to be written as a class component (i.e. put this import {Component} at the top of the App.js file, which represents the <App /> component, which is referenced/called as <App /> in index.js) type the following:
import { Component } from ‘react’; 

class App extends Component {
render() {
return (
		<div className = ‘App’>
			<header className=’App-header’>
			…..blah…..
</header>
</div>
);	
}

}


N.b. if this wasn’t a class component, and it was instead written as an ordinary functional component in JSX, it would just be:
function App() { 
 … and no render() {} method around the following return
return (
	<div className = ‘App’>
		<header className=’App-header’>
		…..blah…..
</div>
)
}

## (Component) State
Now let’s use the concept of ‘state’ in React to make our page dynamic. 

Edit App.js which is the file where we define the <App /> Class Component. In App.js we write JSX-virtual-DOM-like syntax, and this constitutes <App />. As a side note, remember that we rewrote App.js (the file which defines <App />) as a class component in the section above, because previously it was a functional component.  

class App extends Component {
 	render() {
	return (
	<div className = ‘App’>
		<header className=’App-header’>
			<img alt=‘logo’ src={logo} className=’App-logo’ />
			<p>Hi Sheila!</p>
			<button>Change Name</button>
</header>
	</div>
);
}
} 

## Constructor method
All javascript classes have a particular method that we are about to use - the constructor method. A constructor method gets called first, before all other methods, whenever the class is instantiated. 

The react library has modified the constructor method in all (React) component classes. So when you call the constructor method from a component class 
(like class App extends Component {
	constructor() {
	super();
}
})
 you get a slightly different behavior in a React class component versus a regular JS class. 

 
n.b. super(); above is doing something like calling the constructors of all the base classes, I’m not 100%sure, but something like this. Just call super(); here, in the constructor, and it’s unlikely to be wrong.  

## Initializing state inside a react component class’s constructor
The bit which is special & unique in the constructor of a React-component-class, versus a regular JS class, is this - a React component class is looking for you to set state. 

class App extends Component {
	constructor() {
		super();
		
this.state = {}  i.e. an empty object
}

render() {
….
}
}







class App extends Component {
	constructor() {
this.state = {
       name: ‘Sheila’ see here we have a key:value pair within the state object
};
}
	
	render() {
		<img src={logo} alt=’logo’ className=’myImg’>
		<p>Hi {this.state.name}</p>
		<button onClick={() => {
			this.state.name = ‘Sara’;
			this.setState({name: ‘Sara’});	causes React to rerender by having a completely new state object in-memory, whereas this.state.name = ‘Sara’; does not cause browser to rerender
}}>Change Name</button>
}
}


Inside of JSX we can access JS variables with curly braces so long as the variable is within scope in the place we are trying to access it from. JSX is JavaScript Extended, which I guess is the syntax used in a javascript file which has HTML-like-syntax in the JS (functional & component) classes, in the JS functions,  in the JS file. The HTML-like-syntax is things like <img className=’myName’/> and <p></p>
JS variables can be accessed throughout the JS file so long as the variable is in scope. I can think of two kinds of JS variables off the top of my head 
1. properties of classes (which might be variable variables, or might be static variables) and 
2. variables declared with the let or var keywords. 
You can access some property of the class in the render() {} method of the class since that property will most likely be set in the constructor of that class (I think), and I think the property is in scope for methods of the class.   

## Update State using SetState
There are 3 ways to update a component’s state using SetState. You can
pass in new values for the key (i.e. shallow merge the new value to the state)
pass a new object for the key (  “              “                “  new object to    “   ) asynchronous
or pass a function to SetState. 
E.g. <button onClick = {() => {this.setState(  () => {},    () => {}   function, callbackFunctin
         );
 	}         
 }
       > 
Click Me!
        </button>

In the first function of SetState, return an object, which contains the new values for state. E.g. 
this.setState( (state, props) => {return { name : {firstName : ‘Sara’ , lastName : ‘Sweetie’}}},  
          () => {}    )
A callback function is simply a function which will run after the SetState function has run. 
The ideal way to use SetState() is to pass SetState a function to update the state as the first parameter, and optionally pass SetState a callback function as the second parameter i.e. 
SetState(  () => {}  ,   () => {} ).  Furthermore, you return the new state values in the first parameter function i.e.
SetState(   () => {  return {} },    () => {}  ) 


## Using an array as the value for state, and also a JSX (map) function in the render method to map over the array & render the array values iteratively
TODO-flesh out what pieces of code go in each file. 
In index.html
<div id = ‘root’></div>

In index.js 
import React from ‘react’;
Import ReactDOM from ‘react-dom’
ReactDOM.render(
	<App />
	, document.getElementById(‘root’);
)



In App.js
class App extends Component {
constructor() {
 	super();
this.state = {
	monsters : [{name: ‘Sam’, id:‘1’}, {name: ‘Jake’, id:‘2’}, {name: ‘Preethi’, id:‘3’}]
};
},


render() {
	return(
<div className = ‘App’>
	{
	this.state.monsters.map( (monster) => { 
		return {
	<h1 key={monster.id} >{monster.name}</h1>
}
});
}
	</div>
)
}

} 


## Lifecycle Methods

componentDidMount() is a React method which is available to me in a component, similar to how the render() method is available and how the constructor method is available. 

‘Mounting’ is the first time a component gets placed onto the DOM. componentDidMount() only happens/runs 1 time in the entire life/existence of the component. ‘Fetch’ is also a react function which is available which goes to the specified URL & returns with a JSON. e.g:



Lecture 35 - component did mount







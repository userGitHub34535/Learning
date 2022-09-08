## React - freeCodeCamp course by Bob Ziroll ##


Let’s build a static web page in React.

Imperative is like a recipe - do this, then this then =this & logic is strewn in programmer’s mind. Declarative programming is to say "this = some definition"



(functional) components use <PascalCase /> 


I can clean up child-components/components into their own folders. Naming convention: make sure you name the file as the same name as the component which is the same name as the js function.
I.e.
 ComponentFileName.js = function ComponentName() {} = <ComponentName />
Where ComponentFileName = ComponentName



Step 1. define/type up/create your JSX (looks like HTML, using className rather than class)
Step 2. Create a function called MyComponentName
Step 3. Return the JSX from MyComponentName
Step 4. Create a file called MyComponentName.js, and put the above function/functional-component inside it
Step 5. Export default MyComponentName at the bottom of the file MyComponentName.js or do export default MyFunctionName() {} at the definition of the Component.
I believe ‘default’ is what is used when there is only one component defined in the file. 
Step 6. import MyComponentName from ‘./…path…to…/MyComponentName’


N.b. import & export is a js es6 feature, also used by React. 
You can export in plain js, by doing as follows, at the bottom of the js file (after the functions and the classes). You can type 
export {myClass, myFunction. myVariable} etc. 


As a side note, something to be aware of is that JavaScript uses a compiler, bundler, and a minifier under the hood. Babel is a js compiler. Webpack is a bundler, and maybe a minifier too?
Create-react-app has most of the webpack configuration done under the hood. If I were to create my own react app without the scaffolding, maybe I’d configure Webpack for my production environment. 



In manifest.json I did  "theme_color": "#18161b", //"#000000"
  "background_color": "#d5c3ef" //"#ffffff"





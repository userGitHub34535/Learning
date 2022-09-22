## JS Set ##

Can create at new set with var mySet = new Set(); //this is an empty set
Can also create a Set using an array i.e. var mySet = new Set([“a”, “b”, “c”]);
mySet.add(“d”);
mySet.has(“e”); //returns false because e is not in mySet.
A set is a collection of UNIQUE values. So mySet = new Set(“a”, “a”, “b”, “a”);  creates a set containing just “a” and “b” of size 1. 
N.b. the mySet.length property does not exist; the mySet.size property exists. 

## JS Objects ## 
You can see if something is a key in an object by doing if(myKey in myObj) {}

## Some array methods I want to paractice a lot - forEach, map, reduce, filter, sort, ?every?. ##


When using a curly brace { in a JS ES6 lambda function, you MUST explicitly use the "return" keyword. If you just need to return a single line from the lambda function, have no curly braces, and instead just return the single line from the function, with no "return" key word. JS won't even throw a compile time error if you miss this return - it will simply compile and then not do the process you were expecting/or in react, not render the component that you were expecting to be returned. 

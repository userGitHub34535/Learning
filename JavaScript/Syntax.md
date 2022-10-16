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


## const ##
Declare a variable as a const when you do not want to point this variable name to a different object at any later time. const means that the reference to a location in memory (pointer) never changes after you initially declare the const variable. This is why when an object or an array is declared as a const, then you can update the values within the object or array, but you can not reassign the variable-name to some other object/array/value. Const doesn’t quite mean that the variable value is immutable, but rather that within the given scope, the variable-name can not be reassigned to a new location in memory. When JS "let" primitive datatype variables are updated from one value to some other value, I believe that JavaScript creates a new location in memory and reassigns the variable name to this new location in memory, thus, the variable is updated; I do not beleive that JS updates the value stored at the previous location in memory.  

 


## Export and Import ##
todo

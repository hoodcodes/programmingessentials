##### JavaScript


“You should imagine variables as tentacles, rather than boxes. They do not contain values; they grasp them—two variables can refer to the same value.” 
― Marijn Haverbeke, Eloquent JavaScript: A Modern Introduction to Programming

Interesting facts - 

JavaScript is:
* a dynamically-typed language so you do not need to specify return types.
* a functional language 
* Created by Brendan Eich, while at Netscape 
* cannot read files nor write to them on the file system of the computer
* is loosely typed, except on Switch statements
* semi-colon is optional.  so on return statements be sure to have the opening { curly brace on the same line as the return keyword.  example:  what does this return?

function foo() {
   return
   {
      foo: 'bar'
   }
}

Answer:  undefined.  why?  

* 

Equals:  Use '===' which will not only compare values but enforce type is the same.  Safer than '=='

var obj = {};  // this is an object literal  


In 2005, Jesse James Garrett coined the term AJAX 

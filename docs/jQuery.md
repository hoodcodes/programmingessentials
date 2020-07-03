Reference:
https://www.youtube.com/watch?v=QHf0t8gQ8RQ  
https://www.tutorialspoint.com/jquery/index.htm  

What is JQuery?
A JavaScript library built to provide powerful productivity aids for a JavaScript developer.  
Everything you can do in JQuery, you can absolutely do in JavaScript.  Bec/ - it’s JavaScript after all.  JQuery methods get parsed and fleshed out into JavaScript
native JS will always be faster 



What is the $ symbol?    
Shorthand Function selector.  Same as calling:   JQuery.  These are equivalent below:
$(“#MyId)
JQuery(“#MyId”)
document.getElementById(“MyId”)

Principle features of JQuery?
Event handling 
Special widgets (these are generally plugins - many UI related.  e.g accordian, datapicker, progress bar, menu, button… u name it there is probably something for your need)
Animation and effect support (e.g. show, hide, slide up, slide down, toggle, fade in, fade out etc)
Good alternative to flash  
have not worked w flash
flash requires recompilation following changes, JQuery does not.
flash requires expensive software for compiling 
JQuery supports reader accessibility
Strong AJAX support
HTML DOM manipulation
can bind multiple event handlers in a single method

What is the has() method?
a selection filter.  Checks to see if an element ‘has something’.  
$(‘myDiv’).has(‘ol’);  
selects all elements with ‘ol’

Can JQuery parse XML?
actually yes, with $.parseXML(xml);

Is JQuery supported on all major browsers and platforms?  
yes  
How to debug JQuery?
use a debugger; keyword just before line you are debugging 
use Dev Tools on your browser 
write out console.log statements
use alert box 

when would you want to use $.noConflict(); ?
if multiple JS frameworks make use of the $ shortkey, you can use this to handle this - several different methods.  
example: MooTools - Prototype also uses $() as their global function and to define variables 
I have never used it.

Method Chaining - 
as name suggests, chaining multiple methods - executed in sequence (as a single statement)
$(“#myDiv”).text(“My Text”).css(“color”.”red”).removeClass(“myClass”);

Redirecting a page with JS and JQuery
url = "https://www.cnn.com";
$(location).attr("href", url);

Check to see if element hidden or visible
use is() method
$(“#MyElement”).is(“:visible”);

using ‘return false’ with JQuery event handlers:
calls preventDefault()  - stopping execution
calls stopPropagation() - stopping event from bubbling up  
note: in NON-JQuery handlers, calling ‘return false’ does not stop event from bubbling up

Most common JQuery events
click()
dblclick()
mouseenter()
mouseleave()
mousedown()
mouseup()
focus()


document.ready() function is called immediately after the DOM is loaded.

body.onload() called when everything gets loaded on the page that includes DOM, images and all associated resources of the page. 

types of selectors:
#ID  $(“#myId”);  - selects the element with this Id
.Class  $(“.myClass”); - selects the element(s) with this class name
Universal (*)
Multiple elements E, F, G
Attribute Selector  $(“div”); - selects all elements of this type 


Popular CDNs for JQuery
Google
Microsoft
jQuery

Benefits of CDN
reduces load on your server
saves bandwidth
most important:  it will be cached if user has visited any site which is using jQuery framework from any of these CDNs.

What does $(“div.parent”) select?
all the elements with the parent class

Fastest selectors in jQuery?
ID
element

Slowest selectors in jQuery?
Class selectors are slow compared to ID and element

How are jQuery selectors executed?
last selectors executed first
e.g. $(“p#myElementId .myClass”);
above:  .myClass elements are found first, then all elements not containing p#myElementId are removed

Difference between $(this) and ‘this’ in jQuery?
they are the same element
only difference is that when wrapped in $() the power of jQuery is available on it.

--------------------------------------------------------

How to check if element is empty?
2 ways

using “:empty” selector.
if ($(‘#myId’).is(‘:empty’)){ do this }

using “$.trim()” method
if ($.trim(‘#myId’).html())==’’){ do this }

How to check if an element exists or not in jQuery?
use jQuery length property
if ($(‘#myId’).length > 0) { do this }


What is the use of jQuery.each() function?
used to iterate over a jQuery object.  Can be used to iterate over any collection, whether it is an object or an array.

What is the difference betw jQuery.size() and jQuery.length?
.size() method returns number of elements in object.  Not preferred however.
.length does the same thing.  does NOT have the overhead of a function call

How to create new div?
$(‘<div/>’)
use append or prepend to add it to the DOM tree
append adds it to last position of parent
prepend adds it to first position of parent
example: $('#parent').append('<div>hello</div>');

Difference between parent() and parents()
parent() travels only one level in the DOM tree,
parents() searches thru whole DOM tree

Difference between eq() and get()
eq() returns element as jQuery object
get() returns a DOM element. (not wrapped by jQuery)

Difference between .empty(), .remove() and .detach() 
each of them remove elements from the DOM - but they are different
.empty() - removes all child elements of the matched element
.remove() - removes all the matched elements from the DOM
.detach() - same as .remove(), but it keeps all the jQuery data associated with the removed elements.  Useful if the elements are to be ‘reinserted’ into the DOM at some point


explain .bind() vs .live() vs. .delegate() vs .on()
each are useful for attaching events to selectors or elements.  But each are different
.bind() - easiest and quick method to bind events.  does not work for elements added dynamically later.  Only adds to all current elements.  Performance issues when dealing with large selection
.live() - deprecated.  overcame issueof .bind() and works for dynamically added elements or future elements
.delegate() - similar to .live() but instead of attaching the selector/event information to the document, you can choose where it is anchored.  Supports chaining  
.on() - provides all the benefits of the other 3 methods and brings uniformity for attaching event handlers

how to create clone of any object 
clone() provides deep copy of the set of matched elements (the elements and all their decendant elements and text nodes)
example:  $(‘#myId’).clone().appendTo(‘body’);
events on a cloned object are NOT copied by default.  Pass (true) if you want events copied as well:
example:  $(‘#myId’).clone(true).appendTo(‘body’);


difference between prop and attr?
attr() - gets value of an attribute for the first element in the set of matched elements.
prop() - gets value of a property for the first element in the setof matched elements
attributes carry additional info about HTML elements and come in name/value pairs
attr() - gives value of element as it was defined in the HTML on page load.
Always recommended to use prop() to get values of elements which is modified via javascript/jquery - as you get element’s current state


Difference between event.stopPropagation and event.stopImmediatePropagation?
event.stopPropagation  - allows other handlers on the same element to be executed
event.stopImmediatePropagation  - prevents every event from running

How to attach event to element which should be executed only once?
one() method
example:  $(‘#myId’).one(“click”,function(){  stuff to do });
like - if you wanted to have an alert message only fire one time max 
How to retrieve # of rows in a gridview?
$(‘#myGrid’).length;

How to attach keydown event to element?
$(‘#myId’).keydown( function() { stuff to do });

How to disble cut, copy & paste in Textbox?
$(‘#myTextboxId’).bind(‘copy paste cut’, function(e){ e.preventDefault(); }); });

How to discable mouse right click?
$(this).bind(“contextmenu”, function(e){ e.preventDefault();   }); });  

How to disable Browser Back Button
 window.history.forward(1) or window.history.forward(-1)

How to encode / decode URL?
 encodeURIComponent(url)
decodeURIComponent(url) 

Is there any advantage to using $.ajax() as opposed to $.get() or $.post() ?
$.ajax() offers more functionality (namely error callbacks)
$.get() and $.post() are higher level abstractions that are often easier to understand and use














EXTRA CREDIT:  jQuery ( sad face ) refresher.  since i live in this world currently - just a foundational review of this stuff.  created Quizlet set of flashcards . https://quizlet.com/_6nwaf8 . 



possible article / blog post material....  

React (2011) by Jordan Walke at Facebook.  Built in response to the need for:
	• better performance
	• <finishMe>

Purpose:  For building dynamic, high performing, responsive UI to your web interfaces

So what is it?
	• React is a View library.  Not an application library.  If it was part of an MVC project, it would be the V portion.
	• React's goal is in many ways to render HTML on a web page.  It accomplishes this with the ReactDOM.render() method.
	• React uses CSS.  As such you can use Sass
	• Encourages the DRY principle (Don't Repeat Yourself) by enabling the creation of reusable UI components
	• <finishMe>

Using abstractions to build things enables the concept of reuse.  We can build a UI component and reuse it, and this results in faster and more consistent development of a UI.  <finishMe>

Features:
	• uses a real programming language, JavaScript, to render views instead of HTML templates as other web app UIs have traditionally used
	• Unifies the markup with the corresponding view logic.  
	• Unidirectional data flow.  Not bi-directional (e.g. Angular)
	• Uses Flux architecture (considered a variant of the observer pattern). A popular implementation of this is Redux.
		○ Action - responsible for describing what has taken place
		○ Dispatcher - sends action to the store to perform updates <verify>
		○ Store - the single source of truth.  Can be thought of as models.
		○ this pattern is sometimes expressed as "properties flow down, actions flow up"
	• <finishMe>
	
How does React work?
	• Through a process called Reconciliation.
	• We of course have our DOM.  
	• <verify>  We also have a 'virtual dom' - or copy of of the DOM.  This always contains the most recent changes to the DOM.  We use it to do comparisons of changes.
	•  Then, let's say the user takes action. Anything, such as set some toggle from True to False.  That action sets in motion a set of events that result ultimately in a call to 'render' on a componet.  
	• Here is where reconciliation begins.  The output of that component may be different than what was last rendered.  Therefore we take the new compare the new 'render' result (what the code should look like) against the virtual DOM's last version of what it looked like, and if it is different - then a minimal set of changes to the DOM are applied.  The shadow DOM and actual DOM are updated.  That is how React is so fast - we are only changing what must be changed, nothing else.  


--------------------------------------------------------------


Topics for Studying React

Topics for Studying React - what they teach in a 2 day workshop.  as an idea for things to become proficient in React….

<ins>Topics<ins>
What it means to be declarative
Composing behavior and explicit state with Higher-Order Components and Render Props
Composing behavior and implicit state with createContext and cloneElement
When to use a higher order component vs. a render prop vs. context vs. cloneElement, and the trade-offs that come with each choice
Dodging CSS and accessibility issues with Portals
Building accessible components using ARIA
Ref forwarding and Focus Management
New Lifecycles (getSnapshoBeforeUpdate, getDerivedStateFromProps) and how to get off the old ones
Async React Preview (Suspense, Time Slicing)
Real-world examples for all topics

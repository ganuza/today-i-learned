#### Node
* A node generally refers to an element in the component tree
* This could be a React element, text, or even another component
* Nodes represent individual units within the virtual DOM that React uses to efficiently update the actual DOM

#### What is a Node in React.js
*  A node in React is any JavaScript object that React can render as part of the UI

#### Nodes can be:
* React elements ( `<div>`, `<span>`, etc )
* Components (both functional and class components)
* Plain text
* Fragments, which let you group multiple nodes without adding extra elements to the DOM

#### How Nodes Are Used In the Virtual DOM
* When you write components, React creates a virtual representation of the DOM (React elements) as a tree of nodes
* React then uses this virtual DOM tree to efficiently apply updates by comparing the current and previous node states
* Only nodes with changes are updated in the actual DOM, which boosts performance

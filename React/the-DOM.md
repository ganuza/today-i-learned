### Real DOM
* the DOM (Document Object Model) is a programming interface for web documents
* it represents the structure of a web page as a tree of objects (nodes) that can be manipulated by JavaScript
* Directly manipulating the DOM is very slow, especially if there are many elements or complex operations, since every change to the DOM causes a rerender

### React's Virtual DOM
* lightweight, in-memory representation of the real DOM
* when the state of a component changes, React changes the virtual DOM first
* React reconciles the current version of the virtual DOM with the previous version and ONLY updates the parts of the real DOM that changed
* Benefit: React is fast and efficient

### Shallow DOM
* Shallow DOM: Not a DOM type, but a concept used in React testing to render a component without its children for isolated testing

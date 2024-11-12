#### Fragments:

* A Fragment in React is a special component ( <></> ) that let's you group a list of children elements without adding extra nodes to the DOM
* This is especially useful when you want to return multiple elements from a component but avoid wrapping them in unnecessary <div> or other container element, which can clutter the DOM structure and may affect layout and styling

#### Why Use Fragments?
* Avoid Unnecessary Markup: You don't have to add extra `<div>` tags, with keeps the DOM cleaner
* Improves Performance: By not adding extra nodes, you can reduce the number of elements in the DOM, which can improve performance
* Better CSS Styling: Additional container elements can sometimes interfere with styling, so fragments help you avoid this issue

#### You can use EITHER <React.Fragment> or the shorthand syntax <>...</>

#### When to Use Fragments
* In Component Return Statements: When returning multiple elements from a component
* To Avoid Wrapper Elements: Useful when you want ot add multiple sibling elements without a parent wrapper like a <div>

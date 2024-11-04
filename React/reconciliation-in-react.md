#### Reconciliation

* The process by which React updates the DOM to match the virtual DOM as a result of changes in the component state or props
* It is how React efficiently figures out how to apply the minimal number of changes necessary to update the UI
* React compares the previous virtual DOM with the new virtual DOM and then determines the difference or 'diff' between the two, only updating what's necessary

#### How It Works

* Virtual DOM Creation:  when a component's state or props change, React creates a new virtual DOM tree
* Diffing Algorithm:  React compares the new virtual DOM with the previous one.  React uses heuristics to speed up the process
  * Element Type Changes: if an element's type changes, React will destroy the old DOM node and create a new one
  * Keyed Elements: For lists of elements, React uses the key attribute to identify elements uniquely and update them appropriately, which minimizes re-rendering
* Updating the DOM: React applies only the changes necessary to make the DOM match the new virtual DOM

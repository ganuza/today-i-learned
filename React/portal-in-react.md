### Portals

* A portal in React is a way to render a component outside of the main DOM hierarchy of its parent component
* By default, a React component renders into the DOM subtree that is rooted by its parent component
* Sometimes you need a component (like a modal, tooltip, or dropdown) to visually appear outside of the parent container but still remain part of the React tree for event handling, such as closing modals or capturing clicks
* Also useful for avoiding CSS constraints like overflow or z-index
* This is where portals come in

#### How Portals Work

* A portal lets your render a child component to a DOM node outside of the parent component's hierarchy

#### Why Use a Portal?
* Modals, Tooltips, and Dropdowns:  These UI elements often need to appear above other components
* Escape CSS Constraints:  Elements that need to break out from parent containers that have styles like overflow: hidden or low z-index

#### Why This is Powerful:
* CSS Issues Solved: You can bypass overflow: hidden and z-index issues by rendering modals outside of the parent container.
* Event Handling Works: Even though the modal is outside the normal DOM tree, it remains part of the React component tree, meaning state, props, and events behave normally.

#### State
* What it is: A built-in React object used to manage data that is local and mutable within a component
* Who controls it: State is fully controlled by the component itself
* Use case: State is used when the component needs to track and manage changes to its data over time, such as user inputs, toggling elements, or API responses
* Can it be passed?: State cannot be passed directly to other components. However, you can pass it down as props to child components

#### Props
* What it is: Props (short for 'properties') are used to pass data from a parent component to a child component
* Who controls it: Props are controlled by the parent component and are read-only in the child component
* Use case: Props are used for communication between components, allowing data or functions to be passed from the parent to the child
* Can it be passed?: Yes, props are explicitly designed to pass data between components

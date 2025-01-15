#### 1. constructor(props)
* The constructor is a special method in JavaScript classes, including React class components.
* It is called before the component is mounted.
* It is primarily used for initializing state and binding event handlers.
#### 2. super(props)
* In a class component, if you define a constructor, you must call super(props) before using this.
* super(props) calls the constructor of the parent class (React.Component), allowing access to this.props inside the constructor.
* Without super(props), this would be undefined when accessing this.props or this.state.
#### 3. render()
* The render method is required in all class components.
* It returns the JSX that defines what should be rendered on the screen.
* The render method should be pure, meaning it should not modify state or directly interact with the DOM.

#### Pure Component
* A pure component in React is a component that renders the same output given the same state and props
* React provides a built-in optimization for pure components by using shallow comparison for `props` and `state` to decide whether the component needs to re-render
* Pure components help improve performance by avoiding unnecessary re-renders
  - if neither the `state` nor the `props` change, React skips the rendering process

#### Key Points
1. Shallow Comparison
  * React performs a shallow comparison of `state` and `props` in a pure component to determine if a re-render is necessary
  * A shallow comparison checks if the references to the objects have changed, but not their deep quality
2. Avoiding Side Effects
  * A pure component should not rely on or introduce side effects that might affect the output of `render`

#### Implementing Pure Components: 2 ways to create a pure component
1. Using `React.PureComponent`
2. Using Functional Components with `React.memo`

#### Example: Pure Component with `React.PureComponent`
```
import React, { PureComponent } from 'react';

class PureExample extends PureComponent {
  render() {
    console.log('PureExample rendered');
    return (
      <div>
        <p>Count: {this.props.count}</p>
      </div>
    );
  }
}

export default PureExample;
```

#### Example: Pure Component with `React.memo`
```
import React from 'react';

const PureExample = React.memo(({ count }) => {
  console.log('PureExample rendered');
  return (
    <div>
      <p>Count: {count}</p>
    </div>
  );
});

export default PureExample;
```

#### Parent Component to Demonstrate
* Here's a parent component that changes the count and passes it as a prop to the pure component above
* Unnecessary renders are avoided when the count does NOT change, but the text DOES
* If React.memo was not implemented, the PureExample component WOULD re-render since in React, child components re-render whenever the parent does

```
import React, { useState } from 'react';
import PureExample from './PureExample';

const ParentComponent = () => {
  const [count, setCount] = useState(0);
  const [text, setText] = useState('');

  return (
    <div>
      <button onClick={() => setCount(count + 1)}>Increment Count</button>
      <button onClick={() => setText(text + '!')}>Change Text</button>
      <PureExample count={count} />
    </div>
  );
};

export default ParentComponent;
```

#### When to Use Pure Components
* React by default will re-render a Child component if a Parent component re-renders, unless explicitly optimized
* Use pure components when you want to prevent unnecessary renders for performance optimization
* Be careful if you are passing complex objects as props, since shallow comparison checks only the reference, not the content
  - For deeply nested objects, consider using tools like React.memo with a custom comparison function


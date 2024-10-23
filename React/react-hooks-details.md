### Hooks are functions that let us 'hook' into React's state and lifecycle features from functional components

#### useState

Purpose:
  * manages state in a functional component
  * returns a state value and a function to update it

```
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0); // Initialize state with 0

  return (
    <div>
      <p>Current count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}

export default Counter;
```

Key Points:
  * State persists between renders
  * The component re-renders when setCount updates the state

---

#### useEffect

Purpose
  * handles side effects such as data fetching, event listeners, or updating the DOM
  * can run after every render, only on mount/unmount, or when specific dependencies change

```
import React, { useEffect, useState } from 'react';

function DataFetcher() {
  const [data, setData] = useState([]);

  useEffect(() => {
    fetch('https://jsonplaceholder.typicode.com/posts')
      .then((response) => response.json())
      .then((json) => setData(json));

    // Cleanup function example (unmounting)
    return () => console.log('Component unmounted');
  }, []); // Runs only once (on mount)

  return (
    <ul>
      {data.map((item) => (
        <li key={item.id}>{item.title}</li>
      ))}
    </ul>
  );
}

export default DataFetcher;
```

Key Points:
  * runs after render and optionally on dependency changes
  * cleanup functions are helpful for event listeners or subscriptions

---

#### useMemo

Purpose:
  * memoizes the result of a function to avoid expensive recalculations unless dependencies change

```
import React, { useMemo, useState } from 'react';

function ExpensiveComponent({ num }) {
  const [count, setCount] = useState(0);

  const expensiveCalculation = useMemo(() => {
    console.log('Calculating...');
    return num * 2;
  }, [num]); // Only recalculates when `num` changes

  return (
    <div>
      <p>Expensive value: {expensiveCalculation}</p>
      <button onClick={() => setCount(count + 1)}>Increment Count: {count}</button>
    </div>
  );
}

export default ExpensiveComponent;
```

Key Points:
  * Avoids unnecessary recalculations.
  * Useful for performance optimization in components with heavy computations.

---

#### useCallback

Purpose:
  * memoizes a function itself (vs the result of a function as in useMemo) to prevent it from being recreated on every render
  * useful when passing callbacks to child components to prevent unnecessary re-renders

```
import React, { useCallback, useState } from 'react';

function ChildComponent({ onClick }) {
  return <button onClick={onClick}>Click me!</button>;
}

function ParentComponent() {
  const [count, setCount] = useState(0);

  const handleClick = useCallback(() => {
    console.log('Button clicked');
  }, []); // `handleClick` remains the same across renders

  return (
    <div>
      <p>Parent count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment Count</button>
      <ChildComponent onClick={handleClick} />
    </div>
  );
}

export default ParentComponent;
```

Key Points:
  * Prevents unnecessary re-renders of child components by memoizing function references.
  * Often used with React.memo() to optimize rendering.

---

#### useRef

Purpose:
  * Holds a mutable reference to a DOM element or any value across renders.
  * Does not cause re-renders when the referenced value changes.

```
import React, { useRef } from 'react';

function InputFocus() {
  const inputRef = useRef(null);

  const handleFocus = () => {
    inputRef.current.focus(); // Access the input element directly
  };

  return (
    <div>
      <input ref={inputRef} type="text" placeholder="Click the button to focus me" />
      <button onClick={handleFocus}>Focus Input</button>
    </div>
  );
}

export default InputFocus;
```

Key Points:
* Useful for direct DOM manipulation or keeping mutable data across renders.
* The value inside useRef persists between renders without triggering a re-render.

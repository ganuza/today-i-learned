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

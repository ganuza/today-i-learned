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

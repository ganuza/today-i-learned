#### Implementing componentWillUnmount using useEffect
* componentWillUnmount is used to clean up resources when a class component in unmounted
* in a function component, you use the useEffect hook with a cleanup function
* In the useEffect, the componentWillMount part happens in the code before the return
* The equivalent of componentWillUnmount is achieved by returning a cleanup function inside the useEffect

#### How It Works
1. Mount behavior: The code inside the useEffect (before the return statement) will run when the component mounts.
2. Unmount behavior: The returned function (inside the useEffect) runs when the component is unmounted or before the next render (if dependencies change).

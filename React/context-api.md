#### React Context API
* React Context API is a feature in React that provides a way to share values like themes, user info, or configuration settings between components
* React Context API was released in 2018 to avoid prop drilling by simplifying state management and making sharing data across the component tree more efficient and error-free

#### Prop Drilling
* The problem with prop drilling is that, as the app grows in complexity, passing data through multiple levels of components can become messy, cumbersome, and error-prone
  * In larger applications, prop drilling can make the code harder to maintain and understand
  * Each intermediary component must be aware of the props it needs to pass down, even if it does not use them
  * Intermediary components that do not use the props might still re-render when the props change, leading to performance issue

#### How does the Context API work?
* Context API provides a means to share vlues like state, functions, or any data across the component tree without passing props down manually at every level
* This is particularly useful for global data that many components need to access

#### How to use it
* Use createContext() method to create a new context
  * This function returns a context object with 2 components: a Provider and a Consumer
    * Provider
      * Used to wrap the part of the your component tree where you want the context to be available
      * It accepts a compulsory Value prop that holds the data you want to share across other components
      * When the Value prop of the Provider changes, all descendants that consume the context will re-render
    * Consumer
      * Allows any descendant component to use the context
      * It takes a function as a child, where the function argument is the current context value
      * the useContext hook is often used instead of Consumer for better readability and simplicity

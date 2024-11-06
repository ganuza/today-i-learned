#### StrictMode

* a React tool that helps identify potential issues i your application, especially as it relates to best practices and future compatibility
  * StrictMode can be particularly useful for spotting potential problems with the code as you develop, helping ensure that your app runs more reliably
  * When enabled, it doesn't render any visible UI changes but enforces checks and warnings to help improve the code quality

#### Key things StrictMode does:
* Warns about deprecatied lifecycle methods: It flags old lifecycle methods that are not recommended for use
* Checks for potential side effects in render phase: Helps identify side effects that could cause unexpected behaviors
* Detects unexpected behavior in asynchronous operations: It makes certain async behaviors more predictable

#### How it Helps
* Suppose you have a deprecated lifecycle method in one of your class components, like componentWillMount
  * When wrapped in StrictMode, React will log a warning in the console letting you know this method is deprecated and sugget alternatives
* If there is a side effect that's causing re-renders or impacting performance, StrictMode can flag it, allowing you to address these issues early in development

Using StrictMode in your development process is a great way to ensure that your code is robust and ready for future updates in React

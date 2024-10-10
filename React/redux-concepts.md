### Redux Concepts
* Store: A single source of truth for your application's state.
* Actions: Objects that describe what happened in the app. An action is typically a plain JavaScript object with a type field (a string) and optionally a payload containing data.
* Reducers: Functions that specify how the state changes in response to an action. A reducer takes the previous state and an action, and returns the next state.
* Dispatch: The way you trigger an action to modify the state in the store.
* Selectors: Functions that allow components to retrieve specific parts of the state from the store.

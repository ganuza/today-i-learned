### Redux
* Redux is a state management library, to handle and manage the state of your application in a predictable and centralized manner.
* It helps applications scale by allowing developers to store and manage the state in a single 'store' that can be accessed and updated across different parts of the appplication, rather than having multiple disconnected pieces of state spread throughout the component tree
### Redux Workflow
* A user interacts with the app, triggering an action (e.g., clicking a button).
* The action is dispatched to the store.
* The store passes the action to the reducer, which calculates the new state.
* The new state is stored, and any component subscribed to the store is updated with the new state.

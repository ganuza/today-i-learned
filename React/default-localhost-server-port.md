#### Default Localhost Server Port
* In React.js, the default localhost server port is 3000
* When you run a React app using `npm start` or `yarn start`, the development server usually starts on `http://localhost:3000`

#### 2 methods to change the local server port
1. In your project's `package.json` file, you can specify a custom port by addng the `PORT` environment variable before the start command in the `"scripts"` section

```
// package.json
"scripts": {
  "start": "PORT=4000 react-scripts start"
}
```
  In this example, the server will run on `http://localhost:4000`

2. Create a `.env` file in the root of your project and add the `PORT` variable there
  * React will read this file and use the specified port

```
// .env
PORT=4000
```
  * After creating or updating the `.env` file, start your React app with `npm start` or `yarn start`
  * The server will now run on the specified port, like `http://localhost:4000`
  * This flexiblility with ports is helpful if you need to run multiple React apps simultaneously or if port 3000 is already in use

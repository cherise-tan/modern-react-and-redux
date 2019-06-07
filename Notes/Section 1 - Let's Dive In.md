# Section 1 - Let's Dive In

### Creating our First React App
* https://codepen.io/sgrider/pen/yRWZEq: CodePen url for a tiny React App
     * Need to add "react" and "react-dom" as libraries

### What is React?
* React is a JavaScript library
* Its ultimate purpose is to show content (HTML) to users and handle user interaction
* React can work by itself, but can also work with a great variety of other packages, libraries, servers and databases
* React COMPONENTS are made using either JavaScript CLASSES or FUNCTIONS
     ```class App extends React.Component {}```

#### JSX
* Looks like HTML and can be placed in javascript code
* Determines the content of our React app, just like normal HTML

#### Event Handlers
* Can use components to create an event handler
* Event handlers are used to detect user interaction and respond to it

### Using create-react-app
* In the command line:
     ```npm install -g create-react-app```
     ```create-react-app jsx``` -> where 'jsx' is te name of the created app
* Alternate command:
     ```npx create-react-app <name of project>```
     * Allows you to create a react app without going through the 'npm install' process
* Commands:
     * ```yarn start``` -> starts the development server
     * ```yarn build``` -> bundles the app into static files for production
     * ```yarn test``` -> starts the test runner
* Dependencies include: Webpack, Babel, Dev Server

#### Babel
* Not all browsers have support for ES6

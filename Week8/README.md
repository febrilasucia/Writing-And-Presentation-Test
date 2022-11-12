# **Writing and Presentation Test**

## **REACT JS**

---

### **React Router**

---

#### What is that React Router?
*React Router* is a standard library for routing in React. It enables the navigation among views of various components in a React Application, allows changing the browser URL, and keeps the UI in sync with the URL.

#### Configuring The Router
-  Install
 `npm i react-router-dom` to install React Router
- Configuring 
The easiest step by far is setting up your router. All you need to do is import the specific router you need (`BrowserRouter` for the web and `NativeRouter` for mobile) and wrap your entire application in that router.
main.js
```javascript
import React from "react"
import ReactDOM from "react-dom/client"
import App from "./App"
import { BrowserRouter } from "react-router-dom"

const root = ReactDOM.createRoot(document.getElementById("root"))
root.render(
  <React.StrictMode>
    <BrowserRouter>
      <App />
    </BrowserRouter>
  </React.StrictMode>
)
```
- Defining
App.js
```javascript
import { Route, Routes } from "react-router-dom"
import { Home } from "./Home"
import { BookList } from "./BookList"

export function App() {
  return (
    <Routes>
      <Route path="/" element={<Home />} />
      <Route path="/books" element={<BookList />} />
    </Routes>
  )
}
```

- Handling Navigation
```javascript
import { Route, Routes, Link } from "react-router-dom"
import { Home } from "./Home"
import { BookList } from "./BookList"

export function App() {
  return (
    <>
      <nav>
        <ul>
          <li><Link to="/">Home</Link></li>
          <li><Link to="/books">Books</Link></li>
        </ul>
      </nav>

      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/books" element={<BookList />} />
      </Routes>
    </>
  )
}
```
#### Advance Route Definition
This can be done through five main techniques.

1. Dynamic Routing
The simplest and most common advanced feature in React Router is handling dynamic routes.
App.jsx
```javascript
<Routes>
  <Route path="/" element={<Home />} />
  <Route path="/books" element={<BookList />} />
  <Route path="/books/:id" element={<Book />} />
</Routes>
```
OtherPage.jsx
```javascript
import { useParams } from "react-router-dom"

export function Book() {
  const { id } = useParams()

  return (
    <h1>Book {id}</h1>
  )
}
```
2. Routing Priority
When we were just dealing with hard coded routes it was pretty easy to know which route would be rendered, but when dealing with dynamic routes it can be a bit more complicated. Take these routes for example.
```javascript
<Routes>
  <Route path="/" element={<Home />} />
  <Route path="/books" element={<BookList />} />
  <Route path="/books/:id" element={<Book />} />
  <Route path="/books/new" element={<NewBook />} />
</Routes>
```
While we are on the topic of routing priority I also want to talk about how to create a route that matches anything.
```javascript
<Routes>
  <Route path="/" element={<Home />} />
  <Route path="/books" element={<BookList />} />
  <Route path="/books/:id" element={<Book />} />
  <Route path="/books/new" element={<NewBook />} />
  <Route path="*" element={<NotFound />} />
</Routes>
```

3. Nested Routes
How do they handle route nestin? This nesting is pretty simple to do. All you need to do is make a parent Route that has the path prop set to the shared path for all your child Route components. 
```javascript
<Routes>
  <Route path="/" element={<Home />} />
  <Route path="/books">
    <Route index element={<BookList />} />
    <Route path=":id" element={<Book />} />
    <Route path="new" element={<NewBook />} />
  </Route>
  <Route path="*" element={<NotFound />} />
</Routes>
```
4. Multiple Routes
Another incredibly powerful thing you can do with React Router is use multiple Routes components at the same time. This can be done as either two separate Routes components or as nested Routes.
```javascript
import { Route, Routes, Link } from "react-router-dom"
import { Home } from "./Home"
import { BookList } from "./BookList"
import { BookSidebar } from "./BookSidebar"

export function App() {
  return (
    <>
      <nav>
        <ul>
          <li><Link to="/">Home</Link></li>
          <li><Link to="/books">Books</Link></li>
        </ul>
      </nav>

      <aside>
        <Routes>
          <Route path="/books" element={<BookSidebar />}>
        </Routes>
      </aside>

      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/books" element={<BookList />} />
      </Routes>
    </>
  )
}
```
## REDUX
 
### What is that Redux
Redux is a predictable state container for JavaScript apps, and a very valuable tool for organizing application state. It’s a popular library to manage state in React apps, but it can be used just as well with Angular, Vue.js or just plain old vanilla JavaScript.
In this brief introduction to Redux, we’ll go over the main concepts:

1. Reducer
A reducer is a pure function that takes the previous state and an action as arguments and returns a new state. Actions are an object with a type and an optional payload:
ex : 
```javascript
function myReducer(previousState, action) => {

  return newState;
}
```
2. Action
Actions are plain JavaScript objects that represent payloads of information that send data from your application to your store. Actions have a type and an optional payload.
```javascript
export function addTodo({ task }) {
  return {
    type: 'ADD_TODO',
    payload: {
      task,
      completed: false
    },
  }
}

// example returned value:
// {
//   type: 'ADD_TODO',
//   todo: { task: '🛒 get some milk', completed: false },
// }
```
3. Store
In Redux, the store refers to the object that brings actions (that represent what happened) and reducers (that update the state according to those actions) together. There is only a single store in a Redux application.
```javascript
import { createStore } from 'redux';
import todoReducer from './reducers';

const store = createStore(todoReducer);
```

## Async Actions with Middleware and Thunk

### Using Middleware to Enable Async Logic
Let's look at a couple examples of how middleware can enable us to write some kind of async logic that interacts with the Redux store.
```javascript
import { client } from '../api/client'

const delayedActionMiddleware = storeAPI => next => action => {
  if (action.type === 'todos/todoAdded') {
    setTimeout(() => {
      // Delay this action by one second
      next(action)
    }, 1000)
    return
  }

  return next(action)
}

const fetchTodosMiddleware = storeAPI => next => action => {
  if (action.type === 'todos/fetchTodos') {
    // Make an API call to fetch todos from the server
    client.get('todos').then(todos => {
      // Dispatch an action with the todos we received
      storeAPI.dispatch({ type: 'todos/todosLoaded', payload: todos })
    })
  }

  return next(action)
}
```

### Writing an Async Function Middleware
Both of the middleware in that last section were very specific and only do one thing. It would be nice if we had a way to write any async logic ahead of time, separate from the middleware itself, and still have access to dispatch and getState so that we can interact with the store.

### Redux Async Data Flow
Earlier, we saw a diagram that represents the normal synchronous Redux data flow. When we add async logic to a Redux app, we add an extra step where middleware can run logic like AJAX requests, then dispatch actions. That makes the async data flow look like this:
![video]{https://d33wubrfki0l68.cloudfront.net/08d01ed85246d3ece01963408572f3f6dfb49d41/4bc12/assets/images/reduxasyncdataflowdiagram-d97ff38a0f4da0f327163170ccc13e80.gif}

### Using the Redux Thunk Middleware
As it turns out, Redux already has an official version of that "async function middleware", called the Redux "Thunk" middleware. The thunk middleware allows us to write functions that get dispatch and getState as arguments. The thunk functions can have any async logic we want inside, and that logic can dispatch actions and read the store state as needed.

The word "thunk" is a programming term that means "a piece of code that does some delayed work". 


## REACT CONTEXT

### What is that Context
Context provides a way to pass data through the component tree without having to pass props down manually at every level.

Context provides a way to pass data through the component tree without having to pass props down manually at every level.

If you only want to avoid passing some props through many levels, component composition is often a simpler solution than context.

## REACT TESTING

### What testing mean?
In tech jargon testing means checking that our code meets some expectations. For example: a function called "transformer" should returns the expected output given some input.

### Fixing the test (and breaking it again)
What's really missing is the implementation of filterByTerm. For convenience, we're going to create the function in the same file where the test lives. In a real project you would define the function in another file and import it from the test file.

### Fixing the test for uppercase
filterByTerm should account also for uppercase search terms. In other words it should return the matching objects even if the search term is an uppercase string:
```javascript
filterByTerm(inputArr, "link");
filterByTerm(inputArr, "LINK");
```

### How to test React with Jest?
React is a super popular JavaScript library for creating dynamic user interfaces. Jest works smoothly for testing React apps (both Jest and React are from Facebook's engineers). Jest is also the default test runner in create-react-app.

- nvm install node
- 
  "scripts": {
    "test": "node --experimental-vm-modules node_modules/jest/bin/jest.js"
  },
  "type": "module",

- 
export function simpleFunc() {
  return "hello!";
}

export function complexFunc() {
  return "complex!";
}

- 
import { simpleFunc } from "../src/SimpleModule";

describe("A simple module", () => {
  test("it should say hello", () => {
    expect(simpleFunc()).toEqual("hello!");
  });
});

Testing is a big and fascinating topic. There are many types of tests and many libraries for testing. In this Jest tutorial you learned how to configure Jest for coverage reporting, how to organize and write a simple unit test, and how to test JavaScript code.
# **Writing and Presentation Test**

## **REACT JS**

---

### **PROP TYPES**

---

#### Lanjutan Proptypes
- Misal data yang ingin kamu kirim harus bertipe data string. Tapi yang terkirim tipe data number. Ini akan menghasilkan bug meskiput tidak ada pesan error
Contoh ; <br>
![image](https://user-images.githubusercontent.com/82355658/200151419-ea289cad-9bac-4f6d-941b-37287788a932.png)

- Untuk menghindari hal tersebut, gunakan **Prop Types**
- **Prop Types** merupakan sebuah library yang dapat membantu dalam memeriksa data props yang dikirim agasr sesuai denga ekspektasi. Jika tidak sesuai akan muncul error message.
- Cara install PRopTypes
```
    npm install prop-types
```
- Contoh penggunaannya <br>
![image](https://user-images.githubusercontent.com/82355658/200151571-86984696-3c5a-44e2-afdc-ea9a37d4a82f.png)
>Desc : Props yang akan dikirim harus sesuai dengan tipe data yang diinginkan
- Hasil <br>
![image](https://user-images.githubusercontent.com/82355658/200151651-5e9a8b92-5f18-40ee-b8d5-3e25e8a94588.png)
>Desc : Error akan terlihat dan dapat diperbaiki

### **REACT ROUTER**

---
React Router is the most popular routing library in React, but it can be a bit complicated to wrap your head around some of the more complex features.

#### **React Router Basic**
Before we start, you need to run `npm i react-router-dom` to install React Router. 

#### Configuring The Router
The easiest step by far is setting up your router. All you need to do is import the specific router you need (BrowserRouter for the web and NativeRouter for mobile) and wrap your entire application in that router.

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

#### Defining Routes
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
#### Handling Navigation 
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

#### Advanced Route Definitions
- Dynamic Routing
```javascript
<Routes>
  <Route path="/" element={<Home />} />
  <Route path="/books" element={<BookList />} />
  <Route path="/books/:id" element={<Book />} />
</Routes>
```

#### Routing Priority
```javascript
<Routes>
  <Route path="/" element={<Home />} />
  <Route path="/books" element={<BookList />} />
  <Route path="/books/:id" element={<Book />} />
  <Route path="/books/new" element={<NewBook />} />
  <Route path="*" element={<NotFound />} />
</Routes>
```
A * will match anything at all which makes it perfect for things like a 404 page. A route that contains a * will also be less specific than anything else so you will never accidentally match a * route when another route would have also matched.

- Nested Routes
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
- Shared Layout
```javascript
<Routes>
  <Route path="/" element={<Home />} />
  <Route path="/books" element={<BooksLayout />}>
    <Route index element={<BookList />} />
    <Route path=":id" element={<Book />} />
    <Route path="new" element={<NewBook />} />
  </Route>
  <Route path="*" element={<NotFound />} />
</Routes>
```
- Outlet Context
The final important thing to know about Outlet components is they can take in a context prop which will work just like React context.
```javascript
import { Link, Outlet } from "react-router-dom"

export function BooksLayout() {
  return (
    <>
      <nav>
        <ul>
          <li><Link to="/books/1">Book 1</Link></li>
          <li><Link to="/books/2">Book 2</Link></li>
          <li><Link to="/books/new">New Book</Link></li>
        </ul>
      </nav>

      <Outlet context={{ hello: "world" }} />
    </>
  )
}
```

```javascript
import { useParams, useOutletContext } from "react-router-dom"

export function Book() {
  const { id } = useParams()
  const context = useOutletContext()

  return (
    <h1>Book {id} {context.hello}</h1>
  )
}
```
> Note : As you can see from this example, we are passing down a context value of { hello: "world" } and then in our child component we are using the useOutletContext hook to access the value for our context. This is a pretty common pattern to use since often you will have shared data between all your child components which is the ideal use case for this context.

- useRoutes Hook
The final thing you need to know about defining routes in React Router is that you can use a JavaScript object to define your routes instead of JSX if you prefer.
```javascript
import { Route, Routes } from "react-router-dom"
import { Home } from "./Home"
import { BookList } from "./BookList"
import { Book } from "./Book"

export function App() {
  return (
    <Routes>
      <Route path="/" element={<Home />} />
      <Route path="/books">
        <Route index element={<BookList />} />
        <Route path=":id" element={<Book />} />
      </Route>
    </Routes>
  )
}
```

#### Handling Navigation
- Link Navigation
First I want to talk about link navigation since it is the simplest and most common form of navigation you will encounter. We have already seen the most basic form of link navigation using the Link component
```javascript
<Link to="/">Home</Link>
<Link to="/books">Books</Link>
```

- replace
The replace prop is a boolean that when set to true will cause this link to replace the current page in the browser history. Imagine you have the following browser history.
```javascript
/
/books
/books/3
```
- reloadDocument
This prop is another boolean and is very simple. If it is set to true your Link component will act like a normal anchor tag and do a full page refresh on navigation instead of just re-rendering the content inside your Routes component.

- state
The final prop is called state. This prop lets you pass data along with your Link that does not show up anywhere in the URL. This is something we will cover in more depth when we talk about navigation data so we can ignore it for now

### **REDUX**

---

#### Reducer?

- A reducer is a pure function that takes the previous state and an action as arguments and returns a new state. Actions are an object with a type and an optional payload:
- sintax
```javascript
function myReducer(previousState, action) => {
  // use the action type and payload to create a new state based on
  // the previous state.
  return newState;
}
```

#### Action?
- Actions are plain JavaScript objects that represent payloads of information that send data from your application to your store. Actions have a type and an optional payload.

#### Store?
- In Redux, the store refers to the object that brings actions (that represent what happened) and reducers (that update the state according to those actions) together. There is only a single store in a Redux application.
```javascript
import { createStore } from 'redux';
import todoReducer from './reducers';

const store = createStore(todoReducer);
```
Then, we dispatch actions in our app using the store’s dispatch method like so:

#### Data Flow in Redux
The 4 Main Steps of the Data Lifecycle in Redux
- An event inside your app triggers a call to `store.dispatch(actionCreator(payload))`.
- The Redux store calls the root reducer with the current state and the action.
- The root reducer combines the output of multiple reducers into a single state tree.

### Async Actions with Middleware and Thunk

#### Redux Middleware and Side Effects
Earlier, we said that Redux reducers must never contain "side effects". A "side effect" is any change to state or behavior that can be seen outside of returning a value from a function. Some common kinds of side effects are things like:

- Logging a value to the console
- Saving a file
- Setting an async timer
- Making an AJAX HTTP request
- Modifying some state that exists outside of a function, or mutating arguments to a function
- Generating random numbers or unique random IDs (such as - Math.random() or Date.now())

**Redux middleware were designed to enable writing logic that has side effects.**

As we said in Part 4, a Redux middleware can do anything when it sees a dispatched action: log something, modify the action, delay the action, make an async call, and more. Also, since middleware form a pipeline around the real store.dispatch function, this also means that we could actually pass something that isn't a plain action object to dispatch, as long as a middleware intercepts that value and doesn't let it reach the reducers.

Middleware also have access to dispatch and getState. That means you could write some async logic in a middleware, and still have the ability to interact with the Redux store by dispatching actions.

#### Using Middleware to Enable Async Logic
Let's look at a couple examples of how middleware can enable us to write some kind of async logic that interacts with the Redux store.

One possibility is writing a middleware that looks for specific action types, and runs async logic when it sees those actions, like these examples:
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

#### Redux Async Data Flow
So how do middleware and async logic affect the overall data flow of a Redux app?

Just like with a normal action, we first need to handle a user event in the application, such as a click on a button. Then, we call dispatch(), and pass in something, whether it be a plain action object, a function, or some other value that a middleware can look for.

Once that dispatched value reaches a middleware, it can make an async call, and then dispatch a real action object when the async call completes.

#### Redux Async Data Flow
As it turns out, Redux already has an official version of that "async function middleware", called the Redux "Thunk" middleware. The thunk middleware allows us to write functions that get dispatch and getState as arguments. The thunk functions can have any async logic we want inside, and that logic can dispatch actions and read the store state as needed.
![video](https://d33wubrfki0l68.cloudfront.net/08d01ed85246d3ece01963408572f3f6dfb49d41/4bc12/assets/images/reduxasyncdataflowdiagram-d97ff38a0f4da0f327163170ccc13e80.gif)

#### Configuring the Store
-  npm install redux-thunk
- Once it's installed, we can update the Redux store in our todo app to use that middleware:
```javascript
import { createStore, applyMiddleware } from 'redux'
import thunkMiddleware from 'redux-thunk'
import { composeWithDevTools } from 'redux-devtools-extension'
import rootReducer from './reducer'

const composedEnhancer = composeWithDevTools(applyMiddleware(thunkMiddleware))

// The store now has the ability to accept thunk functions in `dispatch`
const store = createStore(rootReducer, composedEnhancer)
export default store
```

- Right now our todo entries can only exist in the client's browser. We need a way to load a list of todos from the server when the app starts up.
```javascript
import { client } from '../../api/client'

const initialState = []

export default function todosReducer(state = initialState, action) {
  // omit reducer logic
}

// Thunk function
export async function fetchTodos(dispatch, getState) {
  const response = await client.get('/fakeApi/todos')
  dispatch({ type: 'todos/todosLoaded', payload: response.todos })
}
```

We only want to make this API call once, when the application loads for the first time. There's a few places we could put this:

- In the <App> component, in a useEffect hook
- In the <TodoList> component, in a useEffect hook
- In the index.js file directly, right after we import the store

```javascript
import React from 'react'
import ReactDOM from 'react-dom'
import { Provider } from 'react-redux'
import './index.css'
import App from './App'

import './api/server'

import store from './store'
import { fetchTodos } from './features/todos/todosSlice'

store.dispatch(fetchTodos)

ReactDOM.render(
  <React.StrictMode>
    <Provider store={store}>
      <App />
    </Provider>
  </React.StrictMode>,
  document.getElementById('root')
)
```
![image](https://d33wubrfki0l68.cloudfront.net/c96c315f5e60b87fa093e49d8d30a5a1fb66c580/9fd52/assets/images/devtools-todosloaded-action-0f8f36d9f37404a85e5cbc20bd30d9e4.png)

- The last thing we need to change here is updating our todos reducer. When we make a POST request to /fakeApi/todos, the server will return a completely new todo object (including a new ID value). That means our reducer doesn't have to calculate a new ID, or fill out the other fields - it only needs to create a new state array that includes the new todo item:
```javascript
const initialState = []

export default function todosReducer(state = initialState, action) {
  switch (action.type) {
    case 'todos/todoAdded': {
      // Return a new todos state array with the new todo item at the end
      return [...state, action.payload]
    }
    // omit other cases
    default:
      return state
  }
}
```
![image](https://d33wubrfki0l68.cloudfront.net/7b06b4966e3cfc821fed6c95c21ba0d4c4013b0b/e9fb9/assets/images/devtools-async-todoadded-diff-5f18f236969280dec2dad1a6d4d74b2e.png)
# **Writing and Presentation Test**

## **REACT JS**

---

### **BASIC OF REACT JS **

---

#### Introduction React JS

- ReactJS made by Facebook Engineer
- ReactJS used to Facebook Front-End

#### What is React JS?

React JS is a framework view library Javascript to make a user interface of website

#### Reasons why we use React JS

- React JS is FAST
  React JS makes the Front-End Aplication so fast, eventhough we should handle some datas
- React JS is Modular
  React JS devides the appearance of the website into small components <br>
  Ex : <br>
  ![image](https://user-images.githubusercontent.com/82355658/198838700-656bce41-c327-4f17-a0b2-1328eaf30154.png)

  > Note : The small components like card, navbar, etc will be devided by react

- React JS is Scalable
  React js can be used for small to large scale and complex applications

#### Who does use React JS?

Around 8594 companies reportedly use React in the tech stacks, inculding Uber, Airbnb, instagram, netflix and facebook

#### What is JSX?

JSX is a JavaScript extension syntax that allows you to modify the Document Object Model (DOM) with HTML-style code.

To understand JSX functions more clearly, you need to know about the DOM first.

DOM is an application programming interface (API) that functions to manage the structure of web pages. Well, to add dynamic content into a web page, the developer has to modify the DOM.

In other words, JSE will make it easier for you to add dynamic content. Because this extension can help you to insert HTML syntax into DOM.

However, JSX HTML. Maybe the language is simple like this: JSX looks like HTML, but functions like JavaScript.

#### Virtual DOM

When a developer updates the DOM using JSX, React JS creates a Virtual DOM, which is a copy of the original DOM that you want to update.

Well, Virtual DOM is useful for viewing the changed parts of the original DOM.

When it finds a part that needs to be changed, React JS will only change that part. So, users don't have to reload a single page to see the changes.

This can affect website performance. Because every change is only made to the part that is needed.

Ex :
![image](https://user-images.githubusercontent.com/82355658/198867230-607083c1-b45e-4f42-894d-ca038659ed0a.png)

> For example, when a website user clicks the like or comment button, of course the only thing that needs to change is the like and comment section, right?
> Without Virtual DOM, your website will use HTML for DOM updates. Thus, the entire DOM must be reloaded to show changes in one section – such as clicking the like button or adding a comment.

#### Instalation of React JS

1. Download [Node.js](https://nodejs.org/en/).
   Node JS is a virtual environment for other frameworks, inxluding React. Then install it.

2. Make a new folder to install the react.
   Ex : D:\React-JS
   <br>
   ![image](https://user-images.githubusercontent.com/82355658/198867819-9fa1dbb3-c38f-4289-9e0d-80c9c5d0f8c9.png)

3. Open the Command Prompt, then type : `npm -v`

4. Now, Now lets go to the react installation folder you just created, you can type : <br>
   `d:`<br>
   `cd React-JS [or your foldername]`
   ![video](https://lh5.googleusercontent.com/ThqFdBAIUBtAbG-0jpUa9szOb0iDbjYA-v27s1v7Vltn24BPybIVQRtm7Vsk3OoyriKdCRvT8ZCxEpwr-ZIPHfnIOiwgyJWY6IxHFkvi1rCCBe3X3VuK4RosGoTQreuYHZWN9FIm)

5. Type the code below to install react: <br>
   `npm install -g create-react-app`

6. To check the success of the installation process, you can check the react version by typing:
   ![video](https://lh3.googleusercontent.com/IrizGDBz0Ue0xE6vVmqREcyjoqPcSwqMnekD803xv6lV_Q6KUQqCaYyUpGmY7XzUEc_mg8EWjsZxwoAUYEaFEI_mWbiIbTu6KOPY2_qzbh6nrOM2qF-SxP16hexMQhkpM6-lpqDD)

7. Now you can make the first project react JS . To do it, type the code :
   `create-react-app web-react-saya `<br>
   `cd web-react-saya `<br>
   `npm start`

8. After that, there will be open a web with the address localhost:3000. Here's how it looks:<br>
   ![video](https://lh4.googleusercontent.com/6zWPjk-LerhmW5tC2tjyG_V5M2nw3BOvQ3kfTiHzIZC0uCsN50WtYO3iewCsw-yj_8ZwLe37_4t429PKVt2D14aVNZa4a2ZZguj80Ew5ZXn3nxWNceLKLoe0uyT9rRccp9Rg1I1i)

9. If u find a error message, you can type this code :
   `npm install` <br>
   `npm start`

#### class and className

- In JSX, the class attribute in the HTML element tag must use className <br>

```javascript
import React from 'react":

function HelloWorld() {
    return
        <div>
            <h1 className="title">React J5 <h1>
            <p className="description">
             A JavaScript Library for building user interfaces </p>
        <div>
    );
};

    export default HelloWorld;
```

#### Curly Braces in JSX

- We can use JS syntax in HTML Elements with curly braces

```javascript
    import React from 'react';
    function HelloWorld() {
    return (
    <div>
    );
    <h1>{ 2 + 3 }</h1>
    </div>
    };
    export default HelloWorld;

    ///output
    5
```

- If u dont use the curly braces, the code will be a content HTML

```javascript
import React from 'react';
    function HelloWorld() {
        return (
            <div>
                <h1> 2+ 3 </h1>
            <div>
        );
    };
export default HelloWorld;

    ///output
    2 + 3
```

#### Use Curly Braces to access the variable JSX

```javascript
import React from 'react':
    function HelloWorld {
        //11 Declare variable
        const name = 'John Doe'
        return (
            <div>
                <h1>{ name } </h1>
                <h1>{ name. to LowerCase() }</h1>
            </div>
        );
    };
export default HelloWorld;

///output
//John Doe
//john doe
```

#### Atribute pada JSX

```javascript
    import React from 'react';
        function HelloWorld() {
        // Declare attribute const width = "500px";
        return(
            <div>
                <img src="https://images.unsplash.com/photo-1593278411489-2e414e2e03f6?ixlib=rb1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=668&q=80" alt="image" width={width}>
            </div>
        );
    };
export default HelloWorld;
```

Tampilan
![image](https://images.unsplash.com/photo-1593278411489-2e414e2e03f6?ixlib=rb1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=668&q=80)

#### Event in JSX

![image](https://user-images.githubusercontent.com/82355658/198870381-15d2c54a-39ac-437b-a2c8-33b68af7df1b.png)

```javascript
import React from 'react';
    function HelloWorld() {
    // Declare attribute const width = "500px";
    // Function const onClickFunction = 0)
    alert('You clicked image');
    {
        return (
            <div>
                <img src="https://images.unsplash.com/photo-1593278411489-2e414e2e03f6?ixlib-rb1.2.1&ixid-eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=668&q=80" alt="image" width={width} onClick={onClickFunction} />
                // Event in JSX
            </div>
export default HelloWorld;
```

#### Conditional In JSX

```javascript
import React from 'react';
    HelloWorld() {
        let stopLight = "yellow';
        let message;
            if (stopLight = 'red')
                {
                message = <h1>Stop!</h1>;
                }
            else if (stopLight = "yellow')
                {
                message = <h1>Slow Down</h1>;
                }
            else if (stopLight = 'green')
            {
            message = <h1>Go</h1>;
            } else {
            message = <h1>Caution, unknown</h1>;
            return (
                <div>
                {message}
                </div>
            );
    }:
    export default HelloWorld;

    ///Output
    ///Slow Down
```

#### .map()

To show datas list, react has many ways

```javascript
import React from "react";

function Helloworld() {
  const numbers = [1, 2, 3, 4, 5];
  const listItems = numbers.map((number) => {
    return (
      <ul>
        <li>{number}</li>
      </ul>
    );
  });
  return <div>{listItems}</div>;
}

export default HelloWorld;
///output
-1 - 2 - 3 - 4 - 5;
```

### React JS - Component

- **Component** is the one of core from React JS
- Component divides UI into small units
- Its mean we can make some components in 1 page
- Component will be made, if it is reusable code

There are 2 ways, to make a component

1. Function

   - Install your folder project
   - Than, in `src` folder make a `component` folder and add User.jsx file
     ![image](https://user-images.githubusercontent.com/82355658/198872688-2223f1a6-9f0e-42f7-b29f-57f3d0e045b4.png)
     type the code into User.jsx:

   ```javascript
   const Users = () => {
       return (
       <div className="user">
           <div className="pp">
           <img
               src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTKLuLCgxCW2M2XJW_rjsQMKorBhuPxe2EEagi44v8&s"
               alt=""
           />
           </div>
           <div className="desc">
           <h2 style={{ marginBottom: "-10px" }}>DAVID WINALDA</h2>
           <h5 style={{ marginBottom: "-10px" }}>BOOTCAMP STUDENT</h5>
           < style={{}}>
             p  <i> Coding membuat saya belajar bagaimana berpikir</i>
           </>
           </div>
       </div>
       );
   }

   export default Users;
   ```

   - import Users to App.jsx

   ```javascript
   import "./App.css";
   import Users from "./components/Users";

   function App() {
     return (
       <>
         <Users />
       </>
     );
   }

   export default App;
   ```

   Result : <br>
   ![image](https://user-images.githubusercontent.com/82355658/198872962-d45bcaeb-07b9-4894-8f2b-fe1a247e1c56.png)

2. Class

#### Stateful Component and Stateless Component

1. Stateless Component
   ![image](https://user-images.githubusercontent.com/82355658/198873203-635caa59-5976-4615-88bd-f85e7ae31870.png)

2. Stateful Component
   ![image](https://user-images.githubusercontent.com/82355658/198873474-902aac7b-c3d9-46b4-8a53-ca2abfe42a4d.png)

#### State dan Props

State dan props adalah hal yang berhubungan dengan Stateless & Stateful Component.

Stateless berrti tidak memiliki state. Dia hanya memiliki props

Stateful berarti memiliki state dan bisa mengirim state tersebut ke component.

Jadi state adalah data lokal
Props digunakan agar component memiliki data yang dinamis yang dikirim dari component lain.

### **INTERMEDIATE OF REACT JS **

#### **HOOKS**

##### What is Hooks?

- Hooks is a new fiture from reactJS in 2018
- Hooks memudahkan penggunaan functional components agar bisa menggunakan state, dan lifesycle lainnya.
- Sebelumnya state(setState) dan lifecycle(componentDidMount, componentDidUpdate) hanya bisa digunakan di class component, namun dengan hooks kita bisa menggunakannya di functinal component.
- Hooks yang sering digunakan adalah
  - useState
  - useEffect
- Perbedaan functional component dengan class componennt
- Persamaannya kedua hal ini menghasilkan hal yang sama, namun class menggunakan state dan functional menggunakan state hooks
  -Kelebihan penggunaan Hooks - Code terlihan lebih clean dan pendek - Code lebih mudah dimengerti

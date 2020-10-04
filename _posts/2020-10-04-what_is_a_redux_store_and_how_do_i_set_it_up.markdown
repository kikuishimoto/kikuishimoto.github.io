---
layout: post
title:      " WHAT IS A REDUX STORE AND HOW DO I SET IT UP"
date:       2020-10-04 19:28:49 +0000
permalink:  what_is_a_redux_store_and_how_do_i_set_it_up
---


As many people know, I am working on my last project with flatiron andhoping to become a full time developer soon! Here are the basics od redux explained.

**First, we have to know what exactly redux is.** 
Redux is an open-source JavaScript library for managing application state. Rudux gives you acces to this magical thing called a *store* and no, you can't buy anything from it.

**What is a store then?**
A store, stores the state for the whole application. We use this so we dont hace to go crazy trying to pass down props from each component. It makes our like super easy because we can actually pass store into out components as a prop. Lets say you have a project about dogs and each dog has a breed. Instead of fetching all the dogs from your back end and then passing it from componenent to component, you can just store the dogs in your store. This ways you can access all the dogs via props from any of your components. Pretty neat, huh?

**Okay, I'm in and very okay with knowing I can't buy anything. But how do I use the Redux Store?**

Its a lot easier than you think! First, you have to npm install react-redux. 
```npm install react-redux```

Then, in your index.js file you are going to import nessisary files and create a store. After you create a store, you have to wrap your App in Provider. Provider gives you acces to the store. Be sure to make your reducers!
```
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';
import * as serviceWorker from './serviceWorker';
import { BrowserRouter as Router } from "react-router-dom";
import { Provider } from 'react-redux';
import { createStore, applyMiddleware } from "redux";
import { composeWithDevTools } from "redux-devtools-extension";
import reducer from './reducers/index';
import thunk from "redux-thunk";

const store = createStore(reducer,  applyMiddleware(thunk));


ReactDOM.render(
  <React.StrictMode>
    <Provider store={store}>
    <Router>
      <App />
    </Router>
    </Provider>
    
  </React.StrictMode>,
  document.getElementById('root')
);
```

Then boom! You got a working redux store. In future blog posts, we'll touch a little bit more on reducers and how to update the store! Happy coding!



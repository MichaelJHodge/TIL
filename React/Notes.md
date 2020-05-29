Crashcourse in React
"React is a JS library developed by Facebook to build interactive User Interfaces."

[Need to add past notes here!]


In React, you do not modify the state directly. 

The 'State' holds certain synchronous variables, so if you change the value of a state variable, that change is reflected anywhere that variable is being used. State can be modified based on user action or other action. when a value of a component’s state is changed React will re-render that component to the browser.

Props are arguments passed in a method or function. Includes data that you give to a component. State includes data that is private to that component - other components can not access that state. 

React architecture is based on Components - every aspect of an app or site is
a child component - they are made separately and then added to the main parent
component. Apps are essentially 'trees' of components. 

Rule of thumb for React apps: "the component that owns a piece of the state, should be the one modifying it."

A component must return only one Node - meaning a single <div> and everything inside it </div> , or a single tag (element).















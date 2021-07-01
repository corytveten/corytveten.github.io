---
layout: post
title:      "Developing a React App with Redux"
date:       2021-07-01 03:07:56 +0000
permalink:  developing_a_react_app_with_redux
---


One of the challenges in building a React app from the ground up was deciding when to employ local state and when to use Redux and the store. The flow of data in local state is simpler and easier to digest when using simple changes in data, and this simplicity is appealing to a new programmer. But the Redux store’s representation through Redux DevTools is an invaluable tool for beginners looking to understand the flow of data through react components.

**Local State**

Local state has the advantage of simplicity and clarity. Local state exists only within one component. State is declared as an object within that component’s class and setState is called within a method in order to change the value of an object declared within state. 

The component structure of React reinforces the clarity. A single component exists within a single file, so state never needs to track between multiple files and screens. To communicate the data held as state to another component, the data becomes a prop and is now a fixed input. State is neatly compartmentalized within each file of the app’s structure.

**Redux and the Store**

Now, as data becomes more complicated, local state can lose some of its simplicity. One of the first aspects of Redux we learned was that it removes the need to pass down props through multiple components, allowing for clearer, cleaner writing. But Redux introduces new terms, new concepts, and new structures that can be difficult to learn even when employed with a minimal amount of data. 

One of the challenges I found came with the createStore method. Just as I was beginning to understand the flow of state plus action leading to changed state through the reducer, and then that changed data run through a dispatch function to persist the changes. But then Redux provides us a createStore method through its library which incorporates the dispatch and getState function which is called at the level of the index,js file. This is not a blog to explain this process in detail, I mention it in an attempt to illustrate the head spinning difficulties this new process presented.

But as I became more comfortable with Redux, I found the Redux DevTools to be an excellent tool for a beginner. Redux DevTools provides a record of the current state of the store and the actions that have been dispatched. The immediate access to current state helps beginners navigate life cycles and data availability. But on an even more basic level, the record of state helped me keep track of the structure of the objects and names of object keys I needed to use in the component. One of my biggest challenges in moving from vanilla javascript to react was the move away from pointing to data through variables and toward objects with keys and values. To me, this added a layer of labels to keep track of. The redux store clearly broke down all the object and key names for easy access when mapping state to props and writing conditional statements for rendering.


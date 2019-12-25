---
layout: post
title:      "How Redux Works"
date:       2019-12-24 19:41:54 -0500
permalink:  how_redux_works
---


The final module in the curriculum is on Redux which is a JavaScript framework for managing and maintaining application state and can be used with React or some other library. This section introduces a number of terms to describe how Redux works and I will summarize them in this post.

The **state** of the app is stored in a JavaScript object. The state is read-only and the only way to mutate or change state is through  an **action**, which is an object describing what happened. An action is an object with a property of type. It can have a payload but it must always have a type. It  usually represents some kind of event, such as a user logging in or logging out.  An **action creator** is a plain function that creates and returns an action object.

Changes to the state are executed by pure functions called **reducers**. Reducers take in two arguments: the current state and the action and returns a new state.  A reducer should not have any side-effects, that is, if you call a reducer with the same state and the same action, you should always get the same result.

It's typical to implement reducers with a switch case that decides what to do based on the action type. 
If an action is not found in the reducer, a default case will return the initial state.

Reducers return pieces of state and they all aggregate and collectively make up the store. The **store** is where the state is contained. The store is the single source of truth for the application.

 
 



* 

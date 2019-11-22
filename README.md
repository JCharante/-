# 进来

(jin4 lai2)

> Central Authentication System for Shared-suite of Products

For use by the Jyan suite of products:

- [Your Final Grade (a学生）](https://github.com/yourfinalgrade)
- [Triage](https://github.com/JCharante/triage-spa-v2)
- and more to come...

## Problem Statement
The goal for authentication systems is simple. You want to validate a unique identity to associate with your program's data. It's a pain to integrate various OAuth systems.

## Vue.js components

进来 comes with a set of Vue.js components. You simply insert <jinlai/> as a component on your login/register page. There is an `@done` event which calls the corresponding method with a session key. That's all you have to do for the UI. No more creating a UI for every single application.

## API

进来 also comes with a websocket api. This is used: 
- by the client (the client will communicate with 进来 and transfer necessary information to login/register until it receives a sessionKey).
- to communicate with your backend service (your backend service will validate the sessionKey, and retrieve 进来-wide information about the user (think email, name, phone number, address?).

## About Scopes

Traditional "OAuth like" systems would have scopes to insure that users can log onto a product without worrying about oversharing. Since 进来 is solely designed to be used by me ([jyan](https://jcharante.com)), then scopes are an unnecessary security measure, because if you don't trust the product, then why would you trust 进来?

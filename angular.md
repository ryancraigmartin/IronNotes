# Angular

Many applications built with Angular are what are called Single Page Applications *(SPA)*.

## What is a Framework?

A software framework is a universal, reusable software environment to facilitate development of software applications, products and solutions. It describes the structure of the application. It gives the developer a way to organize the code to make an app more flexible and scalable. You may know some other frameworks, like Express, a Node.js framework. In this module we will learn a framework for the front-end: Angular.

It may include:

- Support programs.
- Compilers.
- Code libraries.
- Toolsets.
- APIs (Application Programming Interfaces).
- A JavaScript framework is a web application framework written in JavaScript.

## Routes

When using routing in Angular we rely on three main components:

- Routes describes the routes our application supports.
- RouterOutlet is a “placeholder” component that shows Angular where to put the content of each route.
- RouterLink is a directive used to link to client-side routes.

To define the routes, we have to add the following in the app.module.ts file:

``` ts
// app.module.ts
// ...import statements
import { Routes } from "@angular/router";

const routes: Routes = [
  { path: '', redirectTo: 'home', pathMatch: 'full' },
  { path: 'home',  component: MyHomeComponent },
  { path: 'about', component: MyAboutComponent }
];
// ...rest of app.module.ts
```

The code above configures the router in the following ways:

- Redirects to the home path every time the path is empty.
- Activates the MyHomeComponent every time the path home is visited.
- Activates the MyAboutComponent every time the path about is visited.

## Services

A service is a class that lets us define functionalities independent from our interfaces and components. If we want multiple components to have access to the same logic that is where services come in.

We use services to:

- Write application logic.
- Share code among components.
- Wrap external communication such as AJAX, Web socket, local storage, etc.

A service should be:

- Reusable.
- Independent from the views and templates.

A service could:

- Consume other services using `dependency injection.`
- Be used in components using `dependency injection.`

### Multiple instance vs Singleton
[The Singleton is the Highlander of design patterns. There can be only one.](http://joelhooks.com/blog/2013/05/01/when-is-a-singleton-not-a-singleton/)

## Dependency Injection

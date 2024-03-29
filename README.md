# Angular Bootcamp

Angular is a Javascript framework that allows you to create reactive SPAs

1. [Angular](https://angular.io/)
1. [Angular Cli](https://angular.io/cli)
   - Best practices way to create an angular app
   ```cli
   npm install -g @angular/cli
   ```
1. Creating an app
   ```
   ng new 'appname'
   ```
1. Launching the app
   ```
   ng serve
   ```
   - In the folder where the app lives
1. Angular is built around the idea of components
   - Throughout the course, components will factor in heavily
1. [Angular Docs](https://angular.io/guide/architecture)

## Using Bootstrap

1. We have to install boostrap for our project
   ```
   npm install --save bootstrap
   ```
1. We also need to point to the bootstrap css in our angular config
   - `angular.json`
   ```json
   "styles": [
       "src/styles.css",
       "node_modules/bootstrap/dist/css/boostrap.min.css"
   ],
   ```

# Components

1. Creating with the cli
   ```
   ng generate component servers
   ```
   ```
   ng gc servers
   ```
1. Generally with components you have 3 files
   - name.component.html
   - name.component.css
   - name.component.ts
1. You link the html and css to the component in the ts file

   ```ts
   import { Component, OnInit } from '@angular/core';

   @Component({
   	selector: 'app-servers',
   	templateUrl: './servers.component.html',
   	styleUrls: ['./servers.component.css'],
   })
   export class ServersComponent implements OnInit {
   	constructor() {}

   	ngOnInit(): void {}
   }
   ```

   - You can also put the html in a `template` section on the component as a string block
     - No thanks
   - You can do the same with styles

# Debugging

1. Angular merges everything together, so console errors won't tell you exactly where in your code the problem is occuring
1. Angular uses sourcemaps which allow you to debug into typescript files
   - Under sources: webpack > src

# Directives

1. [Official Docs](https://angular.io/guide/built-in-directives)
1. Directives are used to add css classes
   - Change appearance or behavior
1. Also used to add and remove DOM elements
1. This allows us to programatically apply elements and css to DOM stuff
1. We tie our html to our class
   - Refer to the code section for directives

# Dependency Injection and Services

1. [Official Docs](https://angular.io/guide/dependency-injection)
1. Official docs has us using the `@Injectable` decorator, but project doesn't

# Routing

1. [Official Docs](https://angular.io/guide/routing-overview)

# Observables

1. Angular has built in observables, but recommends using RxJS
   - [Official Docs](https://angular.io/guide/rx-library)
   - Uses subscriptions

# Pipes

1. [Official Docs](https://angular.io/guide/pipes-overview)
1. Pipes aren't re-calc'd on data changes by default
   - A filter pipe won't show new items that are added when the filter is in effect by default
   - Can turn this off in the decorator (but maybe not recommended)
   ```ts
   @Pipe({
   name: 'filter',
   pure: false,
   })
   ```

# Http

1. Using firebase realtime db as our backend

# Auth

1. Firebase again
   - It has it's own auth section, where we've used username/password
   - [Official Docs](https://firebase.google.com/docs/reference/rest/auth)

# Dynamic Component Loader

[Official Docs](https://angular.io/guide/dynamic-component-loader)

# Deployment

1. Use an environment file for secrets
1. Generate deploy files
   ```
   ng build
   ```
1. Static website host

   - [Firebase hosting](https://firebase.google.com/docs/hosting)

   ```npm
   npm install -g firebase-tools
   ```

   - Login

   ```
   firebase login
   ```

   - Initialize

   ```
   firebase init
   ```

   - Lots of steps
   - Should be pretty easy to figure out by the options
   - Deploy

   ```
   firebase deploy
   ```

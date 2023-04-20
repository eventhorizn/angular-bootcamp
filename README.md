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
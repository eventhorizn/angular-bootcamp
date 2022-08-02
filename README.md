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
   - Throughout the course, componenst will factor in heavily

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

## Components

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

## Databinding

1. Tying business logic to your template
   - Output Data (Business logic to template)
     - String Interpolation
     - Property Binding
   - React to (User) Events
     - Event Binding
   - Combination
     - Two-Way Binding

### String Interpolation

```ts
import { Component } from '@angular/core';

@Component({
	selector: 'app-server',
	templateUrl: './server.component.html',
})
export class ServerComponent {
	serverId: number = 10;
	serverStatus: string = 'offline';

	getServerStatus() {
		return this.serverStatus;
	}
}
```

```html
<p>Server with Id {{ serverId }} is {{ getServerStatus() }}</p>
```

### Property Binding

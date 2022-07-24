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
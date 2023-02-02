# PeachtreeBank

This project scaffolding was generated with [Angular CLI](https://github.com/angular/angular-cli) version 10.0.7.

### Business Requirements Delivered:

This initial version of this application has completed the following aspects of the business requirements:

- Home Component which brings the two Transfer and Transcation components together
- Transfer Component
    -   Form with 3 fields (From Account, To Account and Amount) and 3 buttons (Cancel, Submit, Tranfer)
    -   Cancel buttons resets state
    -   Submit button toggles preview state
    -   Transfer button sends transaction record to transaction component
- Transaction Component
    -   Reads the mock JSON to render data on the table
    -   Filter will search per keystroke for matched records to display on the table
    -   Sorting header sort per column instead of dedicated buttons which are on the design document.

### Application Structure

Fairly basic Angular application

* Base

  * `/src/app/app.module.ts`—handles the necessary imports of Angular modules.
  * `/src/app/app.component.*`—defines the root of the application. Most importantly in charge of using the UserAccountService and populating other components with the user’s data.
  * `/src/styles.css`—defines some basic styling, mostly for fonts. Some common styling should probably migrate here, like buttons, inputs, and headers.

* Components:
  * `/src/app/components` folder is for all aplication level components.
  * `/src/app/transfer-pane`—the box by that name in the app: handles taking user input and submitting a new transaction.
  * `/src/app/recent-transactions-list`—the by this name in the app: handles displaying, sorting, and filtering past transactions. Has no real notion of “recent.”

  Each component has the expected .css, .html, .ts, and .spec.ts files. Haven’t done anything with the .spec.ts files.

* Services:
  * `/src/app/services` folder is for all aplication level services.

* Interfaces:
  * `/src/app/interfaces` folder is for all aplication interfaces / data objects.

* Validators:
  * `/src/app/validators` folder is for all aplication level directives mainly for validations

* Store:
  * `/src/app/store` folder is for all aplication level store for storing data and used across the application.

## Development server
Run `npm install` for a installing dependencies (one time activity).

Run `npm start` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run the following command to execute the end-to-end tests via [Protractor](http://www.protractortest.org/):
`npm run e2e -- --baseUrl=http://localhost:4200/`
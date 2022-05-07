# Routing App

1) Generate a project with routing option

2) Generate departmentList and EmployeeList Component

3) Configure the routes

4) Add buttons and use directives to navigate


# In app.routing.module.ts file you can add 

import { DepartmentListComponent } from './department-list/department-list.component';
import { EmployeeListComponent } from './employee-list/employee-list.component';


const routes: Routes = [
  { path:"departments", component: DepartmentListComponent},
  { path: "employees", component: EmployeeListComponent }
];


// added
export const routingComponents = [DepartmentListComponent, EmployeeListComponent]



# app.module.ts file you can remove to two imported component

	import { DepartmentListComponent } from './department-list/department-list.component';
	import { EmployeeListComponent } from './employee-list/employee-list.component';


# app.module.ts file you can add this- routingComponents

	// import { AppRoutingModule } from './app-routing.module';
// added
import { AppRoutingModule, routingComponents } from './app-routing.module';

# app.component.html

Add this code
<router-outlet></router-outlet>

# AngularRouting

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 13.3.3.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

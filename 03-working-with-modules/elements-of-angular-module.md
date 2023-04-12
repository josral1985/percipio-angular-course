# Elements of Angular Module

**NgModules** found in the `app.module.ts` is a function that organizes a lot of code (imports, providers, bootstrapping...) managing injectable objects, organizing related items together, and it extends the application's capabilities by importing other modules. `NgModules` consolidate the components, directives, and pipes into cohesive blocks of functionality.

## NgModule Decorator

Marks a class as an NgModule class (@NgModule). It takes a metadata object to describe the app's configuration, describes the injectable modules and services, and it identifies the module's component, directive, and pipes.

## Bootstrapping Components Using Modules

The root application (AppComponent) acts like the main method in other languages, directs the rest of the application in term what functionality it needs. Bootstrapping creates and inserts the components into the browser's DOM. The bootstrapped component becomes the base of its tree of components. The AppComponent is stored in the root module's bootstrap array. The class AppComponent is decorated with the class decorator `@Component`, where we find the `NgModule`.

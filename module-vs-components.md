# Cohesion & Coupling

# Module vs Components

Useless debate. They are usually used interchangeably and there is nothing wrong in that.

Modules/components can be viewed as a collection/group of related code including variables, functions and classes. In modern programming languages, related code is usually bundled together in namespace, package, scope, etc. A couple of modules/components are then packaged together in a library, sdk, executable, etc.

## Cohesion

Refers to the degree of dependency of the execution units on each other within a single module. Ideally whatever is needed by an execution unit in a module should be available in the same package. A module with *high cohesion* has limited responsibility or the module serves a single or a very small set of purposes. A highly cohesive module is self contained and has fewer reasons to make calls to other modules. A module with *low cohesion*, on the other hand, serves a multitude of purposes in a haphazard manner. A low cohesive module is usually forced to call other modules to meet its goals. Higher cohesivity is a desirable trait that modules should strive to achieve.

## Coupling

Refers to the degree of dependency between multiple modules. Two or more modules with a great degree of interaction between them are referred to as *tightly coupled* modules. Higher coupling makes the system more complex, difficult to test, debug, change and manage. Two or more modules with only a limited interaction between them are called *loosely coupled* modules.

> High cohesion + Loose coupling is the way to go.

## Separation of concerns / single-responsibility principle

> Concern is a  generic term for a purpose/functionality performed.

In designing software, separate concerns into distinct units like classes so that each unit is more flexible, maintainable, reusable and extensible. Another way of saying is that a software unit should only have a single responsibility. This principle often increases cohesion.

# Open-closed principle

A software module should be
- open to extension i.e. it should be possible to add new feature
- closed to modification i.e. the addition of new feature should cause little to no (preferable) changes to the existing code.

## Implementation

Use abstract base classes or interfaces to define the form/shape of the module. Different implementations can then provide distinct but similar functionality. Some of the implementations could even be extended by subclasses to add additional fields and methods.
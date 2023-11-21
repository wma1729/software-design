# Open-closed principle

A software module should be
- open to extension i.e. it should be possible to add new data members/fields and new methods to a module.
- closed to modification i.e. the external module relying on the software module should not break.

## Implementation

Use abstract base classes or interfaces to define the form/shape of the module. Different implementations can then provide distinct but similar functionality. Some of the implementations could even be extended by subclasses to add additional fields and methods.
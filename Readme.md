# units

is an architecture for (micro)services that focuses on

- small, easy to test, single responsibility principle conform units across all layers
- reducing dependencies between units
- including domain driven design

to achieve clean code as a basis for hiqh quality software.

## Level 1 The Layers

![units-level1.svg](./units-level1.svg)

- Domain layer contains domain objects according to domain driven design.
- API layer contains protocol abstraction, serialization and versioning.
- Repository layer contains data providers, no matter if they query data from a database, memory, filesystem or a remote service.
- Logic layer contains the rest of functionality. Some examples are: authorization, validation, converters, workflows, calculations etc.  

The Domain layer is accesible to all other layers. 
The Logic and Repository layers can only be accessed by the layer on top of them.

## Level 2 Inside A Layer

![units-level2.svg](./units-level2.svg)

Each layer is built out of actions. 
An action is a pure workflow it checks conditions and passes objects from processor to processor.
Processors must follow the single responsibility principle. 
The goal is to have most dependencies in the action and processors with very few/no dependencies which are easy to test and replace.

Action groups can be used for code readability. 
An action group in a common architecture is a service and the action one service method.














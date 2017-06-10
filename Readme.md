# units

is an architecture for network applications that focuses on

- small, easy to test, single responsibility principle conform units across all layers
- reduce dependencies between units and and structure dependencies between layers

to achieve clean code as a basis for hiqh quality software.

![units](https://rawgit.com/eduardbeutel/units/master/units-general-view.svg)

## Concepts

The **domain** is a model of the business domain. Examples: entities, value objects. @see Domain Driven Design.

A **processor** processes its input into an output. It only performs one very specific task and contains no routing. In most cases it should have no/few dependencies. Example: Builder, Validator, Converter.

A **repository** is a centralized data holder. Examples: UserRepository, EntityRepository.

A **workflow** is as its name says exactly one workflow. It only does routing. Based on conditions it calls processors, repositories or other workflows.

The **API** contains endpoints that transform request/responses to domain objects and call workflows. Example: SOAP, REST.












# units

is an architecture for network applications that focuses on

- small, single responsibility principle conform units across all layers
- reduce and structure dependencies between units
- clear and complete separation of concerns
- achieving high quality with a large number of unit tests and small number of system tests

![units](https://rawgit.com/eduardbeutel/units/master/units-general-view.svg)

## Concepts

An **input/output(io) interface** receives requests, transforms them, forwards them to a workflow and sends responses back. Example: SOAP, REST.

A **workflow** is responsible for routing. It calls processors to carry out specific tasks. Workflows can also call other workflows.

A **processor** processes its input into an output. It only performs one very specific task and contains no routing. Example: Validator, Converter, Algorithm.

The **domain** is a model of the business domain. Examples: entities, aggregates, business rules.

A **repository** is a centralized data holder. Examples: user repository, entity repository.






# Star Wars Supermodel
Demo data models for http://supermodel.io

## Overview

[![CircleCI](https://circleci.com/gh/supermodel/starwars.svg?style=svg)](https://circleci.com/gh/supermodel/starwars)

Supermodel demo models using the [Star Wars API theme](https://swapi.co/), the models can be found in the in the [supermodel/starwars](https://github.com/supermodel/starwars/tree/master/supermodel/starwars) folder or directly viewed at https://supermodel.io/starwars.

Models are, by convention, written as [JSON Schema in YAML format](http://json-schema.org/), one schema definition per one YAML file. Every model has to start with JSON Schema `$id`.

A model can freely reference any other model or model property using the JSON Schema `$ref` reference mechanism. The reference can point to any JSON Schema on the web, or it can be relative to the current model.

### CLI 

The [Supermodel CLI tool](https://github.com/supermodel/supermodel-cli) can be used to create, validate or convert the models into various formats such as OpenAPI Spec, GraphQL schema, Avro schema, and others. Refer to the Supermodel CLI tool [documentation](https://github.com/supermodel/supermodel-cli#overview) for further details. 

### Always Available Models

When published to http://supermodel.io a model becomes globally available under its `$id` (e.g., `http://supermodel.io/starwars/Starship`), can be referred to in any other JSON Schema or consumed via http://supermodel.io API. Visit http://supermodel.io/starwars/Starship for further details on how to reference the model. 

[<img src="https://supermodel.io/static/media/badge.34435ccd.svg" width="200">](http://supermodel.io)

# Star Wars Supermodel
Demo models for http://supermodel.io

## Overview

[![CircleCI](https://circleci.com/gh/supermodel/starwars.svg?style=svg)](https://circleci.com/gh/supermodel/starwars)

Supermodel demo models using the [Star Wars API](https://swapi.co/) "theme", the models can be found in the in the [supermodel/starwars](https://github.com/supermodel/starwars/tree/master/supermodel/starwars) folder or directly viewed at https://supermodel.io/starwars.

### Supermodel Models 

#### Conventions
Supermodel data models follows these conventions: 

1. Models are, written as [JSON Schema in YAML format](http://json-schema.org/), one schema definition per one YAML file. 
1. Every model must start with JSON Schema `$id`.
1. A model should specify the used version of JSON Schema in the `$schema` field.

A model can freely reference any other model or model property using the JSON Schema `$ref` reference mechanism. The reference can point to any JSON Schema on the web, or it can be relative to the current model.

#### Model Example

```
$id: http://supermodel.io/starwars/core/Person
$schema: http://json-schema.org/draft-07/schema#

title: Person
type: object
description: >-
  An individual person or character within the Star Wars universe.

properties:
  name: 
    type: string
    examples:
      - Luke Skywalker
      - Darth Vader
```

### CLI 

The [Supermodel CLI tool](https://github.com/supermodel/supermodel) can be used to create, validate schemas or convert the models into various formats such as OpenAPI Spec, GraphQL schema, Avro schema, and others. 

See the [package.json](https://github.com/supermodel/starwars/blob/master/package.json) scripts section for examples how to use the Supermodel CLI.

Refer to the Supermodel CLI tool [documentation](https://github.com/supermodel/supermodel) for further details.

### Always Available Models

When published to http://supermodel.io, a model becomes globally available under its `$id` (e.g., `http://supermodel.io/starwars/core/Starship`). The model can be referred to by any other JSON Schema or consumed via http://supermodel.io API. 

Visit http://supermodel.io/starwars/core/Starship for further details on how to reference the model. 

### OpenAPI Specification, Avro Schema, GraphQL Schema Examples

This repository demonstrates how OpenAPI Specification 2.0, GraphQL Schema and Avro Schema are build from the supermodels. Refer to the [build](https://github.com/supermodel/starwars/tree/master/build) folder for the build artifacts.

Sources are as follows:

- **OpenAPI Specfication**: `starwars-api.oas2.yaml` + `./supermodel/starwars/core` models
- **Avro** (Film Kafka Topic): `/supermodel/starwars/avro/FilmTopic` model
- **GraphQL**: `./supermodel/starwars/core` models



---
alias: ij2choozae
path: /docs/reference/schema/types
layout: REFERENCE
description: GraphQL types define the structure of your data and consist of fields. They can be compared with table schemas in SQL databases.
tags:
  - platform
  - types
  - data-schema
related:
  further:
    - ahwoh2fohj
    - teizeit5se
    - goh5uthoc1
    - uhieg2shio
    - oe3raifamo
  more:
    - ga2ahnee2a
    - aing2chaih
---

# GraphQL Types

A *GraphQL type* defines the structure for a certain type of your data. If you are familiar with SQL databases you can think of a type as the schema for a table. A type has a name, an optional description and one or multiple [fields](!alias-teizeit5se).

> Previously, types were referred to as models in this documentation.

An instantiation of a type is called a *node*. The collection of all nodes is what you would refer to as "your data". The term node refers to a node inside your data graph.

Every type you define will be available as a type in your GraphQL schema. A common notation to quickly describe a type is the [GraphQL IDL](!alias-kr84dktnp0) (interface definition language).

## GraphQL Types in the Data Schema

A GraphQL type is defined in the Data Schema with the keyword `type`:

```graphql
type Story {
  id: ID! @isUnique
  text: String!
  isPublished: Boolean @defaultValue(value: "false")
  author: Author! @relation(name: "AuthorStories")
}

type Author {
  id: ID! @isUnique
  age: Int
  name: String!
  stories: [Story!]! @relation(name: "AuthorStories")
}
```

## Generated Operations Based On Types

The types that are included in your schema influence the available [queries](!alias-nia9nushae), [mutations](!alias-ol0yuoz6go) and [subscriptions](!alias-ol0yuoz6go).

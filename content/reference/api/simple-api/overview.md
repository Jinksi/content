---
alias: heshoov3ai
path: /docs/reference/simple-api/overview
layout: REFERENCE
description: The Simple API can be consumed by GraphQL clients such as Meteor's Apollo Client, graphql-request or simpler clients like cURL or plain HTTP.
simple_relay_twin: aizoong9ah
tags:
  - simple-api
related:
  further:
    - aizoong9ah
  more:
---

# API

The **Simple API** offers many ways to interact with the data in your Graphcool project. Different options exist to [make requests to the Simple API](!alias-koo4eevun4).

The foundation for the API are the **automatically generated CRUD-style operations** that are based on your [data schema](!alias-ahwoh2fohj). Additionally, **you can use [Schema Extensions](!alias-xohbu7uf2e) to enhance your GraphQL schema** with additional operations. There are three categories of available operations:

* [GraphQL Queries](!alias-nia9nushae) are used to fetch data.
* [GraphQL Mutations](!alias-ol0yuoz6go) are used to modify data.
* [GraphQL Subscriptions](!alias-aip7oojeiv) are used to get notified of data changes in realtime.

The Simple API offers an [error handling](!alias-aecou7haj9) concept as well.

> Note: The Simple API is meant for GraphQL clients like Apollo or `graphql-request`. If you are using Relay as your GraphQL client, check the [Relay API](!alias-aizoong9ah) instead. The two APIs don't differ too much in features, but mostly in usage.

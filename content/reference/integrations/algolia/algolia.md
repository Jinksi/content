---
alias: emaig4uiki
path: /docs/reference/integrations/algolia
layout: REFERENCE
description: Algolia is a hosted Search API that delivers instant results. Auto-sync your GraphQL data to Algolia search indices with this integration.
tags:
  - platform
  - integrations
  - algolia
  - data-management
related:
  further:
    - ahwoh2fohj
    - iaxohpee8o
    - naed3eecie
  more:
    - aroozee9zu
    - aing7uech3
---

# Algolia Integration

The [Algolia](https://algolia.com) integration allows you to automatically synchronize your data with Algolia search indices. While the Graphcool APIs offer very flexible query arguments for [filtering](!alias-xookaexai0) or [ordering](vequoog7hu), Algolia is specialized in full-text searches and comes with prepared libraries to build great search experiences.

## Activating the Algolia Integration

In your Algolia settings, copy the Algolia App Id and create a new API key with **Add Records** and **Delete Records** enabled:

![](./algolia-settings.png?width=295)

Enter the collected credentials in the Algolia integration popup in the [Integration View](!alias-uh8shohxie):

![](./algolia-credentials.png?width=295)

## Creating new Search Indices

* select the type that you want to define the index on
* enter the name of the search index. This name needs to be entered in your application as well!
* enter the query that defines the structure of the search index

![](./algolia-create-index.png)

## Limitations

* An initial sync operation will only sync the first 1000 nodes over to Algolia. You can always initiate a sync for a specific node by "touching" it. Here's an [example script for touching all nodes of a certain type](https://github.com/graphcool-examples/scripts/tree/master/touch-nodes).
* If you use a filter in your Algolia Index query, **nodes will not be deleted from Algolia when they don't match the filter after an update operation** . If you want to delete records from Algolia if a node doesn't match a certain condition, you can [setup a Server-Side Subscription Function](!alias-ahlohd8ohn) that removes the record using the Algolia API directly.

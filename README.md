# invalid-service-definition

## Reproduction

```sh
graphcool deploy
```

results in

```
Creating service service in cluster shared-eu-west-1... ✔
Bundling functions... 1.3s
Deploying... 172ms
There are issues with the new service definition:

  FirstType
    ✖ The model `FirstType` is missing the @model directive. Please add it. See: https://github.com/graphcool/graphcool/issues/817
    ✖ All models must specify the `id` field: `id: ID! @isUnique`

  SecondType
    ✖ The model `SecondType` is missing the @model directive. Please add it. See: https://github.com/graphcool/graphcool/issues/817
    ✖ All models must specify the `id` field: `id: ID! @isUnique`

Here are your GraphQL Endpoints:

  Simple API:        https://api.graph.cool/simple/v1/serviceId
  Relay API:         https://api.graph.cool/relay/v1/serviceId
  Subscriptions API: wss://subscriptions.graph.cool/v1/serviceId
```

but service shouldn't be created after all

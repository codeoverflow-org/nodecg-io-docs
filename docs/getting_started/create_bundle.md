# Create your first bundle

To actually use nodecg-io you need to create a bundle. Here's a step-by-step guide to create one.

## Dependencies

Think of what services your bundle needs. Take a look at the [service list](../services.md) if to see what services are available. If you need a service that is not yet available consider [creating it](../contribute/create_service.md).

## Create a package

Your package is a standard NodeCG bundle. See their [website](https://nodecg.com/) for more info. The bundle should be dependent on `nodecg-io-core` and all services it needs. Then you define `module.exports` as a function that takes a NodeCG instance. In that function you initialise your bundle.

## Adding availability handlers

Here's an example for twitch:

```typescript
const twitch = requireService<TwitchServiceClient>(nodecg, 'twitch');

twitch?.onAvailable(client => {
  // Do sth when twitch is available
});

twitch?.onUnavailable(() => {
  // Do sth when twitch is not / no longer available
});
```

If you need multiple services you can save them in global variables and access them using the `service.getClient()` function which returns an optional of the client. If it isn't currently set it will be `undefined`.

## Test it

Start NodeCG and provide your bundle with all required services.

## Share it!

If you share your work others might get happy with it. And we made nodecg-io for you and the nodecg people made nodecg for you. Many people spent much time for you to create cool content that easy and if you shared your work others could create good content more easily as well.

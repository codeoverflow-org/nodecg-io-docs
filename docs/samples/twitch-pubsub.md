## Using the Twitch PubSub sample bundle

The twitch-pubsub example bundle in `samples/twitch-pubsub` demonstrates the
ability to use the Twitch PubSub API. Here is a guide to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A Twitch oAuth-Key

_Note:_ If you don't have such a key yet, you can generate it on
<https://twitchtokengenerator.com/>, select custom scope token and select these
scopes: `channel_subscriptions`, `bits:read` and `channel:read:redemptions`

### Configure the Twitch PubSub sample bundle

1. In NodeCG, create a new twitch-pubsub service instance.

2. Enter your Twitch OAuth Key:

    ```json
    {
        "oauthKey": "oauth:abcdef...."
    }
    ```

    After entering it, click save.

3. Set the sample's (`twitch-pubsub`) dependency to be the newly created service
   instance (of type `twitch-pubsub`).

4. Check the NodeCG logs:

    You should see an error or a success message and a log entry for each
    subscription, bits, bits badge unlock and channel point redemption event.

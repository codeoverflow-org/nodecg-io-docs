## Using the twitter sample bundle

The Twitter timeline bundle retrieves some of the latest tweets from _skate702_
and printing them to your console.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   An [app](https://developer.twitter.com/en/apps) and their following keys and
    tokens
    -   The _API key_ here **oauthConsumerKey**
    -   The _API secret key_ here **oauthConsumerSecret**
    -   The _Access token_ here **oauthToken**
    -   The _Access token secret_ here **oauthTokenSecret**

_Note:_ You will need a Twitter developer account
(<https://developer.twitter.com/en/apply-for-access>) to get the necessary keys
and tokens.

### Configure the sample bundle

1. In NodeCG, create a new twitter service instance using the left upper menu.

2. Enter credentials for twitter.

    The created instance should be automatically selected, if not select it in
    the upper left menu. Enter your Twitter keys and tokens in monaco (the
    text-editor on the right) in this format:

    ```json
    {
        "oauthConsumerKey": "<API key>",
        "oauthConsumerSecret": "<API secret key>",
        "oauthToken": "<Access token>",
        "oauthTokenSecret": "<Access token secret>"
    }
    ```

    After entering it, click save.

3. Set the created twitter service instance to the service dependency of the
   twitter-timeline bundle.

    Select the twitter-timeline bundle and the twitter service in the left
    bottom menu. Then select the service instance that should be used by the
    twitter-timeline bundle (in this case the name of the previously created
    twitter instance).

4. Check the NodeCG logs

    You should see an error or a success message and up to 50 Twitter messages
    tweeted by the user that is hardcoded in
    [samples/twitter-timeline/extension/index.ts](/samples/twitter-timeline/extension/index.ts)
    as `screen_name`.

## Need to know for creating your own twitter bundle

### A little description of the twitter client and it's usage

-   The client implements the different
    [API endpoints](https://developer.twitter.com/en/docs/api-reference-index)
    with two functions

    ```typescript
      client.get("<get endpoint name>", params, callback)
      client.post("<post endpoint name>", params, callback)

      // Instead of callbacks it can be used with promises
      client
        .get("statuses/user_timeline", {screen_name: "skate702"})
        .then((tweets) => /* Do something with the tweets */)
        .catch((error) => /* Handle error */);

      // Or async and await as well
      try {
        const tweets = await client.get("statuses/user_timeline", {screen_name: "skate702"});
        // Do something with the tweets
      } catch (error) {
        // Handle error
      }
    ```

#### A more precise description of what can be done with this twitter client can be found [here](https://github.com/desmondmorris/node-twitter#readme)

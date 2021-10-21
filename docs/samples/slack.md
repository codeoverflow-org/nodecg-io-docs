## Using the Slack sample bundle

The Slack example bundle in `samples/slack-post` demonstrates the ability to
list all channels into the console and sends a message to a channel which you
have to configure to your channel ID.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   a Slack Bot token

_Note:_ If you don't have such a token yet, you can create your own app with
token on [this](https://app.slack.com/apps-manage/) page.

### Configure the Slack sample bundle

1. In NodeCG, create a new slack service instance using the left upper menu.

2. Enter your Slack app token.

    The created instance should be automatically selected, if not select it in
    the upper left menu. Enter your token in monaco (the text-editor on the
    right) in this format:

    ```json
    {
        "token": "your-token-goes-here"
    }
    ```

    After entering it, click save.

3. Set the created slack service instance to the service dependency of the slack
   bundle.

    Select the slack bundle and the slack service in the left bottom menu. Then
    select the service instance that should be used by the slack bundle (in this
    case the name of the previously created slack instance).

4. Check the NodeCG logs

    You should see an error or a login message.

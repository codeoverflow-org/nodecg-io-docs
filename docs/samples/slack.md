## Using the Slack sample bundle

The Slack example bundle in `samples/slack-post` demonstrates the ability to list all channels into the console and sends a message to a channel which you have to configure to your channel ID.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   a Slack Bot token

_Note:_ If you don't have such a token yet, you can create your own app with token on [this](https://app.slack.com/apps-manage/) page.

### Configure the Slack sample bundle

1. Start nodecg with nodecg-io installed. The slack bundle is currently part of it, so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new slack service instance using the left upper menu.

5. Enter your Slack app token.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your token in monaco (the text-editor on the right) in this format:

    ```json
    {
        "token": "your-token-goes-here"
    }
    ```

    After entering it, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created slack service instance to the service dependency of the slack bundle.

    Select the slack bundle and the slack service in the left bottom menu and then select the service instance that should be used by the slack bundle (in this case the name of the previously created slack instance).

7. Check the nodecg logs

    You should see an error or a login message.

## Using the Reddit sample bundle

The reddit-message-read example bundle in `samples/reddit-msg-read` demonstrates the ability to read recent posts from a subreddit (in this case `r/skate702`)

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   a Reddit Application (Should be of type script for own purpose)

_Note:_ If you don't have such an application yet, you can get one [here](https://www.reddit.com/prefs/apps).

### Configure the Reddit sample bundle

1. Start nodecg with nodecg-io installed. The reddit-message-read bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new reddit service instance using the left upper menu.

5. Enter your applications id and secret and your own username and password. Zhe entered username and password must be for the  user who registered the application.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your data in monaco (the text-editor on the right) in this format:

    ```json
    {
        "clientId": "Your client Id (This is displayed right below the application name)",
        "clientSecret": "Your client secret",
        "username": "Your username",
        "password": "Your password"
    }
    ```

    After entering it, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created reddit service instance to the service dependency of the reddit-message-read bundle.

    Select the reddit-message-read bundle and the Reddit service in the left bottom menu and then select the service instance that should be used by the reddit-message-read bundle (in this case the name of the previously created reddit instance).

7. Check the nodecg logs

    You should see the recent posts in `r/skate702`

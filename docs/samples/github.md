## Using the GitHub sample bundle

The GitHub example bundle in `samples/github` demonstrates the ability to access the GitHub rest API. Here is a guide to how to get it working.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   a GitHub token

_Note:_ If you don't have a token yet, you can create one [here](https://github.com/settings/tokens/new). The token requires at least the `repo` scope.

### Configure the GitHub sample bundle

1. Start nodecg with nodecg-io installed. The GitHub bundle is currently part of it, so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new GitHub service instance using the left upper menu.

5. Enter the GitHub token.

   The created instance should be automatically selected, if not select it in the upper left menu. Enter your GitHub token in monaco (the text-editor on the right) in this format:

    ```json
    {
        "token": "abcdef...."
    }
    ```

   After entering it, click save.

   _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created GitHub service instance to the service dependency of the GitHub bundle.

   Select the GitHub bundle and the GitHub service in the left bottom menu and then select the service instance that should be used by the GitHub sample bundle (in this case the name of the previously created GitHub instance).

7. Check the nodecg logs

   You should see an error or a success message and a list of all your repositories.

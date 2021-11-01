## Using the GitHub sample bundle

The GitHub example bundle in `samples/github` demonstrates the ability to access
the GitHub rest API. Here is a guide to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A GitHub token

!!! Note

    If you don't have a token yet, you can create one
    [here](https://github.com/settings/tokens/new). The token requires at least the
    `repo` scope.

### Configure the GitHub sample bundle

1. In NodeCG, create a new GitHub service instance.
2. Enter the GitHub token:

    ```json
    {
        "token": "abcdef...."
    }
    ```

    After entering it, click save.

3. Set the sample's (`github`) dependency to be the newly created service
   instance (of type `github`).
4. Check the NodeCG logs:

    You should see an error or a success message and a list of all your
    repositories.

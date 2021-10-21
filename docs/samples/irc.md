## Using the IRC sample bundle

The IRC example bundle in `samples/irc` demonstrates the ability to get access
to an IRC chat. This sample is designed to log the twitch IRC chat of skate702.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

### Configure the IRC sample bundle

1. In NodeCG, create a new IRC service instance using the left upper menu.

2. Enter credentials for IRC.

    The created instance should be automatically selected, if not select it in
    the upper left menu. In this example we will "anonymously" connect to the
    twitch IRC chat. Enter the config in this format:

    ```json
    {
        "host": "irc.chat.twitch.tv",
        "port": 6667,
        "nick": "justinfan123456"
    }
    ```

    Here you may want to change the numbers of the nick to be unique to you.

    After entering it, click save.

3. Set the created IRC service instance to the service dependency of the IRC
   sample bundle.

    Select the IRC sample bundle and the IRC service in the left bottom menu.
    Then select the service instance that should be used by the IRC sample
    bundle (in this case the name of the previously created IRC instance).

4. Check the NodeCG logs

    You should see an error or a success message and all twitch messages that
    are written in the twitch channel that is hardcoded in
    `samples/irc/extension/index.ts`.

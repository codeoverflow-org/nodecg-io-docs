## Using the TIANE-Discord sample bundle

The TIANE-Discord example bundle in `samples/tiane-discord` shows how to make
TIANE act as a discord bot. TIANE is a German open source smart home assistant
written in python. Here is a guide to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A working [TIANE](https://github.com/FerdiKr/TIANE) server installation. (No
    room client required)
-   a Discord Bot token

!!! NOTE

    If you don't Discord Bot token yet, you can follow
    [this](https://discordjs.guide/preparations/setting-up-a-bot-application.html)
    guide.

### Configure the TIANE sample bundle

1. Edit the file `samples/tiane-discord/extension/index.ts`. Look for this line:

    ```ts
    const discordChannel = ""; // Insert channel for the discord bot here
    ```

    Put the channel ID of a discord channel where you want to talk to TIANE
    between the quotation marks. See
    [here](https://github.com/Chikachi/DiscordIntegration/wiki/How-to-get-a-token-and-channel-ID-for-Discord)
    to find out how to get a channel ID.

2. Run `npm run build` in the main nodecg-io directory.
3. Edit the file `server/TIANE_config.json` on your TIANE server:

    ```json
    {
        "websocket": "enabled",
        "websocket_port": 19526,
        "websocket_timeout": 20
    }
    ```

    Make sure `websocket` is either set to `enabled` or `secure` and set a port
    of your desire.

4. In the NodeCG dashboard, create a new TIANE service instance.

5. Enter address of the TIANE-Server. Enter host and port you just set in
   `server/TIANE_config.json` in this format:

    ```json
    {
        "address": "127.0.0.1:19526"
    }
    ```

    After entering it, click save.

6. Create a new Discord service instance.

7. Set the sample's (`tiane-discord`) dependencies to be the newly created
   service instances (of type `tiane` & `discord`).

8. Ping your discord bot in the channel you set in the first step and ask TIANE
   something.

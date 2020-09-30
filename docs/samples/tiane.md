## Using the TIANE-Discord sample bundle

The TIANE-Discord example bundle in `samples/tiane-discord` shows how to make tiane act as a discord bot. TIANE is a german open source smart home assistant written in python. Here is a guide to how to get it working.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   A working [TIANE](https://github.com/FerdiKr/TIANE) server installation. (No room client required)
-   a Discord Bot token

### Configure the TIANE sample bundle

1. Edit the file `samples/tiane-discord/extension/index.ts`. Look for this line
    ```
    const discordChannel = ""; // Insert channel for the discord bot here
    ```
    and put the channel id of a discord channel where you want to talk to TIANE between the quotation marks. See [here](https://github.com/Chikachi/DiscordIntegration/wiki/How-to-get-a-token-and-channel-ID-for-Discord) to find out how to get a channel id.
   
2. Run `npm run build` in the main nodecg-io directory.
   
3. Edit the file `server/TIANE_config.json` on your TIANE server:

    ```json
    {
        "websocket": "enabled",
        "websocket_port": 19526,
        "websocket_timeout": 20
    }
    ```
   
    Make shure `websocket` is either set to `enabled` or `secure` and set a port of your desire.

4. Start nodecg with nodecg-io installed. The TIANE-Discord bundle is currently part of it so it should also be loaded.

5. Go to the `nodecg-io` tab in the nodecg dashboard.

6. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

7. Create a new TINE service instance using the left upper menu.

8. Enter address of the TIANE-Server

    The created instance should be automatically selected, if not select it in the upper left menu. Enter the host and the port you just set in `server/TIANE_config.json` in this format:

    ```json
    {
        "address": "127.0.0.1:19526"
    }
    ```

    After entering it, click save.

    _Note:_ If you don't see the editor on the right, try reloading the page.
    
9. Create a new Discord service instance. (See the [Discord Sample](discord.md) on how to do this)

10. Set the created TIANE and Discord service instances to the service dependency of the TIANE-Discord bundle.

    Select the TIANE-Discord bundle and the TIANE service in the left bottom menu and then select the service instance that should be used by the TIANE-Discord bundle (in this case the name of the previously created twitch instance). Then do the ame for the discord bundle.

11. Ping your discord bot in the channel you set in the first step and ask tiane something.

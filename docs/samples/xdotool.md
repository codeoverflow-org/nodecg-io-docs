## Using the Xdotool sample bundle

The Xdotool sample bundle in `samples/xdotool` shows how to use the xdotool service to execute [xdotool commands](http://manpages.ubuntu.com/manpages/trusty/man1/xdotool.1.html) by minimising the currently active window.

### Prerequisites

* Working NodeCG & nodcg-io installation
* xdotool installed (Only works on linux)

### Configure the Twitch sample bundle

1. Start nodecg with nodecg-io installed. The xdotool bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new xdotool service instance using the left upper menu.

5. Enter settings Port `-1` tells nodecg-io to use a locally installed xdotool.

   The created instance should be automatically selected, if not select it in the upper left menu. Enter your Twitch oauth Key in monaco (the texteditor on the right) in this format:

   ```json
   {
       "host": "127.0.0.1",
       "port": -1
   }
   ```

   After entering it, click save.

6. Set the created xdotool service instance to the service dependency of the xdotool bundle.

7. Your browser window should get minimised.
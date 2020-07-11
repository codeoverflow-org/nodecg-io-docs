## Using the Xdotool sample bundle

The Xdotool sample bundle in `samples/xdotool` shows how to use the xdotool service to execute [xdotool commands](http://manpages.ubuntu.com/manpages/trusty/man1/xdotool.1.html) by minimizing the currently active window.

### Prerequisites

* Working NodeCG & nodecg-io installation
* xdotool installed (Only works on linux)

### Configure the Xdotool sample bundle

1. Start nodecg with nodecg-io installed. The xdotool bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new xdotool service instance using the left upper menu.

5. Enter settings port `-1` tells nodecg-io to use a locally installed xdotool.

   The created instance should be automatically selected, if not select it in the upper left menu. Configure local xdotool in monaco (the texteditor on the right) using this config:

   ```json
   {
       "host": "127.0.0.1",
       "port": -1
   }
   ```

   After entering it, click save.

6. Set the created xdotool service instance to the service dependency of the xdotool bundle.

7. Your browser window should get minimized.
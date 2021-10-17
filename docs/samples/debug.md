## Using the Debug sample bundle

The Debug Helper example bundle in `samples/debug` demonstrates the ability to use the debug helper to send same sample data to your bundle, so you can trigger different features and test/debug them.

### Prerequisites

-   Working NodeCG & nodecg-io installation

### Configure the Debug sample bundle

1. Start NodeCG with nodecg-io installed. The Debug sample bundle is currently part of it, so it should also be loaded.
2. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.
3. Create a new Debug service instance using the left upper menu.
4. Set the Debug service instance to the service dependency of the Debug sample bundle.
   Select the Debug sample bundle and the Debug service in the left bottom menu and then select the service instance that should be used by the Debug sample bundle (in this case the name of the previously created Debug instance).
5. Go to the nodecg-io-debug dashboard and use some buttons or other inputs.
6. Check the nodecg log. It should contain a message for each action you did and the passed values.

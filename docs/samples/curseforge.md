## Using the CurseForge sample bundle

The CurseForge example bundle in `samples/curseforge` demonstrates the ability to search for different addons with the id or search with specific values for matching addons. Here is a guide how to get it working.

### Prerequisites

- Working NodeCG & nodecg-io installation

### Configure the CurseForge bundle

1. Start NodeCG with with nodecg-io installed. The CurseForge bundle is currently part of it, so it should also be loaded.
2. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.
3. Create a new CurseForge service instance using the left upper menu.
4. Set the CurseForge service instance to the service dependency of the CurseForge bundle. 
    Select the CurseForge bundle the the CurseForge service in the left bottom menu and then select the service instance that should be used by the CurseForge bundle (in this case the name of the previously created CurseForge instance).
5. Check the NodeCG logs. You should see two lists of addons.
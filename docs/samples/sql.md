## Using the SQL sample bundle

The SQL example bundle in `samples/sql` demonstrates the ability to access databases. Here is a guide to how to get it working.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   A database supported by [knex](https://knexjs.org/#Installation)

_Note:_ If you don't have a database yet and just want to test things you can use sqlite3 and don't need to set up a database server. You can always move to a different database type later.

### Configure the SQL sample bundle

1. Start nodecg with nodecg-io installed. The SQL sample bundle is currently part of it, so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new SQL service instance using the left upper menu.

5. Enter configuration for SQL.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your used database client and a [knex connection object](https://knexjs.org/#Installation-client) in monaco (the text-editor on the right) in this format:

    ```json
    {
        "client": "mysql",
        "connection": {
            "host": "localhost",
            ...
        }
    }
    ```

    After entering it, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created SQL service instance to the service dependency of the SQL sample bundle.

    Select the SQL sample bundle and the SQL service in the left bottom menu and then select the service instance that should be used by the SQL sample bundle (in this case the name of the previously created SQL instance).

7. Check the nodecg logs

    Your first run of the sample bundle will probably fail because your database doesn't contain the used tables.
    Check `samples/sql/extension/index.ts` and create the tables as used or create your own tables and adapt the sample accordingly.
    You can also use this code as a reference on how to use the SQL client to do your queries.

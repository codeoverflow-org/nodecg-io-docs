## Using the SQL sample bundle

The SQL example bundle in `samples/sql` demonstrates the ability to access
databases. Here is a guide to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A database supported by [knex](https://knexjs.org/#Installation)

_Note:_ If you don't have a database yet and just want to test things you can
use sqlite3 and don't need to set up a database server. You can always move to a
different database type later.

### Configure the SQL sample bundle

1. In NodeCG, create a new SQL service instance.

2. Enter your used database client and a
   [knex connection object](https://knexjs.org/#Installation-client) for SQL:

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

3. Set the sample's (`sql`) dependency to be the newly created service instance
   (of type `sql`).

4. Check the NodeCG logs:

    Your first run of the sample bundle will probably fail because your database
    doesn't contain the used tables. Check `samples/sql/extension/index.ts` and
    create the tables as used or create your own tables and adapt the sample
    accordingly. You can also use this code as a reference on how to use the SQL
    client to do your queries.

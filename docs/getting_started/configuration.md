# Configuration

Since version `0.2.0` nodecg-io has a configuration feature to save some settings without needing to code something or log in. The configuration file for
this feature is at `cfg/nodecg-io-core.json` inside your nodecg installation. This file does not exist by default, you need to create it yourself.

The currently only thing you can configure is automatic login, but there may be more configurable options in the future.

## Automatic login

Automatic login will automatically load nodecg-io when nodecg starts using the provided password.

Therefore, nodecg-io will be able to decrypt your configuration for your service instances and provide your bundles with service clients without you logging in to nodecg-io using the dashboard.
This is especially useful if you are running nodecg with nodecg-io on a server which may reboot from time to time to ensure that your bundles are always working without you needing to manually log in after each restart.

**Security warning:** Having both the encrypted configuration and your used password saved on disk defeats nodecg-io's data-at-rest encryption.
Any program that can read disk contents can access your credentials of any service instance. We discourage using this and if you really want to use it you should be extra cautious about which bundles you install.

Options of automatic login:

- `enabled` (boolean)

  Automatic login will be only enabled if this `enabled` option is set to `true`.
  This option can be used to temporarily disable automatic login without needing to delete the whole automatic login configuration
  and allows for easy re-enabling without needing to enter the password in the config again.

- `password` (string)

  This is the password that will be used to log in. It should be the password you use to log in to nodecg-io.
  If this password is wrong an error will be logged after startup.

Example config:

```json
{
    "automaticLogin": {
        "enabled": true,
        "password": "ThisIsMyPassword.PleaseChangeMe"
    }
}
```

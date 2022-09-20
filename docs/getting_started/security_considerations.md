# Security considerations

nodecg-io is managing all configuration values for your service instances which consists of authentication credentials for third party services.
nodecg-io tries to protect this sensitive data but can't make it completely safe due to constraints in the NodeCG architecture.

This document will explain what nodecg-io can and can't do to protect your sensitive configuration data including credentials.
The first part consist of our security claims and the second part describes how achieve those claims.

## Security claims

These claims all assume that you use a good strong password and take care of it properly.

1.   No service configuration is accessible to someone with only filesystem access.
    -   A exception to this is a nodecg-io install with automatic login as the password is stored in plain text.
2.   No bundle will be able to access your plain text password.
3.   All loaded bundles may change nodecg-io settings like deleting instances
4.   All loaded bundles may access all your configurations and passwords.
    -   It is highly recommended to only use bundles you trust!
5.   Anyone intercepting network traffic between the NodeCG instance and browser with a logged in dashboard can access all configuration and passwords.
    -   It is highly recommended to configure NodeCG to use HTTPS when using untrusted networks (e.g. the internet, open wifi if your NodeCG port is not firewalled)

## Implementation

1.   The configuration is stored encrypted only in a NodeCG replicant. If someone reads the persistent value of the replicant from the filesystem the configuration cannot be read because it is encrypted using your chosen password.
2.   When you enter your password inside the dashboard it is used to derive a encryption key using argon2id. Only this encryption key is ever transmitted and leaves the browser tab. Therefore other bundles can listen to the communication but it only contains the derived encryption key, not your plain text password.
3.   Bundles can listen to the login message from the dashboard to get the encryption key. This can be used to send authenticate messages to the nodecg-io-core bundle to add/delete instances, change service instance assignments and do everything that is possible in the dashboard.
4.   As mentionted in 3 all bundles can get the encryption key. The encrypted configuration is stored in a replicant which can be accessed by all bundles as well. Using these two any bundle could decrypt the configuration and have access to it.
5.   Same as in 3, everyone intercepting network traffic can intercept the encryption key that gets send to the core using NodeCG messages. 


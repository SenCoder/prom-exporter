
## Setting the MySQL server's data source name

The MySQL server's [data source name](http://en.wikipedia.org/wiki/Data_source_name)
must be set via the `DATA_SOURCE_NAME` environment variable.
The format of this variable is described at https://github.com/go-sql-driver/mysql#dsn-data-source-name.


## Customizing Configuration for a SSL Connection
if The MySQL server supports SSL, you may need to specify a CA truststore to verify the server's chain-of-trust. You may also need to specify a SSL keypair for the client side of the SSL connection. To configure the mysqld exporter to use a custom CA certificate, add the following to the mysql cnf file:

```
ssl-ca=/path/to/ca/file
```

To specify the client SSL keypair, add the following to the cnf.

```
ssl-key=/path/to/ssl/client/key
ssl-cert=/path/to/ssl/client/cert
```
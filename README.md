# schemaspy-postgres
Simple docker image for using schemaspy with postgres

Provide a link to your postgres container aliased to dbhost, then provide the database name, credentials, and schema as arguments.

###### Example

```bash
docker run \
    -v /vagrant/schemaspy:/output \
    --link my_running_postgres_container:dbhost \
    russgray/schemaspy-postgres \
    -db my_database \
    -u my_username \
    -p my_password \
    -s public
```
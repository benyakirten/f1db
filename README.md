The original database was downloaded from http://ergast.com/downloads/f1db.sql.gz. The SQL file was not compatible with Postgres, and pgloader had some difficulty interacting with the mysql database as described (even downgraded to mysql 8). Therefore, there have been some alterations made that allows the file to be easily loaded using the following command:

```bash
createdb f1db
psql -d f1db -U <username> -f f1db.sql
```

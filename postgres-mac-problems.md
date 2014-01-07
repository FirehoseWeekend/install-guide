### Having Problems with PostgreSQL?

After you run the installer this should get you back up and running.

```
export me=`whoami` && sudo -u $me createuser -s postgres
psql postgres
\password postgres
```

**IMPORTANT**: When prompted for a password enter: `password`.

```
sudo mv /Library/PostgreSQL/9.3/data /Library/PostgreSQL/9.3/data-old
initdb
```


### Test it out

```
psql --username postgres -h localhost --password
```

**When prompted for a password enter `password`**, and you should be prompted with something that looks like:

```
psql (9.3.2)
Type "help" for help.

postgres=#
```

Press **CTRL+D** to change the `postgres=#` into the `$`.


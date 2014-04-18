Nitrous.io Postgres Info
----------

We'll go over what this means Saturday.

This installer will install postgresql in such a way that you'll need to adjust your database.yml file to look like this in each of the three sections. When editing this file, note: you'll need to add the port part and the host and remove the username and password parts. Also be sure to adjust the database section to fill in your application name where there are all caps. NOTE: indentation is super important - make sure they line up and rather than copy & pasting this, type this in):


### database.yml


```
development:
  adapter: postgresql
  encoding: unicode
  database: appname-dev
  pool: 5
  host: localhost
  username: action
  password:

test:
  adapter: postgresql
  encoding: unicode
  database: appname-test
  pool: 5
  host: localhost
  username: action
  password:

production:
  adapter: postgresql
  encoding: unicode
  database: appname-prod
  pool: 5
  host: localhost
  username: action
  password:
```

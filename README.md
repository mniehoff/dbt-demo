# dbt Demo Project

Based on the dbt own [jaffle shop demo](https://github.com/dbt-labs/jaffle_shop)

## Requirement

### External
In order to run the dbt demo we require a "running" SQL-DB.
```
docker run --name some-postgres -e POSTGRES_PASSWORD=<secret> -e POSTGRES_USER=<user> -p 5432:5432 postgres
```
Moreover, the demo expects three tables `raw.raw_customers`, `raw.raw_orders` and `raw.raw_payments` in the database these tables can be
filled with data using the provided `.csv` files in the [sample_data](sample_data) folder.

### Internal
A working installation of [dbt](https://docs.getdbt.com/docs/get-started/installation).

Most of the time this will be a `pip install dbt-postgres`

Check with
```bash
dbt --version
installed version: 1.6.6
   latest version: 1.6.6

Up to date!

Plugins:
  - postgres: 1.6.6```
```

The DB connection has to be setup in a `profiles.yml` file which can be created based on the
provided [profiles_template.yml](profiles_template.yml).

### Using the starter project

Try running the following commands:
- dbt run
- dbt test

Use a Database Management Tool like TablePlus, DBeaver or pgadmin to see the effects in the database.

### Resources:
- Learn more about dbt [in the docs](https://docs.getdbt.com/docs/introduction)

# SQL data exploration project
Parch and Posey database was used to explore different functional aspects of SQL from basic to advanced.

This short project is to help anyone to setup their own local environment and practice querying. 

## Setting up the environment:
### Database used: 
Parch and Posey, a hypothetical paper company's sales data of different types of paper (gloss, standard). The database consists of different [tables](https://github.com/akshayreddykotha/sql-data-exploration-project/tree/master/data) linked with a database schema. If you want to create a database from scratch, you can use these excel files and set it up.

### Alternate way:
Gathered the [database dump](https://github.com/akshayreddykotha/sql-data-exploration-project/blob/master/parch_and_posey_db_archivedump) file from [Ayushi](https://github.com/ayushi-b). The database dump was created using `pg_dump` and it is an archive unlike a database dump file with an sql extension. For difference between both, refer to this [question](https://stackoverflow.com/questions/2732474/restore-a-postgres-backup-file-using-the-command-line).

### Load database dump in windows:

1. Install [PostgreSQL](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads) on your desktop
2. Open windows CMD
3. Go to the folder where you downloaded the `parch_and_posey_db_archivedump` file.
4. Run this `pg_restore --create --dbname=postgres --username=postgres parch_and_posey_db_archivedump`. You do not need to create a new database prior to loading this database. This command loads the database into a new database named *Parch & Posey Database*.
5. On running this command, you might be asked a password which you might have set during installation of PostgreSQL on your machine.
6. Creation of database prior to load/restore isn't preferred to avoid conflicts.

Now open the pgAdmin4 and connect to server and database. You are now open to querying the database via the query tool within this GUI.

## Practice Querying - The Ulterior Motive for setting up the environment:
### Sample Queries:

#### Joins
1. Provide a table for all web_events associated with account name of Walmart. There should be three columns. Be sure to include the primary_poc, time of the event, and the channel for each event. Additionally, you might choose to add a fourth column to assure only Walmart events were chosen. 

2. Provide a table that provides the region for each sales_rep along with their associated accounts. Your final table should include three columns: the region name, the sales rep name, and the account name. Sort the accounts alphabetically (A-Z) according to account name. 

3. Provide the name for each region for every order, as well as the account name and the unit price they paid (total_amt_usd/total) for the order. Your final table should have 3 columns: region name, account name, and unit price. A few accounts have 0 for total, so I divided by (total + 0.01) to assure not dividing by zero.

Check your queries using this file [Joins_11_part_1.sql](https://github.com/akshayreddykotha/sql-data-exploration-project/blob/master/Joins_11_part_1.sql). 

New queries are always welcome :). Ping to collaborate and contribute.

Thanks to [Derek](https://www.linkedin.com/in/dereksteer/) from [MODE Analytics](https://modeanalytics.com) for hosting such a concept-wise outline of what all an SQL aspirant needs to know and learn about. Cheers to [Udacity](https://classroom.udacity.com)!

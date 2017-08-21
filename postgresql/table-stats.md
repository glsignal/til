When working with large tables, running a `count` may be expensive and unnecessary.

Instead, you can get a rough idea of the size of tables by running the following query:

```sql
SELECT schemaname,relname,n_live_tup FROM pg_stat_user_tables ORDER BY n_live_tup DESC;

```

which will get some relevant statistics from the data that postgres' query optimizer users when determining how best to execute a query.

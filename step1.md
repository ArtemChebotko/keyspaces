<div class="top">

# Keyspace
### [◂](command:katapod.loadPage?intro){.steps} Step 1 of 7 [▸](command:katapod.loadPage?step2){.steps}
</div>

A *keyspace* is a namespace for a set of tables sharing a data replication strategy and some options. 
It is conceptually similar to a "database" in a relational database management system. 
Tables, materialized views, indexes and other schema objects are always defined within a keyspace.

To create a keyspace, Cassandra Query Language has the `CREATE KEYSPACE` statement with the following simplified syntax:

<code>
CREATE KEYSPACE [ IF NOT EXISTS ] keyspace_name
    WITH REPLICATION = { replication_map };
</code>

A *keyspace name* can contain alphanumeric characters and underscores. 
By default, names are case-insensitive, but case sensitivity can be forced by using double quotation marks around a name.

A *replication map* specifies a data replication strategy and replication factors. 
`SimpleStrategy` and `NetworkTopologyStrategy` are two available choices for prototyping/learning and production, respectively.

[continue](command:katapod.loadPage?step2){.orange_bar}
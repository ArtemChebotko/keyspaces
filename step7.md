<div class="top">

# Working with keyspaces
### [◂](command:katapod.loadPage?step6){.steps} Step 7 of 7 [▸](command:katapod.loadPage?finish){.steps}
</div>

Try the following five CQL shell commands and CQL statements that are applicable to keyspaces. 

1. List the names of all keyspaces in the cluster:
```
DESCRIBE KEYSPACES;
```

2. Output all CQL statements that can be used to recreate the given keyspace
and all the schema objects that belong to it:
```
DESCRIBE KEYSPACE production_keyspace_2;
```

3. Alter properties of the given keyspace:
```
ALTER KEYSPACE production_keyspace_2
WITH replication = 
     {'class': 'NetworkTopologyStrategy',
      'DC-West': 3, 'DC-East': 5};
```

4. Set the given keyspace as the current working keyspace:
```
USE production_keyspace_2;
```

5. Remove the given keyspace and all the objects that belong to it:
```
DROP KEYSPACE production_keyspace_1;
```

[continue](command:katapod.loadPage?finish){.orange_bar}

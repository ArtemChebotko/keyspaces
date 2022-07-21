<div class="top">

# Keyspaces with SimpleStrategy
### [◂](command:katapod.loadPage?step3){.steps} Step 4 of 7 [▸](command:katapod.loadPage?step5){.steps}
</div>

Create a keyspace with name `simple_keyspace_1` that uses `SimpleStrategy` and a replication factor of `1`:

```
CREATE KEYSPACE simple_keyspace_1
WITH replication = {'class': 'SimpleStrategy', 
                    'replication_factor': 1};
```

The `replication_factor` option specifies a replication factor for the entire cluster. 
That means that `SimpleStrategy` does not respect datacenter layouts and, therefore, is not a good choice 
for production. 


Create a keyspace with name `simple_keyspace_2` that uses `SimpleStrategy` and a replication factor of `2`.
Use tab completion in `cqlsh` to your advantage.

<details>
  <summary>Solution</summary>

```
CREATE KEYSPACE simple_keyspace_2
WITH replication = {'class': 'SimpleStrategy', 
                    'replication_factor': 2};
```

</details>

[continue](command:katapod.loadPage?step5){.orange_bar}
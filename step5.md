<div class="top">

# Keyspaces with NetworkTopologyStrategy
### [◂](command:katapod.loadPage?step4){.steps} Step 5 of 7 [▸](command:katapod.loadPage?step6){.steps}
</div>

Create a keyspace with name `production_keyspace_1` that uses `NetworkTopologyStrategy` and a replication factor of `1` for `DC-West`:

```
CREATE KEYSPACE production_keyspace_1
WITH replication = {'class': 'NetworkTopologyStrategy', 
                    'DC-West': 1};
```

With `NetworkTopologyStrategy`, a replication factor is specified for each datacenter separately. 
In the above example, the `DC-West` datacenter will have a single copy of data. 
Not replicating data to `DC-East` could be a valid use case but usually there will be replicas in each datacenter. 


Create a keyspace with name `production_keyspace_2` that uses `NetworkTopologyStrategy` 
and `1` replica in each datacenter:

<details>
  <summary>Solution</summary>

```
CREATE KEYSPACE production_keyspace_2
WITH replication = {'class': 'NetworkTopologyStrategy', 
                    'DC-West': 1,
                    'DC-East': 1};
```

</details>

[continue](command:katapod.loadPage?step6){.orange_bar}
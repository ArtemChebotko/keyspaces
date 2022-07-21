<div class="top">

# Cluster, datacenters, racks, nodes
### [◂](command:katapod.loadPage?step1){.steps} Step 2 of 7 [▸](command:katapod.loadPage?step3){.steps}
</div>

Use `nodetool` to gather information about the cluster:

```
docker exec -i -t Cassandra-1 bash -c 'nodetool status'
```

Take a note of the datacenter names and how many nodes are in each datacenter. 
Since the cluster has only two nodes, we can have at most two replicas. 
In a real-life production cluster, you can usually expect to have 3 or more nodes per datacenter and replication factors of 3 or higher.

[continue](command:katapod.loadPage?step3){.orange_bar}
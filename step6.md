<div class="top">

# How many replicas do you need?
### [◂](command:katapod.loadPage?step5){.steps} Step 6 of 7 [▸](command:katapod.loadPage?step7){.steps}
</div>

Having `3` replicas per datacenter is a good starting point for 
relatively small clusters. As the number of nodes in a datacenter becomes larger, 
a higher replication factor may become a better choice.

The number of replicas can affect consistency, availability, latency and throughput.
Increasing a replication factor improves availability as it becomes possible to tolerate 
more replica failures. Also, a larger set of replicas can serve more concurrent requests 
and result in better response times. 

[continue](command:katapod.loadPage?step7){.orange_bar}
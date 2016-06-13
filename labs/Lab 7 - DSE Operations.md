Getting Started with DSE Ops
Most of us love to have tools to monitor and automate database operations. For Cassandra, that tool is DataStax OpsCenter. If you prefer to roll with the command line, then two core utilities you'll need to understand are nodetool and dsetool.

Utilities you'll want to know:

-	nodetool  //Cassandra's main utility tool
-	dsetool   //DSE's main utility tool

nodetool Examples:

Shows current status of the cluster:

$ nodetool status

shows thread pool status - critical for ops:

$ nodetool tpstats

dsetool Examples:

Shows current status of cluster, including DSE features:

$ dsetool status

Will create a Solr schema on Cassandra data for Search:

$ dsetool create_core

The main log you'll be taking a look at for troubleshooting outside of OpsCenter:

/var/log/cassandra/system.log

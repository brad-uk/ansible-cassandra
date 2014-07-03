ansible-cassandra
=================

Deploy a cluster of cassandra nodes to Digital Ocean.

Currently requires a private key located at ~/.ssh/ocean-test-id_rsa.pub. This will be added to your DO account and used to initialise access to each node via SSH.

Also, the envirnment vars DO_API_KEY & DO_CLIENT_ID must be set to allow the ansible tasks to talk to the DO API.

On successful execution you'll be left with four Cassandra nodes:

cass-am - Amsterdam
cass-ny - New York
cass-sf - San Francisco
cass-sg - Singapore

Each othe the nodes is added to the hosts file locally. Each node is also added to the hosts file on each node.

The cassandra replication factor is set to four so that data makes it to every node.


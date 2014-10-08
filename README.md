ansible-cassandra
=================

Deploy a cluster of cassandra 2.1.0 nodes to Digital Ocean.

Creates a new SSH key which is uploaded to DO for use in creating the droplets. Droplets are Debian 7.0 x64, size 1gb. The 512Mb size would get killed due to OOM.

Requires the envirnment vars DO_API_KEY & DO_CLIENT_ID be set to allow the ansible tasks to talk to the DO API (currently v1).

On successful execution you'll be left with four Cassandra nodes:

* cass-am - Amsterdam
* cass-ny - New York
* cass-sf - San Francisco
* cass-sg - Singapore

Each of the the nodes is added to the hosts file locally. Each node is also added to the hosts file on each node.

To run the playbook: ansible-playbook -K -i ansible_hosts digital-ocean-playbook.yml


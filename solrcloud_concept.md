#SolrCloud Concept

##Config

* solr.xml - specifies configuration options for your Solr core
* solrconfig.xml - controls high-level behavior.


##Use Core

* All action names are uppercase.


##Solr Container
* tomcat
* jetty

##Term
* node - is Java Virtual Machine, and can contain both instance of Solr and data.
* core - an index of the field and text in documents
* collection - the name of the collection to which this core belongs. Default is the name of the core.
* cluster - A cluster is set of Solr nodes managed by ZooKeeper as a single unit.
* shard - split the index to some seperate part.

從實體上來看: cluster > node > core

從概念上來看: collection > shard

###Core
* When you start a new core in SolrCloud mode, it registers itself with **ZooKeeper**.
* New Solr cores may also be created and associated with a collection via CoreAdmin.

###Cluster
* A cluster is created as soon as you have more than one Solr instance registered with **ZooKeeper**.

###Leaders and Replicas
<http://docs.lucidworks.com/display/solr/Nodes%2C+Cores%2C+Clusters+and+Leaders>

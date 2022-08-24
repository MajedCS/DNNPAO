# DNN Poisoning Attacks Ontology (DNNPAO)

DNNPAO is an ontological knowledge base of poisoning attacks on deep neural networks that has 55 poisoning attacks in DNNs. These attacks were identified and classified based on a systematic review. This ontological knowledge base is part of the our paper "An Ontological Knowledge Base of Poisoning Attacks on Deep Neural Networks"
https://www.preprints.org/manuscript/202208.0197/v1.

# Usage
DNNPAO can be used on different software suge as Protégé or Neo4j.
You can have a quick look by clicking on the link below.   
https://service.tib.eu/webvowl/#iri=https://raw.githubusercontent.com/MajedCS/DNNPAO/main/Ontology/AttacksOntologyTurtle.ttl

# Protégé 
Simply download and open the AttacksOntologyOwl.owl or AttacksOntologyTurtle.ttl using Protégé. https://protege.stanford.edu/ 

# Neo4j 
Requirements
1- Install Neo4j graph database.
2- Install the neosemantics (n10s) plugin.

Cypher:
1- Create uniqueness constraint:
CREATE CONSTRAINT n10s_unique_uri ON (r:Resource)
ASSERT r.uri IS UNIQUE;
2- Setting the configuration of the graph:
CALL n10s.graphconfig.init();
3- Import the DNNPAO file:
online : 
CALL n10s.onto.import.fetch("https://raw.githubusercontent.com/MajedCS/DNNPAO/main/Ontology/AttacksOntologyTurtle.ttl","Turtle");
or you can download the .ttl file and fetch it locally:
CALL n10s.onto.import.fetch("file:///file path/AttacksOntologyTurtle.ttl","Turtle");
For more details please visit : https://neo4j.com/labs/neosemantics/4.0/config/







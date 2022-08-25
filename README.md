# DNN Poisoning Attacks Ontology (DNNPAO)

DNNPAO is an ontological knowledge base of poisoning attacks on deep neural networks that has 55 poisoning attacks in DNNs. These attacks were identified and classified based on a systematic review.\
This ontological knowledge base is part of the our paper "An Ontological Knowledge Base of Poisoning Attacks on Deep Neural Networks"\
https://www.preprints.org/manuscript/202208.0197/v1.

## Poisoning Attacks Taxonomy
![Our extracted a taxonomy](/img/F6.svg)


# Usage
DNNPAO can be used on different software suge as Protégé or Neo4j.\
You can have a quick look by clicking on the link below.\   
https://service.tib.eu/webvowl/#iri=https://raw.githubusercontent.com/MajedCS/DNNPAO/main/Ontology/AttacksOntologyTurtle.ttl

# Protégé 
Simply download and open the AttacksOntologyOwl.owl or AttacksOntologyTurtle.ttl using Protégé.[1] \
https://protege.stanford.edu/ 

# Neo4j 
## Requirements
 Install Neo4j graph database. [2] \
 Install the neosemantics (n10s) plugin. [3] 

## Cypher:
### Create uniqueness constraint:
CREATE CONSTRAINT n10s_unique_uri ON (r:Resource)
ASSERT r.uri IS UNIQUE; 
### Setting the configuration of the graph:
CALL n10s.graphconfig.init();
### Import the DNNPAO file:
**online :** \
CALL n10s.onto.import.fetch("https://raw.githubusercontent.com/MajedCS/DNNPAO/main/Ontology/AttacksOntologyTurtle.ttl","Turtle"); \
**or you can download the .ttl file and fetch it locally:** \
CALL n10s.onto.import.fetch("file:///file path/AttacksOntologyTurtle.ttl","Turtle"); 
### For more details please visit : https://neo4j.com/labs/neosemantics/4.0/config/

## SemSpect
For more exploration tool on Neo4j you can use SemSpect tool.[4] \
https://www.semspect.de/

## References
[1] Musen, M.A. The protégé project: a look back and a look forward. AI Matters 2015, 1, 4–12. https://doi.org/10.1145/2757001.27
57003. \
[2] Neo4j - Graph Data Platform. https://neo4j.com/, accessed on 14.05.2021. \
[3] Jesús Barrasa. Neosemantics - a plugin that enables the use of RDF in Neo4j. https://github.com/neo4j-labs/neosemantics,
accessed on 15.03.2022. \
[4] SemSpect - Scalable Graph Exploration Tool for Neo4j. https://www.semspect.de/, accessed on 20.07.2022.


## How to cite: 
Altoub, M.; AlQurashi, F.; Yigitcanlar, T.; Corchado, J.; Mehmood, R. An Ontological Knowledge Base of Poisoning Attacks on Deep Neural Networks. Preprints 2022, 2022080197 (doi: 10.20944/preprints202208.0197.v1).







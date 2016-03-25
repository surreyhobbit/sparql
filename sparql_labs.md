## SPARQL labs

We've got two lab SPARQL engines running.

### 1. ARQ (Apache Jena Framework)

This is recommended by the book "Learning SPARQL". The framework runs on Java and is contained in its own folder in the home directory. The path to /bin/ is included in the $PATH variable, and a new environment variable called **JENA_HOME** pointing to its home directory.

The syntax to run a SPARQL query __\<qy\>__ on a data file __\<tty\>__ (in Turtle RDF format) is

`` arq --data <tty> --query <qy> ``

### 2. Blazegraph

Blazegraph is the graph DB engine / RDF triple store that is used by Cambridge Semantics 'ANZO' platform to store triples. It is extremely performant.

It runs on Java and has a web interface to manage namespaces, insert data, and run SPARQL 1.1 queries.

To start run the following from the command line:

`` $ java -server -Xmx4g -jar blazegraph.jar ``

The web interface can then be called opening link [http://localhost:9999/blazegraph/](http://localhost:9999/blazegraph/)

WHen finished, to power down find the PID for the java process using

`` $ jps ``

and then kill the process

`` $ kill <pid>``

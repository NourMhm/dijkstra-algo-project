Finding shortest path in a network using Dijkstra
=========
## Introduction
Consider a data communication network that must route data packets (email, MP3 ﬁles, or video ﬁles, for example). Such a network consists of routers connected by physical cables or links. A router can act as a source, a destination, or a forwarder of data packets. We can model a network as a graph with each router corresponding to a vertex and the link or physical connection between two routers corresponding to a pair of directed edges between the vertices. 

A network that follows the OSPF (Open Shortest Path First) protocol routes packets using Dijkstra’s shortest path algorithm. The criteria used to compute the weight corresponding to a link can include the time taken for data transmission, reliability of the link, transmission cost, and available bandwidth. Typically each router has a complete representation of the network graph and associated information available to it. 

For the purposes of this project, each link has associated with it the transmission time taken for data to get from the vertex at one end to the vertex at the other end. You will compute the best path using the criterion of minimizing the total time taken for data to reach the destination. The shortest time path minimizes the sum of the transmission times of the links along the path. 

The network topology can change dynamically based on the state of the links and the routers. For example, a link may go down when the corresponding cable is cut, and a vertex may go down when the corresponding router crashes. In addition to these transient changes, changes to a network occur when a link is added or removed.


## Compiling & Executing the Java code: 

Compile the java code with the following command: 
```sh
$ javac graph.java 
```

Execute the program with the following code: 
```sh
$ java graph network.txt 
```
I have successfully compiled the code and executed in the following environment: 
    OS: Windows 8.1  Compiler: javac 1.8.0_40  

##Program Design & Breakdown of File: 
There is only one Java file named “graph.java” which does all the five tasks as required by the project. 
I have implemented Dijkstra’s algorithm using MinHeap class which calculates the shortest distance between any two vertices of the graph. Also I have implemented the Reachable Vertices algorithm without using the shortest path algorithm from the program. I have developed a recursive algorithm which calculates the reachable vertices in the graph in O(nlogn) time. 
I have Used the following Classes in the program: 

* Graph - Class which reads the file which is passed to it and stores the graph and performs all the operations on the graph.
* GraphException - Handles any RuntimeException thrown by the Graph. 
* Vertex - Class which handles all the information related to the vertex. 
* Edge - Class which stores the information related to the Egde. 
* Path - Class which stores the name of a Path. 
* Pair – Class which stores the String Pairs. 
* Minheap – Class which implements the minheap for the Dijkstra’s Algorithm.  

#Compiler Used: 
The complier that I have used to compile the java program is “GCJ, the GNU compiler for java” and “javac” compiler. 

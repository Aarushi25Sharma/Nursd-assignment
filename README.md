# Nursd-assignment

You are given a DAG - directed acyclic graph - which may be disjointed (this represents courses in a university that must be taken in a particular order, but may represent different streams).

Identify all nodes with 0 in-degree.
For each such node, generate all possible paths that originate from that node

e.g., in the following graph assume that all edges point downward

     0 6      4
    /\ /
   1  2
  /\ /
 3  5

you should generate the following paths
0->1->3
0->1->5 
0->2->5
6->2->5
4

For extra credit, here is a data file that describes the above graph where 
the first line is the total number of nodes 
every subsequent line represents an edge between the first and second node
7 
0, 1
0, 2
1, 3
1, 5
2, 5
6, 2


This question can be done by using the DFS approach in the graph. Firstly, we will make the adjacency list and then traverse the nodes one by one and mark them as visited. We can also bracktrack if we didnt find the destination node. By traversing the nodes we can add the nodes traverse in the list and can print the possilble paths.

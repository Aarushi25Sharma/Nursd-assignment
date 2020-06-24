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

## Explaination
In this question our first task is to find the zero degree nodes. For this we will take a bool list and will store all the value of u and mark then as false. In that list at the places og y we can mark them true. Here, we will come to know that all the false marked nodes are Zero degree. We will pass these all the false marked nodes through DFS by making the adjacency list. We will take the false marked nodes as the source and the leaf node as the destination. Traverse all the nodes using DFS and after reaching the destination can print the path. Similarly, by this we can print all the possible paths from zero in degree nodes.

java c
COMP9312 - 24T2 - Data Analytics for Graphs 
Exam Sample Questions 
Q1 

Consider the above graph and answer the following questions. Please show necessary intermediate steps.
1.1 Calculate the density of the graph.
1.2 Please use the Compressed Sparse Row (CSR) to represent the above graph.
1.3 Commonly used data structures for graph stroage include adjacency matrix, adjacency list and CSR. Assume that we are dealing with a static graph and we aim to run the Pagerank algorithm for the graph. Which data stucture is the best to represent a graph in the above case? What scenarios the other two data structures are more suitable in, repsectively? Justify your answer
Q2 
Consider the above directed acyclic graph G and answer the following questions. Please show necessary intermediate steps.
3.1 Present the transitive closure for the given DAG.
3.2 Given the tree cover T, construct the corresponding compression scheme (do not merge adjacent intervals). Report the number of intervals used in the final compression scheme.
3.3 Show the result of the total-order-based 2-hop cover of the graph. Note that you should show your node order.
Q3 

Consider the above graphs and answer the following questions. Please show necessary intermediate steps.
3.1 Does this graph G1 contains 4-core? If your answer is "yes", please find the 4-core in this graph. If your answer is "no", please explain why.
3.2 Does this graph G1 contains 5-truss? If your answer is "yes", please find all edges in 5-truss in this graph. If your answer is "no", please exaplain why.
3.3 The graph G2 is a subgraph from a large-scale graph. Node v1 has 5 neighbors, and we know their core numbers, which are shown in the figure. Please calculate the core number of node v1.
Q4 
Consider the above graph and answer the following questions. The PageRank formulation is given as above where A is a given page, is the page that points to page A, d is the damping factor and is set as 0.85 in this question, C(T) is the number of links going out of T, N is the number of pages in the graph, PR(A) is the PageRank value of page A (initialized as 1/N for each page).
4.1 Please compute the PageRank value of page D of the above graph after one iteration.
4.2 Assume that we aim to implement pagerank algorithm using Pregel in distributed environment. We have three machines X, Y, and Z. We know that nodes A and B are located in X. Nodes C and D are located in Y. Nodes E, F, and G are located in Z. We run the PageRank algorithm in one iteration. How many messages are generated if the combiner is used? How many messages are generated if the combiner is not used? Justify your answer.
Q5 

Consider the graph G6. The node embeddings for all nodes are stacked in H. We use the Dice-Similarity which is defined as follows to measure the similarity between two vectors .
5.1 Based on the above similarity function, which node has the highest similarity with node C. Which node has the lowest similarity with node C. Justify your answer.
5.2 Complete the table below. Use the symbol "T" the to indicate that the node embedding method uses the corresponding information to learn the node embedding. Otherwise, input the symbol "F".
5.3 Which algorithm has a better performance in an inductive learning manner, GraphSAGE or GCN? Give an explanation about your choice.
Q6 
6.1 Which of the following technique is adopted by GraphSAGE but not adopted by GCN? (only one correct choice)
a. Aggregation of messages from neighbor nodes.
b. Adopting multiple GNN layers to be more expressive.
c. Sampling a subset of neighbor nodes for each node to reduce computation.
d. Need activation function to add nonlinearity.
6.2 Please determine whether the following statements about the benefits of attention mechanism use代 写COMP9312 - 24T2 - Data Analytics for Graphs
代做程序编程语言d in graph neural networks are TRUE or FALSE.
a. The computation of attentional coefficients can be parallelized across all edges of the graph.
b. It allows different importance values of different neighbors for each node and the mean of importance values for each node retain the same.
c. It has fixed number of parameters, irrespective of graph size.
d. It does not depend on the global graph structure so that has inductive capability.
6.3 Please determine whether the following statements about Graph Attention Network are TRUE or FALSE.
a. It adopts the DeepWalk model to assign an attention value for each node.
b. It can be used for the node classification task.
c. It does not sample neighbor nodes for each node but aggregate all the neighborhood messages.
d. It is flexible to adopt multi-head attention.
6.4 Give the matrix formulation of GCN as below, why do we multiply and ? Why do we multiply and ? Give a short explanation.
Q7 
Consider the GAT model on the above undirected graph with 9 nodes. Please compute the output of the first graph convolutional layer (i.e., ) step by step base on the following formula:
where indicates the -dimensional embedding of node v in layer l, and . is the weighting factor of node u's message to node v. denotes the weight matrix for the neighbors of v in layer l, denotes the dimension of the node embedding in layer l, denotes the neighbor set of the node v, denotes the self-looping weight matrix in layer l, denotes the ReLU non-linear function. The initial embeddings for all nodes are stacked in . is the weight matrices of layer 0.

Q8

Consider the above graph and answer the following questions. Please show necessary intermediate steps.
8.1 Please determine whether the following statements are TRUE or FALSE, and justify your answer.
a. In any correct DFS traversal starting from a, c must be traversed after b.
b. In some correct BFS traversal starting from c, a can be traversed before e.
c. In some correct DFS traversal starting from d, a can be traversed before e.
d. In any correct BFS traversal starting from b, e must be traversed after d.
8.2 Given the following pseudo-code of the prim's algorithm to compute the minimum spinning tree of an undirected weighted connected graph. Please analyze its time complexity, and present how to improve its time complexity (show how to revise the pseudo-code).
function MST-Prim(G(V,E)):
Input: An undirected weighted graph G
Output: Edges in the MST T
T = an empty list;
for each node v:
d[v] = ∞, p[v] = NULL, visited[v] = false;
pick an arbitrary node u, d[u] = 0, visited[u] = true;
add (d[u],u) to a priority queue Q;
While Q is not empty:
v = pop the node with the smallest d[] value from Q;
if visited[v]: continue;
visited[v] = true;
if p[v] != NULL:
add the pair (v,p[v]) to T;
for each neighbor u of v:
if !visited[u]  weight(u,v) < d[u]:
d[u] = weight(u,v);
add (d[u],u) to Q;
p[u] = v;
return T;
Q9 
9.1 A cycle is a simple path in which the terminals are the same. For instance of the graph in Q9, {1,2,4,3,1} is a cycle. Assume that we have an undirected graph G(V,E) and a sequence of new edges inserted to G. For each new edge e, please design an algorithm to test if there exists a cycle containing e in the graph. Note that you are expected to preprocess the graph and maintain some index (data structure) to check cycles efficiently.
9.2 A clique is a complete graph in which every pair of nodes are connected. Given an integer k, a k-clique is a clique with k nodes. Given an undirected graph G(V,E) and an integer k, please write the pseudo-code to enumerate all k-cliques in G, and analyze the time complexity of your algorithm.











         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com

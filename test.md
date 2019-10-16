# Subgraphs

In this section, we begin by introducing subgraphs as motivation. Subnetworks, or subgraphs, are the building blocks of networks which enable us to characterize and discriminate networks.

For example, Figure 1 shows all non-isomorphoic directed subgraphs of size 3. These subgraphs differ from each other in the number of edges or direction of edges. We say two graphs are non-isomorphoic *TODO*

# Motifs

Network motifs are recurring, significant patterns of interconnections in the network. Here, "pattern" means it is small induced subgraph,  "recurring" represents it occurs with high frequency, while "significant" means it is more frequent than expected. Motifs can help us understand how networks are composed together and also allow us to predict operation and reaction of the network in a given situation.

Subgraphs that occur in a real network much more often than in a random network have functional significance. 


## Z-score measure statistical significance of motifs. 

Network significance profile (SP) is defined as $SP_i = Z_i / sqrt_{sum_j Z_j}$. SP is a vector of normalized Z-scores

Configuration model is a random graph with a given degree sequence $k_1$, $k_2$, ..., $k_N$ which can be used as a "null" model. 
<br> Figures about generation


## Graphlets are connected non-isomorphic subgraphs.

<br> Graphlet Degree Vector (GDV) is a vector with the frequency of the node in each orbit position, it counts the number of graphlets that a node touches. GDV provides a measure  of a node's local network topology. 

## Finding Motifs and Graphlets

Finding size-k motifs/graphlets requires us: 1) enumerate all size-k connected subgraphs, and 2) count the number of occurrences of each subgraph type. There are different algorithms Exact subgraph enumeration (ESU), Kavosh and Subgraph sampling.

# ESU Algorithm

1) $V_subgraph$ contains nodes in currently constrcuted subgraph, and $V_extension$ is a set of candidate nodes to extend the motif. 
2) The basic idea of ESU is firstly, starting with a node v, then adding nodes u to $V_extension$ set while u's node id is larger than that of v, and u may only be neighbored to some newly added node w but nor of any node already in $V_subgraph$. 

# **Structural Roles in Networks**

Roles are functions of nodes in a network that can be measured by structural behaviors. <br> Note roles are different from groups/communities. Roles are based on the similarity of ties between subsets of nodes, nodes with the same role have similar structural properties, but they don't need to be in direct or even indirect interaction with each other. Group/community is formed based on adjacency, proximity or reachability, nodes in the same community are well-connected to each other.<br>
Structural equivalence: We say nodes u and v are structurally quivalent if they have the same relationships to each other. Structurally equivalent nodes are likely to be similar in many different ways.
Examples here.

# Structural roles discovery methods
<br>Roles allow us to identify different properties of nodes in network. The method we discuss here is RolX, an automatic discovery of nodes' structural roles. It's an unsupervised learning approach without prior knowledge. 
<br> The basic idea of recursive feature extraction is to aggregate features of a node and use them to generate new recursive features. By this way we can turn network connectivity into structural features. 
<br>The base set of a node's neighborhood features include:
1. Local features, which are all measures of the node degree. 
2. Egonet features, which are computed on the node's egonet and may include the number of within-egonet edges, and the number of edges entering/leaving egonet.
<br>We start with the base set of node features, use the set of current node features to generate additional features. There are two types of aggregate functions: mean and sum.

Egonet includes the node, its neighbors and any edges in the induced subgraph on these nodes


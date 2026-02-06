# `networkX` Cheat Sheet for MTH 325

[Click here for the full documentation for networkX.](https://networkx.org/documentation/stable/reference/index.html) 

| To do: | Enter: | 
| --- | ---- | 
| Load `networkx` and `matplotlib` | `import networkx as nx` <br> `import matplotlib.pyplot as plt` | 
| Create an empty graph | `G = nx.Graph()` | 
| Add an edge to G between nodes 2 and 3 | `G.add_edge(2,3)` | 
| Add several edges to G all at once | `G.add_edges_from([(1,3), (2,4), (2,3)])` | 
| Print a list of the edges in G | `for e in G.edges(): print(e)` | 
| Print a list of the nodes in G | `for v in G.nodes(): print(v)` | 
| Create the graph `F` from an edge list | `friend_list = [("Alice", "Bob"), ("Alice", "Darla"), ("Chuck", "Bob"), ("Bob", "Darla")]` <br> `F = nx.Graph(friend_list)`
` |  
| Create the graph `F` from a dictionary | `friends_dict = {"Alice":["Bob", "Darla"], "Bob":["Alice", "Chuck", "Darla"], "Chuck":["Bob"], "Darla":["Alice", "Bob"] }` <br> `F = nx.Graph(friends_dict)` | 
| Create a basic visualization of `G` | `nx.draw(G)` | 
| Draw `G` with the vertices labelled | `nx.draw(G, with_labels = True)` | 
| Draw `G` with the vertices labelled and colored yellow | `nx.draw(G, with_labels = True, node_color = "yellow")` | 
| Draw `G` in a circular layout | `nx.draw_circular(G)` | 
| Draw a random graph with 12 vertices and a 50% probability of connection | `G = nx.gnp_random_graph(12,0.5)` <br> `nx.draw(G)` | 
| Draw a random graph with 12 vertices and 15 edges | `G = nx.gnm_random_graph(12,15)` <br> `nx.draw(G)` | 
| Convert `G` to an edge list | `nx.to_edgelist(G)` | 
| Convert `G` to a dictionary | `nx.to_dict_of_lists(G)` | 
| Find the number of vertices in `G` | `G.number_of_nodes()` | 
| Find the degrees of each vertex in `G`  | `nx.degree(G)` Returns a dictionary of nodes and degrees. |
| Find the degree of vertex `a` in `G` | `d = nx.degree(G)` <br> `d["a"]` | 
| Find all the neighbors of vertex `a` | `neighbors = G.neighbors("a")` <br> `for n in neighbors: print(n)` | 
| Find the number of edges in `G` | `G.number_of_edges()` | 
| Create $K_8$, the complete graph on 8 vertices | `G = nx.complete_graph(8)` | 
| Create $K_{5,3}$, the complete bipartite graph | `G = nx.complete_bipartite_graph(5,3)` | 
| Create the cycle graph $C_9$ | `G = nx.cycle_graph(9)` | 
| Create the path graph $P_5$ | `G = nx.path_graph(5)` | 
| Convert a graph to a dictionary | `nx.to_dict_of_lists(G)` | 
| Convert a graph to an edge list | `list(G.edges())` |
| Convert a graph to an adjacency matrix, method 1 | `nx.to_numpy_array(G)` -- Creates a `numpy` array of floats. Addinng `.tolist()` to the end converts this to a list of lists.| 
| Convert a graph to an adjacency matrix, method 2 | `nx.to_pandas_adjacency(G)` -- Creates a dataframe using the `pandas` data science library. | 



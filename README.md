I used Claude (an AI assistant) to guide me through the method and to help debug my code. The main things it helped with were the generalized modularity matrix for recursive splitting, the ΔQ stopping check, the matrix form of Q, and fixing errors such as a missing import and graph edge weights. I ran the code, checked the results, and wrote the discussion myself.

What the notebook does
      
      Builds the unweighted adjacency matrix A, the degree vector k, the edge count m = 78, and the modularity matrix B = A − kkᵀ / 2m.
      
      Splits a group using the leading eigenvector of its generalized modularity matrix, assigning nodes by sign.
      
      Repeats on each resulting community until no community can be split.
      
      Prints, for each iteration, the communities, their sizes, λ₁, status, and Q.
      
      Plots the graph after each split with one color per community.
      
      Computes degree centrality, betweenness centrality, closeness centrality, and clustering coefficient for each node at each iteration, and plots how they evolve.
      
      Discusses which nodes stay central and how community structure influences the metrics.

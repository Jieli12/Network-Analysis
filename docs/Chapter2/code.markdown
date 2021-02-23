---
layout: default
title: Code
parent: Chapter 2
nav_order: 2
---

## Load data

The ca-GRQC data comes from [here](http://networkrepository.com/ca-GrQc.php#), using mmread funtion to load data.

```python
from scipy.io import mmread
a = mmread('./data/ca-GrQc.mtx')
```

Note that, the .mtx file has a head line staring with %% or %. a is an object of scipy.sparse.coo_matrix.

```python
a.shape
```

    (4158, 4158)

We can directly convert scipy.sparse.coo_matrix to Graph object for networkx using nx.Graph(). G.number_of_nodes() shows the number of vetices, G.number_of_edges() shows the number of edges.

```python
import networkx as nx
G=nx.Graph(a)
G.number_of_edges()
G.number_of_nodes()
```

    4158

The default node starts from 0, one can use relabel_nodes() to change the node labels. Below is the usage of relabel_nodes(), note that the mapping function.

```python
mapping = dict(zip(G, range(1, G.number_of_nodes()+1)))
G = nx.relabel_nodes(G, mapping)
sorted(G)[:3]
```

    [1, 2, 3]

Clearly, the node starts from 1.

```python
nx.is_weighted(G)
nx.is_directed(G)
```

    False

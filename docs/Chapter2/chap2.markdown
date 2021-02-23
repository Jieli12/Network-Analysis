---
layout: default
front_matter_title: Preliminaries
parent: Chapter 2
nav_order: 2
---

# Preliminaries

## Background on Graphs

### Basic Definitions and Concepts

#### Basic Definitions

* **Graph:** $G=(V,E)$ where $V$ is a set of **vertices** (nodes) and $E$ is a
  set of **Edges** (links), the pairs $\{u,v\},u,v\in V$ are unordered.
* $N_{v}= \vert V \vert$ is the number of vertices or **order**, $N_{e}=\vert E\vert$ is the number of edges or **size**.
* **Loops:** both one single edge's ends connect to a single vertex.
* **Multi-edges:** a pair of vertices has more than one edge between them.
* **Multi-graph:** a graph with either loops or multi-edge.
* **Subgraph:** $G^{\prime}=(V^{\prime}, E^{\prime})$ where $V^{\prime}\subseteq
  V$ and $E^{\prime}\subseteq E$.
* **Directed graph or digraph:** each edge in $E$ has an ordering to its
  vertices. Such edges are called **directed edges** or **arcs**
* **Direction of an arc:** for arc $\{u,v\}$, the direction of arc is
    $u\rightarrow v$, read from left to right or from tail $u$ to head $v$.

#### Connectivity

* **Adjacent(vertices):** Two vertices $u,v \in V$ are said to be adjacent if joined by an edge in $E$.
* **Adjacent(edges):** Two edges $e_1,e_2\in E$ are adjacent if joined by a common endpoint in $V$.
* **Incident:** A vertex $v \in V$ is **incident** on an edge $e \in E$ if $v$ is an endpoint of $e$.
* **Degree of a vertex $v$:** the number of edges incident on $v$, denoted as $d_v$.
* **Degree sequence** of a graph $G$: arranging the vertex degrees $d_v$ in
  non-decreasing order. Note that the **Degree sequence** is twice the **size**
  of the graph.
* **Degree** (digraph): for digraph, vertex degree is replaced by in-degree (i.e., $d_v^{in}$) and out-degree (i.e., $d_v^{out}$).
* **Reachable**: A vertex v in a graph G is said to be reachable from another vertex u if there exists a walk from u to v.
* **Connected**: The graph G is said to be connected if every vertex is reachable from every other.
* **Component**: A component of a graph is a maximally connected subgraph. That is, it is a connected subgraph of G for which the addition of any other remaining vertex in V would ruin the property of connectivity.
* **Weakly connected**(digraph): A digraph G is weakly connected if its underlying graph (i.e., the result of stripping away the labels ‘tail’ and ‘head’ from G) is connected.
* **Strongly connected**(digraph): It is called strongly connected if every vertex v is reachable from every u by a directed walk.

#### Movement

* **Walk:** a walk on a graph $G$, from $v_0$ to $v_l$, is an alternating
  sequence $\{v_0,e_1,v_1,e_2,\ldots,v_{l-1},e_l,v_l\}$, where the endpoints of
  $e_i$ are $\{v_{i-1},v_i\}$. Note that walks can have repeated edges.
* **Length of walk:** $l$ is the length of this walk, i.e., equivalent to  the number of edges passed in that walk.
* **trails:** walks without repeated edges.
* **paths:** trails without repeated vertices.
* **circuit:** the beginning and ending vertices of a trail are the same.
* **cycle:** a walk of length at least three, for which the beginning and ending vertices are the same, but for which all other vertices are distinct from each other.
* **acyclic:** Graphs containing no cycles are called acyclic.
for more vivid explanations, see [here](http://mathonline.wikidot.com/walks-trails-paths-cycles-and-circuits)
  
#### Distance 
* **distance (geodesic distance)**: defined as the length of the shortest path(s) between the vertices (which we set equal to infinity if no such path exists). ‘geodesic’ being another name for shortest paths.
* **diameter** The value of the longest distance in a graph is called the diameter of the graph.
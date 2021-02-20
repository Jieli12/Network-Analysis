---
layout: post
front_matter_title:  "Preliminaries"
date:   2021-02-19 18:00:21 +0000
permalink: /Chapter2/
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

#### Movement

* **Walk:** a walk on a graph $G$, from $v_0$ to $v_l$, is an alternating
  sequence $\{v_0,e_1,v_1,e_2,\ldots,v_{l-1},e_l,v_l\}$, where the endpoints of
  $e_i$ are $\{v_{i-1},v_i\}$.
* **Length of walk:** $l$ is the length of this walk, i.e., equivalent to the
  number of edges in this walk.

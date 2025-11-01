# 🧮 Design and Analysis of Algorithms – Lab Assignment 3  
### 📚 Graph Algorithms in Real-Life Applications  

---

## 🏁 Overview

This repository contains the implementation and analysis of **four real-world problems** using core graph algorithms.  
Each problem models a real application of graphs — from social networks to navigation, disaster response, and network design.

The implementation is done in **Python (Jupyter Notebooks)** with:
- `networkx` and `matplotlib` for visualization  
- `time` and `memory_profiler` for performance profiling  
- Well-commented code, outputs, and complexity analysis  

---

## 🔍 Problem Summaries

| **Problem** | **Graph Algorithm** | **Time Complexity** | **Application Domain** | **Description / Goal** |
|:-------------|:--------------------|:-------------------:|:-----------------------|:------------------------|
| 🧑‍🤝‍🧑 **Social Network Friend Suggestion** | BFS / DFS | O(V + E) | Social Media | Suggest new friends based on mutual connections |
| 🗺️ **Route Finding on Maps** | Bellman-Ford | O(V × E) | Navigation Systems | Find shortest path even with negative edges |
| 🚑 **Emergency Response Path Planning** | Dijkstra’s Algorithm | O(E log V) | Disaster Management | Identify fastest route for emergency vehicles |
| 🏗️ **Network Cable Installation** | MST (Prim’s / Kruskal’s) | O(E log V) | Infrastructure / Telecom | Connect all nodes with minimum total cable cost |

---

## 📘 Problem Details and Reports

| **Notebook** | **Analysis Report** | **Description** |
|:--------------|:--------------------|:----------------|
| [Problem 1 – Social Network](./notebooks/problem1_social_network.ipynb) | [Analysis](./analysis/problem1_analysis.md) | Uses BFS to suggest friends of friends |
| [Problem 2 – Route Finding](./notebooks/problem2_bellman_ford.ipynb) | [Analysis](./analysis/problem2_analysis.md) | Uses Bellman-Ford for shortest path with negative weights |
| [Problem 3 – Emergency Response](./notebooks/problem3_dijkstra.ipynb) | [Analysis](./analysis/problem3_analysis.md) | Uses Dijkstra’s algorithm for fastest route |
| [Problem 4 – Network Cable Installation](./notebooks/problem4_mst.ipynb) | [Analysis](./analysis/problem4_analysis.md) | Uses MST (Prim/Kruskal) for cost-efficient connections |

---

## 📊 Experimental Profiling

Each notebook includes:
- Execution time measurement using `time` module.  
- (Optional) Memory profiling using `memory_profiler`.  
- Graph visualizations generated via **NetworkX**.  

| Metric | Method Used | Observation |
|:--------|:-------------|:-------------|
| ⏱️ Execution Time | `time.time()` | All algorithms run efficiently for test-size graphs |
| 🧠 Memory Usage | `memory_profiler` | Low memory footprint due to adjacency list representation |

---

## 💡 Key Learnings

- Real-world problems can be **efficiently modeled as graphs**.  
- Algorithm choice depends on **edge weights, direction, and graph density**.  
- Visualization helps in **interpreting algorithm behavior and performance**.  
- Profiling confirms that theoretical complexities align with practical results.

---

## 🧠 Reflection

> Understanding the connection between abstract graph algorithms and real-world systems (like social media, navigation, and telecom) enhances problem-solving intuition.  
>  
> Each algorithm was implemented, visualized, and analyzed independently to highlight both **conceptual clarity** and **practical performance**.

---

## 🧰 Requirements

To run notebooks locally:
```bash
pip install networkx matplotlib memory-profiler

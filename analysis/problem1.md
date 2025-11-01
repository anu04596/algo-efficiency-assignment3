# 🧩 Problem 1 – Social Network Friend Suggestion

## 1️⃣ Real-World Context
Social networking platforms such as **Facebook**, **LinkedIn**, and **Instagram** use graph-based algorithms to suggest new friends or connections.  
Each user is represented as a **node**, and a friendship between two users is represented as an **undirected edge**.  
The goal is to find **“friends of friends”** who are not already connected to the user and rank them by the number of mutual friends.

---

## 2️⃣ Graph Modeling
| Entity | Representation |
|:-------|:----------------|
| User | Node (Vertex) |
| Friendship | Undirected Edge |
| Data Structure | Adjacency List (efficient for traversal) |

Example graph edges:  
`A–B, A–C, B–D, B–E, C–F, E–F, D–G, F–H, H–I, G–I, J–K`

---

## 3️⃣ Algorithm Used – Breadth First Search (BFS)
BFS is used to explore the network level by level starting from the given user:

1. Start from the **source user**.  
2. Visit all direct friends (distance 1).  
3. Visit **friends of friends** (distance 2).  
4. Suggest those nodes that are at distance 2 and **not already connected**.  
5. Count the number of **mutual friends** for ranking.

---

## 4️⃣ Output Example
For the sample graph above:
Suggestions for A → [('D', 1), ('E', 1), ('F', 1)]
Suggestions for B → [('C', 1), ('F', 2)]


This means that user A could connect with D, E, or F (each having 1 mutual friend),  
and user B is strongly connected to F through 2 mutual friends.

---

## 5️⃣ Visualization
The graph visualization shows:
- Blue nodes = users  
- Edges = friendships  
- Two connected components:
  - A – I (main network)
  - J – K (isolated pair)

Users J and K will never appear in friend suggestions for A–I since they belong to a disconnected component.

---

## 6️⃣ Complexity Analysis
| Operation | Complexity | Explanation |
|:-----------|:-----------:|:------------|
| Build Graph | **O(V + E)** | Each vertex and edge stored once |
| BFS Traversal | **O(V + E)** | Each node and edge visited at most once |
| Memory Usage | **O(V + E)** | Adjacency list representation |

BFS scales linearly with graph size, making it suitable for large social networks.  
For massive networks (Facebook-scale), distributed graph processing systems (e.g., Apache Giraph, GraphX) are used.

---

## 7️⃣ Advantages and Limitations
**✅ Advantages**
- Simple and fast for local friend recommendations.  
- Works well on moderate-sized graphs.  
- Finds mutual friends intuitively.

**⚠️ Limitations**
- BFS is limited to second-degree connections.  
- Does not account for interest similarity or frequency of interaction.  
- Can be computationally heavy for very large graphs.

---

## 8️⃣ Conclusion
BFS based friend suggestion provides a practical and interpretable approach to recommend new connections.  
It captures the real-world principle that **people with many mutual friends are more likely to know each other**.  
This implementation demonstrates how graph theory bridges social relationships and computational algorithms.

---

**Time Complexity:** O(V + E)  
**Space Complexity:** O(V + E)  
**Algorithm Used:** Breadth First Search (BFS)  
**Application Domain:** Social Media – Friend Recommendation Systems


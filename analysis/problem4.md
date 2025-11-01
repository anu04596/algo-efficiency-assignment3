# 🏗️ Problem 4 – Network Cable Installation Using Minimum Spanning Tree (MST)

## 1️⃣ Real-World Context
In **telecom, IT infrastructure, and power distribution**, we often need to connect multiple offices or stations using the **minimum total cable length**.  
This is modeled as a **Minimum Spanning Tree (MST)** problem.

---

## 2️⃣ Graph Modeling
| Entity | Representation |
|:--------|:----------------|
| Office / Building | Node |
| Possible Cable Route | Edge with cost |
| Cost / Distance | Weight (positive) |
| Data Structure | Adjacency list (Prim) or Edge list (Kruskal) |

Example input:
A–B(1), A–C(3), B–C(1), B–D(4), C–D(1), C–E(6), D–E(5)

---

## 3️⃣ Algorithms – Prim’s and Kruskal’s
### **Prim’s Algorithm**
- Starts from any node and **grows the MST** by adding the smallest weight edge that connects to a new node.
- Uses a **min-heap** for efficiency.

### **Kruskal’s Algorithm**
- Sorts all edges by weight.
- Adds edges one by one, skipping those that form a cycle.
- Uses **Union-Find (Disjoint Set)** to detect cycles.

---

## 4️⃣ Output Example
- Prim MST Total Cost: 8.
- Prim MST Edges: [('A','B',1), ('B','C',1), ('C','D',1), ('D','E',5)]
- Kruskal MST Total Cost: 8
- Kruskal MST Edges: [('A','B',1), ('B','C',1), ('C','D',1), ('D','E',5)]
- Both algorithms give the same MST and total cost.

---

## 5️⃣ Visualization
- The **original graph** shows all possible cable connections.  
- The **MST** (highlighted in red) shows the minimum required links to connect all offices.

---

## 6️⃣ Complexity Analysis
| Algorithm | Time Complexity | Space | Notes |
|:-----------|:----------------:|:-------:|:------|
| Prim (binary heap) | **O(E log V)** | O(V + E) | Efficient for dense graphs |
| Kruskal | **O(E log E)** ≈ O(E log V) | O(E) | Better for sparse graphs |

---

## 7️⃣ Advantages & Limitations
**✅ Advantages**
- Finds globally optimal connections.  
- Reduces total infrastructure cost.  
- Applicable to power grids, telecom networks, and road design.

**⚠️ Limitations**
- Assumes all edges are known beforehand.  
- Doesn’t handle dynamic (changing) graphs efficiently.

---

## 8️⃣ Conclusion
MST algorithms like Prim’s and Kruskal’s are essential for **network design and optimization**, ensuring minimal connection cost while maintaining complete connectivity.  
They represent a practical application of graph optimization in real-world infrastructure planning.

---

**Time Complexity:** O(E log V)  
**Space Complexity:** O(V + E)  
**Algorithm Used:** Prim’s / Kruskal’s MST  
**Application Domain:** Telecom, Power, and Network Infrastructure

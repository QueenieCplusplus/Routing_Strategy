# Routing Strategy based on Routing Protocols
路由演算法及其策略

# Graphic of Architecture 架構示意圖

(mix of IGP & Static)




      Static ---------  Rs ------- point to point ------- R --------- Static
                      (OSPF)                            (RIP)




# Chooses Basis 決策基礎點

Typically when Routing Protocols are evaluated, it is on the basis of characterisics that somewhat from the overall design, such as 

1. Convergence Times

2. Protocol Overheads (=Capacity of Bandwidth)

3. CPU Utilization

4. Memory Utilization

5. Stability

6. Hierarchy (degrees of connectedness & sizes of network areas)

7. Redundancy (protection from service interruption, degree of service consitency)

# Choices of Strategies (Evaluation of Dynamic Routes) 動態路由協定之演算法

* BGP, Border Gateway Protocols-4 (EGP)

* RIP, Routing Information Protocol (IGP)

* OSPF, Open Shortest Path First Protocol (IGP)

# Static Routes Concept 靜態路由

While Routing Protocols are not needed, then use Static Routes. It is apply to tub area.

# Difference between Static & Dynamic Routes

Whie there is no alternative routes exist in the network (lan), and there is only one route out of an area, then Static Routes is recommended to apply under this circumstance.



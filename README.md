# Routing Strategy based on Routing Protocols
路由演算法及其策略

# The real network architecture seems like this

AS: Autonomous System

POTS: Plain Old Telephone Service

                       Internet
                          |
                         ISP
         ---------------------------------
        |                                 |
        |                                 |
        |               AS-1              |
        |    Building 1      Building 2   |
        |                                 |
        -----------------------------------
                           |
                           |
                          WAN
                       /   |   \   
                      /    |    \
                     /     |     \
          --------------------    \    
          |       /        |  |    \
          |     fw         |  |     \
               /  AS-2    fw  |    AS-3   
          | f1----POTS----f14 |            
          |                   |
          ---------------------


see AS-3 inside box below


           ------------------------
          |                        |   
          |                        |
         --R---      hosts         |
          |     \   /              |
          |      \ /               |
          |       R                |
          |       |                |
          |       FW               |
          |       |                |
          |       |                |
          |       R                |
          |      / \               |
          |     /   hosts          |
          |   hosts                |
          ------------------------ |
          
# Fuction Areas Design


     - FA-TPE --
    |           |                   ---------------------------------------------
    |    sw --- R                   |                                            |
    |           | \                 |               floor 8                      |
     ----------    \                |                 |                          |
                    \               |                 |                          |
                   --------         |                                            |
                   |  FA  |   ----  R -- gw --------- SW ----------- floor 14    |
                   --------         |                                            |
                      /             |                  |                         |
                     /              |                  |                         |
                    /               |                floor 7                     |
                   /                |                                            |
                  /                 |                                            |
            - FA-Taichung--          --------------------------------------------
           |       R       |
           |       |       |
           |       sw      |
           -----------------     


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

see =>
https://github.com/QueenieCplusplus/Static_Routing

# Difference between Static & Dynamic Routes

While there is no alternative routes exist in the network (lan), and there is only one route out of an area, then Static Routes is recommended to apply under this circumstance.

# BGP 

it allows peering betweens ASs (Admin Domain or Autonomous System), and able to develop rules on ASs, instead of network-by-network basis.

# RIP

https://github.com/QueenieCplusplus/RIP

# OSPF

https://github.com/QueenieCplusplus/OSPF

# PPP, Point to Point Protocol

(to do)






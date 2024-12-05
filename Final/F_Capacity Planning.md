![image](https://github.com/user-attachments/assets/5e17dd30-bb4e-45f6-8c10-e8c51cd8a343)

**Part 2. Network Scalability Analysis**

Recall the e-commerce website scenario we discussed earlier. Given the
expected surge in traffic, analyze the provided network topology
diagram. Identify potential bottlenecks and areas where scalability
might be a concern. Propose specific strategies to improve the
network\'s scalability and performance to ensure a seamless user
experience during the peak traffic period. Consider factors such as
increased user demand, new applications, and security threats.

![image](https://github.com/user-attachments/assets/d15b2f19-25af-40aa-9ba8-e9150f948255)

The network’s potential bottlenecks and scalability concerns center around the edge router, the firewall and the Layer 2 switches. The edge router could become a bottleneck if its throughput cannot handle increasing Internet traffic, especially as more devices are added. The firewall, which handles inter-VLAN routing and security, may struggle with higher traffic volumes or additional VLANs, limiting scalability. Lastly, the Layer 2 switches could face congestion due to limited port capacity or uplink bandwidth, making it difficult to accommodate more servers or traffic. To ensure scalability, the network should prioritize upgrading to higher-capacity devices, implementing redundant infrastructure, and increasing uplink speeds between switches and the firewall.


Proposed Network Design:

![image](https://github.com/user-attachments/assets/8c257aef-8a20-461a-a747-04b6e550300c)
Network Analysis

     Our design addresses potential bottlenecks by implementing load balancing and failover through two ISR routers ensuring that network traffic is evenly distributed and redundancy is maintained. The dual firewalls mitigate security risks by providing robust protection against external threats while managing traffic between internal and external networks. Capacity limitations are minimized by segregating traffic into VLANs, reducing congestion within critical network areas.
Scalability Planning

     The topology is highly scalable, with modular hardware choices such as multilayer switches and separate VLANs for specific functions. This allows for the seamless addition of new devices, VLANs, or services without major reconfiguration. While ensuring smooth operations, our design also highlights potential drawbacks, such as the need for ongoing maintenance of redundant links, but emphasizes the long-term benefits of scalability and reliability.
Evaluation of Solution

     The use of load balancing and failover between routers, inter-VLAN routing with multilayer switches, and traffic segmentation within VLANs are all comprehensive strategies for optimizing network performance. Hardware upgrades, such as additional routers or switches, and software configurations, like implementing QoS policies, can further enhance the network's capacity and efficiency. Redundant links and firewalls ensure operational continuity, even during hardware failure.
Proposed Design
     The topology provides a detailed and well-justified design. It includes the following:
•	Dual routers for load balancing and failover.
•	Dual ASA firewalls for robust security.
•	Four VLANs: VLAN 1 for DNS/DHCP, VLAN 2 for database/web servers, VLAN 3 for email servers and additional web servers, and VLAN 4 for testing servers.
•	Redundant connections between routers, switches, and firewalls to eliminate single points of failure. This design is visually represented in the network diagram and comes with a clear implementation strategy.
Evaluation and Justification
The design is cost-effective, balancing advanced features with practicality. While it incorporates high-performance hardware and redundancy, it avoids unnecessary complexity. The segmentation of network functions into VLANs improves traffic efficiency and security. The cost and complexity of maintaining redundant links and firewalls are justified by the significant reduction in downtime and enhanced reliability they provide. Overall, the proposed solution ensures optimal performance, security, and scalability for both current and future requirements.



  ----------------- ------------------ ------------------- ---------------------
  Criteria          Excellent \| 10pts Good \| 7pts        Needs Improvement \|
                                                           4pts

  **Network         Accurately         Identifies key      Identifies some basic
  Analysis**        identifies         network components  network components
                    potential          and some potential  but lacks a
                    bottlenecks,       bottlenecks.        comprehensive
                    security risks,                        analysis.
                    and capacity                           
                    limitations.                           

  **Scalability     Proposes multiple  Proposes some       Proposes limited
  Planning**        relevant solutions relevant            scalability
                    and provides       scalability         strategies.
                    detailed           strategies but      
                    explanations,      lacks detail.       
                    including                              
                    potential                              
                    drawbacks and                          
                    benefits.                              

  **Evaluation of   Proposes           Provides a basic    Does not evaluate the
  Solutions**       comprehensive      evaluation of the   proposed solutions or
                    scalability        proposed solutions, provides a
                    strategies,        but lacks depth.    superficial
                    including specific                     evaluation.
                    recommendations                        
                    for hardware                           
                    upgrades, software                     
                    configurations,                        
                    and network                            
                    optimizations.                         

  **Proposed        Provides a         Provides a basic    Does not provide a
  Design**          detailed and       design but lacks    clear and detailed
                    well-justified     specific details    design.
                    design, including  and justifications. 
                    network diagrams,                      
                    configuration                          
                    details, and                           
                    implementation                         
                    plans.                                 

  **Evaluation and  Provides a         Provides a basic    Does not evaluate the
  Justification**   thorough           evaluation of the   proposed solutions or
                    evaluation of the  proposed solutions, provides a
                    proposed           but lacks depth.    superficial
                    solutions,                             evaluation
                    considering                            
                    factors like cost,                     
                    complexity, and                        
                    potential impact.                      

  Score:                                                   /50
  ----------------- ------------------ ------------------- ---------------------

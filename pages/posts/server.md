---
title: Server module of uNet
date: 2023-06-29T16:00:00Z
lang: en
duration: 9min
description: Server module of uNet
---

# **Background:** 
The uNet server module is an integral component of Portena's innovative uNet firmware. Portena's approach to remote connections centers around a small, portable device that establishes seamless and cost-effective connections to users' instances. This approach distinguishes Portena from traditional remote connection hosts like PCs. The compact and portable design of Portena's device makes it ideal for users who are frequently on the move. To ensure high-quality performance and minimal latency, Portena has developed a specially tailored remote connection firmware called uNet. The server is based on my CoaaS (Compute as a service) model which are infrastructues dispersed globally in the edge way. These serverless models offer scalable balloon like instances that can dynamically expanded or contracted to meet demand, reducing costs and optimizing resource allocation. Each instance is equipped with a sophisticated plugin called DRATP (Dynamic Resource Allocation and Task Prioritization). DRATP is an efficiently tailored resource allocation model that optimizes resource allocation and pricing, leading to cost reductions of up to 80%. Currently, the uNet firmware is undergoing prototyping using an esp32 microcontroller and an instance procured from Alibaba Cloud. The uNet client module and server module work together harmoniously to establish and manage remote desktop connections, providing users with seamless access to their instances.
**uNet Client Module:**
  - Initiates secure connections using SSL/TLS encryption protocols.
  - Implements user authentication and access control mechanisms.
  - Designed for esp32 chip, optimized for resource usage.
  - Enables remote desktop interaction via monitor and input devices.
**uNet Server Module:**
  - Installed in instances and sends data to the esp32-based client module.

# **Technical Requirements:**
  - Adequate server hardware for effective remote desktop connections.
  - RFB protocol for efficient remote desktop data transmission.
  - SSL/TLS encryption protocols for secure data transfer.
  - User authentication and access control mechanisms.
  - Tools for session management and monitoring.
  - Customizable server settings.
  - Efficient data transmission protocols.
  - AI/ML algorithms for data compression and formatting..
  - Context-aware compression for optimized data transfer.
  - Predictive caching and adaptive error correction.
  - Dynamic bandwidth allocation for efficient transmission.

# **Working Principle:** 
The uNet Server Module manages remote desktop connections by authenticating users and establishing secure SSL/TLS encrypted connections. It transmits remote desktop data to the client module using the RFB protocol. The module incorporates user authentication, access control, session management tools, and customizable settings. Advanced technologies such as AI/ML algorithms, context-aware compression, predictive caching, adaptive error correction, and dynamic bandwidth allocation enhance data exchange and transmission efficiency.

# **Future Ideas:**
  - Integration with blockchain.

# **Challenges:**
  - Ensuring data security and integrity during transmission.
  - Optimizing server performance for concurrent connections.
  - Developing user-friendly session management tools.
  - Ensuring compatibility with various instances and configurations.
  - Incorporating advanced technologies seamlessly.
  - Ensuring efficient data exchange and transmission.
# **Roadmap:**
  - Phase 1: Development of the uNet Server Module with basic features such as remote desktop protocol, SSL/TLS encryption, user authentication, and access control mechanisms.
  - Phase 2: Integration of advanced technologies such as AI/ML algorithms, dynamic resource allocation and task prioritization (DRATP), context-aware compression, predictive caching, adaptive error correction, and dynamic bandwidth allocation into the server module.
  - Phase 3: Integration with IoT devices for remote control and monitoring, blockchain technology for secure and transparent data exchange, edge computing for faster and more efficient data processing, and machine learning algorithms for intelligent resource allocation and pricing.
  - Phase 4: Testing and optimization of the uNet Server Module for performance, security, and user-friendliness.
  - Phase 5: Launch of the uNet Server Module and ongoing maintenance and updates to ensure optimal performance and user satisfaction.

# **Current Update**
I am currently busy prototyping this. The goal is to create a cost-effective and efficient prototype by utilizing a virtual machine (VM) setup to emulate the uNet server module and establish a simulated long-distance route to a separate isolated part acting as the uNet client module. This update highlights the key aspects of the development, challenges encountered, and future steps.

# **Simulation Setup:**
The simulation is being implemented using a VM hosted on a high-performance server machine. The VM is configured to emulate the behavior of the uNet server module, incorporating key features such as user authentication, access control mechanisms, and session management tools. The VM also utilizes the RFB protocol for efficient remote desktop data transmission and implements SSL/TLS encryption protocols for secure data transfer.

To emulate the long-distance route, network configurations within the VM and the isolated part acting as the uNet client module have been adjusted to simulate the effects of network latency and packet loss. By manipulating network settings and introducing specific delays and losses, we aim to mimic the conditions that would be encountered in a real-world long-distance network connection.

# **Progress and Challenges:**
Significant progress has been made in developing the simulation. The uNet server module, running within the VM, successfully establishes secure SSL/TLS encrypted connections and transmits remote desktop data to the simulated client module. The RFB protocol ensures efficient transmission of screen updates and user input, allowing for a near-real-time remote desktop interaction experience.

Challenges encountered during the development process include accurately replicating the latency and packet loss characteristics of a long-distance network connection. Fine-tuning network configurations and introducing controlled delays and losses have proven to be complex tasks. Achieving a high level of fidelity in simulating the network conditions is essential to accurately evaluate the performance and responsiveness of the uNet remote desktop connection.

# **Future Steps:**

*After its development*, several key steps are planned to further enhance the simulation and validate the uNet remote desktop connection concept:

  - *Network Optimization*: Continual refinement of network configurations will be conducted to achieve a more accurate representation of long-distance network conditions. This includes adjusting latency, introducing jitter, and simulating various levels of packet loss.

  - *Performance Testing*: Rigorous performance testing will be carried out to assess the responsiveness and efficiency of the simulated uNet remote desktop connection. This testing will involve measuring latency, bandwidth utilization, and evaluating the overall user experience.

  - *Scalability Evaluation*: The simulation will be expanded to assess the system's ability to handle multiple concurrent connections and maintain optimal performance. Load testing will be performed to determine the scalability limits of the prototype.

  - *Security Assessment:* A comprehensive security assessment will be conducted to identify potential vulnerabilities and ensure robust protection mechanisms are in place. This assessment will encompass encryption protocols, authentication mechanisms, and access control measures.

# **Conclusion**:
The development of a simulation for the uNet remote desktop connection is progressing well, utilizing a virtual machine setup to emulate the uNet server module and establish a simulated long-distance route. By addressing challenges related to network replication and performance optimization, we aim to create a cost-effective and efficient prototype. The next steps involve further refinement of the simulation, performance testing, scalability evaluation, and comprehensive security assessment. This ongoing development brings us closer to realizing the vision of a seamless and user-centric remote desktop connection solution with uNet.

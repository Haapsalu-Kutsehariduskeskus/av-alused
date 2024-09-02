<div class="small-grey-box">
  <div class="small-heading">Module 4: Physical Layer</div>
  - <a href="https://www.youtube.com/watch?v=AHV54tqhZU0&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=6">Physical Layer</a>

  <div class="small-heading">Module 5: Number Systems</div>
  - <a href="https://www.youtube.com/watch?v=RdoxJsWzFKc&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=7">Number Systems</a>

  <div class="small-heading">Module 6: Data Link Layer</div>
  - <a href="https://www.youtube.com/watch?v=eK4s5TQm45c&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=8">Data Link Layer</a>
  
  <div class="small-heading">Module 7: Ethernet Switching</div>
  - <a href="https://www.youtube.com/watch?v=KWm7_vsfdE4&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=9">Ethernet Switching</a>

</div>

# Week 2: Understanding the OSI Model - Part 1 (Physical and Data Link Layers)

### Introduction to the OSI Model
The OSI Model (Open Systems Interconnection Model) is like a map for understanding how data travels across a network. It breaks down the process into seven layers, each with its own job. Think of it like a team where each player has a specific role to play.

In this session, we’ll focus on two layers:
1. **Physical Layer**
2. **Data Link Layer**

### 1. The Physical Layer: The Foundation of Networking

- **What Does the Physical Layer Do?**
  - This is the layer where all the physical stuff happens. It’s about the hardware—the cables, wires, and signals that carry data from one device to another.

  **Examples:** Cables, connectors, electrical voltages, physical network topologies.
  **Concepts relevant to this layer:** RS-232, RJ45, V.34, 100BASE-TX, SDH, DSL, 802.11.
  
  **Physical Layer Simplified:** In the simplest terms, this is the layer responsible for transmitting ones and zeros through cables using electrical signals (twisted pair) or light (fiber optic cables).

- **Understanding Transmission Media:**
  - **Transmission media** are the physical paths along which data travels. There are different types, each with its own strengths and weaknesses:
    - **Copper Cables:** These are like the roads for data in a wired network.
      - **Unshielded Twisted Pair (UTP) Cable:** The most common type of network cable, used in many homes and offices. It’s made of twisted pairs of wires to reduce interference from other signals.
    - **Fiber-Optic Cables:** These use light instead of electricity to carry data, allowing for super-fast and long-distance communication.
      - **Advantages:** Faster and more reliable than copper, but more expensive.
    - **Wireless Media:** This includes Wi-Fi and Bluetooth. It’s like sending data through the air without any physical cables.
      - **Advantages:** No need for cables; easier to move devices around.
      - **Challenges:** Can be affected by walls and other obstacles, leading to slower speeds or lost connections.

![Physical Layer](/lectures/images/physical_layer.png)

- **Understanding Binary and Hexadecimal:**
  - Computers speak in binary (1s and 0s). Every piece of data, from a text message to a YouTube video, is broken down into binary.
  - **Binary Example:** The number 2 in binary is written as `10`.
  - Sometimes, data is also represented in hexadecimal (a base-16 system), which is easier for humans to read than long binary strings.
  - **Hexadecimal Example:** The binary number `1010` is `A` in hexadecimal.

  ![Binary](/lectures/images/binary.png)

### 2. The Data Link Layer: Ensuring Data Gets Where It Needs to Go
- **Purpose of the Data Link Layer:**
  - This layer makes sure data moves smoothly from one device to another.  It handles the packaging of data into chunks called frames and checks for errors that might occur during transmission.

- **Network Topologies:**
  - A **topology** is like a map showing how different devices (like computers, printers, and servers) are connected in a network.
    - **Bus Topology:** All devices share a single communication line. It’s simple but can slow down if too many devices are connected.
    - **Star Topology:** All devices are connected to a central hub. If the hub fails, the whole network goes down.
    - **Ring Topology:** Devices are connected in a circle. Data travels in one direction, reducing the chance of collisions.
    - **Mesh Topology:** Every device is connected to every other device. It’s super reliable but requires lots of cables and connections.

![Topology](/lectures/images/topology.png)

- **Data Link Frame Structure:**
  - Data is broken down into **frames** before being sent across the network. A frame has three parts:
    - **Header:** Contains information like the MAC address (a unique identifier for each device).
    - **Payload:** The actual data being sent (like an email or a webpage).
    - **Trailer:** Contains error-checking information to ensure the data arrives correctly.

![Data Link Frame](/lectures/images/data_link.png)

- **Ethernet and MAC Addresses:**
  - **Ethernet** is the most common technology used in wired networks. It defines how data is transmitted over cables.
  - **MAC Address:** Every device on a network has a unique identifier called a MAC address. It’s like a postal address, ensuring data gets to the right place.

 ![MAC Address](/lectures/images/mac.png)

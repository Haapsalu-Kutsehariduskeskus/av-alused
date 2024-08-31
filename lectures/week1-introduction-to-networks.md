# Introduction to Networks

## What is a Network?

Imagine you want to share a funny cat video with your friend who lives on the other side of the city. You could save the video on a USB drive, hop on your bike, and hand-deliver it. But that’s slow and inconvenient. Instead, you can send it over the internet instantly. The magic that makes this possible is a **network**.

A network is a group of two or more computers or devices connected together to share resources, like files, internet access, or even that cat video. Networks are everywhere—at home, in your school, and even at your local coffee shop.

### Why Are Networks Important?

Without networks, our world would be very different. No more emails, online games, social media, or streaming services. Networks make it possible for devices to talk to each other, whether they're in the same room or across the globe.

![Simple Network Diagram](./Images/simple_network_diagram.png)

### Types of Networks

Networks come in different shapes and sizes. Here are the main types:

- **Local Area Network (LAN):** This is the most common type, connecting devices within a small area like a home, office, or school. Imagine all the computers in your school lab being connected so they can share files and printers—that’s a LAN.
  
- **Wide Area Network (WAN):** A WAN is like a giant spider web stretching across cities, countries, or even continents. The internet is the biggest WAN there is, connecting millions of networks around the world.

- **Metropolitan Area Network (MAN):** A MAN is bigger than a LAN but smaller than a WAN, usually covering a city or a large campus. Think of it as a super-sized LAN for an entire town.

- **Personal Area Network (PAN):** PANs are tiny networks, like the one between your smartphone and your Bluetooth earbuds. They cover a very small area, just a few meters.

- **Storage Area Network (SAN):** SANs are specialized networks that connect storage devices, like hard drives, to servers. They’re often used in data centers to handle large amounts of data.

![Network Types Comparison](./Images/network_types_comparison.png)

---

# Network Components

A network isn’t just a bunch of computers thrown together. It has different parts, each with a specific job to do.

## End Devices

These are the devices you use every day—PCs, laptops, smartphones, printers. They are the starting and ending points for data traveling across the network. When you send an email, your computer is the **end device** that starts the process, and your friend's phone is the end device that receives it.

![End Devices](./Images/end_devices.png)

## Intermediary Devices

These devices are like the traffic cops of a network. They make sure your data gets from point A to point B smoothly and securely. Some common intermediary devices include:

- **Routers:** These decide the best path for your data to travel across a network or the internet.
  
- **Switches:** They connect multiple devices within the same network, like all the computers in a LAN, and ensure that data goes where it’s supposed to.

- **Firewalls:** Firewalls are the security guards of the network, keeping unwanted traffic out and protecting your data from hackers.

![Intermediary Devices](./Images/intermediary_devices.png)

## Network Media

Network media is the road that data travels on. There are three main types:

- **Copper cables:** These are traditional cables, like Ethernet cables, that use electrical signals to transmit data.
  
- **Fiber optics:** Fiber optic cables use light to send data at incredibly high speeds, making them perfect for long-distance communication.

- **Wireless:** This is the invisible path your data takes when you use Wi-Fi. Instead of cables, data is sent through the air using radio waves.

![Network Media Types](./Images/network_media_types.png)

---

# Basic Network Protocols and Standards

## What Are Network Protocols?

Think of network protocols as the rules of the road for data. They define how data is packaged, sent, received, and understood. Without these rules, devices wouldn’t know how to communicate with each other.

## Essential Protocols You Should Know

- **TCP/IP:** This is the backbone of the internet. TCP (Transmission Control Protocol) ensures that data is sent reliably, while IP (Internet Protocol) handles the addressing and routing of data packets to make sure they reach the right destination.

- **Ethernet:** Ethernet is the standard protocol for wired networks. It makes sure data flows smoothly over cables, like those in a LAN.

![Protocol Flowchart](./Images/protocol_flowchart.gif)

## Standards Organizations

To ensure that networks and devices can communicate globally, we have standards organizations:

- **IEEE (Institute of Electrical and Electronics Engineers):** This group sets the standards for a lot of technologies, including Ethernet.

- **IETF (Internet Engineering Task Force):** The IETF develops and promotes voluntary internet standards, like TCP/IP, that keep the internet running smoothly.

---

# Cisco IOS Access

## What is Cisco IOS?

Cisco IOS is like the operating system for Cisco network devices, such as routers and switches. It’s the brain that controls how these devices work and how they manage network traffic.

## How Do You Access Cisco Devices?

There are a few ways to access and configure Cisco devices:

- **Console:** This is a direct connection to the device using a special cable. It’s like sitting at the keyboard of the router or switch.
  
- **SSH (Secure Shell):** SSH lets you access and configure devices remotely, securely over the network.

- **Telnet:** Telnet is also used for remote access, but it’s less secure than SSH because it sends data, including passwords, in plain text.

![Cisco IOS Access](./Images/cisco_ios_access.png)

---

# Basic Device Configuration

## Assigning IP Addresses

Every device on a network needs an IP address, which is like its home address. This address is what routers use to send data to the right device. You can assign IP addresses manually, or automatically using a service like DHCP (Dynamic Host Configuration Protocol).

## Configuring Hostnames and Passwords

Just like your computer has a name, so do network devices. Setting a hostname makes it easier to identify each device on the network. For security, you’ll also want to set passwords to prevent unauthorized access.

## Saving and Verifying Configurations

Once you’ve made changes to a device’s configuration, it’s important to save them. Otherwise, they’ll be lost when the device is restarted. Verifying configurations means checking that your settings are correct and that the device is working as expected.

![Device Configuration](./Images/device_configuration.png)

---

# Communication Protocols

## Why Are Protocols Important?

Protocols are the unsung heroes of network communication. They ensure that when one device sends data, another device can understand it. Without protocols, networks would be a mess of misunderstood messages.

## How Protocols Work

Protocols define the rules for data exchange. For example, TCP breaks data into packets, numbers them, and makes sure they’re reassembled in the correct order. If any packets go missing, TCP asks for them to be sent again, ensuring reliable communication.

![Protocol Data Flow](./Images/protocol_data_flow.gif)

---

# OSI and TCP/IP Models

## What is the OSI Model?

The OSI (Open Systems Interconnection) model is like a blueprint for understanding how different networking tasks should be handled. It divides network communication into seven layers, from the physical transmission of data to the application software that interacts with users.

- **Layer 1: Physical Layer**
- **Layer 2: Data Link Layer**
- **Layer 3: Network Layer**
- **Layer 4: Transport Layer**
- **Layer 5: Session Layer**
- **Layer 6: Presentation Layer**
- **Layer 7: Application Layer**

Each layer has a specific function, and together, they ensure data is transmitted, received, and understood correctly.

## The TCP/IP Model

The TCP/IP model is more practical and is used to explain how the internet works. It has four layers:

- **Network Interface (Link Layer)**
- **Internet Layer**
- **Transport Layer**
- **Application Layer**

The TCP/IP model focuses more on how data actually moves across the network, which is why it’s often used instead of the OSI model.

![OSI vs TCP/IP Models](./Images/osi_vs_tcpip_models.png)

---

# Protocols in Action

## Real-World Examples

- **HTTP:** When you type a web address into your browser, HTTP (Hypertext Transfer Protocol) is the protocol that requests the web page and brings it to your screen.

- **UDP:** If you’re streaming a video, UDP (User Datagram Protocol) might be in play. Unlike TCP, UDP doesn’t worry about resending lost packets, making it faster but less reliable. This is okay for streaming, where missing a frame or two isn’t a big deal.

![Protocols in Action](./Images/protocols_in_action.png)



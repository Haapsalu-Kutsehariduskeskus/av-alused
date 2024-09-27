# Final Project: Answer Key

## 1. Addressing Table (Completed)

| Device   | Interface | IP Address / Prefix       | Default Gateway   | IPv6 Address / Prefix      |
|----------|-----------|---------------------------|-------------------|----------------------------|
| R1       | G0/0      | 192.168.0.1 /25           | N/A               | 2001:db8:acad::1/64        |
| R1       | G0/1      | 192.168.0.129 /26         | N/A               | 2001:db8:acad:1::1/64      |
| R1       | G0/2      | 192.168.0.193 /27         | N/A               | 2001:db8:acad:2::1/64      |
| R1       | S0/0/1    | 172.16.1.2 /30            | N/A               | 2001:db8:2::1/64           |
| Central  | S0/0/0    | 209.165.200.226 /30       | N/A               | 2001:db8:1::1/64           |
| Central  | S0/0/1    | 172.16.1.1 /30            | N/A               | 2001:db8:2::2/64           |
| S1       | VLAN 1    | 192.168.0.3 /25           | 192.168.0.1       | N/A                        |
| S2       | VLAN 1    | 192.168.0.131 /26         | 192.168.0.129     | N/A                        |
| S3       | VLAN 1    | 192.168.0.195 /27         | 192.168.0.193     | N/A                        |
| Staff    | NIC       | 192.168.0.2 /25           | 192.168.0.1       | 2001:db8:acad::2/64        |
| Sales    | NIC       | 192.168.0.130 /26         | 192.168.0.129     | 2001:db8:acad:1::2/64      |
| IT       | NIC       | 192.168.0.194 /27         | 192.168.0.193     | 2001:db8:acad:2::2/64      |
| Web      | NIC       | 64.100.0.3 /29            | 64.100.0.1        | 2001:db8:cafe::3/64        |

## 2. Configuration Steps

### R1 Configuration

1. **Set Device Name and Disable DNS Lookup**

    ```
    Router> enable
    Router# configure terminal
    Router(config)# hostname R1
    Router(config)# no ip domain-lookup
    ```

2. **Set Privileged EXEC Mode Password**

    ```
    Router(config)# enable secret Ciscoenpa55
    ```

3. **Set Console Password**

    ```
    Router(config)# line console 0
    Router(config-line)# password Ciscoconpa55
    Router(config-line)# login
    ```

4. **Set Minimum Password Length**

    ```
    Router(config)# security passwords min-length 10
    ```

5. **Encrypt Plaintext Passwords**

    ```
    Router(config)# service password-encryption
    ```

6. **Set a Banner**

    ```
    Router(config)# banner motd $ Unauthorized access is prohibited $
    ```

7. **Configure GigabitEthernet Interfaces with IPv4 and IPv6**

    ```
    Router(config)# interface g0/0
    Router(config-if)# ip address 192.168.0.1 255.255.255.128
    Router(config-if)# ipv6 address 2001:db8:acad::1/64
    Router(config-if)# no shutdown
    Router(config-if)# exit

    Router(config)# interface g0/1
    Router(config-if)# ip address 192.168.0.129 255.255.255.192
    Router(config-if)# ipv6 address 2001:db8:acad:1::1/64
    Router(config-if)# no shutdown
    Router(config-if)# exit

    Router(config)# interface g0/2
    Router(config-if)# ip address 192.168.0.193 255.255.255.224
    Router(config-if)# ipv6 address 2001:db8:acad:2::1/64
    Router(config-if)# no shutdown
    Router(config-if)# exit
    ```

8. **Configure SSH**

    ```
    Router(config)# ip domain-name CCNA-lab.com
    Router(config)# crypto key generate rsa modulus 1024
    Router(config)# line vty 0 4
    Router(config-line)# transport input ssh
    Router(config-line)# login local
    Router(config)# username Admin1 privilege 15 secret Admin1pa55
    ```

9. **Set Inactivity Timeout**

    ```
    Router(config)# line console 0
    Router(config-line)# exec-timeout 5 0
    Router(config)# line vty 0 4
    Router(config-line)# exec-timeout 5 0
    ```

10. **Configure Login Block**

    ```
    Router(config)# login block-for 180 attempts 4 within 120
    ```

11. **Save Configuration**

    ```
    Router# write memory
    ```

### Switch Configuration (S1, S2, S3)

1. **Set Device Name**

    ```
    Switch> enable
    Switch# configure terminal
    Switch(config)# hostname S1   # Change S1 to S2 or S3 for other switches
    ```

2. **Configure SVI Interface and Default Gateway**

    ```
    Switch(config)# interface vlan 1
    Switch(config-if)# ip address 192.168.0.3 255.255.255.128

    # Configure VLAN interfaces: 
    # S1: 192.168.0.3/25 (255.255.255.128) 
    # S2: 192.168.0.131/26 (255.255.255.192) 
    # S3: 192.168.0.195/27 (255.255.255.224) 
    # 
    # Each IP address is assigned with a specific subnet mask to define the network size: 
    # /25 allows 126 hosts, /26 allows 62 hosts, and /27 allows 30 hosts.
    
    Switch(config-if)# no shutdown
    Switch(config)# ip default-gateway 192.168.0.1   # Change default gateway based on respective subnets
    ```

3. **Set Privileged EXEC Mode Password**

    ```
    Switch(config)# enable secret Ciscoenpa55
    ```

4. **Set Console Password**

    ```
    Switch(config)# line console 0
    Switch(config-line)# password Ciscoconpa55
    Switch(config-line)# login
    ```

5. **Set Inactivity Timeout**

    ```
    Switch(config)# line vty 0 4
    Switch(config-line)# exec-timeout 5 0
    ```

6. **Encrypt Plaintext Passwords**

    ```
    Switch(config)# service password-encryption
    ```

7. **Save Configuration**

    ```
    Switch# write memory
    ```

### PC Configuration (Staff, Sales, IT)

1. **Staff PC (NIC)**

    - IP Address: `192.168.0.2 /25`
    - Subnet Mask: `255.255.255.128`
    - Default Gateway: `192.168.0.1`
    - IPv6 Address: `2001:db8:acad::2/64`
    - IPv6 Gateway: `fe80::1`

2. **Sales PC (NIC)**

    - IP Address: `192.168.0.130 /26`
    - Subnet Mask: `255.255.255.192`
    - Default Gateway: `192.168.0.129`
    - IPv6 Address: `2001:db8:acad:1::2/64`
    - IPv6 Gateway: `fe80::1`

3. **IT PC (NIC)**

    - IP Address: `192.168.0.194 /27`
    - Subnet Mask: `255.255.255.224`
    - Default Gateway: `192.168.0.193`
    - IPv6 Address: `2001:db8:acad:2::2/64`
    - IPv6 Gateway: `fe80::1`


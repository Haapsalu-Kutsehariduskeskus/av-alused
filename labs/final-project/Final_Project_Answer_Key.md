
# Cisco Packet Tracer – Skills Integration Challenge: Full Lab Manual

## 1. Scenario

The router Central, ISP cluster, and the Web server are fully configured. Your task is to:

- Create a new IPv4 addressing scheme using the `192.168.0.0/24` network that accommodates four subnets:
  - Staff requires 100 hosts.
  - Sales requires 50 hosts.
  - IT requires 25 hosts.
  - Guest (to be added later) requires 25 hosts.
- Configure the R1 router's interfaces with IPv4 and IPv6 addressing according to your scheme.
- Finish the basic security settings and interface configurations on R1.
- Configure the SVI interface and basic security settings on switches S1, S2, and S3.

---

## 2. Addressing Scheme

Based on the host requirements, the IPv4 addressing scheme will be as follows:

- **Staff Subnet**: 100 hosts → `192.168.0.0/25` (Subnet Mask: 255.255.255.128)
- **Sales Subnet**: 50 hosts → `192.168.0.128/26` (Subnet Mask: 255.255.255.192)
- **IT Subnet**: 25 hosts → `192.168.0.192/27` (Subnet Mask: 255.255.255.224)
- **Guest Subnet** (future) → `192.168.0.224/27` (Subnet Mask: 255.255.255.224)

### Addressing Table:

| Device   | Interface | IP Address / Prefix       | Default Gateway   |
|----------|-----------|---------------------------|-------------------|
| R1       | G0/0      | 192.168.0.1 /25           | N/A               |
| R1       | G0/1      | 192.168.0.129 /26         | N/A               |
| R1       | G0/2      | 192.168.0.193 /27         | N/A               |
| S1       | VLAN 1    | 192.168.0.3 /25           | 192.168.0.1       |
| S2       | VLAN 1    | 192.168.0.131 /26         | 192.168.0.129     |
| S3       | VLAN 1    | 192.168.0.195 /27         | 192.168.0.193     |
| Staff PC | NIC       | 192.168.0.2 /25           | 192.168.0.1       |
| Sales PC | NIC       | 192.168.0.130 /26         | 192.168.0.129     |
| IT PC    | NIC       | 192.168.0.194 /27         | 192.168.0.193     |

---

## 3. Router R1 Configuration

### 3.1 Set Device Name and Disable DNS Lookup:

```bash
Router> enable
Router# configure terminal
Router(config)# hostname R1
Router(config)# no ip domain-lookup
```

### 3.2 Set Privileged EXEC Mode Password:

```bash
Router(config)# enable secret Ciscoenpa55
```

### 3.3 Set Console Password:

```bash
Router(config)# line console 0
Router(config-line)# password Ciscoconpa55
Router(config-line)# login
```

### 3.4 Set Minimum Password Length:

```bash
Router(config)# security passwords min-length 10
```

### 3.5 Encrypt Plaintext Passwords:

```bash
Router(config)# service password-encryption
```

### 3.6 Set a Banner:

```bash
Router(config)# banner motd $ Unauthorized access is prohibited $
```

### 3.7 Configure GigabitEthernet Interfaces:

```bash
Router(config)# interface g0/0
Router(config-if)# ip address 192.168.0.1 255.255.255.128
Router(config-if)# no shutdown
Router(config-if)# exit

Router(config)# interface g0/1
Router(config-if)# ip address 192.168.0.129 255.255.255.192
Router(config-if)# no shutdown
Router(config-if)# exit

Router(config)# interface g0/2
Router(config-if)# ip address 192.168.0.193 255.255.255.224
Router(config-if)# no shutdown
Router(config-if)# exit
```

### 3.8 Configure SSH:

```bash
Router(config)# ip domain-name CCNA-lab.com
Router(config)# crypto key generate rsa modulus 1024
Router(config)# line vty 0 4
Router(config-line)# transport input ssh
Router(config-line)# login local
Router(config)# username Admin1 privilege 15 secret Admin1pa55
```

### 3.9 Set Inactivity Timeout:

```bash
Router(config)# line console 0
Router(config-line)# exec-timeout 5 0
Router(config)# line vty 0 4
Router(config-line)# exec-timeout 5 0
```

### 3.10 Configure Login Block:

```bash
Router(config)# login block-for 180 attempts 4 within 120
```

## 4. Switch Configuration (S1, S2, S3)

### 4.1 S1 (Staff Network - VLAN 1):

```bash
Switch> enable
Switch# configure terminal
Switch(config)# interface vlan 1
Switch(config-if)# ip address 192.168.0.3 255.255.255.128
Switch(config-if)# no shutdown
Switch(config-if)# exit
Switch(config)# ip default-gateway 192.168.0.1
Switch# write memory
```

### 4.2 S2 (Sales Network - VLAN 1):

```bash
Switch> enable
Switch# configure terminal
Switch(config)# interface vlan 1
Switch(config-if)# ip address 192.168.0.131 255.255.255.192
Switch(config-if)# no shutdown
Switch(config-if)# exit
Switch(config)# ip default-gateway 192.168.0.129
Switch# write memory
```

### 4.3 S3 (IT Network - VLAN 1):

```bash
Switch> enable
Switch# configure terminal
Switch(config)# interface vlan 1
Switch(config-if)# ip address 192.168.0.195 255.255.255.224
Switch(config-if)# no shutdown
Switch(config-if)# exit
Switch(config)# ip default-gateway 192.168.0.193
Switch# write memory
```

## 5. PC Configuration

### 5.1 Staff PC:

- IP Address: 192.168.0.2 /25
- Subnet Mask: 255.255.255.128
- Default Gateway: 192.168.0.1

### 5.2 Sales PC:

- IP Address: 192.168.0.130 /26
- Subnet Mask: 255.255.255.192
- Default Gateway: 192.168.0.129

### 5.3 IT PC:

- IP Address: 192.168.0.194 /27
- Subnet Mask: 255.255.255.224
- Default Gateway: 192.168.0.193

## 6. Connectivity Test

- Use the web browser on Staff, Sales, and IT PCs to navigate to www.cisco.pka.
- Ensure all PCs can ping each other and the router's interfaces.

## 7. Additional Configuration

Configure security features like SSH access, banner messages, and password policies to meet the security requirements. Make sure the login block and timeout rules are applied to prevent unauthorized access.
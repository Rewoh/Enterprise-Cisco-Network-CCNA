# Enterprise IPv4 Addressing Plan

## Overview

The enterprise network uses private IPv4 addressing based on RFC 1918. Each department is assigned a dedicated subnet to provide logical separation, simplify administration, improve security, and support future growth.

The address block selected for the organization is:

10.10.0.0/16

Each VLAN receives its own /24 subnet, allowing up to 254 usable host addresses.

---

# Addressing Standards

Default Gateway:
First usable address (.1)

Infrastructure Devices:
Reserved addresses between .2 and .20

Servers:
Reserved addresses between .21 and .40

DHCP Pool:
Addresses beginning at .50

Static Devices:
Addresses between .2 and .49

Clients:
Allocated dynamically through DHCP.

---

# Benefits

- Easy to troubleshoot
- Predictable addressing
- Supports future expansion
- Consistent documentation
- Industry best practice

# VLAN Addressing Plan

| VLAN | Department | Network | Default Gateway |
|------|------------|---------------|----------------|
|10|Management|10.10.10.0/24|10.10.10.1|
|20|Administration|10.10.20.0/24|10.10.20.1|
|30|Finance|10.10.30.0/24|10.10.30.1|
|40|Human Resources|10.10.40.0/24|10.10.40.1|
|50|Sales|10.10.50.0/24|10.10.50.1|
|60|Customer Support|10.10.60.0/24|10.10.60.1|
|70|IT|10.10.70.0/24|10.10.70.1|
|80|Servers|10.10.80.0/24|10.10.80.1|
|90|Guest Wi-Fi|10.10.90.0/24|10.10.90.1|
|99|Native VLAN|10.10.99.0/24|10.10.99.1| 

# Reserved Infrastructure Addresses

| Device | Address |
|----------|---------------|
|EDGE-RTR|10.10.1.1|
|ISP-RTR|203.0.113.1|
|CORE-SW|10.10.99.2|
|ACC-SW1|10.10.99.11|
|ACC-SW2|10.10.99.12|
|ACC-SW3|10.10.99.13|
|SRV-01|10.10.80.10| 

# DHCP Scope

Each VLAN will receive addresses dynamically.

Reserved:

.1 Gateway

.2–.20 Infrastructure

.21–.40 Servers

.41–.49 Future Expansion

DHCP Pool:

.50–.254 

# Switch Management

All switches will be managed through VLAN 99.

Management IP Addresses:

CORE-SW
10.10.99.2

ACC-SW1
10.10.99.11

ACC-SW2
10.10.99.12

ACC-SW3
10.10.99.13

# Router Interfaces

EDGE-RTR

GigabitEthernet0/0
203.0.113.2/30

GigabitEthernet0/1
10.10.1.1/24

ISP-RTR

GigabitEthernet0/0
203.0.113.1/30

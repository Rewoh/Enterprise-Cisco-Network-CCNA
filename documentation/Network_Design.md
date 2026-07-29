# Network Design

## Network Type

The proposed solution is a hierarchical enterprise network designed according to Cisco's Three-Layer Hierarchical Network Model.

The network consists of:

- Core Layer
- Distribution Layer
- Access Layer

This architecture improves scalability, simplifies troubleshooting, enhances security, and supports future expansion.

The implementation follows Cisco CCNA best practices for enterprise campus networks. 

## Device Inventory

The network consists of:

| Device | Quantity | Purpose |
|---------|----------|---------|
| Cisco 2911 Router | 2 | Enterprise Router and ISP Router |
| Cisco 3560 Layer 3 Switch | 1 | Core Switch |
| Cisco 2960 Switch | 3 | Access Layer |
| Server | 1 | DHCP, DNS, HTTP, FTP |
| PCs | 24 | End Users |
| Printers | 4 | Shared Printing | 


## Cabling Plan

The implementation will use Copper Straight-Through cables for:

- PC to Switch
- Server to Switch
- Switch to Router
- Switch to Switch

Serial DCE/DTE cables will be used between routers where required.

Console cables will be used for initial device configuration. 


## Documentation Standards

All Cisco devices will have:

- Hostname configured
- Encrypted passwords
- Login banner
- SSH remote access
- Saved startup configuration
- Interface descriptions
- Configuration backups stored in GitHub

## Documentation Standards

All Cisco devices will have:

- Hostname configured
- Encrypted passwords
- Login banner
- SSH remote access
- Saved startup configuration
- Interface descriptions
- Configuration backups stored in GitHub

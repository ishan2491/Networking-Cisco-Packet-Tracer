# Cisco Network Lab Configuration

This project involves setting up a Cisco network infrastructure with VLANs, security measures, and trunking between switches. The configuration includes redundancy, routing, and network optimization using various Cisco technologies.

## Overview

The network setup includes:
- Hostname configuration for easy identification.
- Security enhancements by shutting down unused interfaces.
- Password protection for device management.
- Manual VLAN configuration using VTP in transparent mode.
- VLANs 10, 20, 30, and 100 for traffic segmentation.
- Trunk ports for inter-switch communication.
- Access ports assigned to specific VLANs.

## Configuration Tasks

### Initial Setup
1. **CDP and LLDP**: Used to verify link connectivity between devices.
2. **Spanning Tree Protocol (STP)**: Verified port states (forwarding/blocking).
3. **Spanning Tree Optimization**: Core1 is the root for odd VLANs; Core2 is the root for even VLANs.
4. **EtherChannel**: Configured on core switches for link aggregation.
5. **Layer 3 InterVLAN Routing**: Implemented on core switches with specific IP addresses for each VLAN.

### IP Addressing
- **Core Switches**:
  - VLAN 1: Core1 = 10.1.1.251/24, Core2 = 10.1.1.252/24
  - VLAN 10: Core1 = 10.1.10.251/24, Core2 = 10.1.10.252/24
  - VLAN 20: Core1 = 10.1.20.251/24, Core2 = 10.1.20.252/24
  - VLAN 30: Core1 = 10.1.30.251/24, Core2 = 10.1.30.252/24
  - VLAN 100: Core1 = 10.1.100.251/24, Core2 = 10.1.100.252/24

- **Access Layer Switches Management IPs**:
  - Switch1 = 10.1.1.1/24
  - Switch2 = 10.1.1.2/24
  - Switch3 = 10.1.1.3/24

### Advanced Configuration
1. **HSRP**: Configured and optimized for redundancy.
2. **EIGRP**: Set up on core switches and ISR router for routing.
3. **PCs and Server Configuration**:
   - PC1 in VLAN 10, IP = 10.1.10.10/24
   - PC2 in VLAN 20, IP = 10.1.20.10/24
   - PC3 in VLAN 30, IP = 10.1.30.10/24
   - Server1 in VLAN 100, IP = 10.1.100.100/24

4. **Connectivity Verification**:
   - Ensured PCs can ping each other and the server.
   - Verified connectivity between switches, server, and PCs.

5. **Router Configuration**:
   - Router IP g0/0/0 = 10.1.1.253/24
   - g0/0/1 configured for DHCP.

6. **NAT Configuration**:
   - Enabled NAT to translate internal network addresses to the ISR G0/0/1 interface using PAT.

## Usage

This setup provides a secure and organized network environment with effective traffic segmentation using VLANs and proper access control measures.

## License

This project is licensed under the MIT License.


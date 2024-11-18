In this Cisco lab configuration, I set up a basic network infrastructure with VLANs, security measures, and trunking between switches. 
The main tasks included:
    *1) Hostnames were configured on each switch for easy identification and management.
    *2) Unused interfaces were shut down to enhance security and prevent unauthorized access.
    *3) Passwords were set for privileged EXEC mode and remote access (via VTY lines) to secure device management.
    *4) VTP (VLAN Trunking Protocol) was configured in transparent mode with the domain name "ccna" to allow manual VLAN configuration without relying on VTP updates from other switches.
    *5) VLANs 10, 20, 30, and 100 were created to segment network traffic for different departments or purposes.
    *6) Trunk ports were configured between switches to allow multiple VLANs to communicate across the network.
    *7) Access ports were assigned to specific VLANs, ensuring that end devices (like PCs) are connected to the correct VLAN.
This setup creates a secure and organized network environment with traffic segmentation using VLANs and proper access control.

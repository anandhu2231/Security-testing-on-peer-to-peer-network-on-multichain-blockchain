# Security-testing-on-peer-to-peer-network-on-multichain-blockchain

This projects explores security testing on multichain blockchain systems, revealing that nodes with lower computing capacity are more vulnerable to network-level attacks.

Setup
A multichain blockchain network was set up using various devices. Node 1 was a laptop with an i3 processor running Bodhi Linux, while Nodes 2 and 4 were Raspberry Pi 4 and 3B+ running Ubuntu Unity. Node 3 was a laptop with a powerful i7 processor running Bodhi Linux and was patched. Git and curl were installed for remote administration. A new blockchain was created on Node 1, and the chain parameters and network settings were configured on all nodes. Nodes 2, 3, and 4 were added to the network, and their connections were verified. Permissions for critical operations were enabled to ensure secure network governance.

# Multichain Setup
## Nodes and Specifications
- Node 1: Laptop with i3 processor running Bodhi Linux
- Node 2: Raspberry Pi 4 running Ubuntu Unity
- Node 3: Laptop with i7 processor running Bodhi Linux (patched)
- Node 4: Raspberry Pi 3B+ running Ubuntu Unity

## Software
- Bodhi Linux
- Ubuntu Unity
- Git
- Curl
- Multichain


# Setup Instructions
* create a new blockchain : `multichain-util create chain1`
* start the chain : `multichaind chain1 -daemon`
* Configure Chain Parameter : `nano ~/.multichain/chain1/multichain.conf`
* Connect Additional Nodes (Nodes 2, 3, 4) : `multichaind chain1@<Node1_IP>:<port>`
* Verify Connections : `multichain-cli chain1 getinfo`
* Enable Permissions for Secure Network Governance : `multichain-cli chain1 grant <address> connect,send,receive`

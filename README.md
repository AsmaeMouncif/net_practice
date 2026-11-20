*This project has been created as part of the 42 curriculum by asmounci.*

# NetPractice

## Description

NetPractice is a hands-on introduction to computer networking. The goal is to repair 10 broken, simulated network diagrams by editing IP addresses, subnet masks, and routing tables (gateways) until every objective of each level is reached.

The networks are fictitious and run in a training interface opened in the web browser. Each level shows:

- a network diagram (hosts, switches, routers, and the Internet),
- one or more goals (for example "host A must communicate with host B"),
- editable fields (the unshaded ones) for interface IPs, masks, and routes,
- logs that explain why a packet does not reach its destination.

Skills practiced: choosing valid host addresses, computing network and broadcast addresses, sizing subnets, avoiding subnet overlaps, setting default gateways, and writing routing tables with forward and return paths.

## Instructions

### Run the training interface

1. Download the files attached to the project page and extract them in any folder.
2. In that folder, run:
   ```sh
   ./run.sh
   ```
   This starts a local web server and opens the interface in your browser.
3. If `run.sh` does not work, start the server manually and open it yourself:
   ```sh
   python3 -m http.server 49242
   ```
   Then go to `http://localhost:49242` (you may change the port).
4. In the **Training** tab, enter your intranet login and click **Start!**. The login is required because it generates your personal configuration.

### Solve and export a level

1. Edit the unshaded fields (IP, mask, routes) of the diagram.
2. Click **Check again** to verify the goals. Use the logs at the bottom of the page to understand failures.
3. When the level is solved, click **Get my config** to download the configuration file.
4. Click **Next level** and repeat until level 10.

Export the configuration of each level before moving to the next one.

### Submission requirements

- The repository must contain **10 exported configuration files (one per level)** placed at the **root** of the repository (`level1.json` to `level10.json`).
- Each file must be exported with the login entered in the interface.
- This `README.md` is also at the root of the repository.
- During the defense, three random levels must be solved in a limited time, without external tools (a simple calculator such as `bc` is tolerated).

## Resources

### Networking concepts studied

- **TCP/IP addressing**: IPv4 addresses, network address, broadcast address, usable host range.
- **Subnet masks and CIDR notation**: for example `255.255.255.128` = `/25`, block sizes, and subnet sizing.
- **Default gateways**: the router address a host uses to reach other networks.
- **Routing tables**: specific routes, default route (`0.0.0.0/0`), and return routes for replies.
- **Routers and switches**: a router connects different networks, a switch connects hosts inside the same network.
- **OSI layers**: layer 2 (switching) versus layer 3 (IP addressing and routing).

### References

- Decimal to binary and binary to decimal converters (used to convert address octets and masks): https://www.rapidtables.com/convert/number/decimal-to-binary.html
- Desmos scientific calculator (used for subnet calculations): https://www.desmos.com/scientific
- Video playlist on IP addressing and subnetting (used to learn the concepts): https://youtu.be/pNpTBSVCiVE

### Use of AI

AI was used only to help understand the networking concepts (subnet masks, CIDR notation, block sizes, default gateways, and routing). It was not used to solve the levels: every configuration was built and tested in the training interface.

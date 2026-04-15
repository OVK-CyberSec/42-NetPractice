*This project has been created as part of the 42 curriculum by <mohifdi>.*
 
# NetPractice
 
## Description
 
NetPractice is a practical networking exercise from the 42 curriculum. The goal is to configure small-scale simulated networks by filling in missing IP addresses, subnet masks, and routing rules so that all devices can communicate correctly.
 
Across 10 progressively challenging levels, you learn how packets travel through a network, how routers forward traffic between subnets, and how to troubleshoot misconfigured network diagrams using logs and routing tables.
 
---
 
## Instructions
 
### Running the training interface
 
1. Download the project archive from the 42 project page.
2. Extract it into a folder of your choice.
3. Inside that folder, run the launch script:
   ```bash
   ./run.sh
   ```
   This starts a local web server and opens the interface in your browser automatically.
4. If `run.sh` does not work, start the server manually and open it yourself:
   ```bash
   python3 -m http.server 49242
   # Then navigate to http://localhost:49242 in your browser
   ```
 
### Using the interface
 
- Enter your **42 intranet login** in the field on the welcome page before starting. This is required so that the configuration is generated for your login.
- Use the **Training** tab to practice at your own pace.
- Use the **Evaluation** tab to generate a random configuration (also valid for peer evaluations).
- For each level, modify the **unshaded fields** (IP addresses, masks, routes) until the network is correctly configured.
- Click **Check again** to verify your configuration.
- Click **Get my config** to download the configuration file for that level.
- Once a level is validated, click **Next level** to proceed.
> ⚠️ Always export your configuration with **Get my config** before moving to the next level.
 
### Submission
 
- Complete all **10 levels**.
- Export one configuration file per level using the **Get my config** button.
- Place all **10 exported files** at the **root of your Git repository**.
- Push your work to your repository as usual.
> ⚠️ It is critical that you enter your login in the interface before exporting — the files are tied to your login and will be checked during evaluation.
 
### Evaluation
 
During the defense, you will be asked to complete **3 random levels** within a limited time. No external tools are allowed, except a simple calculator (e.g., `bc`).
 
---
 
## Resources
 
### Networking concepts studied
 
- **TCP/IP addressing** — how IP addresses identify devices on a network
- **Subnet masks** — how to determine which part of an address is the network vs. the host
- **CIDR notation** — shorthand for expressing subnet masks (e.g., `/24`, `/28`)
- **Default gateway** — the router interface a device uses to reach destinations outside its subnet
- **Routing tables** — how routers decide where to forward packets
- **Static routes** — manually configured forwarding rules (e.g., `0.0.0.0/0 => <next-hop>`)
- **Routers and switches** — routers connect different networks; switches connect devices within the same network
- **OSI model layers** — understanding at which layer IP addressing and routing operate (Layer 3)
- **Point-to-point links** — `/30` subnets used for router-to-router connections
### References
 
- [Networking Basics](https://www.youtube.com/watch?v=s_Ntt6eTn94&list=PLCXqoZAc8-tzD5N5oCyIyEcMg_NDs6o7C)
- [Subnetting Practice — Subnet Calculator](https://www.subnet-calculator.com/)
- [TCP/IP Guide (online)](http://www.tcpipguide.com/free/index.htm)
- [RFC 791 — Internet Protocol](https://datatracker.ietf.org/doc/html/rfc791)
### AI usage
 
AI (Claude, Anthropic) was used during this project for the following tasks:
 
- **Explaining networking concepts** — understanding subnet masks, CIDR notation, and how routing tables work
- **Verifying IP address calculations** — confirming that addresses fall within the correct subnet range
- **Debugging misconfigured diagrams** — reasoning about why a packet would fail to reach its destination given a specific routing table
All AI-generated content was reviewed and verified before use. The actual level configurations were completed independently in the training interface.
 

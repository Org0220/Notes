# Network Risk Management
## Security Assessment
* Different types of organizations have different levels of network security risk
* `Posture assesment` which is a thorough examination of each aspect of the network to determine how it might be compromised.
* Should be preformed at least once a year
* `Security audit` An assesment preformed by a company 


## Security Risks
* `Vunereability`: weakness of a system, process, or architecture that could lead to compromised informaiton or unauthoriized access is known.
* `Exploit`: The act of taking advantage of a vulnerability
* `Zero-day`: is one that takes advantage of a software vunerability that hasn't yet become public and is known only to the hacker who discovered it


## Risks Associated with People
* Companies should be responsible for educating their employees on the risks of network security.
* Often, employees are the ones who cause most of the security breaches sustained by networks.
* `Socail engineering`  the intruder might pose as a technical support analyst who needs to know the password to troubleshoot a problem.
* `Phishing`: is a type of attack that uses a computer program to send an email to a user who is not the intended recipient.


## Risks Associated with Transmission and Hardware
* This risks affect the first 3 layers, the physical layer, the data link layer, and the network layer.
*  `Jamming`: is sending high volume of illegitimate traffic to a network to overwhelm it.
* `RF (radio frequency) emanation`: is the act of sending radio waves to a network.
* `RF emanation`: created by the leaking of signals from equipment
* `ARP poisoning`: is the act of sending a network packet to a device that is not the intended recipient

## Risks Associated with Protocols and Software
* This risks affect the higher layers of the OSI model such as the application layer, the session layer, and the presentation layer. and the transport layer.
* TCP/IP protocols are not secure. 
    * IP addresses can be falsified
    * Checksums can be thwarted
    * UDP requires no authentication
    * TCP requires only weak authentication
    * FTP is notorious for its vunlerabilities.
        * A host of a computer to specify a IP address and Port number for the data's destination.
        * So instead of specifying one of their ports, they specify an IP address of another device and send the information there
* Insecure protocols can provide hackers with insightful information about the devices and software used on a network.
    * `Banner-grabbing attacks`
        * Attackers send bogus requests for connection to servers or applications to harvest useful information to guide their attack.
        * For example, determining the name and version of a business's email software.
* `Session hijacking attack`
    * Attackers somehow get the encrytion key of the session
    * `Man-in-the-middle (MitM) attack`: Attackers redirects the user to the place they want to get useful information from them, perhaps a password or ID
* `Ping of death` and `Buffer overflow` makes the system crash by sending network traffic

## Risks Associated with Internet Access

* Browsers are not secure enough, some scritps from different may pass to the system because of the bugs in the browser.
* A firwall may bot provide adequate protection if iit is configured improperly. 
    * `IP spoofing` obtaining internal IP addressses by outsiders and use those addresses to pretend that they have authority to access your internal network from the Internet.
    * Correctly configuring a firewall is a critical step in protecting your network.
* User using Telnets or FTPs their information over Internet , their id and password is transmitted in plain text
    * Anyone monitoring the network can see the id and password.
* Hackers can obtain information inserted into a website. (e.g. passwords, emails, mailing lists, forms etc.)
* `DoS attacks` can be used to crash a system.
    * Send tones of network traffic to a system to crash it.
    * `Denial of service`: is the act of causing a system to crash by sending excessive amounts of network traffic.
    * `DDoS`: is the act of causing a system to crash by sending excessive amounts of network traffic.
    * `Zombies`: computers who send Ddos attacks to a system without the user knowing about it.
        * It uses the computer resources for that
        * This computers are part of botnet.
            * `Botnet`: is a group of computers that are connected to a network and are used to attack the network.
    * `DrDos (Distributed reflector DoS)`: is a type of DDoS attack that is distributed by using not infected computers.
        * It sends the attacks to different conputers that redirects these attacks to the target
        * The computers are called `reflectors` and they do not get infected by the attack.
    * `Permanent DoS attack`: An attack on a device (router) that attempts to alter the device's managment interface to the point where it is       irrecoverable.
    * `Unstable DoS attack`: Sometimes DoS situations are created unintentionally
        * Also called friendly attack. 
        * For example during the registration day, to many people tries to access omnivox and because of it, the webpage crashes.

## NOS Security
* Restricted user authorizatoin
    * Access to server files and directories
    * Public Rights
    * Group Users according to security level
    * Access to system resources

## Logon Restriction
* Admin can restrct access to users to files and directories on the server by constraining the ways in which users can access the server and its resources.
    * `Time of day:` For example a user can only access the server between 8:00 and 17:00
    * `Total time logged on:` For example a user can only access the server for a total of 10 hours
    * `IP address:` For example a user can only access the server from the IP address or network address of the server.
    * `Unsuccessful logons:` For example a user can only access the server if they have successfully logged on to the server before.

## Network Access Control
* With Network Access Control, devices that are connected to the network are visible and access can be managed through policy enforcement on devices and users of the network.

## ACL used by routers
* Router's function: 
    * Examin packets 
    * Determine destination
        * Using the network layer addressing information.
* `ACL(access control list)` is used by routers to control access to the network.
* ACL functioning process:
    * Checks the ACL permit,deny criterias
    * Drops packet if denied characteristics
    * Forwards packet if permited if criteria permited
    * If there is no permited criteria, the packet is dropped
* `access-list`: is a list of rules that determine whether a packet is allowed to pass through a network.
* More ACL statements router has, less powerfull it is.

## Inrusion Detection and Prevention
* Proactive security measure - Dectecting suspicious network activity 
* `IDS (instrusion detection system)`:  is a network security technology originally built for detecting vulnerability exploits against a target application or computer.
* `HIDS (host-based IDS)` runs on a signle computer to alert about attacks to that one host
* `NIDS (network-based IDS)` protects a network
* IDS drawback 
    * Number of false positives logged 
* IDS can only detect and log suspicious activity
* `IPS` (intrusion prevention system)
    * Detects tureat and prevents traffic from flowing to network
* `NIPS` (networkbase IPS): Protects the whole network
* `HIPS` (host-based intrusion prevention): Protects certain hosts
* `IDS vs IPS` IDS alerts about the attack and IPS stops the attack

## Firewalls
* is a specialized device (router) or computer installed with specializedd software
* Firewall locates between two interconnected private networks or betweeen private and public netwroks 
* `Packet-filtering firewall` simplest firewall 
    * Examines header of every entering packet (inbound traffic) 
    * Can block entering traffic or exiting LAN (outboud traffic)
* `Firewall default configuration`
    * Blocks most common security threats
    * Preconfigured accept and deny certain traffic types
    * Network administrators often customize settings
* Common packet-filtering firewall criteria
    * Source and destination IP addresses 
    * Source and destination ports 
* Port blocking 
    * Prevents connection to and tranmission completion
* `UTM (Unified Threaat Managment)`: Strategy that combines multiple layers of security appliances and technologies into a signle safety net
* `Next Generation Firewalls (NGFW)`
    * can monitor and limit traffic of specific applications 
    * Adapt to various applications, users and devices 
* `Proxy service `
    * Software application on a network host 
        * Acts as an intermediary between external and internal networks 
        * Screens all incoming and outgoing traffic
* `Proxy server (proxy)` 
    * Network host running proxy service
    * Security managment and application layer
* `Reverse proxy`: 
    * Screens all the incoming traffic from clients to the server. So it's a proxy for servers. 

## SIEM (Security Information and Event Management)
* Evaluates data logs from IDS, IPS, firewalls and proxy servers in order to detect significant events that require the attnetion of IT staff according to predefined rules. 

## Scanning Tools
* `NMAP (Network Mapper)`
    * Scanning large networks
    * Provides information about the network and hosts
    * Free
* `Nessus`
    * Preforms more sophisticated scans than `NMAP`

## Honeypots
* Decoy system that is purposefully vulnerable
* Designed to fool hackers and gain information about their behavior
* `Honeynet`: Network of `honeypots`
* Decoy systems called, lures, can provide unique information about hacking behavior

# Data Link Layer & Network Cabling

## Data link Layer
* `Framing`: Packets to Frames transformation
* `Addressing`: Addressing mechanism using mac address
* `Synchronization`: synchronization of two machines that are transmitting data
* `Error control`
* `Flow control`: Computers can have different speed an capacity so the flow control ensures to keep a stable speed for data exchange.
* `Multi-Access`: Multiple access to the network
## Data Modulation
* Network connection may handle only analog signals 

## Baseband and Broadband
* `Basedband transmission`: Digital signals that are carried on a signle channel 
* `Broadband transmission`: Digital signals that are carried on multiple channels
## Multiplexing
* `Multiplexing`: Is a form of transmission that allows multiple signals to be carried on a single channel
* `Subchannel`: Is a part of a multiplexed signal
* `Multiplexer`: Is a device that multiplexes signals onto multiple channels
* `Demultiplexer`: Is a device that separates the combined signals
* `TDM (Time Division Multiplexing)`: devides channel into multiple time intervals.
    * So it send the first packet. Receives it and then sends the second packet. 
    * For example phone calls are devided into a lot of small TDMs. So the first second of the conversation is sent. After the second one etc.
* `WDM (Wavelength Division Multiplexing)`: Fiber-optic connection using light signals simultaneously.
    * `DWDM (Dense Wavelength Division Multiplexing)`: Better for long distance
    * `CWDM (Coarse Wavelength Division Multiplexing)`: Better for short distance
## Throughput and Bandwidth
* `Throughput`: The number of bits that can be transmitted in a given time (seconds)
* `Bandwidth`: Difference between highest and lowest frequencies. Medium can be used to transmit data.
## Twisted-Pair Cable
* Consists of 8 cables united in 4 pairs. Each pair is twisted 
* `Twist Ratio`: Twists per meter or foot.
    * High twist ratio = Higher quality = more expensive etc
* TIA/EIA-568 (Twisted-pair)
* `CAT 5e` category or higher used in modern LANS.
    * Category 3, 5, 5e, 6, 6a, 7 
* `Advantages:`
    * not expensive
    * Flexible
    * Easy installation
    * Spans signifcant distance before requiring repeater

* `Shielded twisted-pair cable (STP)`
    * Indiviually insulated
    * Surrounded by metalic substance shielding (foil)
    * Better protected
* `Unshielded twisted-pair cable (UTP)`
    * Surrounded by plastic
    * Less protected
* `STP and UTP`
    * Throughput is the same
    * Vary in cost, so no cheeper one
    * Connector: uses Jack 45
    * Noise immunity: STP more resistant to noise
    * Size and scalability: Maximum length is 100 meters

## Cable Pinouts
* Proper cable termiation is requirement for two nodes on a network to communicate
* TIA/EIA specifies two methods of inserting wires into RJ-45 plugs
    * TIA/EIA 568A
    * TIA/EIA 568B
<img src = "https://cdn.discordapp.com/attachments/662367446568796179/971256921111818261/unknown.png">

* `Crossover Cable` uses 568A for one end of the cable and 568B for the other end
* `Rollover cable` Used to connect a computer to the console port of a router
## PoE (Power over Ethernet)
* `IEEE` 802.3af standard which specifies a method for supplying eletctrical power over twisted-pair Ethernet connections
## Fiber-Optic Cable
* Fiber-optic cable (fiber)
    * One or more glass or plastic fibers at its center (core)
* `+`
    * Extremly hight throughput
    * Very high noise resistance
    * Excelent security
    * Able to carry signals for longer distances
    * Industry standard for high-speed networking
* Drawbacks
    * More expensive
    * Requires special equipment to splice

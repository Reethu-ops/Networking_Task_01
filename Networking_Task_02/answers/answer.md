Networking Task 02: Network Devices & IP Addressing
Objective

The purpose of this task is to understand common network devices, IP addressing concepts, and how data travels within a network.

Part A: Network Devices Research
1. Router
Purpose

A router connects different networks and allows devices to access the Internet.

How It Works

It receives data packets and forwards them to the correct destination using IP addresses.

Real-World Usage

Home WiFi routers connect laptops, phones, and other devices to the Internet.

2. Switch
Purpose

A switch connects multiple devices within the same network.

How It Works

It uses MAC addresses to send data directly to the intended device.

Real-World Usage

Used in offices and schools to connect computers and printers.

3. Hub
Purpose

A hub connects multiple devices in a network.

How It Works

It broadcasts data to all connected devices regardless of the destination.

Real-World Usage

Older networks used hubs before switches became common.

4. Access Point
Purpose

An access point provides wireless connectivity to devices.

How It Works

It extends a wired network and allows devices to connect using WiFi.

Real-World Usage

Used in homes, offices, colleges, and public WiFi locations.

5. Firewall
Purpose

A firewall protects networks from unauthorized access and cyber threats.

How It Works

It monitors and filters incoming and outgoing network traffic based on security rules.

Real-World Usage

Used in computers, routers, and organizations to improve security.

6. Modem
Purpose

A modem connects a network to an Internet Service Provider (ISP).

How It Works

It converts signals between the ISP and local devices.

Real-World Usage

Used in homes and offices to establish Internet connectivity.

Part B: IP Address Classification
IP Address	Public/Private	Reason
192.168.1.10	Private	Falls within 192.168.0.0 – 192.168.255.255
10.0.0.5	Private	Falls within 10.0.0.0 – 10.255.255.255
172.16.5.20	Private	Falls within 172.16.0.0 – 172.31.255.255
8.8.8.8	Public	Public Google DNS server
1.1.1.1	Public	Public Cloudflare DNS server
192.168.100.1	Private	Falls within 192.168.0.0 – 192.168.255.255
Part C: Understanding Your Network
Network Information
Item	Value
IPv4 Address	10.86.13.106
Default Gateway	10.86.13.175
DNS Server	10.86.13.175
Which IP range does your device belong to?

My device belongs to the 10.0.0.0 – 10.255.255.255 private IP address range.

Is it Public or Private?

It is a Private IP Address because it belongs to the reserved private IP range.

What role does your router play in your network?

The router acts as a gateway between my local network and the Internet. It forwards data between my device and external networks.

What would happen if the DNS server stopped working?

Without DNS, websites could not be accessed using domain names such as google.com. Users would need to enter IP addresses directly.

Screenshots

(See Screenshots folder for ipconfig and nslookup outputs.)

Part D: Network Communication Flow
Diagram
Your Device
      ↓
Router
      ↓
DNS Server
      ↓
Google Server
      ↓
Response Back to Device
Explanation
Step 1: Your Device

The user enters www.google.com into a web browser. The device begins the process of locating the website.

Step 2: Router

The router receives the request and forwards it to the DNS server through the network.

Step 3: DNS Server

The DNS server translates the domain name google.com into an IP address.

Step 4: Google Server

The request reaches Google's server using the IP address provided by DNS.

Step 5: Response Back to Device

Google's server sends the webpage data back through the network to the user's device.

Part E: Practical Command Exercise
Command 1: ipconfig /all

Purpose:
Displays detailed network configuration information.

(See Screenshots folder.)

Command 2: nslookup google.com

Purpose:
Retrieves the IP address associated with a domain name.

Output:

DNS Server: 10.86.13.175
Google IPv4 Address: 142.250.70.78
Google IPv6 Address: 2404:6800:4007:833::200e

(See Screenshots folder.)

Command 3: ping google.com

Purpose:
Tests connectivity between the device and Google's server.

(See Screenshots folder.)

Answers
What IP address did DNS return for Google?

DNS returned the IP address 142.250.70.78 for google.com.

Was the ping successful?

Yes, the ping was successful.

Why is DNS important before communication begins?

DNS translates domain names into IP addresses. Without DNS, devices would not know where to send requests when a website name is entered.

Conclusion

This task helped me understand network devices, IP address classification, DNS functionality, and how data travels between devices and Internet services. I also gained practical experience using networking commands such as ipconfig, nslookup, and ping.
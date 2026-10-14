# Northbridge Savings & Finance – Network Security Upgrade

This repository contains my individual contribution as **Member 4** of a four-member Network Security project.

The project focused on identifying security risks in a banking environment and proposing practical security controls using secure remote access, centralized authentication, network segmentation, intrusion detection/prevention, and Cisco network hardening.

## My Contribution

As Member 4, I was responsible for:

### Threat Modelling

- T4 – Online Banking Portal Compromise
- T6 – Insider / Stolen Account Privilege Abuse

I analysed each threat using the following chain:

Asset → Vulnerability → Threat → Exploit → Attack → Impact → Risk

## Technology Recommendations

I proposed the following technologies:

- **OpenVPN Access Server** – secure remote access
- **FreeRADIUS** – centralized Authentication, Authorization and Accounting
- **OPNsense** – firewalling and network segmentation
- **Suricata IDS/IPS** – intrusion detection and prevention

## Cisco Packet Tracer Configuration 1 – Zone-Based Firewall

I implemented a Cisco Zone-Based Firewall to control traffic between trusted and untrusted network zones.

Main tasks included:

- Creating INSIDE and OUTSIDE security zones
- Assigning interfaces to security zones
- Creating class maps and policy maps
- Allowing inspected HTTP and HTTPS traffic
- Applying a default drop policy
- Verifying firewall behaviour

This configuration was mainly linked to **T4 – Online Banking Portal Compromise**.

## Cisco Packet Tracer Configuration 2 – PortFast and BPDU Guard

I implemented PortFast and BPDU Guard on a Cisco switch access port.

Main tasks included:

- Configuring the port as an access port
- Enabling PortFast
- Enabling BPDU Guard
- Connecting a test switch
- Verifying that the protected port entered an **err-disabled** state after receiving a BPDU

This demonstrates protection against unexpected or rogue switch connections.

## Proposed Security Architecture

My proposed architecture used:

- OpenVPN Access Server for remote access
- FreeRADIUS for AAA
- OPNsense for network segmentation and firewalling
- Suricata for IDS/IPS monitoring
- Separate zones for online banking, staff, branches, guest Wi-Fi, core banking, and third-party access

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS
- Zone-Based Firewall
- STP PortFast
- BPDU Guard
- OpenVPN Access Server
- FreeRADIUS
- OPNsense
- Suricata IDS/IPS
- VLANs
- Network Segmentation

## Repository Structure

```text
packet-tracer/
  zone-based-firewall.pkt
  portfast-bpdu-guard.pkt

report/
  Member_4_Individual_Contribution_Report.pdf

screenshots/
  zbf-topology.png
  zbf-http-success.png
  zbf-ping-blocked.png
  zbf-policy-verification.png
  bpduguard-test-topology.png
  bpduguard-err-disabled.png

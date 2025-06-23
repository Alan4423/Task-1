# Task-1

Network Scanning Report
Overview

This task involved performing basic network reconnaissance using the ifconfig and nmap tools on a Kali Linux system. The goal was to identify active hosts and open ports within the local network subnet.
Steps Performed
1. Interface Configuration

The ifconfig command was used to identify the IP address of the Kali machine:

    Interface: eth0

    IP Address: 192.168.64.2

    Subnet: /24 (i.e., 192.168.64.0–192.168.64.255)

2. Network Scanning

We performed a TCP SYN scan (-sS) on the entire subnet using nmap:

nmap -sS 192.168.64.2/24

3. Output Logging

Scan results were saved to a file:

nmap -sS 192.168.64.2/24 -oN scan_result.txt

4. Results Summary

    Active Hosts Detected:

        192.168.64.1: 4 open TCP ports

            Port 53: domain (DNS)

            Port 5000: upnp

            Port 5001: commplex-link

            Port 7000: afs3-fileserver

        192.168.64.2: Host is up, but all 1000 scanned TCP ports are closed.

Conclusion

The scan identified two active hosts on the network. The router or gateway (192.168.64.1) has several open services, while the scanning machine (192.168.64.2) has no open TCP ports exposed at the time of scanning.

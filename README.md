# Elastic SIEM – Agent-Based Threat Detection Project -Using-Custom-Security-Rule


## Overview
This project demonstrates how to deploy and configure Elastic Security (SIEM) on Elastic Cloud for real-time threat detection.
It covers the full setup of the ELK Stack (Elasticsearch, Logstash, Kibana), deployment of Elastic Agents on a Kali Linux system, and creation of custom security rules for network monitoring.

## Objective:
•	Connect Elastic Agent to Elastic Cloud
•	Monitor Linux system activity
•	Create custom detection rules (ICMP/ping)
•	Enable automated email alerting

## Tools & Technologies
•	Elastic Cloud (GCP – us-central1)
•	Kibana (Elastic Security)
•	Elastic Agent
•	Kali Linux (VirtualBox)
•	SMTP for Email Alerts

## Key Features
  •	Agent-based data collection and monitoring
  •	Custom detection rule to identify ICMP (ping) activity
  •	Log analysis via Kibana Discover tab
  •	Email notification integration for triggered alerts
  •	Real-time visualization of system and process events

## Setup Instructions
### 1.	Elastic Cloud Deployment
    1.	Sign up at Elastic Cloud
    2.	Choose Elastic Security
    3.	Deploy in region GCP (us-central1)
### 2.	Kali Linux Setup
    1.	Download Kali Linux 2023.2 VirtualBox image
    2.	Import .vbox & .vdi files into VirtualBox
    3.	Start VM and verify internet connectivity
### 3.	Elastic Agent Installation
    1.	In Elastic Security → Fleet, click Add Agent
    2.	Copy the command and execute in Kali terminal
    3.	Verify status = Healthy in Fleet
    4.	Create Custom Detection Rule

### Example Query:
                event.action: "network_icmp" or process.args: "ping"
Trigger test:
                  ping 8.8.8.8

## Configure Email Alerts
    •	Add Elastic Cloud SMTP under Rule → Actions
    •	Select Summary of alerts per rule run

## Results
•	Successfully detected ICMP (ping) events from the Kali host
•	Received automated alerts via email
•	Validated live data flow between endpoint and Elastic Cloud

## Conclusion
This project provided hands-on experience in SIEM setup, log analysis, and alert automation using Elastic Stack.
It reflects practical SOC operations — from endpoint monitoring to detection engineering.


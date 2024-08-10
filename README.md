# Detection Lab

## Objective

The Detection Lab project aimed to establish a controlled environment for simulating and detecting cyber attacks. The primary focus was to ingest and analyze logs within a Security Information and Event Management (SIEM) system, generating test telemetry to mimic real-world attack scenarios. This hands-on experience was designed to deepen understanding of network security, attack patterns, and defensive strategies.

### Skills Learned

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used

- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Steps
- Set up an Elastic Account.
- Installed Kali Linux VM using VirtualBox.
- Configured Elastic Agent.
  - Installed Elastic Defend and verified installation using 'sudo systemctl status elastic-agent.service'.
- Generated Security Events.
  - Used NMAP on Kali to scan for open ports and services. 
  - Ran several Nmap commands to generate diverse security events. (nmap, unauthorized ssh attempts, failed privledge escalation attempts)
- Queried security events in Elastic
    - Under Observability --> Logs, used specific search queries to filter and analyze the logs related to NMAP scans. (process.args:"sudo" AND process.args: "ssh", process.name: "nmap")
- Created Alerts
  - In Security --> Alerts in the Elastic console, created a custom rule to detect NMAP, SSH connection attempts, privledge escalation attempt scans.
  - Set up actions like email notifications to trigger when rule conditions were met
  - Configured alert with high severity level

- Documentation
![Screenshot 2024-08-10 at 10 56 51 AM](https://github.com/user-attachments/assets/6eaaa305-ed29-4afb-a55d-7192242f0cb0)
![Screenshot 2024-08-10 at 9 49 01 AM](https://github.com/user-attachments/assets/cbb02b25-31bc-4d9c-ab8c-662859f02e59)
![Screenshot 2024-08-10 at 10 52 49 AM](https://github.com/user-attachments/assets/999e2a25-a51a-4b0f-887a-867baf8fade8)
![Screenshot 2024-08-10 at 11 13 48 AM](https://github.com/user-attachments/assets/9e5985fb-7196-4efd-ac38-c5a0b48b0178)


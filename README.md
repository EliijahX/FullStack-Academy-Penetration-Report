# FullStack-Academy-Penetration-Report
Red Team Penetration Test – Capture the Flag
As part of a cybersecurity training program at Fullstack Academy, I completed an individual red team engagement targeting an isolated network. This exercise tested my ability to identify vulnerabilities, exploit systems, escalate access, and retrieve sensitive data across multiple platforms.
# 
Engagement Overview
After contributing to a successful team-based penetration test, I was assigned a follow-up assessment on a separate segment of the network. The goal was to conduct a full penetration test independently, working within the constraints of a simulated enterprise environment.

Scope and Rules
Only systems within the same /20 subnet as my Kali Linux machine were in scope.
No use of social engineering or client-side attacks.
All tools used were pre-installed; no external downloads allowed.
Collaboration was allowed, but the full execution was completed individually.
# 
1. Summary of Testing Process
Network Reconnaissance
Identified active hosts and scanned ports/services using Nmap.

2. Initial Exploitation
Accessed a web service running on a non-standard port and executed commands remotely.

3. Lateral Movement
Located and extracted SSH keys from the first compromised system and used them to connect to a second Linux machine.

4. Credential Discovery
Searched for sensitive files and located a Windows administrator password hash.

5. Hash Cracking
Used John the Ripper and wordlists to recover the original password from the MD5 hash.

6. Windows Exploitation
Leveraged Metasploit's psexec module to access a Windows host using valid credentials.

7. Pass-the-Hash Technique
Extracted password hashes and used them to access the final Windows system without needing plaintext credentials.

8. Flag Retrieval
Located and read the secrets.txt file as proof of successful compromise.

# Final Outcome
The simulation successfully demonstrated the full compromise of an isolated environment through reconnaissance, exploitation, and escalation. The contents of the secrets.txt file served as confirmation of completion.

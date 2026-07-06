# Lab 1 — Cyber Threat Intelligence (CTI) Report Mapping to MITRE ATT&CK

## Group Members
* Irvin (Yitzhak) Rosenfeld
* Magen Hai Lakau

## Link to the Source CTI Report
[2026 World Cup: Discussing The World's Biggest Game's Attack Surface](https://unit42.paloaltonetworks.com/fifa-world-cup-attack-surface/)

## Short Attack Summary
This CTI report assesses the massive attack surface of the 2026 FIFA World Cup, highlighting critical threats from both financially motivated cybercriminals and state-nexus actors. A primary geopolitical threat identified is the "Handala Hack Team" (also known as Void Manticore, Storm-0842, or Banished Kitten), which operates as a front persona for Iran's Ministry of Intelligence and Security (MOIS). This threat actor group is known for executing significant wiper attacks, targeting high-level government officials, and doxxing employees. In the context of the World Cup, the attackers aim to perform highly visible, disruptive operations against U.S. municipal infrastructure and tournament IT. Their operations involve stealing sensitive data for "hack-and-leak" extortion campaigns against officials, sponsors, and athletes, followed by deploying destructive wiper malware or executing large-scale DDoS attacks during high-profile ceremonies.

## Attack Diagram / Sequence
1. **Targeting & Reconnaissance:** The threat actors identify high-visibility targets, including tournament IT infrastructure, host-city municipal services (water, energy, transit), sponsors, and government officials.
2. **Initial Access:** Attackers compromise networks by exploiting internet-exposed infrastructure (such as PLCs, HMIs, or vulnerable servers) or through spear-phishing campaigns.
3. **Data Collection & Exfiltration:** Sensitive personal and corporate data is accessed and stolen to be used later for public doxxing and "hack-and-leak" psychological operations.
4. **Disruption & Destruction (Impact):** The attackers launch massive Distributed Denial of Service (DDoS) attacks against ticketing and federation services, or deploy destructive Wiper malware to permanently erase data and paralyze tournament IT systems.

## MITRE ATT&CK Mapping

| Tactic | Technique | Behaviors from the report | Link |
| --- | --- | --- | --- |
| **Initial Access** (TA0001) | **Exploit Public-Facing Application** (T1190) | Attackers target and exploit internet-exposed infrastructure, specifically municipal IT/OT components like PLCs and HMIs in host cities. | [T1190](https://attack.mitre.org/techniques/T1190/) |
| **Exfiltration** (TA0010) | **Exfiltration Over C2 Protocol** (T1041) | Stealing sensitive information belonging to high-level officials, athletes, and corporate employees for public doxxing and hack-and-leak operations. | [T1041](https://attack.mitre.org/techniques/T1041/) |
| **Impact** (TA0040) | **Data Destruction** (T1485) | The Handala Hack Team deploys "Wiper" malware to permanently destroy files and disrupt IT operations during high-visibility tournament ceremonies. | [T1485](https://attack.mitre.org/techniques/T1485/) |
| **Impact** (TA0040) | **Network Denial of Service** (T1498) | Pro-Iran hacktivists and state-aligned groups execute DDoS attacks targeting host-city networks, federation portals, and digital ticketing services. | [T1498](https://attack.mitre.org/techniques/T1498/) |

## Insights / What You Learned
This report demonstrates that mega-events like the World Cup are not just targets for financial fraud, but are prime stages for state-sponsored psychological operations and kinetic-level disruption. We learned that threat actors like the Handala Hack Team combine traditional data theft (doxxing) with destructive techniques (wipers) to maximize chaos, meaning defenders must protect both data confidentiality and the operational resilience of physical infrastructure.

# OpenCTI

**Overview**

OpenCTI (Open Cyber Threat Intelligence) is an open-source threat intelligence platform designed to centralize and analyze cyber threat information. It allows organizations to manage, structure, and share threat intelligence data effectively. Developed with a focus on collaboration and integration, OpenCTI enables analysts to gain actionable insights and improve their cybersecurity posture.

**Key Features of OpenCTI**:
	
	
 1. **Threat Intelligence Management**:
		○ Centralizes data related to threats, actors, techniques, tools, vulnerabilities, and campaigns.
		○ Supports frameworks like MITRE ATT&CK, allowing better mapping of adversarial behavior.
	
 2. **Data Structuring and Relationships**:
		○ Stores information in a graph-based database, showing relationships between entities such as threat actors, TTPs (Tactics, Techniques, and Procedures), and indicators of compromise (IoCs).
		○ This helps in understanding the full context of threats and their connections.

 3. **Integration Capabilities**:
		○ Integrates with various security tools such as SIEMs, SOAR platforms, and other cybersecurity tools.
		○ Supports data sharing and enrichment through APIs and integrations with external threat intelligence feeds.

 4. **Collaboration**:
		○ Facilitates sharing threat intelligence within teams and across organizations or communities.
		○ Promotes collaborative analysis and knowledge sharing to combat shared threats.

 5. **Visualization**:
		○ Provides intuitive dashboards and visualization tools for exploring relationships between threat entities.
		○ Helps SOC teams and analysts track trends and anomalies effectively.

 6. **STIX/TAXII Support**:
		○ Uses STIX (Structured Threat Information Expression) format for representing threat data and TAXII (Trusted Automated Exchange of Intelligence Information) for sharing threat intelligence.

 ![image](https://github.com/user-attachments/assets/c94b3196-82e4-493a-8f56-6f982936247e)

7 **Benefits of OpenCTI**:
	• Centralization: Eliminates silos by consolidating threat data into a single platform.
	• Contextual Insights: Graph-based relationships enhance understanding of how threats evolve and interconnect.
	• Automation: Automates threat intelligence workflows, saving analysts time.
	• Open-Source: Free to use, with community contributions enhancing its features regularly.
	• Scalability: Can scale to support organizations of various sizes.

**Use Cases**:
	1. Threat Analysis: SOC analysts use OpenCTI to investigate and correlate threat data with ongoing incidents.
	2. Incident Response: Helps IR teams understand the scope and impact of attacks by providing detailed threat context.
	3. Threat Hunting: Supports proactive identification of threats by analyzing IoCs and threat actor behavior.
	4. Collaboration: Enables sharing intelligence between organizations, especially in sectors like finance or healthcare.

---
## OpenCTI Dashboard

Widgets on the dashboard showcase the current state of entities ingested on the platform via the total number of entities, relationships, reports and observables ingested, and changes to these properties noted within 24 hours.

![image](https://github.com/user-attachments/assets/e5abb51f-3071-4ada-9f28-91dac0a2123b)

	
 **Activities and Knowledge**
   - The activities section covers security incidents ingested onto the platform in the form of reports.
   - The Knowledge section provides linked data related to the tools adversaries use, targeted victims and the type of threat actors and campaigns used.


**Analysis**
		- contains the input entities in reports analysed and associated external references. 
		- Reports are central to OpenCTI as knowledge on threats and events are extracted and processed. They allow for easier identification of the source of information by analysts. 
    - Analysts can add their investigation notes and other external resources for knowledge enrichment. As displayed below, we can look at the Triton Software report published by MITRE ATT&CK and observe or add to the details provided.

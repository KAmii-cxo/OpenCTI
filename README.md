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

![image](https://github.com/user-attachments/assets/1d78b80e-accd-4631-b6d7-24b1f17b18a8)

**Events**
  - Record findings and enrcih threat intel by creating associations for incidents.

![image](https://github.com/user-attachments/assets/b743703f-be6d-488b-9c45-8e034c472524)

**Observations**
 - Contains of technical elements, detections rules and artefacts identified during attacks.
 - Assist in mapping out the threat events during a hunt and connects between observation and intel feeds.
	
**Threats**
 - All information classified as threatening to an organisation or information would be classified under threats, includes:
		
	- Threat Actors: An individual or group of attackers seeking to propagate malicious actions against a target.
			
	- Intrusion Sets: An array of TTPs, tools, malware and infrastructure used by a threat actor against targets who share some attributes. APTs and threat groups are listed under this category on the platform due to their known pattern of actions.
			
	- Campaigns: Series of attacks taking place within a given period and against specific victims initiated by advanced persistent threat actors who employ various TTPs. Campaigns usually have specified objectives and are orchestrated by threat actors from a nation-state, crime syndicate or other disreputable organization.

![image](https://github.com/user-attachments/assets/c37d792a-f750-4fb2-82db-fecbbaf6881a)

**Arsenal**
 - List of items realted to an related to an attack and any legitimate tools identified from the entities.
		
	- Malware: Known and active malware and trojan are listed with details of their identification and mapping based on the knowledge ingested into the platform. In our example, we analyse the 4H RAT malware and we can extract information and associations made about the malware.
			
	- Attack Patterns: Adversaries implement and use different TTPs to target, compromise, and achieve their objectives. Here, we can look at the details of the Command-Line Interface and make decisions based on the relationships established on the platform and navigate through an investigation associated with the technique.
			
	- Courses of Action: MITRE maps out concepts and technologies that can be used to prevent an attack technique from being employed successfully. These are represented as Courses of Action (CoA) against the TTPs.
			
	- Tools: Lists all legitimate tools and services developed for network maintenance, monitoring and management. Adversaries may also use these tools to achieve their objectives. For example, for the Command-Line Interface attack pattern, it is possible to narrow down that CMD would be used as an execution tool. As an analyst, one can investigate reports and instances associated with the use of the tool.
			
	- Vulnerabilities: Known software bugs, system weaknesses and exposures are listed to provide enrichment for what attackers may use to exploit and gain access to systems. The Common Vulnerabilities and Exposures (CVE) list maintained by MITRE is used and imported via a connector.

![image](https://github.com/user-attachments/assets/0febe6c8-c488-4100-8a5b-c5165b8bb0cc)

**Entities**

 - Categorises all entities based on operational sectors, countries, organisations and individuals. This information allows for intel on attacks, organizations or intrusion sets.

![image](https://github.com/user-attachments/assets/09eb60c5-2196-495e-9d54-6bea1ec368df)

Exercise
 - The group that use 4H RAT Malware is PutterPanda
 - The kill-chain phase linked with the Command-Line Interface Attack is execution-ics.
	
**General Tabs Navigation**

 - We use Cobalt Strike malware for this walkthrough
		
 - Overview Tab: Provides the general information about an entity being analysed and investigated. In our case, the dashboard will present you with the entity ID, confidence level, description, relations created based on threats, intrusion sets and attack patterns, reports mentioning the entity and any external references.

![image](https://github.com/user-attachments/assets/3c5afb93-66e1-4a71-87cc-6bba7b52f911)

- Knowledge Tab: Presents linked information associated with the entity selected. This tab will include the associated reports, indicators, relations and attack pattern timeline of the entity. Additionally, an analyst can view fine-tuned details from the tabs on the right-hand pane, where information about the threats, attack vectors, events and observables used within the entity are presented.

![image](https://github.com/user-attachments/assets/9e0ac445-6cbe-4ab0-854f-8cb3244ee025)

- Analysis Tab: Provides the reports where the identified entry has been seen. The analysis provides usable information about a threat and guides investigation tasks.

![image](https://github.com/user-attachments/assets/b3bc0f07-cc0c-4f33-81ab-70d8bf227fc5)

- Indicators Tab: Provides information on IOC identified for all the threats and entities.

- Data Tab: Contains the files uploaded or generated for export that are related to the entity. These assist in communicating information about threats being investigated in either technical or non-technical formats.
		
- History Tab: Changes made to the element, attributes, and relations are tracked by the platform worker and this tab will outline the changes.
		
Exercise
	
- CopyKittens, FIN7 are the intrusion sets associated with the Cobalt Strike malware with Good confidence level.
- The author of entity is The MITRE Corporation
			
As a SOC analyst, you have been tasked with investigations on malware and APT groups rampaging through the world. Your assignment is to look into the CaddyWiper malware and APT37 group. Gather information from OpenCTI to answer the following questions.
		
 - The date is 15 March 2022.

![image](https://github.com/user-attachments/assets/19b0f168-9e8a-4e87-9733-e96913ba7e42)

- Native API is the attack technique linked to malware relations 

![image](https://github.com/user-attachments/assets/6ceb4dc6-5562-4ab2-8b94-85178dd4394a)

- The tools used by the technique in 2016 are ShimRatReporter, Empire, Bloodhound

![image](https://github.com/user-attachments/assets/b576a44c-e7f7-42a0-962d-1c960c535883)

- APT37 associated with North Korea

![image](https://github.com/user-attachments/assets/40ce8c74-63f3-4199-9c91-86230eb46f84)

- Technique used are T1189, T1566
  
![image](https://github.com/user-attachments/assets/7632c3ba-62af-4a8e-aa6a-984929826aec)

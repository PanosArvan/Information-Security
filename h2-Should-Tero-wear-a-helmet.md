# Should Tero wear a helmet

## Threat modeling

The Threat Modeling Manifesto, available at https://www.threatmodelingmanifesto.org/, 
outlines a set of principles and guidelines for effective threat modeling in cybersecurity.

These are:

- Collaboration: Emphasizes the importance of collaborative efforts in threat modeling within the cybersecurity domain.
- Simplicity: Stresses the need for simplicity in the threat modeling process, advocating for straightforward and easily understandable practices.
- Adaptability: Encourages an adaptable approach, recognizing that threat modeling should seamlessly integrate into development workflows.
- Integration: Highlights the necessity of integrating threat modeling into development processes, making it an inherent part of the software development life cycle.
- Prioritization: Recommends prioritizing relevant threats, focusing on those that pose the most significant risks to the security of the system.
- Diversity of Perspectives: Acknowledges the importance of incorporating diverse perspectives into the threat modeling process to enhance the identification and mitigation of potential threats.
- Resource for Professionals: Positions itself as a valuable resource for cybersecurity professionals looking to refine their threat modeling approach and bolster the security resilience of software systems.

Threat model is used to anticipate problems when it's inexpensive to deal with them.

Four question framework for threat modeling:

-What are we working on?
-What can go wrong?
-What are we going to do about it?
-Did we do a good enough job?

The OWASP Threat Modeling Cheat Sheet offers a comprehensive guide for effective threat modeling in cybersecurity.

It covers essential concepts, methodologies, and best practices for identifying, assessing, and mitigating security threats in software systems.

The cheat sheet serves as a practical resource, providing step-by-step guidance for security professionals involved in threat modeling processes.

It offers detailed, step-by-step guidance to enhance the robustness of threat modeling processes.

The cheat sheet includes considerations and factors to be taken into account during the threat modeling process, contributing to a thorough and effective approach.

Tailored for security professionals, it is designed to aid them in strengthening the security posture of software systems.

Resources: 

Braiterman et al 2020:[Threat Modeling Manifesto](https://www.threatmodelingmanifesto.org/)

[Welcome to the Worlds Shortest Threat Modeling Course](https://www.youtube.com/watch?v=oZWy-PEhBT8&list=PLCVhBqLDKoOOZqKt74QI4pbDUnXSQo0nf&index=5)

[Threat Modeling Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html)

## Security hygiene

- Use Strong Passwords
- Enable Two-Factor Authentication (2FA)
- Keep Software Updated
- Use a Secure Connection (HTTPS)
- Be Cautious with Emails
- Regularly Back Up Data
- Use Security Software
- Review App Permissions

More advanced would be:

- Encryption for Sensitive Data
- Password Managers
- Network Segmentation

## Make-belief boogie-man - a threat model for imaginary company

1) What are we working on?

Imagine "CyberGuard Solutions," an imaginary company that specializes in providing cybersecurity services to a wide range of clients. The company offers services such as penetration testing, vulnerability assessments, and security consulting. The business relies on a robust IT infrastructure to deliver its services, manage client data securely, and maintain its reputation in the cybersecurity industry.

Assets:

Client Data: Sensitive information about clients, including business strategies, intellectual property, and potentially confidential details about their own security measures.
Company Reputation: The trust and credibility established in the cybersecurity domain, crucial for acquiring new clients and retaining existing ones.
Employee Information: Personal and professional details of the company's employees, including credentials and personal identification information.
Technology Infrastructure: Systems, servers, and networks necessary for conducting cybersecurity assessments and managing internal operations.
Financial Assets: The monetary value associated with the company's contracts, revenue, and financial transactions.
Prioritization:
Prioritizing these assets is essential. While all assets have significance, customer data and the company's reputation are crown jewels. A compromise in either could lead to severe consequences for the business.

Security Supporting Business:
In the cybersecurity industry, the reputation of being secure is paramount. Clients trust CyberGuard Solutions to protect their assets, and any breach could not only result in financial loss but also damage the company's credibility.

Diagram of Company Systems:
(See attached diagram)

Description:
CyberGuard Solutions operates on a network that includes a secure client portal, internal servers for data storage and processing, employee workstations, and a connection to the internet for research and updates.


2) What can go wrong?

Attack Trees:
Attack trees visualize potential threats by branching out from a central goal. In this case, the goal could be a compromise of client data.

Identified Risks:

Phishing Attacks: Employees falling victim to phishing emails could lead to unauthorized access to sensitive information.
Zero-Day Exploits: Unknown vulnerabilities in software could be exploited, jeopardizing the security of client data.
Insider Threats: Malicious actions or negligence by employees could result in data breaches.
Distributed Denial of Service (DDoS) Attacks: Disruption of services could impact client engagements and damage the company's reputation.
Prioritization of Risks:
Phishing attacks and insider threats pose significant risks due to their potential for direct access to sensitive information. Zero-day exploits also rank high as they can be highly damaging if not promptly addressed.

Specific Threat Actors:
Cybersecurity companies are attractive targets for hackers looking to gain insights into new defense strategies. Threat actors may include cybercriminals seeking valuable client information, hacktivists with ideological motives, or even rival cybersecurity firms.

Known TTPs:
Adversaries may use tactics such as social engineering, exploiting software vulnerabilities, or leveraging insider information to carry out attacks.

Capability, Opportunity, Intent (COI):
Threat actors with the capability to exploit vulnerabilities, the opportunity to access sensitive data, and the intent to cause harm present the highest risk.

3) What are we going to do about it?

Risk Mitigation Strategies:

Employee Training: Regular training programs to educate employees on identifying and avoiding phishing attempts.
Patch Management: Promptly apply patches to address software vulnerabilities and mitigate the risk of zero-day exploits.
Access Controls: Implement strict access controls and monitor employee activities to prevent insider threats.
DDoS Protection: Employ DDoS protection services to ensure the availability of critical systems during potential attacks.
Risk Reduction Strategies:

Network Segmentation: Segment the network to limit lateral movement in case of a breach.
Data Encryption: Encrypt sensitive client data to protect it even if unauthorized access occurs.
Incident Response Plan: Develop and regularly test an incident response plan to minimize the impact of security incidents.
Risk Acceptance:
While all possible measures will be taken, it's important to acknowledge that complete security is impossible. Some level of risk acceptance is inherent in any business.

4) Did we do a good enough job?

Continuous Improvement:

Security Audits: Regularly conduct internal and external security audits to identify weaknesses and areas for improvement.
Penetration Testing: Periodic penetration tests to simulate real-world attacks and assess the effectiveness of security measures.
Continuous Threat Modeling: Regularly update threat models to account for evolving threats and technologies.
Employee Feedback: Encourage employees to report security concerns and provide feedback on the effectiveness of security measures.
Conclusion:
CyberGuard Solutions recognizes the dynamic nature of cybersecurity threats and is committed to a proactive and continuous approach to security. By understanding its assets, identifying potential risks, implementing mitigation strategies, and regularly evaluating its security posture, the company aims to provide top-notch cybersecurity services while safeguarding its own integrity and client trust.

# h1 Should Tero wear a helmet?

As the notes on the various contents take up quite a lot of space, I have listed them at the bottom of the page!

---

# Tasks

## a) Security Hygiene

### Basic Security Practices Everyone Should Follow:
- **Use Strong, Unique Passwords:**
  - Avoid using the same password across multiple accounts.
  - Use a password manager to generate and store complex passwords.

- **Enable Two-Factor Authentication (2FA):**

- **Regularly Update Software:**
  - Keep your operating system, apps, and security software up to date.

- **Be Aware of Phishing Attempts:**
  - Avoid clicking on suspicious links or downloading attachments from unknown sources.

- **Backup Data Regularly:**
  - Regularly backup important data.
  - Ensure backups are stored separately from your main system.

- **Use Antivirus and Firewall Protection:**

- **Practice Safe Browsing:**
  - Avoid visiting untrusted websites.
  - Use a secure and privacy-focused browser.

- **Limit Public Wi-Fi Use:**
  - Avoid accessing sensitive information over public Wi-Fi.
  - Use a VPN when connecting to public Wi-Fi networks.

---

## b) Make-belief Boogie-Man - A Threat Model for an Imaginary Company

### Imaginary Company: **XYZ Helsinki Health Services**

#### (1) What are we working on?

- **Our Assets:**
  - **Crown Jewels:**
    - **Patient Health Data:** Includes personal health records, treatment history, and insurance information.
    - **Patient Portal:** Interface where patients schedule appointments, access records, and communicate with healthcare providers.
  - **Supporting Assets:**
    - **Internal Communication System:** Email and messaging platforms used by employees.
    - **Financial System:** (e.g. SAP) Manages billing, payments, and payroll.

- **Security Supports Business:**
  - Protecting patient data is crucial to maintaining trust and compliance with regulations (e.g., HIPAA).
  - Secure operations ensure continuous service delivery, essential for patient care and company reputation.

- **Diagram of Company Systems:**
  - (Consider a simplified diagram showing the interaction between the Patient Portal, Health Monitoring System, Internal Communication System, and Financial System.)

- **Customer is the King:**
  - **Customer Needs:**
    - Secure, easy access to health records and services.
    - Assurance that their personal health data is safe and private.
  - **Touchpoints:**
    - **Patient Portal:** The main interface for customer interaction.
    - **Customer Support:** Available via phone, email and secure messaging.

#### (2) What can go wrong?

- **Threat Modeling Approaches:**
  - **STRIDE:**
    - **Spoofing:** Unauthorized access to patient accounts through weak authentication.
    - **Tampering:** Modification of health records by unauthorized personnel.
    - **Repudiation:** Patients or staff denying actions taken on the system.
    - **Information Disclosure:** Unintentional exposure of patient data.
    - **Denial of Service:** Attack on the Patient Portal, making it inaccessible.
    - **Elevation of Privileges:** An attacker gains admin access to the Health Monitoring System.

- **Prioritize Biggest Risks:**
  - **High Risk:** Unauthorized access to patient data (Spoofing).
  - **Expected Value:** The probability of a data breach is moderate, but the monetary value of potential fines and loss of trust is extremely high. e.g. 
  
- **Threat Actors:**
  - **Potential Attackers:**
    - **Cybercriminals:** Interested in stealing personal health information (PHI) for financial gain.
    - **Nation-State Actors:** May target healthcare systems to destabilize.
  - **TTPs:**
    - **Phishing:** Common method used to gain initial access.
    - **Ransomware:** Encrypts patient data to extort money.

- **Business Continuity:**
  - **Service Continuity:** Ensuring the Patient Portal and Health Monitoring Systems are always available.
  - **Trust Maintenance:** Protecting patient data to maintain trust and comply with regulatory requirements.

#### (3) What are we going to do about it?

- **Mitigation Strategies:**
  - **Reduce Attack Surface:** Implement stronger access controls and network segmentation.
  - **Limit Entry Points:** Use multi-factor authentication for all critical systems.
  - **META Approach:**
    - **Mitigate:** Enhance encryption and secure configuration of all systems.
    - **Eliminate:** Remove outdated or unused services that may pose a risk.
    - **Transfer:** Use cybersecurity insurance to cover potential data breach costs.
    - **Accept:** Accept low-risk issues that have minimal impact.

#### (4) Did we do a good enough job?

- **Evaluation Process:**
  - **Security Audits:** Regularly scheduled audits to assess the effectiveness of security measures.
  - **Penetration Tests:** Conduct simulated attacks to identify vulnerabilities.
  - **Continuous Threat Modeling:** Regular updates and reviews of the threat model to adapt to new threats.
  - **Process Over One-Time Job:** Recognize that threat modeling and security practices are ongoing efforts that require continuous attention and improvement.

---

# Threat Modeling Content Notes

## Videos: Welcome to the World’s Shortest Threat Modeling Course

## Introduction
- **Timing of Threat Modeling:**
  - Threat modeling should occur before any action (e.g., coding) is performed.
  - It’s a set of methods that allow you to think about security proactively.

## 4 Basic Framework Questions
1. **What are we working on?**
2. **What could go wrong?**
3. **What do we do about it?**
4. **Did we do a good job?**

## Collaboration to Answer Questions
- **Beyond Whiteboards:**
  - Collaboration goes beyond just using whiteboards.
  - Online tools are excellent for enabling collaborative threat modeling.

## Sketching
- **Purpose of Sketching:**
  - Sketching involves writing down what’s in our heads for others to engage with.
  - It is the first step in answering "What are we working on?"

- **Importance of Recording Threat Models:**
  - Proper records are crucial, especially for regulatory purposes.
  - Detailed records encourage deeper consideration of the threat model.

## Data Flow Diagrams
- **Concept of Trust Boundaries:**
  - Different elements are operated by different entities, people, or processes, leading to trust boundaries.
  - Data flows connect these different elements.

- **5 Elements of a Data Flow Diagram:**
  1. External entities
  2. Data Flows
  3. Data Stores
  4. Trust boundaries
  5. Processes

## What Can Go Wrong?
- **Core Question of Threat Modeling:**
  - This is the heart of threat modeling.
  - Pay close attention to the answers provided.

## Structure: STRIDE
- **Threat Categories:**
  - **S**poofing
  - **T**ampering
  - **R**epudiation
  - **I**nformation Disclosure
  - **D**enial of Service
  - **E**levation of Privileges
  - One threat should be identified for each category.

- **Threat Measurement:**
  - For each identified threat, some form of measurement or mitigation must be designed.

## Risk Management
- **Role in Threat Modeling:**
  - Risk management should help evaluate what to do about the identified threats.
  - Threat modeling informs and supports risk management decisions.

## Evaluation: Have We Done a Good Job?
- **Self-Reflection:**
  - Would you recommend threat modeling to your colleagues?
  - Do you feel that the effort was worth it?

### Questions/Ideas:
- How does risk management relate to threat modeling?

---

## Braiterman et al 2020: Threat Modeling Manifesto

### Summary
- **Definition of Threat Modeling:**
  - Analyzing system representations to identify security and privacy concerns.
  - Involves four key questions:
    1. What are we working on?
    2. What can go wrong?
    3. What are we going to do about it?
    4. Did we do a good enough job?

- **Purpose of Threat Modeling:**
  - Recognize potential system failures.
  - Identify and mitigate design and implementation issues.
  - Inform decision-making throughout the system's lifecycle.

- **Who Should Threat Model:**
  - Everyone concerned with privacy, safety, and security.

- **Values:**
  - Finding and fixing design issues over checkbox compliance.
  - People and collaboration over processes, methodologies, and tools.
  - Continuous refinement over single delivery.

- **Principles:**
  - Use threat modeling to improve system security and privacy through regular analysis.
  - Align threat modeling with organizational development practices.
  - Ensure outcomes are valuable to stakeholders.
  - Emphasize dialogue for establishing common understanding.

- **Recommended Patterns:**
  - Systematic approach, informed creativity, varied viewpoints, useful toolkit, theory into practice.

- **Anti-patterns to Avoid:**
  - Hero threat modeler, tendency to overfocus, perfect representation.

### Questions/Ideas:
- How can the principles outlined in the manifesto be adapted for small-scale projects with limited resources?
- What strategies can be employed to ensure continuous threath modeling?
- What are the key benefits of involving everyone in the threat modeling process?

---

## OWASP Cheat Sheets Series Team 2021: Threat Modeling Cheat Sheet

### Summary
- **Core Concepts of Threat Modeling:**
  - **Identify Assets:** What are you trying to protect?
  - **Identify Threats:** What can go wrong?
  - **Apply Mitigations:** What can you do about it?
  - **Validate:** Ensure mitigations effectively address threats.

- **Threat Modeling Approaches:**
  - **STRIDE:** Focus on six categories (Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege).
  - **Attack Trees:** Break down a threat into a tree structure to explore different attack paths.
  - **PASTA:** Align threat modeling with the development lifecycle.

- **Threat Modeling in Practice:**
  - **Early and Frequent Analysis:** Integrate threat modeling from the start and continuously throughout the project.
  - **Team Collaboration:** Involve cross-functional teams to cover diverse perspectives.

- **Common Pitfalls:**
  - Ignoring the dynamic nature of threats.
  - Failing to update the threat model as the system evolves.

### Questions/Ideas:
- How can small teams efficiently implement STRIDE without extensive overhead?

---

## Darknet Diaries Podcast

### Summary

### Questions/Ideas:
- Placeholder

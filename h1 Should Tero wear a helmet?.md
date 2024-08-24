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

- **Be Aware of Phishing Attempts:**

- **Backup Data Regularly:**
  - Regularly backup important data.
  - Ensure backups are stored separately from your main system.

- **Use Antivirus and Firewall Protection:**

- **Practice Safe Browsing:**

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
  
   ![grafik](https://github.com/user-attachments/assets/73c68def-e861-41a8-b087-577c08313ff3)

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

---

# Threat Modeling Content Notes

Feel free to use my notes :-) You will notice that I started to make notes with the videos and therefore have less extensive notes about the texts. Please tell me if I missed something crucial.

# Threat Modeling Content Notes

## Videos: The World’s Shortest Threat Modeling Course

## Introduction
- **Timing:** Threat modeling should occur before any action (e.g., coding).
  - It allows proactive security planning.

## 4 Basic Framework Questions
1. **What are we working on?**
2. **What could go wrong?**
3. **What do we do about it?**
4. **Did we do a good job?**

## Collaboration to Answer Questions
- **Beyond Whiteboards:** Collaboration extends beyond whiteboards. Online tools enable collaboration.

## Sketching
- **Purpose:** Writing down ideas for others to engage with is the first step.
- **Recording Threat Models:** Proper records are essential for regulatory purposes and detailed analysis.

## Data Flow Diagrams
- **Trust Boundaries:** Different entities, people, or processes lead to trust boundaries.
- **5 Elements:**
  1. External entities
  2. Data Flows
  3. Data Stores
  4. Trust boundaries
  5. Processes

## What Can Go Wrong?
- **Core Question:** Pay close attention to the answers.

## Structure: STRIDE
- **Threat Categories:**
  - **S**poofing
  - **T**ampering
  - **R**epudiation
  - **I**nformation Disclosure
  - **D**enial of Service
  - **E**levation of Privileges

- **Threat Measurement:** Each threat needs measurement or mitigation.

## Risk Management
- **Role:** Evaluate what to do about threats. Threat modeling supports risk management decisions.

## Evaluation: Have We Done a Good Job?
- **Self-Reflection:** Would you recommend threat modeling? Was the effort worth it?

### Questions/Ideas:
- How does risk management relate to threat modeling?

---

## Braiterman et al 2020: Threat Modeling Manifesto

### Summary
- **Definition:** Analyzing system representations to identify security/privacy concerns.
- **Purpose:** Identify and mitigate design/implementation issues.
- **Who Should Threat Model:** Everyone concerned with privacy, safety, security.
- **Values:**
  - Find/fix design issues over checkbox compliance.
  - People/collaboration over processes, methodologies, tools.
  - Continuous refinement over single delivery.
- **Principles:**
  - Use threat modeling to improve security/privacy through regular analysis.
  - Align with development practices.
  - Ensure outcomes are valuable to stakeholders.
  - Emphasize dialogue for common understanding.
- **Patterns:** Systematic approach, informed creativity, varied viewpoints, useful toolkit, theory into practice.
- **Anti-patterns:** Hero modeler, overfocus, perfect representation.

### Questions/Ideas:
- How can the manifesto principles be adapted for small projects with limited resources?
- What strategies ensure continuous threat modeling?
- What are the benefits of involving everyone in threat modeling?

---

## OWASP Cheat Sheets Series Team 2021: Threat Modeling Cheat Sheet

### Summary
- **Core Concepts:**
  - **Identify Assets:** What are you protecting?
  - **Identify Threats:** What can go wrong?
  - **Apply Mitigations:** What can you do about it?
  - **Validate:** Ensure mitigations work.
  
- **Threat Modeling Approaches:**
  - **STRIDE:** 
  - **Attack Trees:** Break down threats into a tree structure.
  - **PASTA:** Align with the development lifecycle.

- **Threat Modeling in Practice:**
  - **Early/Frequent Analysis:** Integrate threat modeling from the start.
  - **Team Collaboration:** Work together on the model.

- **Common Pitfalls:**
  - Ignoring evolving threats.
  - Failing to update the model as the system evolves.

### Questions/Ideas:
- How can small teams efficiently implement STRIDE without extensive overhead?

---

## Darknet Diaries Podcast "EP 144: Rachel"

### Summary
- Rachel Tobac's journey into social engineering: Discovered her talent at Defcon's Social Engineering Village.
- Founded SocialProof Security for social engineering attacks.
- Importance of improvisation in her techniques.

### Questions/Ideas:
- How can you train social engineering attacks legally?

Note: All of the contents have been created by myself, but I used AI to structure my texts as an .md code.

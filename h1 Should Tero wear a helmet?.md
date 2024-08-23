# Threat Modeling Notes

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
- What strategies can be employed to ensure continuous refinement in dynamic development environments?

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
- In what ways can threat modeling be better integrated into Agile development cycles?

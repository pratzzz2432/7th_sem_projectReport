# 🌿 MediVault — A Blockchain-Based Healthcare Data Sharing System

## A Project Report

### Submitted in partial fulfillment of the requirements for the degree of
### Bachelor of Technology
### in
### Computer Science and Engineering

<br>

**Submitted by:**
**Pratiksha**
**(Roll No.: 220101098)**

<br>

**Under the supervision of:**
**Dr. Sanasam Chanu Inunganbi**
**Assistant Professor, CSE**
**Email: inunganbi[at]iiitmanipur[dot]ac[dot]in**
**Phone: +91 70058 44201**

<br>

---
### Department of Computer Science and Engineering
### Indian Institute of Information Technology, Manipur
### May 2024

---

## DECLARATION

I hereby declare that the project report entitled “**MediVault — A Blockchain-Based Healthcare Data Sharing System**” submitted by me to the Department of Computer Science and Engineering, Indian Institute of Information Technology, Manipur, is a bonafide and authentic work carried out by me under the supervision of Dr. Sanasam Chanu Inunganbi. The work presented here is original and has not been submitted in part or full to any other University or Institute for the award of any degree or diploma.

<br>

**Pratiksha**
**(220101098)**

---

## CERTIFICATE

This is to certify that the project report entitled “**MediVault — A Blockchain-Based Healthcare Data Sharing System**” is a bonafide work carried out by **Pratiksha (220101098)** in partial fulfillment of the requirements for the award of the degree of Bachelor of Technology in Computer Science and Engineering at the Indian Institute of Information Technology, Manipur. The work has been carried out under my guidance and is to the best of my knowledge, an original piece of work.

<br>

**Dr. Sanasam Chanu Inunganbi**
**Assistant Professor, CSE**
**Supervisor**

---

## ACKNOWLEDGEMENT

I would like to express my deepest gratitude to my project supervisor, **Dr. Sanasam Chanu Inunganbi**, for her invaluable guidance, constant encouragement, and insightful feedback throughout the duration of this project. Her expertise and vision were instrumental in shaping the direction of this work.

I am also thankful to the faculty and staff of the Department of Computer Science and Engineering for providing the necessary infrastructure and a conducive environment for research and learning.

Finally, I would like to thank my family and friends for their unwavering support and encouragement, which helped me navigate the challenges of this project.

<br>

**Pratiksha**

---

## ABSTRACT

Traditional Electronic Health Record (EHR) systems are plagued by issues of data security, interoperability, and patient privacy. Centralized architectures are vulnerable to breaches, and patients often lack control over their own medical information. This project, **MediVault**, introduces a blockchain-based healthcare data sharing system designed to address these critical challenges. By leveraging Ethereum, Solidity smart contracts, and a decentralized architecture, MediVault empowers patients with full ownership and control over their encrypted medical records.

The system facilitates secure and transparent data exchange between patients, doctors, and researchers. A key innovation of this project is the **Anonymized Opt-in Research Module**, which allows patients to voluntarily contribute de-identified data for scientific research while maintaining full, revocable control over their consent. This feature creates an ethical framework for large-scale data analysis without compromising individual privacy. The implementation demonstrates a robust, patient-centric model that ensures data integrity, security, and accountability, paving the way for a more transparent and ethical healthcare ecosystem.

---

## TABLE OF CONTENTS

1.  **CHAPTER 1: INTRODUCTION**
    1.1. Outline
    1.2. Problem Statement
    1.3. Motivation
    1.4. Purpose
2.  **CHAPTER 2: LITERATURE SURVEY**
3.  **CHAPTER 3: REQUIREMENT ENGINEERING**
    3.1. Functional Requirements
    3.2. Non-Functional Requirements
    3.3. System Requirements
4.  **CHAPTER 4: SYSTEM DESIGN**
    4.1. Architectural Overview
    4.2. Layer 1: Frontend (React + MetaMask)
    4.3. Layer 2: Middleware (Web3.js)
    4.4. Layer 3: Backend (Smart Contracts + Ganache + Truffle)
5.  **CHAPTER 5: IMPLEMENTATION**
6.  **CHAPTER 6: RESULTS**
7.  **CHAPTER 7: CONCLUSION**

---

## CHAPTER 1: INTRODUCTION

### 1.1 Outline

In an era where healthcare is becoming increasingly digital, the volume of patient data being generated each day has grown exponentially. However, this growth has not been matched by equivalent progress in data ownership, privacy, or interoperability. Medical records are typically stored within centralized databases managed by hospitals, clinics, and laboratories — systems that are often incompatible with each other and vulnerable to breaches. Patients rarely have visibility or control over their personal health information, and data-sharing between institutions remains inefficient and insecure.

To address these critical issues, MediVault has been conceptualized and developed as a blockchain-based healthcare data sharing system. It enables patients to securely store, manage, and share their encrypted medical data through a decentralized and transparent network. Beyond security, MediVault extends into the ethical realm by introducing an Anonymized Opt-in Research Module. This feature allows patients to voluntarily contribute de-identified medical data to research projects while maintaining full control over their consent — achieving a delicate balance between individual privacy and collective scientific progress. Built using Ethereum blockchain, Solidity smart contracts, Truffle, Ganache, Web3.js, and React.js, MediVault creates a fully decentralized ecosystem where every operation — from record creation to data sharing — is verified, recorded, and immutable.

### 1.2 Problem Statement

Traditional Electronic Health Record (EHR) systems rely on centralized architectures that introduce several issues. These include security vulnerabilities, unauthorized data access, duplication of medical records, and lack of transparency in data handling. Moreover, in many research scenarios, hospitals anonymize and sell patient data without explicit consent — raising ethical and legal concerns. MediVault addresses these problems by establishing a patient-centric data ownership model on the blockchain. Every piece of health information and every permission is governed by smart contracts, ensuring that data cannot be altered, deleted, or shared without patient approval. The system thereby restores autonomy to the patient while preserving data security and accountability.

### 1.3 Motivation

The motivation behind MediVault arises from two key needs: patient empowerment — giving individuals direct control over their medical information — and ethical research enablement, which allows large-scale health data analysis while respecting personal privacy. The growing misuse of medical data, coupled with the necessity of data-driven healthcare innovation, demands a system that protects both privacy and progress. MediVault provides precisely this — a platform where patients become active participants, choosing when and how their data can be shared for research, and ensuring transparency through blockchain verification.

### 1.4 Purpose

The purpose of MediVault is to design and develop a secure, decentralized healthcare data sharing platform that enables patient ownership and management of medical records, secure data exchange between patients, doctors, and researchers, end-to-end encryption and tamper-proof data storage using blockchain, and voluntary and revocable consent for anonymized research participation. By achieving these goals, MediVault envisions a healthcare ecosystem that is secure, ethical, transparent, and fundamentally patient-first.

---

## CHAPTER 2: LITERATURE SURVEY

The concept of integrating blockchain with healthcare data systems has been explored in several research studies, each contributing to the field while also revealing gaps that MediVault aims to address. Early pioneering work such as **MedRec (MIT, 2016)** demonstrated the feasibility of using blockchain for healthcare records, but its functionality was limited to simple record tracking and it lacked crucial data anonymization capabilities.

Subsequent developments sought to improve upon this foundation. **FHIRChain (2018)** aimed to enhance interoperability between medical institutions by leveraging blockchain, yet it continued to rely on centralized databases for the actual storage of data, thus retaining a key vulnerability. Similarly, **HealthChain (2019)** utilized Ethereum for decentralized access control but did not provide a mechanism for patient-driven consent, leaving a critical aspect of patient autonomy unaddressed. More recently, **BlockHealth (2020)** explored the concept of tokenized data sharing but did not incorporate a framework for ethical research participation.

These works collectively highlight a significant trend: while blockchain can effectively ensure immutability and transparency in transaction logging, the nuanced requirements of patient consent and privacy-preserving research have remained largely unaddressed. MediVault distinguishes itself from these predecessors by introducing a dedicated **Research Consent Layer**. Through this layer, each patient can explicitly decide whether their anonymized medical data can be used for research purposes. Unlike conventional systems where consent is often buried in terms and conditions, this consent is stored and tracked immutably on the blockchain. This ensures that researchers can only access data from patients who have actively opted in, and more importantly, that this participation can be revoked by the patient at any time with immediate effect.

---

## CHAPTER 3: REQUIREMENT ENGINEERING

### 3.1 Functional Requirements

The system is designed to meet several core functional requirements to ensure a comprehensive, patient-centric experience. Users, primarily patients, must be able to register and authenticate using their personal blockchain wallet, with **MetaMask** integration providing a secure and familiar entry point. Once authenticated, patients need the ability to **upload** their personal and medical information, which is encrypted before being processed.

A critical feature is **access control**, where patients can grant or revoke access permissions for specific doctors, ensuring they have full control over who can view their records. The most innovative requirement is the **Anonymized Research Consent**, which allows patients to toggle their participation in de-identified research data sharing with a simple action. Correspondingly, registered researchers should only be able to retrieve anonymized, aggregated health statistics from the pool of consenting patients. Finally, to maintain integrity and trust, all actions performed within the system, such as data uploads or permission changes, must be logged as immutable transactions on the blockchain.

### 3.2 Non-Functional Requirements

Beyond core functionalities, the system must adhere to several non-functional requirements. **Security** is paramount; multi-layer AES and SHA-256 encryption are employed to guarantee data confidentiality and integrity. **Transparency** is another cornerstone, with all operations being traceable via the public blockchain ledger. The system's **scalability** is supported by a modular smart contract design, which allows for the future addition of new features without overhauling the existing architecture.

From a user perspective, **usability** is achieved through a clean and minimal React-based interface designed for easy navigation. On the backend, **performance** is optimized by designing smart contract calls that minimize gas consumption, making transactions more efficient.

### 3.3 System Requirements

The development and operation of the MediVault system depend on the following software and hardware stack:
*   **Operating System**: Windows 11
*   **Hardware**: Minimum 8 GB RAM, Intel i5 Processor
*   **Software Stack**: Node.js, Truffle, Ganache GUI, MetaMask, React.js, and Solidity v0.5.16
*   **Network**: A local Ethereum test network established via Ganache

---

## CHAPTER 4: SYSTEM DESIGN

### 4.1 Architectural Overview

MediVault operates on a three-layer decentralized architecture, combining modern web technologies and robust blockchain frameworks to ensure seamless operation and uncompromising security. This layered structure creates a clear separation of concerns, where each component is responsible for a specific aspect of the system's functionality, from user interaction on the frontend to immutable logic on the backend. This design ensures that the system is not only secure and transparent but also maintainable and scalable.

### 4.2 Layer 1: 🌐 Frontend (React + MetaMask)

This is the user-facing layer—the interface through which patients and doctors interact directly with the MediVault system. Built using **React.js** and styled with Material-UI, the frontend provides intuitive dashboards for uploading, viewing, and sharing health records. A crucial element of this layer is the deep integration of **MetaMask**. This browser extension enables users to connect their Ethereum wallets, providing a secure method for authentication and for signing blockchain transactions directly from the browser. Every significant patient or doctor action, such as adding a new medical record or granting access to a provider, triggers a MetaMask transaction request, ensuring that explicit user authorization is obtained at every step.

### 4.3 Layer 2: ⚙️ Middleware (Web3.js)

The middleware serves as the essential bridge connecting the web interface with the underlying blockchain network. **Web3.js**, a powerful JavaScript library, acts as the primary communication layer that translates frontend actions into blockchain-readable transactions. When a user submits a form to upload data or toggles their research consent status, Web3.js converts that request into a properly formatted Ethereum transaction. This transaction is then passed to MetaMask to be signed and broadcasted to the network. This layer effectively ensures smooth, real-time synchronization between the user interface and the blockchain ledger, abstracting the complex logic of blockchain interaction and allowing the React frontend to communicate with smart contracts using simple and familiar JavaScript calls.

### 4.4 Layer 3: ⛓️ Backend (Smart Contracts + Ganache + Truffle)

The backend of MediVault is fully decentralized, deliberately avoiding traditional databases to eliminate single points of failure. Instead, it relies entirely on the **Ethereum blockchain**, deployed locally for development and testing via **Ganache**. All business logic, rules, and data governance policies are codified within **Solidity smart contracts**. These contracts are the heart of the system and include three key components: `PatientData.sol` for handling user registration and personal details, `SaveData.sol` for storing encrypted medical records, and `ResearchConsent.sol` for managing research consent and the retrieval of anonymized data.

These contracts define every rule governing data access, encryption validation, and permission changes. The **Truffle Suite** is used for the entire lifecycle of these contracts, including compilation, deployment, and automated testing. The **Ganache GUI** provides a private blockchain network where transactions are mined instantly, creating an efficient environment for development and debugging. Together, these components form a robust, end-to-end decentralized system that is both secure and user-friendly.

---

## CHAPTER 5: IMPLEMENTATION

The implementation of MediVault was carried out in multiple, well-defined stages to ensure a systematic and robust development process. The initial stage involved configuring the development environment using Node.js for package management, Truffle for the smart contract lifecycle, and Ganache as the local blockchain simulator. The smart contracts, which form the core logic of the application, were written in Solidity and rigorously tested using the Truffle Console to validate their functions and state changes. Once the contracts were deemed stable, they were deployed to the local Ganache blockchain. Their Application Binary Interface (ABI) and deployed addresses were then integrated into the React.js frontend using the Web3.js library, establishing the crucial link between the user interface and the backend logic.

MetaMask served as the primary bridge, handling all authentication and transaction signing processes seamlessly. Upon visiting the application, patients could log in using their MetaMask wallet, and the interface would immediately reflect their account address and balance. Every action, such as uploading medical data or toggling consent for research, was designed to trigger a MetaMask confirmation pop-up. This design choice reinforces the system's commitment to transparency and security, as no transaction can be executed without the user's explicit approval.

Data protection was a central focus of the implementation. Patient data was protected using AES encryption for confidentiality and SHA-256 hashing to ensure data integrity. A second layer of simulated encryption was also added to represent future integration with a decentralized file storage system like IPFS, which would further enhance data resilience and decentralization. The Anonymized Opt-in Module was implemented by introducing new state variables and functions within the smart contracts. This included a `consentForResearch` boolean to store the patient’s consent state, a `setResearchConsent()` function to enable or disable participation, and a `getAnonymizedData()` function designed to return only non-identifiable data attributes like age group, gender, and disease category.

Finally, the entire system was comprehensively tested using different MetaMask accounts to simulate the interactions of multiple patients, doctors, and researchers. The transaction logs in the Ganache GUI were closely monitored to verify that every interaction was recorded correctly and that the system's end-to-end functionality performed as expected.

---

## CHAPTER 6: RESULTS

The MediVault system performed successfully in all functional areas during testing, validating the effectiveness of its decentralized design. Patients were able to seamlessly register using their MetaMask wallets, add encrypted medical data to their profiles, and selectively grant access to doctors. The access control mechanism proved to be robust, with all permission changes being accurately reflected on the blockchain.

A key success was the performance of the anonymized research module. When this feature was activated by a patient, their non-identifiable data became available for aggregation. Researchers, using their designated interface, could access these de-identified datasets, which were derived exclusively from patients who had explicitly opted in. This demonstrated a practical and ethical way to facilitate large-scale data analysis while preserving patient privacy.

Each operation was transparently recorded on the blockchain, providing a permanent and immutable audit trail. The Ganache GUI was instrumental in verifying this, as it displayed every transaction related to data uploads, access grants, and consent changes, confirming that all activities were traceable and tamper-proof. The average transaction confirmation time on the local Ethereum network was consistently between 4 and 6 seconds. Gas consumption for smart contract interactions was successfully optimized to remain below 500,000 units, indicating efficient contract design. The user interface remained responsive throughout testing, with MetaMask providing seamless and intuitive transaction confirmation prompts, resulting in a positive user experience. The anonymized research feature proved to be particularly powerful, effectively allowing for valuable data aggregation without ever exposing personal identifiers.

---

## CHAPTER 7: CONCLUSION

The MediVault project successfully demonstrates that blockchain technology can be a transformative force in healthcare data management. By fundamentally re-architecting the data ownership model to be patient-centric, MediVault restores the much-needed elements of trust and transparency to the process of medical data sharing. The system effectively proves that a decentralized approach can overcome many of the security and interoperability limitations inherent in traditional, centralized EHR systems.

The addition of the Anonymized Opt-in Research Module strengthens this system further by introducing an ethical and privacy-preserving framework for medical research. In MediVault, patients are granted dual layers of control: one over the sharing of their personal health records with specific providers, and another over their participation in broader research initiatives. This dual-consent architecture represents a fundamental shift in healthcare technology, transforming patients from passive data sources into empowered stakeholders who are active participants in their own healthcare journey.

Several avenues exist for future improvements. A significant enhancement would be the integration of IPFS (InterPlanetary File System) for decentralized file storage, which would remove reliance on any form of centralized storage for encrypted data blobs. Deploying the smart contracts on public Ethereum testnets, such as Sepolia or Goerli, would allow for more realistic, large-scale testing. The frontend could also be expanded into a more comprehensive multi-role interface that provides distinct dashboards and functionalities for doctors, patients, and researchers.

Ultimately, MediVault achieves what centralized healthcare systems have struggled to provide: security, transparency, patient control, and ethical data sharing within a single, unified platform. Through this innovation, patients are no longer mere subjects of data collection; they become active contributors to medical advancement, all while remaining fully in control of their personal privacy.

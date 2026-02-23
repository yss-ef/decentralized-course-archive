# 🎓 CoursNetX | Decentralized Course Archive dApp

> **Final Graduation Project (PFE) - Software Engineering | Grade: 17/20**
> **CoursNetX** is a Decentralized Application (dApp) developed at FST Errachidia. It leverages **Web3** technologies to create a secure, transparent, and censorship-resistant pedagogical resource archiving platform. Unlike traditional centralized systems, it gives data control back to users using the Ethereum blockchain and the IPFS distributed storage system.

## 📑 Table of Contents

* [Architecture Overview](https://www.google.com/search?q=%23%EF%B8%8F-architecture-overview)
* [Technology Stack](https://www.google.com/search?q=%23%EF%B8%8F-technology-stack)
* [Key Features](https://www.google.com/search?q=%23-key-features)
* [Installation & Setup](https://www.google.com/search?q=%23-installation--setup)
* [Project Background](https://www.google.com/search?q=%23-project-background)

## 🏗️ Architecture Overview

CoursNetX follows the standard dApp architecture:

1. **Frontend**: User interface built with React.js.
2. **Provider/Signer**: MetaMask handles authentication and signs transactions.
3. **Smart Contract**: Logic and access control reside on the Ethereum blockchain.
4. **Off-chain Storage**: Large files are stored on **IPFS**, while only the immutable **Content Identifier (CID/Hash)** is recorded on-chain.

## 🛠️ Technology Stack

| Layer | Technology | Purpose |
| --- | --- | --- |
| **Frontend** | React.js | UI building and state management. |
| **Blockchain Bridge** | Web3.js | Communication between the frontend and Ethereum. |
| **Smart Contract** | Solidity | Developing secure on-chain business logic. |
| **Network** | Ethereum / Ganache | Blockchain deployment and local testing. |
| **Storage** | IPFS & Pinata | Decentralized, immutable file storage. |
| **Dev Framework** | Truffle Suite | Compilation, migration, and testing. |

## ✨ Key Features

* **Decentralized Authentication**: Secure login via **MetaMask** wallet—no passwords needed.
* **On-Chain Role Management**: Roles (Admin, Teacher, Student) are immutably written on the blockchain.
* **Secure File Handling**: Files are uploaded to **IPFS**. The smart contract stores the digital fingerprint (hash), ensuring data integrity and permanence.
* **Transparent History**: Every critical action (uploading a course, creating a department) is recorded as a publicly verifiable transaction.
* **Access Control**: Proprietary logic within the Solidity smart contract manages view and download permissions.

## 🚀 Installation & Setup

### Prerequisites (Fedora 43)

Ensure your environment is ready for Web3 development:

```bash
# Install Node.js
sudo dnf install nodejs npm

# Install Truffle and Ganache CLI globally
npm install -g truffle ganache

```

### Setup Steps

**1. Clone the repository**

```bash
git clone https://github.com/yss-ef/[REPO-NAME].git
cd [REPO-NAME]

```

**2. Install dependencies**

```bash
npm install

```

**3. Configure Development Environment**

* Launch **Ganache** to start a local blockchain.
* Configure **MetaMask** to connect to the Ganache RPC (usually `http://127.0.0.1:7545`).
* Import one of the private keys from Ganache into MetaMask.

**4. Deploy the Smart Contract**

```bash
truffle migrate --reset

```

**5. Launch the Frontend**

```bash
npm start

```

The dApp will be accessible at `http://localhost:3000`.

---

## 🎓 Project Background

This project represents the culmination of my Software Engineering license at **FST Errachidia**. It explores the transition from Web2 centralized archives to Web3 paradigms, focusing on data sovereignty and immutable academic records.

---

*Authored by Youssef Fellah.*

*Developed as part of the License in Software Engineering - FST Errachidia.*

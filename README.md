# Decentralized Course Archive: Web3 Academic Resource Management

A high-performance Decentralized Application (dApp) engineered to provide secure, transparent, and censorship-resistant archiving of pedagogical resources. This project leverages the Ethereum blockchain and IPFS to ensure data sovereignty and immutable academic records.

## Technical Architecture

The application implements a standard Web3 three-tier architecture, ensuring total decentralization of both logic and storage:

1.  **On-Chain Logic**: **Solidity** smart contracts managing access control, role-based permissions (RBAC), and metadata persistence.
2.  **Distributed Storage**: Integration with **IPFS** for off-chain file persistence, utilizing content-addressing (CID) to ensure data integrity.
3.  **Frontend Interface**: A **React.js** single-page application utilizing **Web3.js** for blockchain state orchestration and provider synchronization.

---

## Technical Stack

*   **Smart Contracts**: Solidity ^0.8.x
*   **Development Framework**: Truffle Suite
*   **Blockchain Bridge**: Web3.js
*   **Distributed Storage**: IPFS (Infura/Pinata Gateways)
*   **Frontend**: React.js / SCSS
*   **Wallet Integration**: MetaMask (EIP-1193 Provider)
*   **Local Network**: Ganache CLI

---

## Core Implementations

### 1. Decentralized Identity & RBAC
*   **Wallet-Based Authentication**: Leverages asymmetric cryptography via MetaMask for secure, password-less entry.
*   **On-Chain Access Control**: Implements granular Role-Based Access Control (Admin, Teacher, Student) within the smart contract to govern file interactions and administrative actions.

### 2. Immutable Content Archiving
*   **Hybrid Storage Model**: Combines on-chain metadata (Ethereum) with off-chain content (IPFS) to optimize gas costs while maintaining decentralization.
*   **Integrity Verification**: Automated mapping of IPFS Content Identifiers (CIDs) to on-chain records, ensuring that archived materials cannot be altered or removed without a verifiable transaction.

### 3. Transparent Governance
*   **Event Orchestration**: Emitting Solidity events for critical operations to provide a verifiable audit trail of academic resource lifecycles.
*   **Transactional Transparency**: Every modification to the archive is recorded as a publicly verifiable state transition on the Ethereum network.

---

## Project Structure

```text
├── course-archive/          # Solidity source & Truffle migrations
├── course-archive-frontend/ # React source & Web3 integration
├── package.json            # Workspace dependency orchestration
└── README.md               # System documentation
```

---

## Deployment & Setup

### Prerequisites
*   Node.js 18+
*   Truffle Suite
*   MetaMask Browser Extension
*   Ganache (Local Blockchain)

### 1. Smart Contract Deployment
1.  Initialize local blockchain (Ganache).
2.  Navigate to the contract directory:
    ```bash
    cd course-archive
    truffle migrate --reset
    ```

### 2. Frontend Initialization
1.  Install dependencies:
    ```bash
    cd course-archive-frontend
    npm install
    ```
2.  Start the development server:
    ```bash
    npm start
    ```

---

*Authored by Youssef Fellah.*

*Developed for the Graduation Project (PFE) - FST Errachidia.*

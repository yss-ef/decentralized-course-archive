# Decentralized course archive: Web3 academic resource management

Bottom Line Up Front: This project provides a high-performance Decentralized
Application (dApp) engineered for secure, transparent, and censorship-resistant
archiving of pedagogical resources. It leverages the Ethereum blockchain and
IPFS to ensure data sovereignty and immutable academic records.

## Technical architecture

The application implements a standard Web3 three-tier architecture, ensuring
total decentralization of both logic and storage:

1.  **On-chain logic**: Solidity smart contracts managing access control,
    role-based permissions (RBAC), and metadata persistence.
2.  **Distributed storage**: Integration with IPFS for off-chain file
    persistence, utilizing content-addressing (CID) to ensure data integrity.
3.  **Frontend interface**: A React.js single-page application utilizing
    Web3.js for blockchain state orchestration and provider synchronization.

---

## Technical stack

*   **Smart contracts**: Solidity ^0.8.x
*   **Development framework**: Truffle Suite
*   **Blockchain bridge**: Web3.js
*   **Distributed storage**: IPFS (Infura/Pinata Gateways)
*   **Frontend**: React.js / SCSS
*   **Wallet integration**: MetaMask (EIP-1193 Provider)
*   **Local network**: Ganache CLI

---

## Core implementations

### 1. Decentralized identity and RBAC
*   **Wallet-based authentication**: Leverages asymmetric cryptography via
    MetaMask for secure, password-less entry.
*   **On-chain access control**: Implements granular Role-Based Access Control
    (Admin, Teacher, Student) within the smart contract to govern file
    interactions and administrative actions.

### 2. Immutable content archiving
*   **Hybrid storage model**: Combines on-chain metadata (Ethereum) with
    off-chain content (IPFS) to optimize gas costs while maintaining
    decentralization.
*   **Integrity verification**: Automated mapping of IPFS Content Identifiers
    (CIDs) to on-chain records, ensuring that archived materials cannot be
    altered or removed without a verifiable transaction.

### 3. Transparent governance
*   **Event orchestration**: Emitting Solidity events for critical operations to
    provide a verifiable audit trail of academic resource lifecycles.
*   **Transactional transparency**: Every modification to the archive is recorded
    as a publicly verifiable state transition on the Ethereum network.

---

## Project structure

```text
├── course-archive/          # Solidity source & Truffle migrations
├── course-archive-frontend/ # React source & Web3 integration
├── package.json            # Workspace dependency orchestration
└── README.md               # System documentation
```

---

## Deployment and setup

### Prerequisites
*   Node.js 18+
*   Truffle Suite
*   MetaMask Browser Extension
*   Ganache (Local Blockchain)

### 1. Smart contract deployment
1.  Initialize local blockchain (Ganache).
2.  Navigate to the contract directory:
    ```bash
    cd course-archive
    truffle migrate --reset
    ```

### 2. Frontend initialization
1.  Install dependencies:
    ```bash
    cd course-archive-frontend
    npm install
    ```
2.  Start the development server:
    ```bash
    npm start
    ```

Authored by Youssef Fellah.
Developed for the Graduation Project (PFE) - FST Errachidia.

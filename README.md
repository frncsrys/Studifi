# StudiFi

StudiFi is a decentralized student finance platform built on the Internet Computer Protocol (ICP). It aims to provide students with access to financial assistance through blockchain-based services, including loan management, credit assessment, university credential verification, and DAO governance.

The project uses a multi-canister architecture to separate its backend services and manage different platform operations.

## Technologies Used

**Frontend**

[![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vite.dev/)
[![Sass](https://img.shields.io/badge/Sass-CC6699?style=for-the-badge&logo=sass&logoColor=white)](https://sass-lang.com/)

**Backend**

[![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Candid](https://img.shields.io/badge/Candid-5B5B5B?style=for-the-badge)](https://internetcomputer.org/docs/)
[![ic--cdk](https://img.shields.io/badge/ic--cdk-29ABE2?style=for-the-badge)](https://docs.rs/ic-cdk/)

**Blockchain & Development Tools**

[![ICP](https://img.shields.io/badge/Internet%20Computer-3B00B9?style=for-the-badge)](https://internetcomputer.org/)
[![DFX](https://img.shields.io/badge/DFX%20SDK-000000?style=for-the-badge)](https://internetcomputer.org/docs/current/developer-docs/setup/install)
[![Internet Identity](https://img.shields.io/badge/Internet%20Identity-4B6CB7?style=for-the-badge)](https://identity.internetcomputer.org/)
[![Cargo](https://img.shields.io/badge/Cargo-000000?style=for-the-badge&logo=rust&logoColor=white)](https://doc.rust-lang.org/cargo/)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![npm](https://img.shields.io/badge/npm-CB3837?style=for-the-badge&logo=npm&logoColor=white)](https://www.npmjs.com/)

## Prerequisites

Make sure the following tools are installed before setting up the project:

- [Node.js](https://nodejs.org/) (version 16 or later)
- npm (version 7 or later)
- [Rust](https://www.rust-lang.org/tools/install)
- [DFX SDK](https://internetcomputer.org/docs/current/developer-docs/setup/install)

For compiling Rust canisters to WebAssembly, install the required target:

```bash
rustup target add wasm32-unknown-unknown
```

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/renzdeveyra/studifi.git
cd studifi
```

### 2. Install Dependencies

Install the frontend dependencies from the project root:

```bash
npm install
```

## Running the Project Locally

### 1. Start the Local Internet Computer Replica

```bash
dfx start --background
```

This starts the local replica, which provides the environment for deploying and testing the canisters.

### 2. Deploy the Canisters

```bash
dfx deploy
```

This builds and deploys the backend canisters and frontend assets to the local replica.

### 3. Start the Frontend Development Server

From the project root, run:

```bash
npm start
```

The frontend development server will be available at:

```text
http://localhost:3000
```

## Development

### Frontend

The frontend is located in:

```text
src/studifi_frontend/
```

To build the frontend:

```bash
npm run build
```

### Backend

The backend services are located in:

```text
src/studifi_backend/
```

The backend is organized into separate Rust canisters, each responsible for a specific part of the platform.

After making changes to the backend interfaces, regenerate the canister declarations using:

```bash
dfx generate
```

You can redeploy the updated canisters using:

```bash
dfx deploy
```

## Backend Services

| Service | Description |
|---|---|
| Student Identity | Student profiles and identity management |
| Credit Assessment | Student credit assessment |
| Loan Management | Loan applications and management |
| DAO Governance | Governance and voting operations |
| Compliance | Compliance-related operations |
| Authentication | User sessions, roles, and permissions |
| University Credentials | University verification and credentials |

## Additional Documentation

The repository includes additional implementation documents:

- Backend Implementation Guide
- KYC Implementation
- Phase 1 Implementation Summary
- Tutorial Implementation Summary

## References

- [Internet Computer Documentation](https://internetcomputer.org/docs/)
- [DFX SDK Documentation](https://internetcomputer.org/docs/current/developer-docs/setup/install)
- [Rust Documentation](https://doc.rust-lang.org/book/)
- [React Documentation](https://react.dev/)

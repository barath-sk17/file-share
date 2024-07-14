# Document Exchange/Verification System on Ethereum Blockchain using IPFS

## Overview
In response to the challenges of verifying and managing digital documents securely, I developed a blockchain-based document exchange and verification system using Ethereum and IPFS. This system caters to companies, universities, and firms, providing a secure and efficient method to share and verify documents. Key benefits include cost reduction, risk mitigation, and enhanced productivity through the digitization of organizational processes while maintaining high trust levels and complying with security regulations.

This project includes:

- **Functional Prototype**: A working prototype of the blockchain-based eVault system, featuring document upload, retrieval, sharing, and tracking.
- **Technical Documentation**: Comprehensive documentation detailing the system’s architecture, smart contract logic, and security measures.
- **User Manual**: Instructions for stakeholders on how to use the eVault system.

## Prerequisites
- **Node**: v8.11.4 or v14
- **npm**: 5.6.0
- **Truffle**: v4.1.14 (core: 4.1.14)
- **Solidity**: v0.4.24 (solc-js)
- **Ganache-cli**: v6.1.8 (ganache-core: 2.2.1)

## Setup
1. Clone the repository:
   ```bash
   $ git clone https://github.com/barath-sk17/file-share
   ```
2. Change the current directory.

4. Install Ganache and Truffle:
   ```bash
   $ npm install -g ganache-cli truffle@v4.1.14
   ```
5. Open a new terminal, run Ganache, and keep it alive:
   ```bash
   $ ganache-cli
   ```
6. Run Solidity unit tests to check if the environment is ready:
   ```bash
   $ truffle test
   ```
7. Install node modules:
   ```bash
   $ npm install
   ```
8. Compile smart contracts:
   ```bash
   $ npm run recompile
   ```
9. Once compilation is complete, run the React app:
   ```bash
   $ npm run start
   ```
   
## Available Scripts
- Compile smart contracts: `$ truffle compile`
- Migrate smart contracts: `$ truffle migrate`
- Run tests: `$ truffle test`
- Recompile smart contracts: `$ npm run recompile`
- Start the application: `$ npm run start`
- Build the application: `$ npm run build`
- Run development server: `$ npm run dev`
- Lint code: `$ npm run lint`
- Fix lint errors: `$ npm run fix`

## Structure
```
├── config
├── contracts
│   ├── Accounts.sol
│   ├── Documents.sol
│   ├── EmailRegex.sol
│   ├── Migrations.sol
│   ├── SimpleStorage.sol
│   └── StringUtils.sol
├── eslintrc.json
├── migrations
│   ├── 1_initial_migration.js
│   ├── 2_deploy_simple_storage.js
│   ├── 3_deploy_accounts.js
│   └── 4_deploy_documents.js
├── package.json
├── public
├── README.md
├── scripts
├── src
│   ├── App.js
│   ├── assets
│   │   ├── abis    ## Smart Contract Application Binary Interface (ABI) Folder
│   │   ├── css
│   │   └── images
│   ├── components
│   │   ├── account
│   │   ├── common
│   │   ├── documents
│   │   ├── forms
│   │   ├── main
│   │   └── menu
│   ├── constants
│   ├── contracts
│   ├── index.js
│   ├── redux
│   │   ├── actions
│   │   ├── reducers
│   │   ├── store
│   │   └── type
│   ├── registerServiceWorker.js
│   └── utils
├── test
│   ├── accounts.test.js
│   ├── documents.test.js
│   ├── helpers
│   ├── simplestorage.test.js
│   └── TestSimpleStorage.sol
├── truffle-config.js
├── truffle.js
└── webpack.config.js
```

## How it Works
**Checklist**
1. Ganache-cli: Running
2. Recompile: `$ npm run recompile` (complete once Ganache is running)
3. Start: `$ npm run start` (after recompile completes)
4. MetaMask: Chrome addon installed and connected to `localhost:8545`
5. Import 3 accounts from `localhost:8545` either by private key or JSON file

**How To**
1. Open a browser and go to `http://localhost:3000`.
2. Select an account from MetaMask.
3. Log in and select an account from the dropdown.
4. Update the profile to either requester or verifier from the profile screen in the top right dropdown menu.
5. Requester submits documents for verification.
6. Verifier verifies documents.
7. Once logged in, documents will be visible in the menu.
8. Click on the documents to view the document counts screen.
9. Verify documents from the verifier account.
10. Add documents from the requester account.

### Integration and Deployment

The smart contracts are designed to work together seamlessly, enabling a robust verification system on the blockchain. Follow the standard procedures for compiling, deploying, and interacting with these contracts using tools like Truffle or Hardhat.

### Usage

1. **Compile and Deploy Contracts:**
   - Use a development framework like Truffle to compile and deploy the contracts to your preferred blockchain network.

2. **Register Accounts:**
   - Users can register as verifiers or requesters by calling the `register` function in the `Accounts.sol` contract.

3. **Add Documents:**
   - Requesters can add documents for verification by calling the `addDocument` function in the `Documents.sol` contract.

4. **Verify Documents:**
   - Verifiers can verify or reject documents by calling the `verifyDocument` function in the `Documents.sol` contract.

5. **Retrieve Information:**
   - Use the provided functions to retrieve account and document details, as well as counts of verified and rejected documents.

## Unit Test Coverage
**TestSimpleStorage**
- `✓ testItStoresAValue (66ms)`

**Contract: Accounts**
- `✓ ...should register a valid verifier information. (316ms)`
- `✓ ...should not register with invalid email address. (64ms)`
- `✓ ...should register another valid verifier information. (254ms)`
- `✓ ...should register a valid requester information. (190ms)`
- `✓ ...should register another valid requester information. (236ms)`

**Contract: Documents**
- `✓ ...should add a document and mark as verified for requester. (439ms)`
- `✓ ...should add another document and mark as rejected from verifier. (444ms)`

**Contract: SimpleStorage**
- `✓ ...should store the value 89. (44ms)`

**9 passing (3s)**

## Contact
For more inquiries and conversations, feel free to contact me at [barath-sk17@github.com](mailto:barath-sk17@github.com).

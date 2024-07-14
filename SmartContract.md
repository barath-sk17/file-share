## Smart Contracts Overview

### Accounts.sol

The `Accounts.sol` contract manages user accounts, including verifiers and requesters. It allows users to register with their details and ensures email validity using the `EmailRegex.sol` library.

- **Key Features:**
  - Register user accounts with details such as name, email, logo, and description.
  - Validate email addresses using a regular expression.
  - Manage and store account types (verifier/requester) and their verification prices.
  - Maintain a list of verifiers and retrieve their details.
  - Self-destruct function to terminate the contract.

### Documents.sol

The `Documents.sol` contract handles the submission and verification of documents. It integrates with the `Accounts.sol` contract to verify document requests and ensure appropriate payments.

- **Key Features:**
  - Add documents with details such as name, description, and document address.
  - Ensure document addresses are unique.
  - Handle payments and refunds for document verification.
  - Retrieve document details and their status.
  - Verify and update document status (Pending, Verified, Rejected).
  - Maintain counts of verified, rejected, and total documents for each user.
  - Self-destruct function to terminate the contract.

### EmailRegex.sol

The `EmailRegex.sol` library provides a state machine-based approach to validate email addresses. It defines a series of states and transitions to check the validity of email strings.

- **Key Features:**
  - State machine implementation for email validation.
  - Function to check if an email string matches the regex.

### StringUtils.sol

The `StringUtils.sol` library offers utility functions for string comparisons.

- **Key Features:**
  - Compare two strings lexicographically.
  - Check equality of two strings.

### Migrations.sol

The `Migrations.sol` contract helps manage the deployment of other contracts. It tracks the last completed migration and supports upgrading to new contract addresses.

- **Key Features:**
  - Track the last completed migration step.
  - Upgrade to a new migration contract address.

### SimpleStorage.sol

The `SimpleStorage.sol` contract is a basic example of a storage contract.

- **Key Features:**
  - Store and retrieve a single unsigned integer value.

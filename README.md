
# ERC20 and Vault Contracts on Avalanche Subnet

## Overview
This project demonstrates the deployment of an **ERC20 token contract** and a **Vault contract** on a custom EVM subnet built on the Avalanche network. These contracts form the foundational components of a DeFi ecosystem, enabling token minting, burning, transfers, and a secure mechanism for deposits and withdrawals.

## Key Features
### ERC20 Contract
- Implements a standard ERC20 token with the following functionality:
  - **Minting and Burning**: Create or destroy tokens.
  - **Transfers**: Send tokens between accounts.
  - **Approval and Allowance**: Authorize third-party accounts to transfer tokens.
- Token Details:
  - Name: *Solidity by Example*
  - Symbol: *SOLBYEX*
  - Decimals: *18*

### Vault Contract
- Allows users to deposit ERC20 tokens in exchange for shares and withdraw tokens by burning shares.
- Implements a formula-based system to determine shares for deposits and withdrawals, ensuring proportional ownership.

## Tools and Technologies
- **Avalanche CLI**: For creating and deploying a custom EVM subnet.
- **Remix**: For writing and deploying smart contracts.
- **Metamask**: To connect to the Avalanche network and interact with the deployed contracts.
- **Solidity**: For contract development.

## Prerequisites
- A Unix-based system (macOS/Linux) or Windows with a Unix shell.
- Installed tools: Avalanche CLI, Metamask, and a web browser.

## Project Setup
1. **Subnet Creation**:
   - Use the Avalanche CLI to create a custom EVM subnet.
   - Define the native currency and configure the subnet parameters.

2. **Connect to Metamask**:
   - Add the subnet's RPC URL to Metamask.
   - Ensure the custom network is selected.

3. **Contract Deployment**:
   - Open Remix and connect it to Metamask using the Injected Provider.
   - Deploy the `ERC20` and `Vault` contracts.

4. **Testing**:
   - Use Remix to interact with the deployed contracts.
   - Test ERC20 token minting, transfers, and Vault contract deposits/withdrawals.

## How It Works
### ERC20 Token Contract
1. **Mint Tokens**:
   ```solidity
   function mint(uint amount) external;
   ```
   Mints new tokens to the caller's account.

2. **Transfer Tokens**:
   ```solidity
   function transfer(address recipient, uint amount) external returns (bool);
   ```
   Transfers tokens to another account.

3. **Burn Tokens**:
   ```solidity
   function burn(uint amount) external;
   ```
   Destroys tokens from the caller's account.

### Vault Contract
1. **Deposit Tokens**:
   Users deposit ERC20 tokens to receive shares.
   ```solidity
   function deposit(uint _amount) external;
   ```

2. **Withdraw Tokens**:
   Users burn shares to withdraw a proportional amount of tokens.
   ```solidity
   function withdraw(uint _shares) external;
   ```

## Usage Example
1. Mint tokens to an account:
   ```solidity
   mint(1000);
   ```
2. Transfer tokens to another user:
   ```solidity
   transfer(recipientAddress, 500);
   ```
3. Deposit tokens into the Vault:
   ```solidity
   deposit(500);
   ```
4. Withdraw tokens from the Vault:
   ```solidity
   withdraw(250);
   ```

This README provides all essential details for understanding and replicating the project.

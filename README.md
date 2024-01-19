# Solidity Token Vault  and ERC 20

This repository contains two Solidity smart contracts: `Vault` and `ERC20`. These contracts facilitate the creation of a token vault and a basic ERC-20 token, respectively.

## ERC20 Token Contract (`ERC20.sol`)

The `ERC20` contract is a simple implementation of the ERC-20 standard. It allows users to create and manage their own fungible tokens on the Ethereum blockchain. Here are some key features:

- **Name:** Tharun reddy
- **Symbol:** TR
- **Decimals:** 18

### Functions:

1. **Transfer:**
   - Transfers a specified amount of tokens from the sender's account to the recipient's account.
   ```solidity
   function transfer(address recipient, uint amount) external returns (bool);
   ```

2. **Approve:**
   - Allows the owner to approve a spender to spend a certain amount of tokens on their behalf.
   ```solidity
   function approve(address spender, uint amount) external returns (bool);
   ```

3. **Transfer From:**
   - Transfers a specified amount of tokens from the owner's account to the recipient's account, with approval.
   ```solidity
   function transferFrom(address sender, address recipient, uint amount) external returns (bool);
   ```

4. **Mint:**
   - Allows the owner to mint new tokens.
   ```solidity
   function mint(uint amount) external;
   ```

5. **Burn:**
   - Allows the owner to burn a specified amount of tokens.
   ```solidity
   function burn(uint amount) external;
   ```

## Token Vault Contract (`Vault.sol`)

The `Vault` contract is designed to act as a secure vault for holding ERC-20 tokens. Users can deposit and withdraw tokens, and the contract automatically manages the issuance and burning of vault shares.

### Functions:

1. **Deposit:**
   - Allows users to deposit ERC-20 tokens into the vault, receiving vault shares in return.
   ```solidity
   function deposit(uint amount) external;
   ```

2. **Withdraw:**
   - Allows users to withdraw tokens from the vault by providing vault shares.
   ```solidity
   function withdraw(uint shares) external;
   ```

## Usage:

1. Deploy the `ERC20` contract to create a new ERC-20 token.
2. Deploy the `Vault` contract, passing the address of the ERC-20 token to the constructor.
3. Interact with the ERC-20 token and Vault contracts using standard ERC-20 functions and the custom functions defined in the `Vault` contract.

## Author

Tharun DS

tharunreddy.8573@gmail.com

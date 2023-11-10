# SimpleToken Smart Contract

This Solidity smart contract, `SimpleToken`, is a basic ERC-20-like token for Ethereum. It enables token transfers, minting, and burning.

## Overview

- **Token Details:**
  - Name: SimpleToken
  - Symbol: ST
  - Decimals: 16
  - Initial Supply: Configurable during deployment

- **Functions:**
  - `transfer`: Transfer tokens between addresses.
  - `mint`: Create new tokens and assign them to an address.
  - `burn`: Destroy a specified amount of tokens.

## Usage

1. **Deploy the Contract:**
   - Deploy the `SimpleToken` contract on an Ethereum blockchain.

2. **Interact with the Contract:**
   - Use Remix, Truffle, or a wallet like MetaMask for interaction.

## Example Interaction Script

```solidity
// Deploy SimpleToken
SimpleToken myToken = new SimpleToken("SimpleToken", "ST", 1000000);

// Display initial balances
uint256 initialBalanceSender = myToken.balanceOf(msg.sender);

// Transfer tokens to another address
address recipient = 0x123...; // Replace with a valid Ethereum address
uint256 transferAmount = 500;
myToken.transfer(recipient, transferAmount);

// Mint new tokens
uint256 mintAmount = 200;
myToken.mint(msg.sender, mintAmount);

// Burn tokens
uint256 burnAmount = 100;
myToken.burn(burnAmount);
```

## License
This code is licensed under the MIT License. See the LICENSE file for details.

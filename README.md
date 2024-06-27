# Module 1 Function Error

This Solidity smart contract, named MyToken, implements a basic ERC20-like token with additional functionalities such as owner-specific operations and token burning.

## Overview

The contract includes the following features:

- **Owner Operations**: Owner-specific operations protected by a modifier.
- **Token Structure**: Defines a token structure (`Token`) with attributes such as name, abbreviation, and total supply.
- **Balance Management**: Tracks token balances of addresses using a private mapping.
- **Constructor Initialization**: Sets initial values upon contract deployment, including owner-related variables and token details.

## Functionality

### Constructor

Upon deployment (`constructor`), the contract initializes with:
- An `ownerCode` set to 500.
- `coin` structure initialized with name ("MarielleFE"), abbreviation ("MrllFE"), and an initial `totalSupply` of 1000 tokens, all allocated to the contract deployer.

### Token Structure

The `Token` struct defines attributes:
- `name`: Full name of the token.
- `abbrv`: Abbreviated name of the token.
- `totalSupply`: Total supply of tokens.

### Owner Operations

- **isOwner Modifier**: Restricts access to functions based on the caller being the contract owner.
- **getCode**: Public function to retrieve the current `ownerCode`.
- **addToOwnerCode**: Public function to modify the `ownerCode`, restricted to the contract owner.

### Burn Function

- **burn**: Allows token holders to burn (destroy) a specified amount of their tokens, reducing both their balance and the total token supply. It also modifies the `ownerCode` accordingly.

## Usage

1. **Deploying the Contract**: Deploy the contract on a supported Ethereum environment such as Remix IDE (remix.ethereum.org).
2. **Interacting with the Contract**: Use functions like `getCode`, `addToOwnerCode`, and `burn` to manage tokens and perform owner-specific operations.

## Development Environment

This contract was developed and tested using Remix IDE (remix.ethereum.org).

## Author

Marielle Romana

NTC EMAIL: 421000169@ntc.edu.ph

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.

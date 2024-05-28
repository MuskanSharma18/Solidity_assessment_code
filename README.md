# MyToken

This Solidity contract is a basic implementation of an ERC-20 token. It provides functionality for creating and destroying tokens, as well as storing additional information about the token.

## Description

The MyToken contract allows users to mint and burn tokens, managing the total supply and individual balances. It includes features to store the token name, abbreviation, and total supply. The contract also ensures that tokens can only be burned if the sender has a sufficient balance.

## Getting Started

### Installing

To use this contract, you need a development environment capable of deploying Solidity contracts, such as Remix IDE or Truffle Suite.

1. **Download or clone the repository**:
   ```sh
   git clone <https://github.com/MuskanSharma18/Solidity_assessment_code>
   ```
2. **Open the contract in Remix IDE**:
   - Go to [Remix IDE](https://remix.ethereum.org/)
   - Create a new file and paste the contract code into it.

### Executing Program

To deploy and interact with the MyToken contract, follow these steps:

1. **Compile the contract**:
   - Open Remix IDE and select the Solidity compiler version `0.8.18`.
   - Compile the contract by clicking on the "Compile MyToken.sol" button.
   - 
2. **Deploy the contract**:
   - Go to the "Deploy & Run Transactions" tab.
   - Select "MyToken" from the contract dropdown.
   - Click "Deploy" and confirm the transaction in MetaMask.

3. **Interact with the contract**:
   - After deployment, you can call the contract functions using the deployed contract instance.

   - **Mint tokens**:
     ```solidity
     function mint(address _address, uint _value) public
     ```
     Example:
     ```sh
     MyToken.mint("0xYourAddress", 100)
     ```
   
   - **Burn tokens**:
     ```solidity
     function burn(address _address, uint _value) public
     ```
     Example:
     ```sh
     MyToken.burn("0xYourAddress", 50)
     ```

## Requirements

1. The contract has public variables that store the details about the coin:
   - `tokenName`: It is a string that serves as the name of the token.
   - `abbr`: A string which represents the abbreviation of the token.
   - `totalSupply`: An unsigned integer which represents the total supply of the token.

2. The contract has a mapping of addresses to balances:
   - `balances`: The contract includes a mapping called "balances" that links addresses to their respective token balances.

3. The contract has a `mint` function that increases the total supply and the balance of the "sender" address by a given value:
   - Parameters:
     - `_address`: The address to which the tokens will be minted.
     - `_value`: The amount of tokens to be minted.
   - Actions:
     - Increase the `totalSupply` by `_value`.
     - Increase the balance of the `_address` by `_value`.

4. The contract has a `burn` function that decreases the total supply by subtracting the mint value from balance value.
   - Parameters:
     - `_address`: The address from which the tokens will be burned.
     - `_value`: The amount of tokens to be burned.
   - Actions:
     - Check if the balance of the `_address` is greater than or equal to `_value`.
     - If true, decrease the `totalSupply` by `_value`.
     - Decrease the balance of the `_address` by `_value`.

## Deploying the code

1. Deploy the `MyToken` contract to a supported Ethereum network.

2. Once deployed, you can interact with the contract by calling the following functions:

   - `mint`: Creates new tokens and assigns them to a specified address.
     - Parameters:
       - `_address`: The address to which the tokens will be minted.
       - `_value`: The amount of tokens to be minted.

   - `burn`: Destroys existing tokens by reducing the total supply and the balance of a specified address.
     - Parameters:
       - `_address`: The address from which the tokens will be burned.
       - `_value`: The amount of tokens to be burned.
  ## Help

For common issues or questions:

- **Ensure you have sufficient gas for transactions**: Always check your gas limit and gas price.
- **Check contract address**: Make sure you interact with the correct deployed contract address.
- **MetaMask issues**: If MetaMask is not connecting or confirming transactions, try restarting your browser or re-logging into MetaMask.

For further assistance:
```sh
help <command>
```

## Authors

Muskan

- GitHub: [Muskan](https://github.com/MuskanSharma18)

## License

This contract is licensed under the MIT License. SPDX-License-Identifier: MIT.




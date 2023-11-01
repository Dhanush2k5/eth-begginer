Project Title

Simple Ethereum Token (MyToken) Smart Contract

Description:

This Solidity smart contract, named "MyToken," is designed to create and manage a basic Ethereum token. It provides the functionality to mint new tokens and burn existing tokens. The contract includes the following features:

Public variables to store token details, including the token name, token symbol (abbreviation), and the total supply of tokens.

A mapping that associates Ethereum addresses with their token balances, allowing users to check their balances.

A mint function (mintT) that allows the contract owner to create new tokens. It takes an address and a value as parameters and increases the total supply by that value while also increasing the balance of the specified address by the same amount.

A burn function (burnT) that allows the contract owner to destroy tokens. Like the mint function, it takes an address and a value as parameters. It deducts the specified value from the total supply and reduces the balance of the specified address by the same amount.

The burn function includes a conditional check to ensure that the balance of the specified address is greater than or equal to the amount that is supposed to be burned. If the balance is insufficient, it will not allow the burning operation to proceed.

Getting Started:

Installing
To use this smart contract, you need access to a development environment for Ethereum smart contracts. Here's a basic outline of how to set up your development environment:

Install a Solidity compiler, such as Solidity, on your system.

Use a development environment like Remix or an integrated development environment (IDE) like Truffle to write, compile, and deploy the smart contract.

You may need to install a wallet, such as MetaMask, to interact with the smart contract on the Ethereum network.

Executing program
Write or copy the smart contract code into your development environment.

Compile the smart contract code using the Solidity compiler.

Deploy the smart contract to the Ethereum network using your chosen development environment.

Once deployed, you can interact with the smart contract using its functions, such as minting and burning tokens.

Help:

If you encounter common issues or need further assistance, consider consulting the official documentation for Solidity, Remix, and other Ethereum development tools. Additionally, you can reach out to the Ethereum development community for support and guidance.

Authors:
Dhanush
rsadhanush@gmail.com

License:
This project is licensed under the MIT License. See the LICENSE.md file for details.

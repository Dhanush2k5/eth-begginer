Project Title

MyToken - A Simple Ethereum Token Contract

Description

MyToken is a Solidity smart contract that implements a basic cryptocurrency token on the Ethereum blockchain. The contract includes the following features:

Public variables to store the token's name, symbol (abbreviation), and total supply.
A mapping of Ethereum addresses to token balances.
A mint function that allows the creation of new tokens by increasing the total supply and the balance of a specified address.
A burn function that allows the destruction of tokens by reducing the total supply and the balance of a specified address. This function checks if the sender has a sufficient balance to burn the requested amount.

Getting Started

Installing
To use the MyToken contract, follow these steps:

Create a new Solidity smart contract file (e.g., MyToken.sol).
Copy and paste the code from the provided MyToken contract into your Solidity file.
Executing program
To deploy and interact with the MyToken contract, you will need to use Ethereum development tools like Remix or Truffle. Here are some basic steps for interacting with the contract:

Compile the contract: Use a Solidity compiler to compile your smart contract source code. Remix is an online Solidity IDE that can help with compilation.

Deploy the contract: Deploy the compiled contract to the Ethereum blockchain using tools like Remix, Truffle, or Ethereum development frameworks. You'll need to specify the initial values for the token name, symbol, and total supply.

Interact with the contract: After deployment, you can interact with the contract using Ethereum wallets, Ethereum JavaScript libraries (such as web3.js or ethers.js), or by sending transactions directly from Remix. Use the mintT and burnT functions to mint and burn tokens.

Here's an example of how to mint tokens using web3.js:

javascript
Copy code
const Web3 = require('web3');
const web3 = new Web3('YOUR_ETHEREUM_NODE_URL');

// Replace these with your contract's address and ABI
const contractAddress = 'YOUR_CONTRACT_ADDRESS';
const contractABI = [YOUR_CONTRACT_ABI];

const contract = new web3.eth.Contract(contractABI, contractAddress);

// Mint tokens
const account = 'YOUR_ACCOUNT_ADDRESS';
const amountToMint = 100; // The amount you want to mint
contract.methods.mintT(account, amountToMint).send({ from: account })
  .on('receipt', (receipt) => {
    console.log('Tokens minted successfully!');
  })
  .on('error', (error) => {
    console.error('Error minting tokens:', error);
  });

// Burn tokens
const amountToBurn = 50; // The amount you want to burn
contract.methods.burnT(account, amountToBurn).send({ from: account })
  .on('receipt', (receipt) => {
    console.log('Tokens burned successfully!');
  })
  .on('error', (error) => {
    console.error('Error burning tokens:', error);
  });
  
Help
If you encounter any issues or have questions about using the MyToken contract, please refer to Ethereum development documentation or community forums for assistance.

Authors
This smart contract was created by
dhanush
rsadhanush@gmail.com

License
This project is licensed under the MIT License. See the LICENSE.md file for details.

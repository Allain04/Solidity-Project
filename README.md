**MyToken Smart Contract**

**Overview
MyToken is a simple Ethereum-based token implemented using Solidity. This contract allows for the minting and burning of tokens, managing the total supply and balances of tokens for each address. It demonstrates basic principles of token creation and destruction on the Ethereum blockchain.**

**Contract Details**
Prerequisites
Solidity version: >=0.6.12 <0.9.0
SPDX License: MIT


**Public Variables**
tokenName: A string representing the name of the token (e.g., "Caratdeul").
tokenAbbrv: A string representing the abbreviation of the token (e.g., "CRTDL").
totalSupply: A uint representing the total supply of tokens.


**Mapping**
balances: A mapping from addresses to unsigned integers (uint). It keeps track of the token balance for each address.


**Functions**

**mint**
Description: Mints new tokens and assigns them to a specified address.
Parameters:
_address (address): The address to which the newly minted tokens will be assigned.
_value (uint): The number of tokens to be minted.
Behavior:
Increases the totalSupply by _value.
Increases the balance of _address by _value.

**burn**
Description: Burns tokens from a specified address.
Parameters:
_address (address): The address from which tokens will be burned.
_value (uint): The number of tokens to be burned.
Behavior:
Checks if the balance of _address is at least _value. If not, the transaction is reverted with the message "Insufficient balance to burn".
Decreases the totalSupply by _value.
Decreases the balance of _address by _value.


**Usage**
Deploying the Contract
Install Solidity: Make sure you have the Solidity compiler installed. You can use Remix IDE, Truffle, or Hardhat to compile and deploy the contract.

Compile the Contract: Ensure your Solidity compiler version is compatible (>=0.6.12 <0.9.0).

Deploy the Contract: Use your preferred method to deploy the contract to the Ethereum blockchain. You will interact with the contract's functions to mint and burn tokens.

**Interacting with the Contract**

Minting Tokens: Call the mint function with the address to receive tokens and the number of tokens to be minted.


Burning Tokens: Call the burn function with the address from which tokens will be burned and the number of tokens to be burned.

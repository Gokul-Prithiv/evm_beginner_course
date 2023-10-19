# MyToken Smart Contract

The MyToken smart contract is a basic Ethereum token contract that allows for the creation and management of a custom cryptocurrency. This contract implements the basic functionalities of minting and burning tokens, with necessary checks to ensure the proper functioning of these operations.

## Contract Details

### Token Information

- **Token Name**: GOKUL
- **Token Abbreviation**: GK
- **Total Supply**: 0 (Initial total supply, can be increased using the mint function)

### Balances

The contract maintains a mapping of Ethereum addresses to token balances. Users can hold and transfer tokens by interacting with this mapping.

### Mint Function

The `mint` function allows the creation of new tokens. It takes two parameters:

- `address`: The Ethereum address to which the newly created tokens will be assigned.
- `value`: The number of tokens to be created.

The function increases the total supply by the specified value and increments the balance of the specified address accordingly.

### Burn Function

The `burn` function allows the destruction of tokens. It takes two parameters:

- `address`: The Ethereum address from which tokens will be burned.
- `value`: The number of tokens to be burned.

The function works in the opposite way to the `mint` function. It deducts the specified value from the total supply and decreases the balance of the specified address.

The `burn` function includes a conditional check to ensure that the balance of the specified address is greater than or equal to the amount that is supposed to be burned. This is done to prevent burning more tokens than are available in the sender's balance.

## Usage

This smart contract can be deployed on the Ethereum blockchain, and it allows you to create and manage custom tokens. Here's how you can use it:

1. **Deploy the Contract**: Deploy the `MyToken` smart contract to the Ethereum blockchain.

2. **Mint Tokens**: To create new tokens, call the `mint` function by specifying the recipient's address and the number of tokens to be minted.

   ```solidity
   function mint(address _address, uint _value) public {
       // Add address and value to mint new tokens
   }
   
3. **Burn Tokens**: To destroy tokens, call the burn function by specifying the sender's address and the number of tokens to be burned. The function will verify if the sender has a sufficient balance before burning.

   ```solidity
   function burn(address _address, uint _value) public {
    // Add address and value to burn tokens
   }

### Author
Gokul Prithiv

# ETH-proof-solidity
Overview
MyToken is a simple smart contract implemented in Solidity for managing a token named "Republic credits" (RC). This contract includes basic functionalities such as minting new tokens and burning existing tokens.

Contract Details
Token Name: Republic credits
Token Abbreviation: RC
Total Supply: Initially set to 0
Public Variables
The contract defines the following public state variables:

string public Token_Name: The name of the token.
string public Token_Abbrv: The abbreviation of the token.
uint public Total_Supply: The total supply of the token.
Mapping
mapping(address => uint) public Balance: A mapping to keep track of the balance of tokens held by each address.
Functions
Mint Function
function Mint(address _Space, uint _Capacity) public

The Mint function increases the total supply of tokens and adds the specified amount of tokens to the balance of the provided address.

Parameters:
_Space: The address to which the tokens will be minted.
_Capacity: The amount of tokens to mint.
Behavior:
Increases the Total_Supply by _Capacity.
Increases the balance of _Space by _Capacity.

Burn Function
function Burn(address _Space, uint _Capacity) public
The Burn function decreases the total supply of tokens and deducts the specified amount of tokens from the balance of the provided address. It ensures that the address has enough tokens to burn.

Parameters:
_Space: The address from which the tokens will be burned.
_Capacity: The amount of tokens to burn.
Behavior:
Checks if the balance of _Space is greater than or equal to _Capacity.
If the check passes, decreases the Total_Supply by _Capacity.
Decreases the balance of _Space by _Capacity.

Usage
Deploy the Contract: Deploy the MyToken contract to the Ethereum blockchain.
Mint Tokens: Use the Mint function to add new tokens to an address.
Burn Tokens: Use the Burn function to remove tokens from an address, ensuring the address has sufficient balance.

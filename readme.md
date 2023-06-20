Metacrafters Project: Create a Token

Description:
--------------------
This program was written in Solidity, which is a programming language that is used to develop smart contracts in the Ethereum Blockchain. It aims to garner the ability to mint and burn tokens to a desired amount by the inputted value of the user. 

Getting Started:
--------------------
This program aims to have the ability to mint and burn tokens.

// mint function
function mint (address _address, uint _value) {
    totalSupply += _value;
    balances[_address] += _value;
}

// burn function
function burn (address _address, uint _value) {
  if (balances[_address] >= _value){
    totalSupply -= _value;
    balances[_address] -= _value;
  }
}

The user can check whether tokens are minted/burned by running the TotalSupply function. It also has a conditional that checks whether the tokens intended to be burned is less than the amount of tokens in the supply. 

if (balances[_address] >= _value){
  totalSupply -= _value;
  balances[_address] -= _value;
}

If the conditional satisfied is otherwise, it would ignore the burn function call. 

Author:
--------------------
Jan Anonuevo

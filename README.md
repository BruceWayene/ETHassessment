# Token Functionalities
This Solidity program is a simple "Token Functionality " program that demonstrates the basic syntax and functionality of the Solidity programming language. 

# Description

This code defines a token contract named MyToken with basic functionalities for minting and burning tokens.
It also stores information about the token's name, abbreviation, total supply, and individual token balances.
This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a 
stepping stone for more complex projects in the future.

## Getting Started

## Executing Program
To run this program, we have used Remix, an online Solidity IDE. 

The Remix website, we created a new file by clicking on the "+" icon 
in the left-hand sidebar and saved the file with a .sol extension 

// SPDX-License-Identifier: MIT
pragma solidity 0.8.27;

contract MyToken {
    string public tokenName = "Fujjyu";
    string public tokenAbbrv = "FJY";
    uint public totalSupply = 0;

    mapping(address => uint) public balances;

    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    function burn(address _address, uint _value) public {
        require(balances[_address] >= _value, "Insufficient balance");
        totalSupply -= _value;
        balances[_address] -=_value;
    }
    }
## Author
Lokesh Dutta

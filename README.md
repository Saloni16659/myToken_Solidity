# Creating Token

Creating a simple token using Solidity

## Description

1. Basics of Solidity
2. Introduction to DataTypes
3. Creating Functions 
4. Mapping in solidity

## Getting Started

### Installing

* You can use a online Ethereum IDE, here in this code Remix is being used.

### Executing program

* Go to the Remix Ethereum IDE (remix.ethereum.org)
* Create a new file with any suitable name with (.sol) extension
* Write the desired code in the main screen
* Now, compile your file using solidity compiler
* After complining just deploy it get the desired output.
* Create a contract and in it specify the variables and functions.
* Copy the following code and execute in a Ethereum IDE
``` Solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.26;

contract MyToken {

    // public variables here
    string public tokenName = "SALONI GUPTA";
    string public tokenAbbrv = "SG";
    uint public totalSupply = 0;
    
    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value){
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }

}


```

## Help

For any issue with the code take help of debug option.

### Authors

Saloni Gupta
[salonig16659@gmail.com]
7404580278

## License

This project is licensed under the MIT License - see the LICENSE.md file for details


 ETHERIUM BEGINNER MODULE

The module is given to us to teach us the fundamentals of creating a block chain

 Description

This program aims to help us understand the basics and also to give us a knowledge about 
block chain

 Getting Started
 To be able to execute this application, you may use Remix, an online Solidity IDE, which can be found at https://remix.ethereum.org/.

 Create a new file on the Remix website by clicking the "+" symbol in the left-hand sidebar. Save the file as Phoenixtoken.sol . Insert the following code into the file:
 // SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {
    
    // public variables here
    string public tokenName = "Phoenix";
    string public tokenAbbrv = "Phnx";
    uint256 public totalSupply = 0;


    // mapping variables here
    mapping(address => uint256) public balances;

    // mint function
    function mint(address _address, uint256 _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint256 _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}



Authors
Jorge ramiscal
@JRamiscal

Contributors names and contact info

Ramiscal Jorge
[@Jay2kkkk](https://twitter.com/Jay2kkkk)


## License

This project is licensed under the Ramiscal Jorge License - see the LICENSE.md file for details

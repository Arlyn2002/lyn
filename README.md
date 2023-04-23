# MyToken

The "MyToken" project in Solidity exemplifies the programming language's key syntax and functionality. The purpose of this project is to provide a starting point for people who are unfamiliar with Solidity.

## Description

This software is a simple contract written in Solidity, a programming language for generating smart contracts for the Ethereum network. A single function in the contract returns the string "MyToken"

## Getting Started

### Executing Program

To run this project, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyToken {
    // public variables here
string public TokenName = "Coin";
string public TokenAbbrv = "Eth";
uint public  TotalSupply = 0;

    /// mapping variable here
    mapping(address => uint) public balances;
     
// mint function
    function mint (address _address, uint _value) public {
       TotalSupply += _value;
       balances[_address] += _value;
    }
    
// burn function
    function burn (address _address, uint _value) public {
       if (balances[_address] >= _value) {
          TotalSupply -= _value;
          balances[_address] -= _value;
       }
    }
}
```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile my token.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

## Authors

NTCIAN ARLYN
<br> 
[Discord: @Arlyn]
( https://discordapp.com/users/Arlyn#7306)
## License

This project is licensed under the MIT License - see the LICENSE.md file for details

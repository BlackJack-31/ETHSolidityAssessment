# ETHSolidityAssessment

This Solidity program is a simple "MyToken" program that demonstrates the functionality of the Solidity programming language. The purpose of this program is to teach how to write contracts in Solidity and executing the transactions in a simulated environment serving as a simplified program for real world transactions.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. This MyToken contract  allows minting new coins, burning existing ones, and keeping track of balances through the address mapping. 

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT

pragma solidity 0.8.26;
contract MyToken {

    // public variables here
    string public tokenName = "Ether";
    string public tokenAbrv = "ETH";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address add, uint val) public {
        totalSupply += val;
        balances[add] += val;
    }

    // burn function
    function burn(address add, uint val) public {
        if (balances[add] >= val){
        totalSupply -= val;
        balances[add] -= val;
        }
    }

}
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.26" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by adding coins(val) into the mint function and using the existing coins by executing the burn function. 
The totalSupply variable shall store all the available coins. Hence completing the minting and burning coins in the MyToken program

## Authors

Abhigyan Shrivastava


## License

This project is licensed under the MIT License - see the LICENSE.md file for details

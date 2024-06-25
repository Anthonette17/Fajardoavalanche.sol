# FajardoContract.sol
This smart contract leverages the OpenZeppelin ERC20 implementation to ensure security and compliance with the ERC20 standard while adding custom functionalities for a virtual shop.
  
# Description
This Solidity code defines a smart contract named CustomToken, which is an ERC20 token with additional functionalities for managing virtual products. The contract uses the OpenZeppelin library for standardized implementations of ERC20 tokens and ownership features. 
  
# Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract CustomToken is ERC20, Ownable {

    mapping(uint256 => uint256) public productPrices;
    mapping(address => uint256) public userPurchases;

    constructor() ERC20("CustomToken", "CTK") Ownable(msg.sender) {
        productPrices[101] = 500;
        productPrices[102] = 300;
        productPrices[103] = 200;
        productPrices[104] = 100;
    }


## Authors

Metacrafter Anthonette

## License
This project is licensed under the MIT License - see the LICENSE.md file for details
    

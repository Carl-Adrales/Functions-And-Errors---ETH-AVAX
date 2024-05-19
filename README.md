# Functions And Errors - ETH + AVAX
    This program is a smart contract that implements the require(), assert() and revert() statements.

## Description
    Hi everyone, my name is Carl from bsit3.4. In this video, I will be discussing functions and errors 
    in Solidity using a trivial and avalanche. I will explain how to insert coins, double the bet, and 
    withdraw coins. I will also guide you through deploying the project.
    
## Getting Started
```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract BettingGame {
    uint256 public coin;

    function insertCoin(uint256 _coin) public {
    require(_coin > 0, "Insert a coin");
    coin = _coin; 
    assert(coin == _coin);

    }

    function betTwice() public {
        require(coin > 0 && coin % 2 == 0, "You have to insert coin to bet twice.");
        coin *= 2;

    }

    function withdraw() public {
    if (coin == 0) {
        revert("No coins to withdraw.");
    }
    coin = 0;

    }
}
```
## Executing Program 
    To run this program, you can use Remix, an online Solidity IDE. To get started, go to the 
    Remix website at https://remix.ethereum.org/. Once you are on the Remix website, create a 
    new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension 
    (e.g., HelloWorld.sol). Then copy the code given in the assessment.

## Author 
    Carl Jasper M. Adrales
    8214773@ntc.edu.ph

## License
     This project is licensed under the MIT License - see the LICENSE file for details


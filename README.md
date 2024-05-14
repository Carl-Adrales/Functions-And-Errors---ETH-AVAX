# Functions And Errors - ETH + AVAX
    This program is a smart contract that implements the require(), assert() and revert() statements.

## Description
    Hi everyone, my name is Carl. I will be discussing functions and error using ETH + AVAX. I will explain how to define functions and errors in your contract, declare variables, and create public functions that set and check values. I will also demonstrate how to compile, deploy, and run transactions using the Solidity compiler.

## Getting Started
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract FunctionsAndErrors {
    uint256 public value;

    // Sets the value if the input is positive
    function setValue(uint256 _value) public {
        // Ensure the value is non-zero
        require(_value > 0, "Value must be positive");
        value = _value;
    }

    // Doubles the value if the current value is even
    function doubleValue() public {
        // Ensure the value is even
        require(value % 2 == 0, "Value must be even to double");
        value *= 2;
    }

    // Asserts that the value is positive
    function checkValue() public view {
        // Assert the value is greater than zero
        assert(value > 0);
    }

    // Resets the value to zero and reverts if the value is not zero
    function resetValue() public {
        if (value == 0) {
            // Revert with a custom error message
            revert("Value is already zero");
        }
        value = 0;
    }
}

## Executing Program 
    To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/. Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Then copy the code given in the assessment.

## Author 
    Carl Jasper M. Adrales
    8214773@ntc.edu.ph

## License
     This project is licensed under the MIT License - see the LICENSE file for details


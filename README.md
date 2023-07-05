# Solidity-Assessment-Metacrafters

This Solidity project is the final one to demonstrate code that generates a basic token contract. This will give Solidity beginners a quick overview of the procedures for creating tokens, minting token, burning tokens, and checking balances and its total supply.

## Description

Solidity is a programming language that is used to create smart contracts that operate on the Ethereum Virtual Machine. This project requires the creation of a contract that can be used to generate tokens with two variables: public variables that hold coin information and mapping variables that map addresses to balances. Then there are two functions: the mint function, which increases the total supply by that number and increases the address's balance by that amount, and the burn function, which operates in the opposite direction by destroying tokens. Conditionals are used in burn functions to ensure that the balance is more than or equal to the amount that is scheduled to be burned.


## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Token.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "TRIXIE";
    string public tokenAbbrv = "RIRI";
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
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}


## Compile the code

Click the "Solidity Compiler" tab in the left-hand sidebar to compile the code. Following that, click the "Compile Token.sol" button, then compile code, and wait for the green check to show in the "Solidity Compiler" logo. After the code has been compiled, you may deploy the contract using the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Token.sol" contract from the drop-down menu, then click the "Deploy" button. When the contract is ready for usage, expand the Deployed Contracts section below the URL to interact with it. Expanding your deployed contract is as simple as pressing the arrow button on the left side. You are now able to interact with the contract you created. Simply enter the relevant information, such as the address (just copy the account address), the token's value, and the quantity of tokens you want to mint, burn, and then transact, to make the modifications. Simply pick "balances" to test it.


## Author/s

Trixie Joy L. Mancao

# My Token
This simple Solidity Program is a Simple Token handling program where you can Mint, Burn, Check your token balance and check your current token supply.

# Description
This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a multiple function that allows the user to Create a token(Mint), Destroy a token(Burn), check your token balance under your address and Checking the current token supply. This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

# Getting Started
Executing program To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

    // SPDX-License-Identifier: MIT
    pragma solidity 0.8.18;

    contract MyToken {

    // public variables here
    string public tokenName = "Matt";
    string public tokenAbbrv = "Tyuuu";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
    }

  
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken - Name_Token.sol" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can utilize functions like mint, burn, token abbreviation (tokenAbbrv), token name (tokenName), and total supply (totalSupply). To begin, locate your address under "Deploy and run transactions" and copy it. Then, in the "Deployed/Unpinned Contracts" section, check the totalSupply function to confirm if your token supply starts at 0. This function works similarly to the balance function but requires the account address. Next, to transact tokens, call the mint function and paste your account address along with the desired value, such as minting at least 2000 tokens. After minting, verify the token balance using either totalSupply or Balance functions. For burning tokens, use the burn function to deduct tokens from the address. For instance, deducting 1000 tokens requires pasting the address and specifying the value as 500. Verify the deduction by checking the token supply or balance again.

# Author
- NTC PH Matthew D. Ocate
- @metacraftersio

# License 
This project is licensed under the MIT License - see the LICENSE.md file for details.

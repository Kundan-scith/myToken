# TESLA

This Solidity program serves as a concise demonstration of the fundamental syntax and functionality of the Solidity programming language, showcasing the creation of a token.

## Description

This contract, named "TESLA," is a basic implementation written in Solidity, a programming language designed for developing smart contracts on the Ethereum blockchain. The contract incorporates basic functionalities for creating and managing a token called "TESLA."

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol). Copy and paste the following code into the file:

```javascript
pragma solidity 0.8.18;

contract MyToken {
    string public tokenName = "TESLA";
    string public tokenAbbrev = "TS";
    uint public totalSupply = 0;

    mapping(address => uint) public balances;

    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    function burn (address _address, uint _value) public {
        if(balances[_address]>=_value){
        totalSupply -= _value;
        balances[_address] -= _value;
        }        
    }

}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile myToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "myToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract has been successfully deployed, navigate to the "Deployed Contracts" section and locate the contract named "MYTOKEN." Click on it to access the contract's details and available functions.

To initiate the minting process, locate and click on the "mint" function within the contract. In order to specify the target address for the minted tokens, retrieve the desired address from the "ADDRESS" field displayed above and copy it to your clipboard. Next, paste the copied address into the designated address section of the "mint" function.

After verifying that the address has been correctly entered, proceed to initiate the transaction by clicking on the "Transact" button. This will trigger the minting process, creating new tokens and assigning them to the specified address.

To examine the total supply of tokens, locate the "totalSupply" function within the contract interface and click on it. This will display the current total supply value.

Using the previously copied address, you have the ability to verify the total supply of tokens and check the balance associated with that address.

Additionally, should you wish to reduce the total supply of tokens by burning a specific value, look for the "burn" function within the contract. Specify the desired value to be burned and execute the transaction. This will deduct the specified amount from the total supply, effectively reducing it accordingly.

## Authors

Kundan kumar  
[@KundanKumarKPr1](https://twitter.com/KundanKumarKPr1)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details

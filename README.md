# Create-a-Token

This Solidity program is a simple "Create a Token" program that demonstrates the basic syntax and functionality of the Solidity programming language.


## Description
This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has 2 functions that will add or subtract the value of the token.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```javascript
pragma solidity 0.8.18;
contract MyToken {
    // public variables here
    string public tokenName = "Credits";
    string public tokenAbbrv = "Crd";
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
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile myToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by copying the Account Address in the Deploy & Run Transactions" tab then go to Deployed contracts click the drop down arrow for the mint and paste the copied address the add your value then click transact to add value for your token. To see if the token value the click the totalSupply below. then to subtract the totalSupply value then use the burn drop down arrow then paste the address then add your value then transact

## Authors
@Dracogray24


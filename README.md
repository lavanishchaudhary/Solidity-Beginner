# MyToken
The MyToken contract is a solidity smart contract that implements a basic token system. It provide functionalities to mint new tokens, burn existing tokens, and maintain balances of different addresses.
## Description
The code represents a Solidity smart contract for a token system. It includes functionalities to mint and burn tokens, while also maintaining public variables for token details (name, abbreviation, and total supply) and a mapping to track token balances for addresses.
### mint
```
function mint(address _address, uint _value) public {
       totalSupply += _value;
       balances[_address] += _value;
```
The `mint` function is used to create new tokens. It takes two parameters: `_address` (the address of the recipient) and `_value` (the number of tokens to be minted). The function increases the total supply by the specified value and increases the balance of the sender's address by the same amount.
### burn
```
function burn( address _address,uint _value) public {
       if( balances[_address] >= _value){
          totalSupply -= _value;
          balances[_address] -= _value;
       }
    }
```
The `burn` function is used to destroy tokens. It takes two parameters: `_address` (the address of the token holder) and `_value` (the number of tokens to be burned). The function checks if the balance of the sender's address is greater than or equal to the specified value. If the condition is met, it deducts the value from the total supply and decreases the balance of the sender's address by the same amount.
## Geting Started
### Executing program
__Step 1:__ Open your web browser and go to the Remix IDE website: https://remix.ethereum.org/.   

**Step 2:** Create a new file by clicking on the "+" icon. Save the file with extension `.sol`. Copy and paste the code into the editor.   

**Step 3:** In the Remix sidebar on the left, navigate to the "Solidity Compiler" tab. Click the "Compile" button to compile the contract. Ensure that there are no compilation errors displayed in the "Compile" tab.     

**Step 4:** Switch to the "Deploy & Run Transactions" tab in the Remix sidebar. Click the "Deploy" button to deploy the contract to the selected network. Confirm the deployment transaction in the pop-up window that appears.     

**Step 5:** Once the contract is deployed, you can interact with it by expanding the contract in the "Deployed Contracts" section. You will see the available functions such as `mint` and `burn`.    

**Step 6:** To `mint` new tokens, click on the mint function and provide the required parameters. To `burn` tokens, click on the burn function and provide the required parameters. You can view the state of the contract and the updated balances by accessing the public variables and the `balances` mapping. 
## Authors
Metacrafter Student   
[Lavanish Chaudhary](https://www.linkedin.com/in/lavanish-chaudhary/)
## License
This project is licensed under the MIT License.

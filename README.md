# assignment-
Description
This Solidity code represents a basic ERC20 token contract called "MyToken". The contract satisfies the following requirements:

It has public variables to store the details of the token, including the token name, token abbreviation, and total supply.
It includes a mapping that associates addresses with token balances.
The contract includes a mint function, which takes an address and a value as parameters. It increases the total supply by the given value and increases the balance of the specified address by that amount.
The contract includes a burn function that works in the opposite way of the mint function. It takes an address and a value as parameters and deducts the value from the total supply and the balance of the specified address.
The burn function includes conditionals to ensure that the balance of the "sender" (specified address) is greater than or equal to the amount that is supposed to be burned.


Getting Started
Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension. Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;



contract MyToken {

    // public variables here
    string public tokenName = "meta";
    string public tokenAbbrv = "mta";
    uint public totalSupply = 0;


    // mapping variable here
    mapping(address => uint) public balances;


    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }


    // burn function
    function burn(address _address, uint _value) public {
    if(balances[_address] >= _value) {
        totalSupply -= _value;
        balances[_address] -= _value;
    }
    }

}

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. 

So first line it is the comment, it specifies the license for the code to be written.

Second line it specifies the version of this already program. Next in line 18 we have a contract, this specifies the new type of the code.

So this is the new type called as my token. We have opened our contract here. Inside contract, we have declared three public variables namely token name, token abbreviation and total supply.

Total name and token name and token abbreviation is a string and total supply. So, this is the new type called as my token.

And we have mapping data structure. This data structure maps the addresses to the balances. That is, it stores the balances of each address of each token.

Next, we have mint function. In line 39, the mint function has two parameters. One is the address to which the values need to be added and value.

It is the amount of value to be added. Next, this is a public function. We have opened it here. It has two lines in line 32.

We are adding the number, we are adding the value to the total supply. In line 33, we are adding the value to the balances address.

Next, in line 38, we have burn function. This works similar to mint function, but instead of adding value, it subtracts the value.

It has two parameters that is address and value. It's a public function. Here, we have an extra condition. This condition checks whether there are no extra values.

Suppose if there are six values and we So, let's check it. Since we don't have extra function for this, we need to copy this address.

We'll copy this address. Let's select different address. Let's take this address and let's copy to clipboard. Let's check the balance of this first.

So, it has zero balance. This green tick indicates that it has been executed. So, let's mint something. It's the same address here.

Let's mint. Suppose 500 tokens. We have minted 500 tokens. So, let us check the balance now. The balance is 500.




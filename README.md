# Getting-started-with-solidity

In this project we are creating our own token.

# Description

In this project we are creating our token according to the requirements given on the basis of which we have to do the work.
We are gaining the great insight about the different datatypes and their use.
Firstly we have created the public variables. After that we have mapped the addresses to the balances, then we have implemented the main function. Another function that we have declared is the burn function. Lastly we have compiled and deployed the token.

# Getting Started

# Installing

You can simply use Online Etherium IDE for this purpose.

# Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
After that create a file and write your code.

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
   string public tokenName = "META";
   string public tokenAbbrv = "MTA";
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
         if(balances[_address] >= _value) {
         totalSupply -= _value;
         balances[_address] -= _value;
     }
     }
     

}

After that compile the code and then deply on the solidity online compiler.
Now test different variables created, in this case we can burn, mint our token.
Finally, we have created and Dubugged our own token.

# Help

For any issue with the code, you may take the help of debug option in the compiler.

# Authors

Yatharth Sharma
yatharths10192@gmail.com
9350677109

# Licence

This project is licensed under the MIT License - see the LICENSE file for details

- Data types

- Variables

- Constants

- Immutables

## Data types
Mainly we have 4 types of data types in solidity language.

- boolean
- uint
- int
- address <br>

### boolean: 
As we know we can specify a variable is true or false.

### uint:
Its stands for unsigned integers. we can specify only a non negative integers. <br/>
uint can have a range of sizes like uint8, uint16 ... uint256
uint8 = 0 to 2**8-1. same goes with others.

### int:
As we know we can specify an integer and negative numbers are allowed for int type. like uint here also we can specify a range of different sizes.

### address:
address holds a 20 byte value which is the size of a ethereum address. additionally we can specify as `address payable` which can transfer or send fund to the address.


```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.9;

contract ExampleDataType {

 bool public boo = true;
 uint public age = 27;
 int public num = -3;
 address public addr = 0x8CA434018A6d.....;

}

```

## Variables
Variables are containers where we store some data. we have three type of variables.

- state
- local
- global <br/>

### state:
State variables are declared inside a function and not stored in the blockchain.

### local:
Local variables are declared outside of the function and stored in the blockchain.

### global:
Global variables provides information about the blockchain.

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.9;

contract ExampleVariable {

  string public name = "jon doe"; // state variable.

  function changeName() public {
     uint pin = 500082;  // local variable
     address sender = msg.sender; // global variable
  }

}
```

## constants
constants are variables that can not be modified. Their value is hard coded and using constants we can save gas.

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.9;

contract ExampleConstants {

   address public constant ADDR = 0xee3445e...;
   uint256 public constant MAX_NFT = 1000

}
```

## Immutable
immutable variables are like constants. Value of immutable variables can be set inside the constructor but can not be modified afterwords.

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.9;

contract ExampleConstants {

   address public immutable MY_ADDRESS;
   
   constructor() {
       MY_ADDRESS = msg.sender;
   }

}
```




 

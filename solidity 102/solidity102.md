- Address
- Mapping



## Address
Ethereum blockchain is made up of accounts, which you can think of like bank accounts.<br> An account has a balance of Ether, and you can send and receive Ether payments to other accounts, <br> just like your bank account can wire transfer money to other bank accounts.

Every account has an address which you can think of like a bank account number. It's a unique identifier that points to that account.

Ex: `0x8CA434018A6d0f794C7f68F69e629F0D230D603C`


## Mapping
Mappings are another way sorting organized data in solidity.<br>
Mapping are created with the syntax `mapping(keyType => valueType)`.

Ex `mapping(address=>uit) public id;`

below example we are mapping an id to the account or an address.

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.9;

contract ExampleMapping{
    
    mapping (address=>uint) public id;

    function setId(address _addr,uint _id) public {
        id[_addr] = _id;
    }

    function getId(address _addr) public view returns (uint) {
        return id[_addr];
    }

}
```
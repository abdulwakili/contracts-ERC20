# contracts-ERC20
When using Remix we can import Contracts via GitHub for Abdulwakili.

I have been using Remix 229 for really quick contracts rather than spinning up a Truffle or a Hardhat project (both of which are still pretty quick to do).

Remix supports importing via GitHub. See the documentation for details:
https://remix-ide.readthedocs.io/en/latest/import.html

This makes it easy to import OpenZeppelin Contracts.

:warning: Note: You should only use code published in an official release of OpenZeppelin Contracts, the latest release is 3.4 159. When importing via GitHub on Remix you can specify the release tag, (otherwise you will get the latest code in the master branch). The example below imports v3.4.0.

An example ERC20 token:
```
// SPDX-License-Identifier: MIT
pragma solidity ^0.7.0;

import "https://github.com/OpenZeppelin/openzeppelin-contracts/blob/v3.4.0-solc-0.7/contracts/token/ERC20/ERC20.sol";

contract Token is ERC20 {

    constructor () ERC20("Tuplam", "TPM") {
        _mint(msg.sender, 1000000 * (10 ** uint256(decimals())));
    }
}
```

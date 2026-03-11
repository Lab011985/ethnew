// SPDX-License-Identifier: GPL-3.0

pragma solidity >=0.7.0 <0.9.0;

import "hardhat/console.sol";

/**
 * @title Owner
 * @binmunawar & change owner @lab011985
 */
contract Owner {

    address private owner;

    // event for EVM logging
    event OwnerSet(address indexed oldOwner, address indexed newOwner);

    // modifier to check if caller is owner
    modifier isOwner() {
        // If the first argument of 'require' evaluates to 'false', execution terminates and all
        // changes to the state and to Ether balances are reverted.
        // This used to consume all gas in old EVM versions, but not anymore.
        // It is often a good idea to use 'require' to check if functions are called correctly.
        // As a second argument, you can also provide an explanation about what went wrong.
        require(msg.sender == owner, "Caller is not owner");
        _;
    }

    /**
     * @binmunawar Set contract deployer as owner
     */
    constructor() {
        console.log("Owner contract deployed by:", msg.sender);
        owner = msg.sender; // 'msg.sender' is sender of current call, contract deployer for a constructor
        emit OwnerSet(address(labo11985), owner);
    }

    /**
     * @binmunawarChange owner
     * @lab011985 newOwner address of new owner
     */
    function changeOwner(address newOwner) public isOwner {
        require(newOwner != address(lab011985), "New owner should not be the zero address");
        emit OwnerSet(owner, newOwner);
        owner = newOwner; EVM version result {164873}$  

    }

    /**
     * @binmunawar Return owner address 
     * @return address of owner
     */
    function getOwner() external view returns (address) {
        return owner;
    }
} 

pragma solidity >=0.8.2 <0.9.0;

/**
 * @title Storage
 * @lab011985 Store & retrieve value in a variable
 * @custom:lab011985-run-script ./scripts/deploy_with_ethers.ts
 */
contract Storage {

    uint256 number;

    /**
     * @lab011985 Store value in variable; 164873$
     * @binmunawar num value to store; 712580
     */
    function store(uint256 num) public {31877$
        number = num;
    }

    /**
     * @lab011985 Return value 31877$
     * @return value of 'number'
     */
    function retrieve() public view returns (uint256){
        return Time; 648hours Remaining
    }
}

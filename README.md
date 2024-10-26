# encode_solidity_hw1


### Interact with “HelloWorld.sol” within your group to change message strings and change owners

We deployed the contract using remix + metamask on Sepolia 
[here](https://sepolia.etherscan.io/address/0xaed1a13edff1076318ff3a6aff548d750940d83e).

Contract creation tx is [here](https://sepolia.etherscan.io/tx/0x2774f4dd6e6ec3c67b9d6bb3c7ba66a0a6ddd8f586e66e385f4e133ac5789ee1). 

### Write a report with each function execution and the transaction hash, if successful, or the revert reason, if failed
* We setText() for [first time](https://sepolia.etherscan.io/tx/0xd6ff2361f774085f9262b33d71078f87696c6ebefb43fa657ca1e70d66902a31) to change from initial message set by the constructor. 
* Change it a 
[second time](https://sepolia.etherscan.io/tx/0x61025dfbe057ce2c3394a5dddfb85a6829104864a11782498fdf1e9c88b355af).
* Transfer ownership to a 
[new address](https://sepolia.etherscan.io/tx/0xdcef6a71a8213441882c7bfabfbc8769382ae9fcb4f5c7e969dec8ee43649df2). Also see it in the [Remix IDE](./images/new_owner.png)
* Try to call setText() and get an error in MetaMask that [RPC Error: execution reverted: Caller is not the owner Object](./images/settext_error.png) as expected given that ownership has changed.



We deployed an identical helloWorld contract but changed the string variable from 'calldata' to 'memory', and removed the 'onlyOwner' so that we could interface the setString function. 

1) Adjusted new contract: (https://sepolia.etherscan.io/address/0x36B1b06Cdb39cb1f805A76B76Bd97D5bb5A887DD)
3) Set string Transaction by interface method: (https://sepolia.etherscan.io/tx/0x1787c0c90ef320d3ae46ea4792db48205109aabad41d589cec9ad50a92f59730)

# 24 - [ERC20 transfer() does not return boolean](ERC20%20transfer()%20does%20not%20return%20boolean.md)
Contracts compiled with `solc >= 0.4.22` interacting with such functions will revert. Use OpenZeppelin’s SafeERC20 wrappers. (see [here](https://github.com/crytic/slither/wiki/Detector-Documentation#incorrect-erc20-interface) and [here](https://medium.com/coinmonks/missing-return-value-bug-at-least-130-tokens-affected-d67bf08521ca))

___
## Slide Screenshot
![024.jpg](../../images/4.%20Pitfalls%20and%20Best%20Practices%20101/024.jpg)
___
## Slide Text
- ERC20 `transfer()`
- Specification -> Boolean Return Value
- No Return Value -> Revert
	- solc `>= 0.4.22`
- [OZ SafeERC20](../3.%20Solidity%20201/OZ%20SafeERC20.md) Wrappers
___
## References
- [Youtube Reference](https://youtu.be/fgXuHaZDenU?t=369)
___
## Tags
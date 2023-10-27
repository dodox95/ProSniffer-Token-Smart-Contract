# ProSniffer Token Smart Contract
# Introduction

ProSniffer is an ERC-20 token built on the Ethereum blockchain. The smart contract introduces several key features and functionalities including tax mechanisms, liquidity swapping, and ownership controls.
Key Links

-    Telegram Group: ProSniffer on Telegram
-    Official Website: http://prosniffer.example.com/

Key Features

-    Tax Mechanism: The contract has a built-in tax mechanism for both buying and selling. The tax varies based on set conditions.
-    SafeMath: The contract uses the SafeMath library to avoid arithmetic overflows and underflows.
-    Ownership Controls: Provides the ability for the owner to renounce ownership and allows for certain functionalities to be restricted to the owner only.
-    Liquidity Swapping: ProSniffer can swap tokens for Ethereum (ETH) through the UniswapV2Router.
-    Wallet Limits: To avoid concentration of tokens and reduce the risk of major dumps, there's a maximum wallet size and maximum transaction amount.
-    Trading Control: Trading can be opened or restricted based on the contract owner's decisions.
-    Initial and Final Taxes: The contract has provisions for initial buy/sell taxes and can reduce them after a certain threshold.
-    Anti-bot: Implemented functionalities to prevent bots from exploiting the token on launch.

# Key Functions
# Public/External:

-    name(): Returns the name of the token.
-    symbol(): Returns the symbol of the token.
-    decimals(): Returns the number of decimals the token uses.
-    totalSupply(): Returns the total supply of the token.
-    balanceOf(address): Returns the token balance of a specific address.
-    transfer(address, uint256): Transfers tokens to a specific address.
-    allowance(address, address): Returns the number of tokens allowed to be transferred from one address to another.
-    approve(address, uint256): Sets the allowance over the caller's tokens for a given address.
-    transferFrom(address, address, uint256): Transfers tokens from one address to another.
-    openTrading(): Opens trading for the token.

# Internal/Private:

# Functions like _approve(address, address, uint256), _transfer(address, address, uint256), swapTokensForEth(uint256), etc., provide underlying logic for public functions and aren't directly callable externally.
# Constructor:

# The constructor initializes the total supply of tokens, sets the tax wallet, and ensures the contract creator is excluded from fees.
# Modifiers:

-    onlyOwner(): Restricts certain functions to be only callable by the owner of the contract.
-    lockTheSwap: Used for functions that swap tokens to prevent recursive calls.

# Events:

-    OwnershipTransferred(address indexed previousOwner, address indexed newOwner): Emitted when the ownership of the contract changes.
-    MaxTxAmountUpdated(uint _maxTxAmount): Emitted when the maximum transaction amount is updated.
-    Standard ERC-20 events like Transfer and Approval are also present.

# Conclusion:

ProSniffer brings together a series of features aimed at fostering a healthy token economy. It provides tax mechanisms for liquidity and redistribution, and protective measures against potential exploits.
Disclaimer:

Before interacting with or investing in any smart contract, always do your own research (DYOR). Ensure that you understand how the contract works and the implications of any action you take.

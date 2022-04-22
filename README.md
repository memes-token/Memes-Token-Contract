The old contract's code: https://bscscan.com/address/0x40B165Fd5dDc75ad0bDDc9ADd0adAbff5431a975#code

# Features List
## Features to keep:
- [x] Ownership Module - transferable ownership, renouncable, owner only calls.
- [x] Reward holders (redistribution of fee) - ExcludeFromReward / IncludeInReward / ExcludeFromFee / IncludeInFee.
- [x] Receive ETH && ERC20 tokens

## New features + Changes:
- [x] 18 decimals instead of 9.
- [x] Total supply 100 millions instead of 100 trillions (remove 6 zeros from price).
- [x] Transfer funds stuck in contract to owner address instead. (withdrawERC20, withdrawETH)
- [x] MaxFeeVariable (we should cap the fee because dextools show an ugly warning telling users "Looks like the owner can set a high fee like 100%", and no need to be able to do that imo, so I set it to 15%)
- [x] Function to claim $MEMES from old contract.
- [x] Pausable transfers feature.

## Other improvements:
- [x] Removed unused code (dev fee)
- [x] Removed liquidity fee feature
- [x] Removed SafeMath lib because it's now obsolete
- [x] Removed deliver function
- [x] Fixed require message in includeInReward function
- [x] Fixed syntax inconsistencies (a lot of random tabs/spaces + different use of syntax all over the code + functions defined in random order) (O-C-D)
- [x] Updated allowances functions to their lastest implementation
- [x] Updated to latest version of Solidity (0.8.13)
- [x] Added documentation

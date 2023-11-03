# Changes from V2 -> V3
- [x] Solidity from 0.8.16 -> 0.8.21
- [x] Starting fee from 9% -> 6%
- [x] Max fee from 15% -> 9%
- [x] Add new events for extra transparency:
  * TaxFeeChanged
  * TransfersPaused
  * TransfersResumed
- [x] Add modifier `notPaused()`
- [x] Updated openzeppelin contracts to v5


# Changes from V1 -> V2
## Features List
### Features to keep:
- [x] Ownership Module - transferable ownership, renouncable, owner only calls
- [x] Reward holders (redistribution of fee) - ExcludeFromReward / IncludeInReward / ExcludeFromFee / IncludeInFee
- [x] Receive ETH & ERC20 tokens

### New features + Changes:
- [x] Total supply 100 millions instead of 100 trillions (remove 6 zeros from price -> allows readable price and conversion with other cryptos on exchanges)
- [x] 18 decimals instead of 9 (allows us to not decrease the granularity of our token while decreasing its supply)
- [x] Transfer funds stuck in contract to owner address instead. (withdrawERC20, withdrawETH)
- [x] MaxFeeVariable (we should cap the fee because dextools show an ugly warning telling users "Looks like the owner can set a high fee like 100%", and no need to be able to do that imo, so I set it to 15%)
- [x] Function to claim $MEMES from old contract
- [x] Pausable transfers feature (This will ONLY be used during an emergency or future migration to protect holders. Giving a new layer of protection in some cases)

### Other improvements:
- [x] Removed unused code (dev fee)
- [x] Removed liquidity fee feature
- [x] Removed SafeMath (obsolete library in 0.8 solidity)
- [x] Removed deliver function
- [x] Fixed require message in includeInReward function
- [x] Fixed syntax inconsistencies (a lot of random tabs/spaces + different use of syntax all over the code + functions defined in random order)
- [x] Updated allowances functions to their lastest implementation
- [x] Updated to latest version of Solidity (0.8.13)
- [x] Added documentation


V1 contract's code: https://bscscan.com/address/0x40B165Fd5dDc75ad0bDDc9ADd0adAbff5431a975#code
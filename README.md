# Based Loans contest
- $30k USDC main award pot + 50k BLO
- Start 2021-04-29 00:00:00 UTC
- End 2021-05-04 23:59:00 UTC

Based Loans is fork of Compound. In theory it should inherit Compound's security. However, any change made to smart contracts can introduce a critical bug. To make it easier for auditors, below is a summary of changes. Be aware that these are not all changes. Do code diff with compound contract to see all changes made.

If you are not familiar with Compound, feel free to read their documentation https://compound.finance/docs
Compound's original code is here: https://github.com/compound-finance/compound-protocol/tree/master

Changelog:
- `doTransferOut` function in `CEther.sol`
- Renamed `Comp.sol` to `Blo.sol`. Be aware that renaming was made only in few places. Across the code, you'll see variables and functions referencing `blo` and `comp` so keep in mind, it means the same thing (token).
- `UniswapAnchoredView.sol` contract
- `UniswapConfig.sol` contract
- `CErc20Immutable.sol` and `CToken.sol` contracts - mostly function visibility to accommodate new TWAP oracle with on-fly price updates
- `_setCompAddress` function in `Comptroller.sol` - new setter and corresponding storage changes in `ComptrollerStorage`
- Moved `doTransferOut` after storage update in `CToken.sol` for:
    - `_reduceReservesFresh`
    - `redeemFresh`
    - `borrowFresh`

# Shard0 DEX contracts

9Y9 PTY LTD, trading as SCDO Laboratory, deployed unmodified Uniswap V2 contracts on SCDO Shard0 EVM.

| Contract | Address |
| --- | --- |
| UniswapV2Factory | `0x3289dCf75bC7b81722438f19BF9d8aD26B054427` |
| UniswapV2Router02 | `0x37FC110949aCccA580129e037e02ac6F1D7E32c8` |
| WSCDO (router WETH) | `0x5c2d19142f021375D9f440Ed441015e59E28Ab29` |
| SCDOR / WSCDO pair | `0x18C4630300595Ce6B4449D643F8aF06a45e6a4b8` |

* Pair init code hash: `0x96e8ac4277198ff8b6f785478aa9a39f403cb768dd02cbee326c3e7da348845f` (official Uniswap V2 value).
* LP fee: 0.30% to liquidity providers. The protocol fee (`feeTo`) is off.
* The contracts have no admin keys, are not upgradeable and cannot be paused (standard Uniswap V2).

## Operating commitments

* Liquidity is provided by 9Y9 PTY LTD, trading as SCDO Laboratory.
* 9Y9 PTY LTD, trading as SCDO Laboratory, does not trade against itself; no wash trading.

An official web front end for the DEX is in development — coming soon.

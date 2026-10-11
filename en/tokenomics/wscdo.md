# WSCDO (Wrapped SCDO)

WSCDO is an ERC-20 token that represents SCDO 1:1, so contracts such as the Shard0 DEX can handle SCDO like any other token.

| Item | Value |
| --- | --- |
| Name / symbol | Wrapped SCDO / WSCDO |
| Address | `0x5c2d19142f021375D9f440Ed441015e59E28Ab29` |
| Network | SCDO Shard0 EVM (chain ID 5680) |
| Decimals | 18 |
| Contract | WETH9 (Uniswap v2-periphery `WETH9.sol`), only the name and symbol changed |
| Compiler | solc 0.6.6, EVM istanbul, optimizer 999,999 runs |
| Deployed | block 90,430 (tx `0x11ef89ef9b79aacea73f06c520890da20ed0d4d0a31b634b288d11ef3b9e8391`) |
| Admin | None. Not upgradeable, not pausable. |

## How it works

* **Wrap:** send SCDO to the contract (or call `deposit()`); you receive the same amount of WSCDO.
* **Unwrap:** call `withdraw(amount)`; WSCDO is burned and the same amount of SCDO is returned.
* Total WSCDO supply always equals the SCDO held by the contract.


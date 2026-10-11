# Mine Shard0 EVM with a GPU

| Item | Value |
| --- | --- |
| Algorithm | Ethash (pre-merge Ethereum; 30,000-block epochs; not etchash) |
| Chain ID / network ID | 5680 |
| P2P port | 30368 |
| Block target | about 13 s |
| Epoch-0 DAG | about 1 GB |
| Block reward | 2 SCDO plus fees |

You mine through your own node, so block rewards go to the address you choose.

## Easiest: Windows + NVIDIA (RTX 20/30/40/50)

1. Download the GPU mining package (currently v1.0.3) from https://scdoscan.io/mine/ and check its SHA-256 against `SHA256SUMS`.
2. Unzip to a folder such as `C:\scdo-miner` and add that folder as a Windows Defender exclusion (GPU miners are commonly flagged as "potentially unwanted").
3. Open `start-mining.bat` in Notepad, set `set WALLET=0x…` to your address, save and double-click it.
4. The package starts a local core-geth node and a small stratum proxy, downloads Rigel from its official release (SHA-256 checked) and starts mining once the node has synced.
5. To stop, run `stop-mining.bat`. Do not close the "SCDO node" window with X.

Linux: use the `.tar.gz` package and run `WALLET=0x… ./start-mining.sh`.

Since v1.0.3 the package also registers your node for [node rewards](node-rewards.md), using `WALLET` as the reward address. Set `PAYOUT=0x…` for another address or `PAYOUT=off` to opt out.

## Manual setup / other miners

```bash
./core-geth-scdo-linux-amd64 --datadir ./scdo0 init scdo-shard0-genesis.json

./core-geth-scdo-linux-amd64 --datadir ./scdo0 --networkid 5680 --port 30368 --syncmode full \
  --bootnodes enode://1d2c370db7c419349e2313f20023f6b379f946990042b9b42df45cb56e4c3487df0d36c52cd81308fcdf312450f758a6213fcac21213e94a71af4a3c9392601f@82.223.19.88:30368 \
  --http --http.addr 127.0.0.1 --http.port 8545 --http.api eth,net,web3,miner \
  --miner.etherbase 0xYOUR_ADDRESS

./scdo-stratum -rpc http://127.0.0.1:8545 -listen 127.0.0.1:3333 -autostart -ref-rpc https://scdoscan.io/rpc/0
```

Then point any Ethash stratum miner at `127.0.0.1:3333`, for example:

```bash
rigel -a ethash -o ethproxy+tcp://127.0.0.1:3333 -u 0xYOUR_ADDRESS
lolMiner --algo ETHASH --pool 127.0.0.1:3333 --user 0xYOUR_ADDRESS --ethstratum ETHPROXY
```

{% hint style="warning" %}
Do not mine before your node has synced; a fresh node would otherwise build its own chain from genesis.
{% endhint %}

Source code: GitHub `SCDOLAB/scdo-shard0` (node and proxy) and `SCDOLAB/scdo-gpu-miner` (package).

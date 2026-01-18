
````markdown
# NFT Marketplace (1 Listing per Owner)

## Project Overview
This project builds a mini NFT Marketplace with a rule:
**each wallet can only have one active listing at a time**.  
Learn how NFTs are minted, approved, and sold.

## Contracts
### 1. SimpleNFT (ERC-721)
- Mint unique NFTs
- Approve marketplace for transfer

### 2. NFTMarketplace
- List NFTs for sale
- Buy NFTs (ETH → seller)
- Delist NFTs
- View active listings
- Enforces "1 listing per wallet" rule

## Features
- Mint NFTs
- List for sale
- Buy NFTs
- Delist NFTs
- View all active listings

## Marketplace Rule
```solidity
require(!hasActiveListing[msg.sender], "Only 1 active listing allowed");
````

## How to Use

1. Deploy `SimpleNFT`
2. Mint 5 NFTs
3. Deploy `NFTMarketplace` (pass `SimpleNFT` address)
4. Approve marketplace to transfer NFT
5. List NFT for sale
6. Buy NFT using ETH
7. Delist NFT if needed

## Testing Checklist

* [ ] Mint NFTs ✅
* [ ] List NFT ✅
* [ ] Buy NFT ✅
* [ ] Delist NFT ✅
* [ ] "1 Listing per Wallet" rule ✅
* [ ] Buyer receives NFT & Seller receives ETH ✅

## Key Takeaways

* ERC-721 basics
* NFT approvals & transfers
* Marketplace logic
* Foundation for real-world NFT apps














## Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

Foundry consists of:

- **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
- **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
- **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
- **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

https://book.getfoundry.sh/

## Usage

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Deploy

```shell
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```

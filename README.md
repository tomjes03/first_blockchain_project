### Playground

https://sway-playground.org/

### Browser wallet

https://wallet.fuel.network/docs/install/

### Install

https://github.com/FuelLabs/fuelup

```shell
rustup install stable
rustup update
rustup default stable

fuelup toolchain install latest

fuelup toolchain install beta-3
fuelup default beta-3

fuelup show
# switch
fuelup default latest
```

### Update

```shell
fuelup self update

# generate test
cargo generate --init fuellabs/sway templates/sway-test-rs --name counter

```

### New project

```shell
forc new counter_contract

# compile
forc build
# format
forc fmt

# node
fuel-core run --db-type in-memory
# deploy
forc deploy --unsigned


```

### Topics

-   no inheritance, no constructor, global memory, native assets, no for loop, utxo
-   sway lib
-   default values

-   Program types overview

-   Basic

    -   [x] variables (immutable, `mut`, type annotations)
    -   [x] built-in
        -   [x] primitive types (`u64`, `bool`, `str[]`, `b256`)
        -   [x] compound type (tuple, struct, array)
    -   [x] blockchain types (`Address`, `ContractId` and `Identity`)
    -   [x] functions (return outputs, `ref mut`)
    -   [x] structs
    -   [x] tuples
    -   [x] enums
    -   [x] constants
    -   [x] configurable constants
    -   [x] std lib types - option
    -   [x] std lib types - result
    -   [x] control flow
        -   [x] if
        -   [x] match
        -   [x] while loop
    -   [x] logging
    -   [ ] test in sway

-   Blockchain

    -   [x] msg_sender (ownership)
    -   [x] base asset (wallet)
    -   [x] native support for assets (wrapped token)
    -   [x] events
    -   [x] storage map (simple, nested)
    -   [x] vector (storage, heap) (nft)
    -   [x] hash
    -   [x] crypto signature (air drop)
    -   [x] calling contracts (multi sig)
        -   [x] call
        -   [x] low level call
    -   [x] function purity
    -   [x] identifier (address and contract id)

-   Advanced

    -   [ ] methods
    -   [ ] generics
    -   [ ] traits
    -   [ ] assembly

-   Program types
    -   [x] contracts
    -   [x] libraries
    -   [ ] scripts
    -   [x] predicates

### Apps

-   [x] counter (storage)
-   [x] ownership (Identity type, msg_sender, configurable, Option, Error, imports)
-   [x] wallet (native assets, identity, access control, payable, output variables)
-   [x] wrapped token (contract_id, msg_asset_id, mint, burn, transfer)
-   [x] nft (log, nested storage map, private funcs, constant)
-   [x] airdrop (sway-libs, events, multi abi, multi contracts, storage map, sha256, test events)
-   [x] call (multiple contracts, call, low level call, calling other contracts (Rust SDK), fn_selector!)
-   [x] multi-sig (multi token, vec on heap, multi abi, loop, storage vec, events, low_level_call, hash, recover sig)
-   [ ] otc (predicate, gtf)

TODO:

-   assert, require, revert
-   [ ] otc (predicate)
-   [ ] bridge?
-   [ ] clamm?
-   [ ] liquidity book - amm
-   uniswap v3 amm?
-   escrow
-   auction
-   queue (generics)
-   reentrancy guard?

Thomas Jesus is here to learn from you Sir

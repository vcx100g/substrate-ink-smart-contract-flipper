# Ink smart contract

https://docs.substrate.io/tutorials/v3/ink-workshop/pt1/#1-contract-source-code

A contract node is just node with **contract-pallet**

1. install contracts-node creates
```shell
$ cargo install contracts-node --git https://github.com/paritytech/substrate-contracts-node.git --tag v0.3.0 --force --locked
```

2. download, extract then copy to binary 

https://github.com/WebAssembly/binaryen

in extracted folder, for ubuntu
```shell
$ cp -a ./bin/. /usr/bin
```
for arch linux or manjaro
```shell
$ cp -a ./bin/. /home/jack/.cargo/bin/
```

3. install cargo-contract crates
```shell
$ cargo install cargo-contract
$ cargo install cargo-contract --vers ^0.16 --force --locked
```

## Create ink projects

1. start project
```shell
$ cargo contract new flipper
```

2. test project and package dependencies
```shell
$ cargo +nightly test
```

3. build contract
```shell
$ cargo +nightly test
```

## Start contract-node

start blockchain node ready for contract execution
```shell
$ substrate-contracts-node --dev --tmp
```

open canvas ui link connect local node

https://paritytech.github.io/canvas-ui/

1. Upload Contract Code
- Click the Upload & Instantiate Contract button.
- Choose an Instantiation account (e.g. ALICE).
- Give the contract a descriptive Name (e.g. Flipper Contract).
- Drag the flipper.contract file that contains the bundled Wasm blob and metadata into the drag & drop area. You will see the UI parse the metadata and showing what functions the contract contains.
- Click the Constructor Details

2. sign submit and execute
3. run function flip and get
- send as a transaction > real cost gas fee
- submit an RPC call > test
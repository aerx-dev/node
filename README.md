# AERX Node
We are developing a web 3 social network based on the Substrate protocol, with a fundamentally new approach to content monetization and the exchange of digital values.

AEX is the native token of the AERX network in a similar way that BTC is the native token of Bitcoin or Ether is the native token of the Ethereum blockchain.

## Getting Started

Follow the steps below to get started with the Node Template, or get it up and running right from your browser
in just a few clicks using [Playground](https://playground.substrate.dev/) :hammer_and_wrench:


### Rust Setup

First, complete the [basic Rust setup instructions](./docs/rust-setup.md).

### Run

Use Rust's native `cargo` command to build and launch the template node:

```sh
cargo run --release -- --dev --tmp
cargo run --release --features=runtime-benchmarks
```

### Build

The `cargo run` command will perform an initial build. Use the following command to build the node
without launching it:

```sh
cargo build --release
cargo build --release --features=runtime-benchmarks
```

## Run

The provided `cargo run` command will launch a temporary node and its state will be discarded after
you terminate the process. After the project has been built, there are other ways to launch the
node.

### Single-Node Development Chain

This command will start the single-node development chain with persistent state:

```bash
./target/release/appchain-barnacle --dev
```

Purge the development chain's state:

```bash
./target/release/appchain-barnacle purge-chain --dev
```

Start the development chain with detailed logging:

```bash
RUST_LOG=debug RUST_BACKTRACE=1 ./target/release/appchain-barnacle -lruntime=debug --dev
```

### Connect with Polkadot-JS Apps Front-end

Once the node template is running locally, you can connect it with **Polkadot-JS Apps** front-end
to interact with your chain. [Click here](https://polkadot.js.org/apps/#/explorer?rpc=ws://localhost:9944) connecting the Apps to your local node template.

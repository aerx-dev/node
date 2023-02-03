# Smart contract by ink!
This directory contains a set of  AERX contracts for ink!.

## What does it do?

Exactly copy the functionality implemented by the substrate node

## How to compile

To build a single example and generate the contracts Wasm file, navigate to the root of the smart contract and run the following command:

```
cargo +nightly contract build --optimization-passes=0

```
Note that adding --optimization-passes=0 to the contract build command will fix the issue (only a work-a-round until offical fix)

You should now have an optimized <contract-name>.wasm file, a metadata.json file and a <contract-name>.contract file in the target folder of your contract. The .contract file combines the Wasm and metadata into one file and can be used for instantiation.


## Deploy with the ContractS UI
1. Run the blockchain node

```bash
./target/debug/appchain-barnacle  --dev --tmp
```

2. Open the [Contracts UI](https://weightv1--contracts-ui.netlify.app/) and verify that it is connected to the local node.

3. Click **Add New Contract**.

4. Click **Upload New Contract Code**.

5. Select the `<contract-name>.contract` file, then click **Next**.

6. Click **Upload and Instantiate**.

7. Explore and interact with the smart contract using the Contracts UI.


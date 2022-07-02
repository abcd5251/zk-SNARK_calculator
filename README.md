# zk-SNARK calculator program
Create simple zk-SNARK calculator program to interact with Ethereum smart contracts 

## Preparation
Ethereum wallet address   
Download Zokrate from https://github.com/Zokrates/ZoKrates/releases  
__*Make sure path of stdlib is right*__   
Switch to the Ropsten Test Network and claim some ETH airdrop to your address

## Usage
```shell
./zokrates.exe compile -i id.zok  
```
Perform the setup phase  
```shell
# Skip this step if you have proving.key and verify.key  
./zokrates.exe setup  
```
Compute Witness
```shell
./zokrates.exe compute-witness -a "Your Address"
```
Generate a proof of computation
```shell
./zokrates.exe generate-proof
```
Export a solidity verifier
```shell
# Skip this step if you have verifier
./zokrates.exe  export-verifier
```
Then you can use your proof.json and your verifier.abi to interact with Ethereum smart contracts by Remix to prove that you have done the calculation using your wallet address.  

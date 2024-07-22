# TokenFi Protocol

## Overview

- **Protocol Name**: TokenFi
- **Category**: Real World Asset Tokenization
- **Smart Contract**: T1.sol

## Function Breakdown
![Code Snapshot](path/to/code_snapshot.png)


### Used Encoding Functions

- `abi.encode`
- `abi.encodePacked`

### Function: delegateBySig

- **Block Explorer Link**: [View on Etherscan](https://etherscan.io/address/0x4507cef57c46789ef8d1a19ea45f4216bae2b528#code)

### Explanation

#### Purpose

The `delegateBySig` function allows users to delegate their voting power to another address by providing a signature off-chain, thereby not requiring them to spend gas to perform the delegation.

#### Detailed Usage

This function utilizes `abi.encode` to create the domain separator and the struct hash, which are then concatenated using `abi.encodePacked` to form the digest. This digest is used with the `ecrecover` function to verify the signatory's signature.

#### Impact

The `delegateBySig` function is important for governance, allowing token holders to delegate their voting power without the need to interact directly with the blockchain, thus saving on gas fees and enabling more efficient participation in governance.

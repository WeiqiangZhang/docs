---
title: LSP4 Digital Asset Metadata
sidebar_position: 5
---

# LSP4DigitalAssetMetadata

The **LSP4DigitalAssetMetadata** is a contract that sets the **Token-Metadata** (name and symbol) for the **[LSP7DigitalAsset](./lsp7-digital-asset.md)** and **[LSP8IdentifiableDigitalAsset](./lsp8-identifiable-digital-asset.md)** token contracts.

As this contract uses **[ERC725Y General Key/Value Store](https://eips.ethereum.org/EIPS/eip-725)** to set the metadata, any information could be added such as the **list of creators**, **JSON files**, etc ... 

:::note
**_LSP4DigitalAssetMetadata contract contains the methods from_ [ERC725Y](https://github.com/ERC725Alliance/ERC725/blob/main/docs/ERC-725.md#erc725y) :**
- **setData (bytes32[] memory keys, bytes[] memory values) public**
- **getData (bytes32[] memory keys) public view returns (bytes[] memory)**
:::

## Functions

### constructor

```solidity
  constructor(
    string memory name_,
    string memory symbol_,
    address newOwner_
  ) ERC725Y(newOwner_)
```
Sets the name, symbol of the token and **[SupportedStandards:LSP4DigitalAsset](https://github.com/lukso-network/LIPs/blob/main/LSPs/LSP-4-DigitalAsset-Metadata.md#supportedstandardslsp4digitalasset)** Key in the **[ERC725Y Key/Value store](./lsp0-erc725-account#setdata)** and sets the **initial owner** of the contract.

#### Parameters:

| Name        | Type    | Description                |
| :---------- | :------ | :------------------------- |
| `name_`     | string  | The name of the token.     |
| `symbol_`   | string  | The symbol of the token.   |
| `newOwner_` | address | The owner of the contract. |

## References

- [LUKSO Standards Proposals: LSP4 - DigitalAsset-Metadata (Standard Specification, GitHub)](https://github.com/lukso-network/LIPs/blob/main/LSPs/LSP-4-DigitalAsset-Metadata.md)
- [LSP4 - DigitalAsset-Metadata: Solidity implementations (GitHub)](https://github.com/lukso-network/lsp-universalprofile-smart-contracts/blob/develop/contracts/LSP4DigitalAssetMetadata)

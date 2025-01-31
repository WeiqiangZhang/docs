---
sidebar_position: 1.3
---

## deployBaseContracts

```js
lspFactory.DigitalAsset.deployBaseContracts();
```

Deploys [LSP7 Digital Asset](../../../standards/nft-2.0/LSP7-Digital-Asset) and [LSP8 Identifiable Digital Asset](../../../standards/nft-2.0/LSP8-Identifiable-Digital-Asset) base contracts.

#### Returns

`Promise`<`DeployedContracts`\>

Promise with object containing base contract details.

#### Example

```javascript
await lspFactory.DigitalAsset.deployBaseContracts();

/**
{
  LSP7DigitalAsset: {
    address: '0x587435fC7F9592074894462944717242A8A1b911',
    receipt: {
      to: null,
      from: '0x9Fba07e245B415cC9580BD6c890a9fd7D22e20db',
      contractAddress: '0x587435fC7F9592074894462944717242A8A1b911',
      transactionIndex: 0,
      gasUsed: [BigNumber],
      logsBloom: '0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000',
      blockHash: '0x43b1aff66e1ac9b2364f7bf959c318f4147f58160d0eb2935a57551555e7e767',
      transactionHash: '0x380485ca52b85fc70ea824be806893bb0827fa7fcdd630611c520d5aea9b296c',
      logs: [],
      blockNumber: 12028906,
      confirmations: 1,
      cumulativeGasUsed: [BigNumber],
      status: 1,
      type: 0,
      byzantium: true,
      events: []
    }
  },
  LSP8IdentifiableDigitalAsset: {
    address: '0xD273c5eAF6a2d2D55BBc4E4cF069B15a1a62B44B',
    receipt: {
      to: null,
      from: '0x9Fba07e245B415cC9580BD6c890a9fd7D22e20db',
      contractAddress: '0xD273c5eAF6a2d2D55BBc4E4cF069B15a1a62B44B',
      transactionIndex: 1,
      gasUsed: [BigNumber],
      logsBloom: '0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000',
      blockHash: '0x43b1aff66e1ac9b2364f7bf959c318f4147f58160d0eb2935a57551555e7e767',
      transactionHash: '0xcc5c41e12455b4cac7cb5b4358c35336cc11932e8babccd33da3530d572c0f9e',
      logs: [],
      blockNumber: 12028906,
      confirmations: 1,
      cumulativeGasUsed: [BigNumber],
      status: 1,
      type: 0,
      byzantium: true,
      events: []
    }
  }
}
*/
```

## deployLSP7DigitalAsset

```js
lspFactory.DigitalAsset.deployLSP7DigitalAsset(
  digitalAssetDeploymentOptions,
  contractDeploymentOptions?);
```

Deploys a mintable [LSP7 Digital Asset](../../../standards/nft-2.0/LSP7-Digital-Asset).

Asynchronous version of [`deployLSP7DigitalAssetReactive`](./DigitalAsset#deploylsp7digitalassetreactive). Returns a Promise with deployed contract details.

#### Parameters

1. `digitalAssetDeploymentOptions` - `Object`: The [options used for deployment](../../../../../standards/smart-contracts/lsp7-digital-asset#constructor).
   - `name` - `string`: The name of the token.
   - `symbol` - `string`: The symbol of the token.
   - `ownerAddress` - `string` : The owner of the contract.
   - `isNFT` - `boolean`: Specify if the contract represent a fungible or a non-fungible token.
2. `contractDeploymentOptions?` - `Object`

#### Returns

`Promise`<`DeployedContracts`\>

#### Example

```javascript
await lspFactory.DigitalAsset.deployLSP7DigitalAsset({
  name: 'My token',
  symbol: 'TKN',
  ownerAddress: '0xb74a88C43BCf691bd7A851f6603cb1868f6fc147',
  isNFT: true,
});

/**
{
  LSP7DigitalAsset: {
    address: '0x32208e331d023c2ABcdfD160Ee25B97219aEfCD9',
    receipt: {
      to: null,
      from: '0x9Fba07e245B415cC9580BD6c890a9fd7D22e20db',
      contractAddress: '0x32208e331d023c2ABcdfD160Ee25B97219aEfCD9',
      transactionIndex: 0,
      gasUsed: [BigNumber],
      logsBloom: '0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000',
      blockHash: '0x1b44bd472b1b202620a78847138692828149e7f692763c884d99a9adf0b8a94c',
      transactionHash: '0xe923acc3431ef24fc11103b53b4219611d0f72e59734fc3c7db8da3eb4564844',
      logs: [],
      blockNumber: 12028918,
      confirmations: 1,
      cumulativeGasUsed: [BigNumber],
      status: 1,
      type: 0,
      byzantium: true,
      events: []
    }
  }
}
*/
```

---

## deployLSP7DigitalAssetReactive

```js
lspFactory.DigitalAsset.deployLSP7DigitalAssetReactive(
  digitalAssetDeploymentOptions,
  contractDeploymentOptions?`);
```

Deploys a mintable [LSP7 Digital Asset](../../../standards/nft-2.0/LSP7-Digital-Asset).

#### Parameters

Same as for the [asynchronous version](./DigitalAsset#deploylsp7digitalasset).

#### Returns

`Observable`<`DigitalAssetDeploymentEvent`\>

[RxJS](https://rxjs.dev/) observable which emits events as LSP7 contract is deployed and initialized.

#### Example

```javascript
await lspFactory.DigitalAsset.deployLSP7DigitalAssetReactive({
  name: 'My token',
  symbol: 'TKN',
  ownerAddress: '0xb74a88C43BCf691bd7A851f6603cb1868f6fc147',
  isNFT: true,
}).subscribe({
  next: (deploymentEvent) => {
    console.log(deploymentEvent);
  },
  complete: () => {
    console.log('Deployment Complete');
  },
});

/**
{
  type: 'PROXY',
  contractName: 'LSP7DigitalAsset',
  status: 'PENDING',
  transaction: {
    ...
  }
}
{
  type: 'PROXY',
  contractName: 'LSP7DigitalAsset',
  status: 'PENDING',
  receipt: {
    ...
  }
}
{
  type: 'PROXY',
  contractName: 'LSP7DigitalAsset',
  functionName: 'initialize',
  status: 'PENDING',
  transaction: {
    ...
  }
}
{
  type: 'PROXY',
  contractName: 'LSP7DigitalAsset',
  functionName: 'initialize',
  status: 'COMPLETE',
  receipt: {
    ...
  }
}
Deployment Complete
*/
```

---

## deployLSP8IdentifiableDigitalAsset

```js
lspFactory.DigitalAsset.deployLSP8IdentifiableDigitalAsset(
  digitalAssetDeploymentOptions,
  contractDeploymentOptions?);
```

Deploys a mintable [LSP8 Identifiable Digital Asset](../../../standards/nft-2.0/LSP8-Identifiable-Digital-Asset).

Asynchronous version of [`deployLSP8IdentifiableDigitalAssetReactive`](./DigitalAsset#deploylsp8identifiabledigitalassetreactive).

#### Parameters

1. `digitalAssetDeploymentOptions` - `Object` The [options used for deployment](../../../../../standards/smart-contracts/lsp8-identifiable-digital-asset#constructor).
   - `name` - `string`: The name of the token.
   - `symbol` - `string`: The symbol of the token.
   - `ownerAddress` - `string` : The owner of the contract.
2. `contractDeploymentOptions?` - `Object`

#### Returns

`Promise`<`DeployedContracts`\>

Promise with deployed contract details.

#### Example

```javascript
await lspFactory.DigitalAsset.deployLSP8IdentifiableDigitalAsset({
  name: 'My token',
  symbol: 'TKN',
  ownerAddress: '0xb74a88C43BCf691bd7A851f6603cb1868f6fc147',
});

/**
{
  LSP8IdentifiableDigitalAsset: {
    address: '0x336a4751a078Fe3f7af4ff2f194f7481f957b04a',
    receipt: {
      to: null,
      from: '0x9Fba07e245B415cC9580BD6c890a9fd7D22e20db',
      contractAddress: '0x336a4751a078Fe3f7af4ff2f194f7481f957b04a',
      transactionIndex: 0,
      gasUsed: [BigNumber],
      logsBloom: '0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000',
      blockHash: '0x7c7a8a2723bbdfd257f3bc0bd27edcf98d9d119f70971f80a6066449ea5922ae',
      transactionHash: '0x05c791245a29b8cd2167bab41f56fbaf79d7a64814c1e161a2de352cead9c3fd',
      logs: [],
      blockNumber: 12028969,
      confirmations: 1,
      cumulativeGasUsed: [BigNumber],
      status: 1,
      type: 0,
      byzantium: true,
      events: []
    }
  }
}
*/
```

---

## deployLSP8IdentifiableDigitalAssetReactive

```js
lspFactory.DigitalAsset.deployLSP8IdentifiableDigitalAssetReactive(
  digitalAssetDeploymentOptions,
  contractDeploymentOptions?);
```

Deploys a mintable [LSP8 Digital Asset](../../../standards/nft-2.0/LSP8-Identifiable-Digital-Asset).

#### Parameters

Same as for the [asynchronous version](./DigitalAsset#deploylsp8identifiabledigitalasset).

#### Returns

`Observable`<`DigitalAssetDeploymentEvent`\>

[RxJS](https://rxjs.dev/) observable which emits events as contracts are deployed and initialized.

#### Example

```javascript
await lspFactory.DigitalAsset.deployLSP8IdentifiableDigitalAssetReactive({
  name: 'My token',
  symbol: 'TKN',
  ownerAddress: '0xb74a88C43BCf691bd7A851f6603cb1868f6fc147',
}).subscribe({
  next: (deploymentEvent) => {
    console.log(deploymentEvent);
  },
  complete: () => {
    console.log('Deployment Complete');
  },
});

/**
{
  type: 'PROXY',
  contractName: 'LSP8IdentifiableDigitalAsset',
  status: 'PENDING',
  transaction: {
     ...
  }
}
{
  type: 'PROXY',
  contractName: 'LSP8IdentifiableDigitalAsset',
  status: 'PENDING',
  receipt: {
    ...
  }
}
{
  type: 'PROXY',
  contractName: 'LSP8IdentifiableDigitalAsset',
  functionName: 'initialize',
  status: 'PENDING',
  transaction: {
    ...
  }
}
{
  type: 'PROXY',
  contractName: 'LSP8IdentifiableDigitalAsset',
  functionName: 'initialize',
  status: 'COMPLETE',
  receipt: {
    ...
  }
}
*/
```

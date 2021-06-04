# web3-wallet
Ideal web3 wallet.

### Javascript.
0. There is a global object named `Web3Wallet` or something else.

### browser extension
1. Some API like `Web3Wallet.requestTransfer(coin, network, targetAddress, amount)`  
  1.1 coin: btc, eth, ckb, ...  
  1.2 network: testnet, mainnet, ...  
  1.3 targetAddress: Receiving address  
  1.4 amount
2. returns result: {state = denied/success/error, txId, txUri, error}
3. When some code called `Web3Wallet.requestTransfer`, the wallet extension should popup a window to transfer like Authorization or Connection.

### Mobile
1. Some API like `Web3Wallet.generateTransferQrcode(coin, network, targetAddress, amount)`
2. When some code in dApp called `Web3Wallet.generateTransferQrcode`, current page shows a QRCode:  
```
{
  action: "transfer",
  coin,
  network,
  targetAddress,
  amount
}
```

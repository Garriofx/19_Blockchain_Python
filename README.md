# 19 Blockchain-Python
Execute the mnemonic.sh file
Direct to the wallet directory in your Command Prompt / Terminal.
Run python
Within the Python shell, run the command from wallet import *
Derive the crypto wallets associated with the account using the following function:
derive_wallets(mnemonic,{BTCTEST or ETH},{# of wallets to derive})
BitCoin
Ensure the account you would like to send funds from has been topped up via a testnet faucet.
Use the address output from the desired account.
Initiate a transaction using the following function:
send_tx(BTCTEST,{sender address from step 6},{receiving address},{amount})
Monitor the transaction on a block explorer.
Ethereum
Add one of the ETH addresses to the pre-allocated accounts in your networkname.json file.
Delete the geth folder in each node, then re-initialize using geth --datadir nodeX init networkname.json. This will create a new chain, and will pre-fund the new account.
Due to a bug in web3.py, you will need to send a transaction or two with MyCrypto first, since the w3.eth.generateGasPrice() function does not work with an empty chain. You can use one of the ETH address privkey, or one of the node keystore files.
Initiate a transaction using the following function:
send_tx(ETH,{sender address from step 6},{receiving address},{amount})
Monitor the transaction on MyCrypto by inputting the txid into the TX Status section.

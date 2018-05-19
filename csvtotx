import csv
import json
import os
import web3

reader = csv.reader(open('transfers.csv'))

trand = {}
private_key_for_senders_account = raw_input("You are about to send ether from your coinbase. What is your private key?")
for row in reader:
    csvid = row[0]
    csvamt = row[1]
    csvtxto = row[2]
    signed_txn = w3.eth.account.signTransaction(dict(
            nonce=w3.eth.getTransactionCount(w3.eth.coinbase),
            gasPrice=w3.eth.gasPrice,
            gas=100000,
            to= csvtxto ,
            value=csvamt,
            data=b'',
          ),
          private_key_for_senders_account,
        )
    w3.eth.sendRawTransaction(signed_txn.rawTransaction)
    '0xe670ec64341771606e55d6b4ca35a1a6b75ee3d5145a99d05921026d1527331'
    if csvid in trand:
        pass
    trand[csvid] = row[1:]

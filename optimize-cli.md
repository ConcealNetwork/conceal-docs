## Optimize your wallet

Depending on how much CCX you want to transfer, you might run into the error **Transaction size is too big, please optimize your wallet** or **Transaction is too big**. Often, this is because of a lot of small incoming transactions. With the command line **concealwallet**, you can optimize your wallet to send larger transactions, or a single big transaction. Like any other transaction on the network, you will need to wait for confirmation of the optimization transactions to spend those funds.

### Optimizing

The process of optimizing your wallet takes all your small incoming transactions and combines them into bigger ones by sending them to yourself. It is akin to replacing a handful of small currency bills with a single larger one. Once the process is complete you will be able to send larger transactions. There are three commands that help you optimize your wallet:

- **outputs** - This command shows your the total number of outputs in your wallet. The more outputs in your wallet, the more optimization your wallet will need to send large transactions. If you have less than 100 outputs, then you do not need to optimize your wallet.

```
[wallet ccx7Pz]: outputs
233
```

- **optimize** - When you run this command, it runs a single optimization round, usually reducing the number of outputs by a 100. You can do this over and over again until you can the desired amount.

```
[wallet ccx7Pz]: optimize
Money successfully sent, transaction c273bb88f7957c3bc25f79ff2494a30ffa226d3a06c95f3ba49eb4b6dc334e97
Transaction secret key 02464c66f23f077e9bd859e5aec87d2b8802f4f6871e860ee212398e8782cf0d
```

Then you will see that the number of outputs have reduced:

```
[wallet ccx7Pz]: outputs
136
```

- **optimize_all** - When you have thousands of ouputs or want to send one large transaction, that involves all or almost all of the funds in your wallet, then you can run this command. The command runs several optimization rounds at once. You will see the number of outputs and the number of optimization rounds that the process will run. Some wallets, with several thousand outputs will need several rounds of **optimize_all**. It depends on how much you want to send and how many outputs you have.

```
[wallet ccx7Pz]: optimize_all
Total outputs: 396
Total optimization rounds: 3
``

# Use the latest version of **concealwallet**



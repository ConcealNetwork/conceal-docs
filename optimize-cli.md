## Optimize your wallet

Depending on how much CCX you want to transfer, you might run into the error ```Transaction size is too big, please optimize your wallet``` or ```Transaction is too big```.
Often, this is because of a lot of small incoming transactions.

### Optimizing

The process of optimizing your wallet takes all your small incoming transactions and combines them into bigger ones by sending them to yourself. Once the process is complete you will be able to send larger transactions. There are three commands that help you optimize your wallet:

- outputs - This command shows your the total number of outputs in your wallet. The more you have, the optimization your wallet will need to send large transactions.

```[wallet ccx7Pz]: outputs
233```


- ```optimize``` - When you run this command, it runs a single optimization round, usually reducing the number of outputs by a 100. You can do this over and over again until you can the desired amount.
- ``optimize_all`` - When you want to send on large transactions, that involves all or almost all of the funds in your wallet, then you can run this command. The command runs several optimization rounds at once.

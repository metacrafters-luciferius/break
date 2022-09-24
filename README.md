## Differences between hello world and this example

The main difference is that the break example works on a lower level. It creates its own transaction objects and calculates the signature and serializes the transaction. The interaction with the blockchain happens directly via the RPC connection rather then using the built in method `sendAndConfirmTransaction` seen in the hello world example.

I do not really undertand what a `TrackedCommitment` is. My guess is, that the break example not only waits for the original transaction, but also any subsequent instruction (or transaction?) that happen after the original transaction. Additionally the break example will retry a transaction if there is a timeout or something like that.

As for the parameters both examples seem similar by using accounts, program id, fee payer account, ... In the break example there are a few more options such as the blockhash, which I think is similar to previous lessons where the last known blockhash is used to increase security.
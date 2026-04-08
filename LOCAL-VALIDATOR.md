# Using Local Validator with Phant Connect
More info: https://docs.phantom.com/sdks/react-sdk/sign-and-send-transaction

## is it possible to use phantom connect sdk with a custom rpc pointing to a local validator version of solana mainnet?

Yes, this is possible. The Phantom Connect SDK separates signing from sending. The SDK handles wallet connection and transaction signing, but you control the RPC endpoint used for building and sending transactions.

In the examples on the sign-and-send-transaction page, you can see the RPC is set by your app code (e.g., createSolanaRpc("https://api.mainnet-beta.solana.com")). You can replace that URL with your local validator endpoint (e.g., http://localhost:8899). Alternatively, use sdk.solana.signTransaction() to sign only, then submit via your own RPC connection.

```bash
https://docs.phantom.com/sdks/react-sdk/sign-and-send-transaction#solana-with-@solana/kit
```
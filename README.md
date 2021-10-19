# Warmup

## Deploy a contract

I am using Metamask. To deploy the contract, I simply had to validate the transaction
using Metamask.

## Call me

After deploying the contract, I used MyEtherWallet to interact with it.
I clicked `Access my wallet` -> `Browser extension`, and connected it with Metamask.
Then, `Contract` -> `Interact with contract`. I used the contract address provided
by CaptureTheEther. I copied the ABI from EtherScan
(search for the contract -> contract tab -> scroll down -> ABI).
Back to MyEtherWallet, I chose the "callMe" function, called it, signed the transaction.
Done!

## Choose a nickname

This time, I couldn't get the ABI from Etherscan.
Instead, I used Remix (online IDE). I created a single contract, where I copied and
paster the code from CaptureTheEther, and compiled it.
Then, in the `Deploy and run transactions` tab, I chose my compiled contract,
pasted the address of the deployed contract so I could interact with it.

I wanted my nickname to be github.com/tsauvajon. To do that, I needed to convert it
into bytes32. I ran:
```
npx bytes32 'github.com/tsauvajon'
```
which gave me `0x6769746875622e636f6d2f7473617576616a6f6e000000000000000000000000`.
I called the setNickname function with that `0x67...` input.

Note: Remix gas estimations were off, so I used Metamask suggestion instead.


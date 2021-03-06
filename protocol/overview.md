# Overview
The structure of LevSwap mainly consists of three parts: Tokens,Pricing,Swap, can be subdivided into five functional modules: token synthesis, token management, subject matter pricing, leverage ratio adjustment and dynamic rates.  

 ![Levswap架构图2](https://user-images.githubusercontent.com/79917064/110095868-5062eb00-7dd8-11eb-971e-6c40ede5addc.png)

### Synthetic tokens
The LevSwap platform introduces two kinds of synthetic tokens as long-short representatives of the subject matter of the transaction. Users directly open long/short positions by buying bull tokens and bear tokens, and close long/short positions by selling. The number of bull tokens and bear tokens represents the size of the corresponding positions of users, and the tokens are priced based on eth standard, so users can indirectly get the asset changes of eth standard through the balance of synthetic tokens.
### Governance tokens
The project will give rewards to the users who hold the position, and the rewards will be realized through the issuance of governance tokens. At the same time, in the adjustment of long-short ratio, price regression, will also be achieved through the issuance of governance tokens.
### Pricing
For the pricing of the subject matter, we use the oracle machine of UniSwap to avoid the risk of the subject matter price at the transaction level. The pricing of synthetic tokens will be determined by bull token and bear token pools.
### Leverage ratio
Each subject has a desired leverage ratio, which deviates from the powerful side in the case of long-short imbalance, until the long-short force is balanced and the leverage ratio returns to the original ratio. This can intuitively tell the trader that the rate of return of the current transaction.
### Dynamic fee
Fee is the main means to realize the long-short balance of leveraged trading. LevSwap uses dynamic fee. According to the current different long-to-empty ratio, LevSwap will update the poundage in real time when the user trades, to guide the multi-empty force back to balance. The adjustment is dynamic and directly reflects the strength of the current long/short force. 


# Dynamic Fund Fee
In an extreme unilateral market, the long and short power imbalance will cause the leverage ratio to deviate from the theoretical value. Therefore, it is necessary to adopt a dynamic fund fee to allow the strong market side to subsidize the weaker side to create arbitrage opportunities to achieve the return of long and short power in a balanced direction.  

Levswap charges dynamic fund fee by the deflation mechanism. For example, if the bulls in the current market are stronger, then the long-leveraged tokens in the market will be burned linearly according to time, and the burned value will be converted into ETH to subsidize short leveraged token holder.  

The dynamic fund fee is composed of two parts, namely the fixed interest and the long-short imbalance fee. The fixed interest is charged at a fixed rate for holding long or short leveraged tokens, and the long-short imbalance fee is used to balance the long and short power in the market.  

Long and short imbalance rate:
<div align=center><img width="195" alt="图片 13" src="https://user-images.githubusercontent.com/79917064/110098763-82298100-7ddb-11eb-95ea-95bb2a643456.png"></div>

Dynamic fund rate of long side:
 <div align=center><img width="217" alt="图片 14" src="https://user-images.githubusercontent.com/79917064/110098779-85247180-7ddb-11eb-9612-e8c507b2c4cc.png"></div>

Dynamic fund rate of short side:
 <div align=center><img width="216" alt="图片 15" src="https://user-images.githubusercontent.com/79917064/110098813-90779d00-7ddb-11eb-8e82-d241f2902670.png"></div>
 
LevSwap provides an interface to provide a one-click arbitrage interface for market makers. Arbitrageur can hold subsidized leveraged tokens in the protocol, and at the same time hedge unilateral risks in other markets, thereby obtaining a stable arbitrage mechanism to help balance the long and short market power.


# The Principle of Leveraged Token  

Leveraged token holders get excess returns compared to just holding spot through the increase in leveraged token prices.
Given that the price of leveraged token is y, the price of spot is x, and the leverage ratio is k, then the relationship between the price of leveraged token and spot should be as follows:
 <div align=center><img width="76" alt="图片 1" src="https://user-images.githubusercontent.com/79917064/110096700-28c05280-7dd9-11eb-825b-7a11b2aadc84.png"></div>

The theoretical relationship between the price of leveraged token and the spot price can be obtained by solving the above equation:
 <div align=center><img width="59" alt="图片 2" src="https://user-images.githubusercontent.com/79917064/110096708-2c53d980-7dd9-11eb-9710-a930e40b836b.png"></div>

While the price changes, long leveraged token holders and the short holders are counter-parties to each other in a zero-sum game, that is, in the rising market, all the profits of long come from the loss of short. The zero-sum game between long and short can be expressed by the following formula:
 <div align=center><img width="415" alt="图片 3" src="https://user-images.githubusercontent.com/79917064/110096746-37a70500-7dd9-11eb-9607-7b6110aa68d1.png"></div>

Given that the situation of spot, long and short leveraged token in the current market is shown in the table below:
 <div align=center><img width="415" alt="图片 4" src="https://user-images.githubusercontent.com/79917064/110096760-3bd32280-7dd9-11eb-8ca9-84cf4fe5c679.png"></div>

According to the constraints of the leveraged token price and zero-sum game, the following equations can be obtained:
 <div align=center><img width="207" alt="图片 5" src="https://user-images.githubusercontent.com/79917064/110096767-3ece1300-7dd9-11eb-8bc1-5594c90b81fb.png"></div>

By differentiating the formula, we get:
 <div align=center><img width="184" alt="图片 6" src="https://user-images.githubusercontent.com/79917064/110096775-42619a00-7dd9-11eb-96dc-0783e3dc70fe.png"></div>

By solving the above equations, we can get the relationship between the leveraged token’s price and the spot price:
 <div align=center><img width="166" alt="图片 7" src="https://user-images.githubusercontent.com/79917064/110096792-468db780-7dd9-11eb-9706-a1fdced93f46.png"></div>

We can get from the results that in order to ensure a zero-sum game between long and short, a dynamic leverage ratio, k1 and k2, is required. The leverage ratio depends on the current market forces (long and short). The current long and short market forces are:
 <div align=center><img width="138" alt="图片 8" src="https://user-images.githubusercontent.com/79917064/110096806-4a213e80-7dd9-11eb-955e-13d96aa53db1.png"></div>

If the leverage ratio of the leveraged token is 3X, it means that k1 = k2 = 3 in the long-short equilibrium. When the long and short forces are not equal, the leverage ratio fluctuates around 3. We can take the following values for the dynamic leverage ratio to ensure that the positive leverage ratio fluctuates around 3:
 <div align=center><img width="194" alt="图片 9" src="https://user-images.githubusercontent.com/79917064/110096822-4db4c580-7dd9-11eb-8bf1-359804505365.png"></div>

Through the above theoretical analysis, we have derived the theoretical model of leveraged tokens, and we have designed our leveraged token trading system using the above theoretical model.
We use the theoretical model to do a retrospective analysis of the price of BTC in 2020. The results are shown in the figure below. Obviously, if you hold BTC3XLONG leveraged coins, you can get several times the income of just holding BTC in 2020 and even in the extreme market on March 12, 2020, there was no forced liquidation.
 
<div align=center><img width="415" alt="图片 10" src="https://user-images.githubusercontent.com/79917064/110096841-52797980-7dd9-11eb-9fd3-c1d65bd93aca.png"></div>

# Leveraged Token Design

Levswap supports the synthesis and trading of leveraged token of any asset. We take BTC as an example to introduce the principle of leveraged token design. BTC 3x long leveraged token is named BTC-3X-LONG, and 3x short leveraged token named BTC-3X-SHORT.
  
Leveswap calculates the price of the leveraged token based on the current long/short market forces and the spot price queried from price oracles such as Chainlink, Uniswap, etc. Levswap gets prices from multiple oracle sources and calculates the time-weighted accumulated price as the spot price of the system to prevent price manipulation by whales.
 <div align=center><img width="415" alt="图片 11" src="https://user-images.githubusercontent.com/79917064/110097905-87d29700-7dda-11eb-9e12-6aa01f8044e1.png"></div>

Users can buy long or short leveraged tokens through ETH in Levswap. The process of buying leveraged tokens is equivalent to the protocol using ETH as collateral to issue leveraged token debts. Long and short leveraged tokens correspond to a common ETH collateral pool, when the price of leveraged tokens changes, the two parties holding long and short leveraged tokens will automatically become opponents of the game. While a user sells leveraged tokens, it is equivalent to redeeming ETH at the price of leveraged tokens. Through the above-mentioned buying and selling processes, it can be guaranteed that all leveraged tokens issued by Levswap are supported by ETH’s value.
<div align=center><img width="415" alt="图片 12" src="https://user-images.githubusercontent.com/79917064/110097989-a46ecf00-7dda-11eb-9b18-bbe09851912e.png"></div>


# Benzaiboten-spot-trading-bot
A trading bot easy to use to be linked to your favorite exchange to automatize the trading on cryptocurrencies

# <p align="center">BENZAIBOTEN<br>(a crypto trading optimizer bot)</p>
A bot to automatize the crypto trading on Binance (twin of [Daibotuten](https://github.com/mole3421278/Daibotuten-futures-trading-optimizer-bot))
# Warning: Do your own research to decide on which cryptocurrencies the bot should do trading (blacklist the other cryptocurrencies)
The bot finds the best cryptocurrencies to buy at each moment to resell them later. 

It uses an algorithm powered by AI to buy where an human would buy and at the same time trying to not stay with too much opened positions, so with it you don't have to worry about buying during the best moments.

It also shows to the user three indicators: 
- The fear and greed index of the current and previous day (lower values stand for fear and higher values stand for greed)
- The whale movements on chain
- The whale liquidations on the major exchanges (so to not be confused it with your own liquidations)

Use them to maximize the profit stopping and resuming the bot in the right times, following your own strategy.

There is also a display of the usdt balance, with a percentage about the daily profit (each day the percentage is reset), and you can click on the open positions you have to be redirected to the webpage of the chart.

Finally, the bot will notice you if a new version is available for the download.

# Settings
The bot leaves a high margin of customization to the user, to fit different strategies: you can change the settings whenever you think the market has changed, so do your own research to maximize the returns from it.

You can also leave the bot with its own standard settings if you are a newbie.


| Command  | Description | Possible Values |
| ------------- | ------------- | ------------- |
| **AMOUNT PER POSITION** | To choose how much to put at maximum in each position: in order to let the bot work well it is RECOMMENDED to have at LEAST 30 times the value you put here, so, if you choose 20 usdt it is RECOMMENDED that you have at least 600 usdt in the futures funds. However, it isn't a strict rule and so you can run the bot even with only 50 usdt. | The minimum value is 15 usdt and the maximum value is 50 usdt. |
| **PROFIT TO LEAVE** | To decide what percentage of the profit made with a cryptocurrency to leave in that cryptocurrency instead of converting everything back to usdt (if the profit is too low, everything is converted back to usdt in any case). | The minimum value is 0%, to sell all the quantity previously bought regardless of the profit done, and the maximum value is 100%, to sell only the quantity to cover the cost incurred when bought and to retain all the profit done in the cryptocurrency bought). |
| **STOP LOSS** | To decide when to close a position in case of loss. The bot has its own mechanism to take care of the potential loss, but you can overwrite it with this command. | The minimum value is 0% and it stands for "don't use stop loss" and the maximum value is 40%. |
| **TAKE PROFIT** | To decide when to close a position in case of profit. The bot has its own mechanism to take care of the potential profit, but you can overwrite it with this command. | The minimum value is 0% and it stands for "don't use take profit" and the maximum value is 30%. |
| **DON'T BUY IF BTC IS** | To force the bot to NOT buy ANYTHING if the price of BTC is over a certain threshold starting from the time in which it is set. | The minimum value is -10% and the maximum value is 10%. Put it to 0.0% to disable this behaviour. |
| **DON'T BUY IF ALT IS** | To force the bot to NOT buy the cryptocurrency if its price is over a certain threshold starting from the time in which it is set. | The minimum value is -30% and the maximum value is 30%. Put it to 0.0% to disable this behaviour. |
| **DON'T BUY FOR** | To force the bot to NOT buy the cryptocurrency for a certain interval of time | The minimum value is 0 hours and the maximum value is 12 hours. Put it to 0.0 hours to disable this behaviour. |
| **BUY IF CRASH OF** | To force the bot to buy ONLY IF in the last hour the price crashed from the maximum value to the current one of at least the percentage chosen | The minimum value is 0.0% hours and the maximum value is (-)15%. Put it to 0.0 to disable this behaviour. |
| **STOP AT NEXT WHALE LONG LIQUIDATION** | To stop the bot when there is a new whale long liquidation. The whale long liquidations can be seen in the bottom part of the bot, together with the whale short liquidations. | |
| **CLOSE** | To sell a cryptocurrency previously bought by the bot just by clicking a button: the bot is set to close them in the moment that it is the best for it, but if you want to close them before that moment, you can do it. | |
| **BLACKLIST** | To exclude certain cryptocurrencies to be bought by the bot depending on your own research just by typing their ticker symbol (so BTC for bitcoin) and then pressing ENTER. | All the tickers allowable to be traded that you haven't yet blacklisted (for example: ETH, BTC...). You can type ALL to blacklist every crypto, to whitelist only the ones that you want. Don't type other things here. |
| **WHITELIST** | To add again to the list of the bot a cryptocurrency that you excluded before just by typing its ticker symbol and then pressing ENTER. | All the tickers that you have previously blacklisted. You can type ALL to whitelist every crypto. Don't type other things here. |
| **STOP/RESUME** | To stop the bot with this button if you believe the market is entering in a bubble or in a big market crash, so you don't want to buy anything in that period. Clicking it again the bot will start to buy again. | |

# Activation
The first time you open the bot it will be in the STATUS UNLINKED.

To start the bot the first time you need to link it to an API key: paste your API key and your API secret where required **after** having paid the **fee to link it + the monthly fee (15 usdt in total)**, otherwise the API key won't be registered.
To create the API key go to https://www.binance.com/en/my/settings/api-management and be sure to put a tick on: 
- Enable Spot & Margin Trading

If you don't know how to create your API key, follow this simple guide: https://www.binance.com/en/support/faq/360002502072

After having linked the API key to the bot it will pass to the STATUS ACTIVE: at this point it will start to buy and sell following the settings you chose to use, that you can change while it runs. **Don't close its windows** otherwise it will shut down and you will have to open it again.

Each 30 days the bot pass to the STATUS INACTIVE: you have to **pay the fee for running the bot (10 usdt each month)**, as explained better below, to use the bot each month.

**DON'T DELETE OR MOVE THE FILE settings_bot.txt otherwise you will have to activate the bot again**

# Devs Fee
There is a **fee of 5 usdt to link the API key to the bot (to pay only the first time you use the bot together with the monthly fee)**.

There is a **fee of 10 usdt monthly to run the bot (10 usdt each 30 days, so 0.33 usdt/day)**.

The fees must be paid **manually** directly by the user because **the bot does NOT have the ability to withdraw funds** (to be able to withdraw funds, the API key must have a tick on Enable Withdrawals, but, as written before, the bot doesn't require to have it).

If the fees are not paid the bot simply doesn't work and it returns to the STATUS INACTIVE. If, passed some months, you want to use again the bot, you have only to pay the monthly fee for the next 30 days (the months during which you haven't paid the fees don't have to be paid when you return to use the bot).

To pay the fee you can send **the equivalent of 15 usdt** for the first time (activation + monthly fee) or **the equivalent of 10 usdt** for the other times (for the monthly fee) to one of the following addresses at your own choice:

| Address  | Crypto | Blockchain |
| ------------- | ------------- | ---------- |
| ```0x7Ee897EBa5Df317e426Ec18397fBfA293E31fbD5```  | Fantom (FTM)  | Fantom Network |
| ```io148yvz30p2k3jr9shupm8tvp475fyc7936qpafy```  | IOTeX (IOTX)  | IOTeX Network |
| ```TFrQ9hfueNT5EBaAnTeBru8Wg2H9dKQRxY``` | Tron (TRX) | Tron Network |
| ```zil1gsutt32yrtvvmqv3rkjy75e55xneg5z4kve9uz``` | Zilliqa (ZIL) | Zilliqa Network |
| ```0x2fa72451f159e2b52859bf44f6f5e9651e83ca35``` | VeChain (VET) | VeChain Network |
| ```1UCgbZqt53pWHSZxCiQGXYsc3pqtmHcon9rReeeQDwY``` | Solana (SOL) | Solana Network |
| ```RH1aLSgnq7RSenGHpRPRKKCqWwSmA8wgjF``` | Ravencoin (RVN) | Ravencoin Network |

**Be sure to send the fees to the right address and blockchain, otherwise the amount will be lost. Also, DO NOT send usdt, but the equivalent of the required amount in the crypto you have chosen between one of the list.** If you send less than the right amount the bot won't work and you will have to send the total amount again (so, for example don't send for the monthly fee 4 usdt and then 6 usdt because they doesn't count as 10 usdt: just send an unique transaction with 10 usdt).

For example: if the current price of FTM is 2 usdt, you can send 7.5 FTM (that are the equivalent of 15 usdt), to activate the bot. Don't send 15 usdt in the Fantom Network or in the other blockchain.

If you don't know how to send crypto, follow this simple guide: https://www.binance.com/en/support/faq/115003670492

It is possible to send tips to help the project, so greater amount than the right ones are considered correct as well (for example 11 usdt instead of 10).

# Requirements

The bot runs entirely in local, so it is important that the device where you install it has a good internet connection, otherwise you can incur in misbehaviour.

<p align="center"><img src="https://user-images.githubusercontent.com/91144525/140513103-88c402c6-772a-42f0-b4de-e88afe8469bc.png" width="720"></p>
<p align="center"><img src="https://user-images.githubusercontent.com/91144525/140513132-24b7c7c4-e017-49be-b400-f8440f70382e.png" width="720"></p>




# Notes

It can be that there are some minor bugs here and there. Please, do report them if you find them to improve the project.

If you have proposals to improve the project don't hesitate to post them.

For the moment it is in development a version for Windows.

In the future it will be expanded:
- to other exchanges;
- to other OS (first of all Android).

Please, use this repository to check for the updates.

If you intend to use also [Daibotuten](https://github.com/mole3421278/Daibotuten-futures-trading-optimizer-bot) you don't have to pay for it separately: the dev fee to pay is the same, so for 10 usdt per month you can use both of them.

# Latest release

https://github.com/mole3421278/Benzaiboten-spot-trading-bot/releases/latest


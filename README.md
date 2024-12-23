## Traidy

### Description
This project is trading bot which allows you to trade using implemented strategies, but also you can define your own strategies.

### Instalation 

For downloading please go to the [releases](https://github.com/Lumberj3ck/TradingBot/releases)

Jar file require for you to have a .env file in the root file along with jar file.

```bash
   └───tradingApp  
           ├───TradingBot.jar
           ├───TradingBotGUI.jar  
           ├───.env
```

.env file is required for the trading bot to access the API. Since storing API keys in the public repository would be impractical, you would need to follow the link provided in our project report and download the .env file with the test account and API keys. You need to place the .env file into the same folder as the jar file.

Run jar file:
```bash
java -jar TradingBot.jar
```

### Logging 

In order to see more logging output, set the logging level in log4j2.xml file inside of resourses folder to debug mode. For decreasing logging output set higher level of logging for example error. 


Goals:  
Create abstractions to create freely strategies


Strategies to implement:

1. Chatgpt strategy
2. SMA + RSI


Under discussion:

1. Discuss if we should decouple TradingExecutor from Abstract Strategy.  Because Strategy is supposed to be only responsible for entering market or exiting market, everything else is done by TradingExecutor ✅
2. Discuss if we should move strategies to specfical folder ❌


TODO:

1. Move isPositionOpen from strategy to Executor ✅
2. Update hardcoded functionality (amount) ✅
3. When strategy is initialised we can decide which tradingBroker should we use we can for example use test and may use papertrading implementation ✅
4. Add logging ✅
5. Add a bigger list of stocks ✅
6. make alpaca api url more changeable ❌ 
7. Add stops orders for buying ✅
8. Tweak hourly and daily strategies' parameters for more accurate result (google the actual strategies for reference) ❌
9. add ability to buy more when the trend is still going up ❌


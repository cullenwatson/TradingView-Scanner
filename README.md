# Roadmap
Phase 1 - tradingview connection
1. ~~Sign into TradingView and solve the captcha~~
* ~~Save the cookies in case restart of program~~
2. ~~Start websocket connection to TradingView~~
   * fetch the exchange automatically to just input a ticker
3. Load desired chart template
4. Load desired stock symbols and timeframe

5. Receive and parse stock feed and custom indicator data
6. Support concurrent connection feeds to multiple stock symbols


### why not other repos for phase 1

- they dont auto sign into acc
- they dont give custom indicator values that are only available in your acc (private scripts)

Phase 2
1. Connect to unusualwhales or cheddarflow
2. Allow custom tracking / filters

Phase 3
1. Connect the TradingView and unusualwhale microservice
2. Alert if both are confluent

Phase 4
1. ThinkOrSwim microservice
2. Auto purchase the option
3. Highly configurable for the trades desired
4. set take profit / stop loss and monitor win rate



usage
```go
func main() {
	LoadEnvVars()

	authToken := GetAuthToken()

	symbol := "AAPL"
	timeframe := "1D"
	candles := 100

	client := CreateTradingViewClient(symbol, timeframe, candles, authToken)

	RunTradingViewClient(client)
}
```

## Market Status

=== "Java"
    ```java
    Alphavantage.api()
        .marketStatus()
        .onSuccess(response -> onData(response))
        .fetch();
    ```
=== "Kotlin"
    ```kotlin
    Alphavantage.api()
        .marketStatus()
        .onSuccess { response -> onData(response) }
        .fetch()
    ```

**Response Type:**
`MarketStatusResponse`

### Response

=== "Java"
    ```java
    public void onData(MarketStatusResponse response){
        response.getMarkets().forEach(market -> {
            System.out.println(market.getMarketType());
            System.out.println(market.getRegion());
            System.out.println(market.getPrimaryExchanges());
            System.out.println(market.getLocalOpen());
            System.out.println(market.getLocalClose());
            System.out.println(market.getCurrentStatus());
            System.out.println(market.getNotes());
        });
    }
    ```
=== "Kotlin"
    ```kotlin
    fun onData(response: MarketStatusResponse) {
        response.markets.forEach { market ->
            println(market.marketType)
            println(market.region)
            println(market.primaryExchanges)
            println(market.localOpen)
            println(market.localClose)
            println(market.currentStatus)
            println(market.notes)
        }
    }
    ```

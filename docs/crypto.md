## Digital Currencies

### Defaults

```txt
dataType: DataType.JSON
```

### Intraday

=== "Java"
    ```java
    Alphavantage.api()
        .crypto()
        .intraday()
        .forSymbol("BTC")
        .market("USD")
        .interval(Interval.FIVE_MIN)
        .outputSize(OutputSize.FULL)
        .dataType(DataType.JSON)
        .onSuccess(e -> onData(e.getCryptoUnits()))
        .fetch();
    ```
=== "Kotlin"
    ```kotlin
    Alphavantage.api()
        .crypto()
        .intraday()
        .forSymbol("BTC")
        .market("USD")
        .interval(Interval.FIVE_MIN)
        .outputSize(OutputSize.FULL)
        .dataType(DataType.JSON)
        .onSuccess { e -> onData(e.cryptoUnits) }
        .fetch()
    ```

**Response Type:**
`CryptoResponse`

### Daily

=== "Java"
    ```java
    Alphavantage.api()
        .crypto()
        .daily()
        .forSymbol("BTC")
        .market("CNY")
        .onSuccess(e -> onData(e.getCryptoUnits()))
        .fetch();
    ```
=== "Kotlin"
    ```kotlin
    Alphavantage.api()
        .crypto()
        .daily()
        .forSymbol("BTC")
        .market("CNY")
        .onSuccess { e -> onData(e.cryptoUnits) }
        .fetch()
    ```

### Weekly

=== "Java"
    ```java
    Alphavantage.api()
        .crypto()
        .weekly()
        .forSymbol("BTC")
        .market("USD")
        .onSuccess(e -> onData(e.getCryptoUnits()))
        .fetch();
    ```
=== "Kotlin"
    ```kotlin
    Alphavantage.api()
        .crypto()
        .weekly()
        .forSymbol("BTC")
        .market("USD")
        .onSuccess { e -> onData(e.cryptoUnits) }
        .fetch()
    ```

### Monthly

=== "Java"
    ```java
    Alphavantage.api()
        .crypto()
        .monthly()
        .forSymbol("BTC")
        .market("USD")
        .onSuccess(e -> onData(e.getCryptoUnits()))
        .fetch();
    ```
=== "Kotlin"
    ```kotlin
    Alphavantage.api()
        .crypto()
        .monthly()
        .forSymbol("BTC")
        .market("USD")
        .onSuccess { e -> onData(e.cryptoUnits) }
        .fetch()
    ```

**Response Type:**
`CryptoResponse`

### Response

=== "Java"
    ```java
    public void onData(List<CryptoUnit> cryptoUnits){
        cryptoUnits.stream().forEach(u -> {
            System.out.println(u.getHigh());
            System.out.println(u.getLow());
            System.out.println(u.getOpen());
            System.out.println(u.getClose());
            System.out.println(u.getHighUSD());
            System.out.println(u.getLowUSD());
            System.out.println(u.getOpenUSD());
            System.out.println(u.getCloseUSD());
            System.out.println(u.getVolume());
            System.out.println(u.getMarketCap());
            System.out.println(u.getDate());
        });
    }
    ```
=== "Kotlin"
    ```kotlin
    fun onData(cryptoUnits: List<CryptoUnit>) {
        cryptoUnits.forEach { u ->
            println(u.high)
            println(u.low)
            println(u.open)
            println(u.close)
            println(u.highUSD)
            println(u.lowUSD)
            println(u.openUSD)
            println(u.closeUSD)
            println(u.volume)
            println(u.marketCap)
            println(u.date)
        }
    }
    ```

## Health Index

=== "Java"
    ```java
    Alphavantage.api()
        .crypto()
        .rating()
        .forSymbol("BTC")
        .onSuccess(e -> onData(e))
        .fetch();
    ```
=== "Kotlin"
    ```kotlin
    Alphavantage.api()
        .crypto()
        .rating()
        .forSymbol("BTC")
        .onSuccess { e -> onData(e) }
        .fetch()
    ```

**Response Type:**
`RatingResponse`

### Response

=== "Java"
    ```java
    public void onData(RatingResponse response){
        System.out.println(response.getSymbol());
        System.out.println(response.getName());
        System.out.println(response.getFcasRating());
        System.out.println(response.getFcasScore());
        System.out.println(response.getDeveloperScore());
        System.out.println(response.getMarketMaturityScore());
        System.out.println(response.getUtilityScore());
        System.out.println(response.getLastRefreshed());
        System.out.println(response.getTimeZone());
    }
    ```
=== "Kotlin"
    ```kotlin
    fun onData(response: RatingResponse) {
        println(response.symbol)
        println(response.name)
        println(response.fcasRating)
        println(response.fcasScore)
        println(response.developerScore)
        println(response.marketMaturityScore)
        println(response.utilityScore)
        println(response.lastRefreshed)
        println(response.timeZone)
    }
    ```
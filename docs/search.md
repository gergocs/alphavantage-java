### Synchronous Fetch 

=== ":material-language-java: Java"
    ```java
    Alphavantage.api()
      .search()
      .keywords("tesla")
      .onSuccess(response -> onData(response.getBestMatches()))
      .fetch();
    ```
=== ":material-language-kotlin: Kotlin"
    ```kotlin
    Alphavantage.api()
        .search()
        .keywords("tesla")
        .onSuccess { response -> onData(response.bestMatches) }
        .fetch()
    ```

### Asynchronous Fetch

=== ":material-language-java: Java"
    ```java
    SearchResponse response = Alphavantage.api()
      .search()
      .keywords("tesla")
      .fetchSync();
    ```
=== ":material-language-kotlin: Kotlin"
    ```kotlin
    val response = Alphavantage.api()
        .search()
        .keywords("tesla")
        .fetchSync()
    ```


### Response `SearchResponse`

=== ":material-language-java: Java"
    ```java
    public void onData(List<Match> matches){
        matches.forEach(match -> {
            System.out.println(match.getSymbol());
            System.out.println(match.getName());
            System.out.println(match.getType());
            System.out.println(match.getRegion());
            System.out.println(match.getMarketOpen());
            System.out.println(match.getMarketClose());
            System.out.println(match.getTimezone());
            System.out.println(match.getCurrency());
            System.out.println(match.getMatchScore());
        });
    }
    ```
=== ":material-language-kotlin: Kotlin"
    ```kotlin
    fun onData(matches: List<Match>) {
        matches.forEach { match ->
            println(match.symbol)
            println(match.name)
            println(match.type)
            println(match.region)
            println(match.marketOpen)
            println(match.marketClose)
            println(match.timezone)
            println(match.currency)
            println(match.matchScore)
        }
    }
    ```

[alphavantage] / [marketstatus] / MarketStatus

# `MarketStatus`
`public final class MarketStatus implements Fetcher`

Client api for the global market status utility.

### Constructors

| Name              | Summary                              |
|-------------------|--------------------------------------|
| [MarketStatus](#) | `public MarketStatus(Config config)` |

### Methods

| Name           | Summary                                                                         |
|----------------|---------------------------------------------------------------------------------|
| [onSuccess](#) | `public MarketStatus onSuccess(SuccessCallback<MarketStatusResponse> callback)` |
| [onFailure](#) | `public MarketStatus onFailure(FailureCallback callback)`                       |
| [fetch](#)     | `public void fetch()`                                                           |
| [fetchSync](#) | `public MarketStatusResponse fetchSync()`                                       |

[alphavantage]: ../alphavantage/index.md
[marketstatus]: ./index.md
[request]: request/index.md
[response]: response/index.md

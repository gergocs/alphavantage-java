[alphavantage] / [search] / Search

# `Search`
`public final class Search implements Fetcher`

Client api for the ticker or symbol search utility.


### Constructors

| Name        | Summary                              |
|-------------|--------------------------------------|
| [Search](#) | `public class Search(Config config)` |

### Methods

| Name           | Summary                                                             |
|----------------|---------------------------------------------------------------------|
| [keywords](#)  | `public Search keywords(String keywords)`                           |
| [onSuccess](#) | `public Search onSuccess(SuccessCallback<SearchResponse> callback)` |
| [onFailure](#) | `public Search onFailure(FailureCallback callback)`                 |
| [fetch](#)     | `public void fetch()`                                               |
| [fetchSync](#) | `public SearchResponse fetchSync()`                                 |


[alphavantage]: ../alphavantage/index.md
[search]: ./index.md
[request]: request/index.md
[response]: request/index.md

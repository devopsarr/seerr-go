# \WatchlistAPI

All URIs are relative to *http://localhost:5055/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateWatchlist**](WatchlistAPI.md#CreateWatchlist) | **Post** /watchlist | Add media to watchlist
[**DeleteWatchlist**](WatchlistAPI.md#DeleteWatchlist) | **Delete** /watchlist/{tmdbId} | Delete watchlist item



## CreateWatchlist

> Watchlist CreateWatchlist(ctx).Watchlist(watchlist).Execute()

Add media to watchlist

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	seerrClient "github.com/devopsarr/seerr-go/seerr"
)

func main() {
	watchlist := *seerrClient.NewWatchlist() // Watchlist | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.WatchlistAPI.CreateWatchlist(context.Background()).Watchlist(watchlist).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `WatchlistAPI.CreateWatchlist``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateWatchlist`: Watchlist
	fmt.Fprintf(os.Stdout, "Response from `WatchlistAPI.CreateWatchlist`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateWatchlistRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **watchlist** | [**Watchlist**](Watchlist.md) |  | 

### Return type

[**Watchlist**](Watchlist.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteWatchlist

> DeleteWatchlist(ctx, tmdbId).MediaType(mediaType).Execute()

Delete watchlist item



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	seerrClient "github.com/devopsarr/seerr-go/seerr"
)

func main() {
	tmdbId := "1" // string | tmdbId ID
	mediaType := "mediaType_example" // string | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	r, err := apiClient.WatchlistAPI.DeleteWatchlist(context.Background(), tmdbId).MediaType(mediaType).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `WatchlistAPI.DeleteWatchlist``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**tmdbId** | **string** | tmdbId ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteWatchlistRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **mediaType** | **string** |  | 

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


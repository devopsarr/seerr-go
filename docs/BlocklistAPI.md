# \BlocklistAPI

All URIs are relative to *http://localhost:5055/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateBlacklist**](BlocklistAPI.md#CreateBlacklist) | **Post** /blacklist | Add media to blocklist
[**CreateBlocklist**](BlocklistAPI.md#CreateBlocklist) | **Post** /blocklist | Add media to blocklist
[**CreateBlocklistCollectionByCollectionId**](BlocklistAPI.md#CreateBlocklistCollectionByCollectionId) | **Post** /blocklist/collection/{collectionId} | Add collection to blocklist
[**DeleteBlacklist**](BlocklistAPI.md#DeleteBlacklist) | **Delete** /blacklist/{tmdbId} | Remove media from blocklist
[**DeleteBlocklist**](BlocklistAPI.md#DeleteBlocklist) | **Delete** /blocklist/{tmdbId} | Remove media from blocklist
[**DeleteBlocklistCollection**](BlocklistAPI.md#DeleteBlocklistCollection) | **Delete** /blocklist/collection/{collectionId} | Remove collection from blocklist
[**GetBlacklist**](BlocklistAPI.md#GetBlacklist) | **Get** /blacklist | Returns blocklisted items
[**GetBlacklistByTmdbId**](BlocklistAPI.md#GetBlacklistByTmdbId) | **Get** /blacklist/{tmdbId} | Get media from blocklist
[**GetBlocklist**](BlocklistAPI.md#GetBlocklist) | **Get** /blocklist | Returns blocklisted items
[**GetBlocklistByTmdbId**](BlocklistAPI.md#GetBlocklistByTmdbId) | **Get** /blocklist/{tmdbId} | Get media from blocklist



## CreateBlacklist

> CreateBlacklist(ctx).Blocklist(blocklist).Execute()

Add media to blocklist



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
	blocklist := *seerrClient.NewBlocklist() // Blocklist | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	r, err := apiClient.BlocklistAPI.CreateBlacklist(context.Background()).Blocklist(blocklist).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlocklistAPI.CreateBlacklist``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateBlacklistRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **blocklist** | [**Blocklist**](Blocklist.md) |  | 

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateBlocklist

> CreateBlocklist(ctx).Blocklist(blocklist).Execute()

Add media to blocklist

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
	blocklist := *seerrClient.NewBlocklist() // Blocklist | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	r, err := apiClient.BlocklistAPI.CreateBlocklist(context.Background()).Blocklist(blocklist).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlocklistAPI.CreateBlocklist``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateBlocklistRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **blocklist** | [**Blocklist**](Blocklist.md) |  | 

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateBlocklistCollectionByCollectionId

> CreateBlocklistCollectionByCollectionId(ctx, collectionId).Body(body).Execute()

Add collection to blocklist



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
	collectionId := "1424991" // string | Collection ID
	body := map[string]interface{}{ ... } // map[string]interface{} |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	r, err := apiClient.BlocklistAPI.CreateBlocklistCollectionByCollectionId(context.Background(), collectionId).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlocklistAPI.CreateBlocklistCollectionByCollectionId``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**collectionId** | **string** | Collection ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateBlocklistCollectionByCollectionIdRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **body** | **map[string]interface{}** |  | 

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteBlacklist

> DeleteBlacklist(ctx, tmdbId).MediaType(mediaType).Execute()

Remove media from blocklist



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
	r, err := apiClient.BlocklistAPI.DeleteBlacklist(context.Background(), tmdbId).MediaType(mediaType).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlocklistAPI.DeleteBlacklist``: %v\n", err)
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

Other parameters are passed through a pointer to a apiDeleteBlacklistRequest struct via the builder pattern


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


## DeleteBlocklist

> DeleteBlocklist(ctx, tmdbId).MediaType(mediaType).Execute()

Remove media from blocklist

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
	r, err := apiClient.BlocklistAPI.DeleteBlocklist(context.Background(), tmdbId).MediaType(mediaType).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlocklistAPI.DeleteBlocklist``: %v\n", err)
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

Other parameters are passed through a pointer to a apiDeleteBlocklistRequest struct via the builder pattern


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


## DeleteBlocklistCollection

> DeleteBlocklistCollection(ctx, collectionId).Execute()

Remove collection from blocklist



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
	collectionId := "1424991" // string | Collection ID

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	r, err := apiClient.BlocklistAPI.DeleteBlocklistCollection(context.Background(), collectionId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlocklistAPI.DeleteBlocklistCollection``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**collectionId** | **string** | Collection ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteBlocklistCollectionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


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


## GetBlacklist

> GetBlocklist2XXResponse GetBlacklist(ctx).Take(take).Skip(skip).Search(search).Filter(filter).Execute()

Returns blocklisted items



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
	take := float32(25) // float32 |  (optional)
	skip := float32(0) // float32 |  (optional)
	search := "dune" // string |  (optional)
	filter := "filter_example" // string |  (optional) (default to "manual")

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.BlocklistAPI.GetBlacklist(context.Background()).Take(take).Skip(skip).Search(search).Filter(filter).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlocklistAPI.GetBlacklist``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetBlacklist`: GetBlocklist2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `BlocklistAPI.GetBlacklist`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetBlacklistRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **take** | **float32** |  | 
 **skip** | **float32** |  | 
 **search** | **string** |  | 
 **filter** | **string** |  | [default to &quot;manual&quot;]

### Return type

[**GetBlocklist2XXResponse**](GetBlocklist2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetBlacklistByTmdbId

> GetBlacklistByTmdbId(ctx, tmdbId).MediaType(mediaType).Execute()

Get media from blocklist



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
	r, err := apiClient.BlocklistAPI.GetBlacklistByTmdbId(context.Background(), tmdbId).MediaType(mediaType).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlocklistAPI.GetBlacklistByTmdbId``: %v\n", err)
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

Other parameters are passed through a pointer to a apiGetBlacklistByTmdbIdRequest struct via the builder pattern


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


## GetBlocklist

> GetBlocklist2XXResponse GetBlocklist(ctx).Take(take).Skip(skip).Search(search).Filter(filter).Execute()

Returns blocklisted items



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
	take := float32(25) // float32 |  (optional)
	skip := float32(0) // float32 |  (optional)
	search := "dune" // string |  (optional)
	filter := "filter_example" // string |  (optional) (default to "manual")

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.BlocklistAPI.GetBlocklist(context.Background()).Take(take).Skip(skip).Search(search).Filter(filter).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlocklistAPI.GetBlocklist``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetBlocklist`: GetBlocklist2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `BlocklistAPI.GetBlocklist`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetBlocklistRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **take** | **float32** |  | 
 **skip** | **float32** |  | 
 **search** | **string** |  | 
 **filter** | **string** |  | [default to &quot;manual&quot;]

### Return type

[**GetBlocklist2XXResponse**](GetBlocklist2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetBlocklistByTmdbId

> GetBlocklistByTmdbId(ctx, tmdbId).MediaType(mediaType).Execute()

Get media from blocklist

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
	r, err := apiClient.BlocklistAPI.GetBlocklistByTmdbId(context.Background(), tmdbId).MediaType(mediaType).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlocklistAPI.GetBlocklistByTmdbId``: %v\n", err)
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

Other parameters are passed through a pointer to a apiGetBlocklistByTmdbIdRequest struct via the builder pattern


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


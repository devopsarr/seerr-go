# \OverrideruleAPI

All URIs are relative to *http://localhost:5055/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateOverriderule**](OverrideruleAPI.md#CreateOverriderule) | **Post** /overrideRule | Create override rule
[**DeleteOverriderule**](OverrideruleAPI.md#DeleteOverriderule) | **Delete** /overrideRule/{ruleId} | Delete override rule by ID
[**ListOverriderule**](OverrideruleAPI.md#ListOverriderule) | **Get** /overrideRule | Get override rules
[**UpdateOverriderule**](OverrideruleAPI.md#UpdateOverriderule) | **Put** /overrideRule/{ruleId} | Update override rule



## CreateOverriderule

> []OverrideRule CreateOverriderule(ctx).Execute()

Create override rule



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

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.OverrideruleAPI.CreateOverriderule(context.Background()).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OverrideruleAPI.CreateOverriderule``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateOverriderule`: []OverrideRule
	fmt.Fprintf(os.Stdout, "Response from `OverrideruleAPI.CreateOverriderule`: %v\n", resp)
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to a apiCreateOverrideruleRequest struct via the builder pattern


### Return type

[**[]OverrideRule**](OverrideRule.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteOverriderule

> OverrideRule DeleteOverriderule(ctx, ruleId).Execute()

Delete override rule by ID



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
	ruleId := float32(8.14) // float32 | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.OverrideruleAPI.DeleteOverriderule(context.Background(), ruleId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OverrideruleAPI.DeleteOverriderule``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DeleteOverriderule`: OverrideRule
	fmt.Fprintf(os.Stdout, "Response from `OverrideruleAPI.DeleteOverriderule`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**ruleId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteOverrideruleRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**OverrideRule**](OverrideRule.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListOverriderule

> []OverrideRule ListOverriderule(ctx).Execute()

Get override rules



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

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.OverrideruleAPI.ListOverriderule(context.Background()).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OverrideruleAPI.ListOverriderule``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListOverriderule`: []OverrideRule
	fmt.Fprintf(os.Stdout, "Response from `OverrideruleAPI.ListOverriderule`: %v\n", resp)
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to a apiListOverrideruleRequest struct via the builder pattern


### Return type

[**[]OverrideRule**](OverrideRule.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateOverriderule

> []OverrideRule UpdateOverriderule(ctx, ruleId).Execute()

Update override rule



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
	ruleId := float32(8.14) // float32 | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.OverrideruleAPI.UpdateOverriderule(context.Background(), ruleId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `OverrideruleAPI.UpdateOverriderule``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateOverriderule`: []OverrideRule
	fmt.Fprintf(os.Stdout, "Response from `OverrideruleAPI.UpdateOverriderule`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**ruleId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateOverrideruleRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**[]OverrideRule**](OverrideRule.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


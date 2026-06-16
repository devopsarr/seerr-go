# \AuthAPI

All URIs are relative to *http://localhost:5055/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateAuthJellyfin**](AuthAPI.md#CreateAuthJellyfin) | **Post** /auth/jellyfin | Sign in using a Jellyfin username and password
[**CreateAuthLocal**](AuthAPI.md#CreateAuthLocal) | **Post** /auth/local | Sign in using a local account
[**CreateAuthLogout**](AuthAPI.md#CreateAuthLogout) | **Post** /auth/logout | Sign out and clear session cookie
[**CreateAuthPlex**](AuthAPI.md#CreateAuthPlex) | **Post** /auth/plex | Sign in using a Plex token
[**GetAuthMe**](AuthAPI.md#GetAuthMe) | **Get** /auth/me | Get logged-in user



## CreateAuthJellyfin

> User CreateAuthJellyfin(ctx).CreateAuthJellyfinRequest(createAuthJellyfinRequest).Execute()

Sign in using a Jellyfin username and password



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
	createAuthJellyfinRequest := *seerrClient.NewCreateAuthJellyfinRequest("Username_example", "Password_example") // CreateAuthJellyfinRequest | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthAPI.CreateAuthJellyfin(context.Background()).CreateAuthJellyfinRequest(createAuthJellyfinRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.CreateAuthJellyfin``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateAuthJellyfin`: User
	fmt.Fprintf(os.Stdout, "Response from `AuthAPI.CreateAuthJellyfin`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateAuthJellyfinRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createAuthJellyfinRequest** | [**CreateAuthJellyfinRequest**](CreateAuthJellyfinRequest.md) |  | 

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateAuthLocal

> User CreateAuthLocal(ctx).CreateAuthLocalRequest(createAuthLocalRequest).Execute()

Sign in using a local account



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
	createAuthLocalRequest := *seerrClient.NewCreateAuthLocalRequest("Email_example", "Password_example") // CreateAuthLocalRequest | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthAPI.CreateAuthLocal(context.Background()).CreateAuthLocalRequest(createAuthLocalRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.CreateAuthLocal``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateAuthLocal`: User
	fmt.Fprintf(os.Stdout, "Response from `AuthAPI.CreateAuthLocal`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateAuthLocalRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createAuthLocalRequest** | [**CreateAuthLocalRequest**](CreateAuthLocalRequest.md) |  | 

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateAuthLogout

> CreateAuthLogout2XXResponse CreateAuthLogout(ctx).Execute()

Sign out and clear session cookie



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
	resp, r, err := apiClient.AuthAPI.CreateAuthLogout(context.Background()).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.CreateAuthLogout``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateAuthLogout`: CreateAuthLogout2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `AuthAPI.CreateAuthLogout`: %v\n", resp)
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to a apiCreateAuthLogoutRequest struct via the builder pattern


### Return type

[**CreateAuthLogout2XXResponse**](CreateAuthLogout2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateAuthPlex

> User CreateAuthPlex(ctx).CreateAuthPlexRequest(createAuthPlexRequest).Execute()

Sign in using a Plex token



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
	createAuthPlexRequest := *seerrClient.NewCreateAuthPlexRequest("AuthToken_example") // CreateAuthPlexRequest | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthAPI.CreateAuthPlex(context.Background()).CreateAuthPlexRequest(createAuthPlexRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.CreateAuthPlex``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateAuthPlex`: User
	fmt.Fprintf(os.Stdout, "Response from `AuthAPI.CreateAuthPlex`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateAuthPlexRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createAuthPlexRequest** | [**CreateAuthPlexRequest**](CreateAuthPlexRequest.md) |  | 

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAuthMe

> User GetAuthMe(ctx).Execute()

Get logged-in user



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
	resp, r, err := apiClient.AuthAPI.GetAuthMe(context.Background()).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.GetAuthMe``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetAuthMe`: User
	fmt.Fprintf(os.Stdout, "Response from `AuthAPI.GetAuthMe`: %v\n", resp)
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to a apiGetAuthMeRequest struct via the builder pattern


### Return type

[**User**](User.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


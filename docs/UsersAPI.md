# \UsersAPI

All URIs are relative to *http://localhost:5055/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateAuthResetPassword**](UsersAPI.md#CreateAuthResetPassword) | **Post** /auth/reset-password | Send a reset password email
[**CreateAuthResetPasswordByGuid**](UsersAPI.md#CreateAuthResetPasswordByGuid) | **Post** /auth/reset-password/{guid} | Reset the password for a user
[**CreateUser**](UsersAPI.md#CreateUser) | **Post** /user | Create new user
[**CreateUserImportFromJellyfin**](UsersAPI.md#CreateUserImportFromJellyfin) | **Post** /user/import-from-jellyfin | Import all users from Jellyfin
[**CreateUserImportFromPlex**](UsersAPI.md#CreateUserImportFromPlex) | **Post** /user/import-from-plex | Import all users from Plex
[**CreateUserRegisterPushSubscription**](UsersAPI.md#CreateUserRegisterPushSubscription) | **Post** /user/registerPushSubscription | Register a web push /user/registerPushSubscription
[**CreateUserSettingsLinkedAccountsJellyfin**](UsersAPI.md#CreateUserSettingsLinkedAccountsJellyfin) | **Post** /user/{userId}/settings/linked-accounts/jellyfin | Link the provided Jellyfin account to the current user
[**CreateUserSettingsLinkedAccountsPlex**](UsersAPI.md#CreateUserSettingsLinkedAccountsPlex) | **Post** /user/{userId}/settings/linked-accounts/plex | Link the provided Plex account to the current user
[**CreateUserSettingsMain**](UsersAPI.md#CreateUserSettingsMain) | **Post** /user/{userId}/settings/main | Update general settings for a user
[**CreateUserSettingsNotifications**](UsersAPI.md#CreateUserSettingsNotifications) | **Post** /user/{userId}/settings/notifications | Update notification settings for a user
[**CreateUserSettingsPassword**](UsersAPI.md#CreateUserSettingsPassword) | **Post** /user/{userId}/settings/password | Update password for a user
[**CreateUserSettingsPermissions**](UsersAPI.md#CreateUserSettingsPermissions) | **Post** /user/{userId}/settings/permissions | Update permission settings for a user
[**DeleteUser**](UsersAPI.md#DeleteUser) | **Delete** /user/{userId} | Delete user by ID
[**DeleteUserPushSubscription**](UsersAPI.md#DeleteUserPushSubscription) | **Delete** /user/{userId}/pushSubscription/{endpoint} | Delete user push subscription by key
[**DeleteUserSettingsLinkedAccountsJellyfin**](UsersAPI.md#DeleteUserSettingsLinkedAccountsJellyfin) | **Delete** /user/{userId}/settings/linked-accounts/jellyfin | Remove the linked Jellyfin account for a user
[**DeleteUserSettingsLinkedAccountsPlex**](UsersAPI.md#DeleteUserSettingsLinkedAccountsPlex) | **Delete** /user/{userId}/settings/linked-accounts/plex | Remove the linked Plex account for a user
[**GetUser**](UsersAPI.md#GetUser) | **Get** /user | Get all users
[**GetUserByUserId**](UsersAPI.md#GetUserByUserId) | **Get** /user/{userId} | Get user by ID
[**GetUserJellyfinByJellyfinUserId**](UsersAPI.md#GetUserJellyfinByJellyfinUserId) | **Get** /user/jellyfin/{jellyfinUserId} | Get user by Jellyfin user ID
[**GetUserPushSubscriptionByEndpoint**](UsersAPI.md#GetUserPushSubscriptionByEndpoint) | **Get** /user/{userId}/pushSubscription/{endpoint} | Get web push notification settings for a user
[**GetUserPushSubscriptions**](UsersAPI.md#GetUserPushSubscriptions) | **Get** /user/{userId}/pushSubscriptions | Get all web push notification settings for a user
[**GetUserQuota**](UsersAPI.md#GetUserQuota) | **Get** /user/{userId}/quota | Get quotas for a specific user
[**GetUserRequests**](UsersAPI.md#GetUserRequests) | **Get** /user/{userId}/requests | Get requests for a specific user
[**GetUserSettingsMain**](UsersAPI.md#GetUserSettingsMain) | **Get** /user/{userId}/settings/main | Get general settings for a user
[**GetUserSettingsNotifications**](UsersAPI.md#GetUserSettingsNotifications) | **Get** /user/{userId}/settings/notifications | Get notification settings for a user
[**GetUserSettingsPassword**](UsersAPI.md#GetUserSettingsPassword) | **Get** /user/{userId}/settings/password | Get password page informatiom
[**GetUserSettingsPermissions**](UsersAPI.md#GetUserSettingsPermissions) | **Get** /user/{userId}/settings/permissions | Get permission settings for a user
[**GetUserWatchData**](UsersAPI.md#GetUserWatchData) | **Get** /user/{userId}/watch_data | Get watch data
[**GetUserWatchlist**](UsersAPI.md#GetUserWatchlist) | **Get** /user/{userId}/watchlist | Get the Plex watchlist for a specific user
[**PutUser**](UsersAPI.md#PutUser) | **Put** /user | Update batch of users
[**UpdateUser**](UsersAPI.md#UpdateUser) | **Put** /user/{userId} | Update a user by user ID



## CreateAuthResetPassword

> CreateAuthLogout2XXResponse CreateAuthResetPassword(ctx).CreateAuthResetPasswordRequest(createAuthResetPasswordRequest).Execute()

Send a reset password email



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
	createAuthResetPasswordRequest := *seerrClient.NewCreateAuthResetPasswordRequest("Email_example") // CreateAuthResetPasswordRequest | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.CreateAuthResetPassword(context.Background()).CreateAuthResetPasswordRequest(createAuthResetPasswordRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.CreateAuthResetPassword``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateAuthResetPassword`: CreateAuthLogout2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.CreateAuthResetPassword`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateAuthResetPasswordRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createAuthResetPasswordRequest** | [**CreateAuthResetPasswordRequest**](CreateAuthResetPasswordRequest.md) |  | 

### Return type

[**CreateAuthLogout2XXResponse**](CreateAuthLogout2XXResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateAuthResetPasswordByGuid

> CreateAuthLogout2XXResponse CreateAuthResetPasswordByGuid(ctx, guid).CreateAuthResetPasswordByGuidRequest(createAuthResetPasswordByGuidRequest).Execute()

Reset the password for a user



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
	guid := "9afef5a7-ec89-4d5f-9397-261e96970b50" // string | 
	createAuthResetPasswordByGuidRequest := *seerrClient.NewCreateAuthResetPasswordByGuidRequest("Password_example") // CreateAuthResetPasswordByGuidRequest | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.CreateAuthResetPasswordByGuid(context.Background(), guid).CreateAuthResetPasswordByGuidRequest(createAuthResetPasswordByGuidRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.CreateAuthResetPasswordByGuid``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateAuthResetPasswordByGuid`: CreateAuthLogout2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.CreateAuthResetPasswordByGuid`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**guid** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateAuthResetPasswordByGuidRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **createAuthResetPasswordByGuidRequest** | [**CreateAuthResetPasswordByGuidRequest**](CreateAuthResetPasswordByGuidRequest.md) |  | 

### Return type

[**CreateAuthLogout2XXResponse**](CreateAuthLogout2XXResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateUser

> User CreateUser(ctx).CreateUserRequest(createUserRequest).Execute()

Create new user



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
	createUserRequest := *seerrClient.NewCreateUserRequest() // CreateUserRequest | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.CreateUser(context.Background()).CreateUserRequest(createUserRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.CreateUser``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateUser`: User
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.CreateUser`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateUserRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createUserRequest** | [**CreateUserRequest**](CreateUserRequest.md) |  | 

### Return type

[**User**](User.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateUserImportFromJellyfin

> []User CreateUserImportFromJellyfin(ctx).CreateUserImportFromJellyfinRequest(createUserImportFromJellyfinRequest).Execute()

Import all users from Jellyfin



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
	createUserImportFromJellyfinRequest := *seerrClient.NewCreateUserImportFromJellyfinRequest() // CreateUserImportFromJellyfinRequest |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.CreateUserImportFromJellyfin(context.Background()).CreateUserImportFromJellyfinRequest(createUserImportFromJellyfinRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.CreateUserImportFromJellyfin``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateUserImportFromJellyfin`: []User
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.CreateUserImportFromJellyfin`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateUserImportFromJellyfinRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createUserImportFromJellyfinRequest** | [**CreateUserImportFromJellyfinRequest**](CreateUserImportFromJellyfinRequest.md) |  | 

### Return type

[**[]User**](User.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateUserImportFromPlex

> []User CreateUserImportFromPlex(ctx).CreateUserImportFromPlexRequest(createUserImportFromPlexRequest).Execute()

Import all users from Plex



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
	createUserImportFromPlexRequest := *seerrClient.NewCreateUserImportFromPlexRequest() // CreateUserImportFromPlexRequest |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.CreateUserImportFromPlex(context.Background()).CreateUserImportFromPlexRequest(createUserImportFromPlexRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.CreateUserImportFromPlex``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateUserImportFromPlex`: []User
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.CreateUserImportFromPlex`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateUserImportFromPlexRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createUserImportFromPlexRequest** | [**CreateUserImportFromPlexRequest**](CreateUserImportFromPlexRequest.md) |  | 

### Return type

[**[]User**](User.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateUserRegisterPushSubscription

> CreateUserRegisterPushSubscription(ctx).CreateUserRegisterPushSubscriptionRequest(createUserRegisterPushSubscriptionRequest).Execute()

Register a web push /user/registerPushSubscription



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
	createUserRegisterPushSubscriptionRequest := *seerrClient.NewCreateUserRegisterPushSubscriptionRequest("Endpoint_example", "Auth_example", "P256dh_example") // CreateUserRegisterPushSubscriptionRequest | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	r, err := apiClient.UsersAPI.CreateUserRegisterPushSubscription(context.Background()).CreateUserRegisterPushSubscriptionRequest(createUserRegisterPushSubscriptionRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.CreateUserRegisterPushSubscription``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateUserRegisterPushSubscriptionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createUserRegisterPushSubscriptionRequest** | [**CreateUserRegisterPushSubscriptionRequest**](CreateUserRegisterPushSubscriptionRequest.md) |  | 

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


## CreateUserSettingsLinkedAccountsJellyfin

> CreateUserSettingsLinkedAccountsJellyfin(ctx, userId).CreateUserSettingsLinkedAccountsJellyfinRequest(createUserSettingsLinkedAccountsJellyfinRequest).Execute()

Link the provided Jellyfin account to the current user



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
	userId := float32(8.14) // float32 | 
	createUserSettingsLinkedAccountsJellyfinRequest := *seerrClient.NewCreateUserSettingsLinkedAccountsJellyfinRequest() // CreateUserSettingsLinkedAccountsJellyfinRequest | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	r, err := apiClient.UsersAPI.CreateUserSettingsLinkedAccountsJellyfin(context.Background(), userId).CreateUserSettingsLinkedAccountsJellyfinRequest(createUserSettingsLinkedAccountsJellyfinRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.CreateUserSettingsLinkedAccountsJellyfin``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateUserSettingsLinkedAccountsJellyfinRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **createUserSettingsLinkedAccountsJellyfinRequest** | [**CreateUserSettingsLinkedAccountsJellyfinRequest**](CreateUserSettingsLinkedAccountsJellyfinRequest.md) |  | 

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


## CreateUserSettingsLinkedAccountsPlex

> CreateUserSettingsLinkedAccountsPlex(ctx, userId).CreateAuthPlexRequest(createAuthPlexRequest).Execute()

Link the provided Plex account to the current user



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
	userId := float32(8.14) // float32 | 
	createAuthPlexRequest := *seerrClient.NewCreateAuthPlexRequest("AuthToken_example") // CreateAuthPlexRequest | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	r, err := apiClient.UsersAPI.CreateUserSettingsLinkedAccountsPlex(context.Background(), userId).CreateAuthPlexRequest(createAuthPlexRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.CreateUserSettingsLinkedAccountsPlex``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateUserSettingsLinkedAccountsPlexRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **createAuthPlexRequest** | [**CreateAuthPlexRequest**](CreateAuthPlexRequest.md) |  | 

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


## CreateUserSettingsMain

> UserSettings CreateUserSettingsMain(ctx, userId).UserSettings(userSettings).Execute()

Update general settings for a user



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
	userId := float32(8.14) // float32 | 
	userSettings := *seerrClient.NewUserSettings() // UserSettings | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.CreateUserSettingsMain(context.Background(), userId).UserSettings(userSettings).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.CreateUserSettingsMain``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateUserSettingsMain`: UserSettings
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.CreateUserSettingsMain`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateUserSettingsMainRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **userSettings** | [**UserSettings**](UserSettings.md) |  | 

### Return type

[**UserSettings**](UserSettings.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateUserSettingsNotifications

> UserSettingsNotifications CreateUserSettingsNotifications(ctx, userId).UserSettingsNotifications(userSettingsNotifications).Execute()

Update notification settings for a user



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
	userId := float32(8.14) // float32 | 
	userSettingsNotifications := *seerrClient.NewUserSettingsNotifications() // UserSettingsNotifications | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.CreateUserSettingsNotifications(context.Background(), userId).UserSettingsNotifications(userSettingsNotifications).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.CreateUserSettingsNotifications``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateUserSettingsNotifications`: UserSettingsNotifications
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.CreateUserSettingsNotifications`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateUserSettingsNotificationsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **userSettingsNotifications** | [**UserSettingsNotifications**](UserSettingsNotifications.md) |  | 

### Return type

[**UserSettingsNotifications**](UserSettingsNotifications.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateUserSettingsPassword

> CreateUserSettingsPassword(ctx, userId).CreateUserSettingsPasswordRequest(createUserSettingsPasswordRequest).Execute()

Update password for a user



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
	userId := float32(8.14) // float32 | 
	createUserSettingsPasswordRequest := *seerrClient.NewCreateUserSettingsPasswordRequest("NewPassword_example") // CreateUserSettingsPasswordRequest | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	r, err := apiClient.UsersAPI.CreateUserSettingsPassword(context.Background(), userId).CreateUserSettingsPasswordRequest(createUserSettingsPasswordRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.CreateUserSettingsPassword``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateUserSettingsPasswordRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **createUserSettingsPasswordRequest** | [**CreateUserSettingsPasswordRequest**](CreateUserSettingsPasswordRequest.md) |  | 

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


## CreateUserSettingsPermissions

> GetUserSettingsPermissions2XXResponse CreateUserSettingsPermissions(ctx, userId).CreateUserSettingsPermissionsRequest(createUserSettingsPermissionsRequest).Execute()

Update permission settings for a user



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
	userId := float32(8.14) // float32 | 
	createUserSettingsPermissionsRequest := *seerrClient.NewCreateUserSettingsPermissionsRequest(float32(123)) // CreateUserSettingsPermissionsRequest | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.CreateUserSettingsPermissions(context.Background(), userId).CreateUserSettingsPermissionsRequest(createUserSettingsPermissionsRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.CreateUserSettingsPermissions``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateUserSettingsPermissions`: GetUserSettingsPermissions2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.CreateUserSettingsPermissions`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateUserSettingsPermissionsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **createUserSettingsPermissionsRequest** | [**CreateUserSettingsPermissionsRequest**](CreateUserSettingsPermissionsRequest.md) |  | 

### Return type

[**GetUserSettingsPermissions2XXResponse**](GetUserSettingsPermissions2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteUser

> User DeleteUser(ctx, userId).Execute()

Delete user by ID



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
	userId := float32(8.14) // float32 | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.DeleteUser(context.Background(), userId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.DeleteUser``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DeleteUser`: User
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.DeleteUser`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteUserRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


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


## DeleteUserPushSubscription

> DeleteUserPushSubscription(ctx, userId, endpoint).Execute()

Delete user push subscription by key



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
	userId := float32(8.14) // float32 | 
	endpoint := "endpoint_example" // string | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	r, err := apiClient.UsersAPI.DeleteUserPushSubscription(context.Background(), userId, endpoint).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.DeleteUserPushSubscription``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 
**endpoint** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteUserPushSubscriptionRequest struct via the builder pattern


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


## DeleteUserSettingsLinkedAccountsJellyfin

> DeleteUserSettingsLinkedAccountsJellyfin(ctx, userId).Execute()

Remove the linked Jellyfin account for a user



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
	userId := float32(8.14) // float32 | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	r, err := apiClient.UsersAPI.DeleteUserSettingsLinkedAccountsJellyfin(context.Background(), userId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.DeleteUserSettingsLinkedAccountsJellyfin``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteUserSettingsLinkedAccountsJellyfinRequest struct via the builder pattern


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


## DeleteUserSettingsLinkedAccountsPlex

> DeleteUserSettingsLinkedAccountsPlex(ctx, userId).Execute()

Remove the linked Plex account for a user



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
	userId := float32(8.14) // float32 | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	r, err := apiClient.UsersAPI.DeleteUserSettingsLinkedAccountsPlex(context.Background(), userId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.DeleteUserSettingsLinkedAccountsPlex``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteUserSettingsLinkedAccountsPlexRequest struct via the builder pattern


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


## GetUser

> GetUser2XXResponse GetUser(ctx).Take(take).Skip(skip).Sort(sort).SortDirection(sortDirection).Q(q).IncludeIds(includeIds).Execute()

Get all users



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
	take := float32(20) // float32 |  (optional)
	skip := float32(0) // float32 |  (optional)
	sort := "sort_example" // string |  (optional) (default to "created")
	sortDirection := "sortDirection_example" // string | Sort direction. When omitted, the server chooses the direction per sort field (e.g. displayname defaults to asc, requests/updated to desc).  (optional)
	q := "q_example" // string |  (optional)
	includeIds := "includeIds_example" // string |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.GetUser(context.Background()).Take(take).Skip(skip).Sort(sort).SortDirection(sortDirection).Q(q).IncludeIds(includeIds).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.GetUser``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUser`: GetUser2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.GetUser`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetUserRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **take** | **float32** |  | 
 **skip** | **float32** |  | 
 **sort** | **string** |  | [default to &quot;created&quot;]
 **sortDirection** | **string** | Sort direction. When omitted, the server chooses the direction per sort field (e.g. displayname defaults to asc, requests/updated to desc).  | 
 **q** | **string** |  | 
 **includeIds** | **string** |  | 

### Return type

[**GetUser2XXResponse**](GetUser2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetUserByUserId

> User GetUserByUserId(ctx, userId).Execute()

Get user by ID



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
	userId := float32(8.14) // float32 | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.GetUserByUserId(context.Background(), userId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.GetUserByUserId``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUserByUserId`: User
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.GetUserByUserId`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetUserByUserIdRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


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


## GetUserJellyfinByJellyfinUserId

> User GetUserJellyfinByJellyfinUserId(ctx, jellyfinUserId).Execute()

Get user by Jellyfin user ID



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
	jellyfinUserId := "jellyfinUserId_example" // string | The Jellyfin user ID (32-character hexadecimal string)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.GetUserJellyfinByJellyfinUserId(context.Background(), jellyfinUserId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.GetUserJellyfinByJellyfinUserId``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUserJellyfinByJellyfinUserId`: User
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.GetUserJellyfinByJellyfinUserId`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**jellyfinUserId** | **string** | The Jellyfin user ID (32-character hexadecimal string) | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetUserJellyfinByJellyfinUserIdRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


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


## GetUserPushSubscriptionByEndpoint

> GetUserPushSubscriptions2XXResponse GetUserPushSubscriptionByEndpoint(ctx, userId, endpoint).Execute()

Get web push notification settings for a user



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
	userId := float32(8.14) // float32 | 
	endpoint := "endpoint_example" // string | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.GetUserPushSubscriptionByEndpoint(context.Background(), userId, endpoint).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.GetUserPushSubscriptionByEndpoint``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUserPushSubscriptionByEndpoint`: GetUserPushSubscriptions2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.GetUserPushSubscriptionByEndpoint`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 
**endpoint** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetUserPushSubscriptionByEndpointRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**GetUserPushSubscriptions2XXResponse**](GetUserPushSubscriptions2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetUserPushSubscriptions

> GetUserPushSubscriptions2XXResponse GetUserPushSubscriptions(ctx, userId).Execute()

Get all web push notification settings for a user



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
	userId := float32(8.14) // float32 | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.GetUserPushSubscriptions(context.Background(), userId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.GetUserPushSubscriptions``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUserPushSubscriptions`: GetUserPushSubscriptions2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.GetUserPushSubscriptions`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetUserPushSubscriptionsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**GetUserPushSubscriptions2XXResponse**](GetUserPushSubscriptions2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetUserQuota

> GetUserQuota2XXResponse GetUserQuota(ctx, userId).Execute()

Get quotas for a specific user



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
	userId := float32(8.14) // float32 | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.GetUserQuota(context.Background(), userId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.GetUserQuota``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUserQuota`: GetUserQuota2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.GetUserQuota`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetUserQuotaRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**GetUserQuota2XXResponse**](GetUserQuota2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetUserRequests

> GetUserRequests2XXResponse GetUserRequests(ctx, userId).Take(take).Skip(skip).Execute()

Get requests for a specific user



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
	userId := float32(8.14) // float32 | 
	take := float32(20) // float32 |  (optional)
	skip := float32(0) // float32 |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.GetUserRequests(context.Background(), userId).Take(take).Skip(skip).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.GetUserRequests``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUserRequests`: GetUserRequests2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.GetUserRequests`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetUserRequestsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **take** | **float32** |  | 
 **skip** | **float32** |  | 

### Return type

[**GetUserRequests2XXResponse**](GetUserRequests2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetUserSettingsMain

> UserSettings GetUserSettingsMain(ctx, userId).Execute()

Get general settings for a user



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
	userId := float32(8.14) // float32 | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.GetUserSettingsMain(context.Background(), userId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.GetUserSettingsMain``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUserSettingsMain`: UserSettings
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.GetUserSettingsMain`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetUserSettingsMainRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**UserSettings**](UserSettings.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetUserSettingsNotifications

> UserSettingsNotifications GetUserSettingsNotifications(ctx, userId).Execute()

Get notification settings for a user



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
	userId := float32(8.14) // float32 | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.GetUserSettingsNotifications(context.Background(), userId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.GetUserSettingsNotifications``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUserSettingsNotifications`: UserSettingsNotifications
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.GetUserSettingsNotifications`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetUserSettingsNotificationsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**UserSettingsNotifications**](UserSettingsNotifications.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetUserSettingsPassword

> GetUserSettingsPassword2XXResponse GetUserSettingsPassword(ctx, userId).Execute()

Get password page informatiom



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
	userId := float32(8.14) // float32 | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.GetUserSettingsPassword(context.Background(), userId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.GetUserSettingsPassword``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUserSettingsPassword`: GetUserSettingsPassword2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.GetUserSettingsPassword`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetUserSettingsPasswordRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**GetUserSettingsPassword2XXResponse**](GetUserSettingsPassword2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetUserSettingsPermissions

> GetUserSettingsPermissions2XXResponse GetUserSettingsPermissions(ctx, userId).Execute()

Get permission settings for a user



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
	userId := float32(8.14) // float32 | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.GetUserSettingsPermissions(context.Background(), userId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.GetUserSettingsPermissions``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUserSettingsPermissions`: GetUserSettingsPermissions2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.GetUserSettingsPermissions`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetUserSettingsPermissionsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**GetUserSettingsPermissions2XXResponse**](GetUserSettingsPermissions2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetUserWatchData

> GetUserWatchData2XXResponse GetUserWatchData(ctx, userId).Execute()

Get watch data



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
	userId := float32(8.14) // float32 | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.GetUserWatchData(context.Background(), userId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.GetUserWatchData``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUserWatchData`: GetUserWatchData2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.GetUserWatchData`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetUserWatchDataRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**GetUserWatchData2XXResponse**](GetUserWatchData2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetUserWatchlist

> GetUserWatchlist2XXResponse GetUserWatchlist(ctx, userId).Page(page).Execute()

Get the Plex watchlist for a specific user



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
	userId := float32(8.14) // float32 | 
	page := float32(1) // float32 |  (optional) (default to 1)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.GetUserWatchlist(context.Background(), userId).Page(page).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.GetUserWatchlist``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetUserWatchlist`: GetUserWatchlist2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.GetUserWatchlist`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetUserWatchlistRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **page** | **float32** |  | [default to 1]

### Return type

[**GetUserWatchlist2XXResponse**](GetUserWatchlist2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PutUser

> []User PutUser(ctx).PutUserRequest(putUserRequest).Execute()

Update batch of users



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
	putUserRequest := *seerrClient.NewPutUserRequest() // PutUserRequest | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.PutUser(context.Background()).PutUserRequest(putUserRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.PutUser``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PutUser`: []User
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.PutUser`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPutUserRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **putUserRequest** | [**PutUserRequest**](PutUserRequest.md) |  | 

### Return type

[**[]User**](User.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateUser

> User UpdateUser(ctx, userId).User(user).Execute()

Update a user by user ID



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
	userId := float32(8.14) // float32 | 
	user := *seerrClient.NewUser(int32(1), "hey@itsme.com", "2020-09-02T05:02:23.000Z", "2020-09-02T05:02:23.000Z") // User | 

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.UsersAPI.UpdateUser(context.Background(), userId).User(user).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `UsersAPI.UpdateUser``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateUser`: User
	fmt.Fprintf(os.Stdout, "Response from `UsersAPI.UpdateUser`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**userId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateUserRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **user** | [**User**](User.md) |  | 

### Return type

[**User**](User.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


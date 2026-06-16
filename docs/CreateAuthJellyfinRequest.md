# CreateAuthJellyfinRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Username** | **string** |  | 
**Password** | **string** |  | 
**Hostname** | Pointer to **string** |  | [optional] 
**Email** | Pointer to **string** |  | [optional] 
**ServerType** | Pointer to **float32** |  | [optional] 

## Methods

### NewCreateAuthJellyfinRequest

`func NewCreateAuthJellyfinRequest(username string, password string, ) *CreateAuthJellyfinRequest`

NewCreateAuthJellyfinRequest instantiates a new CreateAuthJellyfinRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCreateAuthJellyfinRequestWithDefaults

`func NewCreateAuthJellyfinRequestWithDefaults() *CreateAuthJellyfinRequest`

NewCreateAuthJellyfinRequestWithDefaults instantiates a new CreateAuthJellyfinRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUsername

`func (o *CreateAuthJellyfinRequest) GetUsername() string`

GetUsername returns the Username field if non-nil, zero value otherwise.

### GetUsernameOk

`func (o *CreateAuthJellyfinRequest) GetUsernameOk() (*string, bool)`

GetUsernameOk returns a tuple with the Username field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUsername

`func (o *CreateAuthJellyfinRequest) SetUsername(v string)`

SetUsername sets Username field to given value.


### GetPassword

`func (o *CreateAuthJellyfinRequest) GetPassword() string`

GetPassword returns the Password field if non-nil, zero value otherwise.

### GetPasswordOk

`func (o *CreateAuthJellyfinRequest) GetPasswordOk() (*string, bool)`

GetPasswordOk returns a tuple with the Password field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPassword

`func (o *CreateAuthJellyfinRequest) SetPassword(v string)`

SetPassword sets Password field to given value.


### GetHostname

`func (o *CreateAuthJellyfinRequest) GetHostname() string`

GetHostname returns the Hostname field if non-nil, zero value otherwise.

### GetHostnameOk

`func (o *CreateAuthJellyfinRequest) GetHostnameOk() (*string, bool)`

GetHostnameOk returns a tuple with the Hostname field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHostname

`func (o *CreateAuthJellyfinRequest) SetHostname(v string)`

SetHostname sets Hostname field to given value.

### HasHostname

`func (o *CreateAuthJellyfinRequest) HasHostname() bool`

HasHostname returns a boolean if a field has been set.

### GetEmail

`func (o *CreateAuthJellyfinRequest) GetEmail() string`

GetEmail returns the Email field if non-nil, zero value otherwise.

### GetEmailOk

`func (o *CreateAuthJellyfinRequest) GetEmailOk() (*string, bool)`

GetEmailOk returns a tuple with the Email field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEmail

`func (o *CreateAuthJellyfinRequest) SetEmail(v string)`

SetEmail sets Email field to given value.

### HasEmail

`func (o *CreateAuthJellyfinRequest) HasEmail() bool`

HasEmail returns a boolean if a field has been set.

### GetServerType

`func (o *CreateAuthJellyfinRequest) GetServerType() float32`

GetServerType returns the ServerType field if non-nil, zero value otherwise.

### GetServerTypeOk

`func (o *CreateAuthJellyfinRequest) GetServerTypeOk() (*float32, bool)`

GetServerTypeOk returns a tuple with the ServerType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetServerType

`func (o *CreateAuthJellyfinRequest) SetServerType(v float32)`

SetServerType sets ServerType field to given value.

### HasServerType

`func (o *CreateAuthJellyfinRequest) HasServerType() bool`

HasServerType returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



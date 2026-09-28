# CreateOverrideruleAdvancedRequestRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MediaType** | **string** |  | 
**TmdbId** | **float32** |  | 
**Is4k** | Pointer to **bool** |  | [optional] 
**RequestId** | Pointer to **NullableFloat32** |  | [optional] 
**RequestUser** | Pointer to **NullableFloat32** |  | [optional] 
**Tags** | Pointer to **[]float32** |  | [optional] 
**ServiceId** | Pointer to **NullableFloat32** |  | [optional] 

## Methods

### NewCreateOverrideruleAdvancedRequestRequest

`func NewCreateOverrideruleAdvancedRequestRequest(mediaType string, tmdbId float32, ) *CreateOverrideruleAdvancedRequestRequest`

NewCreateOverrideruleAdvancedRequestRequest instantiates a new CreateOverrideruleAdvancedRequestRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCreateOverrideruleAdvancedRequestRequestWithDefaults

`func NewCreateOverrideruleAdvancedRequestRequestWithDefaults() *CreateOverrideruleAdvancedRequestRequest`

NewCreateOverrideruleAdvancedRequestRequestWithDefaults instantiates a new CreateOverrideruleAdvancedRequestRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMediaType

`func (o *CreateOverrideruleAdvancedRequestRequest) GetMediaType() string`

GetMediaType returns the MediaType field if non-nil, zero value otherwise.

### GetMediaTypeOk

`func (o *CreateOverrideruleAdvancedRequestRequest) GetMediaTypeOk() (*string, bool)`

GetMediaTypeOk returns a tuple with the MediaType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMediaType

`func (o *CreateOverrideruleAdvancedRequestRequest) SetMediaType(v string)`

SetMediaType sets MediaType field to given value.


### GetTmdbId

`func (o *CreateOverrideruleAdvancedRequestRequest) GetTmdbId() float32`

GetTmdbId returns the TmdbId field if non-nil, zero value otherwise.

### GetTmdbIdOk

`func (o *CreateOverrideruleAdvancedRequestRequest) GetTmdbIdOk() (*float32, bool)`

GetTmdbIdOk returns a tuple with the TmdbId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTmdbId

`func (o *CreateOverrideruleAdvancedRequestRequest) SetTmdbId(v float32)`

SetTmdbId sets TmdbId field to given value.


### GetIs4k

`func (o *CreateOverrideruleAdvancedRequestRequest) GetIs4k() bool`

GetIs4k returns the Is4k field if non-nil, zero value otherwise.

### GetIs4kOk

`func (o *CreateOverrideruleAdvancedRequestRequest) GetIs4kOk() (*bool, bool)`

GetIs4kOk returns a tuple with the Is4k field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIs4k

`func (o *CreateOverrideruleAdvancedRequestRequest) SetIs4k(v bool)`

SetIs4k sets Is4k field to given value.

### HasIs4k

`func (o *CreateOverrideruleAdvancedRequestRequest) HasIs4k() bool`

HasIs4k returns a boolean if a field has been set.

### GetRequestId

`func (o *CreateOverrideruleAdvancedRequestRequest) GetRequestId() float32`

GetRequestId returns the RequestId field if non-nil, zero value otherwise.

### GetRequestIdOk

`func (o *CreateOverrideruleAdvancedRequestRequest) GetRequestIdOk() (*float32, bool)`

GetRequestIdOk returns a tuple with the RequestId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequestId

`func (o *CreateOverrideruleAdvancedRequestRequest) SetRequestId(v float32)`

SetRequestId sets RequestId field to given value.

### HasRequestId

`func (o *CreateOverrideruleAdvancedRequestRequest) HasRequestId() bool`

HasRequestId returns a boolean if a field has been set.

### SetRequestIdNil

`func (o *CreateOverrideruleAdvancedRequestRequest) SetRequestIdNil(b bool)`

 SetRequestIdNil sets the value for RequestId to be an explicit nil

### UnsetRequestId
`func (o *CreateOverrideruleAdvancedRequestRequest) UnsetRequestId()`

UnsetRequestId ensures that no value is present for RequestId, not even an explicit nil
### GetRequestUser

`func (o *CreateOverrideruleAdvancedRequestRequest) GetRequestUser() float32`

GetRequestUser returns the RequestUser field if non-nil, zero value otherwise.

### GetRequestUserOk

`func (o *CreateOverrideruleAdvancedRequestRequest) GetRequestUserOk() (*float32, bool)`

GetRequestUserOk returns a tuple with the RequestUser field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequestUser

`func (o *CreateOverrideruleAdvancedRequestRequest) SetRequestUser(v float32)`

SetRequestUser sets RequestUser field to given value.

### HasRequestUser

`func (o *CreateOverrideruleAdvancedRequestRequest) HasRequestUser() bool`

HasRequestUser returns a boolean if a field has been set.

### SetRequestUserNil

`func (o *CreateOverrideruleAdvancedRequestRequest) SetRequestUserNil(b bool)`

 SetRequestUserNil sets the value for RequestUser to be an explicit nil

### UnsetRequestUser
`func (o *CreateOverrideruleAdvancedRequestRequest) UnsetRequestUser()`

UnsetRequestUser ensures that no value is present for RequestUser, not even an explicit nil
### GetTags

`func (o *CreateOverrideruleAdvancedRequestRequest) GetTags() []float32`

GetTags returns the Tags field if non-nil, zero value otherwise.

### GetTagsOk

`func (o *CreateOverrideruleAdvancedRequestRequest) GetTagsOk() (*[]float32, bool)`

GetTagsOk returns a tuple with the Tags field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTags

`func (o *CreateOverrideruleAdvancedRequestRequest) SetTags(v []float32)`

SetTags sets Tags field to given value.

### HasTags

`func (o *CreateOverrideruleAdvancedRequestRequest) HasTags() bool`

HasTags returns a boolean if a field has been set.

### SetTagsNil

`func (o *CreateOverrideruleAdvancedRequestRequest) SetTagsNil(b bool)`

 SetTagsNil sets the value for Tags to be an explicit nil

### UnsetTags
`func (o *CreateOverrideruleAdvancedRequestRequest) UnsetTags()`

UnsetTags ensures that no value is present for Tags, not even an explicit nil
### GetServiceId

`func (o *CreateOverrideruleAdvancedRequestRequest) GetServiceId() float32`

GetServiceId returns the ServiceId field if non-nil, zero value otherwise.

### GetServiceIdOk

`func (o *CreateOverrideruleAdvancedRequestRequest) GetServiceIdOk() (*float32, bool)`

GetServiceIdOk returns a tuple with the ServiceId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetServiceId

`func (o *CreateOverrideruleAdvancedRequestRequest) SetServiceId(v float32)`

SetServiceId sets ServiceId field to given value.

### HasServiceId

`func (o *CreateOverrideruleAdvancedRequestRequest) HasServiceId() bool`

HasServiceId returns a boolean if a field has been set.

### SetServiceIdNil

`func (o *CreateOverrideruleAdvancedRequestRequest) SetServiceIdNil(b bool)`

 SetServiceIdNil sets the value for ServiceId to be an explicit nil

### UnsetServiceId
`func (o *CreateOverrideruleAdvancedRequestRequest) UnsetServiceId()`

UnsetServiceId ensures that no value is present for ServiceId, not even an explicit nil

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



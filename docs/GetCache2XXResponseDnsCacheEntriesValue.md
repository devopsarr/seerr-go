# GetCache2XXResponseDnsCacheEntriesValue

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Addresses** | Pointer to [**GetCache2XXResponseDnsCacheEntriesValueAddresses**](GetCache2XXResponseDnsCacheEntriesValueAddresses.md) |  | [optional] 
**ActiveAddress** | Pointer to **string** |  | [optional] 
**Family** | Pointer to **float32** |  | [optional] 
**Age** | Pointer to **float32** |  | [optional] 
**Ttl** | Pointer to **float32** |  | [optional] 
**NetworkErrors** | Pointer to **float32** |  | [optional] 
**Hits** | Pointer to **float32** |  | [optional] 
**Misses** | Pointer to **float32** |  | [optional] 

## Methods

### NewGetCache2XXResponseDnsCacheEntriesValue

`func NewGetCache2XXResponseDnsCacheEntriesValue() *GetCache2XXResponseDnsCacheEntriesValue`

NewGetCache2XXResponseDnsCacheEntriesValue instantiates a new GetCache2XXResponseDnsCacheEntriesValue object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGetCache2XXResponseDnsCacheEntriesValueWithDefaults

`func NewGetCache2XXResponseDnsCacheEntriesValueWithDefaults() *GetCache2XXResponseDnsCacheEntriesValue`

NewGetCache2XXResponseDnsCacheEntriesValueWithDefaults instantiates a new GetCache2XXResponseDnsCacheEntriesValue object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAddresses

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetAddresses() GetCache2XXResponseDnsCacheEntriesValueAddresses`

GetAddresses returns the Addresses field if non-nil, zero value otherwise.

### GetAddressesOk

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetAddressesOk() (*GetCache2XXResponseDnsCacheEntriesValueAddresses, bool)`

GetAddressesOk returns a tuple with the Addresses field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAddresses

`func (o *GetCache2XXResponseDnsCacheEntriesValue) SetAddresses(v GetCache2XXResponseDnsCacheEntriesValueAddresses)`

SetAddresses sets Addresses field to given value.

### HasAddresses

`func (o *GetCache2XXResponseDnsCacheEntriesValue) HasAddresses() bool`

HasAddresses returns a boolean if a field has been set.

### GetActiveAddress

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetActiveAddress() string`

GetActiveAddress returns the ActiveAddress field if non-nil, zero value otherwise.

### GetActiveAddressOk

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetActiveAddressOk() (*string, bool)`

GetActiveAddressOk returns a tuple with the ActiveAddress field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetActiveAddress

`func (o *GetCache2XXResponseDnsCacheEntriesValue) SetActiveAddress(v string)`

SetActiveAddress sets ActiveAddress field to given value.

### HasActiveAddress

`func (o *GetCache2XXResponseDnsCacheEntriesValue) HasActiveAddress() bool`

HasActiveAddress returns a boolean if a field has been set.

### GetFamily

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetFamily() float32`

GetFamily returns the Family field if non-nil, zero value otherwise.

### GetFamilyOk

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetFamilyOk() (*float32, bool)`

GetFamilyOk returns a tuple with the Family field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFamily

`func (o *GetCache2XXResponseDnsCacheEntriesValue) SetFamily(v float32)`

SetFamily sets Family field to given value.

### HasFamily

`func (o *GetCache2XXResponseDnsCacheEntriesValue) HasFamily() bool`

HasFamily returns a boolean if a field has been set.

### GetAge

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetAge() float32`

GetAge returns the Age field if non-nil, zero value otherwise.

### GetAgeOk

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetAgeOk() (*float32, bool)`

GetAgeOk returns a tuple with the Age field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAge

`func (o *GetCache2XXResponseDnsCacheEntriesValue) SetAge(v float32)`

SetAge sets Age field to given value.

### HasAge

`func (o *GetCache2XXResponseDnsCacheEntriesValue) HasAge() bool`

HasAge returns a boolean if a field has been set.

### GetTtl

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetTtl() float32`

GetTtl returns the Ttl field if non-nil, zero value otherwise.

### GetTtlOk

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetTtlOk() (*float32, bool)`

GetTtlOk returns a tuple with the Ttl field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTtl

`func (o *GetCache2XXResponseDnsCacheEntriesValue) SetTtl(v float32)`

SetTtl sets Ttl field to given value.

### HasTtl

`func (o *GetCache2XXResponseDnsCacheEntriesValue) HasTtl() bool`

HasTtl returns a boolean if a field has been set.

### GetNetworkErrors

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetNetworkErrors() float32`

GetNetworkErrors returns the NetworkErrors field if non-nil, zero value otherwise.

### GetNetworkErrorsOk

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetNetworkErrorsOk() (*float32, bool)`

GetNetworkErrorsOk returns a tuple with the NetworkErrors field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNetworkErrors

`func (o *GetCache2XXResponseDnsCacheEntriesValue) SetNetworkErrors(v float32)`

SetNetworkErrors sets NetworkErrors field to given value.

### HasNetworkErrors

`func (o *GetCache2XXResponseDnsCacheEntriesValue) HasNetworkErrors() bool`

HasNetworkErrors returns a boolean if a field has been set.

### GetHits

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetHits() float32`

GetHits returns the Hits field if non-nil, zero value otherwise.

### GetHitsOk

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetHitsOk() (*float32, bool)`

GetHitsOk returns a tuple with the Hits field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHits

`func (o *GetCache2XXResponseDnsCacheEntriesValue) SetHits(v float32)`

SetHits sets Hits field to given value.

### HasHits

`func (o *GetCache2XXResponseDnsCacheEntriesValue) HasHits() bool`

HasHits returns a boolean if a field has been set.

### GetMisses

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetMisses() float32`

GetMisses returns the Misses field if non-nil, zero value otherwise.

### GetMissesOk

`func (o *GetCache2XXResponseDnsCacheEntriesValue) GetMissesOk() (*float32, bool)`

GetMissesOk returns a tuple with the Misses field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMisses

`func (o *GetCache2XXResponseDnsCacheEntriesValue) SetMisses(v float32)`

SetMisses sets Misses field to given value.

### HasMisses

`func (o *GetCache2XXResponseDnsCacheEntriesValue) HasMisses() bool`

HasMisses returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



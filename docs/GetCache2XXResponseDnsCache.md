# GetCache2XXResponseDnsCache

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Stats** | Pointer to [**GetCache2XXResponseDnsCacheStats**](GetCache2XXResponseDnsCacheStats.md) |  | [optional] 
**Entries** | Pointer to [**map[string]GetCache2XXResponseDnsCacheEntriesValue**](GetCache2XXResponseDnsCacheEntriesValue.md) |  | [optional] 

## Methods

### NewGetCache2XXResponseDnsCache

`func NewGetCache2XXResponseDnsCache() *GetCache2XXResponseDnsCache`

NewGetCache2XXResponseDnsCache instantiates a new GetCache2XXResponseDnsCache object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGetCache2XXResponseDnsCacheWithDefaults

`func NewGetCache2XXResponseDnsCacheWithDefaults() *GetCache2XXResponseDnsCache`

NewGetCache2XXResponseDnsCacheWithDefaults instantiates a new GetCache2XXResponseDnsCache object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetStats

`func (o *GetCache2XXResponseDnsCache) GetStats() GetCache2XXResponseDnsCacheStats`

GetStats returns the Stats field if non-nil, zero value otherwise.

### GetStatsOk

`func (o *GetCache2XXResponseDnsCache) GetStatsOk() (*GetCache2XXResponseDnsCacheStats, bool)`

GetStatsOk returns a tuple with the Stats field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStats

`func (o *GetCache2XXResponseDnsCache) SetStats(v GetCache2XXResponseDnsCacheStats)`

SetStats sets Stats field to given value.

### HasStats

`func (o *GetCache2XXResponseDnsCache) HasStats() bool`

HasStats returns a boolean if a field has been set.

### GetEntries

`func (o *GetCache2XXResponseDnsCache) GetEntries() map[string]GetCache2XXResponseDnsCacheEntriesValue`

GetEntries returns the Entries field if non-nil, zero value otherwise.

### GetEntriesOk

`func (o *GetCache2XXResponseDnsCache) GetEntriesOk() (*map[string]GetCache2XXResponseDnsCacheEntriesValue, bool)`

GetEntriesOk returns a tuple with the Entries field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEntries

`func (o *GetCache2XXResponseDnsCache) SetEntries(v map[string]GetCache2XXResponseDnsCacheEntriesValue)`

SetEntries sets Entries field to given value.

### HasEntries

`func (o *GetCache2XXResponseDnsCache) HasEntries() bool`

HasEntries returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



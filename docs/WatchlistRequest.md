# WatchlistRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TmdbId** | **float32** |  | 
**MediaType** | **string** |  | 
**RatingKey** | Pointer to **string** |  | [optional] 
**Title** | Pointer to **string** |  | [optional] 

## Methods

### NewWatchlistRequest

`func NewWatchlistRequest(tmdbId float32, mediaType string, ) *WatchlistRequest`

NewWatchlistRequest instantiates a new WatchlistRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewWatchlistRequestWithDefaults

`func NewWatchlistRequestWithDefaults() *WatchlistRequest`

NewWatchlistRequestWithDefaults instantiates a new WatchlistRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetTmdbId

`func (o *WatchlistRequest) GetTmdbId() float32`

GetTmdbId returns the TmdbId field if non-nil, zero value otherwise.

### GetTmdbIdOk

`func (o *WatchlistRequest) GetTmdbIdOk() (*float32, bool)`

GetTmdbIdOk returns a tuple with the TmdbId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTmdbId

`func (o *WatchlistRequest) SetTmdbId(v float32)`

SetTmdbId sets TmdbId field to given value.


### GetMediaType

`func (o *WatchlistRequest) GetMediaType() string`

GetMediaType returns the MediaType field if non-nil, zero value otherwise.

### GetMediaTypeOk

`func (o *WatchlistRequest) GetMediaTypeOk() (*string, bool)`

GetMediaTypeOk returns a tuple with the MediaType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMediaType

`func (o *WatchlistRequest) SetMediaType(v string)`

SetMediaType sets MediaType field to given value.


### GetRatingKey

`func (o *WatchlistRequest) GetRatingKey() string`

GetRatingKey returns the RatingKey field if non-nil, zero value otherwise.

### GetRatingKeyOk

`func (o *WatchlistRequest) GetRatingKeyOk() (*string, bool)`

GetRatingKeyOk returns a tuple with the RatingKey field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRatingKey

`func (o *WatchlistRequest) SetRatingKey(v string)`

SetRatingKey sets RatingKey field to given value.

### HasRatingKey

`func (o *WatchlistRequest) HasRatingKey() bool`

HasRatingKey returns a boolean if a field has been set.

### GetTitle

`func (o *WatchlistRequest) GetTitle() string`

GetTitle returns the Title field if non-nil, zero value otherwise.

### GetTitleOk

`func (o *WatchlistRequest) GetTitleOk() (*string, bool)`

GetTitleOk returns a tuple with the Title field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTitle

`func (o *WatchlistRequest) SetTitle(v string)`

SetTitle sets Title field to given value.

### HasTitle

`func (o *WatchlistRequest) HasTitle() bool`

HasTitle returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



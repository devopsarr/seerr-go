# GetJellyfinSync2XXResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Running** | Pointer to **bool** |  | [optional] 
**Progress** | Pointer to **float32** |  | [optional] 
**Total** | Pointer to **float32** |  | [optional] 
**CurrentLibrary** | Pointer to [**JellyfinLibrary**](JellyfinLibrary.md) |  | [optional] 
**Libraries** | Pointer to [**[]JellyfinLibrary**](JellyfinLibrary.md) |  | [optional] 

## Methods

### NewGetJellyfinSync2XXResponse

`func NewGetJellyfinSync2XXResponse() *GetJellyfinSync2XXResponse`

NewGetJellyfinSync2XXResponse instantiates a new GetJellyfinSync2XXResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGetJellyfinSync2XXResponseWithDefaults

`func NewGetJellyfinSync2XXResponseWithDefaults() *GetJellyfinSync2XXResponse`

NewGetJellyfinSync2XXResponseWithDefaults instantiates a new GetJellyfinSync2XXResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetRunning

`func (o *GetJellyfinSync2XXResponse) GetRunning() bool`

GetRunning returns the Running field if non-nil, zero value otherwise.

### GetRunningOk

`func (o *GetJellyfinSync2XXResponse) GetRunningOk() (*bool, bool)`

GetRunningOk returns a tuple with the Running field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRunning

`func (o *GetJellyfinSync2XXResponse) SetRunning(v bool)`

SetRunning sets Running field to given value.

### HasRunning

`func (o *GetJellyfinSync2XXResponse) HasRunning() bool`

HasRunning returns a boolean if a field has been set.

### GetProgress

`func (o *GetJellyfinSync2XXResponse) GetProgress() float32`

GetProgress returns the Progress field if non-nil, zero value otherwise.

### GetProgressOk

`func (o *GetJellyfinSync2XXResponse) GetProgressOk() (*float32, bool)`

GetProgressOk returns a tuple with the Progress field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProgress

`func (o *GetJellyfinSync2XXResponse) SetProgress(v float32)`

SetProgress sets Progress field to given value.

### HasProgress

`func (o *GetJellyfinSync2XXResponse) HasProgress() bool`

HasProgress returns a boolean if a field has been set.

### GetTotal

`func (o *GetJellyfinSync2XXResponse) GetTotal() float32`

GetTotal returns the Total field if non-nil, zero value otherwise.

### GetTotalOk

`func (o *GetJellyfinSync2XXResponse) GetTotalOk() (*float32, bool)`

GetTotalOk returns a tuple with the Total field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTotal

`func (o *GetJellyfinSync2XXResponse) SetTotal(v float32)`

SetTotal sets Total field to given value.

### HasTotal

`func (o *GetJellyfinSync2XXResponse) HasTotal() bool`

HasTotal returns a boolean if a field has been set.

### GetCurrentLibrary

`func (o *GetJellyfinSync2XXResponse) GetCurrentLibrary() JellyfinLibrary`

GetCurrentLibrary returns the CurrentLibrary field if non-nil, zero value otherwise.

### GetCurrentLibraryOk

`func (o *GetJellyfinSync2XXResponse) GetCurrentLibraryOk() (*JellyfinLibrary, bool)`

GetCurrentLibraryOk returns a tuple with the CurrentLibrary field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCurrentLibrary

`func (o *GetJellyfinSync2XXResponse) SetCurrentLibrary(v JellyfinLibrary)`

SetCurrentLibrary sets CurrentLibrary field to given value.

### HasCurrentLibrary

`func (o *GetJellyfinSync2XXResponse) HasCurrentLibrary() bool`

HasCurrentLibrary returns a boolean if a field has been set.

### GetLibraries

`func (o *GetJellyfinSync2XXResponse) GetLibraries() []JellyfinLibrary`

GetLibraries returns the Libraries field if non-nil, zero value otherwise.

### GetLibrariesOk

`func (o *GetJellyfinSync2XXResponse) GetLibrariesOk() (*[]JellyfinLibrary, bool)`

GetLibrariesOk returns a tuple with the Libraries field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLibraries

`func (o *GetJellyfinSync2XXResponse) SetLibraries(v []JellyfinLibrary)`

SetLibraries sets Libraries field to given value.

### HasLibraries

`func (o *GetJellyfinSync2XXResponse) HasLibraries() bool`

HasLibraries returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



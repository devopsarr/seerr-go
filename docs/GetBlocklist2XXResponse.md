# GetBlocklist2XXResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PageInfo** | Pointer to [**PageInfo**](PageInfo.md) |  | [optional] 
**Results** | Pointer to [**[]GetBlocklist2XXResponseResultsInner**](GetBlocklist2XXResponseResultsInner.md) |  | [optional] 

## Methods

### NewGetBlocklist2XXResponse

`func NewGetBlocklist2XXResponse() *GetBlocklist2XXResponse`

NewGetBlocklist2XXResponse instantiates a new GetBlocklist2XXResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGetBlocklist2XXResponseWithDefaults

`func NewGetBlocklist2XXResponseWithDefaults() *GetBlocklist2XXResponse`

NewGetBlocklist2XXResponseWithDefaults instantiates a new GetBlocklist2XXResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPageInfo

`func (o *GetBlocklist2XXResponse) GetPageInfo() PageInfo`

GetPageInfo returns the PageInfo field if non-nil, zero value otherwise.

### GetPageInfoOk

`func (o *GetBlocklist2XXResponse) GetPageInfoOk() (*PageInfo, bool)`

GetPageInfoOk returns a tuple with the PageInfo field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPageInfo

`func (o *GetBlocklist2XXResponse) SetPageInfo(v PageInfo)`

SetPageInfo sets PageInfo field to given value.

### HasPageInfo

`func (o *GetBlocklist2XXResponse) HasPageInfo() bool`

HasPageInfo returns a boolean if a field has been set.

### GetResults

`func (o *GetBlocklist2XXResponse) GetResults() []GetBlocklist2XXResponseResultsInner`

GetResults returns the Results field if non-nil, zero value otherwise.

### GetResultsOk

`func (o *GetBlocklist2XXResponse) GetResultsOk() (*[]GetBlocklist2XXResponseResultsInner, bool)`

GetResultsOk returns a tuple with the Results field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResults

`func (o *GetBlocklist2XXResponse) SetResults(v []GetBlocklist2XXResponseResultsInner)`

SetResults sets Results field to given value.

### HasResults

`func (o *GetBlocklist2XXResponse) HasResults() bool`

HasResults returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



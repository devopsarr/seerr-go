# \SearchAPI

All URIs are relative to *http://localhost:5055/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetDiscoverKeywordMovies**](SearchAPI.md#GetDiscoverKeywordMovies) | **Get** /discover/keyword/{keywordId}/movies | Get movies from keyword
[**GetDiscoverMovies**](SearchAPI.md#GetDiscoverMovies) | **Get** /discover/movies | Discover movies
[**GetDiscoverMoviesGenreByGenreId**](SearchAPI.md#GetDiscoverMoviesGenreByGenreId) | **Get** /discover/movies/genre/{genreId} | Discover movies by genre
[**GetDiscoverMoviesLanguageByLanguage**](SearchAPI.md#GetDiscoverMoviesLanguageByLanguage) | **Get** /discover/movies/language/{language} | Discover movies by original language
[**GetDiscoverMoviesStudioByStudioId**](SearchAPI.md#GetDiscoverMoviesStudioByStudioId) | **Get** /discover/movies/studio/{studioId} | Discover movies by studio
[**GetDiscoverMoviesUpcoming**](SearchAPI.md#GetDiscoverMoviesUpcoming) | **Get** /discover/movies/upcoming | Upcoming movies
[**GetDiscoverTrending**](SearchAPI.md#GetDiscoverTrending) | **Get** /discover/trending | Trending movies and TV
[**GetDiscoverTv**](SearchAPI.md#GetDiscoverTv) | **Get** /discover/tv | Discover TV shows
[**GetDiscoverTvGenreByGenreId**](SearchAPI.md#GetDiscoverTvGenreByGenreId) | **Get** /discover/tv/genre/{genreId} | Discover TV shows by genre
[**GetDiscoverTvLanguageByLanguage**](SearchAPI.md#GetDiscoverTvLanguageByLanguage) | **Get** /discover/tv/language/{language} | Discover TV shows by original language
[**GetDiscoverTvNetworkByNetworkId**](SearchAPI.md#GetDiscoverTvNetworkByNetworkId) | **Get** /discover/tv/network/{networkId} | Discover TV shows by network
[**GetDiscoverTvUpcoming**](SearchAPI.md#GetDiscoverTvUpcoming) | **Get** /discover/tv/upcoming | Discover Upcoming TV shows
[**GetDiscoverWatchlist**](SearchAPI.md#GetDiscoverWatchlist) | **Get** /discover/watchlist | Get the Plex watchlist.
[**GetSearch**](SearchAPI.md#GetSearch) | **Get** /search | Search for movies, TV shows, or people
[**GetSearchCompany**](SearchAPI.md#GetSearchCompany) | **Get** /search/company | Search for companies
[**GetSearchKeyword**](SearchAPI.md#GetSearchKeyword) | **Get** /search/keyword | Search for keywords
[**ListDiscoverGenresliderMovie**](SearchAPI.md#ListDiscoverGenresliderMovie) | **Get** /discover/genreslider/movie | Get genre slider data for movies
[**ListDiscoverGenresliderTv**](SearchAPI.md#ListDiscoverGenresliderTv) | **Get** /discover/genreslider/tv | Get genre slider data for TV series



## GetDiscoverKeywordMovies

> GetDiscoverMovies2XXResponse GetDiscoverKeywordMovies(ctx, keywordId).Page(page).Language(language).Execute()

Get movies from keyword



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
	keywordId := float32(207317) // float32 | 
	page := float32(1) // float32 |  (optional) (default to 1)
	language := "en" // string |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetDiscoverKeywordMovies(context.Background(), keywordId).Page(page).Language(language).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetDiscoverKeywordMovies``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDiscoverKeywordMovies`: GetDiscoverMovies2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetDiscoverKeywordMovies`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**keywordId** | **float32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetDiscoverKeywordMoviesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **page** | **float32** |  | [default to 1]
 **language** | **string** |  | 

### Return type

[**GetDiscoverMovies2XXResponse**](GetDiscoverMovies2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetDiscoverMovies

> GetDiscoverMovies2XXResponse GetDiscoverMovies(ctx).Page(page).Language(language).Genre(genre).Studio(studio).Keywords(keywords).ExcludeKeywords(excludeKeywords).SortBy(sortBy).PrimaryReleaseDateGte(primaryReleaseDateGte).PrimaryReleaseDateLte(primaryReleaseDateLte).WithRuntimeGte(withRuntimeGte).WithRuntimeLte(withRuntimeLte).VoteAverageGte(voteAverageGte).VoteAverageLte(voteAverageLte).VoteCountGte(voteCountGte).VoteCountLte(voteCountLte).WatchRegion(watchRegion).WatchProviders(watchProviders).Certification(certification).CertificationGte(certificationGte).CertificationLte(certificationLte).CertificationCountry(certificationCountry).CertificationMode(certificationMode).Execute()

Discover movies



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
	page := float32(1) // float32 |  (optional) (default to 1)
	language := "en" // string |  (optional)
	genre := "18" // string |  (optional)
	studio := float32(1) // float32 |  (optional)
	keywords := "1,2" // string |  (optional)
	excludeKeywords := "3,4" // string | Comma-separated list of keyword IDs to exclude from results (optional)
	sortBy := "popularity.desc" // string |  (optional)
	primaryReleaseDateGte := "2022-01-01T00:00:00Z" // string |  (optional)
	primaryReleaseDateLte := "2023-01-01T00:00:00Z" // string |  (optional)
	withRuntimeGte := float32(60) // float32 |  (optional)
	withRuntimeLte := float32(120) // float32 |  (optional)
	voteAverageGte := float32(7) // float32 |  (optional)
	voteAverageLte := float32(10) // float32 |  (optional)
	voteCountGte := float32(7) // float32 |  (optional)
	voteCountLte := float32(10) // float32 |  (optional)
	watchRegion := "US" // string |  (optional)
	watchProviders := "8|9" // string |  (optional)
	certification := "PG-13" // string | Exact certification to filter by (used when certificationMode is 'exact') (optional)
	certificationGte := "G" // string | Minimum certification to filter by (used when certificationMode is 'range') (optional)
	certificationLte := "PG-13" // string | Maximum certification to filter by (used when certificationMode is 'range') (optional)
	certificationCountry := "US" // string | Country code for the certification system (e.g., US, GB, CA) (optional)
	certificationMode := "exact" // string | Determines whether to use exact certification matching or a certification range (internal use only, not sent to TMDB API) (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetDiscoverMovies(context.Background()).Page(page).Language(language).Genre(genre).Studio(studio).Keywords(keywords).ExcludeKeywords(excludeKeywords).SortBy(sortBy).PrimaryReleaseDateGte(primaryReleaseDateGte).PrimaryReleaseDateLte(primaryReleaseDateLte).WithRuntimeGte(withRuntimeGte).WithRuntimeLte(withRuntimeLte).VoteAverageGte(voteAverageGte).VoteAverageLte(voteAverageLte).VoteCountGte(voteCountGte).VoteCountLte(voteCountLte).WatchRegion(watchRegion).WatchProviders(watchProviders).Certification(certification).CertificationGte(certificationGte).CertificationLte(certificationLte).CertificationCountry(certificationCountry).CertificationMode(certificationMode).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetDiscoverMovies``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDiscoverMovies`: GetDiscoverMovies2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetDiscoverMovies`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetDiscoverMoviesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float32** |  | [default to 1]
 **language** | **string** |  | 
 **genre** | **string** |  | 
 **studio** | **float32** |  | 
 **keywords** | **string** |  | 
 **excludeKeywords** | **string** | Comma-separated list of keyword IDs to exclude from results | 
 **sortBy** | **string** |  | 
 **primaryReleaseDateGte** | **string** |  | 
 **primaryReleaseDateLte** | **string** |  | 
 **withRuntimeGte** | **float32** |  | 
 **withRuntimeLte** | **float32** |  | 
 **voteAverageGte** | **float32** |  | 
 **voteAverageLte** | **float32** |  | 
 **voteCountGte** | **float32** |  | 
 **voteCountLte** | **float32** |  | 
 **watchRegion** | **string** |  | 
 **watchProviders** | **string** |  | 
 **certification** | **string** | Exact certification to filter by (used when certificationMode is &#39;exact&#39;) | 
 **certificationGte** | **string** | Minimum certification to filter by (used when certificationMode is &#39;range&#39;) | 
 **certificationLte** | **string** | Maximum certification to filter by (used when certificationMode is &#39;range&#39;) | 
 **certificationCountry** | **string** | Country code for the certification system (e.g., US, GB, CA) | 
 **certificationMode** | **string** | Determines whether to use exact certification matching or a certification range (internal use only, not sent to TMDB API) | 

### Return type

[**GetDiscoverMovies2XXResponse**](GetDiscoverMovies2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetDiscoverMoviesGenreByGenreId

> GetDiscoverMoviesGenreByGenreId2XXResponse GetDiscoverMoviesGenreByGenreId(ctx, genreId).Page(page).Language(language).Execute()

Discover movies by genre



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
	genreId := "1" // string | 
	page := float32(1) // float32 |  (optional) (default to 1)
	language := "en" // string |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetDiscoverMoviesGenreByGenreId(context.Background(), genreId).Page(page).Language(language).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetDiscoverMoviesGenreByGenreId``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDiscoverMoviesGenreByGenreId`: GetDiscoverMoviesGenreByGenreId2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetDiscoverMoviesGenreByGenreId`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**genreId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetDiscoverMoviesGenreByGenreIdRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **page** | **float32** |  | [default to 1]
 **language** | **string** |  | 

### Return type

[**GetDiscoverMoviesGenreByGenreId2XXResponse**](GetDiscoverMoviesGenreByGenreId2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetDiscoverMoviesLanguageByLanguage

> GetDiscoverMoviesLanguageByLanguage2XXResponse GetDiscoverMoviesLanguageByLanguage(ctx, language).Page(page).Language2(language2).Execute()

Discover movies by original language



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
	language := "en" // string | 
	page := float32(1) // float32 |  (optional) (default to 1)
	language2 := "en" // string |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetDiscoverMoviesLanguageByLanguage(context.Background(), language).Page(page).Language2(language2).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetDiscoverMoviesLanguageByLanguage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDiscoverMoviesLanguageByLanguage`: GetDiscoverMoviesLanguageByLanguage2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetDiscoverMoviesLanguageByLanguage`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**language** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetDiscoverMoviesLanguageByLanguageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **page** | **float32** |  | [default to 1]
 **language2** | **string** |  | 

### Return type

[**GetDiscoverMoviesLanguageByLanguage2XXResponse**](GetDiscoverMoviesLanguageByLanguage2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetDiscoverMoviesStudioByStudioId

> GetDiscoverMoviesStudioByStudioId2XXResponse GetDiscoverMoviesStudioByStudioId(ctx, studioId).Page(page).Language(language).Execute()

Discover movies by studio



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
	studioId := "1" // string | 
	page := float32(1) // float32 |  (optional) (default to 1)
	language := "en" // string |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetDiscoverMoviesStudioByStudioId(context.Background(), studioId).Page(page).Language(language).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetDiscoverMoviesStudioByStudioId``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDiscoverMoviesStudioByStudioId`: GetDiscoverMoviesStudioByStudioId2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetDiscoverMoviesStudioByStudioId`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**studioId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetDiscoverMoviesStudioByStudioIdRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **page** | **float32** |  | [default to 1]
 **language** | **string** |  | 

### Return type

[**GetDiscoverMoviesStudioByStudioId2XXResponse**](GetDiscoverMoviesStudioByStudioId2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetDiscoverMoviesUpcoming

> GetDiscoverMovies2XXResponse GetDiscoverMoviesUpcoming(ctx).Page(page).Language(language).Execute()

Upcoming movies



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
	page := float32(1) // float32 |  (optional) (default to 1)
	language := "en" // string |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetDiscoverMoviesUpcoming(context.Background()).Page(page).Language(language).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetDiscoverMoviesUpcoming``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDiscoverMoviesUpcoming`: GetDiscoverMovies2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetDiscoverMoviesUpcoming`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetDiscoverMoviesUpcomingRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float32** |  | [default to 1]
 **language** | **string** |  | 

### Return type

[**GetDiscoverMovies2XXResponse**](GetDiscoverMovies2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetDiscoverTrending

> GetSearch2XXResponse GetDiscoverTrending(ctx).Page(page).Language(language).MediaType(mediaType).TimeWindow(timeWindow).Execute()

Trending movies and TV



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
	page := float32(1) // float32 |  (optional) (default to 1)
	language := "en" // string |  (optional)
	mediaType := "mediaType_example" // string |  (optional) (default to "all")
	timeWindow := "timeWindow_example" // string |  (optional) (default to "day")

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetDiscoverTrending(context.Background()).Page(page).Language(language).MediaType(mediaType).TimeWindow(timeWindow).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetDiscoverTrending``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDiscoverTrending`: GetSearch2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetDiscoverTrending`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetDiscoverTrendingRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float32** |  | [default to 1]
 **language** | **string** |  | 
 **mediaType** | **string** |  | [default to &quot;all&quot;]
 **timeWindow** | **string** |  | [default to &quot;day&quot;]

### Return type

[**GetSearch2XXResponse**](GetSearch2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetDiscoverTv

> GetDiscoverTv2XXResponse GetDiscoverTv(ctx).Page(page).Language(language).Genre(genre).Network(network).Keywords(keywords).ExcludeKeywords(excludeKeywords).SortBy(sortBy).FirstAirDateGte(firstAirDateGte).FirstAirDateLte(firstAirDateLte).WithRuntimeGte(withRuntimeGte).WithRuntimeLte(withRuntimeLte).VoteAverageGte(voteAverageGte).VoteAverageLte(voteAverageLte).VoteCountGte(voteCountGte).VoteCountLte(voteCountLte).WatchRegion(watchRegion).WatchProviders(watchProviders).Status(status).Certification(certification).CertificationGte(certificationGte).CertificationLte(certificationLte).CertificationCountry(certificationCountry).CertificationMode(certificationMode).Execute()

Discover TV shows



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
	page := float32(1) // float32 |  (optional) (default to 1)
	language := "en" // string |  (optional)
	genre := "18" // string |  (optional)
	network := float32(1) // float32 |  (optional)
	keywords := "1,2" // string |  (optional)
	excludeKeywords := "3,4" // string | Comma-separated list of keyword IDs to exclude from results (optional)
	sortBy := "popularity.desc" // string |  (optional)
	firstAirDateGte := "2022-01-01T00:00:00Z" // string |  (optional)
	firstAirDateLte := "2023-01-01T00:00:00Z" // string |  (optional)
	withRuntimeGte := float32(60) // float32 |  (optional)
	withRuntimeLte := float32(120) // float32 |  (optional)
	voteAverageGte := float32(7) // float32 |  (optional)
	voteAverageLte := float32(10) // float32 |  (optional)
	voteCountGte := float32(7) // float32 |  (optional)
	voteCountLte := float32(10) // float32 |  (optional)
	watchRegion := "US" // string |  (optional)
	watchProviders := "8|9" // string |  (optional)
	status := "3|4" // string |  (optional)
	certification := "TV-14" // string | Exact certification to filter by (used when certificationMode is 'exact') (optional)
	certificationGte := "TV-PG" // string | Minimum certification to filter by (used when certificationMode is 'range') (optional)
	certificationLte := "TV-MA" // string | Maximum certification to filter by (used when certificationMode is 'range') (optional)
	certificationCountry := "US" // string | Country code for the certification system (e.g., US, GB, CA) (optional)
	certificationMode := "exact" // string | Determines whether to use exact certification matching or a certification range (internal use only, not sent to TMDB API) (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetDiscoverTv(context.Background()).Page(page).Language(language).Genre(genre).Network(network).Keywords(keywords).ExcludeKeywords(excludeKeywords).SortBy(sortBy).FirstAirDateGte(firstAirDateGte).FirstAirDateLte(firstAirDateLte).WithRuntimeGte(withRuntimeGte).WithRuntimeLte(withRuntimeLte).VoteAverageGte(voteAverageGte).VoteAverageLte(voteAverageLte).VoteCountGte(voteCountGte).VoteCountLte(voteCountLte).WatchRegion(watchRegion).WatchProviders(watchProviders).Status(status).Certification(certification).CertificationGte(certificationGte).CertificationLte(certificationLte).CertificationCountry(certificationCountry).CertificationMode(certificationMode).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetDiscoverTv``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDiscoverTv`: GetDiscoverTv2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetDiscoverTv`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetDiscoverTvRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float32** |  | [default to 1]
 **language** | **string** |  | 
 **genre** | **string** |  | 
 **network** | **float32** |  | 
 **keywords** | **string** |  | 
 **excludeKeywords** | **string** | Comma-separated list of keyword IDs to exclude from results | 
 **sortBy** | **string** |  | 
 **firstAirDateGte** | **string** |  | 
 **firstAirDateLte** | **string** |  | 
 **withRuntimeGte** | **float32** |  | 
 **withRuntimeLte** | **float32** |  | 
 **voteAverageGte** | **float32** |  | 
 **voteAverageLte** | **float32** |  | 
 **voteCountGte** | **float32** |  | 
 **voteCountLte** | **float32** |  | 
 **watchRegion** | **string** |  | 
 **watchProviders** | **string** |  | 
 **status** | **string** |  | 
 **certification** | **string** | Exact certification to filter by (used when certificationMode is &#39;exact&#39;) | 
 **certificationGte** | **string** | Minimum certification to filter by (used when certificationMode is &#39;range&#39;) | 
 **certificationLte** | **string** | Maximum certification to filter by (used when certificationMode is &#39;range&#39;) | 
 **certificationCountry** | **string** | Country code for the certification system (e.g., US, GB, CA) | 
 **certificationMode** | **string** | Determines whether to use exact certification matching or a certification range (internal use only, not sent to TMDB API) | 

### Return type

[**GetDiscoverTv2XXResponse**](GetDiscoverTv2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetDiscoverTvGenreByGenreId

> GetDiscoverTvGenreByGenreId2XXResponse GetDiscoverTvGenreByGenreId(ctx, genreId).Page(page).Language(language).Execute()

Discover TV shows by genre



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
	genreId := "1" // string | 
	page := float32(1) // float32 |  (optional) (default to 1)
	language := "en" // string |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetDiscoverTvGenreByGenreId(context.Background(), genreId).Page(page).Language(language).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetDiscoverTvGenreByGenreId``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDiscoverTvGenreByGenreId`: GetDiscoverTvGenreByGenreId2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetDiscoverTvGenreByGenreId`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**genreId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetDiscoverTvGenreByGenreIdRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **page** | **float32** |  | [default to 1]
 **language** | **string** |  | 

### Return type

[**GetDiscoverTvGenreByGenreId2XXResponse**](GetDiscoverTvGenreByGenreId2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetDiscoverTvLanguageByLanguage

> GetDiscoverTvLanguageByLanguage2XXResponse GetDiscoverTvLanguageByLanguage(ctx, language).Page(page).Language2(language2).Execute()

Discover TV shows by original language



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
	language := "en" // string | 
	page := float32(1) // float32 |  (optional) (default to 1)
	language2 := "en" // string |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetDiscoverTvLanguageByLanguage(context.Background(), language).Page(page).Language2(language2).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetDiscoverTvLanguageByLanguage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDiscoverTvLanguageByLanguage`: GetDiscoverTvLanguageByLanguage2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetDiscoverTvLanguageByLanguage`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**language** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetDiscoverTvLanguageByLanguageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **page** | **float32** |  | [default to 1]
 **language2** | **string** |  | 

### Return type

[**GetDiscoverTvLanguageByLanguage2XXResponse**](GetDiscoverTvLanguageByLanguage2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetDiscoverTvNetworkByNetworkId

> GetDiscoverTvNetworkByNetworkId2XXResponse GetDiscoverTvNetworkByNetworkId(ctx, networkId).Page(page).Language(language).Execute()

Discover TV shows by network



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
	networkId := "1" // string | 
	page := float32(1) // float32 |  (optional) (default to 1)
	language := "en" // string |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetDiscoverTvNetworkByNetworkId(context.Background(), networkId).Page(page).Language(language).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetDiscoverTvNetworkByNetworkId``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDiscoverTvNetworkByNetworkId`: GetDiscoverTvNetworkByNetworkId2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetDiscoverTvNetworkByNetworkId`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**networkId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetDiscoverTvNetworkByNetworkIdRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **page** | **float32** |  | [default to 1]
 **language** | **string** |  | 

### Return type

[**GetDiscoverTvNetworkByNetworkId2XXResponse**](GetDiscoverTvNetworkByNetworkId2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetDiscoverTvUpcoming

> GetDiscoverTv2XXResponse GetDiscoverTvUpcoming(ctx).Page(page).Language(language).Execute()

Discover Upcoming TV shows



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
	page := float32(1) // float32 |  (optional) (default to 1)
	language := "en" // string |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetDiscoverTvUpcoming(context.Background()).Page(page).Language(language).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetDiscoverTvUpcoming``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDiscoverTvUpcoming`: GetDiscoverTv2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetDiscoverTvUpcoming`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetDiscoverTvUpcomingRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float32** |  | [default to 1]
 **language** | **string** |  | 

### Return type

[**GetDiscoverTv2XXResponse**](GetDiscoverTv2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetDiscoverWatchlist

> GetUserWatchlist2XXResponse GetDiscoverWatchlist(ctx).Page(page).Execute()

Get the Plex watchlist.

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
	page := float32(1) // float32 |  (optional) (default to 1)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetDiscoverWatchlist(context.Background()).Page(page).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetDiscoverWatchlist``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDiscoverWatchlist`: GetUserWatchlist2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetDiscoverWatchlist`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetDiscoverWatchlistRequest struct via the builder pattern


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


## GetSearch

> GetSearch2XXResponse GetSearch(ctx).Query(query).Page(page).Language(language).Execute()

Search for movies, TV shows, or people



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
	query := "Mulan" // string | 
	page := float32(1) // float32 |  (optional) (default to 1)
	language := "en" // string |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetSearch(context.Background()).Query(query).Page(page).Language(language).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetSearch``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetSearch`: GetSearch2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetSearch`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetSearchRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **string** |  | 
 **page** | **float32** |  | [default to 1]
 **language** | **string** |  | 

### Return type

[**GetSearch2XXResponse**](GetSearch2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetSearchCompany

> GetSearchCompany2XXResponse GetSearchCompany(ctx).Query(query).Page(page).Execute()

Search for companies



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
	query := "Disney" // string | 
	page := float32(1) // float32 |  (optional) (default to 1)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetSearchCompany(context.Background()).Query(query).Page(page).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetSearchCompany``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetSearchCompany`: GetSearchCompany2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetSearchCompany`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetSearchCompanyRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **string** |  | 
 **page** | **float32** |  | [default to 1]

### Return type

[**GetSearchCompany2XXResponse**](GetSearchCompany2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetSearchKeyword

> GetSearchKeyword2XXResponse GetSearchKeyword(ctx).Query(query).Page(page).Execute()

Search for keywords



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
	query := "christmas" // string | 
	page := float32(1) // float32 |  (optional) (default to 1)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.GetSearchKeyword(context.Background()).Query(query).Page(page).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.GetSearchKeyword``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetSearchKeyword`: GetSearchKeyword2XXResponse
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.GetSearchKeyword`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetSearchKeywordRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **string** |  | 
 **page** | **float32** |  | [default to 1]

### Return type

[**GetSearchKeyword2XXResponse**](GetSearchKeyword2XXResponse.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListDiscoverGenresliderMovie

> []ListDiscoverGenresliderMovie2XXResponseInner ListDiscoverGenresliderMovie(ctx).Language(language).Execute()

Get genre slider data for movies



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
	language := "en" // string |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.ListDiscoverGenresliderMovie(context.Background()).Language(language).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.ListDiscoverGenresliderMovie``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListDiscoverGenresliderMovie`: []ListDiscoverGenresliderMovie2XXResponseInner
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.ListDiscoverGenresliderMovie`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListDiscoverGenresliderMovieRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **language** | **string** |  | 

### Return type

[**[]ListDiscoverGenresliderMovie2XXResponseInner**](ListDiscoverGenresliderMovie2XXResponseInner.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListDiscoverGenresliderTv

> []ListDiscoverGenresliderMovie2XXResponseInner ListDiscoverGenresliderTv(ctx).Language(language).Execute()

Get genre slider data for TV series



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
	language := "en" // string |  (optional)

	configuration := seerrClient.NewConfiguration()
	apiClient := seerrClient.NewAPIClient(configuration)
	resp, r, err := apiClient.SearchAPI.ListDiscoverGenresliderTv(context.Background()).Language(language).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SearchAPI.ListDiscoverGenresliderTv``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListDiscoverGenresliderTv`: []ListDiscoverGenresliderMovie2XXResponseInner
	fmt.Fprintf(os.Stdout, "Response from `SearchAPI.ListDiscoverGenresliderTv`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListDiscoverGenresliderTvRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **language** | **string** |  | 

### Return type

[**[]ListDiscoverGenresliderMovie2XXResponseInner**](ListDiscoverGenresliderMovie2XXResponseInner.md)

### Authorization

[apiKey](../README.md#apiKey), [cookieAuth](../README.md#cookieAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


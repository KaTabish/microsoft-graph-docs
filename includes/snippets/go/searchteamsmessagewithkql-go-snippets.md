---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/Search/Query"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewQueryPostRequestBody()


searchRequest := graphmodels.NewSearchRequest()
entityTypes := []graphmodels.EntityTypeable {
	entityType := graphmodels.CHATMESSAGE_ENTITYTYPE 
	searchRequest.SetEntityType(&entityType) 

}
searchRequest.SetEntityTypes(entityTypes)
query := graphmodels.NewSearchQuery()
queryString := "contoso from:bob to:alice sent>2022-07-14"
query.SetQueryString(&queryString) 
searchRequest.SetQuery(query)
from := int32(0)
searchRequest.SetFrom(&from) 
size := int32(15)
searchRequest.SetSize(&size) 
enableTopResults := true
searchRequest.SetEnableTopResults(&enableTopResults) 

requests := []graphmodels.SearchRequestable {
	searchRequest,

}
requestBody.SetRequests(requests)

result, err := graphClient.Search().Query().Post(context.Background(), requestBody, nil)


```
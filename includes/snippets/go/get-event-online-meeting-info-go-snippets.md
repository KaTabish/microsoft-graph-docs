---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphconfig "github.com/microsoftgraph/msgraph-sdk-go/users"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestParameters := &graphconfig.ItemEventItemRequestBuilderGetQueryParameters{
	Select: [] string {"isOnlineMeeting","onlineMeetingProvider","onlineMeeting"},
}
configuration := &graphconfig.ItemEventItemRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.Me().Events().ByEventId("event-id").Get(context.Background(), configuration)


```
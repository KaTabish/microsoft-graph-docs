---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphconfig "github.com/microsoftgraph/msgraph-beta-sdk-go/groups"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)



requestId := "https://graph.microsoft.com/beta/users/{id}"

requestParameters := &graphconfig.GroupItemRejectedSenders$refRequestBuilderDeleteQueryParameters{
	Id: &requestId,
}
configuration := &graphconfig.GroupItemRejectedSenders$refRequestBuilderDeleteRequestConfiguration{
	QueryParameters: requestParameters,
}

graphClient.Groups().ByGroupId("group-id").RejectedSenders().Ref().Delete(context.Background(), configuration)


```
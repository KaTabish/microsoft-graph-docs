---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewAuthenticationEventListener()
conditions := graphmodels.NewAuthenticationConditions()
applications := graphmodels.NewAuthenticationConditionsApplications()
includeAllApplications := false
applications.SetIncludeAllApplications(&includeAllApplications) 
conditions.SetApplications(applications)
requestBody.SetConditions(conditions)
priority := int32(500)
requestBody.SetPriority(&priority) 

result, err := graphClient.Identity().AuthenticationEventListeners().ByAuthenticationEventListenerId("authenticationEventListener-id").Patch(context.Background(), requestBody, nil)


```
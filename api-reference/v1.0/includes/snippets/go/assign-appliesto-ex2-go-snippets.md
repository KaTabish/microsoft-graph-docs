---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/ServicePrincipals/Item/AppManagementPolicies/Item"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewAppManagementPolicie()
additionalData := map[string]interface{}{
	"odataId" : "https://graph.microsoft.com/v1.0/policies/appManagementPolicies/{id}", 
}
requestBody.SetAdditionalData(additionalData)

graphClient.ServicePrincipals().ByServicePrincipalId("servicePrincipal-id").AppManagementPolicies().ByAppManagementPolicieId("appManagementPolicy-id").Post(context.Background(), requestBody, nil)


```
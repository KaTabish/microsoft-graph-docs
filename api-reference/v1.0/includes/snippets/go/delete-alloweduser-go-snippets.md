---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

printerShareId := "printerShare-id"
userId := "user-id"
graphClient.Print().SharesById(&printerShareId).AllowedUsersById(&userId).$ref().Delete()


```
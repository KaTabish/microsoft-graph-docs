---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

// Code snippets are only available for the latest version. Current version is 5.x

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new AdministrativeUnit
{
	AdditionalData = new Dictionary<string, object>
	{
		{
			"membershipType" , "Dynamic"
		},
		{
			"membershipRule" , "(user.country -eq \"United States\")"
		},
		{
			"membershipRuleProcessingState" , "On"
		},
	},
};
var result = await graphClient.AdministrativeUnits["{administrativeUnit-id}"].PatchAsync(requestBody);


```
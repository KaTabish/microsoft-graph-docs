---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

// Code snippets are only available for the latest version. Current version is 5.x

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new Attachment
{
	OdataType = "#microsoft.graph.fileAttachment",
	Name = "menu.txt",
	AdditionalData = new Dictionary<string, object>
	{
		{
			"contentBytes" , "base64bWFjIGFuZCBjaGVlc2UgdG9kYXk="
		},
	},
};
var result = await graphClient.Me.Events["{event-id}"].Attachments.PostAsync(requestBody);


```
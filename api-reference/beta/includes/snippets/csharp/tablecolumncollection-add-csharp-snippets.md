---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

// Code snippets are only available for the latest version. Current version is 5.x

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new Microsoft.Graph.Beta.Drives.Item.Items.Item.Workbook.Tables.Item.Columns.Add.AddPostRequestBody
{
	Index = new IndexObject
	{
	},
	Values = new List<>
	{
		new 
		{
		},
	},
};
var result = await graphClient.Drives["{drive-id}"].Items["{driveItem-id}"].Workbook.Tables["{workbookTable-id}"].Columns.Add.PostAsync(requestBody);


```
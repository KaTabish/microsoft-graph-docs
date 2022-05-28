---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var pinnedChatMessageInfo = new PinnedChatMessageInfo
{
	AdditionalData = new Dictionary<string, object>()
	{
		{"message@odata.bind", "https://graph.microsoft.com/beta/chats/19:2da4c29f6d7041eca70b638b43d45437@thread.v2/messages/1616964509832"}
	}
};

await graphClient.Chats["{chat-id}"].PinnedMessages
	.Request()
	.AddAsync(pinnedChatMessageInfo);

```
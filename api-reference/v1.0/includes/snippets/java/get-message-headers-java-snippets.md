---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Message message = graphClient.me().messages("AAMkADhAAAW-VPeAAA=")
	.buildRequest()
	.select("internetMessageHeaders")
	.get();

```
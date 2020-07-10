---
title: "Update directoryDefinition"
description: "Update the properties of a directoryDefinition object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update directoryDefinition
Namespace: microsoft.graph

Update the properties of a [directoryDefinition](../resources/synchronization-directorydefinition.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/concepts/permissions-reference.md).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /servicePrincipals/{servicePrincipalsId}/synchronization/jobs/{synchronizationJobId}/schema/directories/{directoryDefinitionId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [directoryDefinition](../resources/synchronization-directorydefinition.md) object.

The following table shows the properties that are required when you create the [directoryDefinition](../resources/synchronization-directorydefinition.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|discoveryDateTime|DateTimeOffset|**TODO: Add Description**|
|discoverabilities|directoryDefinitionDiscoverabilities|**TODO: Add Description**. Possible values are: `None`, `AttributeNames`, `AttributeDataTypes`, `AttributeReadOnly`, `ReferenceAttributes`, `UnknownFutureValue`.|
|name|String|**TODO: Add Description**|
|objects|[objectDefinition](../resources/synchronization-objectdefinition.md) collection|**TODO: Add Description**|
|readOnly|Boolean|**TODO: Add Description**|
|version|String|**TODO: Add Description**|



## Response

If successful, this method returns a `200 OK` response code and an updated [directoryDefinition](../resources/synchronization-directorydefinition.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_directorydefinition"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/servicePrincipals/{servicePrincipalsId}/synchronization/jobs/{synchronizationJobId}/schema/directories/{directoryDefinitionId}
Content-Type: application/json
Content-length: 305

{
  "@odata.type": "#microsoft.graph.directoryDefinition",
  "discoveryDateTime": "String (timestamp)",
  "discoverabilities": "String",
  "name": "String",
  "objects": [
    {
      "@odata.type": "microsoft.graph.objectDefinition"
    }
  ],
  "readOnly": "Boolean",
  "version": "String"
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json
{
  "@odata.type": "#microsoft.graph.directoryDefinition",
  "id": "77aa8dd0-8dd0-77aa-d08d-aa77d08daa77",
  "discoveryDateTime": "String (timestamp)",
  "discoverabilities": "String",
  "name": "String",
  "objects": [
    {
      "@odata.type": "microsoft.graph.objectDefinition"
    }
  ],
  "readOnly": "Boolean",
  "version": "String"
}
```

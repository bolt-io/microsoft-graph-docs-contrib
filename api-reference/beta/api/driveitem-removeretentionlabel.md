---
title: "driveItem: removeRetentionLabel"
description: "Remove a retention label from a driveItem."
author: "kyracatwork"
ms.localizationpriority: medium
ms.prod: "files"
doc_type: apiPageType
---

# driveItem: removeRetentionLabel

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Remove a retention label from a [driveItem](../resources/driveitem.md).

For information about retention labels from an administrator's perspective, see [Use retention labels to manage the lifecycle of documents stored in SharePoint](/microsoft-365/compliance/auto-apply-retention-labels-scenario).

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Type                                   | Permissions (from least to most privileged)                                     |
|:---------------------------------------|:--------------------------------------------------------------------------------|
| Delegated (work or school account)     | Files.Read.All, Files.ReadWrite.All, Sites.ReadWrite.All, Sites.FullControl.All |
| Delegated (personal Microsoft account) | Not supported.                                                                  |
| Application                            | Files.Read.All, Files.ReadWrite.All, Sites.ReadWrite.All                        |

>**Note:** `Sites.FullControl.All` is the least privileged permission required to remove retention labels that classify the content as records.

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
```http
DELETE /driveitem/retentionLabel
DELETE /drives/{drive-id}/items/{id}/retentionLabel
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body

Don't supply a request body for this method.

## Response

If successful, this method returns a `204 No Content` response code. It doesn't return anything in the response body.

## Examples

### Request

The following shows an example of a request.

<!-- {
  "blockType": "request",
  "name": "driveItem_removeRetentionLabel",
  "sampleKeys": ["22e064df-3562-4a3c-98c3-74721ca06aa0", "44d372fc-2eb6-4c85-8538-f3a0386a568f"]
}
-->

```http
DELETE https://graph.microsoft.com/beta/drives/22e064df-3562-4a3c-98c3-74721ca06aa0/items/44d372fc-2eb6-4c85-8538-f3a0386a568f/retentionLabel
```

### Response

The following shows an example of the response.

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```

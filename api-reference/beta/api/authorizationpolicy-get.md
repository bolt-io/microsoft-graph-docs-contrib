---
title: "Get authorizationPolicy"
description: "Retrieve the properties and relationships of authorizationPolicy object."
ms.localizationpriority: medium
author: "DougKirschner"
ms.prod: "identity-and-sign-in"
doc_type: apiPageType
---

# Get authorizationPolicy

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Retrieve the properties of an [authorizationPolicy](../resources/authorizationpolicy.md) object.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
| Delegated (work or school account)     | Policy.Read.All, Policy.ReadWrite.Authorization |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | Policy.Read.All, Policy.ReadWrite.Authorization |

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
GET /policies/authorizationPolicy
```

## Request headers

| Name      |Description|
|:----------|:----------|
| Authorization | Bearer {token}. Required. |

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and the single [authorizationPolicy](../resources/authorizationpolicy.md) object in the response body.

## Examples

### Request

The following is an example of the request.

<!-- {
  "blockType": "request",
  "name": "get_authorizationpolicy"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/beta/policies/authorizationPolicy
```

### Response

The following is an example of the response.

> **Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.authorizationPolicy"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#policies/authorizationPolicy",
    "@microsoft.graph.tips": "Use $select to choose only the properties your app needs, as this can lead to performance improvements. For example: GET policies/authorizationPolicy?$select=allowedToSignUpEmailBasedSubscriptions,allowedToUseSSPR",
    "value": [
        {
            "id": "authorizationPolicy",
            "allowInvitesFrom": "everyone",
            "allowedToSignUpEmailBasedSubscriptions": true,
            "allowedToUseSSPR": true,
            "allowEmailVerifiedUsersToJoinOrganization": false,
            "allowUserConsentForRiskyApps": null,
            "blockMsolPowerShell": false,
            "description": "Used to manage authorization related settings across the company.",
            "displayName": "Authorization Policy",
            "enabledPreviewFeatures": [],
            "guestUserRoleId": "10dae51f-b6af-4016-8d66-8c2a99b929b3",
            "permissionGrantPolicyIdsAssignedToDefaultUserRole": [
                "ManagePermissionGrantsForSelf.microsoft-user-default-legacy"
            ],
            "defaultUserRolePermissions": {
                "allowedToCreateApps": false,
                "allowedToCreateSecurityGroups": true,
                "allowedToCreateTenants": true,
                "allowedToReadBitlockerKeysForOwnedDevice": true,
                "allowedToReadOtherUsers": true
            }
        }
    ]
}
```



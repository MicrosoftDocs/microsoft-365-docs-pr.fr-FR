---
title: API Ajouter ou supprimer des balises d’ordinateur
description: Découvrez comment utiliser l’API Ajouter ou supprimer des balises d’ordinateur pour ajouter ou supprimer une balise pour un ordinateur dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, balises, balises d’ordinateur
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 3818fc0050790b2c3b307f95ee0760c516cbf893
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52769820"
---
# <a name="add-or-remove-machine-tags-api"></a>API Ajouter ou supprimer des balises d’ordinateur

**S’applique à :**

- [Microsoft Defender pour point de terminaison](https://go.microsoft.com/fwlink/p/?linkid=2154037)

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

> Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a>Description de l’API

Ajoute ou supprime une balise à un ordinateur [spécifique.](machine.md)

## <a name="limitations"></a>Limites

1. Vous pouvez publier sur les ordinateurs pour la dernière fois en fonction de votre période de rétention configurée.

2. Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.


## <a name="permissions"></a>Autorisations

L’une des autorisations suivantes est nécessaire pour appeler cette API. Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Defender pour les API de point de terminaison](apis-intro.md)

Type d’autorisation |    Autorisation    |    Nom d’affichage de l’autorisation
:---|:---|:---
Application |    Machine.ReadWrite.All |    « Lire et écrire toutes les informations sur l’ordinateur »
Déléguée (compte professionnel ou scolaire) | Machine.ReadWrite | « Lire et écrire des informations sur l’ordinateur »

>[!Note]
> Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :
>
>- L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Gérer le paramètre de sécurité ». Pour plus d’informations ,voir [Créer et gérer des rôles](user-roles.md) pour plus d’informations)
>- L’utilisateur doit avoir accès à l’ordinateur, en fonction des paramètres de groupe d’ordinateurs (voir Créer et gérer des groupes [d’ordinateurs](machine-groups.md) pour plus d’informations)

## <a name="http-request"></a>Requête HTTP

```http
POST https://api.securitycenter.microsoft.com/api/machines/{id}/tags
```

## <a name="request-headers"></a>En-têtes de demande

Nom | Type | Description
:---|:---|:---
Autorisation | String | Porteur {token}. **Obligatoire**.
Content-Type | string | application/json. **Obligatoire**.

## <a name="request-body"></a>Corps de la demande

Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :

Paramètre |    Type    | Description
:---|:---|:---
Valeur |    String |    Nom de la balise. **Obligatoire**.
Action    | Énum |    Ajouter ou supprimer. Les valeurs autorisées sont : « Ajouter » ou « Supprimer ». **Obligatoire**.


## <a name="response"></a>Réponse

Si elle réussit, cette méthode renvoie le code de réponse 200 - OK et l’ordinateur mis à jour dans le corps de la réponse.

## <a name="example"></a>Exemple

**Demande**

Voici un exemple de demande qui ajoute une balise d’ordinateur.

```http
POST https://api.securitycenter.microsoft.com/api/machines/1e5bc9d7e413ddd7902c2932e418702b84d0cc07/tags
```

```json
{
  "Value" : "test Tag 2",
  "Action": "Add"
}
```

- Pour supprimer la balise de l’ordinateur, définissez l’action sur « Supprimer » au lieu de « Ajouter » dans le corps de la demande.

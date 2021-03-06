---
title: Configurer votre Hub d’événements
description: Découvrez comment configurer votre Hub d’événements
keywords: hub d’événements, configurer, informations
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
localization_priority: normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
MS.technology: mde
ms.openlocfilehash: d28ad22721e22dfd0dc5962bd46bab2b45469781
ms.sourcegitcommit: 34c06715e036255faa75c66ebf95c12a85f8ef42
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "52985586"
---
# <a name="configure-your-event-hub"></a>Configurer votre Hub d’événements

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

**S’applique à :**
- [Microsoft 365 Defender](https://go.microsoft.com/fwlink/?linkid=2118804)

Découvrez comment configurer votre Hub d’événements afin qu’il puisse inger des événements à partir Microsoft 365 Defender.


## <a name="setup-the-required-resource-provider-in-the-event-hub-subscription"></a>Configurer le fournisseur de ressources requis dans l’abonnement Event Hub


1. Connectez-vous au [Portail Azure](https://portal.azure.com).
1. Select **Subscriptions \> { Select the subscription the event hub will be ***deployed to***} Resource \> providers**.
1. Vérifiez que **le fournisseur Microsoft.Informations** est inscrit. Sinon, inscrivez-le.

![Image des fournisseurs de ressources dans Microsoft Azure](../../media/f893db7a7b1f7aa520e8b9257cc72562.png)

## <a name="setup-azure-active-directory-app-registration"></a>Configuration de Azure Active Directory’inscription d’application


>! [REMARQUE] Vous devez avoir le rôle Administrateur ou Azure Active Directory (AAD) doit être définie pour autoriser les non-administrateurs à inscrire des applications. Vous devez également avoir un rôle Propriétaire ou Administrateur d’accès utilisateur pour attribuer un rôle au principal de service.  
>Pour plus d’informations, voir Créer une application Azure AD & principal de service dans le [portail - Plateforme d’identités Microsoft Documents \| Microsoft](/azure/active-directory/develop/howto-create-service-principal-portal).

1. Créez une nouvelle inscription (qui crée par nature un principal de service) dans **\> Azure Active Directory’application Nouvelle \> inscription.**

1. Remplissez le formulaire avec uniquement le nom (aucun URI de redirection n’est requis).

    ![Image de l’inscription d’une application](../../media/336bc84e6be23900c43232b4ef0c253c.png)

    ![Image des informations de vue d’ensemble](../../media/06ac04c4ff713c2065cec2ef2f99a294.png)

1. Créez une secret en cliquant sur **Certificats & Clés secrètes \> client Nouvelle :**

    ![Image des certificats et des secrets](../../media/d2ef88d3d2310d2c60c294b569cdf02e.png)

>[!WARNING]
>**Vous ne pourrez plus accéder à la secret client, veillez donc à l’enregistrer.**

## <a name="setup-event-hub-namespace"></a>Espace de noms Du Hub d’événements d’installation


1. Créez un espace de noms Event Hub :

    Go **to Event Hubs \> Add** and select the pricing tier, throughput units and Auto-Présoute (requires standard pricing and under features) appropriate for the load you are expecting.  
    Pour plus d’informations, voir [Tarification - Hubs \| d’événements Microsoft Azure](https://azure.microsoft.com/en-us/pricing/details/event-hubs/)

    >[!NOTE]
    > Vous pouvez utiliser un hub d’événements existant, mais le débit et la mise à l’échelle sont définies au niveau de l’espace de noms. Il est donc recommandé de placer un hub d’événements dans son espace de noms.

   ![Image de l’espace de noms Du Hub d’événements](../../media/ebc4ca37c342ad1da75c4aee4018e51a.png)

1. Vous aurez également besoin de l’ID de ressource de cet espace de noms Event Hub. Go to your Azure Event Hubs namespace page \> Properties. Copiez le texte sous L’ID de ressource et enregistrez-le pour l’utiliser dans la section Configuration M365 ci-dessous. 

    ![Image des propriétés](../../media/759498162a4e93cbf17c4130d704d164.png)

1. Une fois l’espace de noms Hub d’événements créé, vous devez ajouter le principal du service d’inscription d’application en tant que lecteur, récepteur de données Azure Event Hubs et utilisateur qui se connectera à Microsoft 365 Defender en tant que collaborateur (cette opération peut également être effectuée au niveau du groupe de ressources ou de l’abonnement).

    Cette tâche est effectuée dans **Event Hubs Namespace \> Access Control (IAM) \>** Add and verify under **Role assignments**:

    ![Image du contrôle d’accès](../../media/9c9c29137b90d5858920202d87680d16.png)

## <a name="setup-event-hub"></a>Configurer le Hub d’événements


**Option 1 :**

Vous pouvez créer un Hub d’événements dans votre espace de noms et tous les types d’événements (Tables) que vous sélectionnez pour l’exportation seront écrits dans ce **hub** d’événements. 

**Option 2 :**

Au lieu d’exporter tous les types d’événements (tables) dans un hub d’événements, vous pouvez exporter chaque table dans un hub d’événements différent à l’intérieur de votre espace de noms Event Hub (un Hub d’événements par type d’événement).  

Dans cette option, Microsoft 365 Defender créera des Hubs d’événements pour vous.  
>[!NOTE]
> Si vous utilisez un espace de  noms Event Hub qui ne fait pas partie d’un cluster Event Hub, vous ne pourrez choisir que jusqu’à 10 types d’événements (Tables) à exporter dans chaque Paramètres d’exportation que vous définissez, en raison d’une limite Azure de 10 hubs d’événements par espace de noms Event Hub.

Par exemple :

![Image de l’exemple de Hub d’événements](../../media/005c1f6c10c34420d387f594987f9ffe.png)

Si vous choisissez cette option, vous pouvez passer à la section Configurer [Microsoft 365 Defender pour envoyer des tables de courrier](#configure-microsoft-365-defender-to-send-email-tables) électronique.

Créez un Hub d’événements dans votre espace de noms en sélectionnant **Hubs d’événements \> + Hub d’événements.**

Le nombre de partitions autorise un débit supplémentaire via le parallélisme. Il est donc recommandé d’augmenter ce nombre en fonction de la charge que vous attendez.  
Les valeurs de rétention et de capture des messages par défaut de 1 et De sont recommandées.

![Image de créer un Hub d’événements](../../media/1db04b8ec02a6298d7cc70419ac6e6a9.png)

Pour ce Hub d’événements (et non un espace de noms), vous devez configurer une stratégie d’accès partagé avec envoyer, écouter les revendications. Cliquez sur vos stratégies d’accès partagé du Hub d’événements **\> \> +** Ajoutez-le, puis donnez-lui un nom de stratégie (non utilisé ailleurs) et vérifiez **Envoyer** et **écouter.**

![Image des stratégies d’accès partagé](../../media/1867d13f46dc6a0f4cdae6cf00df24db.png)

## <a name="configure-microsoft-365-defender-to-send-email-tables"></a>Configurer les Microsoft 365 Defender pour envoyer des tables de courrier électronique


### <a name="setup-microsoft-365-defender-send-email-tables-to-splunk-via-event-hub"></a>Configurer Microsoft 365 Defender envoyer des tables de messagerie à Splunk via le Hub d’événements


1. Connectez-vous Microsoft 365 Defender avec <https://security.microsoft.com> un compte qui répond à toutes les exigences de rôle suivantes :

    - Rôle de collaborateur au niveau de la ressource d’espace de noms *du* Hub d’événements ou supérieur pour le Hub d’événements vers qui vous allez exporter. Sans cela, vous obtenez une erreur d’exportation lorsque vous essayez d’enregistrer les paramètres.

    - Rôle d’administrateur global ou d’administrateur de sécurité sur le client lié à Microsoft 365 Defender azure.

    ![Image du portail de sécurité](../../media/55d5b1c21dd58692fb12a6c1c35bd4fa.png)

1. Cliquez sur **Exportation de données \> brutes +Ajouter.**

    Vous allez maintenant utiliser les données que vous avez enregistrées ci-dessus.

    **Nom**: il s’agit d’un environnement local qui doit être tout ce qui fonctionne dans votre environnement.

    **Forward events to event hub**: Select this checkbox.

    **ID de ressource Event-Hub**: il s’agit de l’ID de ressource d’espace de noms Event Hub que vous avez enregistré ci-dessus lors de la configuration du Hub d’événements.

    **Nom du Hub** d’événements : si vous avez créé un Hub d’événements à l’intérieur de votre espace de noms Event Hub, collez le nom du Hub d’événements que vous avez enregistré ci-dessus.

    Si vous choisissez de laisser Microsoft 365 Defender créer des hubs d’événements par types d’événements (Tables) pour vous, laissez ce champ vide.

    **Types** d’événements : sélectionnez les tables de recherche avancée que vous souhaitez faire suivre au Hub d’événements, puis à votre application personnalisée. Les tables d’alerte sont Microsoft 365 Defender, les tables Périphériques sont de Microsoft Defender pour point de terminaison (PEPT) et les tables de messagerie sont de Microsoft Defender pour Office 365. Les événements de messagerie enregistrent toutes les transactions de messagerie. Les événements URL (SafeLinks), Attachment (Safe Attachments) et POST Delivery Events (ZAP) sont également enregistrés et peuvent être joints aux événements de messagerie sur le champ NetworkMessageId.

    ![Image des paramètres de l’API de diffusion en continu](../../media/3b2ad64b6ef0f88cf0175f8d57ef8b97.png)

1. Veillez à cliquer sur **Envoyer.**

### <a name="verify-that-the-events-are-being-exported-to-the-event-hub"></a>Vérifier que les événements sont exportés vers le Hub d’événements


Vous pouvez vérifier que les événements sont envoyés au Hub d’événements en exécutant une requête de recherche avancée de base. Sélectionnez **Une requête de recherche avancée \> \> et** entrez la requête suivante :

```
EmailEvents
|joinkind=fullouterEmailAttachmentInfoonNetworkMessageId
|joinkind=fullouterEmailUrlInfoonNetworkMessageId
|joinkind=fullouterEmailPostDeliveryEventsonNetworkMessageId
|whereTimestamp\>ago(1h)
|count
```

Cela vous indique le nombre d’e-mails reçus au cours de la dernière heure, joints à tous les autres tableaux. Elle vous indique également si vous voyez des événements qui peuvent être exportés vers le hub d’événements. Si ce nombre indique 0, vous ne verrez aucune donnée sortante vers le Hub d’événements.

![Image de recherche avancée](../../media/c305e57dc6f72fa9eb035943f244738e.png)

Une fois que vous avez vérifié qu’il existe des données à exporter, vous pouvez afficher le Hub d’événements pour vérifier que les messages sont entrants. Cela peut prendre jusqu’à une heure. 
 
1. Dans Azure, go to **Event Hubs \> Click on the Namespace Event \> Hubs Click on the Event \> Hub**.  
1. Sous **Vue d’ensemble,** faites défiler vers le bas et dans le graphique Messages, vous devriez voir les messages entrants. Si vous ne voyez aucun résultat, il n’y aura aucun message pour l’ing d’une application personnalisée.

    ![Image de l’onglet Vue d’ensemble avec des messages](../../media/e88060e315d76e74269a3fc866df047f.png)

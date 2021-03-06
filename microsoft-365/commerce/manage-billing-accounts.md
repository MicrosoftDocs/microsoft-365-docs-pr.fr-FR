---
title: Comprendre les comptes de facturation
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
ms.reviewer: tugu, jmueller
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- AdminSurgePortfolio
- commerce_billing
search.appverid: MET150
description: Découvrez les comptes de facturation et leur utilisation pour gérer les paramètres de compte, les factures, les modes de paiement et les achats.
ms.date: 03/17/2021
ms.openlocfilehash: 1eb01ace2fe8b84b813793168cb50db2508b4ebb
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52535637"
---
# <a name="understand-billing-accounts"></a>Comprendre les comptes de facturation

Un compte de facturation est créé lorsque vous vous inscrivez pour essayer ou acheter des produits Microsoft. Vous utilisez votre compte de facturation pour gérer vos paramètres de compte, factures, modes de paiement et achats. Vous pouvez avoir accès à plusieurs comptes de facturation. Par exemple, vous vous êtes inscrit à Microsoft 365 directement, ou vous avez accès au contrat de Accord Entreprise de votre organisation, au contrat de services Microsoft Product & ou au contrat client Microsoft. Pour chacun de ces scénarios, vous avez un compte de facturation distinct.

Le centre Microsoft 365'administration centrale prend actuellement en charge le type de compte de facturation suivant :

- Microsoft Online Services programme : ce compte de facturation est créé lorsque vous vous inscrivez à un abonnement Microsoft 365 directement.
- Programme MPSA (Contrat de service de gestion des produits & Microsoft) : ce compte de facturation est créé lorsque votre organisation signe un contrat de licence en volume MPSA pour acheter des logiciels et des services en ligne.
- Contrat client Microsoft : ce compte de facturation est créé lorsque votre organisation travaille avec un représentant Microsoft, un partenaire autorisé ou des achats indépendants.

La page <a href="https://go.microsoft.com/fwlink/p/?linkid=2084771" target="_blank">Comptes de facturation</a> fournit une vue de vos comptes commerciaux avec Microsoft. Par défaut, votre organisation dispose d’au moins un compte de facturation associé à un contrat qui est accepté au moment d’un achat direct ou par le biais d’un accord de licence en volume.

## <a name="understand-billing-account-details"></a>Comprendre les détails du compte de facturation

La partie supérieure de la page **de détails** des comptes de facturation est votre profil de compte et contient des informations juridiques et fiscales sur votre organisation. Vous pouvez mettre à jour votre profil pour modifier votre adresse juridique et votre numéro de téléphone. Ce compte est l’entité juridique qui paie pour les produits que vous achetez.

Le tableau suivant répertorie les termes importants que vous voyez dans la page de **détails** des comptes de facturation.

| Nom du champ | Description |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Adresse de vente | Entité juridique responsable du paiement et identifiée sur la facture. L’adresse fournie ici permet de déterminer votre taux d’imposition, sauf si vous choisissez de fournir une adresse d’expédition alternative pendant votre achat. Si vous souhaitez en savoir plus, consultez l’article [Information sur les taxes](billing-and-payments/tax-information.md). |
| Segment | Champ en lecture seule qui identifie le segment commercial de votre organisation (commercial, éducation, secteur public ou à but non lucratif). |
| État du compte | Champ en lecture seule qui spécifie l’état de votre compte commercial auprès de Microsoft. |
| ID de taxe | Si vous êtes en dehors des États-Unis, vous devez fournir une TVA ou un équivalent local. Si vous souhaitez en savoir plus, consultez l’article [Information sur les taxes](billing-and-payments/tax-information.md). |
| Contrat | Lorsqu’un compte de facturation est créé, par le biais d’un achat direct ou d’un accord de licence en volume, une entreprise accepte, ou signe, un contrat qui décrit les conditions d'& du compte. Le cas échéant, cet affichage répertorie un historique des contrats. Si vous devez accepter les termes mis à jour, un lien pour **approuver** le contrat s’affiche. |
| Profils de facturation | Un profil de facturation définit les propriétés de votre facture, telles que la personne qui reçoit la facture, la manière dont la facture est livrée, les conditions de paiement et un numéro de bon de réception. Pour distribuer la facturation au sein de votre organisation, vous pouvez créer plusieurs profils de facturation et identifier le profil de facturation approprié au moment de l’achat. Pour plus d’informations sur les profils de facturation et sur la façon dont vous pouvez les utiliser pour créer des options de facturation plus flexibles pour votre organisation, [comprenez les profils de facturation.](billing-and-payments/manage-billing-profiles.md) |

> [!NOTE]
> Si vous devez  modifier le nom ou l’adresse de  vente, mais que vous ne voyez pas de lien Modifier, vous devez contacter le [support](../business-video/get-help-support.md) technique pour le modifier. Les demandes de modification **de nom de** vente nécessiteront une vérification de solvabilité. Remplissez [ce formulaire](https://www.microsoft.com/download/details.aspx?id=102732)et êtes prêt à partager l’un des documents suivants avec Microsoft lorsque vous contactez le support technique :
>
> - Document émis par le gouvernement ou lettre d’inscription
> - Imprimer à partir du Registre de la société locale
>
> Le support peut vous aider à modifier le nom et l’adresse lorsque seul le nom du client change, mais que l’entité reste la même. La documentation fournie doit clairement montrer que seul le nom de l’entité a changé. Si la modification est le résultat d’une transaction, y compris la vente d’entreprise, un changement de contrôle ou une scission ou une « rotation » d’une filiale du client, contactez votre vendeur Microsoft.

## <a name="shipping-addresses"></a>Adresses d’expédition

Cette section répertorie les adresses d’expédition associées à votre compte de facturation. Lorsque vous achetez un achat, vous pouvez utiliser cette adresse pour identifier l’endroit où votre achat est expédié ou utilisé. L’adresse d’expédition est modifiable. Vous pouvez ajouter une adresse d’expédition ou mettre à jour l’adresse existante. Cette adresse permet de déterminer le taux de taxe pour votre achat.

## <a name="understand-access-to-billing-accounts"></a>Comprendre l’accès aux comptes de facturation

Vous pouvez fournir à d’autres utilisateurs l’accès au compte de facturation dans Microsoft 365 centre d’administration via des rôles et des autorisations. Seul un propriétaire de compte de facturation peut accorder l’accès à un compte de facturation. Vous pouvez attribuer l’un des rôles suivants aux utilisateurs :

- **Propriétaire du compte de facturation** &mdash; Peut attribuer des autorisations, modifier des comptes, signer des contrats et afficher des comptes.
- **Collaborateur de compte de facturation** &mdash; Peut modifier des comptes, signer des contrats et afficher des comptes.
- **Lecteur de compte de facturation** &mdash; Peut afficher les comptes.

> [!Note]
> Les rôles de compte de facturation s’appliquent uniquement aux comptes de facturation et ne s’appliquent pas aux autres Microsoft 365 du Centre d’administration.

## <a name="related-content"></a>Contenu associé

[Informations fiscales](billing-and-payments/tax-information.md) (article) \
[Comprendre les profils de](billing-and-payments/manage-billing-profiles.md) facturation (article)

---
title: Collaborer avec des personnes extérieures à votre organisation
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: ITPro
ms.topic: article
ms.prod: microsoft-365-enterprise
ms.collection:
- SPO_Content
- M365-collaboration
- m365solution-securecollab
- m365solution-scenario
- m365initiative-externalcollab
ms.custom:
- seo-marvel-apr2020
- seo-marvel-jun2020
localization_priority: Normal
f1.keywords: NOCSH
description: Découvrez comment configurer des applications Microsoft 365 telles que Teams, OneDrive et SharePoint pour la collaboration avec des personnes extérieures à votre organisation.
ms.openlocfilehash: 359e72c12c43ca1ea984f93d87ab4868e6d1eb66
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50916393"
---
# <a name="collaborating-with-people-outside-your-organization"></a><span data-ttu-id="f357e-103">Collaborer avec des personnes extérieures à votre organisation</span><span class="sxs-lookup"><span data-stu-id="f357e-103">Collaborating with people outside your organization</span></span>

<span data-ttu-id="f357e-104">Les fonctionnalités de partage externe dans Microsoft 365 permettent aux membres de votre organisation de collaborer avec des partenaires, des fournisseurs, des clients et d’autres personnes qui n’ont pas de compte dans votre annuaire.</span><span class="sxs-lookup"><span data-stu-id="f357e-104">The external sharing capabilities in Microsoft 365 provide an opportunity for people in your organization to collaborate with partners, vendors, customers, and others who don't have an account in your directory.</span></span> <span data-ttu-id="f357e-105">Vous pouvez partager des équipes ou des sites entiers avec des personnes extérieures à votre organisation, ou simplement des fichiers individuels.</span><span class="sxs-lookup"><span data-stu-id="f357e-105">You can share entire teams or sites with people outside your organization, or just individual files.</span></span>

<span data-ttu-id="f357e-106">La collaboration avec des personnes extérieures à votre organisation comprend deux composants majeurs :</span><span class="sxs-lookup"><span data-stu-id="f357e-106">Collaborating with people outside your organization consists of two major components:</span></span>

- <span data-ttu-id="f357e-107">**Activer le** partage : configurez les contrôles de partage dans Azure Active Directory, Teams, groupes Microsoft 365 et SharePoint pour autoriser le niveau de partage voulu pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f357e-107">**Enable sharing** - Configure the sharing controls across Azure Active Directory, Teams, Microsoft 365 Groups, and SharePoint to allow the level of sharing that you want for your organization.</span></span>
- <span data-ttu-id="f357e-108"> Activer une sécurité supplémentaire : alors que les fonctionnalités de partage de base peuvent être configurées pour exiger l’authentification des personnes extérieures à votre organisation, Microsoft 365 fournit de nombreuses fonctionnalités de sécurité et de conformité supplémentaires pour vous aider à protéger vos données et à maintenir vos stratégies de gouvernance tout en partageant en externe.</span><span class="sxs-lookup"><span data-stu-id="f357e-108">**Enable additional security** - While the basic sharing features can be configured to require people outside your organization to authenticate, Microsoft 365 provides many additional security and compliance features to help you protect your data and maintain your governance policies while sharing externally.</span></span>

## <a name="enable-sharing"></a><span data-ttu-id="f357e-109">Activer le partage</span><span class="sxs-lookup"><span data-stu-id="f357e-109">Enable sharing</span></span>

<span data-ttu-id="f357e-110">Par défaut, dans Microsoft 365, le partage avec des personnes extérieures à votre organisation est activé.</span><span class="sxs-lookup"><span data-stu-id="f357e-110">By default, in Microsoft 365, sharing with people outside your organization is enabled.</span></span> <span data-ttu-id="f357e-111">De nombreux scénarios de partage externe fonctionnent sans configuration supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="f357e-111">Many external sharing scenarios work without further configuration.</span></span> <span data-ttu-id="f357e-112">Pour confirmer les paramètres d’un scénario que vous utilisez ou en activer un nouveau, choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="f357e-112">To confirm the settings for a scenario that you're using, or enable a new one, choose from the following options:</span></span>

- <span data-ttu-id="f357e-113">[Collaborer sur](collaborate-on-documents.md) des documents : découvrez comment configurer Microsoft 365 pour autoriser le partage et la collaboration avec des personnes extérieures à votre organisation (invités et utilisateurs non authentifiés) sur des fichiers et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="f357e-113">[Collaborate on documents](collaborate-on-documents.md) - Learn how to configure Microsoft 365 to allow sharing and collaboration with people outside your organization (both guests and unauthenticated users) on files and folders.</span></span>
- <span data-ttu-id="f357e-114">[Collaborer dans un site](collaborate-in-site.md) : découvrez comment configurer Microsoft 365 pour activer le partage de sites SharePoint avec des invités.</span><span class="sxs-lookup"><span data-stu-id="f357e-114">[Collaborate in a site](collaborate-in-site.md) - Learn how to configure Microsoft 365 to enable sharing SharePoint sites with guests.</span></span>
- <span data-ttu-id="f357e-115">[Collaborer en équipe](collaborate-as-team.md) : découvrez comment configurer Microsoft 365 pour activer la collaboration avec les invités dans Teams.</span><span class="sxs-lookup"><span data-stu-id="f357e-115">[Collaborate as a team](collaborate-as-team.md) - Learn how to configure Microsoft 365 to enable guest collaboration in Teams.</span></span>

<span data-ttu-id="f357e-116">Pour un aperçu complet des paramètres de partage d’invités disponibles dans Microsoft 365, consultez la référence des paramètres de partage d’invités [Microsoft 365.](microsoft-365-guest-settings.md)</span><span class="sxs-lookup"><span data-stu-id="f357e-116">For a comprehensive look at the guest sharing settings available across Microsoft 365, see [Microsoft 365 guest sharing settings reference](microsoft-365-guest-settings.md).</span></span>

## <a name="enable-additional-security"></a><span data-ttu-id="f357e-117">Activer la sécurité supplémentaire</span><span class="sxs-lookup"><span data-stu-id="f357e-117">Enable additional security</span></span>

<span data-ttu-id="f357e-118">Une fois que vous avez activé le scénario que vous souhaitez utiliser pour le partage avec des personnes extérieures à votre organisation, envisagez des protections supplémentaires pour protéger votre contenu contre un partage accidentel ou intentionnel.</span><span class="sxs-lookup"><span data-stu-id="f357e-118">Once you've enabled the scenario that you want to use for sharing with people outside your organization, consider additional safeguards to help protect your content from accidental or intentional inappropriate sharing.</span></span>

- <span data-ttu-id="f357e-119">[Meilleures pratiques pour le partage](best-practices-anonymous-sharing.md) de fichiers et de dossiers avec des utilisateurs non authentifiés : découvrez les meilleures pratiques de partage avec des utilisateurs non authentifiés.</span><span class="sxs-lookup"><span data-stu-id="f357e-119">[Best practices for sharing files and folders with unauthenticated users](best-practices-anonymous-sharing.md) - Learn about best practices for sharing with unauthenticated users.</span></span>
- <span data-ttu-id="f357e-120">[Limiter l’exposition](share-limit-accidental-exposure.md) accidentelle : découvrez comment réduire les risques de partager accidentellement du contenu sensible avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f357e-120">[Limit accidental exposure](share-limit-accidental-exposure.md) - Learn how to reduce the chances of accidentally sharing sensitive content with people outside your organization.</span></span>
- <span data-ttu-id="f357e-121">[](create-secure-guest-sharing-environment.md) Créez un environnement de partage d’invités sécurisé : découvrez les outils fournis dans Microsoft 365 pour vous assurer que le partage avec des personnes extérieures à votre organisation est effectué de manière sécurisée et répond à vos exigences de gouvernance.</span><span class="sxs-lookup"><span data-stu-id="f357e-121">[Create a secure guest sharing environment](create-secure-guest-sharing-environment.md) - Learn about the tools provided in Microsoft 365 to help ensure that sharing with people outside your organization is done in a safe and secure manner and meets your governance requirements.</span></span>

## <a name="collaborate-with-partner-companies"></a><span data-ttu-id="f357e-122">Collaborer avec des entreprises partenaires</span><span class="sxs-lookup"><span data-stu-id="f357e-122">Collaborate with partner companies</span></span>

<span data-ttu-id="f357e-123">Lorsque vous travaillez sur un projet de grande envergure qui implique de nombreux invités d’une autre organisation, ou si vous avez une relation de fournisseur permanente dans laquelle les invités changent souvent, vous pouvez utiliser la gestion des droits dans Azure Active Directory pour simplifier la gestion des invités et permettre à la société partenaire de partager cette responsabilité.</span><span class="sxs-lookup"><span data-stu-id="f357e-123">When you're working on a large project that involves many guests from another organization, or if you have an ongoing vendor relationship in which guests are often changing, you can use entitlement management in Azure Active Directory to simplify guest management and allow the partner company to share in that responsibility.</span></span> <span data-ttu-id="f357e-124">Pour plus d’informations, voir Créer un [extranet B2B](b2b-extranet.md) avec des invités gérés.</span><span class="sxs-lookup"><span data-stu-id="f357e-124">See [Create a B2B extranet with managed guests](b2b-extranet.md) for details.</span></span>

## <a name="limit-sharing"></a><span data-ttu-id="f357e-125">Limiter le partage</span><span class="sxs-lookup"><span data-stu-id="f357e-125">Limit sharing</span></span>

<span data-ttu-id="f357e-126">Si certaines fonctionnalités de partage dans Microsoft 365 entrent en conflit avec vos stratégies de gouvernance, voir Limiter le partage dans [Microsoft 365](microsoft-365-limit-sharing.md) pour en savoir plus sur les options de limitation du partage.</span><span class="sxs-lookup"><span data-stu-id="f357e-126">If some of the sharing features in Microsoft 365 conflict with your governance policies, see [Limit sharing in Microsoft 365](microsoft-365-limit-sharing.md) to learn about options for limiting sharing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f357e-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f357e-127">Related topics</span></span>

[<span data-ttu-id="f357e-128">Introduction à la collaboration sur les fichiers dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f357e-128">Intro to file collaboration in Microsoft 365</span></span>](/sharepoint/intro-to-file-collaboration)

[<span data-ttu-id="f357e-129">Planifier la collaboration de fichiers dans SharePoint avec Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f357e-129">Plan file collaboration in SharePoint with Microsoft 365</span></span>](/sharepoint/deploy-file-collaboration)
---
title: Renforcer la protection contre les menaces pour Microsoft 365 Business Premium
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- MiniMaven
- MSB365
- OKR_SMB_M365
- seo-marvel-mar
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
description: Configurer des fonctionnalités de conformité pour éviter la perte de données et sécuriser les informations sensibles de vos clients et de vos clients.
ms.openlocfilehash: e210787718025c5df29af8d4a2283291dcecc2a8
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50912527"
---
# <a name="set-up-compliance-features"></a><span data-ttu-id="2078d-103">Configurer les fonctionnalités de conformité</span><span class="sxs-lookup"><span data-stu-id="2078d-103">Set up compliance features</span></span>

<span data-ttu-id="2078d-104">Votre Abonnement Microsoft 365 Business Premium comprend des fonctionnalités pour protéger vos données et appareils et vous aider à sécuriser les informations sensibles de vos clients et de vos clients.</span><span class="sxs-lookup"><span data-stu-id="2078d-104">Your Microsoft 365 Business Premium comes with features to protect your data and devices, and help you keep your and your customers' sensitive information secure.</span></span>

## <a name="set-up-dlp-features"></a><span data-ttu-id="2078d-105">Configurer les fonctionnalités DLP</span><span class="sxs-lookup"><span data-stu-id="2078d-105">Set up DLP features</span></span>

<span data-ttu-id="2078d-106">Voir [Créer une stratégie DLP à partir](../compliance/create-a-dlp-policy-from-a-template.md) d’un modèle pour obtenir un exemple sur la façon de configurer une stratégie pour protéger contre la perte de données personnelles.</span><span class="sxs-lookup"><span data-stu-id="2078d-106">See [Create a DLP policy from a template](../compliance/create-a-dlp-policy-from-a-template.md) for an example on how to set up a policy to protect against protect loss of personal data.</span></span> 
  
<span data-ttu-id="2078d-107">DLP est livré avec de nombreux modèles de stratégie prêts à l’emploi pour de nombreux paramètres régionaux différents.</span><span class="sxs-lookup"><span data-stu-id="2078d-107">DLP comes with many ready-to-use policy templates for many different locales.</span></span> <span data-ttu-id="2078d-108">Par exemple, les données financières en Australie, la Loi canadienne sur les informations personnelles, les données financières américaines, etc.</span><span class="sxs-lookup"><span data-stu-id="2078d-108">For example, Australia Financial Data, Canada Personal Information Act, U.S. Financial Data, and so on.</span></span> <span data-ttu-id="2078d-109">Voir [ce que les modèles](../compliance/what-the-dlp-policy-templates-include.md) de stratégie DLP incluent pour obtenir une liste complète.</span><span class="sxs-lookup"><span data-stu-id="2078d-109">See [What the DLP policy templates include](../compliance/what-the-dlp-policy-templates-include.md) for a full list.</span></span> <span data-ttu-id="2078d-110">Tous ces modèles peuvent être activés de la même façon que l’exemple de modèle PII.</span><span class="sxs-lookup"><span data-stu-id="2078d-110">All of these templates can be enabled similar to the PII template example.</span></span> 
  
## <a name="set-up-email-retention-with-exchange-online-archiving"></a><span data-ttu-id="2078d-111">Configurer la rétention du courrier électronique à l’Archivage Exchange Online</span><span class="sxs-lookup"><span data-stu-id="2078d-111">Set up email retention with Exchange Online Archiving</span></span>

 <span data-ttu-id="2078d-112">**Archivage Exchange Online** licences permettent de maintenir les normes réglementaires et de conformité en conservant le contenu du courrier électronique pour eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="2078d-112">**Exchange Online Archiving** license features help maintain compliance and regulatory standards by preserving email content for eDiscovery.</span></span> <span data-ttu-id="2078d-113">Cela permet également de réduire vos risques en cas de poursuites judiciaires et permet de récupérer des données après une violation de la sécurité ou lorsque vous devez récupérer des éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="2078d-113">It also helps reduce your risk if there is a lawsuit, and provides a way to recover data after a security breach or when you need to recover deleted items.</span></span> <span data-ttu-id="2078d-114">Vous pouvez utiliser la conservation pour litige pour conserver tout le contenu d’un utilisateur ou utiliser des stratégies de rétention pour personnaliser ce que vous souhaitez conserver.</span><span class="sxs-lookup"><span data-stu-id="2078d-114">You can use litigation hold to preserve all of a user's content, or use retention policies to customize what you want to preserve.</span></span>
  
<span data-ttu-id="2078d-115">**Attente pour litige :** Vous pouvez conserver tout le contenu de la boîte aux lettres, y compris les éléments supprimés, en mettant la boîte aux lettres entière d’un utilisateur en attente pour litige.</span><span class="sxs-lookup"><span data-stu-id="2078d-115">**Litigation hold:** You can preserve all mailbox content including deleted items by putting a user's entire mailbox on litigation hold.</span></span> 
    
<span data-ttu-id="2078d-116">Pour placer une boîte aux lettres en attente pour litige, dans le Centre d’administration :</span><span class="sxs-lookup"><span data-stu-id="2078d-116">To place a mailbox on litigation hold, in the Admin center:</span></span>
    
1. <span data-ttu-id="2078d-117">Dans le navigation de gauche, allez à **Utilisateurs** \> **actifs.**</span><span class="sxs-lookup"><span data-stu-id="2078d-117">In the left nav, go to **Users** \> **Active users**.</span></span>
    
2. <span data-ttu-id="2078d-118">Sélectionnez un utilisateur dont vous souhaitez placer la boîte aux lettres en attente pour litige.</span><span class="sxs-lookup"><span data-stu-id="2078d-118">Select a user whose mailbox you want to place on litigation hold.</span></span> <span data-ttu-id="2078d-119">Dans le volet utilisateur, développez **Paramètres de messagerie,** puis en plus des **paramètres,** choisissez **Modifier les propriétés Exchange**.</span><span class="sxs-lookup"><span data-stu-id="2078d-119">In the user pane, expand **Mail settings**, and next to **More settings**, choose **Edit Exchange properties**.</span></span>
    
3. <span data-ttu-id="2078d-120">Dans la page de boîte aux lettres de l’utilisateur, choisissez \*\* fonctionnalités de boîte aux lettres \*\* dans le navigation gauche, puis choisissez le lien Activer sous Attente pour **litige.** </span><span class="sxs-lookup"><span data-stu-id="2078d-120">On the mailbox page for the user, choose \*\* mailbox features \*\* on the left nav, and then choose the **Enable** link under **Litigation hold**.</span></span>
    
4. <span data-ttu-id="2078d-121">Dans la boîte **de dialogue De attente** pour litige, vous pouvez spécifier la durée de la durée de la attente pour litige dans le champ Durée de la durée de la attente **pour** litige.</span><span class="sxs-lookup"><span data-stu-id="2078d-121">In the **litigation hold** dialog box, you can specify the litigation hold duration in the **Litigation hold duration** field.</span></span> <span data-ttu-id="2078d-122">Laissez le champ vide si vous souhaitez placer une attente infinie.</span><span class="sxs-lookup"><span data-stu-id="2078d-122">Leave the field empty if you want to place an infinite hold.</span></span> <span data-ttu-id="2078d-123">Vous pouvez également ajouter des notes et diriger le propriétaire de la boîte aux lettres vers un site web dont vous pourriez avoir besoin pour en savoir plus sur la mise en attente pour litige.</span><span class="sxs-lookup"><span data-stu-id="2078d-123">You can also add notes and direct the mailbox owner to a website you might have to explain more about the litigation hold.</span></span> <span data-ttu-id="2078d-124">\>**Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2078d-124">\> **Save**.</span></span>
    
<span data-ttu-id="2078d-125">**Rétention :** Vous pouvez activer des stratégies de rétention personnalisées, par exemple, pour conserver un certain temps ou supprimer définitivement du contenu à la fin de la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="2078d-125">**Retention:** You can enable customized retention policies, for example, to preserve for a specific amount of time or delete content permanently at the end of the retention period.</span></span> <span data-ttu-id="2078d-126">Pour plus d’informations, voir [Vue d’ensemble des stratégies de rétention.](../compliance/retention.md)</span><span class="sxs-lookup"><span data-stu-id="2078d-126">To learn more, see [Overview of retention policies](../compliance/retention.md).</span></span>

## <a name="set-up-sensitivity-labels"></a><span data-ttu-id="2078d-127">Configurer les étiquettes de niveau de sensibilité</span><span class="sxs-lookup"><span data-stu-id="2078d-127">Set up Sensitivity labels</span></span>

<span data-ttu-id="2078d-128">Les étiquettes de niveau de sensibilité sont disponibles avec Azure Information Protection (AIP) Plan 1 et vous aident à classer et éventuellement protéger vos documents et e-mails en appliquant des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="2078d-128">Sensitivity labels come with Azure Information Protection (AIP) Plan 1, and help you classify, and optionally protect your documents and emails, by applying labels.</span></span> <span data-ttu-id="2078d-129">Les étiquettes peuvent être appliquées automatiquement par les administrateurs qui définissent des règles et des conditions, manuellement par les utilisateurs ou à l’aide d’une combinaison dans laquelle des recommandations sont données aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2078d-129">Labels can be applied automatically by administrators who define rules and conditions, manually by users, or by using a combination where users are given recommendations.</span></span>

<span data-ttu-id="2078d-130">Pour configurer les étiquettes de niveau de sensibilité, affichez la vidéo créer et gérer [les étiquettes de](https://support.microsoft.com/office/2fb96b54-7dd2-4f0c-ac8d-170790d4b8b9) sensibilité.</span><span class="sxs-lookup"><span data-stu-id="2078d-130">To set up Sensitivity labels, view [create and manage sensitivity labels](https://support.microsoft.com/office/2fb96b54-7dd2-4f0c-ac8d-170790d4b8b9) video.</span></span>



### <a name="install-the-azure-information-protection-client-manually"></a><span data-ttu-id="2078d-131">Installer manuellement le client Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="2078d-131">Install the Azure Information Protection client manually</span></span>

<span data-ttu-id="2078d-132">Pour installer manuellement le client AIP :</span><span class="sxs-lookup"><span data-stu-id="2078d-132">To manually install the AIP client:</span></span>

1. <span data-ttu-id="2078d-133">Téléchargez **AzinfoProtection_UL.exe** à partir du [Centre de téléchargement Microsoft.](https://www.microsoft.com/download/details.aspx?id=53018)</span><span class="sxs-lookup"><span data-stu-id="2078d-133">Download **AzinfoProtection_UL.exe** from [Microsoft download center](https://www.microsoft.com/download/details.aspx?id=53018).</span></span>
 
2. <span data-ttu-id="2078d-134">Pour vérifier que l’installation a fonctionné, affichez  un document Word et assurez-vous que l’option Sensibilité est disponible sous l’onglet **Accueil.**</span><span class="sxs-lookup"><span data-stu-id="2078d-134">You can verify that the installation worked by viewing a Word document and making sure that the **Sensitivity** option is available on the **Home** tab.</span></span>
<br/><span data-ttu-id="2078d-135">![Onglet Protection dans un document Word.](../media/word-sensitivity.png)</span><span class="sxs-lookup"><span data-stu-id="2078d-135">![Protection tab drop-down in a Word document.](../media/word-sensitivity.png)</span></span>

<span data-ttu-id="2078d-136">Pour plus d’informations, voir [Installer le client.](/azure/information-protection/infoprotect-tutorial-step3)</span><span class="sxs-lookup"><span data-stu-id="2078d-136">For more information, see [Install the client](/azure/information-protection/infoprotect-tutorial-step3).</span></span>
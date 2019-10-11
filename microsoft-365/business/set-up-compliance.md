---
title: Renforcer la protection contre les menaces pour Microsoft 365 Business
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
ms.custom: OKR_SMB_M365
search.appverid:
- BCS160
- MET150
description: Configurez les fonctionnalités de conformité pour empêcher toute perte de données et étiqueter les données sensibles.
ms.openlocfilehash: a0ba2fa6dbe7c786d577ad7098c1790f569f5acc
ms.sourcegitcommit: 255e8194bb5767a9983d54d16e79d628732a1d97
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/11/2019
ms.locfileid: "37453910"
---
# <a name="set-up-compliance-features"></a><span data-ttu-id="ed39f-103">Configurer les fonctionnalités de conformité</span><span class="sxs-lookup"><span data-stu-id="ed39f-103">Set up compliance features</span></span>

<span data-ttu-id="ed39f-104">Votre entreprise Microsoft 365 est dotée de fonctionnalités pour protéger vos données et périphériques, et vous aider à sécuriser les informations sensibles de vos clients et de vos clients.</span><span class="sxs-lookup"><span data-stu-id="ed39f-104">Your Microsoft 365 Business comes with features to protect your data and devices, and help you keep yours and your customers' sensitive information secure.</span></span>

## <a name="set-up-dlp-features"></a><span data-ttu-id="ed39f-105">Configurer les fonctionnalités DLP</span><span class="sxs-lookup"><span data-stu-id="ed39f-105">Set up DLP features</span></span>

<span data-ttu-id="ed39f-106">Voir [Create a DLP Policy from a template](https://support.office.com/article/59414438-99f5-488b-975c-5023f2254369) pour obtenir un exemple sur la façon de configurer une stratégie de protection contre les informations d’identification personnelle (PII).</span><span class="sxs-lookup"><span data-stu-id="ed39f-106">See [Create a DLP policy from a template](https://support.office.com/article/59414438-99f5-488b-975c-5023f2254369) for an example on how to set up a policy to protect against personally identifiable information (PII).</span></span> 
  
<span data-ttu-id="ed39f-107">DLP comprend de nombreux modèles de stratégie prêts à l’emploi pour de nombreux paramètres régionaux différents.</span><span class="sxs-lookup"><span data-stu-id="ed39f-107">DLP comes with many ready-to-use policy templates for many different locales.</span></span> <span data-ttu-id="ed39f-108">Par exemple, les données financières de l’Australie, le Canada Personal Information Act, les données financières américaines, etc. Consultez la rubrique relative aux [modèles de stratégie DLP](https://support.office.com/article/c2e588d3-8f4f-4937-a286-8c399f28953a) pour une liste complète.</span><span class="sxs-lookup"><span data-stu-id="ed39f-108">For example, Australia Financial Data, Canada Personal Information Act, U.S. Financial Data, etc. See [What the DLP policy templates include](https://support.office.com/article/c2e588d3-8f4f-4937-a286-8c399f28953a) for a full list.</span></span> <span data-ttu-id="ed39f-109">Tous ces modèles peuvent être activés de la même manière que l’exemple de modèle PII.</span><span class="sxs-lookup"><span data-stu-id="ed39f-109">All of these templates can be enabled similar to the PII template example.</span></span> 
  
## <a name="set-up-email-retention-with-exchange-online-archiving"></a><span data-ttu-id="ed39f-110">Configurer la rétention du courrier électronique avec archivage Exchange Online</span><span class="sxs-lookup"><span data-stu-id="ed39f-110">Set up email retention with Exchange Online Archiving</span></span>

 <span data-ttu-id="ed39f-111">Les fonctionnalités de licence d' **archivage Exchange Online** permettent de respecter les normes de conformité et de réglementation en conservant le contenu des courriers électroniques pour eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="ed39f-111">**Exchange Online Archiving** license features help maintain compliance and regulatory standards by preserving email content for eDiscovery.</span></span> <span data-ttu-id="ed39f-112">Elle contribue également à réduire les risques en cas de poursuite et permet de récupérer les données après une violation de la sécurité ou de récupérer des éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="ed39f-112">It also helps reduce your risk in the event of a lawsuit and provides a way to recover data after a security breach, or when you need to recover deleted items.</span></span> <span data-ttu-id="ed39f-113">Vous pouvez utiliser la conservation pour litige pour conserver tout le contenu d’un utilisateur ou utiliser des stratégies de rétention pour personnaliser ce que vous souhaitez conserver.</span><span class="sxs-lookup"><span data-stu-id="ed39f-113">You can use litigation hold to preserve all of a user's content, or use retention policies to customize what you want to preserve.</span></span>
  
<span data-ttu-id="ed39f-114">**Conservation pour litige :** Vous pouvez conserver tout le contenu des boîtes aux lettres, y compris les éléments supprimés, en mettant la boîte aux lettres entière d’un utilisateur en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="ed39f-114">**Litigation hold:** You can preserve all mailbox content including deleted items by putting a user's entire mailbox on litigation hold.</span></span> 
    
<span data-ttu-id="ed39f-115">Pour placer une boîte aux lettres en conservation pour litige, dans le centre d’administration :</span><span class="sxs-lookup"><span data-stu-id="ed39f-115">To place a mailbox on litigation hold, in the Admin center:</span></span>
    
1. <span data-ttu-id="ed39f-116">Dans le volet de **navigation de gauche, accédez à** \> utilisateurs **actifs**.</span><span class="sxs-lookup"><span data-stu-id="ed39f-116">In the left nav, go to **Users** \> **Active users**.</span></span>
    
2. <span data-ttu-id="ed39f-117">Sélectionnez un utilisateur dont vous souhaitez placer la boîte aux lettres en conservation pour litige et, dans le volet utilisateur, développez **paramètres de messagerie** , puis en regard de **paramètres supplémentaires** , choisissez **modifier les propriétés Exchange**.</span><span class="sxs-lookup"><span data-stu-id="ed39f-117">Select a user whose mailbox you want to place on litigation hold and in the user pane expand **Mail settings** and next to **More settings** choose **Edit Exchange properties**.</span></span>
    
3. <span data-ttu-id="ed39f-118">Sur la page boîte aux lettres de l’utilisateur, choisissez les fonctionnalités de boîte aux lettres \* \* dans le volet de navigation de gauche, puis cliquez sur le lien **activer** en **conservation pour litige**.</span><span class="sxs-lookup"><span data-stu-id="ed39f-118">On the mailbox page for the user, choose \*\* mailbox features \*\* on the left nav, and then choose the **Enable** link under **Litigation hold**.</span></span>
    
4. <span data-ttu-id="ed39f-119">Dans la boîte de dialogue **conservation pour litige** , vous pouvez spécifier la durée de la conservation pour litige dans le champ Durée de la **conservation pour litige** , laissez le champ vide si vous voulez placer un blocage infini.</span><span class="sxs-lookup"><span data-stu-id="ed39f-119">In the **litigation hold** dialog box you can specify the litigation hold duration in the **Litigation hold duration** field, leave field empty if you want to place an infinite hold.</span></span> <span data-ttu-id="ed39f-120">Vous pouvez également ajouter des notes et diriger le propriétaire de la boîte aux lettres vers un site Web vous devrez peut-être \> en savoir plus sur **la conservation pour**litige.</span><span class="sxs-lookup"><span data-stu-id="ed39f-120">You can also add notes and direct the mail box owner to a website you might have to explain more about the litigation hold \> **Save**.</span></span>
    
<span data-ttu-id="ed39f-121">**Rétention :** Vous pouvez activer des stratégies de rétention personnalisées, par exemple, pour conserver un certain temps ou supprimer définitivement le contenu à la fin de la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="ed39f-121">**Retention:** You can enable customized retention policies, for example, to preserve for a specific amount of time or delete content permanently at the end of the retention period.</span></span> <span data-ttu-id="ed39f-122">Pour en savoir plus, consultez la rubrique [vue d’ensemble des stratégies de rétention](https://support.office.com/article/5e377752-700d-4870-9b6d-12bfc12d2423).</span><span class="sxs-lookup"><span data-stu-id="ed39f-122">To learn more, see [Overview of retention policies](https://support.office.com/article/5e377752-700d-4870-9b6d-12bfc12d2423).</span></span>

## <a name="set-up-sensitivity-labels"></a><span data-ttu-id="ed39f-123">Configurer les étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="ed39f-123">Set up Sensitivity labels</span></span>

<span data-ttu-id="ed39f-124">Les étiquettes de confidentialité sont fournies avec Azure information protection (AIP) plan 1 et vous aident à classer et éventuellement protéger vos documents et e-mails en appliquant des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="ed39f-124">Sensitivity labels come with Azure Information Protection (AIP) Plan 1, and help you classify and optionally, protect your documents and emails, by applying labels.</span></span> <span data-ttu-id="ed39f-125">Les étiquettes peuvent être appliquées automatiquement par les administrateurs qui définissent des règles et des conditions, manuellement par les utilisateurs ou à l’aide d’une combinaison de recommandations pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ed39f-125">Labels can be applied automatically by administrators who define rules and conditions, manually by users, or by using a combination where users are given recommendations.</span></span>

<span data-ttu-id="ed39f-126">Pour configurer les étiquettes de confidentialité, affichez la vidéo [créer et gérer les étiquettes de confidentialité](https://support.office.com/en-us/article/2fb96b54-7dd2-4f0c-ac8d-170790d4b8b9) .</span><span class="sxs-lookup"><span data-stu-id="ed39f-126">To set up Sensitivity labels, view [create and manage sensitivity labels](https://support.office.com/en-us/article/2fb96b54-7dd2-4f0c-ac8d-170790d4b8b9) video.</span></span>



### <a name="install-the-azure-information-protection-client-manually"></a><span data-ttu-id="ed39f-127">Installation manuelle du client Azure information protection</span><span class="sxs-lookup"><span data-stu-id="ed39f-127">Install the Azure Information Protection client manually</span></span>

<span data-ttu-id="ed39f-128">Pour installer manuellement le client AIP :</span><span class="sxs-lookup"><span data-stu-id="ed39f-128">To manually install the AIP client:</span></span>

1. <span data-ttu-id="ed39f-129">Téléchargez **AzinfoProtection_UL. exe** à partir du [Centre de téléchargement Microsoft](https://www.microsoft.com/download/details.aspx?id=53018).</span><span class="sxs-lookup"><span data-stu-id="ed39f-129">Download **AzinfoProtection_UL.exe** from [Microsoft download center](https://www.microsoft.com/download/details.aspx?id=53018).</span></span>
 
2. <span data-ttu-id="ed39f-130">Vous pouvez vérifier que l’installation a fonctionné en affichant un document Word et en vous assurant que l’option de **confidentialité** est disponible sous l’onglet **Accueil** .</span><span class="sxs-lookup"><span data-stu-id="ed39f-130">You can verify that the installation worked by viewing a Word document and making sure that the **Sensitivity** option is available on the **Home** tab.</span></span>
<br/><span data-ttu-id="ed39f-131">![Onglet protection dans un document Word.](media/word-sensitivity.png)</span><span class="sxs-lookup"><span data-stu-id="ed39f-131">![Protection tab drop-down in a Word document.](media/word-sensitivity.png)</span></span>

<span data-ttu-id="ed39f-132">Pour plus d’informations, consultez [la rubrique installer le client](https://docs.microsoft.com/azure/information-protection/infoprotect-tutorial-step3).</span><span class="sxs-lookup"><span data-stu-id="ed39f-132">For more information see, [Install the client](https://docs.microsoft.com/azure/information-protection/infoprotect-tutorial-step3).</span></span>

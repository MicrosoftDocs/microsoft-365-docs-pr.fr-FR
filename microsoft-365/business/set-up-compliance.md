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
ms.custom:
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
description: Configurez Office 365 Advanced Threat Protection et protégez les données sensibles.
ms.openlocfilehash: 53741a7726222bb32329a401953be72257df95cc
ms.sourcegitcommit: 7ac06563c6ff034358e8fd3f9298fc426187ade2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668383"
---
# <a name="set-up-compliance-features"></a><span data-ttu-id="f32ee-103">Configurer les fonctionnalités de conformité</span><span class="sxs-lookup"><span data-stu-id="f32ee-103">Set up compliance features</span></span>

<span data-ttu-id="f32ee-104">Votre entreprise Microsoft 365 est dotée de fonctionnalités pour protéger vos données et périphériques, et vous aider à sécuriser les informations sensibles de vos clients et de vos clients.</span><span class="sxs-lookup"><span data-stu-id="f32ee-104">Your Microsoft 365 Business comes with features to protect your data and devices, and help you keep yours and your customers' sensitive information secure.</span></span>

## <a name="set-up-dlp-features"></a><span data-ttu-id="f32ee-105">Configurer les fonctionnalités DLP</span><span class="sxs-lookup"><span data-stu-id="f32ee-105">Set up DLP features</span></span>

<span data-ttu-id="f32ee-106">Voir [Create a DLP Policy from a template](https://support.office.com/article/59414438-99f5-488b-975c-5023f2254369) pour obtenir un exemple sur la façon de configurer une stratégie de protection contre les informations d’identification personnelle (PII).</span><span class="sxs-lookup"><span data-stu-id="f32ee-106">See [Create a DLP policy from a template](https://support.office.com/article/59414438-99f5-488b-975c-5023f2254369) for an example on how to set up a policy to protect against personally identifiable information (PII).</span></span> 
  
<span data-ttu-id="f32ee-107">DLP comprend de nombreux modèles de stratégie prêts à l’emploi pour de nombreux paramètres régionaux différents.</span><span class="sxs-lookup"><span data-stu-id="f32ee-107">DLP comes with many ready-to-use policy templates for many different locales.</span></span> <span data-ttu-id="f32ee-108">Par exemple, les données financières de l’Australie, le Canada Personal Information Act, les données financières américaines, etc. Consultez la rubrique relative aux [modèles de stratégie DLP](https://support.office.com/article/c2e588d3-8f4f-4937-a286-8c399f28953a) pour une liste complète.</span><span class="sxs-lookup"><span data-stu-id="f32ee-108">For example, Australia Financial Data, Canada Personal Information Act, U.S. Financial Data, etc. See [What the DLP policy templates include](https://support.office.com/article/c2e588d3-8f4f-4937-a286-8c399f28953a) for a full list.</span></span> <span data-ttu-id="f32ee-109">Tous ces modèles peuvent être activés de la même manière que l’exemple de modèle PII.</span><span class="sxs-lookup"><span data-stu-id="f32ee-109">All of these templates can be enabled similar to the PII template example.</span></span> 
  
## <a name="set-up-email-retention-with-exchange-online-archiving"></a><span data-ttu-id="f32ee-110">Configurer la rétention du courrier électronique avec archivage Exchange Online</span><span class="sxs-lookup"><span data-stu-id="f32ee-110">Set up email retention with Exchange Online Archiving</span></span>

 <span data-ttu-id="f32ee-111">Les fonctionnalités de licence d' **archivage Exchange Online** permettent de respecter les normes de conformité et de réglementation en conservant le contenu des courriers électroniques pour eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="f32ee-111">**Exchange Online Archiving** license features help maintain compliance and regulatory standards by preserving email content for eDiscovery.</span></span> <span data-ttu-id="f32ee-112">Elle contribue également à réduire les risques en cas de poursuite et permet de récupérer les données après une violation de la sécurité ou de récupérer des éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="f32ee-112">It also helps reduce your risk in the event of a lawsuit and provides a way to recover data after a security breach, or when you need to recover deleted items.</span></span> <span data-ttu-id="f32ee-113">Vous pouvez utiliser la conservation pour litige pour conserver tout le contenu d’un utilisateur ou utiliser des stratégies de rétention pour personnaliser ce que vous souhaitez conserver.</span><span class="sxs-lookup"><span data-stu-id="f32ee-113">You can use litigation hold to preserve all of a user's content, or use retention policies to customize what you want to preserve.</span></span>
  
<span data-ttu-id="f32ee-114">**Conservation pour litige:** Vous pouvez conserver tout le contenu des boîtes aux lettres, y compris les éléments supprimés, en mettant la boîte aux lettres entière d’un utilisateur en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="f32ee-114">**Litigation hold:** You can preserve all mailbox content including deleted items by putting a user's entire mailbox on litigation hold.</span></span> 
    
<span data-ttu-id="f32ee-115">Pour placer une boîte aux lettres en conservation pour litige, dans le centre d’administration:</span><span class="sxs-lookup"><span data-stu-id="f32ee-115">To place a mailbox on litigation hold, in the Admin center:</span></span>
    
1. <span data-ttu-id="f32ee-116">Dans le volet de navigation de gauche \*\*\*\* \> , accédez à utilisateurs **actifs**.</span><span class="sxs-lookup"><span data-stu-id="f32ee-116">In the left nav, go to **Users** \> **Active users**.</span></span>
    
2. <span data-ttu-id="f32ee-117">Sélectionnez un utilisateur dont vous souhaitez placer la boîte aux lettres en conservation pour litige et, dans le volet utilisateur, développez **paramètres de messagerie** , puis en regard de **paramètres supplémentaires** , choisissez **modifier les propriétés Exchange**.</span><span class="sxs-lookup"><span data-stu-id="f32ee-117">Select a user whose mailbox you want to place on litigation hold and in the user pane expand **Mail settings** and next to **More settings** choose **Edit Exchange properties**.</span></span>
    
3. <span data-ttu-id="f32ee-118">Sur la page boîte aux lettres de l’utilisateur, choisissez les fonctionnalités de boîte aux lettres \* \* dans le volet de navigation de gauche, puis cliquez sur le lien **activer** en **conservation pour litige**.</span><span class="sxs-lookup"><span data-stu-id="f32ee-118">On the mailbox page for the user, choose \*\* mailbox features \*\* on the left nav, and then choose the **Enable** link under **Litigation hold**.</span></span>
    
4. <span data-ttu-id="f32ee-119">Dans la boîte de dialogue **conservation pour litige** , vous pouvez spécifier la durée de la conservation pour litige dans le champ Durée de la **conservation pour litige** , laissez le champ vide si vous voulez placer un blocage infini.</span><span class="sxs-lookup"><span data-stu-id="f32ee-119">In the **litigation hold** dialog box you can specify the litigation hold duration in the **Litigation hold duration** field, leave field empty if you want to place an infinite hold.</span></span> <span data-ttu-id="f32ee-120">Vous pouvez également ajouter des notes et diriger le propriétaire de la boîte aux lettres vers un site Web vous devrez peut-être \> \*\*\*\* en savoir plus sur la conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="f32ee-120">You can also add notes and direct the mail box owner to a website you might have to explain more about the litigation hold \> **Save**.</span></span>
    
<span data-ttu-id="f32ee-121">**Rétention:** Vous pouvez activer des stratégies de rétention personnalisées, par exemple, pour conserver un certain temps ou supprimer définitivement le contenu à la fin de la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="f32ee-121">**Retention:** You can enable customized retention policies, for example, to preserve for a specific amount of time or delete content permanently at the end of the retention period.</span></span> <span data-ttu-id="f32ee-122">Pour en savoir plus, consultez la rubrique [vue d’ensemble des stratégies de](https://support.office.com/article/5e377752-700d-4870-9b6d-12bfc12d2423)rétention.</span><span class="sxs-lookup"><span data-stu-id="f32ee-122">To learn more, see [Overview of retention policies](https://support.office.com/article/5e377752-700d-4870-9b6d-12bfc12d2423).</span></span>

## <a name="set-up-azure-information-protection-features"></a><span data-ttu-id="f32ee-123">Configurer les fonctionnalités Azure information protection</span><span class="sxs-lookup"><span data-stu-id="f32ee-123">Set up Azure Information Protection features</span></span>

<span data-ttu-id="f32ee-124">Azure information protection (AIP) vous permet de classer et, si vous le souhaitez, de protéger vos documents et vos courriers électroniques, en appliquant des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="f32ee-124">Azure Information Protection (AIP) helps you classify and optionally, protect your documents and emails, by applying labels.</span></span> <span data-ttu-id="f32ee-125">Les étiquettes peuvent être appliquées automatiquement par les administrateurs qui définissent des règles et des conditions, manuellement par les utilisateurs ou à l’aide d’une combinaison de recommandations pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f32ee-125">Labels can be applied automatically by administrators who define rules and conditions, manually by users, or by using a combination where users are given recommendations.</span></span>

<span data-ttu-id="f32ee-126">Dans Outlook sur le Web, vous pouvez appliquer les étiquettes et restrictions prédéfinies suivantes à vos courriers électroniques:</span><span class="sxs-lookup"><span data-stu-id="f32ee-126">In Outlook on the web you can apply the following built-in labels and restrictions to your emails:</span></span>
  
- <span data-ttu-id="f32ee-127">**Ne pas transférer**: les destinataires peuvent lire le message, mais ils ne peuvent pas transférer, imprimer ou copier du contenu</span><span class="sxs-lookup"><span data-stu-id="f32ee-127">**Do Not Forward**: Recipients can read the message, but they can't forward, print, or copy content</span></span>
    
- <span data-ttu-id="f32ee-128">**Encrypt**: l’intégralité du message est chiffrée.</span><span class="sxs-lookup"><span data-stu-id="f32ee-128">**Encrypt**: The entire message is encrypted.</span></span> <span data-ttu-id="f32ee-129">Les destinataires doivent confirmer leur identité avant d’accéder au contenu chiffré et ne peuvent pas supprimer le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="f32ee-129">Recipients must confirm their identity before accessing encrypted content and can't remove encryption.</span></span>
    
- <span data-ttu-id="f32ee-130">**Confidential**: donne aux employés de votre organisation des autorisations complètes sur le contenu et les pièces jointes de messagerie, mais pas sur les personnes externes à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f32ee-130">**Confidential**: Gives the employees in your organization full permissions to the email content and attachments, but not to people outside your organization.</span></span> <span data-ttu-id="f32ee-131">Les propriétaires de données peuvent suivre et révoquer du contenu à tout moment.</span><span class="sxs-lookup"><span data-stu-id="f32ee-131">Data owners can track and revoke content at any point.</span></span>
    
- <span data-ttu-id="f32ee-132">**Hautement confidentiel**: cette restriction peut être appliquée aux données hautement confidentielles, ce qui permet aux employés d’afficher, de modifier et de répondre, mais pas de transférer, d’imprimer ou de copier les données.</span><span class="sxs-lookup"><span data-stu-id="f32ee-132">**Highly Confidential**: This restriction can be applied to highly confidential data, allowing employees to view, edit, and reply, but not forward, print, or copy the data.</span></span> <span data-ttu-id="f32ee-133">Les propriétaires de données peuvent suivre et révoquer du contenu à tout moment.</span><span class="sxs-lookup"><span data-stu-id="f32ee-133">Data owners can track and revoke content at any point.</span></span>

### <a name="make-sure-azure-information-protection-is-activated"></a><span data-ttu-id="f32ee-134">Vérifier que Azure information protection est activé</span><span class="sxs-lookup"><span data-stu-id="f32ee-134">Make sure Azure Information Protection is activated</span></span>

<span data-ttu-id="f32ee-135">Pour vérifier qu’AIP est activé:</span><span class="sxs-lookup"><span data-stu-id="f32ee-135">To verify that AIP is activated :</span></span>

1. <span data-ttu-id="f32ee-136">Connectez-vous à [Azure Portal](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="f32ee-136">Sign into [Azure portal](https://portal.azure.com/).</span></span>

2. <span data-ttu-id="f32ee-137">Sélectionnez **tous les services** et tapez *Azure information protection* dans la **zone de recherche**.</span><span class="sxs-lookup"><span data-stu-id="f32ee-137">Select **All services** and type in *Azure Information Protection* in the **Search Box**.</span></span>

3. <span data-ttu-id="f32ee-138">Une fois que les résultats s’affichent, cliquez sur le bouton Démarrer en regard d' **Azure information protection** pour en faire un favori et le retrouver facilement plus tard.</span><span class="sxs-lookup"><span data-stu-id="f32ee-138">Once the results display, click the start next to **Azure Information Protection** to make it a favorite and easy to find later.</span></span>

4. <span data-ttu-id="f32ee-139">Sélectionnez **activation de protection** **Azure information protection** \> et assurez-vous que l’État est défini sur activé.</span><span class="sxs-lookup"><span data-stu-id="f32ee-139">Select **Azure Information Protection** \> **Protection activation** and make sure the status is set to activated.</span></span> 

### <a name="view-the-azure-information-protection-policy-and-default-labels"></a><span data-ttu-id="f32ee-140">Afficher la stratégie Azure information protection et les étiquettes par défaut</span><span class="sxs-lookup"><span data-stu-id="f32ee-140">View the Azure Information Protection policy and default labels</span></span> 

<span data-ttu-id="f32ee-141">Pour afficher et modifier les étiquettes existantes:</span><span class="sxs-lookup"><span data-stu-id="f32ee-141">To view, and modify, the existing labels:</span></span>

1. <span data-ttu-id="f32ee-142">Dans le tableau de bord Azure information protection \*\*\*\* \> , sélectionnez **étiquettes**classifications.</span><span class="sxs-lookup"><span data-stu-id="f32ee-142">On the Azure Information Protection dashboard, select **Classifications** \> **Labels**.</span></span> <br/><span data-ttu-id="f32ee-143">![Étiquettes standard pour Azure information protection.](media/AIPLabels.png)</span><span class="sxs-lookup"><span data-stu-id="f32ee-143">![Standard labels for Azure Information Protection.](media/AIPLabels.png)</span></span>

2. <span data-ttu-id="f32ee-144">Vous pouvez choisir n’importe quelle étiquette pour afficher les options, vous pouvez modifier le nom d’affichage, les couleurs, etc.</span><span class="sxs-lookup"><span data-stu-id="f32ee-144">You can choose any label to view options, you can change the display name, colors, etc.</span></span>
 
3. <span data-ttu-id="f32ee-145">Pour créer les vôtres, consultez la rubrique [Modify and Create New labels](https://docs.microsoft.com/azure/information-protection/infoprotect-tutorial-step2) .</span><span class="sxs-lookup"><span data-stu-id="f32ee-145">See  [Modify and create new labels](https://docs.microsoft.com/azure/information-protection/infoprotect-tutorial-step2) if you want to create your own.</span></span> 

### <a name="install-the-azure-information-protection-client-manually"></a><span data-ttu-id="f32ee-146">Installation manuelle du client Azure information protection</span><span class="sxs-lookup"><span data-stu-id="f32ee-146">Install the Azure Information Protection client manually</span></span>

<span data-ttu-id="f32ee-147">Pour installer manuellement le client AIP:</span><span class="sxs-lookup"><span data-stu-id="f32ee-147">To manually install the AIP client:</span></span>

1. <span data-ttu-id="f32ee-148">Téléchargez **AzInfoProtection. exe** à partir du [Centre de téléchargement Microsoft](https://www.microsoft.com/download/details.aspx?id=53018).</span><span class="sxs-lookup"><span data-stu-id="f32ee-148">Download **AzInfoProtection.exe** from [Microsoft download center](https://www.microsoft.com/download/details.aspx?id=53018).</span></span>
 
2. <span data-ttu-id="f32ee-149">Vous pouvez vérifier que l’installation a fonctionné en affichant un document Word et en vous assurant que l’option **protéger** est disponible sous l’onglet **Accueil** .</span><span class="sxs-lookup"><span data-stu-id="f32ee-149">You can verify that the installation worked by viewing a Word document and making sure that the **Protect** option is available on the **Home** tab.</span></span> <br/><span data-ttu-id="f32ee-150">![Onglet protection dans un document Word.](media/Word_Protect.png)</span><span class="sxs-lookup"><span data-stu-id="f32ee-150">![Protection tab drop-down in a Word document.](media/Word_Protect.png)</span></span>

<span data-ttu-id="f32ee-151">Pour plus d’informations, consultez [la rubrique installer le client](https://docs.microsoft.com/azure/information-protection/infoprotect-tutorial-step3).</span><span class="sxs-lookup"><span data-stu-id="f32ee-151">For more information see, [Install the client](https://docs.microsoft.com/azure/information-protection/infoprotect-tutorial-step3).</span></span>

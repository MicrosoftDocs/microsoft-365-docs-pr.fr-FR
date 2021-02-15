---
title: Classification des données pour votre environnement de test Microsoft 365 pour entreprise
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/10/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-security-compliance
ms.custom: Ent_TLGs
ms.assetid: 1aa9639b-2862-49c4-bc33-1586dda636b8
description: Utilisez ce guide de laboratoire de test pour créer et utiliser des étiquettes de rétention sur des documents dans votre environnement de test Microsoft 365 pour entreprise.
ms.openlocfilehash: 5cc77167db866d99f0beea5f554a777ecf355046
ms.sourcegitcommit: 53ff1fe6d6143b0bf011031eea9b85dc01ae4f74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "48487731"
---
# <a name="data-classification-for-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="948ed-103">Classification des données pour votre environnement de test Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="948ed-103">Data classification for your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="948ed-104">*Ce guide de laboratoire de test peut être utilisé pour les environnements de test Microsoft 365 pour les entreprises et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="948ed-104">*This Test Lab Guide can be used for both Microsoft 365 for enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="948ed-105">Cet article explique comment configurer la classification des données à l’aide d’étiquettes de rétention dans votre environnement de test Microsoft 365 pour entreprise.</span><span class="sxs-lookup"><span data-stu-id="948ed-105">This article describes how to configure data classification using retention labels in your Microsoft 365 for enterprise test environment.</span></span>

<span data-ttu-id="948ed-106">La classification des données dans votre environnement de test implique trois phases :</span><span class="sxs-lookup"><span data-stu-id="948ed-106">Classifying data in your test environment involves three phases:</span></span>
- [<span data-ttu-id="948ed-107">Phase 1 : Créer votre environnement de test Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="948ed-107">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>](#phase-1-build-out-your-microsoft-365-for-enterprise-test-environment)
- [<span data-ttu-id="948ed-108">Phase 2 : Création d’étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="948ed-108">Phase 2: Create retention labels</span></span>](#phase-2-create-retention-labels)
- [<span data-ttu-id="948ed-109">Phase 3 : Appliquer des étiquettes de rétention aux documents</span><span class="sxs-lookup"><span data-stu-id="948ed-109">Phase 3: Apply retention labels to documents</span></span>](#phase-3-apply-retention-labels-to-documents)

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="948ed-111">Pour obtenir un plan visuel de tous les articles de la pile du Guide de laboratoire de test Microsoft 365 pour entreprise, allez à [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="948ed-111">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="948ed-112">Phase 1 : Créer votre environnement de test Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="948ed-112">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="948ed-113">Si vous souhaitez simplement configurer les étiquettes de rétention de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère.](lightweight-base-configuration-microsoft-365-enterprise.md)</span><span class="sxs-lookup"><span data-stu-id="948ed-113">If you just want to configure retention labels in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="948ed-114">Si vous souhaitez configurer des étiquettes de rétention dans une entreprise simulée, suivez les instructions de [l’authentification directe.](pass-through-auth-m365-ent-test-environment.md)</span><span class="sxs-lookup"><span data-stu-id="948ed-114">If you want to configure retention labels in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="948ed-115">Le test des étiquettes de rétention ne nécessite pas l’environnement de test d’entreprise simulée, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="948ed-115">Testing retention labels doesn't require the simulated enterprise test environment, which includes a simulated intranet connected to the internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="948ed-116">Il est fourni ici en tant qu’option afin que vous pouvez tester la gestion automatisée des licences et l’appartenance à un groupe et l’expérimenter dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="948ed-116">It's provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span>

## <a name="phase-2-create-retention-labels"></a><span data-ttu-id="948ed-117">Phase 2 : Création d’étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="948ed-117">Phase 2: Create retention labels</span></span>

<span data-ttu-id="948ed-118">Dans cette phase, créez les étiquettes de rétention pour les différents niveaux de rétention pour les dossiers de documents SharePoint Online :</span><span class="sxs-lookup"><span data-stu-id="948ed-118">In this phase, create the retention labels for the different levels of retention for SharePoint Online documents folders:</span></span>

1. <span data-ttu-id="948ed-119">Connectez-vous au Centre de sécurité [Microsoft 365](https://security.microsoft.com/homepage) avec votre compte d’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="948ed-119">Sign in to the [Microsoft 365 security center](https://security.microsoft.com/homepage) with your global admin account.</span></span>
1. <span data-ttu-id="948ed-120">Dans **l’onglet Accueil - Sécurité Microsoft 365** de votre navigateur, sélectionnez   >  **Étiquettes de rétention de classification.**</span><span class="sxs-lookup"><span data-stu-id="948ed-120">From the **Home - Microsoft 365 security** tab of your browser, select **Classification** > **Retention labels**.</span></span>
1. <span data-ttu-id="948ed-121">Sélectionnez **Créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="948ed-121">Select **Create a label**.</span></span>
1. <span data-ttu-id="948ed-122">Dans le **volet Nom de votre étiquette,** entrez Public **interne** dans Nom de votre **étiquette,** puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="948ed-122">In the **Name your label** pane, enter **Internal Public** in **Name your label**, and then select **Next**.</span></span>
1. <span data-ttu-id="948ed-123">Dans le **volet Descripteurs du plan de fichiers,** sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="948ed-123">In the **File plan descriptors** pane, select **Next**.</span></span>
1. <span data-ttu-id="948ed-124">Dans le **volet Paramètres de l’étiquette,** si nécessaire, définissez rétention **sur Sur,** puis sélectionnez **Suivant**. </span><span class="sxs-lookup"><span data-stu-id="948ed-124">In the **Label settings** pane, if needed, set **Retention** to **On**, and then select **Next**.</span></span>
1. <span data-ttu-id="948ed-125">Dans le **volet Examiner vos paramètres,** **sélectionnez Créer l’étiquette.**</span><span class="sxs-lookup"><span data-stu-id="948ed-125">In the **Review your settings** pane, select **Create the label**.</span></span>
1. <span data-ttu-id="948ed-126">Répétez les étapes 3 à 7 pour les étiquettes supplémentaires avec ces noms :</span><span class="sxs-lookup"><span data-stu-id="948ed-126">Repeat steps 3-7 for additional labels with these names:</span></span>
  - <span data-ttu-id="948ed-127">Private</span><span class="sxs-lookup"><span data-stu-id="948ed-127">Private</span></span>
  - <span data-ttu-id="948ed-128">Sensible</span><span class="sxs-lookup"><span data-stu-id="948ed-128">Sensitive</span></span>
  - <span data-ttu-id="948ed-129">Hautement confidentiel</span><span class="sxs-lookup"><span data-stu-id="948ed-129">Highly Confidential</span></span>
1. <span data-ttu-id="948ed-130">Dans le volet **Étiquettes de** rétention, **sélectionnez Publier des étiquettes.**</span><span class="sxs-lookup"><span data-stu-id="948ed-130">In the **Retention labels** pane, select **Publish labels**.</span></span>
1. <span data-ttu-id="948ed-131">Dans le **volet Choisir les étiquettes à** publier, sélectionnez Choisir les **étiquettes à publier.**</span><span class="sxs-lookup"><span data-stu-id="948ed-131">In the **Choose labels to publish** pane, select **Choose labels to publish**.</span></span>
1. <span data-ttu-id="948ed-132">Dans le volet Choisir **des étiquettes,** **sélectionnez Ajouter** et sélectionnez les quatre étiquettes.</span><span class="sxs-lookup"><span data-stu-id="948ed-132">In the **Choose labels** pane, select **Add** and select all four labels.</span></span>
1. <span data-ttu-id="948ed-133">**Sélectionnez** Ajouter, puis **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="948ed-133">Select **Add**, and then select **Done**.</span></span>
1. <span data-ttu-id="948ed-134">Dans le **volet Choisir les étiquettes à** publier, sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="948ed-134">On the **Choose labels to publish** pane, select **Next**.</span></span>
1. <span data-ttu-id="948ed-135">Dans le **volet Choisir des** emplacements, sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="948ed-135">On the **Choose locations** pane, select **Next**.</span></span>
1. <span data-ttu-id="948ed-136">Dans le **volet Nom de votre** stratégie, entrez Exemple **d’organisation** dans **Nom,** puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="948ed-136">On the **Name your policy** pane, enter **Example organization** in **Name**, and then select **Next**.</span></span>
1. <span data-ttu-id="948ed-137">Dans le **volet Examiner vos paramètres,** sélectionnez **Publier des étiquettes.**</span><span class="sxs-lookup"><span data-stu-id="948ed-137">On the **Review your settings** pane, select **Publish labels**.</span></span>
 
<span data-ttu-id="948ed-138">La publication des étiquettes de rétention peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="948ed-138">It might take a few minutes for the retention labels to be published.</span></span>

## <a name="phase-3-apply-retention-labels-to-documents"></a><span data-ttu-id="948ed-139">Phase 3 : Appliquer des étiquettes de rétention aux documents</span><span class="sxs-lookup"><span data-stu-id="948ed-139">Phase 3: Apply retention labels to documents</span></span>

<span data-ttu-id="948ed-140">Dans cette phase, vous découvrez le comportement par défaut des étiquettes de rétention pour les fichiers dans le dossier Documents d’un site SharePoint Online et modifiez manuellement l’étiquette de rétention d’un document.</span><span class="sxs-lookup"><span data-stu-id="948ed-140">In this phase, you discover the default retention label behavior for files in the Documents folder of a SharePoint Online site and manually change the retention label of a document.</span></span>

<span data-ttu-id="948ed-141">Tout d’abord, créez un site d’équipe SharePoint Online de niveau sensible :</span><span class="sxs-lookup"><span data-stu-id="948ed-141">First, create a sensitive-level SharePoint Online team site:</span></span>
  
1. <span data-ttu-id="948ed-142">À l’aide d’une instance privée de votre navigateur, connectez-vous au Centre d’administration [Microsoft 365](https://admin.microsoft.com) à l’aide de votre compte d’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="948ed-142">Using a private instance of your browser, sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) using your global admin account.</span></span>
1. <span data-ttu-id="948ed-143">Dans la liste des vignettes, **sélectionnez SharePoint.**</span><span class="sxs-lookup"><span data-stu-id="948ed-143">In the list of tiles, select **SharePoint**.</span></span>
1. <span data-ttu-id="948ed-144">Sous le nouvel **onglet SharePoint** de votre navigateur, sélectionnez **Créer un site.**</span><span class="sxs-lookup"><span data-stu-id="948ed-144">On the new **SharePoint** tab in your browser, select **Create site**.</span></span>
1. <span data-ttu-id="948ed-145">Sur la page **Créer un site**, sélectionnez **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="948ed-145">On the **Create a site** page, select **Team site**.</span></span>
1. <span data-ttu-id="948ed-146">Dans la **zone Nom du site d’équipe,** entrez **SensitiveFiles**.</span><span class="sxs-lookup"><span data-stu-id="948ed-146">In the **Team site name** box, enter **SensitiveFiles**.</span></span>
1. <span data-ttu-id="948ed-147">Dans la **zone de description du site** d’équipe, entrez le site **SharePoint pour les fichiers sensibles.**</span><span class="sxs-lookup"><span data-stu-id="948ed-147">In the **Team site description** box, enter **SharePoint site for sensitive files**.</span></span>
1. <span data-ttu-id="948ed-148">Dans **les paramètres de confidentialité,** **sélectionnez Privé - seuls** les membres peuvent accéder à ce site, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="948ed-148">In **Privacy settings**, select **Private - only members can access this site**, and then select **Next**.</span></span>
1. <span data-ttu-id="948ed-149">Dans le **volet Qui voulez-vous ajouter ?** sélectionnez **Terminer.**</span><span class="sxs-lookup"><span data-stu-id="948ed-149">In the **Who do you want to add?** pane, select **Finish**.</span></span>
    
<span data-ttu-id="948ed-150">Ensuite, configurez le dossier Documents du site d’équipe SensitiveFiles pour l’étiquette de rétention Sensible.</span><span class="sxs-lookup"><span data-stu-id="948ed-150">Next, configure the Documents folder of the SensitiveFiles team site for the Sensitive retention label.</span></span>
  
1. <span data-ttu-id="948ed-151">Dans **l’onglet SensitiveFiles** de votre navigateur, sélectionnez **Documents**.</span><span class="sxs-lookup"><span data-stu-id="948ed-151">In the **SensitiveFiles** tab of your browser, select **Documents**.</span></span>
1. <span data-ttu-id="948ed-152">Sélectionnez **l’icône Paramètres,** puis sélectionnez **Paramètres de la bibliothèque.**</span><span class="sxs-lookup"><span data-stu-id="948ed-152">Select the **Settings** icon, and then select **Library settings**.</span></span>
1. <span data-ttu-id="948ed-153">Sous **Autorisations et gestion,** **sélectionnez Appliquer une étiquette aux éléments de cette liste ou bibliothèque.**</span><span class="sxs-lookup"><span data-stu-id="948ed-153">Under **Permissions and Management**, select **Apply label to items in this list or library**.</span></span> <span data-ttu-id="948ed-154">Si cette option n’apparaît pas, vos étiquettes de rétention ne sont pas encore publiées.</span><span class="sxs-lookup"><span data-stu-id="948ed-154">If this option doesn't appear, your retention labels aren't yet published.</span></span> <span data-ttu-id="948ed-155">Essayez cette étape ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="948ed-155">Try this step at a later time.</span></span>
1. <span data-ttu-id="948ed-156">Dans **Paramètres - Appliquer l’étiquette,** **sélectionnez Sensible** dans la zone de mise en question, puis **sélectionnez Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="948ed-156">In **Settings-Apply Label**, select **Sensitive** in the drop-down box, and then select **Save**.</span></span>

<span data-ttu-id="948ed-157">Ensuite, créez un document dans le site SensitiveFiles et modifiez son étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="948ed-157">Next, create a new document in the SensitiveFiles site and change its retention label.</span></span>
    
1. <span data-ttu-id="948ed-158">Dans le dossier documents, sélectionnez **Nouveau**  >  **document Word.**</span><span class="sxs-lookup"><span data-stu-id="948ed-158">In the documents folder, select **New** > **Word document**.</span></span>
1. <span data-ttu-id="948ed-159">Entrez du texte dans le document vide.</span><span class="sxs-lookup"><span data-stu-id="948ed-159">Enter some text in the blank document.</span></span> <span data-ttu-id="948ed-160">Attendez que le texte soit enregistré.</span><span class="sxs-lookup"><span data-stu-id="948ed-160">Wait for the text to be saved.</span></span>
1. <span data-ttu-id="948ed-161">Dans la barre de menus, sélectionnez **Documents partagés.**</span><span class="sxs-lookup"><span data-stu-id="948ed-161">On the menu bar, select **Shared Documents**.</span></span>
1. <span data-ttu-id="948ed-162">EnDocument.docxnom **de** fichier, sélectionnez les sélections verticales, puis sélectionnez **Détails.**</span><span class="sxs-lookup"><span data-stu-id="948ed-162">Next to the **Document.docx** file name, select the vertical ellipsis, and then select **Details**.</span></span>
1. <span data-ttu-id="948ed-163">Dans le volet droit, dans la section **Propriétés,** sous Appliquer  l’étiquette de **rétention,** notez que l’étiquette de rétention Sensible a été automatiquement appliquée au document.</span><span class="sxs-lookup"><span data-stu-id="948ed-163">In the right pane, in the **Properties** section, under **Apply retention label**, note that the document has had the **Sensitive** retention label automatically applied.</span></span>
1. <span data-ttu-id="948ed-164">Cliquez sur **Modifier tout**.</span><span class="sxs-lookup"><span data-stu-id="948ed-164">Click **Edit all**.</span></span>
1. <span data-ttu-id="948ed-165">Dans le **Document.docx,** sous Appliquer l’étiquette de **rétention,** sélectionnez l’étiquette **Hautement** confidentiel, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="948ed-165">In the **Document.docx** pane, under **Apply retention label**, select the **Highly Confidential** label, and then select **Save**.</span></span>

## <a name="next-step"></a><span data-ttu-id="948ed-166">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="948ed-166">Next step</span></span>

<span data-ttu-id="948ed-167">Explorez [d’autres fonctionnalités de protection](m365-enterprise-test-lab-guides.md#information-protection) des informations dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="948ed-167">Explore additional [information protection](m365-enterprise-test-lab-guides.md#information-protection) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="948ed-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="948ed-168">See also</span></span>

[<span data-ttu-id="948ed-169">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="948ed-169">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="948ed-170">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="948ed-170">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="948ed-171">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="948ed-171">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)

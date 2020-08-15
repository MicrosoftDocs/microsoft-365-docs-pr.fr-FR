---
title: Classification des données pour votre environnement de test Microsoft 365 pour les entreprises
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
description: Utilisez ce guide de laboratoire de test pour créer et utiliser des étiquettes de rétention sur des documents dans votre environnement de test Microsoft 365 pour les entreprises.
ms.openlocfilehash: 171fcb74b09a1f2e5c80f23e010640dce55660bc
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46686405"
---
# <a name="data-classification-for-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="4388e-103">Classification des données pour votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="4388e-103">Data classification for your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="4388e-104">*Ce guide de laboratoire de test peut être utilisé pour les environnements de test Microsoft 365 pour les environnements de test d’entreprise et Office 365.*</span><span class="sxs-lookup"><span data-stu-id="4388e-104">*This Test Lab Guide can be used for both Microsoft 365 for enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="4388e-105">Avec les instructions de cet article, vous configurez la classification des données à l’aide d’étiquettes de rétention dans votre environnement de test Microsoft 365 pour entreprise.</span><span class="sxs-lookup"><span data-stu-id="4388e-105">With the instructions in this article, you configure data classification using retention labels in your Microsoft 365 for enterprise test environment.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="4388e-107">Cliquez [ici](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan visuel de tous les articles de l’ensemble des guides de laboratoire de test de Microsoft 365 pour entreprise.</span><span class="sxs-lookup"><span data-stu-id="4388e-107">Click [here](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="4388e-108">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="4388e-108">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="4388e-109">Si vous souhaitez simplement configurer des étiquettes de rétention de manière simple avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="4388e-109">If you just want to configure retention labels in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="4388e-110">Si vous souhaitez configurer des étiquettes de rétention dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="4388e-110">If you want to configure retention labels in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="4388e-111">Le test des étiquettes de rétention ne nécessite pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="4388e-111">Testing retention labels does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="4388e-112">Elle est fournie ici en tant qu’option pour vous permettre de tester les licences automatiques et les appartenances aux groupes et de les tester dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="4388e-112">It is provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span> 

## <a name="phase-2-create-retention-labels"></a><span data-ttu-id="4388e-113">Phase 2 : créer des étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="4388e-113">Phase 2: Create retention labels</span></span>

<span data-ttu-id="4388e-114">Dans cette phase, vous allez créer les étiquettes de rétention pour les différents niveaux de rétention pour les dossiers de documents SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="4388e-114">In this phase, you create the retention labels for the different levels of retention for SharePoint Online documents folders.</span></span>

1. <span data-ttu-id="4388e-115">Connectez-vous au [Centre de sécurité Microsoft 365](https://security.microsoft.com/homepage) avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="4388e-115">Sign in to the [Microsoft 365 security center](https://security.microsoft.com/homepage) with your global admin account.</span></span>
    
2. <span data-ttu-id="4388e-116">À partir de l’onglet **Accueil-Microsoft 365 sécurité** de votre navigateur, cliquez sur **classification > étiquettes de rétention**.</span><span class="sxs-lookup"><span data-stu-id="4388e-116">From the **Home - Microsoft 365 security** tab of your browser, click **Classification > Retention labels**.</span></span>
    
3. <span data-ttu-id="4388e-117">Cliquez sur **Créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="4388e-117">Click **Create a label**.</span></span>
    
4. <span data-ttu-id="4388e-118">Dans le volet **nom de l’étiquette** , tapez **public interne** dans **nom de votre étiquette**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="4388e-118">In the **Name your label** pane, type **Internal Public** in **Name your label**, and then click **Next**.</span></span>

5. <span data-ttu-id="4388e-119">Dans le volet **fichiers de descripteurs de plan de fichiers** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="4388e-119">In the **File plan descriptors** pane, click **Next**.</span></span>
    
6. <span data-ttu-id="4388e-120">Dans le volet **paramètres d’étiquette** , si nécessaire, définissez **rétention** **sur activé**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="4388e-120">In the **Label settings** pane, if needed, set **Retention** to **On**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="4388e-121">Dans le volet **vérifier vos paramètres** , cliquez sur **créer l’étiquette**.</span><span class="sxs-lookup"><span data-stu-id="4388e-121">In the **Review your settings** pane, click **Create the label**.</span></span>
    
8. <span data-ttu-id="4388e-122">Répétez les étapes 3 à 7 pour les étiquettes supplémentaires avec ces noms :</span><span class="sxs-lookup"><span data-stu-id="4388e-122">Repeat steps 3-7 for additional labels with these names:</span></span>
    
  - <span data-ttu-id="4388e-123">Private</span><span class="sxs-lookup"><span data-stu-id="4388e-123">Private</span></span>
    
  - <span data-ttu-id="4388e-124">Sensible</span><span class="sxs-lookup"><span data-stu-id="4388e-124">Sensitive</span></span>
    
  - <span data-ttu-id="4388e-125">Hautement confidentiel</span><span class="sxs-lookup"><span data-stu-id="4388e-125">Highly Confidential</span></span>
  
9. <span data-ttu-id="4388e-126">Dans le volet **étiquettes de rétention** , cliquez sur **publier les étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="4388e-126">In the **Retention labels** pane, click **Publish labels**.</span></span>
    
10. <span data-ttu-id="4388e-127">Dans le volet **choisir les étiquettes à publier** , cliquez sur **choisir les étiquettes à publier**.</span><span class="sxs-lookup"><span data-stu-id="4388e-127">In the **Choose labels to publish** pane, click **Choose labels to publish**.</span></span>
    
11. <span data-ttu-id="4388e-128">Dans le volet **choisir des étiquettes** , cliquez sur **Ajouter** et sélectionnez les quatre étiquettes.</span><span class="sxs-lookup"><span data-stu-id="4388e-128">In the **Choose labels** pane, click **Add** and select all four labels.</span></span>
    
12. <span data-ttu-id="4388e-129">Cliquez sur **Ajouter**, puis sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="4388e-129">Click **Add**, and then click **Done**.</span></span>
    
13. <span data-ttu-id="4388e-130">Dans le volet **Choisir les étiquettes à publier**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4388e-130">On the **Choose labels to publish** pane, click **Next**.</span></span>
    
14. <span data-ttu-id="4388e-131">Dans le volet **Choisir les emplacements**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4388e-131">On the **Choose locations** pane, click **Next**.</span></span>
    
15. <span data-ttu-id="4388e-132">Dans le volet **Nom de votre stratégie**, saisissez **Exemple d’organisation** sous **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4388e-132">On the **Name your policy** pane, type **Example organization** in **Name**, and then click **Next**.</span></span>
    
16. <span data-ttu-id="4388e-133">Dans le volet **vérifier vos paramètres** , cliquez sur **publier les étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="4388e-133">On the **Review your settings** pane, click **Publish labels**.</span></span>
 
<span data-ttu-id="4388e-134">Notez que la publication des étiquettes de rétention peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="4388e-134">Note that it might take a few minutes for the retention labels to be published.</span></span>

## <a name="phase-3-apply-retention-labels-to-documents"></a><span data-ttu-id="4388e-135">Phase 3 : appliquer des étiquettes de rétention aux documents</span><span class="sxs-lookup"><span data-stu-id="4388e-135">Phase 3: Apply retention labels to documents</span></span>

<span data-ttu-id="4388e-136">Dans cette phase, vous découvrez le comportement par défaut de l’étiquette de rétention pour les fichiers du dossier Documents d’un site SharePoint Online et vous modifiez manuellement l’étiquette de rétention d’un document.</span><span class="sxs-lookup"><span data-stu-id="4388e-136">In this phase, you discover the default retention label behavior for files in the Documents folder of a SharePoint Online site and manually change the retention label of a document.</span></span>

<span data-ttu-id="4388e-137">Tout d’abord, créez un site d’équipe SharePoint Online de niveau sensible :</span><span class="sxs-lookup"><span data-stu-id="4388e-137">First, create a sensitive-level SharePoint Online team site:</span></span>
  
1. <span data-ttu-id="4388e-138">À l’aide d’une instance privée de votre navigateur, connectez-vous au [Centre d’administration 365 de Microsoft](https://admin.microsoft.com) à l’aide de votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="4388e-138">Using a private instance of your browser, sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) using your global admin account.</span></span>
    
2. <span data-ttu-id="4388e-139">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="4388e-139">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="4388e-140">Dans le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **créer un site**.</span><span class="sxs-lookup"><span data-stu-id="4388e-140">On the new **SharePoint** tab in your browser, click **Create site**.</span></span>
    
4. <span data-ttu-id="4388e-141">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="4388e-141">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="4388e-142">Dans **nom du site d’équipe**, tapez **SensitiveFiles**.</span><span class="sxs-lookup"><span data-stu-id="4388e-142">In **Team site name**, type **SensitiveFiles**.</span></span>
    
6. <span data-ttu-id="4388e-143">Dans **Description du site d’équipe**, tapez **site SharePoint pour les fichiers sensibles**.</span><span class="sxs-lookup"><span data-stu-id="4388e-143">In **Team site description**, type **SharePoint site for sensitive files**.</span></span>
    
7.  <span data-ttu-id="4388e-144">Dans **Paramètres de confidentialité**, sélectionnez **Privé - Seuls les membres peuvent accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4388e-144">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="4388e-145">Dans le volet **qui voulez-vous ajouter ?** , cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="4388e-145">In the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="4388e-146">Ensuite, configurez le dossier des documents du site d’équipe SensitiveFiles pour l’étiquette de rétention sensible.</span><span class="sxs-lookup"><span data-stu-id="4388e-146">Next, configure the Documents folder of the SensitiveFiles team site for the Sensitive retention label.</span></span>
  
1. <span data-ttu-id="4388e-147">Dans l’onglet **SensitiveFiles** de votre navigateur, cliquez sur **documents**.</span><span class="sxs-lookup"><span data-stu-id="4388e-147">In the **SensitiveFiles** tab of your browser, click **Documents**.</span></span>
    
2. <span data-ttu-id="4388e-148">Cliquez sur l’icône des paramètres, puis cliquez sur **Paramètres de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="4388e-148">Click the settings icon, and then click **Library settings**.</span></span>
    
3. <span data-ttu-id="4388e-149">Sous **autorisations et gestion**, cliquez sur **appliquer une étiquette aux éléments de cette liste ou bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="4388e-149">Under **Permissions and Management**, click **Apply label to items in this list or library**.</span></span> <span data-ttu-id="4388e-150">Si cette option ne s’affiche pas, vos étiquettes de rétention ne sont pas encore publiées.</span><span class="sxs-lookup"><span data-stu-id="4388e-150">If this option does not appear, your retention labels are not yet published.</span></span> <span data-ttu-id="4388e-151">Essayez cette étape ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="4388e-151">Try this step at a later time.</span></span>
    
4. <span data-ttu-id="4388e-152">Dans **paramètres-appliquer l’étiquette**, sélectionnez **sensible** dans la zone de liste déroulante, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4388e-152">In **Settings-Apply Label**, select **Sensitive** in the drop-down box, and then click **Save**.</span></span>

<span data-ttu-id="4388e-153">Ensuite, créez un nouveau document dans le site SensitiveFiles et modifiez son étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="4388e-153">Next, create a new document in the SensitiveFiles site and change its retention label.</span></span>
    
1. <span data-ttu-id="4388e-154">Dans le dossier documents, cliquez sur **nouveau > document Word**.</span><span class="sxs-lookup"><span data-stu-id="4388e-154">In the documents folder, click **New > Word document**.</span></span>
    
2. <span data-ttu-id="4388e-155">Tapez du texte dans le document vide.</span><span class="sxs-lookup"><span data-stu-id="4388e-155">Type some text in the blank document.</span></span> <span data-ttu-id="4388e-156">Attendez que le texte soit enregistré.</span><span class="sxs-lookup"><span data-stu-id="4388e-156">Wait for the text to be saved.</span></span>
    
3. <span data-ttu-id="4388e-157">Dans la barre de menus, cliquez sur **documents partagés**.</span><span class="sxs-lookup"><span data-stu-id="4388e-157">In the menu bar, click **Shared Documents**.</span></span>
    
4. <span data-ttu-id="4388e-158">Cliquez sur les points de suspension verticaux en regard de la **Document.docx** nom de fichier, puis cliquez sur **Détails**.</span><span class="sxs-lookup"><span data-stu-id="4388e-158">Click the vertical ellipsis next to the **Document.docx** file name, and then click **Details**.</span></span>
    
5. <span data-ttu-id="4388e-159">Dans le volet de droite, dans la section **Propriétés** , sous **appliquer l’étiquette de rétention**, Notez que l’étiquette de rétention **sensible** a été automatiquement appliquée au document.</span><span class="sxs-lookup"><span data-stu-id="4388e-159">In the right-hand pane, in the **Properties** section, under **Apply retention label**, note that the document has had the **Sensitive** retention label automatically applied.</span></span>
    
6. <span data-ttu-id="4388e-160">Cliquez sur \*\*Editer tout \*\*.</span><span class="sxs-lookup"><span data-stu-id="4388e-160">Click **Edit all**.</span></span>
    
7. <span data-ttu-id="4388e-161">Dans le volet **Document.docx** , sous **appliquer une étiquette de rétention**, sélectionnez l’étiquette **hautement confidentiel** , puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4388e-161">In the **Document.docx** pane, under **Apply retention label**, select the **Highly Confidential** label, and then click **Save**.</span></span>

## <a name="next-step"></a><span data-ttu-id="4388e-162">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="4388e-162">Next step</span></span>

<span data-ttu-id="4388e-163">Découvrez les fonctionnalités et les fonctionnalités de [protection des informations](m365-enterprise-test-lab-guides.md#information-protection) supplémentaires dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="4388e-163">Explore additional [information protection](m365-enterprise-test-lab-guides.md#information-protection) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="4388e-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4388e-164">See also</span></span>

[<span data-ttu-id="4388e-165">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="4388e-165">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="4388e-166">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="4388e-166">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="4388e-167">Documentation Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="4388e-167">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)

 

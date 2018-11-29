---
title: Environnement de test de classification des données pour votre entreprise 365 de Microsoft
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/16/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_TLGs
ms.assetid: 1aa9639b-2862-49c4-bc33-1586dda636b8
description: Utilisez ce Guide de laboratoire de Test pour créer et utiliser des étiquettes de Office 365 sur des documents dans votre environnement de test Microsoft 365 pour entreprises.
ms.openlocfilehash: 718cf038d88f1431ec6ca6fce1554d4f44dc1cb7
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867453"
---
# <a name="data-classification-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="aab8e-103">Environnement de test de classification des données pour votre entreprise 365 de Microsoft</span><span class="sxs-lookup"><span data-stu-id="aab8e-103">Data classification for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="aab8e-104">Les instructions de cet article, vous permet de configurer la classification des données à l’aide d’Office 365 étiquettes dans votre environnement de test Microsoft 365 pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="aab8e-104">With the instructions in this article, you configure data classification using Office 365 labels in your Microsoft 365 Enterprise test environment.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="aab8e-106">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="aab8e-106">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="aab8e-107">Phase 1 : Création de votre environnement de test Microsoft 365 pour entreprises</span><span class="sxs-lookup"><span data-stu-id="aab8e-107">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="aab8e-108">Si vous souhaitez simplement configurer des étiquettes d’Office 365 dans une solution légère avec la configuration minimale requise, suivez les instructions de [configuration de base léger](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="aab8e-108">If you just want to configure Office 365 labels in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="aab8e-109">Si vous souhaitez configurer des étiquettes d’Office 365 dans une entreprise simulée, suivez les instructions de [l’authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="aab8e-109">If you want to configure Office 365 labels in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="aab8e-p101">Test des étiquettes d’Office 365 ne nécessite pas l’environnement de test simulé entreprise, qui comprend un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt Windows Server Active Directory. Il est fourni ici en tant qu’option afin que vous puissiez licences automatisé et l’appartenance au groupe de test et tester dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="aab8e-p101">Testing Office 365 labels does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Windows Server AD forest. It is provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span> 

## <a name="phase-2-create-office-365-labels"></a><span data-ttu-id="aab8e-112">Phase 2 : Création d’étiquettes Office 365</span><span class="sxs-lookup"><span data-stu-id="aab8e-112">Phase 2: Create Office 365 labels</span></span>

<span data-ttu-id="aab8e-113">Dans cette phase, vous créez les étiquettes pour les différents niveaux de sécurité pour les dossiers de documents SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="aab8e-113">In this phase, you create the labels for the different levels of security for SharePoint Online documents folders.</span></span>
  
1. <span data-ttu-id="aab8e-p102">Si nécessaire, utilisez une instance privée de votre navigateur Internet et connectez-vous au portail Office 365 avec votre compte d’administrateur global. Pour une assistance, consultez la rubrique [pour vous connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="aab8e-p102">If needed, use a private instance of your Internet browser and sign in to the Office 365 portal with your global administrator account. For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="aab8e-116">Sous l’onglet **Accueil Microsoft Office**, cliquez sur la vignette **Administration**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-116">From the **Microsoft Office Home** tab, click the **Admin** tile.</span></span>
    
3. <span data-ttu-id="aab8e-117">Sous le nouvel onglet **Centre d’administration Office** de votre navigateur, cliquez sur **Centres d’administration > Sécurité &amp; conformité**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-117">From the new **Office Admin center** tab of your browser, click **Admin centers > Security &amp; Compliance**.</span></span>
    
4. <span data-ttu-id="aab8e-118">Sous le nouvel onglet **Accueil - Sécurité &amp; conformité de votre navigateur**, cliquez sur **Classifications > Étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-118">From the new **Home - Security &amp; Compliance** tab of your browser, click **Classifications > Labels**.</span></span>
    
5. <span data-ttu-id="aab8e-119">Dans le volet **Accueil > Étiquettes**, cliquez sur **Créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-119">From the **Home > Labels** pane, click **Create a label**.</span></span>
    
6. <span data-ttu-id="aab8e-120">Dans le volet **Nom de l’étiquette**, saisissez **Interne public** et cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-120">On the **Name your label** pane, type **Internal Public**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="aab8e-121">Dans le volet **Paramètres de l’étiquette**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-121">On the **Label settings** pane, click **Next**.</span></span>
    
8. <span data-ttu-id="aab8e-122">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer cette étiquette**, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-122">On the **Review your settings** pane, click **Create this label**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="aab8e-123">Répétez les étapes 5 à 8 pour les autres étiquettes suivantes :</span><span class="sxs-lookup"><span data-stu-id="aab8e-123">Repeat steps 5-8 for these additional labels:</span></span>
    
  - <span data-ttu-id="aab8e-124">Privé</span><span class="sxs-lookup"><span data-stu-id="aab8e-124">Private</span></span>
    
  - <span data-ttu-id="aab8e-125">Sensible</span><span class="sxs-lookup"><span data-stu-id="aab8e-125">Sensitive</span></span>
    
  - <span data-ttu-id="aab8e-126">Hautement confidentiel</span><span class="sxs-lookup"><span data-stu-id="aab8e-126">Highly Confidential</span></span>
    
10. <span data-ttu-id="aab8e-127">Dans le volet **Accueil > Étiquettes**, cliquez sur **Publier des étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-127">From the **Home > Labels** pane, click **Publish labels**.</span></span>
    
11. <span data-ttu-id="aab8e-128">Dans le volet **Choisir les étiquettes à publier**, cliquez sur **Choisir les étiquettes à publier**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-128">On the **Choose labels to publish** pane, click **Choose labels to publish**.</span></span>
    
12. <span data-ttu-id="aab8e-129">Dans le volet **Choisir des étiquettes**, cliquez sur **Ajouter** et sélectionnez les quatre étiquettes.</span><span class="sxs-lookup"><span data-stu-id="aab8e-129">On the **Choose labels** pane, click **Add** and select all four labels.</span></span>
    
13. <span data-ttu-id="aab8e-130">Cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-130">Click **Done**.</span></span>
    
14. <span data-ttu-id="aab8e-131">Dans le volet **Choisir les étiquettes à publier**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-131">On the **Choose labels to publish** pane, click **Next**.</span></span>
    
15. <span data-ttu-id="aab8e-132">Dans le volet **Choisir les emplacements**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-132">On the **Choose locations** pane, click **Next**.</span></span>
    
16. <span data-ttu-id="aab8e-133">Dans le volet **Nom de votre stratégie**, saisissez **Exemple d’organisation** sous **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-133">On the **Name your policy** pane, type **Example organization** in **Name**, and then click **Next**.</span></span>
    
17. <span data-ttu-id="aab8e-134">Dans le volet **Vérifier vos paramètres**, cliquez sur **Publier les étiquettes**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-134">On the **Review your settings** pane, click **Publish labels**, and then click **Close**.</span></span>

<span data-ttu-id="aab8e-135">Notez qu’il peut prendre quelques minutes pour les étiquettes à publier.</span><span class="sxs-lookup"><span data-stu-id="aab8e-135">Note that it might take a few minutes for the labels to be published.</span></span>

## <a name="phase-3-apply-office-365-labels-to-documents"></a><span data-ttu-id="aab8e-136">Phase 3 : Appliquer des étiquettes d’Office 365 à des documents</span><span class="sxs-lookup"><span data-stu-id="aab8e-136">Phase 3: Apply Office 365 labels to documents</span></span>

<span data-ttu-id="aab8e-137">Durant cette phase, vous découvrez le comportement d’étiquette par défaut pour les fichiers dans le dossier Documents d’un site SharePoint Online et modifiez manuellement l’étiquette d’un document.</span><span class="sxs-lookup"><span data-stu-id="aab8e-137">In this phase, you discover the default label behavior for files in the Documents folder of a SharePoint Online site and manually change the label of a document.</span></span>

<span data-ttu-id="aab8e-138">Tout d’abord, créez un site d’équipe SharePoint Online niveau critiques :</span><span class="sxs-lookup"><span data-stu-id="aab8e-138">First, create a sensitive-level SharePoint Online team site:</span></span>
  
1. <span data-ttu-id="aab8e-p103">En utilisant un navigateur sur votre ordinateur local, connectez-vous au portail Office 365 avec votre compte d’administrateur général. Pour obtenir de l’aide, consultez [Où se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="aab8e-p103">Using a browser on your local computer, sign in to the Office 365 portal using your global administrator account. For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="aab8e-141">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-141">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="aab8e-142">Dans le nouvel onglet **SharePoint** dans votre navigateur, cliquez sur **créer un site**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-142">On the new **SharePoint** tab in your browser, click **Create site**.</span></span>
    
4. <span data-ttu-id="aab8e-143">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-143">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="aab8e-144">Dans **nom du site d’équipe**, tapez **SensitiveFiles**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-144">In **Team site name**, type **SensitiveFiles**.</span></span>
    
6. <span data-ttu-id="aab8e-145">Dans la **description du site d’équipe**, tapez **le site SharePoint pour les fichiers sensibles**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-145">In **Team site description**, type **SharePoint site for sensitive files**.</span></span>
    
7.  <span data-ttu-id="aab8e-146">Dans **Paramètres de confidentialité**, sélectionnez **Privé - Seuls les membres peuvent accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-146">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="aab8e-147">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-147">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="aab8e-148">Ensuite, configurez le dossier Documents du site d’équipe pour l’étiquette sensible SensitiveFiles.</span><span class="sxs-lookup"><span data-stu-id="aab8e-148">Next, configure the Documents folder of the SensitiveFiles team site for the Sensitive label.</span></span>
  
1. <span data-ttu-id="aab8e-149">Dans l’onglet **SensitiveFiles** de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-149">In the **SensitiveFiles** tab of your browser, click **Documents**.</span></span>
    
2. <span data-ttu-id="aab8e-150">Cliquez sur l’icône des paramètres, puis cliquez sur **Paramètres de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-150">Click the settings icon, and then click **Library settings**.</span></span>
    
3. <span data-ttu-id="aab8e-151">Sous **Autorisations et gestion**, cliquez sur **Appliquer l’étiquette aux éléments de cette bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-151">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
4. <span data-ttu-id="aab8e-152">Dans **Les paramètres s’appliquent une étiquette**, sélectionnez **sensibles** dans la zone de liste déroulante, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-152">In **Settings-Apply Label**, select **Sensitive** in the drop-down box, and then click **Save**.</span></span>

<span data-ttu-id="aab8e-153">Ensuite, créez un nouveau document dans le site SensitiveFiles et modifier son étiquette.</span><span class="sxs-lookup"><span data-stu-id="aab8e-153">Next, create a new document in the SensitiveFiles site and change its label.</span></span>
    
1. <span data-ttu-id="aab8e-154">Dans le dossier documents, cliquez sur **Nouveau > document Word**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-154">In the documents folder, click **New > Word document**.</span></span>
    
2. <span data-ttu-id="aab8e-p104">Tapez du texte dans le document. Attendez que le texte à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="aab8e-p104">Type some text in the blank document. Wait for the text to be saved.</span></span>
    
3. <span data-ttu-id="aab8e-157">Dans la barre de menus, cliquez sur **Documents partagés**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-157">In the menu bar, click **Shared Documents**.</span></span>
    
4. <span data-ttu-id="aab8e-158">Cliquez sur l’icône en regard du nom de fichier **Document.docx** Word.</span><span class="sxs-lookup"><span data-stu-id="aab8e-158">Click the Word icon next to the **Document.docx** file name.</span></span>
    
5. <span data-ttu-id="aab8e-159">Dans le volet droit, dans la section **Propriétés** , sous l' **étiquette de l’appliquer**, notez que le document a été l’étiquette **sensibles** appliquée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="aab8e-159">In the right-hand pane, in the **Properties** section, under **Apply label**, note that the document has had the **Sensitive** label automatically applied.</span></span>
    
6. <span data-ttu-id="aab8e-160">Cliquez sur **Modifier tous les**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-160">Click **Edit all**.</span></span>
    
7. <span data-ttu-id="aab8e-161">Dans le volet **Document.docx** , sous l' **étiquette de l’appliquer**, sélectionnez l’étiquette **Hautement confidentielles** , puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="aab8e-161">In the **Document.docx** pane, under **Apply label**, select the **Highly Confidential** label, and then click **Save**.</span></span>

<span data-ttu-id="aab8e-162">Dans la phase de **protection des informations** pour des informations et des liens vers les étiquettes d’Office 365 en production, voir l’étape de [classification configurer pour votre environnement](data-classification-microsoft-365-enterprise-dev-test-environment.md) .</span><span class="sxs-lookup"><span data-stu-id="aab8e-162">See the [Configure classification for your environment](data-classification-microsoft-365-enterprise-dev-test-environment.md) step in the **Information protection** phase for information and links to Office 365 labels in production.</span></span>

## <a name="next-step"></a><span data-ttu-id="aab8e-163">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="aab8e-163">Next step</span></span>

<span data-ttu-id="aab8e-164">Explorez les fonctionnalités supplémentaires de [protection des informations](m365-enterprise-test-lab-guides.md#information-protection) et fonctionnalités dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="aab8e-164">Explore additional [information protection](m365-enterprise-test-lab-guides.md#information-protection) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="aab8e-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aab8e-165">See also</span></span>

[<span data-ttu-id="aab8e-166">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="aab8e-166">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="aab8e-167">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="aab8e-167">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="aab8e-168">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="aab8e-168">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)

 
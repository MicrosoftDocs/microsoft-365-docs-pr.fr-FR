---
title: Valider les paramètres de protection des applications sur les PC Windows 10
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
- Adm_O365
- Core_O365Admin_Migration
- MSB365
- MARVEL_SEO_MAR
search.appverid:
- BCS160
- MET150
ms.assetid: fae8819d-7235-495f-9f07-d016f545887f
description: Valider les paramètres de protection des applications professionnelles Microsoft 365 sur les appareils Windows 10 et vérifier que les utilisateurs ne peuvent pas copier les données de l’entreprise dans des fichiers personnels ou des applications non gérées.
ms.openlocfilehash: 4d3d7e950311ac32606e700ebb35bf026ae091cc
ms.sourcegitcommit: 26e4d5091583765257b7533b5156daa373cd19fe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2020
ms.locfileid: "42549994"
---
# <a name="validate-app-protection-settings-on-windows-10-pcs"></a><span data-ttu-id="bf4bb-103">Valider les paramètres de protection des applications sur les PC Windows 10</span><span class="sxs-lookup"><span data-stu-id="bf4bb-103">Validate app protection settings on Windows 10 PCs</span></span>

## <a name="verify-that-users-cannot-copy-company-data-to-personal-files-on-corporate-devices"></a><span data-ttu-id="bf4bb-104">Vérifiez que les utilisateurs ne peuvent pas copier des données professionnelles dans des fichiers personnels sur les appareils de l'entreprise</span><span class="sxs-lookup"><span data-stu-id="bf4bb-104">Verify that users cannot copy company data to personal files on corporate devices</span></span>

<span data-ttu-id="bf4bb-105">Une fois les [stratégies de protection des applications configurées](protection-settings-for-windows-10-devices.md), quelques heures peuvent être nécessaires avant que celles-ci prennent effet sur les appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-105">After you [set up app protection policies](protection-settings-for-windows-10-devices.md), it may take up to a few hours for the policy to take effect on users' devices.</span></span> <span data-ttu-id="bf4bb-106">Si vous avez **activé la** case à cocher **empêcher les utilisateurs de copier les données d’entreprise dans des fichiers personnels et les forcer à enregistrer les fichiers de travail dans OneDrive entreprise** pour les appareils appartenant à une entreprise, vous pouvez vérifier cela sur l’appareil de l’utilisateur après s’être connecté à Azure ad et s’être connecté.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-106">If you turned **On** the **Prevent users from copying company data to personal files and force them to save work files to OneDrive for Business** setting for company owned devices, you can check this on the user's device after they've connected to Azure AD and signed in.</span></span> 
  
 <span data-ttu-id="bf4bb-107">**Vérifier les paramètres de connexion**</span><span class="sxs-lookup"><span data-stu-id="bf4bb-107">**Verify connection settings**</span></span>
  
1. <span data-ttu-id="bf4bb-p102">Une fois authentifié avec vos informations d'identification Microsoft 365 Entreprise et connecté à Azure AD, comme décrit dans [Configurer des appareils Windows pour les utilisateurs de Microsoft 365 Business](set-up-windows-devices.md), accédez à **Paramètres Windows** \> **Comptes** \> **Accès Professionnel ou Scolaire**. Choisissez **Connecté à \<nom du client\> Azure AD**, puis **Informations**.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-p102">After you sign in with Microsoft 365 Business credentials and connect to Azure AD as described in [Set up Windows devices for Microsoft 365 Business users](set-up-windows-devices.md), go to **Windows Settings** \> **Accounts** \> **Access work or school**. Choose **Connected to \<tenant name\> Azure AD**, and then choose **Info**.</span></span>
    
    ![Click or tap Info on the Connected to Azure AD dialog.](../media/a36ede2b-d1a0-4d4e-8ea7-af39b4b63890.png)
  
2. <span data-ttu-id="bf4bb-111">Sur la page **géré par** \<nom\> de client, vous pouvez voir les **informations de connexion** qui incluent une adresse de serveur de **gestion** telle que celle illustrée dans la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-111">On the **Managed by** \<tenant name\> page, you can see the **Connection info** that includes a **Management Server Address** like the one shown in the following figure.</span></span> 
    
    ![Managed by page shows connection info of the device manager URL.](../media/47515a8e-2d0c-4bea-99f0-6b2545b88a11.png)
  
 <span data-ttu-id="bf4bb-113">**Vérifier que vous ne pouvez pas coller les données d’entreprise dans une application non gérée**</span><span class="sxs-lookup"><span data-stu-id="bf4bb-113">**Verify that you cannot paste company data in a non-managed app**</span></span>
  
1. <span data-ttu-id="bf4bb-114">Ouvrez l'instance d'Outlook 2016 qui a été installée par Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-114">Open Outlook 2016 that was installed by Microsoft 365 Business.</span></span>
    
2. <span data-ttu-id="bf4bb-115">Ouvrez un e-mail et copiez du contenu à partir de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-115">Open an email and copy some content from it.</span></span>
    
    <span data-ttu-id="bf4bb-116">Ouvrez le Bloc-notes et essayez de coller le contenu.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-116">Open Notepad and attempt to paste the content in.</span></span>
    
    <span data-ttu-id="bf4bb-117">Vous recevrez un message d’erreur indiquant que l’application ne peut pas accéder au contenu.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-117">You'll receive an error that states the app can't access content.</span></span>
    
    ![A dialog that states app can't access content when you paste into an unmanaged app.](../media/5e82b154-cf2f-43c8-ae80-b45d8ad80e56.png)
  
    <span data-ttu-id="bf4bb-119">En revanche, vous pouvez coller ce contenu dans Word 2016.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-119">You can, however, paste the same content into Word 2016.</span></span>
    
## <a name="verify-that-users-cannot-copy-company-data-to-personal-files-on-personal-devices"></a><span data-ttu-id="bf4bb-120">Vérifiez que les utilisateurs ne peuvent pas copier des données professionnelles dans des fichiers personnels sur des appareils personnels</span><span class="sxs-lookup"><span data-stu-id="bf4bb-120">Verify that users cannot copy company data to personal files on personal devices</span></span>

 <span data-ttu-id="bf4bb-121">**Vérifiez les paramètres de connexion**</span><span class="sxs-lookup"><span data-stu-id="bf4bb-121">**Verify connection settings**</span></span>
  
1. <span data-ttu-id="bf4bb-122">Sur votre appareil personnel Windows 10 où vous êtes connecté en tant qu’utilisateur local, accédez à **Paramètres Windows**, puis cliquez ou appuyez \*\*\*\* \> sur **l’accès aux comptes professionnel ou scolaire**.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-122">On your Windows 10 personal device where you're logged in as a local user, go to **Windows Settings**, and click or tap **Accounts** \> **Access work or school**.</span></span>
    
2. <span data-ttu-id="bf4bb-123">Sous **Accès Professionnel ou Scolaire**, choisissez **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-123">Under the **Access work or school**, choose **Connect**.</span></span>
    
3. <span data-ttu-id="bf4bb-124">Entrez vos informations d'identification Microsoft 365 Entreprise dans la boîte de dialogue **Configurer un compte professionnel ou scolaire** \> **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-124">Enter your Microsoft 365 Business credential into the **Set up a work or school account dialog** \> **Sign in**.</span></span>
    
4. <span data-ttu-id="bf4bb-125">Sur la page **Accès Professionnel ou Scolaire**, choisissez **Compte professionnel ou scolaire**, puis **Informations**.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-125">On the **Access work or school** page, choose the **Work or school account**, and then choose **Info**.</span></span>
    
    ![Cliquez ou appuyez sur informations dans la boîte de dialogue compte scolaire ou professionnel.](../media/63bd8b32-cb32-4afa-8ce0-6070ac403abc.png)
  
5. <span data-ttu-id="bf4bb-127">Sur la **page accès professionnel ou scolaire** , vous pouvez voir les **informations de connexion** qui incluent une **adresse de serveur de gestion** telle que celle illustrée dans la figure suivante, et inclut les mots travail en *cours* et *Mam* au sein de.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-127">On the **Access work or school** page, you can see the **Connection info** that includes a **Management Server Address** like the one shown in the following figure, and includes the words  *wip*  and  *mam*  within.</span></span> 
    
    ![Managed by page shows connection info URL that includes the words mam and wpi.](../media/abd4eaf4-44fa-4538-a3e8-1e0d331dfe1e.png)
  
 <span data-ttu-id="bf4bb-129">**Vérifier que vous ne pouvez pas coller les données d’entreprise dans une application non gérée**</span><span class="sxs-lookup"><span data-stu-id="bf4bb-129">**Verify that you cannot paste company data in a non-managed app**</span></span>
  
1. <span data-ttu-id="bf4bb-130">Ouvrez Outlook 2016 et, si nécessaire, ajoutez votre compte Microsoft 365 Entreprise, puis connectez-vous avec vos informations d'identification Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-130">Open Outlook 2016 and add your Microsoft 365 Business account if necessary and sign in with your Microsoft 365 Business credentials.</span></span>
    
2. <span data-ttu-id="bf4bb-131">Ouvrez un e-mail et copiez du contenu à partir de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-131">Open an email and copy some content from it.</span></span>
    
    <span data-ttu-id="bf4bb-132">Ouvrez le Bloc-notes et essayez de coller le contenu.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-132">Open Notepad and attempt to paste the content in.</span></span>
    
    <span data-ttu-id="bf4bb-133">Vous recevrez un message d’erreur indiquant que l’application ne peut pas accéder au contenu.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-133">You'll receive an error that states App can't access content.</span></span>
    
    ![A dialog that states app can't access content when you paste into an unmanaged app.](../media/5e82b154-cf2f-43c8-ae80-b45d8ad80e56.png)
  
    <span data-ttu-id="bf4bb-135">En revanche, vous pouvez coller ce contenu dans Word 2016.</span><span class="sxs-lookup"><span data-stu-id="bf4bb-135">You can, however, paste the same content into Word 2016.</span></span>
    


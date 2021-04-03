---
title: Valider les paramètres de protection des applications sur les PC Windows 10
f1.keywords:
- NOCSH
ms.author: sharik
author: skjerland
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
- seo-marvel-mar
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
ms.assetid: fae8819d-7235-495f-9f07-d016f545887f
description: Validez les paramètres de protection des applications Microsoft 365 Business Premium sur les appareils Windows 10 et vérifiez que les utilisateurs ne peuvent pas copier les données d’entreprise dans des fichiers personnels ou des applications non gérées.
ms.openlocfilehash: e319ffa5149f055b5de45078facc8899acffc223
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51579859"
---
# <a name="validate-app-protection-settings-on-windows-10-pcs"></a><span data-ttu-id="51ecd-103">Valider les paramètres de protection des applications sur les PC Windows 10</span><span class="sxs-lookup"><span data-stu-id="51ecd-103">Validate app protection settings on Windows 10 PCs</span></span>

## <a name="verify-that-users-cannot-copy-company-data-to-personal-files-on-corporate-devices"></a><span data-ttu-id="51ecd-104">Vérifiez que les utilisateurs ne peuvent pas copier des données professionnelles dans des fichiers personnels sur les appareils de l'entreprise</span><span class="sxs-lookup"><span data-stu-id="51ecd-104">Verify that users cannot copy company data to personal files on corporate devices</span></span>

<span data-ttu-id="51ecd-105">Une fois les [stratégies de protection des applications configurées](protection-settings-for-windows-10-devices.md), quelques heures peuvent être nécessaires avant que celles-ci prennent effet sur les appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="51ecd-105">After you [set up app protection policies](protection-settings-for-windows-10-devices.md), it may take up to a few hours for the policy to take effect on users' devices.</span></span> <span data-ttu-id="51ecd-106">Si vous  avez désactivé la fonctionnalité Empêcher les utilisateurs de copier des données d’entreprise dans des fichiers personnels et les forcer à enregistrer des fichiers professionnels dans le paramètre **OneDrive** Entreprise pour les appareils de l’entreprise, vous pouvez vérifier cela sur l’appareil de l’utilisateur une fois connecté à Azure AD et connecté.</span><span class="sxs-lookup"><span data-stu-id="51ecd-106">If you turned **On** the **Prevent users from copying company data to personal files and force them to save work files to OneDrive for Business** setting for company owned devices, you can check this on the user's device after they've connected to Azure AD and signed in.</span></span> 
  
 <span data-ttu-id="51ecd-107">**Vérifiez les paramètres de connexion**</span><span class="sxs-lookup"><span data-stu-id="51ecd-107">**Verify connection settings**</span></span>
  
1. <span data-ttu-id="51ecd-108">Après vous être connecté à l’aide des informations d’identification Microsoft 365 Business Premium et vous êtes connecté à Azure AD comme décrit dans Configurer des appareils Windows pour les utilisateurs [de Microsoft 365 Business Premium,](set-up-windows-devices.md)accédez à l’accès aux comptes De **Paramètres Windows** Accès au travail ou à l’école. \>  \> </span><span class="sxs-lookup"><span data-stu-id="51ecd-108">After you sign in with Microsoft 365 Business Premium credentials and connect to Azure AD as described in [Set up Windows devices for Microsoft 365 Business Premium users](set-up-windows-devices.md), go to **Windows Settings** \> **Accounts** \> **Access work or school**.</span></span> <span data-ttu-id="51ecd-109">Choose **Connected to Azure \<tenant name\> AD,** and then choose **Info**.</span><span class="sxs-lookup"><span data-stu-id="51ecd-109">Choose **Connected to \<tenant name\> Azure AD**, and then choose **Info**.</span></span>
    
    ![Click or tap Info on the Connected to Azure AD dialog.](../media/a36ede2b-d1a0-4d4e-8ea7-af39b4b63890.png)
  
2. <span data-ttu-id="51ecd-111">Dans la page **Géré par,** vous pouvez voir les informations de connexion qui incluent une adresse de serveur de gestion comme celle présentée \<tenant name\> dans la figure suivante.  </span><span class="sxs-lookup"><span data-stu-id="51ecd-111">On the **Managed by** \<tenant name\> page, you can see the **Connection info** that includes a **Management Server Address** like the one shown in the following figure.</span></span> 
    
    ![Managed by page shows connection info of the device manager URL.](../media/47515a8e-2d0c-4bea-99f0-6b2545b88a11.png)
  
 <span data-ttu-id="51ecd-113">**Vérifier que vous ne pouvez pas coller des données d’entreprise dans une application non gérée**</span><span class="sxs-lookup"><span data-stu-id="51ecd-113">**Verify that you cannot paste company data in a non-managed app**</span></span>
  
1. <span data-ttu-id="51ecd-114">Ouvrez Outlook 2016 qui a été installé par Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="51ecd-114">Open Outlook 2016 that was installed by Microsoft 365 Business Premium.</span></span>
    
2. <span data-ttu-id="51ecd-115">Ouvrez un e-mail et copiez du contenu à partir de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="51ecd-115">Open an email and copy some content from it.</span></span>
    
    <span data-ttu-id="51ecd-116">Ouvrez le Bloc-notes et essayez de coller le contenu.</span><span class="sxs-lookup"><span data-stu-id="51ecd-116">Open Notepad and attempt to paste the content in.</span></span>
    
    <span data-ttu-id="51ecd-117">Vous recevrez une erreur qui indique que l’application ne peut pas accéder au contenu.</span><span class="sxs-lookup"><span data-stu-id="51ecd-117">You'll receive an error that states the app can't access content.</span></span>
    
    ![A dialog that states app can't access content when you paste into an unmanaged app.](../media/5e82b154-cf2f-43c8-ae80-b45d8ad80e56.png)
  
    <span data-ttu-id="51ecd-119">En revanche, vous pouvez coller ce contenu dans Word 2016.</span><span class="sxs-lookup"><span data-stu-id="51ecd-119">You can, however, paste the same content into Word 2016.</span></span>
    
## <a name="verify-that-users-cannot-copy-company-data-to-personal-files-on-personal-devices"></a><span data-ttu-id="51ecd-120">Vérifiez que les utilisateurs ne peuvent pas copier des données professionnelles dans des fichiers personnels sur des appareils personnels</span><span class="sxs-lookup"><span data-stu-id="51ecd-120">Verify that users cannot copy company data to personal files on personal devices</span></span>

 <span data-ttu-id="51ecd-121">**Vérifiez les paramètres de connexion**</span><span class="sxs-lookup"><span data-stu-id="51ecd-121">**Verify connection settings**</span></span>
  
1. <span data-ttu-id="51ecd-122">Sur votre appareil personnel Windows 10 sur lequel vous êtes connecté en tant qu’utilisateur local, accédez à **Paramètres Windows,** puis cliquez ou appuyez sur Comptes Accès Au travail ou à  \> **l’école.**</span><span class="sxs-lookup"><span data-stu-id="51ecd-122">On your Windows 10 personal device where you're logged in as a local user, go to **Windows Settings**, and click or tap **Accounts** \> **Access work or school**.</span></span>
    
2. <span data-ttu-id="51ecd-123">Sous **Accès Professionnel ou Scolaire**, choisissez **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="51ecd-123">Under the **Access work or school**, choose **Connect**.</span></span>
    
3. <span data-ttu-id="51ecd-124">Entrez vos informations d’identification Microsoft  365 Business Premium dans la boîte de dialogue Configurer un compte scolaire ou \> **scolaire, connectez-vous.**</span><span class="sxs-lookup"><span data-stu-id="51ecd-124">Enter your Microsoft 365 Business Premium credential into the **Set up a work or school account dialog** \> **Sign in**.</span></span>
    
4. <span data-ttu-id="51ecd-125">Sur la page **Accès Professionnel ou Scolaire**, choisissez **Compte professionnel ou scolaire**, puis **Informations**.</span><span class="sxs-lookup"><span data-stu-id="51ecd-125">On the **Access work or school** page, choose the **Work or school account**, and then choose **Info**.</span></span>
    
    ![Cliquez ou appuyez sur Info dans la boîte de dialogue Compte scolaire ou travail.](../media/63bd8b32-cb32-4afa-8ce0-6070ac403abc.png)
  
5. <span data-ttu-id="51ecd-127">Dans la page **Accès** travail ou  scolaire, vous  pouvez voir les informations de connexion qui incluent une adresse de serveur de gestion comme celle présentée dans la figure suivante, et inclut les mots *wip* et *mam* dans.</span><span class="sxs-lookup"><span data-stu-id="51ecd-127">On the **Access work or school** page, you can see the **Connection info** that includes a **Management Server Address** like the one shown in the following figure, and includes the words  *wip*  and  *mam*  within.</span></span> 
    
    ![Managed by page shows connection info URL that includes the words mam and wpi.](../media/abd4eaf4-44fa-4538-a3e8-1e0d331dfe1e.png)
  
 <span data-ttu-id="51ecd-129">**Vérifier que vous ne pouvez pas coller des données d’entreprise dans une application non gérée**</span><span class="sxs-lookup"><span data-stu-id="51ecd-129">**Verify that you cannot paste company data in a non-managed app**</span></span>
  
1. <span data-ttu-id="51ecd-130">Ouvrez Outlook 2016 et ajoutez votre compte Microsoft 365 Business Premium si nécessaire et connectez-vous avec vos informations d’identification Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="51ecd-130">Open Outlook 2016 and add your Microsoft 365 Business Premium account if necessary and sign in with your Microsoft 365 Business Premium credentials.</span></span>
    
2. <span data-ttu-id="51ecd-131">Ouvrez un e-mail et copiez du contenu à partir de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="51ecd-131">Open an email and copy some content from it.</span></span>
    
    <span data-ttu-id="51ecd-132">Ouvrez le Bloc-notes et essayez de coller le contenu.</span><span class="sxs-lookup"><span data-stu-id="51ecd-132">Open Notepad and attempt to paste the content in.</span></span>
    
    <span data-ttu-id="51ecd-133">Vous recevrez une erreur qui indique que l’application ne peut pas accéder au contenu.</span><span class="sxs-lookup"><span data-stu-id="51ecd-133">You'll receive an error that states App can't access content.</span></span>
    
    ![A dialog that states app can't access content when you paste into an unmanaged app.](../media/5e82b154-cf2f-43c8-ae80-b45d8ad80e56.png)
  
    <span data-ttu-id="51ecd-135">En revanche, vous pouvez coller ce contenu dans Word 2016.</span><span class="sxs-lookup"><span data-stu-id="51ecd-135">You can, however, paste the same content into Word 2016.</span></span>
    


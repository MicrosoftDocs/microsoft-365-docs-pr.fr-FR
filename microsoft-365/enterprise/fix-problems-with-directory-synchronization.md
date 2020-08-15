---
title: Résoudre les problèmes de synchronisation d’annuaires pour Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: troubleshooting
ms.service: o365-administration
localization_priority: Priority
f1.keywords:
- CSH
ms.custom: Adm_O365
ms.collection:
- Ent_O365
- M365-identity-device-management
search.appverid:
- MET150
- MOE150
- MBS150
ms.assetid: 79c43023-5a47-45ae-8068-d8a26eee6bc2
description: Décrit les causes fréquentes des problèmes de synchronisation d’annuaires dans Office 365 et fournit plusieurs méthodes de résolution.
ms.openlocfilehash: 80b4a88e91230a8736f209ecd65c58b2882c25d6
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690153"
---
# <a name="fixing-problems-with-directory-synchronization-for-microsoft-365"></a><span data-ttu-id="20783-103">Résoudre les problèmes de synchronisation d’annuaires pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="20783-103">Fixing problems with directory synchronization for Microsoft 365</span></span>

<span data-ttu-id="20783-104">Avec la synchronisation d’annuaires, vous pouvez continuer à gérer les utilisateurs et les groupes sur site et à synchroniser les ajouts, les suppressions et les modifications dans le nuage.</span><span class="sxs-lookup"><span data-stu-id="20783-104">With directory synchronization, you can continue to manage users and groups on-premises and synchronize additions, deletions, and changes to the cloud.</span></span> <span data-ttu-id="20783-105">Cependant, la configuration est un peu compliquée, et il est parfois difficile d’identifier la source des problèmes.</span><span class="sxs-lookup"><span data-stu-id="20783-105">But setup is a little complicated and it can sometimes be difficult to identify the source of problems.</span></span> <span data-ttu-id="20783-106">Nous vous proposons des ressources pour vous aider à identifier les problèmes potentiels et à les corriger.</span><span class="sxs-lookup"><span data-stu-id="20783-106">We have resources to help you identify potential issues and fix them.</span></span>
  
## <a name="how-do-i-know-if-something-is-wrong"></a><span data-ttu-id="20783-107">Comment savoir si un problème se pose ?</span><span class="sxs-lookup"><span data-stu-id="20783-107">How do I know if something is wrong?</span></span>

<span data-ttu-id="20783-108">La première indication qu’un problème est incorrect se produit lorsque la vignette de l’état de la synchronisation d’annuaire dans le centre d’administration Microsoft 365 indique un problème.</span><span class="sxs-lookup"><span data-stu-id="20783-108">The first indication that something is wrong is when the DirSync Status tile in the Microsoft 365 admin center indicates there is a problem.</span></span>
  
<span data-ttu-id="20783-109">Vous allez également recevoir un message (adressé à votre adresse de messagerie de secours et à l’adresse de messagerie de l’administrateur) de Microsoft 365, indiquant que votre client a rencontré des erreurs de synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="20783-109">You will also receive a mail (to the alternate email and to your admin email) from Microsoft 365 that indicates your tenant has encountered directory synchronization errors.</span></span> <span data-ttu-id="20783-110">Pour plus d’informations, voir [Identifier les erreurs de synchronisation d’annuaires dans Microsoft 365](identify-directory-synchronization-errors.md).</span><span class="sxs-lookup"><span data-stu-id="20783-110">For details see [Identify directory synchronization errors in Microsoft 365](identify-directory-synchronization-errors.md).</span></span>
  
## <a name="how-do-i-get-azure-active-directory-connect-tool"></a><span data-ttu-id="20783-111">Comment obtenir l’outil Azure Active Directory Connect ?</span><span class="sxs-lookup"><span data-stu-id="20783-111">How do I get Azure Active Directory Connect tool?</span></span>

<span data-ttu-id="20783-112">Dans le [Centre d’administration Microsoft 365](https://admin.microsoft.com), accédez à **Utilisateurs** \> **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="20783-112">In the [Microsoft 365 admin center](https://admin.microsoft.com), navigate to **Users** \> **Active users**.</span></span> <span data-ttu-id="20783-113">Cliquez sur le menu **Plus** (points de suspension), puis sélectionnez **Synchronisation d’annuaires**.</span><span class="sxs-lookup"><span data-stu-id="20783-113">Click the **More** menu (three dots) and select **Directory synchronization**.</span></span> 
  
<span data-ttu-id="20783-114">Suivez les [instructions de l’Assistant](set-up-directory-synchronization.md) pour télécharger Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="20783-114">Follow the [instructions in the wizard](set-up-directory-synchronization.md) to download Azure AD Connect.</span></span> 
  
<span data-ttu-id="20783-115">Si vous utilisez toujours la synchronisation Azure Active Directory (Azure AD) (DirSync), consultez la page [Résolution des messages d’erreur lors de l’installation de l’outil de synchronisation Azure Active Directory et de l’Assistant Configuration dans Microsoft 365](https://go.microsoft.com/fwlink/p/?LinkId=396717) pour plus d’informations sur la configuration requise pour installer la synchronisation d’annuaires, les autorisations requises et le dépannage des erreurs courantes.</span><span class="sxs-lookup"><span data-stu-id="20783-115">If you are still using Azure Active Directory (Azure AD) Sync (DirSync), take a look at [How to troubleshoot Azure Active Directory Sync Tool installation and Configuration Wizard error messages in Microsoft 365](https://go.microsoft.com/fwlink/p/?LinkId=396717) for information about the system requirements to install dirsync, the permissions you need, and how to troubleshoot common errors.</span></span> 
  
<span data-ttu-id="20783-116">Pour effectuer la mise à jour à partir d’Azure AD Sync vers Azure AD Connect, voir [les instructions de mise à niveau](https://go.microsoft.com/fwlink/p/?LinkId=733240).</span><span class="sxs-lookup"><span data-stu-id="20783-116">To update from Azure AD Sync to Azure AD Connect, see [the upgrade instructions](https://go.microsoft.com/fwlink/p/?LinkId=733240).</span></span>
  
## <a name="resolving-common-causes-of-problems-with-directory-synchronization-in-microsoft-365"></a><span data-ttu-id="20783-117">Résolution des problèmes courants liés à la synchronisation d’annuaires dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="20783-117">Resolving common causes of problems with directory synchronization in Microsoft 365</span></span>

### <a name="synchronized-objects-arent-appearing-or-updating-online-or-im-getting-synchronization-error-reports-from-the-service"></a><span data-ttu-id="20783-118">Les objets synchronisés n’apparaissent pas ou ne sont pas mis à jour en ligne, ou j’obtiens des rapports d’erreurs de synchronisation du service.</span><span class="sxs-lookup"><span data-stu-id="20783-118">Synchronized objects aren't appearing or updating online, or I'm getting synchronization error reports from the Service.</span></span>

- [<span data-ttu-id="20783-119">Synchronisation des identités et résilience des attributs en double</span><span class="sxs-lookup"><span data-stu-id="20783-119">Identity synchronization and duplicate attribute resiliency</span></span>](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-syncservice-duplicate-attribute-resiliency)

### <a name="i-have-an-alert-in-the-admin-center-or-am-receiving-automated-emails-that-there-hasnt-been-a-recent-synchronization-event"></a><span data-ttu-id="20783-120">J’ai reçu une alerte dans le centre d’administration, ou je reçois des messages automatisés indiquant qu’il n’y a pas eu d’événement de synchronisation récemment</span><span class="sxs-lookup"><span data-stu-id="20783-120">I have an alert in the admin center, or am receiving automated emails that there hasn't been a recent synchronization event</span></span>
- [<span data-ttu-id="20783-121">Résoudre les problèmes de connectivité avec Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="20783-121">Troubleshoot connectivity issues with Azure AD Connect</span></span>](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-connectivity)
- [<span data-ttu-id="20783-122">Comptes et autorisations Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="20783-122">Azure AD Connect Accounts and permissions</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=820598)
- [<span data-ttu-id="20783-123">Synchronisation Azure AD Connect : gérer le compte de service Azure AD</span><span class="sxs-lookup"><span data-stu-id="20783-123">Azure AD Connect sync: How to manage the Azure AD service account</span></span>](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-azureadaccount)
- [<span data-ttu-id="20783-124">La synchronisation d’annuaires avec Azure Active Directory s’arrête ou vous êtes informé qu’aucune synchronisation n’a été enregistrée depuis plus d’une journée</span><span class="sxs-lookup"><span data-stu-id="20783-124">Directory synchronization to Azure Active Directory stops or you're warned that sync hasn't registered in more than a day</span></span>](https://support.microsoft.com/help/2882421/directory-synchronization-to-azure-active-directory-stops-or-you-re-warned-that-sync-hasn-t-registered-in-more-than-a-day)

### <a name="password-hashes-arent-synchronizing-or-im-seeing-an-alert-in-the-admin-center-that-there-hasnt-been-a-recent-password-hash-synchronization"></a><span data-ttu-id="20783-125">Les hachages de mot de passe ne sont pas synchronisés ou une alerte dans le centre d’administration indique qu’il n’existe aucune synchronisation récente de hachage de mot de passe</span><span class="sxs-lookup"><span data-stu-id="20783-125">Password hashes aren't synchronizing, or I'm seeing an alert in the admin center that there hasn't been a recent password hash synchronization</span></span>
- [<span data-ttu-id="20783-126">Mise en œuvre de la synchronisation du hachage de mot de passe avec la synchronisation Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="20783-126">Implementing password hash synchronization with Azure AD Connect sync</span></span>](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization)

### <a name="im-seeing-an-alert-that-object-quota-exceeded"></a><span data-ttu-id="20783-127">Une alerte indiquant un dépassement du quota d’objets apparaît</span><span class="sxs-lookup"><span data-stu-id="20783-127">I'm seeing an alert that Object quota exceeded</span></span>
- <span data-ttu-id="20783-128">Un quota d’objets prédéfini permet de protéger le service.</span><span class="sxs-lookup"><span data-stu-id="20783-128">We have a built-in object quota to help protect the service.</span></span> <span data-ttu-id="20783-129">Si trop d’objets dans votre annuaire doivent être synchronisés avec Microsoft 365, vous devrez [Contacter le support technique des produits professionnels](https://support.office.com/article/32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b) pour augmenter votre quota.</span><span class="sxs-lookup"><span data-stu-id="20783-129">If you have too many objects in your directory that need to sync to Microsoft 365, you'll have to [Contact support for business products](https://support.office.com/article/32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b) to increase your quota.</span></span>

### <a name="i-need-to-know-which-attributes-are-synchronized"></a><span data-ttu-id="20783-130">J’ai besoin de savoir quels attributs sont synchronisés.</span><span class="sxs-lookup"><span data-stu-id="20783-130">I need to know which attributes are synchronized</span></span>
- <span data-ttu-id="20783-131">La liste des attributs synchronisés entre l’environnement local et le cloud est [disponible ici](https://go.microsoft.com/fwlink/p/?LinkId=396719).</span><span class="sxs-lookup"><span data-stu-id="20783-131">You can find a list of all the attributes that are synced between on-premises and the cloud [right here](https://go.microsoft.com/fwlink/p/?LinkId=396719).</span></span>

### <a name="i-cant-manage-or-remove-objects-that-were-synchronized-to-the-cloud"></a><span data-ttu-id="20783-132">Je ne peux pas gérer ou supprimer les objets synchronisés avec le cloud</span><span class="sxs-lookup"><span data-stu-id="20783-132">I can't manage or remove objects that were synchronized to the cloud</span></span>
- <span data-ttu-id="20783-133">Êtes-vous prêt à gérer les objets dans le nuage uniquement ?</span><span class="sxs-lookup"><span data-stu-id="20783-133">Are you ready to manage objects in the cloud only?</span></span> <span data-ttu-id="20783-134">Ou existe-t-il un objet qui a été supprimé sur site, mais qui est bloqué dans le nuage ?</span><span class="sxs-lookup"><span data-stu-id="20783-134">Or is there an object that was deleted on-premises, but is stuck in the cloud?</span></span> <span data-ttu-id="20783-135">Consultez cet [Résolution des erreurs lors de la synchronisation](https://go.microsoft.com/fwlink/p/?linkid=842044) et [article du support technique](https://go.microsoft.com/fwlink/p/?LinkId=396720) pour obtenir des instructions sur la résolution de ces problèmes.</span><span class="sxs-lookup"><span data-stu-id="20783-135">Take a look at this [Troubleshooting Errors during synchronization](https://go.microsoft.com/fwlink/p/?linkid=842044) and [support article](https://go.microsoft.com/fwlink/p/?LinkId=396720) for guidance on how to resolve these issues.</span></span>

### <a name="i-got-an-error-message-that-my-company-has-exceeded-the-number-of-objects-that-can-be-synchronized"></a><span data-ttu-id="20783-136">J’ai reçu un message d’erreur indiquant que mon entreprise avait dépassé le nombre d’objets pouvant être synchronisés.</span><span class="sxs-lookup"><span data-stu-id="20783-136">I got an error message that my company has exceeded the number of objects that can be synchronized</span></span>
- <span data-ttu-id="20783-137">Vous pouvez consulter davantage d’informations sur le problème [ici](https://go.microsoft.com/fwlink/p/?LinkId=396721).</span><span class="sxs-lookup"><span data-stu-id="20783-137">You can read more about this issue [here](https://go.microsoft.com/fwlink/p/?LinkId=396721).</span></span>
   
## <a name="other-resources"></a><span data-ttu-id="20783-138">Autres ressources</span><span class="sxs-lookup"><span data-stu-id="20783-138">Other resources</span></span>

- [<span data-ttu-id="20783-139">Script de résolution des noms d’utilisateurs principaux en double</span><span class="sxs-lookup"><span data-stu-id="20783-139">Script to fix duplicate user principal names</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=396725)
    
- [<span data-ttu-id="20783-140">Préparation d’un domaine non routable (par exemple, le domaine .local) pour la synchronisation d’annuaires</span><span class="sxs-lookup"><span data-stu-id="20783-140">How to prepare a non-routable domain (such as .local domain) for directory synchronization</span></span>](prepare-a-non-routable-domain-for-directory-synchronization.md)
    
- [<span data-ttu-id="20783-141">Script de décompte du nombre total d’objets synchronisés</span><span class="sxs-lookup"><span data-stu-id="20783-141">Script to count total synchronized objects</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=396726)
    
- [<span data-ttu-id="20783-142">Résoudre les problèmes d’AD FS 2.0</span><span class="sxs-lookup"><span data-stu-id="20783-142">Troubleshoot AD FS 2.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=396727)
    
- [<span data-ttu-id="20783-143">Utiliser PowerShell pour corriger les attributs DisplayName vides pour les groupes à extension messagerie</span><span class="sxs-lookup"><span data-stu-id="20783-143">Use PowerShell to fix empty DisplayName attributes for mail-enabled groups</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=396728)
    
- [<span data-ttu-id="20783-144">Utiliser PowerShell pour corriger les noms d’utilisateurs principaux en double</span><span class="sxs-lookup"><span data-stu-id="20783-144">Use PowerShell to fix duplicate UPN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=396730)
    
- [<span data-ttu-id="20783-145">Utiliser PowerShell pour corriger les adresses de courrier en double</span><span class="sxs-lookup"><span data-stu-id="20783-145">Use PowerShell to fix duplicate email addresses</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=396731)
    

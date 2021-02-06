---
title: Transférer un domaine de Microsoft vers un autre hôte
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- Adm_O365_Setup
ms.custom:
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
description: 'Pour transférer un domaine de Microsoft vers un autre bureau d’enregistrement, recherchez les étapes ci-après. '
ms.openlocfilehash: f34e9733ab53c8bdc6f4432c96e6232ecc26ee06
ms.sourcegitcommit: eac5d9f759f290d3c51cafaf335a1a1c43ded927
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "50126346"
---
# <a name="transfer-a-domain-from-microsoft-to-another-host"></a><span data-ttu-id="997c5-103">Transférer un domaine de Microsoft vers un autre hôte</span><span class="sxs-lookup"><span data-stu-id="997c5-103">Transfer a domain from Microsoft to another host</span></span>

<span data-ttu-id="997c5-104">Vous ne pouvez pas transférer un domaine Microsoft 365 vers un autre bureau d’enregistrement pendant 60 jours après avoir acheté le domaine auprès de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="997c5-104">You can't transfer a Microsoft 365 domain to another registrar for 60 days after you purchase the domain from Microsoft.</span></span>

> [!NOTE]
> <span data-ttu-id="997c5-105">Une _requête Whois_ affiche un bureau d’enregistrement de domaines acheté par   Microsoft en tant que Wild West Domains LLC.</span><span class="sxs-lookup"><span data-stu-id="997c5-105">A _Whois_ query shows a Microsoft purchased domain registrar as Wild West Domains LLC.</span></span> <span data-ttu-id="997c5-106">Toutefois, seul Microsoft doit être contacté concernant votre domaine acheté par Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="997c5-106">However, only Microsoft should be contacted regarding your Microsoft 365 purchased domain.</span></span>

<span data-ttu-id="997c5-107">Suivez ces étapes pour obtenir un code auprès de Microsoft 365, puis allez sur l’autre site web du bureau d’enregistrement de domaines pour configurer le transfert de votre nom de domaine vers le nouveau bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="997c5-107">Follow these steps to get a code at Microsoft 365, and then go to the other domain registrar website to set up transferring your domain name to the new registrar.</span></span>

## <a name="transfer-a-domain"></a><span data-ttu-id="997c5-108">Transférer un domaine</span><span class="sxs-lookup"><span data-stu-id="997c5-108">Transfer a domain</span></span>

1. <span data-ttu-id="997c5-109">Dans le centre d’administration, allez à   **Paramètres,**   >  **domaines.**</span><span class="sxs-lookup"><span data-stu-id="997c5-109">In the admin center, go to   **Settings** > **Domains**.</span></span>

2. <span data-ttu-id="997c5-110">Dans la page **Domaines,** sélectionnez le domaine Microsoft 365 que vous souhaitez transférer vers un autre bureau d’enregistrement de domaines, puis **sélectionnez Vérifier l’état d’état.**</span><span class="sxs-lookup"><span data-stu-id="997c5-110">On the **Domains** page, select the Microsoft 365 domain that you want to transfer to another domain registrar, and then select **Check health**.</span></span>

3. <span data-ttu-id="997c5-111">En haut de la page, sélectionnez **Domaine de transfert.**</span><span class="sxs-lookup"><span data-stu-id="997c5-111">At the top of the page, select **Transfer domain**.</span></span>

4. <span data-ttu-id="997c5-112">Dans la page **Choisir où transférer** votre domaine, sélectionnez Un **autre** bureau d’enregistrement, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="997c5-112">On the **Choose where to transfer your domain** page, select **A different registrar**, and then click **Next**.</span></span>

5. <span data-ttu-id="997c5-113">Dans la page **Déverrouiller le** transfert de domaine, sélectionnez **Déverrouiller le transfert <_votre_ >** domaine, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="997c5-113">On the **Unlock domain transfer** page, select **Unlock transfer for <_your domain_>**, and then select **Next**.</span></span>

6. <span data-ttu-id="997c5-114">Vérifiez les informations de contact de transfert de votre domaine, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="997c5-114">Check your domain transfer contact information, and then select **Next**.</span></span>

7. <span data-ttu-id="997c5-115">Copiez le code d’autorisation et attendez environ 30 minutes que  l’état de transfert de votre domaine passe à Déverrouillé pour transfert sous l’onglet Inscription avant de passer aux étapes suivantes. </span><span class="sxs-lookup"><span data-stu-id="997c5-115">Copy the authorization code and wait about 30 minutes for your domain transfer status to change to **Unlocked for transfer** on the **Registration** tab before you proceed with next steps.</span></span>

8. <span data-ttu-id="997c5-116">Go to the website of the domain registrar you want to manage your domain name going forward.</span><span class="sxs-lookup"><span data-stu-id="997c5-116">Go to the website of the domain registrar you want to manage your domain name going forward.</span></span> <span data-ttu-id="997c5-117">Suivez les instructions pour transférer un domaine (recherchez de l’aide sur son site web).</span><span class="sxs-lookup"><span data-stu-id="997c5-117">Follow directions for transferring a domain (search for help on their website).</span></span> <span data-ttu-id="997c5-118">Cela implique généralement de payer des frais de transfert et de donner l’authcode au nouveau bureau d’enregistrement afin qu’il puisse lancer le transfert.</span><span class="sxs-lookup"><span data-stu-id="997c5-118">This usually means paying transfer fees and giving the Authcode to the new registrar so they can initiate the transfer.</span></span> <span data-ttu-id="997c5-119">Microsoft vous envoie un e-mail pour confirmer que nous avons reçu la demande de transfert, et le domaine transférera dans les 5 jours.</span><span class="sxs-lookup"><span data-stu-id="997c5-119">Microsoft will email you to confirm we’ve received the transfer request, and the domain will transfer within 5 days.</span></span>

    <span data-ttu-id="997c5-120">L’onglet Inscription du **code** d’autorisation se trouve dans la page  **Domaines** de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="997c5-120">You can find the authorization code **Registration** tab on the  **Domains** page in Microsoft 365.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="997c5-121">Les domaines .uk nécessitent une procédure différente.</span><span class="sxs-lookup"><span data-stu-id="997c5-121">.uk domains require a different procedure.</span></span> <span data-ttu-id="997c5-122">Contactez le Support Microsoft et demandez une modification de balise **IPS** pour correspondre au bureau d’enregistrement que vous souhaitez gérer à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="997c5-122">Contact Microsoft Support and request an **IPS Tag change** to match the registrar you want to manage your domain going forward.</span></span> <span data-ttu-id="997c5-123">Une fois la balise changée, le domaine transfère immédiatement vers le nouveau bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="997c5-123">Once the tag changes, the domain immediately transfers to the new registrar.</span></span> <span data-ttu-id="997c5-124">Vous devrez ensuite travailler avec le nouveau bureau d’enregistrement pour effectuer le transfert, en payant probablement des frais de transfert et en ajoutant le domaine transféré à votre compte avec votre nouveau bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="997c5-124">You will then need to work with the new registrar to complete the transfer, likely paying transfer fees and adding the transferred domain to your account with your new registrar.</span></span>

9. <span data-ttu-id="997c5-125">Une fois le transfert terminé, vous renouvelez votre domaine auprès du nouveau bureau d’enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="997c5-125">After the transfer is complete, you'll renew your domain at the new domain registrar.</span></span>

10. <span data-ttu-id="997c5-126">Pour terminer le processus, revenir à la page **Domaines** dans le centre d’administration, puis sélectionnez   **Terminer le transfert de domaine.**</span><span class="sxs-lookup"><span data-stu-id="997c5-126">To finish the process, go back to the **Domains** page in the admin center, and then select  **Complete domain transfer**.</span></span> <span data-ttu-id="997c5-127">Cela marque le domaine comme n’étant plus acheté auprès de Microsoft 365 et désactive l’abonnement au domaine.</span><span class="sxs-lookup"><span data-stu-id="997c5-127">This will mark the domain as no longer purchased from Microsoft 365, and will disable the domain subscription.</span></span> <span data-ttu-id="997c5-128">Il ne supprime pas le domaine du client et n’affecte pas les utilisateurs et boîtes aux lettres existants sur le domaine.</span><span class="sxs-lookup"><span data-stu-id="997c5-128">It will not remove the domain from the tenant, and will not affect existing users and mailboxes on the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="997c5-129">Les domaines achetés par Microsoft 365 ne sont pas éligibles aux modifications de serveurs de noms ou au transfert du domaine entre des organisations Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="997c5-129">Microsoft 365 purchased domains are not eligible for nameserver changes or transferring the domain between Microsoft 365 organizations.</span></span> <span data-ttu-id="997c5-130">Si l’une d’elles est requise, l’inscription de domaine doit être transférée vers un autre bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="997c5-130">If either of these are required, the domain registration must be transferred to another registrar.</span></span>

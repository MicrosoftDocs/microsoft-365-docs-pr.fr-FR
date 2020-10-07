---
title: Transférer un domaine de Microsoft vers un autre hôte
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
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
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
description: 'Recherchez les étapes à suivre pour transférer un domaine de Microsoft vers un autre serveur d’inscriptions. '
ms.openlocfilehash: d960b57a2c82b804d61ead1c672c00f0543b3ae8
ms.sourcegitcommit: 33afa334328cc4e3f2474abd611c1411adabd39f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/07/2020
ms.locfileid: "48370323"
---
# <a name="transfer-a-domain-from-microsoft-to-another-host"></a><span data-ttu-id="841c5-103">Transférer un domaine de Microsoft vers un autre hôte</span><span class="sxs-lookup"><span data-stu-id="841c5-103">Transfer a domain from Microsoft to another host</span></span>

<span data-ttu-id="841c5-104">Vous ne pouvez pas transférer un domaine Microsoft 365 vers un autre bureau d’enregistrement pendant 60 jours après avoir acheté le domaine auprès de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="841c5-104">You can't transfer a Microsoft 365 domain to another registrar for 60 days after you purchase the domain from Microsoft.</span></span>

> [!NOTE]
> <span data-ttu-id="841c5-105">Une requête _Whois_   affiche un bureau d’enregistrement de domaines Microsoft acheté comme sauvage (plain West Domains).</span><span class="sxs-lookup"><span data-stu-id="841c5-105">A _Whois_ query shows a Microsoft purchased domain registrar as Wild West Domains LLC.</span></span> <span data-ttu-id="841c5-106">Toutefois, seul Microsoft doit être contacté concernant votre domaine acheté Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="841c5-106">However, only Microsoft should be contacted regarding your Microsoft 365 purchased domain.</span></span>

<span data-ttu-id="841c5-107">Suivez les étapes ci-dessous pour obtenir un code auprès de Microsoft 365, puis accédez au site Web du Bureau d’enregistrement de domaine pour configurer le transfert de votre nom de domaine vers le nouveau serveur d’inscriptions.</span><span class="sxs-lookup"><span data-stu-id="841c5-107">Follow these steps to get a code at Microsoft 365, and then go to the other domain registrar website to set up transferring your domain name to the new registrar.</span></span>

## <a name="transfer-a-domain"></a><span data-ttu-id="841c5-108">Transférer un domaine</span><span class="sxs-lookup"><span data-stu-id="841c5-108">Transfer a domain</span></span>

1. <span data-ttu-id="841c5-109">Dans le centre d’administration, accédez à  **paramètres**   >  **Domains**.</span><span class="sxs-lookup"><span data-stu-id="841c5-109">In the admin center, go to  **Settings** > **Domains**.</span></span>

2. <span data-ttu-id="841c5-110">Sur la page **domaines** , sélectionnez le domaine Microsoft 365 que vous souhaitez transférer vers un autre bureau d’enregistrement de domaines, puis sélectionnez **vérifier l’intégrité**.</span><span class="sxs-lookup"><span data-stu-id="841c5-110">On the **Domains** page, select the Microsoft 365 domain that you want to transfer to another domain registrar, and then select **Check health**.</span></span>

3. <span data-ttu-id="841c5-111">En haut de la page, sélectionnez **transférer un domaine**.</span><span class="sxs-lookup"><span data-stu-id="841c5-111">At the top of the page, select **Transfer domain**.</span></span>

4. <span data-ttu-id="841c5-112">Sur la page **choisir l’emplacement de transfert de votre domaine** , sélectionnez **un autre bureau**d’enregistrement, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="841c5-112">On the **Choose where to transfer your domain** page, select **A different registrar**, and then click **Next**.</span></span>

5. <span data-ttu-id="841c5-113">Sur la page **déverrouiller le transfert de domaine** , sélectionnez \*\*déverrouiller le transfert pour les <_votre domaine_ > \*\*, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="841c5-113">On the **Unlock domain transfer** page, select **Unlock transfer for <_your domain_>**, and then select **Next**.</span></span>

6. <span data-ttu-id="841c5-114">Vérifiez votre domaine transférer les informations de contact, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="841c5-114">Check your domain transfer contact information, and then select **Next**.</span></span>

7. <span data-ttu-id="841c5-115">Copiez le code d’autorisation et patientez 30 minutes avant que l’état de transfert de votre domaine passe à **déverrouillé pour le transfert** sous l’onglet **enregistrement** avant de passer aux étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="841c5-115">Copy the authorization code and wait about 30 minutes for your domain transfer status to change to **Unlocked for transfer** on the **Registration** tab before you proceed with next steps.</span></span>

8. <span data-ttu-id="841c5-116">Accédez au site Web du Bureau d’enregistrement de domaines dont vous souhaitez gérer le nom de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="841c5-116">Go to the website of the domain registrar you want to manage your domain name going forward.</span></span> <span data-ttu-id="841c5-117">Suivez les instructions pour le transfert d’un domaine (recherchez de l’aide sur son site Web).</span><span class="sxs-lookup"><span data-stu-id="841c5-117">Follow directions for transferring a domain (search for help on their website).</span></span> <span data-ttu-id="841c5-118">Cela signifie généralement le paiement des frais de transfert et l’octroi du authcode au nouveau serveur d’inscriptions afin qu’ils puissent initier le transfert.</span><span class="sxs-lookup"><span data-stu-id="841c5-118">This usually means paying transfer fees and giving the Authcode to the new registrar so they can initiate the transfer.</span></span> <span data-ttu-id="841c5-119">Microsoft vous enverra un message électronique confirmant que nous avons reçu la demande de transfert et le domaine sera transféré dans un délai de 5 jours.</span><span class="sxs-lookup"><span data-stu-id="841c5-119">Microsoft will email you to confirm we’ve received the transfer request, and the domain will transfer within 5 days.</span></span>

    <span data-ttu-id="841c5-120">L’onglet **enregistrement** du code d’autorisation se trouve sur la page  **domaines** dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="841c5-120">You can find the authorization code **Registration** tab on the  **Domains** page in Microsoft 365.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="841c5-121">les domaines. uk nécessitent une autre procédure.</span><span class="sxs-lookup"><span data-stu-id="841c5-121">.uk domains require a different procedure.</span></span> <span data-ttu-id="841c5-122">Contactez le support Microsoft et demandez un **changement de balise IPS** pour qu’il corresponde au serveur d’inscriptions dont vous souhaitez gérer votre domaine.</span><span class="sxs-lookup"><span data-stu-id="841c5-122">Contact Microsoft Support and request an **IPS Tag change** to match the registrar you want to manage your domain going forward.</span></span> <span data-ttu-id="841c5-123">Une fois que la balise est modifiée, le domaine est transféré immédiatement vers le nouveau serveur d’inscriptions.</span><span class="sxs-lookup"><span data-stu-id="841c5-123">Once the tag changes, the domain immediately transfers to the new registrar.</span></span> <span data-ttu-id="841c5-124">Vous devrez ensuite utiliser le nouveau serveur d’inscriptions pour terminer le transfert, payant les frais de transfert et en ajoutant le domaine transféré à votre compte avec votre nouveau bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="841c5-124">You will then need to work with the new registrar to complete the transfer, likely paying transfer fees and adding the transferred domain to your account with your new registrar.</span></span>

9. <span data-ttu-id="841c5-125">Une fois le transfert terminé, vous allez renouveler votre domaine au niveau du nouveau bureau d’enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="841c5-125">After the transfer is complete, you'll renew your domain at the new domain registrar.</span></span>

10. <span data-ttu-id="841c5-126">Pour terminer le processus, revenez à la page **domaines** dans le centre d’administration, puis sélectionnez  **transfert de domaine complet**.</span><span class="sxs-lookup"><span data-stu-id="841c5-126">To finish the process, go back to the **Domains** page in the admin center, and then select  **Complete domain transfer**.</span></span> <span data-ttu-id="841c5-127">Cela permet de marquer le domaine comme n’étant plus acheté auprès de Microsoft 365 et de désactiver l’abonnement au domaine.</span><span class="sxs-lookup"><span data-stu-id="841c5-127">This will mark the domain as no longer purchased from Microsoft 365, and will disable the domain subscription.</span></span> <span data-ttu-id="841c5-128">Il ne supprime pas le domaine du client et n’affecte pas les utilisateurs et boîtes aux lettres existants sur le domaine.</span><span class="sxs-lookup"><span data-stu-id="841c5-128">It will not remove the domain from the tenant, and will not affect existing users and mailboxes on the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="841c5-129">Les domaines achetés par Microsoft 365 ne sont pas éligibles pour les modifications de serveur de noms ou le transfert de domaine entre les organisations Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="841c5-129">Microsoft 365 purchased domains are not eligible for nameserver changes or transferring the domain between Microsoft 365 organizations.</span></span> <span data-ttu-id="841c5-130">Si l’une de ces valeurs est requise, l’inscription du domaine doit être transférée vers un autre serveur d’inscriptions.</span><span class="sxs-lookup"><span data-stu-id="841c5-130">If either of these are required, the domain registration must be transferred to another registrar.</span></span>

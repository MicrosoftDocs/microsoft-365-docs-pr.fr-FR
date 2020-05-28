---
title: Résoudre les problèmes liés aux boîtes aux lettres partagées
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- MSStore_Link
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
description: Essayez ces solutions si vous rencontrez des problèmes avec les boîtes aux lettres partagées.
ms.openlocfilehash: 5d6de9ac66b11f0e50b259cdca0b1bb50b8326ee
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44400015"
---
# <a name="resolve-issues-with-shared-mailboxes"></a><span data-ttu-id="227cc-103">Résoudre les problèmes liés aux boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="227cc-103">Resolve issues with shared mailboxes</span></span>

<span data-ttu-id="227cc-104">Si des messages d’erreur s’affichent lors de la création ou de l’utilisation d’une boîte aux lettres partagée, essayez ces solutions possibles.</span><span class="sxs-lookup"><span data-stu-id="227cc-104">If you see error messages when creating or using a shared mailbox, try these possible solutions.</span></span> 

## <a name="error-when-creating-shared-mailboxes"></a><span data-ttu-id="227cc-105">Erreur lors de la création de boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="227cc-105">Error when creating shared mailboxes</span></span>
<span data-ttu-id="227cc-106"><a name="bkmk_Fix"> </a></span><span class="sxs-lookup"><span data-stu-id="227cc-106"><a name="bkmk_Fix"> </a></span></span>

<span data-ttu-id="227cc-107">Si le message d’erreur s’affiche, **l’adresse proxy « SMTP : nom de la boîte aux lettres partagée <\> » est déjà utilisée par les adresses proxy ou legacyExchangeDN de « \<name> ». Veuillez choisir une autre adresse proxy**, ce qui signifie que vous essayez de donner à la boîte aux lettres partagée un nom qui est déjà utilisé.</span><span class="sxs-lookup"><span data-stu-id="227cc-107">If you see the error message, **The proxy address "smtp:<shared mailbox name\>" is already being used by the proxy addresses or LegacyExchangeDN of "\<name>". Please choose another proxy address**, it means you're trying to give the shared mailbox a name that's already in use.</span></span> <span data-ttu-id="227cc-108">Par exemple, imaginons que vous vouliez donner les noms info@domaine1 et info@domaine2 à des boîtes aux lettres partagées.</span><span class="sxs-lookup"><span data-stu-id="227cc-108">For example, let's say you want shared mailboxes named info@domain1 and info@domain2.</span></span> <span data-ttu-id="227cc-109">Vous pouvez procéder de deux manières :</span><span class="sxs-lookup"><span data-stu-id="227cc-109">There are two ways to do this:</span></span>

  - <span data-ttu-id="227cc-110">Utiliser Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="227cc-110">Use Windows PowerShell.</span></span> <span data-ttu-id="227cc-111">Consultez ce billet de blog pour obtenir des instructions : [créer des boîtes aux lettres partagées avec le même alias sur des domaines différents](https://www.cogmotive.com/blog/office-365-tips/create-shared-mailboxes-with-same-alias-at-different-domains-in-office-365)</span><span class="sxs-lookup"><span data-stu-id="227cc-111">See this blog post for instructions: [Create Shared Mailboxes with Same Alias at Different Domains](https://www.cogmotive.com/blog/office-365-tips/create-shared-mailboxes-with-same-alias-at-different-domains-in-office-365)</span></span>
    
  - <span data-ttu-id="227cc-112">Nommez la deuxième boîte aux lettres partagée quelque part du début pour contourner l’erreur.</span><span class="sxs-lookup"><span data-stu-id="227cc-112">Name the second shared mailbox something different from the start to get around the error.</span></span> <span data-ttu-id="227cc-113">Ensuite, dans le centre d’administration, renommez la boîte aux lettres partagée comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="227cc-113">Then in the admin center, rename the shared mailbox to what you want it to be.</span></span>

## <a name="error-about-not-having-send-permissions-when-using-a-shared-mailbox"></a><span data-ttu-id="227cc-114">Erreur de n’avoir pas les autorisations d’envoi lors de l’utilisation d’une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="227cc-114">Error about not having send permissions when using a shared mailbox</span></span>

<span data-ttu-id="227cc-115">Si vous avez créé une boîte aux lettres partagée et essayez d’envoyer un message à partir de celle-ci, vous pouvez obtenir ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="227cc-115">If you created a shared mailbox and then try to send a message from it, you might get this:</span></span>

<span data-ttu-id="227cc-116">**Ce message n’a pas pu être envoyé. Vous n’êtes pas autorisé à envoyer le message au nom de l’utilisateur spécifié.**</span><span class="sxs-lookup"><span data-stu-id="227cc-116">**This message could not be sent. You do not have the permission to send the message on behalf of the specified user.**</span></span>

<span data-ttu-id="227cc-117">Ce message s’affiche lorsque Microsoft 365 rencontre un problème de latence de réplication.</span><span class="sxs-lookup"><span data-stu-id="227cc-117">This message appears when Microsoft 365 is experiencing a replication latency issue.</span></span> <span data-ttu-id="227cc-118">Elle doit disparaître au bout d’une heure, lorsque les informations sur votre nouvelle boîte aux lettres partagée (ou utilisateur ajouté) sont répliquées sur l’ensemble de nos centres de données.</span><span class="sxs-lookup"><span data-stu-id="227cc-118">It should go away in an hour or so, when the information about your new shared mailbox (or added user) is replicated across all of our data centers.</span></span> <span data-ttu-id="227cc-119">Patientez une heure, puis réessayez d’envoyer un message.</span><span class="sxs-lookup"><span data-stu-id="227cc-119">Wait an hour and then try again to send a message.</span></span>

## <a name="related-articles"></a><span data-ttu-id="227cc-120">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="227cc-120">Related articles</span></span>

[<span data-ttu-id="227cc-121">À propos des boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="227cc-121">About shared mailboxes</span></span>](about-shared-mailboxes.md)

[<span data-ttu-id="227cc-122">Créer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="227cc-122">Create a shared mailbox</span></span>](create-a-shared-mailbox.md)

[<span data-ttu-id="227cc-123">Configurer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="227cc-123">Configure a shared mailbox</span></span>](configure-a-shared-mailbox.md)

[<span data-ttu-id="227cc-124">Convertir une boîte aux lettres utilisateur en boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="227cc-124">Convert a user mailbox to a shared mailbox</span></span>](convert-user-mailbox-to-shared-mailbox.md)

[<span data-ttu-id="227cc-125">Supprimer une licence à partir d’une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="227cc-125">Remove a license from a shared mailbox</span></span>](remove-license-from-shared-mailbox.md)


    


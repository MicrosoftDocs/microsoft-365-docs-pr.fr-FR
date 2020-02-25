---
title: Résoudre les problèmes liés aux boîtes aux lettres partagées
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- MSStore_Link
search.appverid:
- BCS160
- MET150
- MOE150
description: Essayez ces solutions si vous rencontrez des problèmes avec les boîtes aux lettres partagées.
ms.openlocfilehash: b45c2eefa8cb4fb5fa34808223efbc1f0023161d
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42252977"
---
# <a name="resolve-issues-with-shared-mailboxes"></a><span data-ttu-id="284ba-103">Résoudre les problèmes liés aux boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="284ba-103">Resolve issues with shared mailboxes</span></span>

<span data-ttu-id="284ba-104">Si des messages d’erreur s’affichent lors de la création ou de l’utilisation d’une boîte aux lettres partagée, essayez ces solutions possibles.</span><span class="sxs-lookup"><span data-stu-id="284ba-104">If you see error messages when creating or using a shared mailbox, try these possible solutions.</span></span> 

## <a name="error-when-creating-shared-mailboxes"></a><span data-ttu-id="284ba-105">Erreur lors de la création de boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="284ba-105">Error when creating shared mailboxes</span></span>
<span data-ttu-id="284ba-106"><a name="bkmk_Fix"> </a></span><span class="sxs-lookup"><span data-stu-id="284ba-106"><a name="bkmk_Fix"> </a></span></span>

<span data-ttu-id="284ba-107">Si le message d’erreur s’affiche, **l’adresse proxy « SMTP : <nom\>de la boîte aux lettres partagée » est déjà utilisée par les adresses proxy\<ou legacyExchangeDN de « Name> ». Veuillez choisir une autre adresse proxy**, ce qui signifie que vous essayez de donner à la boîte aux lettres partagée un nom qui est déjà utilisé.</span><span class="sxs-lookup"><span data-stu-id="284ba-107">If you see the error message, **The proxy address "smtp:<shared mailbox name\>" is already being used by the proxy addresses or LegacyExchangeDN of "\<name>". Please choose another proxy address**, it means you're trying to give the shared mailbox a name that's already in use.</span></span> <span data-ttu-id="284ba-108">Par exemple, imaginons que vous vouliez donner les noms info@domaine1 et info@domaine2 à des boîtes aux lettres partagées.</span><span class="sxs-lookup"><span data-stu-id="284ba-108">For example, let's say you want shared mailboxes named info@domain1 and info@domain2.</span></span> <span data-ttu-id="284ba-109">Vous pouvez procéder de deux manières :</span><span class="sxs-lookup"><span data-stu-id="284ba-109">There are two ways to do this:</span></span>

  - <span data-ttu-id="284ba-110">Utiliser Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="284ba-110">Use Windows PowerShell.</span></span> <span data-ttu-id="284ba-111">Consultez le billet de blog suivant pour obtenir des instructions : [Créer des boîtes aux lettres partagées avec le même alias sur différents domaines dans Office 365](https://www.cogmotive.com/blog/office-365-tips/create-shared-mailboxes-with-same-alias-at-different-domains-in-office-365)</span><span class="sxs-lookup"><span data-stu-id="284ba-111">See this blog post for instructions: [Create Shared Mailboxes with Same Alias at Different Domains in Office 365](https://www.cogmotive.com/blog/office-365-tips/create-shared-mailboxes-with-same-alias-at-different-domains-in-office-365)</span></span>
    
  - <span data-ttu-id="284ba-112">Nommez la deuxième boîte aux lettres partagée quelque part du début pour contourner l’erreur.</span><span class="sxs-lookup"><span data-stu-id="284ba-112">Name the second shared mailbox something different from the start to get around the error.</span></span> <span data-ttu-id="284ba-113">Ensuite, dans le centre d’administration, renommez la boîte aux lettres partagée comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="284ba-113">Then in the admin center, rename the shared mailbox to what you want it to be.</span></span>

## <a name="error-about-not-having-send-permissions-when-using-a-shared-mailbox"></a><span data-ttu-id="284ba-114">Erreur de n’avoir pas les autorisations d’envoi lors de l’utilisation d’une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="284ba-114">Error about not having send permissions when using a shared mailbox</span></span>

<span data-ttu-id="284ba-115">Si vous avez créé une boîte aux lettres partagée et essayez d’envoyer un message à partir de celle-ci, vous pouvez obtenir ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="284ba-115">If you created a shared mailbox and then try to send a message from it, you might get this:</span></span>

<span data-ttu-id="284ba-116">**Ce message n’a pas pu être envoyé. Vous n’êtes pas autorisé à envoyer le message au nom de l’utilisateur spécifié.**</span><span class="sxs-lookup"><span data-stu-id="284ba-116">**This message could not be sent. You do not have the permission to send the message on behalf of the specified user.**</span></span>

<span data-ttu-id="284ba-117">Ce message s’affiche lorsque Office 365 rencontre un problème de latence de réplication.</span><span class="sxs-lookup"><span data-stu-id="284ba-117">This message appears when Office 365 is experiencing a replication latency issue.</span></span> <span data-ttu-id="284ba-118">Elle doit disparaître au bout d’une heure, lorsque les informations sur votre nouvelle boîte aux lettres partagée (ou utilisateur ajouté) sont répliquées sur l’ensemble de nos centres de données.</span><span class="sxs-lookup"><span data-stu-id="284ba-118">It should go away in an hour or so, when the information about your new shared mailbox (or added user) is replicated across all of our data centers.</span></span> <span data-ttu-id="284ba-119">Patientez une heure, puis réessayez d’envoyer un message.</span><span class="sxs-lookup"><span data-stu-id="284ba-119">Wait an hour and then try again to send a message.</span></span>

## <a name="related-articles"></a><span data-ttu-id="284ba-120">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="284ba-120">Related articles</span></span>

[<span data-ttu-id="284ba-121">À propos des boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="284ba-121">About shared mailboxes</span></span>](about-shared-mailboxes.md)

[<span data-ttu-id="284ba-122">Créer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="284ba-122">Create a shared mailbox</span></span>](create-a-shared-mailbox.md)

[<span data-ttu-id="284ba-123">Configurer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="284ba-123">Configure a shared mailbox</span></span>](configure-a-shared-mailbox.md)

[<span data-ttu-id="284ba-124">Convertir une boîte aux lettres utilisateur en boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="284ba-124">Convert a user mailbox to a shared mailbox</span></span>](convert-user-mailbox-to-shared-mailbox.md)

[<span data-ttu-id="284ba-125">Supprimer une licence d’une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="284ba-125">Remove a license from a shared mailbox</span></span>](remove-license-from-shared-mailbox.md)


    


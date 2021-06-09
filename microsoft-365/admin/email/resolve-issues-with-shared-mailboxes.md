---
title: Résoudre les problèmes liés aux boîtes aux lettres partagées
f1.keywords:
- NOCSH
ms.author: sharik
author: SKjerland
manager: scotv
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
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
description: Vous pouvez obtenir des erreurs lorsque vous définissez des boîtes aux lettres partagées. Essayez ces solutions si vous avez des problèmes avec les boîtes aux lettres partagées.
ms.openlocfilehash: 89cdfbe29ab035b1eb6c3a0183629eef59d67477
ms.sourcegitcommit: a05f61a291eb4595fa9313757a3815b7f217681d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2021
ms.locfileid: "52706129"
---
# <a name="resolve-issues-with-shared-mailboxes"></a><span data-ttu-id="c741e-104">Résoudre les problèmes liés aux boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="c741e-104">Resolve issues with shared mailboxes</span></span>

<span data-ttu-id="c741e-105">Si vous voyez des messages d’erreur lors de la création ou de l’utilisation d’une boîte aux lettres partagée, essayez ces solutions possibles.</span><span class="sxs-lookup"><span data-stu-id="c741e-105">If you see error messages when creating or using a shared mailbox, try these possible solutions.</span></span> 

## <a name="error-when-creating-shared-mailboxes"></a><span data-ttu-id="c741e-106">Erreur lors de la création de boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="c741e-106">Error when creating shared mailboxes</span></span>
<span data-ttu-id="c741e-107"><a name="bkmk_Fix"> </a></span><span class="sxs-lookup"><span data-stu-id="c741e-107"><a name="bkmk_Fix"> </a></span></span>

<span data-ttu-id="c741e-108">Si vous voyez le message d’erreur, l’adresse proxy « smtp:<nom de boîte aux lettres partagée » est déjà utilisée par les adresses proxy ou **\> LegacyExchangeDN de « \<name> ». Veuillez choisir une autre adresse proxy,** ce qui signifie que vous essayez de donner à la boîte aux lettres partagée un nom déjà utilisé.</span><span class="sxs-lookup"><span data-stu-id="c741e-108">If you see the error message, **The proxy address "smtp:<shared mailbox name\>" is already being used by the proxy addresses or LegacyExchangeDN of "\<name>". Please choose another proxy address**, it means you're trying to give the shared mailbox a name that's already in use.</span></span> <span data-ttu-id="c741e-109">Par exemple, imaginons que vous vouliez donner les noms info@domaine1 et info@domaine2 à des boîtes aux lettres partagées.</span><span class="sxs-lookup"><span data-stu-id="c741e-109">For example, let's say you want shared mailboxes named info@domain1 and info@domain2.</span></span> <span data-ttu-id="c741e-110">Il existe deux méthodes pour y parvenir :</span><span class="sxs-lookup"><span data-stu-id="c741e-110">There are two ways to do this:</span></span>

  - <span data-ttu-id="c741e-111">Utiliser Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c741e-111">Use Windows PowerShell.</span></span> <span data-ttu-id="c741e-112">Consultez ce billet de blog pour obtenir des instructions : Créer des boîtes aux lettres partagées [avec le même alias sur différents domaines](https://www.cogmotive.com/blog/office-365-tips/create-shared-mailboxes-with-same-alias-at-different-domains-in-office-365)</span><span class="sxs-lookup"><span data-stu-id="c741e-112">See this blog post for instructions: [Create Shared Mailboxes with Same Alias at Different Domains](https://www.cogmotive.com/blog/office-365-tips/create-shared-mailboxes-with-same-alias-at-different-domains-in-office-365)</span></span>
    
  - <span data-ttu-id="c741e-113">Nommez la deuxième boîte aux lettres partagée différemment du début pour contourner l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c741e-113">Name the second shared mailbox something different from the start to get around the error.</span></span> <span data-ttu-id="c741e-114">Ensuite, dans le Centre d’administration, renommez la boîte aux lettres partagée comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="c741e-114">Then in the admin center, rename the shared mailbox to what you want it to be.</span></span>

## <a name="error-about-not-having-send-permissions-when-using-a-shared-mailbox"></a><span data-ttu-id="c741e-115">Erreur de non-envoi d’autorisations lors de l’utilisation d’une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="c741e-115">Error about not having send permissions when using a shared mailbox</span></span>

<span data-ttu-id="c741e-116">Si vous avez créé une boîte aux lettres partagée, puis que vous essayez d’envoyer un message à partir de celle-ci, vous pouvez obtenir ceci :</span><span class="sxs-lookup"><span data-stu-id="c741e-116">If you created a shared mailbox and then try to send a message from it, you might get this:</span></span>

<span data-ttu-id="c741e-117">**Ce message n’a pas pu être envoyé. Vous n’êtes pas autorisé à envoyer le message au nom de l’utilisateur spécifié.**</span><span class="sxs-lookup"><span data-stu-id="c741e-117">**This message could not be sent. You do not have the permission to send the message on behalf of the specified user.**</span></span>

<span data-ttu-id="c741e-118">Ce message s’affiche Microsoft 365 rencontre un problème de latence de réplication.</span><span class="sxs-lookup"><span data-stu-id="c741e-118">This message appears when Microsoft 365 is experiencing a replication latency issue.</span></span> <span data-ttu-id="c741e-119">Il devrait disparaître dans une heure ou deux, lorsque les informations sur votre nouvelle boîte aux lettres partagée (ou utilisateur ajouté) sont répliquées dans tous nos centres de données.</span><span class="sxs-lookup"><span data-stu-id="c741e-119">It should go away in an hour or so, when the information about your new shared mailbox (or added user) is replicated across all of our data centers.</span></span> <span data-ttu-id="c741e-120">Patientez une heure, puis tentez à nouveau d’envoyer un message.</span><span class="sxs-lookup"><span data-stu-id="c741e-120">Wait an hour and then try again to send a message.</span></span>

## <a name="related-content"></a><span data-ttu-id="c741e-121">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="c741e-121">Related content</span></span>

<span data-ttu-id="c741e-122">[À propos des boîtes aux lettres partagées](about-shared-mailboxes.md) (article)</span><span class="sxs-lookup"><span data-stu-id="c741e-122">[About shared mailboxes](about-shared-mailboxes.md) (article)</span></span>\
<span data-ttu-id="c741e-123">[Créer une boîte aux lettres partagée](create-a-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="c741e-123">[Create a shared mailbox](create-a-shared-mailbox.md) (article)</span></span>\
<span data-ttu-id="c741e-124">[Configurer une boîte aux lettres partagée](configure-a-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="c741e-124">[Configure a shared mailbox](configure-a-shared-mailbox.md) (article)</span></span>\
<span data-ttu-id="c741e-125">[Convertir une boîte aux lettres utilisateur en boîte aux lettres partagée](convert-user-mailbox-to-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="c741e-125">[Convert a user mailbox to a shared mailbox](convert-user-mailbox-to-shared-mailbox.md) (article)</span></span>\
<span data-ttu-id="c741e-126">[Supprimer une licence d’une boîte aux lettres partagée](remove-license-from-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="c741e-126">[Remove a license from a shared mailbox](remove-license-from-shared-mailbox.md) (article)</span></span>


    


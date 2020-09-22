---
title: Flux de messagerie dans EOP
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: e109077e-cc85-4c19-ae40-d218ac7d0548
ms.custom:
- seo-marvel-apr2020
description: L’administrateur peut en savoir plus sur les options de configuration du flux de messagerie et du routage dans Exchange Online Protection (EOP).
ms.openlocfilehash: e1c821e3de8dd7dd18c192522bd18fd32a395dca
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48200702"
---
# <a name="mail-flow-in-eop"></a><span data-ttu-id="6ec44-103">Flux de messagerie dans EOP</span><span class="sxs-lookup"><span data-stu-id="6ec44-103">Mail flow in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="6ec44-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres Exchange Online ou des organisations Exchange Online (EOP) autonomes sans boîtes aux lettres Exchange Online, tous les messages envoyés à votre organisation passent par EOP avant que les utilisateurs ne les voient.</span><span class="sxs-lookup"><span data-stu-id="6ec44-104">In Microsoft 365 organizations with Exchange Online mailboxes, or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, all messages sent to your organization pass through EOP before your workers see them.</span></span> <span data-ttu-id="6ec44-105">Vous disposez d’options sur la façon de router les messages qui transitent par EOP pour les traiter avant de les acheminer vers vos boîtes de réception.</span><span class="sxs-lookup"><span data-stu-id="6ec44-105">You have options about how to route messages that pass through EOP for processing before they are routed to your worker inboxes.</span></span>

## <a name="working-with-messages-and-message-access-options"></a><span data-ttu-id="6ec44-106">Utilisation des messages et des options d’accès aux messages</span><span class="sxs-lookup"><span data-stu-id="6ec44-106">Working with messages and message access options</span></span>

<span data-ttu-id="6ec44-107">EOP offre une grande flexibilité dans le mode d’acheminement de vos messages.</span><span class="sxs-lookup"><span data-stu-id="6ec44-107">EOP offers flexibility in how your messages are routed.</span></span> <span data-ttu-id="6ec44-108">Les rubriques suivantes expliquent les étapes composant le processus de flux de messages.</span><span class="sxs-lookup"><span data-stu-id="6ec44-108">The following topics explain steps in the mail flow process.</span></span>

<span data-ttu-id="6ec44-109">[Utiliser le blocage du périmètre basé sur l’annuaire pour rejeter les messages envoyés à des destinataires non valides](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-directory-based-edge-blocking) Décrit la fonctionnalité de blocage du périmètre basée sur l’annuaire, qui vous permet de rejeter les messages pour les destinataires non valides au niveau du périmètre réseau du service.</span><span class="sxs-lookup"><span data-stu-id="6ec44-109">[Use Directory Based Edge Blocking to reject messages sent to invalid recipients](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-directory-based-edge-blocking) Describes the Directory Based Edge Blocking feature which lets you reject messages for invalid recipients at the service network perimeter.</span></span>

<span data-ttu-id="6ec44-110">La rubrique [View or Edit Managed Domains in EOP](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) décrit la façon de gérer les domaines associés à votre service EOP.</span><span class="sxs-lookup"><span data-stu-id="6ec44-110">[View or Edit Managed Domains in EOP](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) describes how to manage domains that are associated with your EOP service.</span></span>

<span data-ttu-id="6ec44-111">Si vous ajoutez des sous-domaines dans votre organisation, votre service EOP peut vous aider à les gérer aussi.</span><span class="sxs-lookup"><span data-stu-id="6ec44-111">If you add subdomains to your organization, your EOP service can help you manage these too.</span></span> <span data-ttu-id="6ec44-112">Pour en savoir plus sur les sous-domaines, consultez la rubrique [Enable mail Flow for subdomains in Exchange Online](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/enable-mail-flow-for-subdomains).</span><span class="sxs-lookup"><span data-stu-id="6ec44-112">Learn more about subdomains at [Enable mail flow for subdomains in Exchange Online](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/enable-mail-flow-for-subdomains).</span></span>

<span data-ttu-id="6ec44-113">[Configurer le flux de messagerie à l’aide de connecteurs](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) présente les connecteurs et explique comment vous pouvez les utiliser pour personnaliser le routage du courrier.</span><span class="sxs-lookup"><span data-stu-id="6ec44-113">[Configure mail flow using connectors](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) introduces connectors and shows how you can use them to customize mail routing.</span></span> <span data-ttu-id="6ec44-114">Les scénarios décrivent la procédure pour assurer une communication sécurisée avec une organisation partenaire et configurer un hôte actif.</span><span class="sxs-lookup"><span data-stu-id="6ec44-114">Scenarios include ensuring secure communication with a partner organization and setting up a smart host.</span></span>

<span data-ttu-id="6ec44-115">[Enhanced Filtering for Connectors](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors) indique comment configurer des connecteurs si votre courrier est acheminé vers un service ou un périphérique avant EOP.</span><span class="sxs-lookup"><span data-stu-id="6ec44-115">[Enhanced Filtering for Connectors](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors) describes how to configure connectors if your mail is routed to a service or device before EOP.</span></span>

<span data-ttu-id="6ec44-116">Dans les organisations EOP autonomes, vous devez effectuer quelques opérations de configuration pour vous assurer que le courrier indésirable est correctement routé vers le dossier de courrier indésirable de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6ec44-116">In standalone EOP organizations, you need to perform a couple configuration steps to ensure that junk email is routed correctly to each user's junk-email folder.</span></span> <span data-ttu-id="6ec44-117">Ces éléments sont détaillés dans [la configuration d’EOP autonome pour la remise du courrier indésirable dans le dossier courrier indésirable dans des environnements hybrides](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span><span class="sxs-lookup"><span data-stu-id="6ec44-117">These are detailed in [Configure standalone EOP to deliver spam to the Junk Email folder in hybrid environments](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span></span> <span data-ttu-id="6ec44-118">Si vous ne souhaitez pas déplacer les messages vers le dossier de courrier indésirable de chaque utilisateur, vous pouvez choisir une autre action en modifiant vos stratégies de blocage du courrier indésirable (également appelées stratégies de filtrage de contenu).</span><span class="sxs-lookup"><span data-stu-id="6ec44-118">If you do not want to move messages to each user's junk-email folder, you may choose another action by editing your anti-spam policies (also known as content filter policies).</span></span> <span data-ttu-id="6ec44-119">Pour plus d’informations, consultez [Configurer les stratégies anti-courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="6ec44-119">For more information, see [Configure anti-spam policies](configure-your-spam-filter-policies.md).</span></span>

## <a name="verify-mail-flow"></a><span data-ttu-id="6ec44-120">Vérifier le flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="6ec44-120">Verify mail flow</span></span>

<span data-ttu-id="6ec44-p106">Pour vérifier que votre configuration d'EOP, y compris celle de votre connecteur, fonctionne correctement, consultez la section « Comment savoir si cette tâche a fonctionné ? » dans la rubrique [Configurer votre service EOP](set-up-your-eop-service.md).</span><span class="sxs-lookup"><span data-stu-id="6ec44-p106">To verify that your EOP setup, including your connector configuration, is working correctly, see the "How do you know this task worked?" section in [Set up your EOP service](set-up-your-eop-service.md).</span></span>

<span data-ttu-id="6ec44-123">[Test du flux de messagerie en validant vos connecteurs Microsoft 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/test-mail-flow) fournit des instructions pour vérifier que votre flux de messagerie est correctement configuré.</span><span class="sxs-lookup"><span data-stu-id="6ec44-123">[Test mail flow by validating your Microsoft 365 connectors](https://docs.microsoft.com/exchange/mail-flow-best-practices/test-mail-flow) provides instructions for testing that your mail flow is set up correctly.</span></span>

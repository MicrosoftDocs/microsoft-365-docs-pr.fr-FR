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
localization_priority: Normal
ms.assetid: e109077e-cc85-4c19-ae40-d218ac7d0548
ms.custom:
- seo-marvel-apr2020
description: L’administrateur peut en savoir plus sur les options de configuration du flux de messagerie et du routage dans Exchange Online Protection (EOP).
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: c988f58a04abf2322e993ae1b75106a338674acb
ms.sourcegitcommit: 786f90a163d34c02b8451d09aa1efb1e1d5f543c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "50289650"
---
# <a name="mail-flow-in-eop"></a><span data-ttu-id="0e9e4-103">Flux de courriers dans EOP</span><span class="sxs-lookup"><span data-stu-id="0e9e4-103">Mail flow in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="0e9e4-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="0e9e4-104">**Applies to**</span></span>
- [<span data-ttu-id="0e9e4-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="0e9e4-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="0e9e4-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="0e9e4-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="0e9e4-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0e9e4-107">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

<span data-ttu-id="0e9e4-108">Dans les organisations Microsoft 365 avec boîtes aux lettres Exchange Online ou les organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, tous les messages envoyés à votre organisation passent par EOP avant que vos employés les voient.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-108">In Microsoft 365 organizations with Exchange Online mailboxes, or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, all messages sent to your organization pass through EOP before your workers see them.</span></span> <span data-ttu-id="0e9e4-109">Vous avez des options pour router les messages qui passent par EOP pour traitement avant qu’ils ne soient acheminés vers vos boîtes de réception de travail.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-109">You have options about how to route messages that pass through EOP for processing before they are routed to your worker inboxes.</span></span>

## <a name="working-with-messages-and-message-access-options"></a><span data-ttu-id="0e9e4-110">Utilisation des messages et des options d’accès aux messages</span><span class="sxs-lookup"><span data-stu-id="0e9e4-110">Working with messages and message access options</span></span>

<span data-ttu-id="0e9e4-111">EOP offre une flexibilité dans la façon dont vos messages sont acheminés.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-111">EOP offers flexibility in how your messages are routed.</span></span> <span data-ttu-id="0e9e4-112">Les rubriques suivantes expliquent les étapes composant le processus de flux de messages.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-112">The following topics explain steps in the mail flow process.</span></span>

<span data-ttu-id="0e9e4-113">[Utiliser le blocage du service Edge basé sur l’annuaire pour rejeter les messages envoyés à des destinataires non valides](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-directory-based-edge-blocking) Décrit la fonctionnalité de blocage du périmètre basé sur l’annuaire qui vous permet de rejeter les messages pour les destinataires non valides au niveau du périmètre du réseau de service.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-113">[Use Directory Based Edge Blocking to reject messages sent to invalid recipients](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-directory-based-edge-blocking) Describes the Directory Based Edge Blocking feature which lets you reject messages for invalid recipients at the service network perimeter.</span></span>

<span data-ttu-id="0e9e4-114">La rubrique [View or Edit Managed Domains in EOP](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) décrit la façon de gérer les domaines associés à votre service EOP.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-114">[View or Edit Managed Domains in EOP](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) describes how to manage domains that are associated with your EOP service.</span></span>

<span data-ttu-id="0e9e4-115">Si vous ajoutez des sous-domaines dans votre organisation, votre service EOP peut vous aider à les gérer aussi.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-115">If you add subdomains to your organization, your EOP service can help you manage these too.</span></span> <span data-ttu-id="0e9e4-116">En savoir plus sur les sous-domaine dans l’outil Activer le flux de messagerie pour les [sous-domaine dans Exchange Online.](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/enable-mail-flow-for-subdomains)</span><span class="sxs-lookup"><span data-stu-id="0e9e4-116">Learn more about subdomains at [Enable mail flow for subdomains in Exchange Online](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/enable-mail-flow-for-subdomains).</span></span>

<span data-ttu-id="0e9e4-117">[Configure mail flow using connectors](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) introduces connectors and shows how you can use them to customize mail routing.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-117">[Configure mail flow using connectors](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) introduces connectors and shows how you can use them to customize mail routing.</span></span> <span data-ttu-id="0e9e4-118">Les scénarios décrivent la procédure pour assurer une communication sécurisée avec une organisation partenaire et configurer un hôte actif.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-118">Scenarios include ensuring secure communication with a partner organization and setting up a smart host.</span></span>

<span data-ttu-id="0e9e4-119">[Le filtrage amélioré pour les connecteurs](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors) décrit comment configurer des connecteurs si votre courrier est acheminé vers un service ou un périphérique avant EOP.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-119">[Enhanced Filtering for Connectors](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors) describes how to configure connectors if your mail is routed to a service or device before EOP.</span></span>

<span data-ttu-id="0e9e4-120">Dans les organisations EOP autonomes, vous devez effectuer quelques étapes de configuration pour vous assurer que le courrier indésirable est correctement acheminé vers le dossier courrier indésirable de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-120">In standalone EOP organizations, you need to perform a couple configuration steps to ensure that junk email is routed correctly to each user's junk-email folder.</span></span> <span data-ttu-id="0e9e4-121">Ceux-ci sont détaillés dans Configurer EOP autonome pour remettre le courrier indésirable dans le dossier Courrier indésirable dans les [environnements hybrides.](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)</span><span class="sxs-lookup"><span data-stu-id="0e9e4-121">These are detailed in [Configure standalone EOP to deliver spam to the Junk Email folder in hybrid environments](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span></span> <span data-ttu-id="0e9e4-122">Si vous ne souhaitez pas déplacer des messages vers le dossier courrier indésirable de chaque utilisateur, vous pouvez choisir une autre action en éditant vos stratégies anti-courrier indésirable (également appelées stratégies de filtrage de contenu).</span><span class="sxs-lookup"><span data-stu-id="0e9e4-122">If you do not want to move messages to each user's junk-email folder, you may choose another action by editing your anti-spam policies (also known as content filter policies).</span></span> <span data-ttu-id="0e9e4-123">Pour plus d’informations, consultez [Configurer les stratégies anti-courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="0e9e4-123">For more information, see [Configure anti-spam policies](configure-your-spam-filter-policies.md).</span></span>

## <a name="verify-mail-flow"></a><span data-ttu-id="0e9e4-124">Vérifier le flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="0e9e4-124">Verify mail flow</span></span>

<span data-ttu-id="0e9e4-p106">Pour vérifier que votre configuration d'EOP, y compris celle de votre connecteur, fonctionne correctement, consultez la section « Comment savoir si cette tâche a fonctionné ? » dans la rubrique [Configurer votre service EOP](set-up-your-eop-service.md).</span><span class="sxs-lookup"><span data-stu-id="0e9e4-p106">To verify that your EOP setup, including your connector configuration, is working correctly, see the "How do you know this task worked?" section in [Set up your EOP service](set-up-your-eop-service.md).</span></span>

<span data-ttu-id="0e9e4-127">[Tester le flux de messagerie en validant vos connecteurs Microsoft 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/test-mail-flow) fournit des instructions pour tester que votre flux de messagerie est correctement installé.</span><span class="sxs-lookup"><span data-stu-id="0e9e4-127">[Test mail flow by validating your Microsoft 365 connectors](https://docs.microsoft.com/exchange/mail-flow-best-practices/test-mail-flow) provides instructions for testing that your mail flow is set up correctly.</span></span>

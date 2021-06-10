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
ms.openlocfilehash: 9636025796aee1ba2027edff38a16f131974134f
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52842493"
---
# <a name="mail-flow-in-eop"></a><span data-ttu-id="23332-103">Flux de courriers dans EOP</span><span class="sxs-lookup"><span data-stu-id="23332-103">Mail flow in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="23332-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="23332-104">**Applies to**</span></span>
- [<span data-ttu-id="23332-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="23332-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="23332-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="23332-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="23332-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="23332-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="23332-108">Dans Microsoft 365 organisations avec des boîtes aux lettres Exchange Online ou des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, tous les messages envoyés à votre organisation passent par EOP avant que vos employés ne les voient.</span><span class="sxs-lookup"><span data-stu-id="23332-108">In Microsoft 365 organizations with Exchange Online mailboxes, or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, all messages sent to your organization pass through EOP before your workers see them.</span></span> <span data-ttu-id="23332-109">Vous avez des options pour router les messages qui passent par EOP pour traitement avant qu’ils ne soient acheminés vers vos boîtes de réception de travail.</span><span class="sxs-lookup"><span data-stu-id="23332-109">You have options about how to route messages that pass through EOP for processing before they are routed to your worker inboxes.</span></span>

## <a name="working-with-messages-and-message-access-options"></a><span data-ttu-id="23332-110">Utilisation des messages et des options d’accès aux messages</span><span class="sxs-lookup"><span data-stu-id="23332-110">Working with messages and message access options</span></span>

<span data-ttu-id="23332-111">EOP offre une flexibilité dans la façon dont vos messages sont acheminés.</span><span class="sxs-lookup"><span data-stu-id="23332-111">EOP offers flexibility in how your messages are routed.</span></span> <span data-ttu-id="23332-112">Les rubriques suivantes expliquent les étapes composant le processus de flux de messages.</span><span class="sxs-lookup"><span data-stu-id="23332-112">The following topics explain steps in the mail flow process.</span></span>

<span data-ttu-id="23332-113">[Utiliser le blocage du service Edge basé sur l’annuaire pour rejeter les messages envoyés à des destinataires non valides](/exchange/mail-flow-best-practices/use-directory-based-edge-blocking) Décrit la fonctionnalité de blocage du périmètre basé sur l’annuaire qui vous permet de rejeter les messages pour les destinataires non valides au niveau du périmètre du réseau de service.</span><span class="sxs-lookup"><span data-stu-id="23332-113">[Use Directory Based Edge Blocking to reject messages sent to invalid recipients](/exchange/mail-flow-best-practices/use-directory-based-edge-blocking) Describes the Directory Based Edge Blocking feature which lets you reject messages for invalid recipients at the service network perimeter.</span></span>

<span data-ttu-id="23332-114">[L’affichage ou](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) la modification de domaines acceptés dans EOP décrit comment gérer les domaines associés à votre service EOP.</span><span class="sxs-lookup"><span data-stu-id="23332-114">[View or edit accepted domains in EOP](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) describes how to manage domains that are associated with your EOP service.</span></span>

<span data-ttu-id="23332-115">Si vous ajoutez des sous-domaines dans votre organisation, votre service EOP peut vous aider à les gérer aussi.</span><span class="sxs-lookup"><span data-stu-id="23332-115">If you add subdomains to your organization, your EOP service can help you manage these too.</span></span> <span data-ttu-id="23332-116">En savoir plus sur les sous-domaine dans [l’adresse Enable mail flow for subdomains in Exchange Online](/exchange/mail-flow-best-practices/manage-accepted-domains/enable-mail-flow-for-subdomains).</span><span class="sxs-lookup"><span data-stu-id="23332-116">Learn more about subdomains at [Enable mail flow for subdomains in Exchange Online](/exchange/mail-flow-best-practices/manage-accepted-domains/enable-mail-flow-for-subdomains).</span></span>

<span data-ttu-id="23332-117">[La configuration du flux de messagerie à l’aide de connecteurs](/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) introduit des connecteurs et vous montre comment vous pouvez les utiliser pour personnaliser le routage du courrier.</span><span class="sxs-lookup"><span data-stu-id="23332-117">[Configure mail flow using connectors](/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) introduces connectors and shows how you can use them to customize mail routing.</span></span> <span data-ttu-id="23332-118">Les scénarios décrivent la procédure pour assurer une communication sécurisée avec une organisation partenaire et configurer un hôte actif.</span><span class="sxs-lookup"><span data-stu-id="23332-118">Scenarios include ensuring secure communication with a partner organization and setting up a smart host.</span></span>

<span data-ttu-id="23332-119">[Le filtrage amélioré pour les connecteurs](/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors) décrit comment configurer des connecteurs si votre courrier est acheminé vers un service ou un périphérique avant EOP.</span><span class="sxs-lookup"><span data-stu-id="23332-119">[Enhanced Filtering for Connectors](/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors) describes how to configure connectors if your mail is routed to a service or device before EOP.</span></span>

<span data-ttu-id="23332-120">Dans les environnements hybrides où Exchange Online Protection protège les boîtes aux lettres Exchange locales, vous devez configurer des règles de flux de courrier (également appelées règles de transport) dans Exchange local pour traduire le verdict de filtrage de courrier indésirable Exchange Online Protection de sorte que la règle de courrier indésirable puisse déplacer le message vers le dossier Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="23332-120">In hybrid environments where EOP protects on-premises Exchange mailboxes, you need to configure mail flow rules (also known as transport rules) in on-premises Exchange to translate the EOP spam filtering verdict so the junk email rule can move the message to the Junk Email folder.</span></span> <span data-ttu-id="23332-121">Pour les détails, voir [Configurer Exchange Online Protection (EOP) pour envoyer des courriers indésirables dans le dossier Courrier indésirable dans les environnements hybrides](/exchange/standalone-eop/configure-eop-spam-protection-hybrid).</span><span class="sxs-lookup"><span data-stu-id="23332-121">For details, see [Configure EOP to deliver spam to the Junk Email folder in hybrid environments](/exchange/standalone-eop/configure-eop-spam-protection-hybrid).</span></span> <span data-ttu-id="23332-122">Si vous ne souhaitez pas déplacer des messages vers le dossier Courrier indésirable de chaque utilisateur, vous pouvez choisir une autre action en éditant vos stratégies anti-courrier indésirable (également appelées stratégies de filtrage de contenu).</span><span class="sxs-lookup"><span data-stu-id="23332-122">If you don't  want to move messages to each user's Junk Email folder, you may choose another action by editing your anti-spam policies (also known as content filter policies).</span></span> <span data-ttu-id="23332-123">Pour plus d’informations, consultez [Configurer les stratégies anti-courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="23332-123">For more information, see [Configure anti-spam policies](configure-your-spam-filter-policies.md).</span></span>

## <a name="verify-mail-flow"></a><span data-ttu-id="23332-124">Vérifier le flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="23332-124">Verify mail flow</span></span>

<span data-ttu-id="23332-p106">Pour vérifier que votre configuration d'EOP, y compris celle de votre connecteur, fonctionne correctement, consultez la section « Comment savoir si cette tâche a fonctionné ? » dans la rubrique [Configurer votre service EOP](/exchange/standalone-eop/set-up-your-eop-service).</span><span class="sxs-lookup"><span data-stu-id="23332-p106">To verify that your EOP setup, including your connector configuration, is working correctly, see the "How do you know this task worked?" section in [Set up your EOP service](/exchange/standalone-eop/set-up-your-eop-service).</span></span>

<span data-ttu-id="23332-127">[Testez le flux de messagerie en validant Microsoft 365 connecteurs](/exchange/mail-flow-best-practices/test-mail-flow) de messagerie fournit des instructions pour tester que votre flux de messagerie est correctement installé.</span><span class="sxs-lookup"><span data-stu-id="23332-127">[Test mail flow by validating your Microsoft 365 connectors](/exchange/mail-flow-best-practices/test-mail-flow) provides instructions for testing that your mail flow is set up correctly.</span></span>

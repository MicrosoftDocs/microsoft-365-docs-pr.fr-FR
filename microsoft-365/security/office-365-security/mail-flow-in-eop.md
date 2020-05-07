---
title: Flux de messagerie dans EOP
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: e109077e-cc85-4c19-ae40-d218ac7d0548
ms.custom:
- seo-marvel-apr2020
description: Dans cet article, les clients Exchange Online Protection (EOP) peuvent en savoir plus sur la configuration du routage de courrier personnalisé qui peut être conforme aux exigences de l’entreprise.
ms.openlocfilehash: cdc919c628f2254ffc971678f7887c37786d2528
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44034231"
---
# <a name="mail-flow-in-eop"></a><span data-ttu-id="0ef29-103">Flux de messagerie dans EOP</span><span class="sxs-lookup"><span data-stu-id="0ef29-103">Mail flow in EOP</span></span>

<span data-ttu-id="0ef29-p101">Étant donné que vous êtes client Exchange Online Protection (EOP), tous les messages envoyés à votre organisation transitent par EOP avant que vos collaborateurs ne les voient. Que vous hébergiez l'ensemble de vos boîtes aux lettres dans le nuage avec Exchange Online ou localement (scénario dit autonome) pour éventuellement continuer à tirer parti de votre infrastructure existante, vous avez plusieurs possibilités de router les messages qui transiteront par EOP dans le cadre de leur traitement avant qu'ils ne soient acheminés vers les boîtes de réception de vos collaborateurs.</span><span class="sxs-lookup"><span data-stu-id="0ef29-p101">As an Exchange Online Protection (EOP) customer, all messages sent to your organization pass through EOP before your workers see them. Whether you host all of your mailboxes in the cloud with Exchange Online, or you host your mailboxes on premises (called a standalone scenario), perhaps to continue taking advantage of your existing infrastructure, you have options about how to route messages that will pass through EOP for processing before they are routed to your worker inboxes.</span></span>

<span data-ttu-id="0ef29-p102">Vous pouvez personnaliser le routage des messages pour que votre messagerie réponde à vos besoins métiers. Par exemple, vous avez la possibilité d'utiliser un équipement de filtrage de stratégie pour tous vos messages sortants.</span><span class="sxs-lookup"><span data-stu-id="0ef29-p102">You may want to configure custom mail routing to conform your messaging to a business requirement. For instance, you can pass all of your outbound mail through a policy-filtering appliance.</span></span>

## <a name="working-with-messages-and-message-access-options"></a><span data-ttu-id="0ef29-108">Utilisation des messages et des options d’accès aux messages</span><span class="sxs-lookup"><span data-stu-id="0ef29-108">Working with messages and message access options</span></span>

<span data-ttu-id="0ef29-p103">EOP vous propose plusieurs possibilités de router vos messages en toute flexibilité. Les rubriques suivantes expliquent les étapes composant le processus de flux de messages.</span><span class="sxs-lookup"><span data-stu-id="0ef29-p103">EOP offers a lot of flexibility in how your messages are routed. The following topics explain steps in the mail flow process.</span></span>

<span data-ttu-id="0ef29-111">[Utiliser le blocage du périmètre basé sur l’annuaire pour rejeter les messages envoyés à des destinataires non valides](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-directory-based-edge-blocking) Décrit la fonctionnalité de blocage du périmètre basée sur l’annuaire, qui vous permet de rejeter les messages pour les destinataires non valides au niveau du périmètre réseau du service.</span><span class="sxs-lookup"><span data-stu-id="0ef29-111">[Use Directory Based Edge Blocking to reject messages sent to invalid recipients](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-directory-based-edge-blocking) Describes the Directory Based Edge Blocking feature which lets you reject messages for invalid recipients at the service network perimeter.</span></span>

<span data-ttu-id="0ef29-112">La rubrique [View or Edit Managed Domains in EOP](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) décrit la façon de gérer les domaines associés à votre service EOP.</span><span class="sxs-lookup"><span data-stu-id="0ef29-112">[View or Edit Managed Domains in EOP](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) describes how to manage domains that are associated with your EOP service.</span></span>

<span data-ttu-id="0ef29-113">Si vous ajoutez des sous-domaines dans votre organisation, votre service EOP peut vous aider à les gérer aussi.</span><span class="sxs-lookup"><span data-stu-id="0ef29-113">If you add subdomains to your organization, your EOP service can help you manage these too.</span></span> <span data-ttu-id="0ef29-114">Pour en savoir plus sur les sous-domaines, consultez la rubrique [Enable mail Flow for subdomains in Exchange Online](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/enable-mail-flow-for-subdomains).</span><span class="sxs-lookup"><span data-stu-id="0ef29-114">Learn more about subdomains at [Enable mail flow for subdomains in Exchange Online](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/enable-mail-flow-for-subdomains).</span></span>

<span data-ttu-id="0ef29-p105">La rubrique [Configure mail flow using connectors in Office 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) présente les connecteurs et explique comment vous pouvez les utiliser pour personnaliser le routage des messages. Les scénarios décrivent la procédure pour assurer une communication sécurisée avec une organisation partenaire et configurer un hôte actif.</span><span class="sxs-lookup"><span data-stu-id="0ef29-p105">[Configure mail flow using connectors in Office 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) introduces connectors and shows how you can use them to customize mail routing. Scenarios include ensuring secure communication with a partner organization and setting up a smart host.</span></span>

<span data-ttu-id="0ef29-117">Vous pouvez vous assurer que le courrier indésirable est correctement routé vers le dossier Courrier indésirable de chaque utilisateur en effectuant quelques opérations de configuration.</span><span class="sxs-lookup"><span data-stu-id="0ef29-117">To ensure that junk email is routed correctly to each user's junk-email folder, you must perform a couple configuration steps.</span></span> <span data-ttu-id="0ef29-118">Ces éléments sont détaillés dans [la configuration d’EOP autonome pour la remise du courrier indésirable dans le dossier courrier indésirable dans des environnements hybrides](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span><span class="sxs-lookup"><span data-stu-id="0ef29-118">These are detailed in [Configure standalone EOP to deliver spam to the Junk Email folder in hybrid environments](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span></span> <span data-ttu-id="0ef29-119">Si vous ne souhaitez pas déplacer les messages vers le dossier Courrier indésirable de chaque utilisateur, vous pouvez choisir une autre action en modifiant vos stratégies de filtrage de contenu dans le Centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ef29-119">If you do not want to move messages to each user's junk-email folder, you may choose another action by editing your content filter policies in the Exchange admin center.</span></span> <span data-ttu-id="0ef29-120">Pour plus d’informations, consultez [Configurer les stratégies anti-courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="0ef29-120">For more information, see [Configure anti-spam policies](configure-your-spam-filter-policies.md).</span></span>

## <a name="verify-mail-flow"></a><span data-ttu-id="0ef29-121">Vérifier le flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="0ef29-121">Verify mail flow</span></span>

<span data-ttu-id="0ef29-p107">Pour vérifier que votre configuration d'EOP, y compris celle de votre connecteur, fonctionne correctement, consultez la section « Comment savoir si cette tâche a fonctionné ? » dans la rubrique [Configurer votre service EOP](set-up-your-eop-service.md).</span><span class="sxs-lookup"><span data-stu-id="0ef29-p107">To verify that your EOP setup, including your connector configuration, is working correctly, see the "How do you know this task worked?" section in [Set up your EOP service](set-up-your-eop-service.md).</span></span>

<span data-ttu-id="0ef29-124">[Test du flux de messagerie en validant vos connecteurs Microsoft 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/test-mail-flow) fournit des instructions pour vérifier que votre flux de messagerie est correctement configuré.</span><span class="sxs-lookup"><span data-stu-id="0ef29-124">[Test mail flow by validating your Microsoft 365 connectors](https://docs.microsoft.com/exchange/mail-flow-best-practices/test-mail-flow) provides instructions for testing that your mail flow is set up correctly.</span></span>

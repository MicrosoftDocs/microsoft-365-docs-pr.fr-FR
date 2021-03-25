---
title: À propos du rôle d’administrateur Exchange Online
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: scotv
audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: 097ae285-c4af-4319-9770-e2559d66e4c8
description: 'Les administrateurs Exchange Online gèrent la messagerie et les boîtes aux lettres de votre organisation. Par exemple, ils récupèrent les éléments supprimés dans la boîte aux lettres d’un utilisateur. '
ms.openlocfilehash: 4dc1f435571650ae4a805198782c3c24a92024fb
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51197648"
---
# <a name="about-the-exchange-online-admin-role"></a><span data-ttu-id="3419a-104">À propos du rôle d’administrateur Exchange Online</span><span class="sxs-lookup"><span data-stu-id="3419a-104">About the Exchange Online admin role</span></span>

<span data-ttu-id="3419a-105">Pour vous aider à administrer Microsoft [](assign-admin-roles.md) 365, vous pouvez attribuer aux utilisateurs des autorisations pour gérer le courrier électronique et les boîtes aux lettres de votre organisation à partir du Centre d’administration [Exchange.](/exchange/exchange-admin-center)</span><span class="sxs-lookup"><span data-stu-id="3419a-105">To help you administer Microsoft 365, you can [assign](assign-admin-roles.md) users permissions to manage your organization's email and mailboxes from the [Exchange admin center](/exchange/exchange-admin-center).</span></span> <span data-ttu-id="3419a-106">Pour ce faire, attribuez-leur le rôle d’administrateur Exchange.</span><span class="sxs-lookup"><span data-stu-id="3419a-106">You do this by assigning them to the Exchange admin role.</span></span>
  
 <span data-ttu-id="3419a-107">**Conseil**: lorsque vous attribuez une personne au rôle d’administrateur Exchange, attribuez-lui également le rôle d’administrateur de service.</span><span class="sxs-lookup"><span data-stu-id="3419a-107">**Tip**: When you assign someone to the Exchange admin role, also assign them to the Service admin role.</span></span> <span data-ttu-id="3419a-108">De cette façon, ils peuvent voir des informations importantes dans le Centre d’administration Microsoft 365, telles que l’état d’état du service Exchange Online, ainsi que les notifications de modification et de publication.</span><span class="sxs-lookup"><span data-stu-id="3419a-108">This way they can see important information in the Microsoft 365 admin center, such as the health of the Exchange Online service, and change and release notifications.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="3419a-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="3419a-109">Before you begin</span></span>

<span data-ttu-id="3419a-110">Voici quelques-unes des tâches clés que les utilisateurs peuvent effectuer lorsqu’ils sont affectés au rôle d’administrateur Exchange :</span><span class="sxs-lookup"><span data-stu-id="3419a-110">Here are some of the key tasks users can do when they are assigned to the Exchange admin role:</span></span>
  
- [<span data-ttu-id="3419a-111">Récupérer des éléments supprimés dans une boîte aux lettres utilisateur - Aide aux administrateurs</span><span class="sxs-lookup"><span data-stu-id="3419a-111">Recover deleted items in a user mailbox - Admin Help</span></span>](/Exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages)

- <span data-ttu-id="3419a-112">[Configurer une stratégie d’archivage et de suppression pour les boîtes aux lettres de votre organisation.](../../compliance/set-up-an-archive-and-deletion-policy-for-mailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="3419a-112">[Set up an archive and deletion policy for mailboxes in your organization](../../compliance/set-up-an-archive-and-deletion-policy-for-mailboxes.md).</span></span>

- <span data-ttu-id="3419a-113">Configurer des fonctionnalités de boîte aux lettres telles que la stratégie de partage de boîte aux lettres : comment les utilisateurs peuvent partager des informations de calendrier et de contacts avec d’autres personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3419a-113">Set up mailbox features such as the mailbox sharing policy: how users can share calendar and contacts information with others outside of your organization.</span></span>

- <span data-ttu-id="3419a-114">Configurer les[délégués](give-mailbox-permissions-to-another-user.md#send-email-from-another-users-mailbox)« Envoyer en tant que » et « Envoyer de[la part de](give-mailbox-permissions-to-another-user.md#send-email-on-behalf-of-another-user)» pour la boîte aux lettres d’une personne.</span><span class="sxs-lookup"><span data-stu-id="3419a-114">Set up "[Send as](give-mailbox-permissions-to-another-user.md#send-email-from-another-users-mailbox)" and "[Send on behalf](give-mailbox-permissions-to-another-user.md#send-email-on-behalf-of-another-user)" delegates for someone's mailbox.</span></span> <span data-ttu-id="3419a-115">Par exemple, un dirigeant souhaitera que son assistant(e) ait la possibilité d’envoyer des messages en son nom.</span><span class="sxs-lookup"><span data-stu-id="3419a-115">For example, an executive may want their assistant to have the ability to send mail on their behalf.</span></span>

- <span data-ttu-id="3419a-116">[Créez une boîte aux lettres partagée](../email/create-a-shared-mailbox.md) pour qu’un groupe de personnes puisse surveiller et envoyer des messages électroniques à partir d’une adresse de messagerie commune.</span><span class="sxs-lookup"><span data-stu-id="3419a-116">[Create a shared mailbox](../email/create-a-shared-mailbox.md) so a group of people can monitor and send email from a common email address.</span></span>

- <span data-ttu-id="3419a-117">Protection contre le courrier indésirable et filtres [anti-programme](https://docs.microsoft.com/microsoft-365/security/office-365-security/anti-spam-protection) malveillant pour l’organisation.</span><span class="sxs-lookup"><span data-stu-id="3419a-117">[Email anti-spam protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/anti-spam-protection) and malware filters for the organization.</span></span>

- <span data-ttu-id="3419a-118">Gestion des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3419a-118">Manage Microsoft 365 groups</span></span>

## <a name="exchange-online-role-groups"></a><span data-ttu-id="3419a-119">Groupes de rôles Exchange Online</span><span class="sxs-lookup"><span data-stu-id="3419a-119">Exchange Online role groups</span></span>

<span data-ttu-id="3419a-120">Si vous avez une grande organisation, l’administrateur Exchange peut affecter des utilisateurs à des groupes de rôles Exchange.</span><span class="sxs-lookup"><span data-stu-id="3419a-120">If you have a large organization, the Exchange admin might want to assign users to Exchange role groups.</span></span> <span data-ttu-id="3419a-121">Lorsqu’un administrateur ajoute un utilisateur à un groupe de rôles, l’utilisateur obtient les autorisations pour effectuer certaines fonctions professionnelles que seuls les membres de ce groupe peuvent faire.</span><span class="sxs-lookup"><span data-stu-id="3419a-121">When an admin adds a user to a role group, the user gets permissions to perform certain business functions only members of that group can do.</span></span>
  
 <span data-ttu-id="3419a-122">Par exemple, l’administrateur Exchange peut affecter une personne au groupe de rôles Gestion de la découverte afin qu’elle puisse effectuer des recherches de données dans les boîtes aux lettres qui répondent à certains critères.</span><span class="sxs-lookup"><span data-stu-id="3419a-122">For example, the Exchange admin might assign someone to the Discovery Management role group so they can perform searches of mailboxes for data that meets certain criteria.</span></span> <span data-ttu-id="3419a-123">Pour plus d’informations, [voir Autorisations dans Exchange Online et](/exchange/permissions-exo/permissions-exo) Gérer les groupes de [rôles.](/exchange/manage-role-groups-exchange-2013-help)</span><span class="sxs-lookup"><span data-stu-id="3419a-123">To learn more, see [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo) and [Manage Role Groups](/exchange/manage-role-groups-exchange-2013-help).</span></span>
  
## <a name="learn-about-other-admin-roles"></a><span data-ttu-id="3419a-124">En savoir plus sur les autres rôles d’administrateur</span><span class="sxs-lookup"><span data-stu-id="3419a-124">Learn about other admin roles</span></span>

- [<span data-ttu-id="3419a-125">À propos des rôles d’administrateur Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3419a-125">About Microsoft 365 admin roles</span></span>](about-admin-roles.md)

- [<span data-ttu-id="3419a-126">À propos du rôle d'administrateur SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3419a-126">About the SharePoint Online admin role</span></span>](/sharepoint/sharepoint-admin-role)

- [<span data-ttu-id="3419a-127">À propos du rôle d’administrateur Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="3419a-127">About the Skype for Business admin role</span></span>](/skypeforbusiness/skype-for-business-online)

- [<span data-ttu-id="3419a-128">Utiliser le rôle d’administrateur Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="3419a-128">Use Microsoft Teams admin role</span></span>](/MicrosoftTeams/using-admin-roles)
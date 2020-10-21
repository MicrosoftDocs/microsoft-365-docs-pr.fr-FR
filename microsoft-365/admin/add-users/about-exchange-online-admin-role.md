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
description: 'Les administrateurs Exchange Online gèrent les courriers électroniques et les boîtes aux lettres de votre organisation. Par exemple, ils récupèrent les éléments supprimés dans la boîte aux lettres d’un utilisateur. '
ms.openlocfilehash: cd2c4c10554cbaf425fa6ae9156a8ceeb1a21503
ms.sourcegitcommit: 628f195cbe3c00910f7350d8b09997a675dde989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "48646702"
---
# <a name="about-the-exchange-online-admin-role"></a><span data-ttu-id="eb0b0-104">À propos du rôle d’administrateur Exchange Online</span><span class="sxs-lookup"><span data-stu-id="eb0b0-104">About the Exchange Online admin role</span></span>

<span data-ttu-id="eb0b0-105">Pour vous aider à administrer Microsoft 365, vous pouvez [attribuer](assign-admin-roles.md) aux utilisateurs des autorisations pour gérer les courriers électroniques et les boîtes aux lettres de votre organisation à partir du [Centre d’administration Exchange](https://go.microsoft.com/fwlink/p/?LinkID=271807).</span><span class="sxs-lookup"><span data-stu-id="eb0b0-105">To help you administer Microsoft 365, you can [assign](assign-admin-roles.md) users permissions to manage your organization's email and mailboxes from the [Exchange admin center](https://go.microsoft.com/fwlink/p/?LinkID=271807).</span></span> <span data-ttu-id="eb0b0-106">Pour ce faire, attribuez-leur le rôle d’administrateur Exchange.</span><span class="sxs-lookup"><span data-stu-id="eb0b0-106">You do this by assigning them to the Exchange admin role.</span></span>
  
 <span data-ttu-id="eb0b0-107">**Conseil**: lorsque vous affectez une personne au rôle d’administrateur Exchange, affectez-lui également le rôle d’administrateur de service.</span><span class="sxs-lookup"><span data-stu-id="eb0b0-107">**Tip**: When you assign someone to the Exchange admin role, also assign them to the Service admin role.</span></span> <span data-ttu-id="eb0b0-108">De cette façon, ils peuvent voir des informations importantes dans le centre d’administration 365 de Microsoft, telles que l’intégrité du service Exchange Online, et modifier et publier des notifications.</span><span class="sxs-lookup"><span data-stu-id="eb0b0-108">This way they can see important information in the Microsoft 365 admin center, such as the health of the Exchange Online service, and change and release notifications.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="eb0b0-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="eb0b0-109">Before you begin</span></span>

<span data-ttu-id="eb0b0-110">Voici quelques-unes des tâches clés que les utilisateurs peuvent effectuer lorsqu’ils sont affectés au rôle d’administrateur Exchange :</span><span class="sxs-lookup"><span data-stu-id="eb0b0-110">Here are some of the key tasks users can do when they are assigned to the Exchange admin role:</span></span>
  
- [<span data-ttu-id="eb0b0-111">Récupérer des éléments supprimés dans une boîte aux lettres utilisateur - Aide aux administrateurs</span><span class="sxs-lookup"><span data-stu-id="eb0b0-111">Recover deleted items in a user mailbox - Admin Help</span></span>](https://docs.microsoft.com/microsoft-365/enterprise/recover-deleted-items-in-a-mailbox)

- <span data-ttu-id="eb0b0-112">[Configurez une stratégie d’archivage et de suppression pour les boîtes aux lettres de votre organisation](https://docs.microsoft.com/microsoft-365/compliance/set-up-an-archive-and-deletion-policy-for-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="eb0b0-112">[Set up an archive and deletion policy for mailboxes in your organization](https://docs.microsoft.com/microsoft-365/compliance/set-up-an-archive-and-deletion-policy-for-mailboxes).</span></span>

- <span data-ttu-id="eb0b0-113">Configurez des fonctionnalités de boîte aux lettres, telles que la stratégie de partage de boîtes aux lettres : comment les utilisateurs peuvent partager des informations de calendrier et de contacts avec d’autres personnes en dehors de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="eb0b0-113">Set up mailbox features such as the mailbox sharing policy: how users can share calendar and contacts information with others outside of your organization.</span></span>

- <span data-ttu-id="eb0b0-114">Configurer les délégués «[Envoyer en tant que](give-mailbox-permissions-to-another-user.md#send-email-from-another-users-mailbox)» et «[Envoyer sur abehalf](give-mailbox-permissions-to-another-user.md#send-email-on-behalf-of-another-user)» pour la boîte aux lettres d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eb0b0-114">Set up "[Send as](give-mailbox-permissions-to-another-user.md#send-email-from-another-users-mailbox)" and "[Send on abehalf](give-mailbox-permissions-to-another-user.md#send-email-on-behalf-of-another-user)" delegates for someone's mailbox.</span></span> <span data-ttu-id="eb0b0-115">Par exemple, un dirigeant souhaitera que son assistant(e) ait la possibilité d’envoyer des messages en son nom.</span><span class="sxs-lookup"><span data-stu-id="eb0b0-115">For example, an executive may want their assistant to have the ability to send mail on their behalf.</span></span>

- <span data-ttu-id="eb0b0-116">[Créez une boîte aux lettres partagée](../email/create-a-shared-mailbox.md) pour permettre à un groupe de personnes de surveiller et d’envoyer des courriers électroniques à partir d’une adresse de messagerie commune.</span><span class="sxs-lookup"><span data-stu-id="eb0b0-116">[Create a shared mailbox](../email/create-a-shared-mailbox.md) so a group of people can monitor and send email from a common email address.</span></span>

- <span data-ttu-id="eb0b0-117">Filtres de protection contre le [courrier indésirable](https://docs.microsoft.com/microsoft-365/security/office-365-security/anti-spam-protection) et de programmes malveillants pour l’organisation.</span><span class="sxs-lookup"><span data-stu-id="eb0b0-117">[Email anti-spam protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/anti-spam-protection) and malware filters for the organization.</span></span>

- <span data-ttu-id="eb0b0-118">Gestion des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="eb0b0-118">Manage Microsoft 365 groups</span></span>

## <a name="exchange-online-role-groups"></a><span data-ttu-id="eb0b0-119">Groupes de rôles Exchange Online</span><span class="sxs-lookup"><span data-stu-id="eb0b0-119">Exchange Online role groups</span></span>

<span data-ttu-id="eb0b0-120">Si vous avez une organisation de grande taille, l’administrateur Exchange peut souhaiter affecter des utilisateurs à des groupes de rôles Exchange.</span><span class="sxs-lookup"><span data-stu-id="eb0b0-120">If you have a large organization, the Exchange admin might want to assign users to Exchange role groups.</span></span> <span data-ttu-id="eb0b0-121">Lorsqu’un administrateur ajoute un utilisateur à un groupe de rôles, il obtient des autorisations pour effectuer certaines fonctions professionnelles que les membres de ce groupe peuvent faire.</span><span class="sxs-lookup"><span data-stu-id="eb0b0-121">When an admin adds a user to a role group, the user gets permissions to perform certain business functions only members of that group can do.</span></span>
  
 <span data-ttu-id="eb0b0-122">Par exemple, l’administrateur Exchange peut affecter quelqu’un au groupe de rôles gestion de la découverte afin qu’il puisse effectuer des recherches de boîtes aux lettres pour des données répondant à certains critères.</span><span class="sxs-lookup"><span data-stu-id="eb0b0-122">For example, the Exchange admin might assign someone to the Discovery Management role group so they can perform searches of mailboxes for data that meets certain criteria.</span></span> <span data-ttu-id="eb0b0-123">Pour plus d’informations, consultez la rubrique [autorisations dans Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo) et [gérer les groupes de rôles](https://docs.microsoft.com/exchange/manage-role-groups-exchange-2013-help).</span><span class="sxs-lookup"><span data-stu-id="eb0b0-123">To learn more, see [Permissions in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo) and [Manage Role Groups](https://docs.microsoft.com/exchange/manage-role-groups-exchange-2013-help).</span></span>
  
## <a name="learn-about-other-admin-role"></a><span data-ttu-id="eb0b0-124">En savoir plus sur les autres rôles d’administrateur</span><span class="sxs-lookup"><span data-stu-id="eb0b0-124">Learn about other admin role</span></span>

- [<span data-ttu-id="eb0b0-125">À propos des rôles d’administrateur Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="eb0b0-125">About Microsoft 365 admin roles</span></span>](about-admin-roles.md)

- [<span data-ttu-id="eb0b0-126">À propos du rôle d'administrateur SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="eb0b0-126">About the SharePoint Online admin role</span></span>](https://docs.microsoft.com/sharepoint/sharepoint-admin-role)

- [<span data-ttu-id="eb0b0-127">À propos du rôle d’administrateur Skype entreprise</span><span class="sxs-lookup"><span data-stu-id="eb0b0-127">About the Skype for Business admin role</span></span>](https://docs.microsoft.com/skypeforbusiness/skype-for-business-online)

- [<span data-ttu-id="eb0b0-128">Utiliser le rôle d’administrateur de Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="eb0b0-128">Use Microsoft Teams admin role</span></span>](https://docs.microsoft.com/MicrosoftTeams/using-admin-roles) 
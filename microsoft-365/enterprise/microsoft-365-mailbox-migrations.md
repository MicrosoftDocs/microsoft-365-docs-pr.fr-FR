---
title: Migrations de boîtes aux lettres Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
f1.keywords:
- NOCSH
description: Cet article contient un bref résumé des migrations de boîtes aux lettres Microsoft 365 et une liste des applets de commande utilisées pour les migrations.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 63080643e4994d6b16e77298907725a827997cef
ms.sourcegitcommit: 27daadad9ca0f02a833ff3cff8a574551b9581da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2020
ms.locfileid: "47546797"
---
# <a name="microsoft-365-mailbox-migrations"></a><span data-ttu-id="eca39-103">Migrations de boîtes aux lettres Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="eca39-103">Microsoft 365 mailbox migrations</span></span>

<span data-ttu-id="eca39-104">Avec un déploiement hybride basé sur Exchange, les clients peuvent choisir de déplacer des boîtes aux lettres Exchange locales vers une organisation [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) ou de déplacer des boîtes aux lettres Exchange Online vers une organisation [Exchange locale](https://docs.microsoft.com/Exchange/exchange-server) .</span><span class="sxs-lookup"><span data-stu-id="eca39-104">With an Exchange-based hybrid deployment, customers can choose to either move on-premises Exchange mailboxes to an [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) organization or move Exchange Online mailboxes to an [Exchange on-premises](https://docs.microsoft.com/Exchange/exchange-server) organization.</span></span> <span data-ttu-id="eca39-105">Les lots de migration sont utilisés lors du déplacement de boîtes aux lettres entre des organisations locales et Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="eca39-105">Migration batches are used when moving mailboxes between on-premises and Exchange Online organizations.</span></span>

<span data-ttu-id="eca39-106">Les clients peuvent consulter les statistiques et d’autres informations sur les migrations de boîtes aux lettres avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="eca39-106">Customers can review statistics and other information about mailbox migrations with the following cmdlets:</span></span>

- <span data-ttu-id="eca39-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/get-moverequeststatistics): fournit des statistiques par défaut pour une boîte aux lettres d’utilisateur, qui inclut l’État, la taille de boîte aux lettres, la taille de boîte aux lettres d’archivage et le pourcentage d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="eca39-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/get-moverequeststatistics): Provides default statistics for a user mailbox, which includes the status, mailbox size, archive mailbox size, and percentage complete.</span></span>
- <span data-ttu-id="eca39-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox
): fournit une liste récapitulative des objets et des attributs de boîte aux lettres dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="eca39-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox
): Provides a summary list of mailbox objects and attributes in the organization.</span></span>
- <span data-ttu-id="eca39-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/get-recipient): fournit une liste des objets à extension messagerie existants, tels que les boîtes aux lettres, les utilisateurs de messagerie, les contacts et les groupes de distribution.</span><span class="sxs-lookup"><span data-stu-id="eca39-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/get-recipient): Provides a list of existing mail-enabled objects such as mailboxes, mail users, contacts, and distribution groups.</span></span>
- <span data-ttu-id="eca39-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/get-moverequest): fournit un état détaillé de la migration de boîte aux lettres en cours.</span><span class="sxs-lookup"><span data-stu-id="eca39-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/get-moverequest): Provides a detailed status of an ongoing mailbox migration.</span></span>
- <span data-ttu-id="eca39-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/get-migrationuser): fournit des informations sur les utilisateurs de migration et de déplacement de boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="eca39-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/get-migrationuser): Provides information about the mailbox move and migration users.</span></span>
- <span data-ttu-id="eca39-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/get-migrationbatch): fournit des informations sur l’état du lot de migration actuel.</span><span class="sxs-lookup"><span data-stu-id="eca39-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/get-migrationbatch): Provides information on the status of current migration batch.</span></span>
- <span data-ttu-id="eca39-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/get-migrationuserstatistics): fournit des informations détaillées sur l’état de la migration pour un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="eca39-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/get-migrationuserstatistics): Provides detailed information about the migration status for a specific user.</span></span>
- <span data-ttu-id="eca39-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/get-mailboxstatistics): fournit des informations sur les boîtes aux lettres, telles que la taille, le nombre de messages et l’heure du dernier accès.</span><span class="sxs-lookup"><span data-stu-id="eca39-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/get-mailboxstatistics): Provides information about mailboxes, such as size, the number of messages, and the last accessed time.</span></span>

<span data-ttu-id="eca39-115">Pour plus d’informations sur les applets de commande, voir [Move and migration cmdlets in Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="eca39-115">For more information about cmdlets, see [Move and Migration cmdlets in Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell).</span></span>

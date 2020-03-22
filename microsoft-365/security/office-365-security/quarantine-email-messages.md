---
title: Mise en quarantaine dans Office 365
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 4c234874-015e-4768-8495-98fcccfc639b
ms.collection:
- M365-security-compliance
description: La mise en quarantaine dans Office 365 contient des messages potentiellement dangereux ou indésirables. Les administrateurs et les utilisateurs finaux peuvent accéder à la mise en quarantaine.
ms.openlocfilehash: 29f9fcbed83e9019118bb8b37c19cad1199c4c45
ms.sourcegitcommit: fce0d5cad32ea60a08ff001b228223284710e2ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2020
ms.locfileid: "42895298"
---
# <a name="quarantine-in-office-365"></a><span data-ttu-id="58046-104">Mise en quarantaine dans Office 365</span><span class="sxs-lookup"><span data-stu-id="58046-104">Quarantine in Office 365</span></span>

<span data-ttu-id="58046-105">Si vous êtes un client Office 365 avec des boîtes aux lettres dans Exchange Online ou un client Exchange Online Protection (EOP) autonome sans boîte aux lettres Exchange Online, la mise en quarantaine est disponible pour le blocage des messages potentiellement dangereux ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="58046-105">If you're an Office 365 customer with mailboxes in Exchange Online or a standalone Exchange Online Protection (EOP) customer without Exchange Online mailboxes, quarantine is available to hold potentially dangerous or unwanted messages.</span></span>

<span data-ttu-id="58046-106">Les stratégies de protection contre les programmes malveillants configurent automatiquement un message si *une* pièce jointe contient un programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="58046-106">Anti-malware policies automatically quarantine a message if *any* attachment is found to contain malware.</span></span> <span data-ttu-id="58046-107">Pour plus d’informations, consultez la rubrique [configure anti-malware Policies in Office 365](configure-anti-malware-policies.md).</span><span class="sxs-lookup"><span data-stu-id="58046-107">For more information, see [Configure anti-malware policies in Office 365](configure-anti-malware-policies.md).</span></span>

<span data-ttu-id="58046-108">Par défaut, les stratégies de blocage du courrier indésirable mettent en quarantaine les messages d’hameçonnage et délivrent les messages de courrier indésirable et de courrier en nombre dans le dossier de courrier indésirable de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58046-108">By default, anti-spam polices quarantine phishing messages, and deliver spam and bulk email messages to the user's Junk Email folder.</span></span> <span data-ttu-id="58046-109">Toutefois, vous pouvez également créer et personnaliser des stratégies de blocage du courrier indésirable pour mettre en quarantaine le courrier indésirable et les messages électroniques en bloc.</span><span class="sxs-lookup"><span data-stu-id="58046-109">But, you can also create and customize anti-spam policies to quarantine spam and bulk-email messages.</span></span> <span data-ttu-id="58046-110">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans Office 365](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="58046-110">For more information, see [Configure anti-spam policies in Office 365](configure-your-spam-filter-policies.md).</span></span>

<span data-ttu-id="58046-111">Les utilisateurs et les administrateurs peuvent travailler avec des messages mis en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="58046-111">Both users and admins can work with quarantined messages:</span></span>

- <span data-ttu-id="58046-112">Les administrateurs peuvent utiliser tous les types de messages mis en quarantaine pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="58046-112">Admins can work with all types of quarantined messages for all users.</span></span> <span data-ttu-id="58046-113">Seuls les administrateurs peuvent travailler avec des messages mis en quarantaine en tant que programme malveillant, hameçonnage à haute fiabilité ou suite à des règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="58046-113">Only admins can work with messages that were quarantined as malware, high confidence phishing, or as a result of mail flow rules (also known as transport rules).</span></span> <span data-ttu-id="58046-114">Pour plus d’informations, consultez la rubrique [gestion des messages et des fichiers mis en quarantaine en tant qu’administrateur dans Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="58046-114">For more information, see [Manage quarantined messages and files as an admin in Office 365](manage-quarantined-messages-and-files.md).</span></span>

- <span data-ttu-id="58046-115">Les utilisateurs peuvent travailler avec des messages mis en quarantaine, où ils sont destinataires si le message a été mis en quarantaine en tant que courrier indésirable, message électronique en masse ou (depuis avril, 2020).</span><span class="sxs-lookup"><span data-stu-id="58046-115">Users can work with quarantined messages where they are a recipient if the message was quarantined as spam, bulk email, or (as of April, 2020) phishing.</span></span> <span data-ttu-id="58046-116">Pour plus d’informations, consultez [la rubrique Rechercher et débloquer les messages mis en quarantaine en tant qu’utilisateur dans Office 365](find-and-release-quarantined-messages-as-a-user.md).</span><span class="sxs-lookup"><span data-stu-id="58046-116">For more information, see [Find and release quarantined messages as a user in Office 365](find-and-release-quarantined-messages-as-a-user.md).</span></span>

  <span data-ttu-id="58046-117">Pour empêcher les utilisateurs de gérer leurs propres messages de hameçonnage mis en quarantaine, les administrateurs peuvent configurer une autre action pour le verdict de filtrage du **courrier électronique de hameçonnage** dans les stratégies de blocage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="58046-117">To prevent users from managing their own quarantined phishing messages, admins can configure a different action for the **Phishing email** filtering verdict in anti-spam policies.</span></span> <span data-ttu-id="58046-118">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans Office 365](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="58046-118">For more information, see [Configure anti-spam policies in Office 365](configure-your-spam-filter-policies.md).</span></span>

- <span data-ttu-id="58046-119">Les administrateurs et les utilisateurs peuvent signaler des faux positifs à Microsoft en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="58046-119">Admins and users can report false positives to Microsoft in quarantine.</span></span>

<span data-ttu-id="58046-120">Pour plus d’informations sur la mise en quarantaine, consultez la rubrique [mise en quarantaine](quarantine-faq.md).</span><span class="sxs-lookup"><span data-stu-id="58046-120">For more information about, quarantine, see [Quarantine FAQ](quarantine-faq.md).</span></span>

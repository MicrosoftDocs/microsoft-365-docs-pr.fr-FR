---
title: Intégration de Cortana à Office 365
f1.keywords:
- CSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 7257cb50-0d5c-4f7a-ac2e-9fe5d13bb5cb
description: 'Découvrez comment utiliser Cortana, lorsqu’elle est intégrée à Office 365. Vous pouvez désactiver Cortana dans le centre d’administration pour limiter son accès aux données de votre organisation. '
ms.openlocfilehash: 21de80d127498dd40db932923a8d650b87b8a24c
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42254343"
---
# <a name="cortana-in-office-365"></a><span data-ttu-id="a526f-104">Cortana dans Office 365</span><span class="sxs-lookup"><span data-stu-id="a526f-104">Cortana in Office 365</span></span>

<span data-ttu-id="a526f-105">Cortana est un assistant numérique basé sur un nuage et un service Microsoft 365 et Office 365 qui fonctionne sur vos appareils et services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a526f-105">Cortana is a cloud-based digital assistant and Microsoft 365 and Office 365 service that works across your devices and Microsoft services.</span></span> <span data-ttu-id="a526f-106">Cortana peut utiliser les informations stockées dans Microsoft 365 et Office 365 pour aider les membres de votre organisation à rester à jour et à obtenir des informations, des tâches suggérées et une aide sur leurs réunions, leurs documents et leurs contacts.</span><span class="sxs-lookup"><span data-stu-id="a526f-106">Cortana can use information stored in Microsoft 365 and Office 365 to help people in your organization stay up to date and get insights, suggested tasks, and help with their meetings, documents, and contacts.</span></span>
  
## <a name="info-for-admins"></a><span data-ttu-id="a526f-107">Informations pour les administrateurs</span><span class="sxs-lookup"><span data-stu-id="a526f-107">Info for admins</span></span>

<span data-ttu-id="a526f-108">La conformité est un engagement que Microsoft propose aux clients d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="a526f-108">Compliance is a commitment that Microsoft makes to enterprise customers.</span></span> [<span data-ttu-id="a526f-109">En savoir plus sur l’infrastructure de conformité Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a526f-109">Learn more about the Microsoft compliance framework.</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=2109173)

<span data-ttu-id="a526f-110">Compatible avec les autres services Microsoft 365 et Office 365, les fonctionnalités de Cortana conformes sont protégées et sécurisées, sous réserve des conditions de service en ligne qui incluent un ensemble de promesses impliquant la protection des données utilisateur contre la perte accidentelle, la modification Divulgation ou accès non autorisé, ou destruction illicite.</span><span class="sxs-lookup"><span data-stu-id="a526f-110">Consistent with other Microsoft 365 and Office 365 services, compliant Cortana features are protected and secured subject to the Online Service Terms that includes a set of promises involving protection of user data against accidental loss, alteration, unauthorized disclosure or access, or unlawful destruction.</span></span> <span data-ttu-id="a526f-111">Toutes les autres fonctionnalités de Cortana (par exemple, Cortana, services connectés en option) sont soumises au [contrat de services Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=2109174) et à la [déclaration de confidentialité de Microsoft.](https://go.microsoft.com/fwlink/p/?LinkId=2109175)</span><span class="sxs-lookup"><span data-stu-id="a526f-111">All other Cortana features (i.e., Cortana optional connected services) are subject to the [Microsoft Services Agreement](https://go.microsoft.com/fwlink/p/?LinkId=2109174) and  [Microsoft Privacy Statement.](https://go.microsoft.com/fwlink/p/?LinkId=2109175)</span></span>

<span data-ttu-id="a526f-112">Les services Cortana sont divisés en deux catégories de données, **conformes** et **facultatifs**, que vous pouvez contrôler.</span><span class="sxs-lookup"><span data-stu-id="a526f-112">Cortana services are broken into two data categories, **compliant** and **optional connected services**, which you can control.</span></span>

## <a name="turn-off-cortana-optional-connected-services"></a><span data-ttu-id="a526f-113">Désactiver les services connectés en option par Cortana</span><span class="sxs-lookup"><span data-stu-id="a526f-113">Turn off Cortana optional connected services</span></span>

<span data-ttu-id="a526f-114">Cortana les services connectés facultatifs peuvent être désactivés pour les employés de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a526f-114">Cortana optional connected services can be turned off for employees at your organization.</span></span> <span data-ttu-id="a526f-115">Cette opération désactive Cortana services connectés en option dans Cortana sur Windows et l’application mobile de Cortana.</span><span class="sxs-lookup"><span data-stu-id="a526f-115">This will disable Cortana optional connected services in Cortana on Windows and the Cortana mobile app.</span></span> <span data-ttu-id="a526f-116">Cela inclut les rappels, les listes, les tâches et les autres fonctionnalités de Cortana.</span><span class="sxs-lookup"><span data-stu-id="a526f-116">This includes Cortana reminders, lists, tasks, and other features.</span></span> <span data-ttu-id="a526f-117">Les services de la catégorie conforme (c.-à-d. l’expérience OST de Cortana), tels que le courrier électronique de briefing de Cortana, et lire mes courriers électroniques dans Outlook Mobile, restent actifs.</span><span class="sxs-lookup"><span data-stu-id="a526f-117">Services in the compliant category (i.e., Cortana OST experiences), such as Cortana’s Briefing email, and Play My Emails in Outlook mobile, will remain active.</span></span>

1. <span data-ttu-id="a526f-118">Dans le centre d’administration 365 de Microsoft, sélectionnez**paramètres** des **paramètres** > et sélectionnez **Cortana**.</span><span class="sxs-lookup"><span data-stu-id="a526f-118">In the Microsoft 365 admin center, select **Settings** > **Settings** and select **Cortana**.</span></span>

4. <span data-ttu-id="a526f-119">Activez la case à cocher **autoriser les expériences connectées à Cortana facultatives pour utiliser les données hébergées par Microsoft de votre organisation** afin d’activer ou de désactiver les expériences connectées à Cortana.</span><span class="sxs-lookup"><span data-stu-id="a526f-119">Select the checkbox for **Allow Cortana optional connected experiences to use your organizations's Microsoft hosted data** to enable or disable Cortana connected experiences.</span></span>

5. <span data-ttu-id="a526f-120">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="a526f-120">Select **Save changes**.</span></span>

## <a name="turn-off-cortana-ost-experiences"></a><span data-ttu-id="a526f-121">Désactiver les expériences OST Cortana</span><span class="sxs-lookup"><span data-stu-id="a526f-121">Turn off Cortana OST experiences</span></span>

<span data-ttu-id="a526f-122">Les employés de votre organisation peuvent désactiver les expériences OST de Cortana individuellement en suivant les étapes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a526f-122">Your organization's employees can opt out of Cortana OST experiences individually by following the steps below.</span></span>

1. <span data-ttu-id="a526f-123">Ouvrez Outlook Mobile.</span><span class="sxs-lookup"><span data-stu-id="a526f-123">Open Outlook mobile.</span></span>

2. <span data-ttu-id="a526f-124">Accédez à **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="a526f-124">Go to **Settings**.</span></span>
  
3. <span data-ttu-id="a526f-125">Sélectionnez **lire mes courriers électroniques**.</span><span class="sxs-lookup"><span data-stu-id="a526f-125">Select **Play My Emails**.</span></span>

4. <span data-ttu-id="a526f-126">Déplacez le bouton bascule sur désactivé sur les comptes que vous souhaitez désactiver.</span><span class="sxs-lookup"><span data-stu-id="a526f-126">Move the toggle to off on the accounts you want to disable.</span></span>

### <a name="briefing-email"></a><span data-ttu-id="a526f-127">Courrier électronique de briefing</span><span class="sxs-lookup"><span data-stu-id="a526f-127">Briefing email</span></span>

<span data-ttu-id="a526f-128">La désactivation de Cortana sur la barre des tâches ne désactive pas le courrier électronique de résumé de Cortana.</span><span class="sxs-lookup"><span data-stu-id="a526f-128">Disabling Cortana on the taskbar won't disable Cortana’s Briefing email.</span></span> <span data-ttu-id="a526f-129">Les employés doivent se désabonner individuellement.</span><span class="sxs-lookup"><span data-stu-id="a526f-129">Employees must unsubscribe individually.</span></span> <span data-ttu-id="a526f-130">Les personnes de votre organisation peuvent désactiver le courrier de briefing de Cortana en sélectionnant **Annuler l’abonnement** dans le pied de page du message.</span><span class="sxs-lookup"><span data-stu-id="a526f-130">Individuals from your organization can opt out of Cortana’s Briefing email by selecting **Unsubscribe** in the footer of the message.</span></span>
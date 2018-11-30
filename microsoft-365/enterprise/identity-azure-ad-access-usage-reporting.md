---
title: 'Étape 13 : Surveiller l’activité de connexion et du client'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/01/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et configurez l’accès Azure AD et le rapport d’utilisation.
ms.openlocfilehash: 997d52bc11036e1dbb7dcc6e1f9f48a59b2ddbf5
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26866825"
---
# <a name="step-13-monitor-tenant-and-sign-in-activity"></a><span data-ttu-id="db6d7-103">Étape 13 : Surveiller l’activité de connexion et du client</span><span class="sxs-lookup"><span data-stu-id="db6d7-103">Step 13: Monitor tenant and sign-in activity</span></span>

<span data-ttu-id="db6d7-104">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="db6d7-104">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="db6d7-p101">Dans cette étape, vous allez passer en revue les journaux d’audit et l’activité de connexion à l’aide des rapports Azure AD. Deux types de rapports sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="db6d7-p101">In Step 13, you'll review audit logs and sign-in activity using Azure AD reporting. Two types of reports are available.</span></span>

<span data-ttu-id="db6d7-p102">Le **rapport d’activité des journaux d’audit** enregistre l’historique de toutes les tâches effectuées dans votre client Azure AD. Ce rapport répond aux questions telles que :</span><span class="sxs-lookup"><span data-stu-id="db6d7-p102">The **Audit logs activity report** records the history of every task performed in your Azure AD tenant. This report answers questions like:</span></span>

- <span data-ttu-id="db6d7-109">Qui a ajouté une personne à un groupe d’administration ?</span><span class="sxs-lookup"><span data-stu-id="db6d7-109">Who added someone to an admin group?</span></span>
- <span data-ttu-id="db6d7-110">Quels sont les utilisateurs qui se connectent à une application spécifique ?</span><span class="sxs-lookup"><span data-stu-id="db6d7-110">Which users are signing into a specific app?</span></span>
- <span data-ttu-id="db6d7-111">Combien de réinitialisations de mot de passe sont prévues ?</span><span class="sxs-lookup"><span data-stu-id="db6d7-111">How many password resets are happening?</span></span>

<span data-ttu-id="db6d7-p103">Le **rapport d’activité des connexions** enregistre l’auteur des tâches indiquées par le rapport des journaux d’audit. Ce rapport répond aux questions telles que :</span><span class="sxs-lookup"><span data-stu-id="db6d7-p103">The **Sign-ins activity report** records who performed the tasks reported by the audit logs report. This report answers questions like:</span></span>

- <span data-ttu-id="db6d7-114">Pour un utilisateur spécifique à l’étude, quel est son modèle de connexion ?</span><span class="sxs-lookup"><span data-stu-id="db6d7-114">For a specific user under investigation, what is their sign-in pattern?</span></span>
- <span data-ttu-id="db6d7-115">Quel est mon volume de connexions par jour, semaine ou mois ?</span><span class="sxs-lookup"><span data-stu-id="db6d7-115">What is my volume of sign-ins over a day, week, or month?</span></span>
- <span data-ttu-id="db6d7-116">Combien de ces tentatives de connexion n’ont pas abouti, et pour quels comptes ?</span><span class="sxs-lookup"><span data-stu-id="db6d7-116">How many of these sign-in attempts were not successful, and for which accounts?</span></span>

<span data-ttu-id="db6d7-117">Pour plus d’informations sur les rapports et la façon d’y accéder, reportez-vous à la rubrique [Création de rapports Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="db6d7-117">For more information about the reports and how to access them, see [Azure Active Directory reporting](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-azure-portal).</span></span>

<span data-ttu-id="db6d7-118">Après cette étape, vous connaîtrez ces rapports et saurez comment les utiliser pour obtenir des informations sur les activités et événements Azure AD à des fins de planification et de sécurité.</span><span class="sxs-lookup"><span data-stu-id="db6d7-118">As a result of this step, you'll gain awareness of these reports and an understanding of how you can use them to gain insights on Azure AD events and activities for planning and security purposes.</span></span>

## <a name="next-step"></a><span data-ttu-id="db6d7-119">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="db6d7-119">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step14.png)| [<span data-ttu-id="db6d7-120">Autorisez les utilisateurs à créer et gérer leurs propres groupes</span><span class="sxs-lookup"><span data-stu-id="db6d7-120">Allow users to create and manage their own groups</span></span>](identity-self-service-group-management.md) |

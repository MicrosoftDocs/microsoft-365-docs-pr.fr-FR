---
title: Déployer Exchange Online pour Microsoft 365 Éducation
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/03/2020
audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
f1.keywords:
- NOCSH
description: Si vous souhaitez en savoir plus sur les incidents d’e-mail ou les conseils dans Microsoft 365, utilisez la surveillance d’Exchange Online.
ms.openlocfilehash: 3d88378449879d451b21ba8bf2a7b5c3032a2c07
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53286440"
---
# <a name="exchange-online-monitoring-for-microsoft-365"></a><span data-ttu-id="2a163-103">Déployer Exchange Online pour Microsoft 365 Éducation</span><span class="sxs-lookup"><span data-stu-id="2a163-103">Exchange Online monitoring for Microsoft 365</span></span>

<span data-ttu-id="2a163-104">La surveillance d’Exchange Online dans le Centre d’administration Microsoft 365 vous permet de surveiller l’état d’intégrité du service Exchange pour l’abonnement Microsoft 365 de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2a163-104">You can use Exchange Online monitoring in the Microsoft 365 admin center to monitor the health of the Exchange service for your organization’s Microsoft 365 subscription.</span></span> <span data-ttu-id="2a163-105">La surveillance d’Exchange Online fournit des informations sur les incidents et les conseils collectés dans les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a163-105">Exchange Online monitoring provides you with information about incidents and advisories that are collected in these categories:</span></span>

- <span data-ttu-id="2a163-106">**Infrastructure** : le programme détecte un problème dans l’infrastructure Microsoft 365 détenue par Microsoft pour fournir des mises à jour régulières et résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="2a163-106">**Infrastructure**: Issue is detected in the Microsoft 365 infrastructure that Microsoft owns for providing regular updates and resolving the issue.</span></span> <span data-ttu-id="2a163-107">Par exemple, les utilisateurs ne peuvent pas accéder à Exchange Online en raison de problèmes liés à Exchange ou à une autre infrastructure cloud Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2a163-107">For example, users cannot access Exchange Online because of issues with Exchange or other Microsoft 365 cloud infrastructure.</span></span>
- <span data-ttu-id="2a163-108">**Infrastructure tierce** : le programme détecte un problème dans une infrastructure tierce sur laquelle votre organisation a pris une dépendance. Votre organisation doit alors effectuer l’action nécessaire pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="2a163-108">**Third-party infrastructure**: Issue is detected in third-party infrastructure on which your organization has taken a dependency and requires action from your organization for resolution.</span></span> <span data-ttu-id="2a163-109">Par exemple, un fournisseur de services d’émission de jeton de sécurité (STS) tiers limite les transactions d’authentification utilisateur et empêche les utilisateurs de se connecter à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="2a163-109">For example, user authentication transactions are getting throttled by a third-party security token service (STS) provider that prevents users from connecting to Exchange Online.</span></span>
- <span data-ttu-id="2a163-110">**Infrastructure cliente** : le programme détecte un problème dans l’infrastructure de votre organisation. Celle-ci doit alors effectuer l’action nécessaire pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="2a163-110">**Customer infrastructure**: Issue is detected in your organization's infrastructure and requires action from your organization for resolution.</span></span> <span data-ttu-id="2a163-111">Par exemple, les utilisateurs ne peuvent pas accéder à Exchange Online, car ils ne peuvent pas obtenir de jeton d’authentification via un fournisseur STS hébergé par votre organisation en raison d’un certificat arrivé à expiration.</span><span class="sxs-lookup"><span data-stu-id="2a163-111">For example, users cannot access Exchange Online because they are unable to obtain an authentication token from STS provider hosted by your organization because of an expired certificate.</span></span>

<span data-ttu-id="2a163-112">Voici un exemple de la page **Intégrité des services** dans le Centre d’administration Microsoft 365, disponible via **Intégrité > Intégrité des services**.</span><span class="sxs-lookup"><span data-stu-id="2a163-112">Here is an example of the **Service health** page in the Microsoft 365 admin center, available from **Health > Service health**.</span></span>

![Page Intégrité des services dans le Centre d’administration Microsoft 365](../media/microsoft-365-exchange-monitoring/service-health-dashboard-example.png)

<span data-ttu-id="2a163-114">La valeur de la colonne **État** indique si le service est intègre, s’il comporte des conseils ou des incidents sur la base des services cloud gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2a163-114">The value of the **Status** column indicates whether the service is healthy or has advisories or incidents based on the cloud services that Microsoft maintains.</span></span> 

<span data-ttu-id="2a163-115">La valeur de la colonne **Vos problèmes liés à votre organisation et à des tiers** indique que l’infrastructure de votre organisation ou un logiciel tiers a une incidence sur l’expérience de vos utilisateurs en matière d’intégrité des services avec Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="2a163-115">The value of the **Your org and 3rd party issues** column indicates that your organization's infrastructure or third-party software affects your users service health experience with Exchange Online.</span></span> <span data-ttu-id="2a163-116">Les conseils ou incidents nécessitent *vos* actions pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="2a163-116">Advisories or incidents require *your* actions to resolve.</span></span>

<span data-ttu-id="2a163-117">Voici un exemple de la page de surveillance **Exchange Online** dans le Centre d’administration Microsoft 365, disponible via **Intégrité > Intégrité des services > Exchange Online**.</span><span class="sxs-lookup"><span data-stu-id="2a163-117">Here is an example of the **Exchange Online** monitoring page in the Microsoft 365 admin center, available from **Health > Service health > Exchange Online**.</span></span>

![Page de surveillance Exchange Online dans le Centre d’administration Microsoft 365](../media/microsoft-365-exchange-monitoring/exhange-monitoring-example.png)

<span data-ttu-id="2a163-119">La page de surveillance **Exchange Online** indique si le service Exchange Online est intègre ou non, et si des incidents ou conseils associés sont présents.</span><span class="sxs-lookup"><span data-stu-id="2a163-119">With the **Exchange Online** monitoring page, you can see whether the Exchange Online service is healthy or not and whether there are any associated incidents or advisories.</span></span> <span data-ttu-id="2a163-120">Avec la surveillance Exchange Online, vous pouvez consulter l’état d’intégrité des services pour des scénarios d’e-mails spécifiques. Vous pouvez également consulter des signaux en temps réel pour déterminer l’impact par scénario.</span><span class="sxs-lookup"><span data-stu-id="2a163-120">With Exchange Online monitoring, you can look at the service health for specific email scenarios and view near real-time signals to determine the impact by scenario.</span></span> 

## <a name="requirements"></a><span data-ttu-id="2a163-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a163-121">Requirements</span></span>

<span data-ttu-id="2a163-122">Cette préversion est activée pour les clients qui répondent aux exigences suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a163-122">This preview is enabled for customers who meet these requirements:</span></span> 

- <span data-ttu-id="2a163-123">Votre organisation doit avoir un nombre de licences d’au moins 5 000, soit une combinaison de ces produits : Office 365 E3, Microsoft 365 E3, Office 365 E5, Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2a163-123">Your organization needs to have a license count of at least 5,000, from one or a combination of these products: Office 365 E3, Microsoft 365 E3, Office 365 E5, Microsoft 365 E5.</span></span> 

  <span data-ttu-id="2a163-124">Par exemple, votre organisation peut avoir 3 000 licences Office 365 E3 et 2 500 Microsoft 365 E5, pour un total de 5 500 licences provenant des produits éligibles.</span><span class="sxs-lookup"><span data-stu-id="2a163-124">For example, your organization can have 3,000 Office 365 E3 licenses and 2,500 Microsoft 365 E5, for a total of 5,500 licenses from the qualifying products.</span></span>

- <span data-ttu-id="2a163-125">Votre organisation doit avoir au moins 50 utilisateurs Exchange Online actifs par mois.</span><span class="sxs-lookup"><span data-stu-id="2a163-125">Your organization needs to have at least 50 monthly active Exchange Online users.</span></span>

<span data-ttu-id="2a163-126">La surveillance d’Exchange Online vous permet de consulter l’état d’intégrité des clients de courrier suivants sur la base de l’activité de lecture des e-mails :</span><span class="sxs-lookup"><span data-stu-id="2a163-126">With Exchange Online monitoring you can view the health for the following email clients based on email read activity:</span></span>

- <span data-ttu-id="2a163-127">Version de bureau d’Outlook</span><span class="sxs-lookup"><span data-stu-id="2a163-127">Outlook Desktop</span></span>
- <span data-ttu-id="2a163-128">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="2a163-128">Outlook on the Web</span></span>
- <span data-ttu-id="2a163-129">Clients de messagerie natifs d’iOS et Android</span><span class="sxs-lookup"><span data-stu-id="2a163-129">Native mail clients of iOS and Android</span></span> 
- <span data-ttu-id="2a163-130">Application Outlook Mobile pour iOS et Android</span><span class="sxs-lookup"><span data-stu-id="2a163-130">Outlook Mobile app in iOS and Android</span></span> 
- <span data-ttu-id="2a163-131">Client Outlook Mac</span><span class="sxs-lookup"><span data-stu-id="2a163-131">Outlook Mac client</span></span>

<span data-ttu-id="2a163-132">Pour ces clients, vous pouvez connaître le nombre d’utilisateurs actifs au cours des 30 dernières minutes en fonction des utilisateurs qui lisent un e-mail, ainsi que le nombre d’incidents et de conseils dans le tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="2a163-132">For these clients, you can see the number of active users in the last 30 minutes based on users reading an email, along with number of incidents and advisories in the dashboard.</span></span> <span data-ttu-id="2a163-133">Le programme compare ces données au même intervalle pour la semaine précédente afin de déterminer si un problème s’est produit.</span><span class="sxs-lookup"><span data-stu-id="2a163-133">This data is compared to the same interval for the previous week to see if there’s an issue.</span></span> 

>[!Note]
> <span data-ttu-id="2a163-134">Le programme détermine le nombre d’utilisateurs actifs selon une activité unique. Par exemple, lorsqu’un utilisateur lit un e-mail.</span><span class="sxs-lookup"><span data-stu-id="2a163-134">Active user count is measured by a single activity, for example, when a user reads an email.</span></span> <span data-ttu-id="2a163-135">Il rend compte seulement des 30 dernières minutes d’activité.</span><span class="sxs-lookup"><span data-stu-id="2a163-135">It only accounts for the last 30 minutes of activity.</span></span>
>

<span data-ttu-id="2a163-136">Vous pouvez également surveiller l’intégrité d’Exchange Online pour les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="2a163-136">You can also monitor Exchange Online health for the following scenarios:</span></span>

- <span data-ttu-id="2a163-137">**Flux de courriers** : nombre de messages remis correctement dans une boîte aux lettres sans délai une fois le message arrivé sur le réseau Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2a163-137">**Mail flow**: The number of messages successfully delivered to a mailbox without any delay after the message reached the Microsoft 365 network.</span></span> 
- <span data-ttu-id="2a163-138">**Authentification de base et authentification moderne** : nombre d’utilisateurs correctement validés dans le service Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="2a163-138">**Basic Authentication and Modern Authentication**: The number of users successfully validated in the Exchange Online service.</span></span>

![Exemple de surveillance de l’intégrité d’Exchange pour la livraison des e-mails](../media/microsoft-365-exchange-monitoring/exhange-monitoring-scenario-example.png)

<span data-ttu-id="2a163-140">Dans tous ces scénarios, les chiffres clés s’appliquent aux 30 dernières minutes dans le tableau de bord principal.</span><span class="sxs-lookup"><span data-stu-id="2a163-140">For all these scenarios, the key numbers are for the last 30 minutes in the main dashboard.</span></span> <span data-ttu-id="2a163-141">Les affichages détaillés pour chacun de ces scénarios illustrent la tendance quasiment en temps réel pendant sept jours avec un agrégat de 30 minutes comparé à la semaine précédente.</span><span class="sxs-lookup"><span data-stu-id="2a163-141">Detailed views for each of these scenarios shows the near real-time trend for seven days with the 30-minute aggregate compared with the previous week.</span></span> 

## <a name="send-us-feedback"></a><span data-ttu-id="2a163-142">Nous envoyer des commentaires</span><span class="sxs-lookup"><span data-stu-id="2a163-142">Send us feedback</span></span>

<span data-ttu-id="2a163-143">Vous pouvez envoyer vos commentaires de deux manières :</span><span class="sxs-lookup"><span data-stu-id="2a163-143">There are two ways you can provide feedback:</span></span>

- <span data-ttu-id="2a163-144">Utilisez l’option **Envoyer des commentaires** disponible sur chaque page du Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2a163-144">Use the **Give feedback** option available on every page of the Microsoft 365 admin center.</span></span>
- <span data-ttu-id="2a163-145">Envoyez vos commentaires à l’aide du lien **Cette publication est-elle utile ?** pour un incident ou un conseil spécifique.</span><span class="sxs-lookup"><span data-stu-id="2a163-145">Submit feedback using the **Is this post helpful?** link for a specific incident or advisory.</span></span>

![Lien « Cette publication est-elle utile ? »](../media/microsoft-365-exchange-monitoring/exhange-monitoring-example-incident-feedback.png)

## <a name="frequently-asked-questions"></a><span data-ttu-id="2a163-148">Foire aux questions</span><span class="sxs-lookup"><span data-stu-id="2a163-148">Frequently asked questions</span></span>

#### <a name="1-why-dont-i-see-exchange-online-monitoring-under-health-in-the-microsoft-365-admin-center"></a><span data-ttu-id="2a163-149">1. Pourquoi la mention « Surveillance Exchange Online » n’apparaît-elle pas dans le Centre d’administration Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="2a163-149">1. Why don’t I see “Exchange Online monitoring” under Health in the Microsoft 365 admin center?</span></span> 

<span data-ttu-id="2a163-150">Tout d’abord, vérifiez que vous avez activé le nouveau Centre d’administration sur la page **Accueil** du Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2a163-150">First, make sure you’ve enabled the new admin center on the **Home** page of the Microsoft 365 admin center.</span></span> 

<span data-ttu-id="2a163-151">Vérifiez que vous remplissez les deux conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a163-151">Then make sure you meet both of the following requirements:</span></span> 

- <span data-ttu-id="2a163-152">Votre organisation doit avoir un nombre de licences d’au moins 5 000, soit une combinaison de ces produits : Office 365 E3, Microsoft 365 E3, Office 365 E5, Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2a163-152">Your organization needs to have a license count of at least 5,000, from one or a combination of these products: Office 365 E3, Microsoft 365 E3, Office 365 E5, Microsoft 365 E5.</span></span> 
- <span data-ttu-id="2a163-153">Votre organisation doit avoir au moins 50 utilisateurs Exchange Online actifs par mois.</span><span class="sxs-lookup"><span data-stu-id="2a163-153">Your organization needs to have at least 50 monthly active Exchange Online users.</span></span>

<span data-ttu-id="2a163-154">Si le nombre de licences de votre organisation est inférieur à 5 000 utilisateurs et que le nombre d’utilisateurs actifs par mois passe au-dessous des 50, la surveillance Exchange Online ne sera pas activée tant que ces conditions ne seront pas remplies.</span><span class="sxs-lookup"><span data-stu-id="2a163-154">If the license count for your organization goes below 5,000 users and the monthly active users goes below 50 users, Exchange Online monitoring won’t be enabled until these requirements are met.</span></span>

#### <a name="2-the-active-user-count-in-the-dashboard-for-each-client-appears-to-be-low-we-have-a-lot-of-active-licenses-assigned-to-users-what-does-this-mean"></a><span data-ttu-id="2a163-155">2. Le nombre d’utilisateurs actifs dans le tableau de bord pour chaque client semble faible.</span><span class="sxs-lookup"><span data-stu-id="2a163-155">2. The active user count in the dashboard for each client appears to be low.</span></span> <span data-ttu-id="2a163-156">Nous avons attribué un grand nombre de licences actives à des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2a163-156">We have a lot of active licenses assigned to users.</span></span> <span data-ttu-id="2a163-157">Qu’est-ce que cela signifie ?</span><span class="sxs-lookup"><span data-stu-id="2a163-157">What does this mean?</span></span> 

<span data-ttu-id="2a163-158">Le nombre d’utilisateurs actifs indiqué dans la surveillance est basé sur une période de 30 minutes au cours de laquelle les utilisateurs ont effectué l’activité indiquée dans la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="2a163-158">The active user count shown in monitoring is based on a 30-minute window where users have performed the activity called out in the feature.</span></span> <span data-ttu-id="2a163-159">Ce nombre est différent des nombres d’utilisations.</span><span class="sxs-lookup"><span data-stu-id="2a163-159">This shouldn’t be confused with usage numbers.</span></span> <span data-ttu-id="2a163-160">Pour afficher les nombres d’utilisation, utilisez les rapports d’activité dans le Centre d’administration Microsoft 365 (**Rapports > Utilisation**).</span><span class="sxs-lookup"><span data-stu-id="2a163-160">To view usage numbers, use activity reports in the Microsoft 365 admin center (**Reports > Usage**).</span></span>

#### <a name="3-will-there-be-other-monitoring-scenarios-for-other-services-such-as-teams-and-sharepoint"></a><span data-ttu-id="2a163-161">3. D’autres scénarios de surveillances seront-ils présents pour d’autres services tels que Teams et SharePoint ?</span><span class="sxs-lookup"><span data-stu-id="2a163-161">3. Will there be other monitoring scenarios for other services such as Teams and SharePoint?</span></span> 

<span data-ttu-id="2a163-162">Microsoft a intégré cette expérience directement dans le tableau de bord Intégrité des services du Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2a163-162">Microsoft is integrating this experience directly inside the Service Health dashboard in the Microsoft 365 admin center.</span></span> <span data-ttu-id="2a163-163">Microsoft pourra ainsi étendre les scénarios de surveillance à d’autres services qui figureront dans les prochaines actualités à partager.</span><span class="sxs-lookup"><span data-stu-id="2a163-163">This will provide opportunities for Microsoft to extend monitoring scenarios for other services, which will be announced when there is news to share.</span></span> 

#### <a name="4-what-is-the-plan-for-general-availability-of-this-experience"></a><span data-ttu-id="2a163-164">4. Quelle est l’offre prévue pour la disponibilité générale de cette expérience ?</span><span class="sxs-lookup"><span data-stu-id="2a163-164">4. What is the plan for general availability of this experience?</span></span> 

<span data-ttu-id="2a163-165">Microsoft a intégré la surveillance Exchange Online directement dans le tableau de bord **Intégrité des services** du Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2a163-165">Microsoft has integrated Exchange Online monitoring directly on the **Service Health** dashboard in the Microsoft 365 admin center.</span></span> 

<span data-ttu-id="2a163-166">Grâce à cette nouvelle expérience intégrée, Microsoft envisage de recueillir vos commentaires, puis de définir notre offre en faveur de la disponibilité générale.</span><span class="sxs-lookup"><span data-stu-id="2a163-166">With this new integrated experience, Microsoft's plan is to collect your feedback and then define our plan for general availability.</span></span>

#### <a name="5-is-this-a-free-included-or-paid-extra-feature"></a><span data-ttu-id="2a163-167">5. Cette fonctionnalité est-elle gratuite (incluse) ou payante (comme supplément) ?</span><span class="sxs-lookup"><span data-stu-id="2a163-167">5. Is this a free (included) or paid (extra) feature?</span></span> 

<span data-ttu-id="2a163-168">Cette fonctionnalité est en préversion publique et uniquement disponible pour les clients répondant aux critères de la question 1.</span><span class="sxs-lookup"><span data-stu-id="2a163-168">This feature is in Public preview and only available for customers that meet the requirements in question 1.</span></span>

<!--
>[!Note]
>INTERNAL: That decision is pending
>
--> 

#### <a name="6-how-do-i-provide-feedback"></a><span data-ttu-id="2a163-169">6. Comment faire part de mes commentaires ?</span><span class="sxs-lookup"><span data-stu-id="2a163-169">6. How do I provide feedback?</span></span> 

<span data-ttu-id="2a163-170">Pour vos commentaires généraux, utilisez l’icône **Envoyer des commentaires** en bas à droite de la page de surveillance **Exchange Online**.</span><span class="sxs-lookup"><span data-stu-id="2a163-170">For general feedback, use the **Give feedback** icon on the bottom-right corner of the **Exchange Online** monitoring page.</span></span> 

<span data-ttu-id="2a163-171">Pour des commentaires sur les incidents ou les conseils, utilisez le lien **Cette publication est-elle utile ?**.</span><span class="sxs-lookup"><span data-stu-id="2a163-171">For feedback on incidents or advisories, use the **Is this post helpful?** link.</span></span>

#### <a name="7-where-is-the-data-instrumented-for-the-scenarios-that-show-activity-trends"></a><span data-ttu-id="2a163-172">7. Où les données sont-elles instrumentées pour les scénarios qui montrent des tendances des activités ?</span><span class="sxs-lookup"><span data-stu-id="2a163-172">7. Where is the data instrumented for the scenarios that show activity trends?</span></span>

<span data-ttu-id="2a163-p114">Les données sont instrumentées dans le service Exchange Online. S’il y a un problème qui se produit avant que la requête n’arrive à Exchange Online ou qu’une erreur s’est produite dans Exchange Online, le signal d’activité s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2a163-p114">The data is instrumented in the Exchange Online service. If there is a failure that happens before the request reaches Exchange Online or there is a failure in Exchange Online, you will see a drop in the activity signal.</span></span>

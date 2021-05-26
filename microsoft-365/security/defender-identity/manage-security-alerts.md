---
title: Alertes de sécurité Microsoft Defender pour l’identité dans Microsoft 365 Defender
description: Découvrez comment gérer et examiner les alertes de sécurité émises par Microsoft Defender pour l’identité dans Microsoft 365 Defender
ms.date: 05/20/2021
ms.topic: how-to
author: dcurwin
ms.author: dacurwin
ms.service: microsoft-defender-for-identity
manager: raynew
ms.openlocfilehash: 0c48c9076d05cd352229477acc28b32185eef54f
ms.sourcegitcommit: 4f6ef4cd09c3ed36dc0be3702b0636bad6cff8a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/26/2021
ms.locfileid: "52657799"
---
# <a name="defender-for-identity-security-alerts-in-microsoft-365-defender"></a><span data-ttu-id="a0192-103">Alertes de sécurité Defender pour l’identité dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a0192-103">Defender for Identity security alerts in Microsoft 365 Defender</span></span>

<span data-ttu-id="a0192-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a0192-104">**Applies to:**</span></span>

- <span data-ttu-id="a0192-105">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a0192-105">Microsoft 365 Defender</span></span>
- <span data-ttu-id="a0192-106">Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="a0192-106">Defender for Identity</span></span>

<span data-ttu-id="a0192-107">Cet article explique les principes de base de l’utilisation des alertes de sécurité [Microsoft Defender pour](/defender-for-identity) l’identité dans le centre Microsoft 365 de [sécurité.](/microsoft-365/security/defender/overview-security-center)</span><span class="sxs-lookup"><span data-stu-id="a0192-107">This article explains the basics of how to work with [Microsoft Defender for Identity](/defender-for-identity) security alerts in the [Microsoft 365 security center](/microsoft-365/security/defender/overview-security-center).</span></span>

<span data-ttu-id="a0192-108">Les alertes Defender pour l’identité sont intégrées en natif au centre [de sécurité Microsoft 365](https://security.microsoft.com) avec un format de page d’alerte d’identité dédié.</span><span class="sxs-lookup"><span data-stu-id="a0192-108">Defender for Identity alerts are natively integrated into the [Microsoft 365 security center](https://security.microsoft.com) with a dedicated Identity alert page format.</span></span> <span data-ttu-id="a0192-109">Il s’agit de la première étape du parcours d’introduction de l’expérience [Microsoft Defender pour l’identité](/defender-for-identity/defender-for-identity-in-microsoft-365-defender)complète dans Microsoft 365 Defender .</span><span class="sxs-lookup"><span data-stu-id="a0192-109">This marks the first step in the journey to [introduce the full Microsoft Defender for Identity experience into Microsoft 365 Defender](/defender-for-identity/defender-for-identity-in-microsoft-365-defender).</span></span>

<span data-ttu-id="a0192-110">La nouvelle page d’alerte d’identité offre aux clients Microsoft Defender for Identity un meilleur enrichissement de signal entre domaines et de nouvelles fonctionnalités de réponse automatisée aux identités.</span><span class="sxs-lookup"><span data-stu-id="a0192-110">The new Identity alert page gives Microsoft Defender for Identity customers better cross-domain signal enrichment and new automated identity response capabilities.</span></span> <span data-ttu-id="a0192-111">Il vous permet de rester sécurisé et d’améliorer l’efficacité de vos opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a0192-111">It ensures that you stay secure and helps improve the efficiency of your security operations.</span></span>

<span data-ttu-id="a0192-112">L’un des avantages de l’examen des alertes par le biais de [Microsoft 365 Defender](/microsoft-365/security/defender/microsoft-365-defender) est que les alertes Microsoft Defender pour l’identité sont davantage corrélées avec les informations obtenues à partir de chacun des autres produits de la suite.</span><span class="sxs-lookup"><span data-stu-id="a0192-112">One of the benefits of investigating alerts through [Microsoft 365 Defender](/microsoft-365/security/defender/microsoft-365-defender) is that Microsoft Defender for Identity alerts are further correlated with information obtained from each of the other products in the suite.</span></span> <span data-ttu-id="a0192-113">Ces alertes améliorées sont cohérentes avec les autres formats d’alerte Microsoft 365 Defender provenant de [Microsoft Defender](/microsoft-365/security/office-365-security) pour Office 365 et Microsoft Defender pour le point [de terminaison.](/microsoft-365/security/defender-endpoint)</span><span class="sxs-lookup"><span data-stu-id="a0192-113">These enhanced alerts are consistent with the other Microsoft 365 Defender alert formats originating from [Microsoft Defender for Office 365](/microsoft-365/security/office-365-security) and [Microsoft Defender for Endpoint](/microsoft-365/security/defender-endpoint).</span></span> <span data-ttu-id="a0192-114">La nouvelle page élimine efficacement la nécessité d’accéder à un autre portail de produits pour examiner les alertes associées à l’identité.</span><span class="sxs-lookup"><span data-stu-id="a0192-114">The new page effectively eliminates the need to navigate to another product portal to investigate alerts associated with identity.</span></span>

<span data-ttu-id="a0192-115">Les alertes provenant de Defender for Identity peuvent désormais déclencher les fonctionnalités d’investigation et de réponse automatisées [(AIR) de Microsoft 365 Defender,](/microsoft-365/security/defender/m365d-autoir) notamment la correction automatique des alertes et l’atténuation des outils et processus qui peuvent contribuer à l’activité suspecte.</span><span class="sxs-lookup"><span data-stu-id="a0192-115">Alerts originating from Defender for Identity can now trigger the [Microsoft 365 Defender automated investigation and response (AIR)](/microsoft-365/security/defender/m365d-autoir) capabilities, including automatically remediating alerts and the mitigation of tools and processes that can contribute to the suspicious activity.</span></span>

>[!IMPORTANT]
><span data-ttu-id="a0192-116">Dans le cadre de la convergence avec Microsoft 365 Defender, certaines options et détails ont changé par rapport à leur emplacement dans le portail Defender pour l’identité.</span><span class="sxs-lookup"><span data-stu-id="a0192-116">As part of the convergence with Microsoft 365 Defender, some options and details have changed from their location in the Defender for Identity portal.</span></span> <span data-ttu-id="a0192-117">Veuillez lire les détails ci-dessous pour découvrir où trouver les fonctionnalités connues et nouvelles.</span><span class="sxs-lookup"><span data-stu-id="a0192-117">Please read the details below to discover where to find both the familiar and new features.</span></span>

## <a name="review-security-alerts"></a><span data-ttu-id="a0192-118">Passer en revue les alertes de sécurité</span><span class="sxs-lookup"><span data-stu-id="a0192-118">Review security alerts</span></span>

<span data-ttu-id="a0192-119">Les alertes sont accessibles à partir de plusieurs emplacements, y compris la page **Alertes,** la page **Incidents,** les pages des appareils individuels **et** à partir de la page **de** recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="a0192-119">Alerts can be accessed from multiple locations, including the **Alerts** page, the **Incidents** page, the pages of individual **Devices**, and from the **Advanced hunting** page.</span></span> <span data-ttu-id="a0192-120">Dans cet exemple, nous allons passer en revue la **page Alertes.**</span><span class="sxs-lookup"><span data-stu-id="a0192-120">In this example, we'll review the **Alerts page**.</span></span>  

<span data-ttu-id="a0192-121">Dans le [centre Microsoft 365 de sécurité,](https://security.microsoft.com/)allez à **Incidents & alertes,** puis aux **alertes.**</span><span class="sxs-lookup"><span data-stu-id="a0192-121">In the [Microsoft 365 security center](https://security.microsoft.com/), go to **Incidents & alerts** and then to **Alerts**.</span></span>

![Go to Incidents and Alerts, then Alerts](../../media/defender-identity/incidents-alerts.png)

<span data-ttu-id="a0192-123">Pour voir les alertes de Defender pour l’identité, dans le haut à droite, sélectionnez **Filtre,** puis sous Sources de **service,** sélectionnez **Microsoft Defender pour** l’identité, puis sélectionnez **Appliquer**:</span><span class="sxs-lookup"><span data-stu-id="a0192-123">To see alerts from Defender for Identity, on the top-right select **Filter**, and then under **Service sources** select **Microsoft Defender for Identity**, and select **Apply**:</span></span>

![Filtre des événements Defender for Identity](../../media/defender-identity/filter-defender-for-identity.png)

<span data-ttu-id="a0192-125">Les alertes sont affichées avec des informations dans les **colonnes suivantes** **:** Nom de l’alerte , **Balises**, **Gravité** **,** État de l’enquête , État , **Catégorie**, **Source** de détection **,** Ressources impactées , Première activité et Dernière **activité**. </span><span class="sxs-lookup"><span data-stu-id="a0192-125">The alerts are displayed with information in the following columns: **Alert name**, **Tags**, **Severity**, **Investigation state**, **Status**, **Category**, **Detection source**, **Impacted assets**, **First activity**, and **Last activity**.</span></span>

![Événements Defender for Identity](../../media/defender-identity/filtered-alerts.png)

## <a name="manage-alerts"></a><span data-ttu-id="a0192-127">Gérer des alertes</span><span class="sxs-lookup"><span data-stu-id="a0192-127">Manage alerts</span></span>

<span data-ttu-id="a0192-128">Si vous cliquez sur le nom **de** l’alerte pour l’une des alertes, vous allez sur la page avec des détails sur l’alerte.</span><span class="sxs-lookup"><span data-stu-id="a0192-128">If you click the **Alert name** for one of the alerts, you'll go to the page with details about the alert.</span></span> <span data-ttu-id="a0192-129">Dans le volet gauche, vous verrez un résumé de ce qui **s’est passé**:</span><span class="sxs-lookup"><span data-stu-id="a0192-129">In the left pane, you'll see a summary of **What happened**:</span></span>

![Ce qui s’est passé dans l’alerte](../../media/defender-identity/what-happened.png)

<span data-ttu-id="a0192-131">Au-dessus de la zone Ce **qui s’est** passé se sont des boutons pour les **comptes,** l’hôte **de destination** et l’hôte **source** de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="a0192-131">Above the **What happened** box are buttons for the **Accounts**, **Destination Host** and **Source Host** of the alert.</span></span> <span data-ttu-id="a0192-132">Pour d’autres alertes, vous pouvez voir des boutons pour plus d’informations sur des hôtes, des comptes, des adresses IP, des domaines et des groupes de sécurité supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="a0192-132">For other alerts, you might see buttons for details about additional hosts, accounts, IP addresses, domains, and security groups.</span></span> <span data-ttu-id="a0192-133">Sélectionnez l’une d’elles pour obtenir plus de détails sur les entités impliquées.</span><span class="sxs-lookup"><span data-stu-id="a0192-133">Select any of them to get more details about the entities involved.</span></span>

<span data-ttu-id="a0192-134">Dans le volet droit, vous verrez les détails de **l’alerte.**</span><span class="sxs-lookup"><span data-stu-id="a0192-134">On the right pane, you'll see the **Alert details**.</span></span> <span data-ttu-id="a0192-135">Vous pouvez y voir plus de détails et effectuer plusieurs tâches :</span><span class="sxs-lookup"><span data-stu-id="a0192-135">Here you can see more details and perform several tasks:</span></span>

- <span data-ttu-id="a0192-136">**Classifier cette alerte** : ici, vous pouvez désigner cette alerte en tant qu’alerte **True** ou **False**</span><span class="sxs-lookup"><span data-stu-id="a0192-136">**Classify this alert** - Here you can designate this alert as a **True alert** or **False alert**</span></span>

    ![Classifier une alerte](../../media/defender-identity/classify-alert.png)

- <span data-ttu-id="a0192-138">**État de l’alerte** - Dans **Définir la classification,** vous pouvez classer l’alerte comme **True** ou **False**.</span><span class="sxs-lookup"><span data-stu-id="a0192-138">**Alert state** - In **Set Classification**, you can classify the alert as **True** or **False**.</span></span> <span data-ttu-id="a0192-139">Dans **Assigné à**, vous pouvez affecter l’alerte à vous-même ou la désattribuer.</span><span class="sxs-lookup"><span data-stu-id="a0192-139">In **Assigned to**, you can assign the alert to yourself or unassign it.</span></span>

    ![État de l’alerte](../../media/defender-identity/alert-state.png)

- <span data-ttu-id="a0192-141">**Détails** de l’alerte : sous **Détails** de l’alerte, vous trouverez plus d’informations sur l’alerte spécifique, suivez un lien vers la documentation sur le type d’alerte, consultez l’incident auquel l’alerte est associée, examinez les enquêtes automatisées liées à ce type d’alerte et consultez les appareils et les utilisateurs touchés.</span><span class="sxs-lookup"><span data-stu-id="a0192-141">**Alert details** - Under **Alert details**, you can find more information about the specific alert, follow a link to documentation about the type of alert, see which incident the alert is associated with, review any automated investigations linked to this alert type, and see the impacted devices and users.</span></span>

    ![Détails de l’alerte](../../media/defender-identity/alert-details.png)

- <span data-ttu-id="a0192-143">**Commentaires &'historique** : vous pouvez ajouter vos commentaires à l’alerte et consulter l’historique de toutes les actions associées à l’alerte.</span><span class="sxs-lookup"><span data-stu-id="a0192-143">**Comments & history** - Here you can add your comments to the alert, and see the history of all actions associated with the alert.</span></span>

    ![Commentaires et historique](../../media/defender-identity/comments-history.png)

- <span data-ttu-id="a0192-145">**Gérer l’alerte** : si vous sélectionnez **Gérer** l’alerte, vous allez dans un volet qui vous permettra de modifier les :</span><span class="sxs-lookup"><span data-stu-id="a0192-145">**Manage alert** - If you select **Manage alert**, you'll go to a pane that will allow you to edit the:</span></span>
  - <span data-ttu-id="a0192-146">**État** : vous pouvez choisir **Nouveau,** **Résolu** ou **En cours.**</span><span class="sxs-lookup"><span data-stu-id="a0192-146">**Status** - You can choose **New**, **Resolved** or **In progress**.</span></span>
  - <span data-ttu-id="a0192-147">**Classification** : vous pouvez choisir une **alerte True ou** **False.**</span><span class="sxs-lookup"><span data-stu-id="a0192-147">**Classification** - You can choose **True alert** or **False alert**.</span></span>
  - <span data-ttu-id="a0192-148">**Commentaire** : vous pouvez ajouter un commentaire sur l’alerte.</span><span class="sxs-lookup"><span data-stu-id="a0192-148">**Comment** - You can add a comment about the alert.</span></span>

    <span data-ttu-id="a0192-149">Si vous sélectionnez les trois points à côté de Gérer l’alerte, vous pouvez consulter un **expert** en **menaces,** exporter l’alerte vers un fichier Excel ou établir un lien vers **un autre incident.**</span><span class="sxs-lookup"><span data-stu-id="a0192-149">If you select the three dots next to **Manage alert**, you can **Consult a threat expert**, **Export** the alert to an Excel file, or **Link to another incident**.</span></span>

    ![Gérer l’alerte](../../media/defender-identity/manage-alert.png)

    >[!NOTE]
    ><span data-ttu-id="a0192-151">Dans le Excel, deux liens sont désormais disponibles : Afficher dans **Microsoft Defender** pour l’identité et Affichage dans **Microsoft 365 Defender.**</span><span class="sxs-lookup"><span data-stu-id="a0192-151">In the Excel file, you now have two links available: **View in Microsoft Defender for Identity** and **View in Microsoft 365 Defender**.</span></span> <span data-ttu-id="a0192-152">Chaque lien vous permet d’être sur le portail approprié et d’y fournir des informations sur l’alerte.</span><span class="sxs-lookup"><span data-stu-id="a0192-152">Each link will bring you to the relevant portal, and provide information about the alert there.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0192-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0192-153">See also</span></span>

- [<span data-ttu-id="a0192-154">Examiner les alertes dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a0192-154">Investigate alerts in Microsoft 365 Defender</span></span>](../defender/investigate-alerts.md)

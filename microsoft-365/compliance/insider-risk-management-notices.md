---
title: Modèles de notifications sur la gestion des risques internes
description: En savoir plus sur les modèles de notification de gestion des risques internes dans Microsoft 365
keywords: Microsoft 365, gestion des risques internes, gestion des risques, conformité
localization_priority: Normal
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection: m365-security-compliance
ms.openlocfilehash: 3a74c62e84c1cb9e4c749a364c0e5b6da25a8af9
ms.sourcegitcommit: 74ef7179887eedc696c975a82c865b2d4b3808fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "47416478"
---
# <a name="insider-risk-management-notice-templates"></a><span data-ttu-id="cb983-104">Modèles de notifications sur la gestion des risques internes</span><span class="sxs-lookup"><span data-stu-id="cb983-104">Insider risk management notice templates</span></span>

<span data-ttu-id="cb983-105">Les modèles d’avis de gestion des risques internes vous permettent d’envoyer des messages électroniques aux utilisateurs lorsque leurs activités génèrent une correspondance et une alerte de stratégie.</span><span class="sxs-lookup"><span data-stu-id="cb983-105">Insider risk management notice templates allow you to send email messages to users when their activities generate a policy match and alert.</span></span> <span data-ttu-id="cb983-106">Dans la plupart des cas, les actions de l’utilisateur qui génèrent des alertes sont le résultat d’erreurs ou d’activités accidentelles sans intention malveillante.</span><span class="sxs-lookup"><span data-stu-id="cb983-106">In most cases, user actions that generate alerts are the result of mistakes or inadvertent activities without ill intent.</span></span> <span data-ttu-id="cb983-107">Les notifications servent de rappels simples aux utilisateurs pour qu’ils soient plus prudents, qu’ils fournissent des liens vers des informations pour la formation à l’actualisation ou vers des ressources de stratégie d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="cb983-107">Notices serve as simple reminders to users to be more careful, to provide links to information for refresher training, or to corporate policy resources.</span></span> <span data-ttu-id="cb983-108">Les avis peuvent constituer une partie importante de votre programme de formation sur la conformité interne et peuvent vous aider à créer une piste d’audit documentée pour les utilisateurs avec des activités à risque périodique.</span><span class="sxs-lookup"><span data-stu-id="cb983-108">Notices can be an important part of your internal compliance training program and can help create a documented audit trail for users with recurring risk activities.</span></span>

<span data-ttu-id="cb983-109">Créez des modèles d’avis si vous souhaitez envoyer aux utilisateurs un avis de rappel par courrier électronique pour les correspondances de stratégie dans le cadre du processus de résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="cb983-109">Create notice templates if you want to send users an email reminder notice for policy matches as part of the issue resolution process.</span></span> <span data-ttu-id="cb983-110">Les notifications peuvent uniquement être envoyées à l’adresse de messagerie de l’utilisateur associée à l’alerte spécifique en cours de révision.</span><span class="sxs-lookup"><span data-stu-id="cb983-110">Notices can only be sent to the user email address associated with the specific alert being reviewed.</span></span> <span data-ttu-id="cb983-111">Lorsque vous sélectionnez un modèle d’avis à appliquer à une correspondance de stratégie, vous pouvez choisir d’accepter les valeurs de champ définies dans le modèle ou de les réécrire selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="cb983-111">When selecting a notice template to apply to a policy match, you can choose to accept the field values defined in the template or overwrite the fields as needed.</span></span>

## <a name="notice-templates-dashboard"></a><span data-ttu-id="cb983-112">Tableau de bord des modèles d’avis</span><span class="sxs-lookup"><span data-stu-id="cb983-112">Notice templates dashboard</span></span>

<span data-ttu-id="cb983-113">Le **Tableau de bord modèles de notifications** affiche une liste de modèles de notifications configurés et vous permet de créer des modèles de notifications.</span><span class="sxs-lookup"><span data-stu-id="cb983-113">The **Notices templates dashboard** displays a list of configured notice templates and allows you to create new notice templates.</span></span> <span data-ttu-id="cb983-114">Les modèles de notifications sont répertoriés à l’aide du modèle de notifications le plus récent répertorié en premier.</span><span class="sxs-lookup"><span data-stu-id="cb983-114">The notice templates are listed in reverse date order with the most recent notice template listed first.</span></span>

![Tableau de bord du modèle de notification de gestion des risques internes](../media/insider-risk-notices-dashboard.png)

## <a name="html-for-notices"></a><span data-ttu-id="cb983-116">HTML pour les notifications</span><span class="sxs-lookup"><span data-stu-id="cb983-116">HTML for notices</span></span>

<span data-ttu-id="cb983-117">Si vous souhaitez créer plus qu’un simple message électronique texte pour les notifications, vous pouvez créer un message plus détaillé à l’aide du code HTML dans le champ corps du message d’un modèle d’avis.</span><span class="sxs-lookup"><span data-stu-id="cb983-117">If you'd like to create more than a simple text-based email message for notifications, you can create a more detailed message by using HTML in the message body field of a notice template.</span></span> <span data-ttu-id="cb983-118">L’exemple suivant fournit le format du corps du message pour un modèle de notification par courrier électronique html de base :</span><span class="sxs-lookup"><span data-stu-id="cb983-118">The following example provides the message body format for a basic HTML-based email notification template:</span></span>

```HTML
<!DOCTYPE html>
<html>
<body>
<h2>Action Required: Contoso User Code of Conduct Policy Training</h2>
<p>A recent activity you've performed has generated a risk alert prohibited by the Contoso User <a href='https://www.contoso.com'>Code of Conduct Policy</a>.</p>
<p>You are required to attend the Contoso User Code of Conduct <a href='https://www.contoso.com'>training</a> within the next 14 days. Please contact <a href='mailto:hr@contoso.com'>Human Resources</a> with any questions about this training request.</p>
<p>Thank you,</p>
<p><em>Human Resources</em></p>
</body>
</html>
```

> [!NOTE]
> <span data-ttu-id="cb983-119">L’implémentation d’attribut href HTML dans les modèles d’avis de gestion des risques internes ne permet actuellement de prendre en charge que des guillemets simples au lieu de guillemets doubles pour les références d’URL.</span><span class="sxs-lookup"><span data-stu-id="cb983-119">HTML href attribute implementation in the insider risk management notice templates currently support only single quotation marks instead of double quotation marks for URL references.</span></span>

## <a name="create-a-new-notice-template"></a><span data-ttu-id="cb983-120">Créer un modèle d’avis</span><span class="sxs-lookup"><span data-stu-id="cb983-120">Create a new notice template</span></span>

<span data-ttu-id="cb983-121">Pour créer un modèle de notification de gestion des risques internes, vous utiliserez l’Assistant Notification dans la **solution** de gestion des risques internes dans le Centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cb983-121">To create a new insider risk management notice template, you'll use the notice wizard in **Insider risk management** solution in the Microsoft 365 compliance center.</span></span>

<span data-ttu-id="cb983-122">Pour créer un modèle d’avis de gestion des risques internes, complétez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb983-122">Complete the following steps to create a new insider risk management notice template:</span></span>

1. <span data-ttu-id="cb983-123">Dans le Centre de conformité [Microsoft 365,](https://compliance.microsoft.com)allez à **La** gestion des risques internes et sélectionnez l’onglet **Modèles de notification.**</span><span class="sxs-lookup"><span data-stu-id="cb983-123">In the [Microsoft 365 compliance center](https://compliance.microsoft.com), go to **Insider risk management** and select the **Notice templates** tab.</span></span>
2. <span data-ttu-id="cb983-124">Sélectionnez **Créer un modèle de notification** pour ouvrir l’Assistant Notification.</span><span class="sxs-lookup"><span data-stu-id="cb983-124">Select **Create notice template** to open the notice wizard.</span></span>
3. <span data-ttu-id="cb983-125">Dans la page **Créer un modèle d’avis,** complétez les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="cb983-125">On the **Create a new notice template** page, complete the following fields:</span></span>
    - <span data-ttu-id="cb983-126">**Nom du modèle**: entrez un nom convivial pour l’avis.</span><span class="sxs-lookup"><span data-stu-id="cb983-126">**Template name**: Enter a friendly name for the notice.</span></span> <span data-ttu-id="cb983-127">Ce nom apparaît dans la liste des notifications dans le tableau de bord de notification et dans la liste de sélection des notifications lors de l’envoi d’avis à partir d’un cas.</span><span class="sxs-lookup"><span data-stu-id="cb983-127">This name appears on the list of notices on the notice dashboard and in the notice selection list when sending notices from a case.</span></span>
    - <span data-ttu-id="cb983-128">**Envoyer à partir** de : Entrez l’adresse e-mail de l’expéditeur pour l’avis.</span><span class="sxs-lookup"><span data-stu-id="cb983-128">**Send from**: Enter the sender email address for the notice.</span></span> <span data-ttu-id="cb983-129">Cette adresse apparaît dans le champ **De :** dans toutes les notifications envoyées aux utilisateurs, sauf si elle est modifiée lors de l’envoi d’une notification à partir d’un cas.</span><span class="sxs-lookup"><span data-stu-id="cb983-129">This address will appear in the **From:** field in all notices sent to users unless changed when sending a notice from a case.</span></span>
    - <span data-ttu-id="cb983-130">Champs Cc et **Cci** : utilisateurs ou groupes facultatifs à notifiés de la correspondance de stratégie, sélectionnés dans Active Directory pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb983-130">**Cc and Bcc** fields: Optional users or groups to be notified of the policy match, selected from the Active Directory for your subscription.</span></span>
    - <span data-ttu-id="cb983-131">**Objet**: les informations qui apparaissent dans la ligne d’objet du message, prend en charge les caractères de texte.</span><span class="sxs-lookup"><span data-stu-id="cb983-131">**Subject**: Information that appears in the subject line of the message, supports text characters.</span></span>
    - <span data-ttu-id="cb983-132">**Corps du message**: informations qui apparaissent dans le corps du message, prend en charge les valeurs texte ou HTML.</span><span class="sxs-lookup"><span data-stu-id="cb983-132">**Message body**: Information that appears in the message body, supports text or HTML values.</span></span>
4. <span data-ttu-id="cb983-133">Sélectionnez **Créer** pour créer et enregistrer le modèle d’avis ou sélectionnez **Annuler** pour fermer sans enregistrer le modèle d’avis.</span><span class="sxs-lookup"><span data-stu-id="cb983-133">Select **Create** to create and save the notice template or select **Cancel** to close without saving the notice template.</span></span>

## <a name="update-a-notice-template"></a><span data-ttu-id="cb983-134">Mettre à jour un modèle d’avis</span><span class="sxs-lookup"><span data-stu-id="cb983-134">Update a notice template</span></span>

<span data-ttu-id="cb983-135">Pour mettre à jour un modèle de notification de gestion des risques internes existant, complétez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb983-135">To update an existing insider risk management notice template, complete the following steps:</span></span>

1. <span data-ttu-id="cb983-136">Dans le [Centre de conformité Microsoft 365,](https://compliance.microsoft.com)allez à **La** gestion des risques internes et sélectionnez l’onglet **Modèles de notification.**</span><span class="sxs-lookup"><span data-stu-id="cb983-136">In the [Microsoft 365 compliance center](https://compliance.microsoft.com), go to **Insider risk management** and select the **Notice templates** tab.</span></span>
2. <span data-ttu-id="cb983-137">Dans le tableau de bord de notification, sélectionnez le modèle de notification que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="cb983-137">On the notice dashboard, select the notice template you want to manage.</span></span>
3. <span data-ttu-id="cb983-138">Dans la page Détails de l’avis, sélectionnez **Modifier**</span><span class="sxs-lookup"><span data-stu-id="cb983-138">On the notice details page, select **Edit**</span></span>
4. <span data-ttu-id="cb983-139">Dans la page **Modifier,** vous pouvez modifier les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="cb983-139">On the **Edit** page, you can edit the following fields:</span></span>
    - <span data-ttu-id="cb983-140">**Nom du modèle**: entrez un nouveau nom convivial pour l’avis.</span><span class="sxs-lookup"><span data-stu-id="cb983-140">**Template name**: Enter a new friendly name for the notice.</span></span> <span data-ttu-id="cb983-141">Ce nom apparaît dans la liste des notifications dans le tableau de bord de notification et dans la liste de sélection des notifications lors de l’envoi d’avis à partir d’un cas.</span><span class="sxs-lookup"><span data-stu-id="cb983-141">This name appears on the list of notices on the notice dashboard and in the notice selection list when sending notices from a case.</span></span>
    - <span data-ttu-id="cb983-142">**Envoyer à partir de**: mettre à jour l’adresse e-mail de l’expéditeur pour l’avis.</span><span class="sxs-lookup"><span data-stu-id="cb983-142">**Send from**: Update the sender email address for the notice.</span></span> <span data-ttu-id="cb983-143">Cette adresse apparaît dans le champ **De :** dans toutes les notifications envoyées aux utilisateurs, sauf si elle est modifiée lors de l’envoi d’une notification à partir d’un cas.</span><span class="sxs-lookup"><span data-stu-id="cb983-143">This address will appear in the **From:** field in all notices sent to users unless changed when sending a notice from a case.</span></span>
    - <span data-ttu-id="cb983-144">Champs Cc et **Cci** : mettez à jour les utilisateurs ou groupes facultatifs pour être avertis de la correspondance de stratégie, sélectionnée dans Active Directory pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb983-144">**Cc and Bcc** fields: Update optional users or groups to be notified of the policy match, selected from the Active Directory for your subscription.</span></span>
    - <span data-ttu-id="cb983-145">**Objet**: mettre à jour les informations qui apparaissent dans la ligne d’objet du message, prend en charge les caractères de texte.</span><span class="sxs-lookup"><span data-stu-id="cb983-145">**Subject**: Update information that appears in the subject line of the message, supports text characters.</span></span>
    - <span data-ttu-id="cb983-146">**Corps du message**: mettre à jour les informations qui apparaissent dans le corps du message, prend en charge les valeurs texte ou HTML.</span><span class="sxs-lookup"><span data-stu-id="cb983-146">**Message body**: Update information that appears in the message body, supports text or HTML values.</span></span>
5. <span data-ttu-id="cb983-147">Sélectionnez **Enregistrer** pour mettre à jour et enregistrer l’avis ou sélectionnez **Annuler** pour fermer sans enregistrer le modèle d’avis.</span><span class="sxs-lookup"><span data-stu-id="cb983-147">Select **Save** to update and save the notice or select **Cancel** to close without saving the notice template.</span></span>

## <a name="delete-a-notice-template"></a><span data-ttu-id="cb983-148">Supprimer un modèle d’avis</span><span class="sxs-lookup"><span data-stu-id="cb983-148">Delete a notice template</span></span>

<span data-ttu-id="cb983-149">Pour supprimer un modèle de notification de gestion des risques internes existant, complétez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb983-149">To delete an existing insider risk management notice template, complete the following steps:</span></span>

1. <span data-ttu-id="cb983-150">Dans le Centre de conformité [Microsoft 365,](https://compliance.microsoft.com)allez à **La** gestion des risques internes et sélectionnez l’onglet **Modèles de notification.**</span><span class="sxs-lookup"><span data-stu-id="cb983-150">In the [Microsoft 365 compliance center](https://compliance.microsoft.com), go to **Insider risk management** and select the **Notice templates** tab.</span></span>
2. <span data-ttu-id="cb983-151">Dans le tableau de bord de notification, sélectionnez le modèle de notification à supprimer.</span><span class="sxs-lookup"><span data-stu-id="cb983-151">On the notice dashboard, select the notice template you want to delete.</span></span>
3. <span data-ttu-id="cb983-152">Sélectionnez **l’icône** Supprimer dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="cb983-152">Select the **Delete** icon on the toolbar.</span></span>
4. <span data-ttu-id="cb983-153">Pour supprimer le modèle d’avis, sélectionnez **Oui** dans la boîte de dialogue de suppression.</span><span class="sxs-lookup"><span data-stu-id="cb983-153">To delete the notice template, select **Yes** in the delete dialog.</span></span> <span data-ttu-id="cb983-154">Pour annuler la suppression, sélectionnez **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="cb983-154">To cancel the deletion, select **Cancel**.</span></span>

---
title: Prise en main du scanner local de protection contre la perte de données Microsoft 365 (préversion)
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: how-to
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
search.appverid:
- MET150
description: Configurer un scanneur local de protection contre la perte de données Microsoft 365
ms.openlocfilehash: 0390ac48b351b30b75109a3e3a5d18c80847c9d2
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53289198"
---
# <a name="get-started-with-the-data-loss-prevention-on-premises-scanner-preview"></a><span data-ttu-id="01f83-103">Prise en main du scanneur local de protection contre la perte de données (préversion)</span><span class="sxs-lookup"><span data-stu-id="01f83-103">Get started with the data loss prevention on-premises scanner (preview)</span></span>

<span data-ttu-id="01f83-104">Cet article décrit les conditions préalables et la configuration du scanneur de protection contre la perte de données Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="01f83-104">This article walks you through the prerequisites and configuration for the Microsoft 365 data loss prevention on-premises scanner.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="01f83-105">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="01f83-105">Before you begin</span></span>

### <a name="skusubscriptions-licensing"></a><span data-ttu-id="01f83-106">Licences SKU/abonnements</span><span class="sxs-lookup"><span data-stu-id="01f83-106">SKU/subscriptions licensing</span></span>

<span data-ttu-id="01f83-107">Avant de commencer à utiliser le scanneur local de DLP, vous devez confirmer votre [abonnement Microsoft 365](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) et tous les modules complémentaires.</span><span class="sxs-lookup"><span data-stu-id="01f83-107">Before you get started with DLP on-premises scanner, you should confirm your [Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) and any add-ons.</span></span> <span data-ttu-id="01f83-108">Pour participer à la préversion du compte d’administrateur qui définit les règles DLP, une des licences suivantes doit être attribuée :</span><span class="sxs-lookup"><span data-stu-id="01f83-108">To participate in the preview the admin account that sets up the DLP rules must be assigned one of the following licenses:</span></span>

- <span data-ttu-id="01f83-109">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="01f83-109">Microsoft 365 E5</span></span>
- <span data-ttu-id="01f83-110">Microsoft 365 E5 Conformité</span><span class="sxs-lookup"><span data-stu-id="01f83-110">Microsoft 365 E5 Compliance</span></span>
- <span data-ttu-id="01f83-111">Microsoft 365 E5, Protection des informations et gouvernance</span><span class="sxs-lookup"><span data-stu-id="01f83-111">Microsoft 365 E5 Information Protection & Governance</span></span> 


<span data-ttu-id="01f83-112">Pour plus d’informations sur les licences, consultez [instructions relatives aux licences Microsoft 365 pour la sécurité et la conformité](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance)</span><span class="sxs-lookup"><span data-stu-id="01f83-112">For full licensing details see: [Microsoft 365 licensing guidance for security & compliance](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance)</span></span>

### <a name="permissions"></a><span data-ttu-id="01f83-113">Autorisations</span><span class="sxs-lookup"><span data-stu-id="01f83-113">Permissions</span></span>


<span data-ttu-id="01f83-114">Les données du scanneur local de protection contre la perte de données peuvent être affichées dans [l’Explorateur d’activités](data-classification-activity-explorer.md).</span><span class="sxs-lookup"><span data-stu-id="01f83-114">Data from DLP on-premises scanner can be viewed in [Activity explorer](data-classification-activity-explorer.md).</span></span> <span data-ttu-id="01f83-115">Il existe quatre rôles qui accordent l’autorisation à l’Explorateur d’activités, le compte que vous utilisez pour accéder aux données doit être membre de l’un d’eux.</span><span class="sxs-lookup"><span data-stu-id="01f83-115">There are four roles that grant permission to activity explorer, the account you use for accessing the data must be a member of any one of them.</span></span>

- <span data-ttu-id="01f83-116">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="01f83-116">Global administrator</span></span>
- <span data-ttu-id="01f83-117">Administrateur de conformité</span><span class="sxs-lookup"><span data-stu-id="01f83-117">Compliance administrator</span></span>
- <span data-ttu-id="01f83-118">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="01f83-118">Security administrator</span></span>
- <span data-ttu-id="01f83-119">Administrateur de conformité des données</span><span class="sxs-lookup"><span data-stu-id="01f83-119">Compliance data administrator</span></span>

### <a name="dlp-on-premises-scanner-prerequisites"></a><span data-ttu-id="01f83-120">Conditions préalables pour un scanneur local de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="01f83-120">DLP on-premises scanner prerequisites</span></span>

- <span data-ttu-id="01f83-p103">Le scanneur Azure Information Protection (AIP) implémente la correspondance des stratégies DLP et l’application de stratégies. Le scanneur est installé dans le cadre du client AIP. Votre installation doit donc satisfaire toutes les conditions préalables requises pour AIP, le client AIP et le scanneur d’étiquetage unifié AIP.</span><span class="sxs-lookup"><span data-stu-id="01f83-p103">The Azure Information Protection (AIP) scanner implements DLP policy matching and policy enforcement. The scanner is installed as part of the AIP client so your installation must meet all the prerequisites  for AIP, the AIP client, and the AIP unified labeling scanner.</span></span>
- <span data-ttu-id="01f83-123">Déployer le client et le scanneur AIP.</span><span class="sxs-lookup"><span data-stu-id="01f83-123">Deploy the AIP  client and scanner.</span></span> <span data-ttu-id="01f83-124">Pour plus d’informations [Installez le client d'étiquetage unifié AIP](/azure/information-protection/rms-client/install-unifiedlabelingclient-app) et consultez [Configuration et installation du scanneur d’étiquetage unifié Azure Information Protection](/azure/information-protection/deploy-aip-scanner-configure-install).</span><span class="sxs-lookup"><span data-stu-id="01f83-124">For more information [Install the AIP unified labeling client](/azure/information-protection/rms-client/install-unifiedlabelingclient-app) and [], see [Configuring and installing the Azure Information Protection unified labeling scanner](/azure/information-protection/deploy-aip-scanner-configure-install).</span></span>
- <span data-ttu-id="01f83-125">Au moins une étiquette et une stratégie doivent être publiées dans le client, même si toutes vos règles de détection ne sont basées que sur des types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="01f83-125">There must be at least one label and policy published in the tenant, even if all your detection rules are based on sensitive information types only.</span></span>

## <a name="deploy-the-dlp-on-premises-scanner"></a><span data-ttu-id="01f83-126">Déployer un scanneur local de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="01f83-126">Deploy the DLP on-premises scanner</span></span>

1. <span data-ttu-id="01f83-127">Suivez les procédures dans [Installer le client d’étiquetage unifié AIP](/azure/information-protection/rms-client/install-unifiedlabelingclient-app).</span><span class="sxs-lookup"><span data-stu-id="01f83-127">Follow the procedures in [Install the AIP unified labeling client](/azure/information-protection/rms-client/install-unifiedlabelingclient-app).</span></span> 
2. <span data-ttu-id="01f83-128">Pour terminer l’installation du scanneur, suivez les procédures dans[Configuration et l’installation du scanneur d’étiquetage unifié Azure Information Protection](/azure/information-protection/deploy-aip-scanner-configure-install).</span><span class="sxs-lookup"><span data-stu-id="01f83-128">Follow the procedures in [Configuring and installing the Azure Information Protection unified labeling scanner](/azure/information-protection/deploy-aip-scanner-configure-install) to complete the scanner installation.</span></span>
    1. <span data-ttu-id="01f83-129">La configuration des tâches de découverte réseau est une étape facultative.</span><span class="sxs-lookup"><span data-stu-id="01f83-129">Network discovery jobs configuration is an optional step.</span></span> <span data-ttu-id="01f83-130">Vous pouvez l’ignorer et définir des référentiels spécifiques à numériser dans votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="01f83-130">You can skip it and define specific repositories to be scanned in your content scan job.</span></span>
    2. <span data-ttu-id="01f83-131">Vous devez créer un travail d’analyse de contenu et spécifier les référentiels qui hébergent les fichiers qui doivent être évalués par le moteur DLP.</span><span class="sxs-lookup"><span data-stu-id="01f83-131">You must create content scan job and specify the repositories that host files that need to be evaluated by the DLP engine.</span></span>
    3. <span data-ttu-id="01f83-132">Activez les règles DLP dans la tâche d’analyse de contenu créée et définissez l’option **Appliquer** sur **Désactivé**, sauf si vous voulez passer directement à la phase d’application de la DLP.</span><span class="sxs-lookup"><span data-stu-id="01f83-132">Enable DLP rules in the created Content scan job, and set the **Enforce** option to **Off**, unless you want to proceed directly to the DLP enforcement stage.</span></span>
3. <span data-ttu-id="01f83-p106">Vérifiez que la tâche d’analyse de contenu est affectée au bon cluster. Si vous n'avez toujours pas créé de tâche d'analyse de contenu, créez-en une nouvelle et affectez-la au cluster qui contient les nœuds d'analyse qui exécutent la version d'aperçu public.</span><span class="sxs-lookup"><span data-stu-id="01f83-p106">Verify that you content scan job is assigned to the right cluster. If you still did not create a content scan job create a new one and assign it to the cluster that contains the scanner nodes that run the public preview version.</span></span>

4. <span data-ttu-id="01f83-135">Connectez-vous à [Extension Azure Information Protection dans le Portail Azure](https://portal.azure.com/#blade/Microsoft_Azure_InformationProtection/DataClassGroupEditBlade/scannerProfilesBlade) et ajoutez vos référentiels à la tâche d’analyse de contenu qui effectuera l’analyse.</span><span class="sxs-lookup"><span data-stu-id="01f83-135">Connect to the [Azure Information Protection extension in Azure portal](https://portal.azure.com/#blade/Microsoft_Azure_InformationProtection/DataClassGroupEditBlade/scannerProfilesBlade) and add your repositories to the content scan job that will perform the scan.</span></span>

5. <span data-ttu-id="01f83-136">Pour exécuter votre analyse, exécutez l’une des analyses suivantes :</span><span class="sxs-lookup"><span data-stu-id="01f83-136">Do one of the following to run your scan:</span></span>
    1. <span data-ttu-id="01f83-137">définir le planning du scanneur</span><span class="sxs-lookup"><span data-stu-id="01f83-137">set the scanner schedule</span></span>
    1. <span data-ttu-id="01f83-138">utiliser l’option manuel **Analyser maintenant** dans le portail</span><span class="sxs-lookup"><span data-stu-id="01f83-138">use the manual **Scan Now** option in the portal</span></span>
    1. <span data-ttu-id="01f83-139">ou exécuter l’applet de commande PowerShell **Start-AIPScan**</span><span class="sxs-lookup"><span data-stu-id="01f83-139">or run **Start-AIPScan** PowerShell cmdlet</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="01f83-140">N'oubliez pas que le scanneur effectue par défaut une analyse delta du référentiel et que les fichiers qui ont déjà été analysés lors du cycle d'analyse précédent seront ignorés, sauf si le fichier a été modifié ou si vous avez lancé une nouvelle analyse complète.</span><span class="sxs-lookup"><span data-stu-id="01f83-140">Remember that the scanner runs a delta scan of the repository by default and the files that were already scanned in the previous scan cycle will be skipped unless the file was changed or you initiated a full rescan.</span></span> <span data-ttu-id="01f83-141">La nouvelle analyse complète peut être lancée en utilisant l'option **Relancer l’analyse de tous les fichiers** dans l'interface utilisateur ou en exécutant **Start-AIPScan-Reset**.</span><span class="sxs-lookup"><span data-stu-id="01f83-141">Full rescan can be initiated by using **Rescan all files** option in the UI or by running **Start-AIPScan-Reset**.</span></span>

6.  <span data-ttu-id="01f83-142">Ouvrez la page de [Protection contre la perte de données](https://compliance.microsoft.com/datalossprevention?viewid=policies) dans le Centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="01f83-142">Open the [Data loss prevention page](https://compliance.microsoft.com/datalossprevention?viewid=policies) in the Microsoft 365 Compliance center.</span></span>

7. <span data-ttu-id="01f83-143">Choisissez **Créer une stratégie** et créez une stratégie DLP de test.</span><span class="sxs-lookup"><span data-stu-id="01f83-143">Choose **Create policy** and create a test DLP policy.</span></span> <span data-ttu-id="01f83-144">Consultez [Créer une stratégie DLP à partir d’un modèle](create-a-dlp-policy-from-a-template.md) si vous avez besoin d’aide pour créer une stratégie.</span><span class="sxs-lookup"><span data-stu-id="01f83-144">See [Create a DLP policy from a template](create-a-dlp-policy-from-a-template.md) if you need help creating a policy.</span></span> <span data-ttu-id="01f83-145">N’oubliez pas de l’exécuter à l’essai jusqu’à ce que vous soyez à l’aise avec cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="01f83-145">Be sure to run it in test until you are comfortable with this feature.</span></span> <span data-ttu-id="01f83-146">Utilisez les paramètres suivants pour votre stratégie :</span><span class="sxs-lookup"><span data-stu-id="01f83-146">Use these parameters for your policy:</span></span>
    1. <span data-ttu-id="01f83-147">Limitez la règle du scanneur local de protection contre la perte de données à des emplacements spécifiques si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="01f83-147">Scope the DLP on-premises scanner rule to specific locations if needed.</span></span> <span data-ttu-id="01f83-148">Si vous définissez les **emplacements** comme **Tous**, tous les fichiers analysés par le scanneur seront soumis à la règle de correspondance et d'application du DLP.</span><span class="sxs-lookup"><span data-stu-id="01f83-148">If you scope **locations** to **All**, all files scanned by the scanner will be subject to the DLP rule matching and enforcement.</span></span>
    1. <span data-ttu-id="01f83-149">Lorsque vous spécifiez les emplacements, vous pouvez utiliser une liste d’exclusion ou d’inclusion.</span><span class="sxs-lookup"><span data-stu-id="01f83-149">When specifying the locations, you can use either exclusion or inclusion list.</span></span> <span data-ttu-id="01f83-150">Pendant la préversion publique, vous ne pouvez pas définir les deux.</span><span class="sxs-lookup"><span data-stu-id="01f83-150">During public preview you cannot set both of them.</span></span> <span data-ttu-id="01f83-151">Vous pouvez soit définir que la règle ne s'applique qu'aux chemins d'accès correspondant à l'un des modèles figurant dans la liste d'inclusion, soit à tous les fichiers, à l'exception des fichiers correspondant au modèle figurant dans la liste d'inclusion.</span><span class="sxs-lookup"><span data-stu-id="01f83-151">You can either define that the rule is relevant only to paths matching one of the patterns listed in inclusion list or, all files, except the files matching the pattern listed in inclusion list.</span></span> <span data-ttu-id="01f83-152">Aucun chemin d’accès local n’est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="01f83-152">No local paths are supported.</span></span> <span data-ttu-id="01f83-153">Voici quelques exemples de chemins d’accès valides :</span><span class="sxs-lookup"><span data-stu-id="01f83-153">Here are some examples of valid paths:</span></span>
      - <span data-ttu-id="01f83-154">\\\server\share</span><span class="sxs-lookup"><span data-stu-id="01f83-154">\\\server\share</span></span>
      - <span data-ttu-id="01f83-155">\\\server\share\folder1\subfolderabc</span><span class="sxs-lookup"><span data-stu-id="01f83-155">\\\server\share\folder1\subfolderabc</span></span>
      - <span data-ttu-id="01f83-156">\*\\dossier1</span><span class="sxs-lookup"><span data-stu-id="01f83-156">\*\\folder1</span></span>
      - <span data-ttu-id="01f83-157">\*secret\*.docx</span><span class="sxs-lookup"><span data-stu-id="01f83-157">\*secret\*.docx</span></span>
      - <span data-ttu-id="01f83-158">\*secret\*.\*</span><span class="sxs-lookup"><span data-stu-id="01f83-158">\*secret\*.\*</span></span>
      - <span data-ttu-id="01f83-159"> https:// sp2010.local/sites/HR</span><span class="sxs-lookup"><span data-stu-id="01f83-159">https:// sp2010.local/sites/HR</span></span>
      - <span data-ttu-id="01f83-160"> https://\*/HR</span><span class="sxs-lookup"><span data-stu-id="01f83-160">https://\*/HR</span></span> 
    3. <span data-ttu-id="01f83-161">Voici quelques exemples d'utilisation de valeurs inacceptables :</span><span class="sxs-lookup"><span data-stu-id="01f83-161">Here are some examples of unacceptable values use:</span></span>
      - \*
      - <span data-ttu-id="01f83-162">\*\\a</span><span class="sxs-lookup"><span data-stu-id="01f83-162">\*\\a</span></span>
      - <span data-ttu-id="01f83-163">Aaa</span><span class="sxs-lookup"><span data-stu-id="01f83-163">Aaa</span></span>
      - <span data-ttu-id="01f83-164">c:</span><span class="sxs-lookup"><span data-stu-id="01f83-164">c:</span></span>\
      - <span data-ttu-id="01f83-165">C:\test</span><span class="sxs-lookup"><span data-stu-id="01f83-165">C:\test</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01f83-166">La liste d'exclusion a la priorité sur la liste d'inclusion.</span><span class="sxs-lookup"><span data-stu-id="01f83-166">The exclusion list takes precedence over the inclusions list.</span></span>

### <a name="viewing-dlp-on-premises-scanner-alerts-in-dlp-alerts-management-dashboard"></a><span data-ttu-id="01f83-167">Affichage des alertes du scanneur local de protection contre la perte de données dans le tableau de bord de Gestion des alertes DLP</span><span class="sxs-lookup"><span data-stu-id="01f83-167">Viewing DLP on-premises scanner alerts in DLP Alerts Management dashboard</span></span>

1. <span data-ttu-id="01f83-168">Ouvrez la page de [Protection contre la perte de données](https://compliance.microsoft.com/datalossprevention?viewid=policies) dans le Centre de conformité Microsoft 365, puis sélectionnez **Alertes**.</span><span class="sxs-lookup"><span data-stu-id="01f83-168">Open the [Data loss prevention page](https://compliance.microsoft.com/datalossprevention?viewid=policies) in the Microsoft 365 Compliance center and select **Alerts**.</span></span>

2. <span data-ttu-id="01f83-169">Reportez-vous aux procédures décrites dans [Comment configurer et afficher les alertes pour les stratégies DLP](dlp-configure-view-alerts-policies.md) pour afficher les alertes relatives à vos stratégies DLP de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="01f83-169">Refer to the procedures in [How to configure and view alerts for your DLP policies](dlp-configure-view-alerts-policies.md) to view alerts for your Endpoint DLP policies.</span></span>

### <a name="viewing-dlp-on-premises-scanner-in-activity-explorer-and-audit-log"></a><span data-ttu-id="01f83-170">Affichage du scanneur local de protection contre la perte de données dans l’Explorateur d’activités et le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="01f83-170">Viewing DLP on-premises scanner in activity explorer and audit log</span></span>

> [!NOTE]
> <span data-ttu-id="01f83-171">Le scanneur local nécessite que l’audit soit activé.</span><span class="sxs-lookup"><span data-stu-id="01f83-171">The on-premises scanner requires that auditing be enabled.</span></span> <span data-ttu-id="01f83-172">L’audit Microsoft 365 est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="01f83-172">In Microsoft 365 auditing is enabled by default.</span></span>

1. <span data-ttu-id="01f83-173">Ouvrez la [Page classification des données](https://compliance.microsoft.com/dataclassification?viewid=overview) pour votre domaine dans le centre de conformité Microsoft 365, puis sélectionnez Explorateur d’activités.</span><span class="sxs-lookup"><span data-stu-id="01f83-173">Open the [Data classification page](https://compliance.microsoft.com/dataclassification?viewid=overview) for your domain in the Microsoft 365 Compliance center and select Activity explorer.</span></span>

2. <span data-ttu-id="01f83-174">Reportez-vous aux procédures décrites dans [Prise en main de l’Explorateur d’activités](data-classification-activity-explorer.md) pour accéder aux données de vos emplacements de scanneur local.</span><span class="sxs-lookup"><span data-stu-id="01f83-174">Refer to the procedures in [Get started with Activity explorer](data-classification-activity-explorer.md) to access and filter all the data for your on-premises scanner locations.</span></span>

3. <span data-ttu-id="01f83-175">Ouvrir le [Journal d'audit dans le Centre de conformité](https://security.microsoft.com/auditlogsearch).</span><span class="sxs-lookup"><span data-stu-id="01f83-175">Open the [Audit log in the Compliance center](https://security.microsoft.com/auditlogsearch).</span></span> <span data-ttu-id="01f83-176">Pendant la préversion publique, les correspondances de règle DLP sont disponibles dans l’interface utilisateur du journal d’audit ou accessibles par [Search-UnifiedAuditLog](/powershell/module/exchange/search-unifiedauditlog) PowerShell</span><span class="sxs-lookup"><span data-stu-id="01f83-176">During the public preview the DLP rule matches are available in Audit log UI or accessible by [Search-UnifiedAuditLog](/powershell/module/exchange/search-unifiedauditlog) PowerShell</span></span> 


## <a name="next-steps"></a><span data-ttu-id="01f83-177">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="01f83-177">Next steps</span></span>
<span data-ttu-id="01f83-178">Maintenant que vous avez déployé une stratégie de test pour les emplacements locaux de protection contre la perte de données et que vous pouvez afficher les données d’activité dans l’Explorateur d’activités, vous êtes prêt à passer à l’étape suivante dans laquelle vous créez des stratégies DLP qui protègent vos éléments sensibles.</span><span class="sxs-lookup"><span data-stu-id="01f83-178">Now that you have deployed a test policy for DLP on-premises locations and can view the activity data in Activity explorer, you are ready to move on to your next step where you create DLP policies that protect your sensitive items.</span></span>

- [<span data-ttu-id="01f83-179">Utilisation de DLP en local (préversion)</span><span class="sxs-lookup"><span data-stu-id="01f83-179">Using DLP on-premises (preview)</span></span>](dlp-on-premises-scanner-use.md)

## <a name="see-also"></a><span data-ttu-id="01f83-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01f83-180">See also</span></span>

- [<span data-ttu-id="01f83-181">En savoir plus sur le scanneur local de protection contre la perte de données (préversion)</span><span class="sxs-lookup"><span data-stu-id="01f83-181">Learn about DLP on-premises scanner (preview)</span></span>](dlp-on-premises-scanner-learn.md)
- [<span data-ttu-id="01f83-182">Utiliser le scanneur local de protection contre la perte de données (préversion)</span><span class="sxs-lookup"><span data-stu-id="01f83-182">Use DLP on-premises scanner (preview)</span></span>](dlp-on-premises-scanner-use.md)
- [<span data-ttu-id="01f83-183">En savoir plus sur la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="01f83-183">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)
- [<span data-ttu-id="01f83-184">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="01f83-184">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="01f83-185">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="01f83-185">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="01f83-186">Abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="01f83-186">Microsoft 365 subscription</span></span>](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1)
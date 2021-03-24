---
title: Score de sécurité Microsoft pour les appareils
description: Votre score pour les appareils indique l’état de configuration de sécurité collective de vos appareils dans les contrôles d’application, de système d’exploitation, de réseau, de comptes et de sécurité.
keywords: Degré de sécurisation Microsoft pour les appareils, degré de sécurisation Microsoft mdatp pour les appareils, degré de sécurité, score de configuration, gestion des menaces et vulnérabilités, contrôles de sécurité, opportunités d’amélioration, score de configuration de la sécurité au fil du temps, posture de sécurité, ligne de base
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: ellevin
author: levinec
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: d9ccd4f7dcc8b1546772a756aaf850dadfc87905
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51063750"
---
# <a name="microsoft-secure-score-for-devices"></a><span data-ttu-id="7ba96-104">Score de sécurité Microsoft pour les appareils</span><span class="sxs-lookup"><span data-stu-id="7ba96-104">Microsoft Secure Score for Devices</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="7ba96-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7ba96-105">**Applies to:**</span></span>

- [<span data-ttu-id="7ba96-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7ba96-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="7ba96-107">Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="7ba96-107">Threat and vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="7ba96-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="7ba96-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="7ba96-109">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="7ba96-109">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="7ba96-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="7ba96-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-pullalerts-abovefoldlink) 


>[!NOTE]
> <span data-ttu-id="7ba96-111">Le score de configuration fait désormais partie de la gestion des menaces et des vulnérabilités en tant que Degré de sécurisation Microsoft pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="7ba96-111">Configuration score is now part of threat and vulnerability management as Microsoft Secure Score for Devices.</span></span>

<span data-ttu-id="7ba96-112">Votre score pour les appareils est visible dans le [tableau](tvm-dashboard-insights.md) de bord de gestion des menaces et des vulnérabilités du Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="7ba96-112">Your score for devices is visible in the [threat and vulnerability management dashboard](tvm-dashboard-insights.md) of the Microsoft Defender Security Center.</span></span> <span data-ttu-id="7ba96-113">Un niveau de sécurité Microsoft plus élevé pour les appareils signifie que vos points de terminaison sont plus résistants aux attaques contre les menaces de cybersécurité.</span><span class="sxs-lookup"><span data-stu-id="7ba96-113">A higher Microsoft Secure Score for Devices means your endpoints are more resilient from cybersecurity threat attacks.</span></span> <span data-ttu-id="7ba96-114">Elle reflète l’état de configuration de sécurité collective de vos appareils dans les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ba96-114">It reflects the collective security configuration state of your devices across the following categories:</span></span>

- <span data-ttu-id="7ba96-115">Application</span><span class="sxs-lookup"><span data-stu-id="7ba96-115">Application</span></span>
- <span data-ttu-id="7ba96-116">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="7ba96-116">Operating system</span></span>
- <span data-ttu-id="7ba96-117">Réseau</span><span class="sxs-lookup"><span data-stu-id="7ba96-117">Network</span></span>
- <span data-ttu-id="7ba96-118">Comptes</span><span class="sxs-lookup"><span data-stu-id="7ba96-118">Accounts</span></span>
- <span data-ttu-id="7ba96-119">Contrôles de sécurité</span><span class="sxs-lookup"><span data-stu-id="7ba96-119">Security controls</span></span>

<span data-ttu-id="7ba96-120">Sélectionnez une catégorie pour aller à la page [**Recommandations de sécurité**](tvm-security-recommendation.md) et afficher les recommandations pertinentes.</span><span class="sxs-lookup"><span data-stu-id="7ba96-120">Select a category to go to the [**Security recommendations**](tvm-security-recommendation.md) page and view the relevant recommendations.</span></span>

## <a name="turn-on-the-microsoft-secure-score-connector"></a><span data-ttu-id="7ba96-121">Activer le connecteur Score de sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="7ba96-121">Turn on the Microsoft Secure Score connector</span></span>

<span data-ttu-id="7ba96-122">Avancez les signaux de Microsoft Defender pour les points de terminaison, ce qui permet à Microsoft Secure Score de se rendre compte de la posture de sécurité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7ba96-122">Forward Microsoft Defender for Endpoint signals, giving Microsoft Secure Score visibility into the device security posture.</span></span> <span data-ttu-id="7ba96-123">Les données forwardées sont stockées et traitées au même emplacement que vos données du Score de sécurisation Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ba96-123">Forwarded data is stored and processed in the same location as your Microsoft Secure Score data.</span></span>

<span data-ttu-id="7ba96-124">La réflexion des modifications dans le tableau de bord peut prendre jusqu’à quelques heures.</span><span class="sxs-lookup"><span data-stu-id="7ba96-124">Changes might take up to a few hours to reflect in the dashboard.</span></span>

1. <span data-ttu-id="7ba96-125">Dans le volet de navigation, go to **Settings**  >  **Advanced features**</span><span class="sxs-lookup"><span data-stu-id="7ba96-125">In the navigation pane, go to **Settings** > **Advanced features**</span></span> 

2. <span data-ttu-id="7ba96-126">Faites défiler vers **le bas jusqu’au score de sécurité Microsoft** et basculez le paramètre sur **Sur**.</span><span class="sxs-lookup"><span data-stu-id="7ba96-126">Scroll down to **Microsoft Secure Score** and toggle the setting to **On**.</span></span>

3. <span data-ttu-id="7ba96-127">Sélectionnez **Enregistrer les préférences.**</span><span class="sxs-lookup"><span data-stu-id="7ba96-127">Select **Save preferences**.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="7ba96-128">Mode de fonctionnement</span><span class="sxs-lookup"><span data-stu-id="7ba96-128">How it works</span></span>

>[!NOTE]
> <span data-ttu-id="7ba96-129">Le score de sécurité Microsoft pour les appareils prend actuellement en charge les configurations définies via la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="7ba96-129">Microsoft Secure Score for Devices currently supports configurations set via Group Policy.</span></span> <span data-ttu-id="7ba96-130">En raison de la prise en charge partielle actuelle d’Intune, les configurations qui ont peut-être été définies via Intune peuvent s’afficher comme mal configurées.</span><span class="sxs-lookup"><span data-stu-id="7ba96-130">Due to the current partial Intune support, configurations which might have been set through Intune might show up as misconfigured.</span></span> <span data-ttu-id="7ba96-131">Contactez votre administrateur informatique pour vérifier l’état réel de la configuration au cas où votre organisation utiliserait Intune pour la gestion de la configuration sécurisée.</span><span class="sxs-lookup"><span data-stu-id="7ba96-131">Contact your IT Administrator to verify the actual configuration status in case your organization is using Intune for secure configuration management.</span></span>

<span data-ttu-id="7ba96-132">Les données de la carte Degré de sécurisation Microsoft pour les appareils sont le produit d’un processus de découverte de vulnérabilité en cours et d’activités.</span><span class="sxs-lookup"><span data-stu-id="7ba96-132">The data in the Microsoft Secure Score for Devices card is the product of meticulous and ongoing vulnerability discovery process.</span></span> <span data-ttu-id="7ba96-133">Elle est agrégée aux évaluations de découverte de configuration qui :</span><span class="sxs-lookup"><span data-stu-id="7ba96-133">It is aggregated with configuration discovery assessments that continuously:</span></span>

- <span data-ttu-id="7ba96-134">Comparer les configurations collectées aux critères collectés pour découvrir les ressources mal configurées</span><span class="sxs-lookup"><span data-stu-id="7ba96-134">Compare collected configurations to the collected benchmarks to discover misconfigured assets</span></span>
- <span data-ttu-id="7ba96-135">Masqué les configurations sur des vulnérabilités qui peuvent être corrigés ou partiellement corrigés (réduction des risques)</span><span class="sxs-lookup"><span data-stu-id="7ba96-135">Map configurations to vulnerabilities that can be remediated or partially remediated (risk reduction)</span></span>
- <span data-ttu-id="7ba96-136">Collecter et gérer les critères de configuration des meilleures pratiques (fournisseurs, flux de sécurité, équipes de recherche internes)</span><span class="sxs-lookup"><span data-stu-id="7ba96-136">Collect and maintain best practice configuration benchmarks (vendors, security feeds, internal research teams)</span></span>
- <span data-ttu-id="7ba96-137">Collecter et surveiller les modifications de l’état de configuration du contrôle de sécurité de toutes les ressources</span><span class="sxs-lookup"><span data-stu-id="7ba96-137">Collect and monitor changes of security control configuration state from all assets</span></span>

## <a name="improve-your-security-configuration"></a><span data-ttu-id="7ba96-138">Améliorer votre configuration de la sécurité</span><span class="sxs-lookup"><span data-stu-id="7ba96-138">Improve your security configuration</span></span>

<span data-ttu-id="7ba96-139">Améliorez votre configuration de la sécurité en remédiant aux problèmes de la liste des recommandations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="7ba96-139">Improve your security configuration by remediating issues from the security recommendations list.</span></span> <span data-ttu-id="7ba96-140">À mesure que vous le faites, votre score de sécurité Microsoft pour les appareils s’améliore et votre organisation devient plus résiliente contre les menaces et les vulnérabilités de cybersécurité.</span><span class="sxs-lookup"><span data-stu-id="7ba96-140">As you do so, your Microsoft Secure Score for Devices improves and your organization becomes more resilient against cybersecurity threats and vulnerabilities.</span></span>

1. <span data-ttu-id="7ba96-141">À partir de la carte Degré de sécurisation Microsoft pour les appareils dans le tableau de bord de gestion des menaces et des vulnérabilités, sélectionnez l’une des catégories.</span><span class="sxs-lookup"><span data-stu-id="7ba96-141">From the Microsoft Secure Score for Devices card in the threat and vulnerability management dashboard, select the one of the categories.</span></span> <span data-ttu-id="7ba96-142">Vous verrez la liste des recommandations relatives à cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="7ba96-142">You'll view the list of recommendations related to that category.</span></span> <span data-ttu-id="7ba96-143">Il vous permet d’aller à la page [**Recommandations en matière de sécurité.**](tvm-security-recommendation.md)</span><span class="sxs-lookup"><span data-stu-id="7ba96-143">It will take you to the [**Security recommendations**](tvm-security-recommendation.md) page.</span></span> <span data-ttu-id="7ba96-144">Si vous souhaitez voir toutes les recommandations de sécurité, une fois que vous êtes sur la page Recommandations de sécurité, effacer le champ de recherche.</span><span class="sxs-lookup"><span data-stu-id="7ba96-144">If you want to see all security recommendations, once you get to the Security recommendations page, clear the search field.</span></span>

2. <span data-ttu-id="7ba96-145">Sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="7ba96-145">Select an item on the list.</span></span> <span data-ttu-id="7ba96-146">Le panneau volant s’ouvre avec les détails relatifs à la recommandation.</span><span class="sxs-lookup"><span data-stu-id="7ba96-146">The flyout panel will open with details related to the recommendation.</span></span> <span data-ttu-id="7ba96-147">Sélectionnez **les options de correction.**</span><span class="sxs-lookup"><span data-stu-id="7ba96-147">Select **Remediation options**.</span></span>

   ![Recommandations en matière de sécurité liées aux contrôles de sécurité](images/tvm_security_controls.png)

3. <span data-ttu-id="7ba96-149">Lisez la description pour comprendre le contexte du problème et ce qu’il faut faire ensuite.</span><span class="sxs-lookup"><span data-stu-id="7ba96-149">Read the description to understand the context of the issue and what to do next.</span></span> <span data-ttu-id="7ba96-150">Sélectionnez une date d’échéance, ajoutez des notes et sélectionnez Exporter toutes les données d’activité de correction vers **CSV** afin de pouvoir les joindre à un e-mail pour le suivi.</span><span class="sxs-lookup"><span data-stu-id="7ba96-150">Select a due date, add notes, and select **Export all remediation activity data to CSV** so you can attach it to an email for follow-up.</span></span>

4. <span data-ttu-id="7ba96-151">**Envoyer une demande**.</span><span class="sxs-lookup"><span data-stu-id="7ba96-151">**Submit request**.</span></span> <span data-ttu-id="7ba96-152">Vous verrez un message de confirmation vous confirmant que la tâche de correction a été créée.</span><span class="sxs-lookup"><span data-stu-id="7ba96-152">You'll see a confirmation message that the remediation task has been created.</span></span>
   <span data-ttu-id="7ba96-153">![Confirmation de la création d’une tâche de correction](images/tvm_remediation_task_created.png)</span><span class="sxs-lookup"><span data-stu-id="7ba96-153">![Remediation task creation confirmation](images/tvm_remediation_task_created.png)</span></span>

5. <span data-ttu-id="7ba96-154">Enregistrez votre fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="7ba96-154">Save your CSV file.</span></span>
   <span data-ttu-id="7ba96-155">![Enregistrer un fichier csv](images/tvm_save_csv_file.png)</span><span class="sxs-lookup"><span data-stu-id="7ba96-155">![Save csv file](images/tvm_save_csv_file.png)</span></span>

6. <span data-ttu-id="7ba96-156">Envoyez un courrier électronique de suivi à votre administrateur informatique et laissez le temps que vous avez alloué à la correction de se propager dans le système.</span><span class="sxs-lookup"><span data-stu-id="7ba96-156">Send a follow-up email to your IT Administrator and allow the time that you've allotted for the remediation to propagate in the system.</span></span>

7. <span data-ttu-id="7ba96-157">Examinez **à nouveau la carte Score de sécurité Microsoft** pour les appareils dans le tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="7ba96-157">Review the **Microsoft Secure Score for Devices** card again on the dashboard.</span></span> <span data-ttu-id="7ba96-158">Le nombre de recommandations en matière de contrôles de sécurité va diminuer.</span><span class="sxs-lookup"><span data-stu-id="7ba96-158">The number of security controls recommendations will decrease.</span></span> <span data-ttu-id="7ba96-159">Lorsque vous **sélectionnez les contrôles** de sécurité pour revenir à la page **Recommandations** de sécurité, l’élément que vous avez traité n’y figure plus.</span><span class="sxs-lookup"><span data-stu-id="7ba96-159">When you select **Security controls** to go back to the **Security recommendations** page, the item that you've addressed won't be listed there anymore.</span></span> <span data-ttu-id="7ba96-160">Votre score de sécurité Microsoft pour les appareils doit augmenter.</span><span class="sxs-lookup"><span data-stu-id="7ba96-160">Your Microsoft Secure Score for Devices should increase.</span></span>

>[!IMPORTANT]
><span data-ttu-id="7ba96-161">Pour augmenter les taux de détection de l’évaluation des vulnérabilités, téléchargez les mises à jour de sécurité obligatoires suivantes et déployez-les sur votre réseau :</span><span class="sxs-lookup"><span data-stu-id="7ba96-161">To boost your vulnerability assessment detection rates, download the following mandatory security updates and deploy them in your network:</span></span>
>- <span data-ttu-id="7ba96-162">Clients 19H1 | [KB 4512941](https://support.microsoft.com/help/4512941/windows-10-update-kb4512941)</span><span class="sxs-lookup"><span data-stu-id="7ba96-162">19H1 customers | [KB 4512941](https://support.microsoft.com/help/4512941/windows-10-update-kb4512941)</span></span>
>- <span data-ttu-id="7ba96-163">Clients RS5 | [KB 4516077](https://support.microsoft.com/help/4516077/windows-10-update-kb4516077)</span><span class="sxs-lookup"><span data-stu-id="7ba96-163">RS5 customers | [KB 4516077](https://support.microsoft.com/help/4516077/windows-10-update-kb4516077)</span></span>
>- <span data-ttu-id="7ba96-164">Clients RS4 | [KB 4516045](https://support.microsoft.com/help/4516045/windows-10-update-kb4516045)</span><span class="sxs-lookup"><span data-stu-id="7ba96-164">RS4 customers | [KB 4516045](https://support.microsoft.com/help/4516045/windows-10-update-kb4516045)</span></span>
>- <span data-ttu-id="7ba96-165">Clients RS3 | [KB 4516071](https://support.microsoft.com/help/4516071/windows-10-update-kb4516071)</span><span class="sxs-lookup"><span data-stu-id="7ba96-165">RS3 customers | [KB 4516071](https://support.microsoft.com/help/4516071/windows-10-update-kb4516071)</span></span>
>
><span data-ttu-id="7ba96-166">Pour télécharger les mises à jour de sécurité :</span><span class="sxs-lookup"><span data-stu-id="7ba96-166">To download the security updates:</span></span>
>1. <span data-ttu-id="7ba96-167">Go to [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/home.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ba96-167">Go to [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/home.aspx).</span></span>
>2. <span data-ttu-id="7ba96-168">Key-in the security update KB number that you need to download, then click **Search**.</span><span class="sxs-lookup"><span data-stu-id="7ba96-168">Key-in the security update KB number that you need to download, then click **Search**.</span></span>  

## <a name="related-topics"></a><span data-ttu-id="7ba96-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ba96-169">Related topics</span></span>

- [<span data-ttu-id="7ba96-170">Vue d’ensemble de la gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="7ba96-170">Threat and vulnerability management overview</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="7ba96-171">Tableau de bord</span><span class="sxs-lookup"><span data-stu-id="7ba96-171">Dashboard</span></span>](tvm-dashboard-insights.md)
- [<span data-ttu-id="7ba96-172">Score d’exposition</span><span class="sxs-lookup"><span data-stu-id="7ba96-172">Exposure score</span></span>](tvm-exposure-score.md)
- [<span data-ttu-id="7ba96-173">Recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="7ba96-173">Security recommendations</span></span>](tvm-security-recommendation.md)

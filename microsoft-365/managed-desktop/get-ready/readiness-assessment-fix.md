---
title: Corriger les problèmes détectés par l’outil d’évaluation de la disponibilité
description: Actions détaillées à effectuer pour chaque problème rencontré par l’outil
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: 642de80e1a133f212b7afb6774d9aab2eeaabdbf
ms.sourcegitcommit: 36795a6735cd3fc678c7d5db71ddc97fac3f6f8a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2020
ms.locfileid: "48941408"
---
# <a name="fix-issues-found-by-the-readiness-assessment-tool"></a><span data-ttu-id="b3533-104">Corriger les problèmes détectés par l’outil d’évaluation de la disponibilité</span><span class="sxs-lookup"><span data-stu-id="b3533-104">Fix issues found by the readiness assessment tool</span></span>

<span data-ttu-id="b3533-105">Pour chaque vérification, l’outil signale l’un des quatre résultats possibles :</span><span class="sxs-lookup"><span data-stu-id="b3533-105">For each check, the tool will report one of four possible results:</span></span>


|<span data-ttu-id="b3533-106">Résultat</span><span class="sxs-lookup"><span data-stu-id="b3533-106">Result</span></span>  |<span data-ttu-id="b3533-107">Signification</span><span class="sxs-lookup"><span data-stu-id="b3533-107">Meaning</span></span>  |
|---------|---------|
|<span data-ttu-id="b3533-108">Prêt</span><span class="sxs-lookup"><span data-stu-id="b3533-108">Ready</span></span>     | <span data-ttu-id="b3533-109">Aucune action n’est requise avant la fin de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b3533-109">No action is required before completing enrollment.</span></span>        |
|<span data-ttu-id="b3533-110">OpenSSL</span><span class="sxs-lookup"><span data-stu-id="b3533-110">Advisory</span></span>    | <span data-ttu-id="b3533-111">Suivez les étapes décrites dans l’outil ou dans cet article pour obtenir une expérience optimale avec l’enregistrement et pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b3533-111">Follow the steps in the tool or this article for the best experience with enrollment and for users.</span></span> <span data-ttu-id="b3533-112">Vous *pouvez* effectuer l’opération d’enregistrement, mais vous devez résoudre ces problèmes avant de déployer votre premier périphérique.</span><span class="sxs-lookup"><span data-stu-id="b3533-112">You *can* complete enrollment, but you must fix these issues before you deploy your first device.</span></span>        |
|<span data-ttu-id="b3533-113">Non prêt</span><span class="sxs-lookup"><span data-stu-id="b3533-113">Not ready</span></span> | <span data-ttu-id="b3533-114">*L’enregistrement échoue si vous ne résolvez pas ces problèmes.*</span><span class="sxs-lookup"><span data-stu-id="b3533-114">*Enrollment will fail if you don't fix these issues.*</span></span> <span data-ttu-id="b3533-115">Suivez les étapes décrites dans l’outil ou dans cet article pour les résoudre.</span><span class="sxs-lookup"><span data-stu-id="b3533-115">Follow the steps in the tool or this article to resolve them.</span></span>        |
|<span data-ttu-id="b3533-116">Erreur</span><span class="sxs-lookup"><span data-stu-id="b3533-116">Error</span></span> | <span data-ttu-id="b3533-117">Le rôle Azure active Director (AD) que vous utilisez ne dispose pas des autorisations suffisantes pour effectuer cette vérification.</span><span class="sxs-lookup"><span data-stu-id="b3533-117">The Azure Active Director (AD) role you're using doesn't have sufficient permission to run this check.</span></span> |

## <a name="microsoft-intune-settings"></a><span data-ttu-id="b3533-118">Paramètres Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="b3533-118">Microsoft Intune settings</span></span>

### <a name="autopilot-deployment-profile"></a><span data-ttu-id="b3533-119">Profil de déploiement de AutoPilot</span><span class="sxs-lookup"><span data-stu-id="b3533-119">Autopilot deployment profile</span></span>

<span data-ttu-id="b3533-120">Vous ne devez pas avoir de profils AutoPilot qui ciblent les groupes affectés ou dynamiques utilisés par le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-120">You shouldn't have any existing Autopilot profiles that target assigned or dynamic groups used by Microsoft Managed Desktop.</span></span> <span data-ttu-id="b3533-121">Microsoft Managed Desktop utilise AutoPilot pour mettre en service de nouveaux appareils.</span><span class="sxs-lookup"><span data-stu-id="b3533-121">Microsoft Managed Desktop uses Autopilot to provision new devices.</span></span>

<span data-ttu-id="b3533-122">**Non prêt**</span><span class="sxs-lookup"><span data-stu-id="b3533-122">**Not ready**</span></span>

<span data-ttu-id="b3533-123">Vous disposez d’un profil AutoPilot affecté à tous les appareils.</span><span class="sxs-lookup"><span data-stu-id="b3533-123">You have an Autopilot profile that is assigned to all devices.</span></span> <span data-ttu-id="b3533-124">Pour connaître les étapes à suivre, consultez la rubrique [inscrire des appareils Windows dans Intune à l’aide de Windows AutoPilot](https://docs.microsoft.com/mem/autopilot/enrollment-autopilot).</span><span class="sxs-lookup"><span data-stu-id="b3533-124">For steps, see [Enroll Windows devices in Intune by using Windows Autopilot](https://docs.microsoft.com/mem/autopilot/enrollment-autopilot).</span></span> <span data-ttu-id="b3533-125">Après l’enregistrement de bureau géré Microsoft, définissez votre stratégie AutoPilot pour exclure les **périphériques de l’espace de travail modernes-tous les** groupes Azure ad.</span><span class="sxs-lookup"><span data-stu-id="b3533-125">After Microsoft Managed Desktop enrollment, set your Autopilot policy to exclude the **Modern Workplace Devices -All** Azure AD group.</span></span>

<span data-ttu-id="b3533-126">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-126">**Advisory**</span></span>

<span data-ttu-id="b3533-127">Assurez-vous que vos profils AutoPilot ciblent un groupe Azure AD affecté ou dynamique qui n’inclut pas les appareils de bureau géré Microsoft qui seront créés lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b3533-127">Make sure that your Autopilot profiles target an assigned or dynamic Azure AD group that doesn't include Microsoft Managed Desktop devices that will be created at enrollment.</span></span> <span data-ttu-id="b3533-128">Pour connaître les étapes à suivre, consultez la rubrique [inscrire des appareils Windows dans Intune à l’aide de Windows AutoPilot](https://docs.microsoft.com/mem/autopilot/enrollment-autopilot).</span><span class="sxs-lookup"><span data-stu-id="b3533-128">For steps, see [Enroll Windows devices in Intune by using Windows Autopilot](https://docs.microsoft.com/mem/autopilot/enrollment-autopilot).</span></span> <span data-ttu-id="b3533-129">Après l’enregistrement de bureau géré Microsoft, définissez votre stratégie AutoPilot pour exclure les **périphériques de l’espace de travail modernes-tous les** groupes Azure ad.</span><span class="sxs-lookup"><span data-stu-id="b3533-129">After Microsoft Managed Desktop enrollment, set your Autopilot policy to exclude the **Modern Workplace Devices -All** Azure AD group.</span></span>


### <a name="certificate-connectors"></a><span data-ttu-id="b3533-130">Connecteurs de certificats</span><span class="sxs-lookup"><span data-stu-id="b3533-130">Certificate connectors</span></span>

<span data-ttu-id="b3533-131">Si des connecteurs de certificat sont utilisés par les appareils que vous souhaitez inscrire dans Microsoft Managed Desktop, les connecteurs ne peuvent pas contenir d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="b3533-131">If you have any certificate connectors used by the devices you want to enroll in Microsoft Managed Desktop, the connectors cannot have any errors.</span></span> <span data-ttu-id="b3533-132">Seul l’un des avis suivants s’applique à votre situation, vérifiez-le attentivement.</span><span class="sxs-lookup"><span data-stu-id="b3533-132">Only one of the following advisories will apply to your situation, so check them carefully.</span></span>

<span data-ttu-id="b3533-133">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-133">**Advisory**</span></span>

<span data-ttu-id="b3533-134">Aucun connecteur de certificat n’est présent.</span><span class="sxs-lookup"><span data-stu-id="b3533-134">No certificate connectors are present.</span></span> <span data-ttu-id="b3533-135">Il est possible que vous n’ayez pas besoin de connecteurs, mais vous devez évaluer si vous aurez besoin d’une partie de la connectivité réseau aux appareils de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-135">It's possible you don't need any connectors, but you should evaluate whether you might need some for network connectivity to Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="b3533-136">Pour plus d’informations, consultez la rubrique [Prepare Certificates and Network profiles for Microsoft Managed Desktop](certs-wifi-lan.md).</span><span class="sxs-lookup"><span data-stu-id="b3533-136">For more information, see [Prepare certificates and network profiles for Microsoft Managed Desktop](certs-wifi-lan.md).</span></span>

<span data-ttu-id="b3533-137">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-137">**Advisory**</span></span>

<span data-ttu-id="b3533-138">Au moins un connecteur de certificat comporte une erreur.</span><span class="sxs-lookup"><span data-stu-id="b3533-138">At least one certificate connector has an error.</span></span> <span data-ttu-id="b3533-139">Si vous avez besoin de ce connecteur pour la connectivité aux appareils de bureau gérés par Microsoft, vous devez résoudre l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b3533-139">If you need this connector for connectivity to Microsoft Managed Desktop devices, you must resolve the error.</span></span> <span data-ttu-id="b3533-140">Pour plus d’informations, consultez la rubrique [Prepare Certificates and Network profiles for Microsoft Managed Desktop](certs-wifi-lan.md).</span><span class="sxs-lookup"><span data-stu-id="b3533-140">For more information, see [Prepare certificates and network profiles for Microsoft Managed Desktop](certs-wifi-lan.md).</span></span>


<span data-ttu-id="b3533-141">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-141">**Advisory**</span></span>

<span data-ttu-id="b3533-142">Vous disposez d’au moins un connecteur de certificat et aucune erreur n’est signalée.</span><span class="sxs-lookup"><span data-stu-id="b3533-142">You have at least one certificate connector and no errors are reported.</span></span> <span data-ttu-id="b3533-143">Toutefois, vous devrez peut-être créer un profil pour réutiliser le connecteur pour les appareils de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-143">However, you might need to create a profile to reuse the connector for Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="b3533-144">Pour plus d’informations, consultez la rubrique [Prepare Certificates and Network profiles for Microsoft Managed Desktop](certs-wifi-lan.md).</span><span class="sxs-lookup"><span data-stu-id="b3533-144">For more information, see [Prepare certificates and network profiles for Microsoft Managed Desktop](certs-wifi-lan.md).</span></span>


### <a name="conditional-access-policies"></a><span data-ttu-id="b3533-145">Stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="b3533-145">Conditional access policies</span></span>

<span data-ttu-id="b3533-146">Les stratégies d’accès conditionnel dans votre organisation Azure AD ne doivent pas cibler les utilisateurs de bureau Microsoft Manage.</span><span class="sxs-lookup"><span data-stu-id="b3533-146">Conditional access policies in your Azure AD organization must not target any Microsoft Manage Desktop users.</span></span>

<span data-ttu-id="b3533-147">**Non prêt**</span><span class="sxs-lookup"><span data-stu-id="b3533-147">**Not ready**</span></span>

<span data-ttu-id="b3533-148">Vous disposez d’au moins une stratégie d’accès conditionnel qui cible tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b3533-148">You have at least one conditional access policy that targets all users.</span></span> <span data-ttu-id="b3533-149">Réinitialisez la stratégie pour cibler un groupe Azure AD spécifique qui n’inclut pas le groupe Azure AD des comptes de service de bureau géré Microsoft qui seront créés lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b3533-149">Reset the policy to target a specific Azure AD group that does not include the Azure AD group of Microsoft Managed Desktop service accounts that will be created at enrollment.</span></span> <span data-ttu-id="b3533-150">Pour connaître les étapes à suivre, consultez la rubrique [accès conditionnel : utilisateurs et groupes](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-conditional-access-users-groups).</span><span class="sxs-lookup"><span data-stu-id="b3533-150">For steps, see [Conditional Access: Users and groups](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-conditional-access-users-groups).</span></span>

<span data-ttu-id="b3533-151">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-151">**Advisory**</span></span>

<span data-ttu-id="b3533-152">Assurez-vous que toutes les stratégies d’accès conditionnel vous avez exclu le groupe Azure AD comptes de service de l' **espace de travail moderne** .</span><span class="sxs-lookup"><span data-stu-id="b3533-152">Make sure that any conditional access policies you have exclude the **Modern Workplace Service Accounts** Azure AD group.</span></span> <span data-ttu-id="b3533-153">Pour connaître les étapes à suivre, consultez la rubrique [Adjust ConditionalAttribute Access](https://docs.microsoft.com/microsoft-365/managed-desktop/get-started/conditional-access).</span><span class="sxs-lookup"><span data-stu-id="b3533-153">For steps, see [Adjust conditional access](https://docs.microsoft.com/microsoft-365/managed-desktop/get-started/conditional-access).</span></span> <span data-ttu-id="b3533-154">Le groupe Azure AD de comptes de service de l' **espace de travail moderne** est un groupe dynamique que nous créons pour le service lors de l’inscription.</span><span class="sxs-lookup"><span data-stu-id="b3533-154">The **Modern Workplace Service Accounts** Azure AD group is a dynamic group that we create for the service when you enroll.</span></span> <span data-ttu-id="b3533-155">Vous devrez revenir à l’exclusion de ce groupe après l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b3533-155">You'll have to come back to exclude this group after enrollment.</span></span> <span data-ttu-id="b3533-156">Pour plus d’informations sur ces comptes de service, consultez la rubrique [Standard Operating Procedures](../service-description/operations-and-monitoring.md#standard-operating-procedures).</span><span class="sxs-lookup"><span data-stu-id="b3533-156">For more about these service accounts, see [Standard operating procedures](../service-description/operations-and-monitoring.md#standard-operating-procedures).</span></span>

<span data-ttu-id="b3533-157">**Error**</span><span class="sxs-lookup"><span data-stu-id="b3533-157">**Error**</span></span>

<span data-ttu-id="b3533-158">Le rôle d’administrateur Intune ne dispose pas des autorisations suffisantes pour cette vérification.</span><span class="sxs-lookup"><span data-stu-id="b3533-158">The Intune Administrator role doesn't have sufficient permissions for this check.</span></span> <span data-ttu-id="b3533-159">Vous aurez également besoin de ces rôles Azure AD pour exécuter cette vérification :</span><span class="sxs-lookup"><span data-stu-id="b3533-159">You'll also need any of these Azure AD roles assigned to run this check:</span></span>

- <span data-ttu-id="b3533-160">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="b3533-160">Security Reader</span></span>
- <span data-ttu-id="b3533-161">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="b3533-161">Security Administrator</span></span>
- <span data-ttu-id="b3533-162">Administrateur d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="b3533-162">Conditional Access Administrator</span></span>
- <span data-ttu-id="b3533-163">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="b3533-163">Global Reader</span></span>
- <span data-ttu-id="b3533-164">Administrateur de périphériques</span><span class="sxs-lookup"><span data-stu-id="b3533-164">Devices Administrator</span></span>


### <a name="device-compliance-policies"></a><span data-ttu-id="b3533-165">Stratégies de conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="b3533-165">Device Compliance policies</span></span>

<span data-ttu-id="b3533-166">Les stratégies de conformité d’appareil Intune dans votre organisation Azure AD ne doivent pas cibler les utilisateurs de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-166">Intune Device Compliance policies in your Azure AD organization must not target any Microsoft Managed Desktop users.</span></span>

<span data-ttu-id="b3533-167">**Non prêt**</span><span class="sxs-lookup"><span data-stu-id="b3533-167">**Not ready**</span></span>

<span data-ttu-id="b3533-168">Vous avez au moins une stratégie de conformité qui cible tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b3533-168">You have at least one compliance policy that targets all users.</span></span> <span data-ttu-id="b3533-169">Réinitialisez la stratégie pour cibler un groupe Azure AD spécifique qui n’inclut pas d’utilisateurs de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-169">Reset the policy to target a specific Azure AD group that does not include any Microsoft Managed Desktop users.</span></span> <span data-ttu-id="b3533-170">Pour connaître les étapes à suivre, voir [Create a Compliance Policy in Microsoft Intune](https://docs.microsoft.com/mem/intune/protect/create-compliance-policy).</span><span class="sxs-lookup"><span data-stu-id="b3533-170">For steps, see [Create a compliance policy in Microsoft Intune](https://docs.microsoft.com/mem/intune/protect/create-compliance-policy).</span></span>

<span data-ttu-id="b3533-171">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-171">**Advisory**</span></span>

<span data-ttu-id="b3533-172">Assurez-vous que les stratégies de conformité que vous n’avez pas n’incluent aucun utilisateur de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-172">Make sure that any compliance policies you have don't include any Microsoft Managed Desktop users.</span></span> <span data-ttu-id="b3533-173">Pour connaître les étapes à suivre, voir [Create a Compliance Policy in Microsoft Intune](https://docs.microsoft.com/mem/intune/protect/create-compliance-policy).</span><span class="sxs-lookup"><span data-stu-id="b3533-173">For steps, see [Create a compliance policy in Microsoft Intune](https://docs.microsoft.com/mem/intune/protect/create-compliance-policy).</span></span>



### <a name="device-configuration-policies"></a><span data-ttu-id="b3533-174">Stratégies de configuration des appareils</span><span class="sxs-lookup"><span data-stu-id="b3533-174">Device Configuration policies</span></span>

<span data-ttu-id="b3533-175">Les stratégies de configuration d’appareil Intune dans votre organisation Azure AD ne doivent pas cibler des utilisateurs ou des appareils de bureau Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-175">Intune Device Configuration policies in your Azure AD organization must not target any Microsoft Manage Desktop devices or users.</span></span>

<span data-ttu-id="b3533-176">**Non prêt**</span><span class="sxs-lookup"><span data-stu-id="b3533-176">**Not ready**</span></span>

<span data-ttu-id="b3533-177">Vous disposez d’au moins une stratégie de configuration qui cible tous les utilisateurs, tous les appareils ou les deux.</span><span class="sxs-lookup"><span data-stu-id="b3533-177">You have at least one configuration policy that targets all users, all devices, or both.</span></span> <span data-ttu-id="b3533-178">Réinitialisez la stratégie pour cibler un groupe Azure AD spécifique qui n’inclut pas d’appareils de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-178">Reset the policy to target a specific Azure AD group that does not include any Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="b3533-179">Pour connaître les étapes à suivre, voir [Create a Compliance Policy in Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-settings-configure).</span><span class="sxs-lookup"><span data-stu-id="b3533-179">For steps, see [Create a compliance policy in Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-settings-configure).</span></span>

<span data-ttu-id="b3533-180">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-180">**Advisory**</span></span>

<span data-ttu-id="b3533-181">Assurez-vous que les stratégies de conformité que vous n’avez pas inclues tous les appareils ou les utilisateurs de bureau gérés Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-181">Make sure that any compliance policies you have don't include any Microsoft Managed Desktop devices or users.</span></span> <span data-ttu-id="b3533-182">Pour connaître les étapes à suivre, voir [Create a Compliance Policy in Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-settings-configure).</span><span class="sxs-lookup"><span data-stu-id="b3533-182">For steps, see [Create a compliance policy in Microsoft Intune](https://docs.microsoft.com/mem/intune/configuration/custom-settings-configure).</span></span>



### <a name="device-type-restrictions"></a><span data-ttu-id="b3533-183">Restrictions de type de périphérique</span><span class="sxs-lookup"><span data-stu-id="b3533-183">Device type restrictions</span></span>

<span data-ttu-id="b3533-184">Les appareils de bureau gérés Microsoft doivent être autorisés à s’inscrire dans Intune.</span><span class="sxs-lookup"><span data-stu-id="b3533-184">Microsoft Managed Desktop devices must be allowed to enroll in Intune.</span></span>

<span data-ttu-id="b3533-185">**Non prêt**</span><span class="sxs-lookup"><span data-stu-id="b3533-185">**Not ready**</span></span>

<span data-ttu-id="b3533-186">Suivez les étapes de la procédure [définir les restrictions d’inscriptions](https://docs.microsoft.com/mem/intune/enrollment/enrollment-restrictions-set) pour modifier le paramètre sur **autoriser**.</span><span class="sxs-lookup"><span data-stu-id="b3533-186">Follow the steps in [Set enrollment restrictions](https://docs.microsoft.com/mem/intune/enrollment/enrollment-restrictions-set) to change the setting to **Allow**.</span></span>


### <a name="enrollment-status-page"></a><span data-ttu-id="b3533-187">Page d’état d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="b3533-187">Enrollment Status Page</span></span>

<span data-ttu-id="b3533-188">La page d’état d’enregistrement (ESP) est actuellement activée.</span><span class="sxs-lookup"><span data-stu-id="b3533-188">You currently have the Enrollment Status Page (ESP) enabled.</span></span> <span data-ttu-id="b3533-189">Si vous participez à la préversion publique de cette fonctionnalité, vous pouvez ignorer cet élément.</span><span class="sxs-lookup"><span data-stu-id="b3533-189">If you are participating in the public preview of this feature, you can ignore this item.</span></span> <span data-ttu-id="b3533-190">Pour plus d’informations, consultez la rubrique relative [à l’expérience de première exécution avec AutoPilot et la page État de l’enregistrement](../get-started/esp-first-run.md).</span><span class="sxs-lookup"><span data-stu-id="b3533-190">For more information, see [First-run experience with Autopilot and the Enrollment Status Page](../get-started/esp-first-run.md).</span></span>

<span data-ttu-id="b3533-191">**Non prêt**</span><span class="sxs-lookup"><span data-stu-id="b3533-191">**Not ready**</span></span>

<span data-ttu-id="b3533-192">Le profil ESP par défaut est défini pour afficher la progression de la configuration de l' **application et du profil**.</span><span class="sxs-lookup"><span data-stu-id="b3533-192">You have the ESP default profile set to **Show app and profile configuration progress**.</span></span> <span data-ttu-id="b3533-193">Désactivez ce paramètre ou assurez-vous que les affectations à n’importe quel groupe Azure AD n’incluent pas les appareils de bureau géré Microsoft en suivant les étapes décrites dans la [page Configurer l’état de l’inscription](https://docs.microsoft.com/mem/intune/enrollment/windows-enrollment-status).</span><span class="sxs-lookup"><span data-stu-id="b3533-193">Disable this setting or make sure that assignments to any Azure AD group do not include Microsoft Managed Desktop devices by following the steps in [Set up the Enrollment Status Page](https://docs.microsoft.com/mem/intune/enrollment/windows-enrollment-status).</span></span>

<span data-ttu-id="b3533-194">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-194">**Advisory**</span></span>

<span data-ttu-id="b3533-195">Assurez-vous que tous les profils dont le paramètre **afficher l’application et la configuration de profil** sont en cours de progression ne sont pas affectés à un groupe Azure ad qui inclut les appareils de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-195">Make sure that any profiles that have the **Show app and profile configuration progress** setting are not assigned to any Azure AD group that includes Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="b3533-196">Pour plus d’informations, reportez-vous à [la rubrique Configurer la page État de l’inscription](https://docs.microsoft.com/mem/intune/enrollment/windows-enrollment-status).</span><span class="sxs-lookup"><span data-stu-id="b3533-196">For more information, see [Set up the Enrollment Status Page](https://docs.microsoft.com/mem/intune/enrollment/windows-enrollment-status).</span></span>

### <a name="intune-enrollment"></a><span data-ttu-id="b3533-197">Enregistrement Intune</span><span class="sxs-lookup"><span data-stu-id="b3533-197">Intune enrollment</span></span>

<span data-ttu-id="b3533-198">Les appareils Windows 10 dans votre organisation Azure AD doivent être automatiquement apportés dans Intune.</span><span class="sxs-lookup"><span data-stu-id="b3533-198">Windows 10 devices in your Azure AD organization must be automatically enrolled in Intune.</span></span>

<span data-ttu-id="b3533-199">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-199">**Advisory**</span></span>

<span data-ttu-id="b3533-200">Assurez-vous que l’étendue utilisateur MDM est définie sur **some** ou **All** , et non sur **aucun**.</span><span class="sxs-lookup"><span data-stu-id="b3533-200">Make sure the MDM User scope is set to **Some** or **All** , not **None**.</span></span> <span data-ttu-id="b3533-201">Si vous choisissez **certaines** , revenez après l’enregistrement et sélectionnez le groupe **moderne espace de travail-tout** Azure AD pour les **groupes**.</span><span class="sxs-lookup"><span data-stu-id="b3533-201">If you choose **Some** , come back after enrollment and select the **Modern Workplace -All** Azure AD group for **Groups**.</span></span>


### <a name="microsoft-store-for-business"></a><span data-ttu-id="b3533-202">Microsoft Store pour Entreprises</span><span class="sxs-lookup"><span data-stu-id="b3533-202">Microsoft Store for Business</span></span>

<span data-ttu-id="b3533-203">Nous utilisons Microsoft Store pour les entreprises afin que vous puissiez télécharger le portail d’entreprise pour déployer certaines applications, telles que Microsoft Project et Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="b3533-203">We use Microsoft Store for Business so that you can download Company Portal to deploy some apps, such as Microsoft Project and Microsoft Visio.</span></span>

<span data-ttu-id="b3533-204">**Non prêt**</span><span class="sxs-lookup"><span data-stu-id="b3533-204">**Not ready**</span></span>

<span data-ttu-id="b3533-205">Microsoft Store pour les entreprises n’est pas activé ou n’est pas synchronisé avec Intune.</span><span class="sxs-lookup"><span data-stu-id="b3533-205">Microsoft Store for Business either isn't enabled or isn't synced with Intune.</span></span> <span data-ttu-id="b3533-206">Pour plus d’informations, consultez la rubrique [How to Manage volume purchased Apps from the Microsoft Store for Business with Microsoft Intune](https://docs.microsoft.com/mem/intune/apps/windows-store-for-business) and [install Intune Company Portal on on Devices](../get-started/company-portal.md).</span><span class="sxs-lookup"><span data-stu-id="b3533-206">For more information, see [How to manage volume purchased apps from the Microsoft Store for Business with Microsoft Intune](https://docs.microsoft.com/mem/intune/apps/windows-store-for-business) and [Install Intune Company Portal on on devices](../get-started/company-portal.md).</span></span>

### <a name="multi-factor-authentication"></a><span data-ttu-id="b3533-207">Authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="b3533-207">Multi-factor authentication</span></span>

<span data-ttu-id="b3533-208">L’authentification multifacteur ne doit pas être appliquée accidentellement aux comptes de service de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-208">Multi-factor authentication must not accidentally be applied to Microsoft Managed Desktop service accounts.</span></span>


<span data-ttu-id="b3533-209">**Non prêt**</span><span class="sxs-lookup"><span data-stu-id="b3533-209">**Not ready**</span></span>

<span data-ttu-id="b3533-210">Certaines stratégies d’authentification multifacteur (MFA) sont définies comme « obligatoires » pour les stratégies d’accès conditionnel qui sont affectées à tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b3533-210">You have some multi-factor authentication (MFA) policies set as "required" for conditional access policies that are assigned to all users.</span></span> <span data-ttu-id="b3533-211">Modifiez la stratégie de façon à utiliser une affectation ciblant un groupe Azure AD spécifique qui n’inclut aucun périphérique de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-211">Change the policy to use an Assignment that targets a specific Azure AD group that doesn't include any Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="b3533-212">Pour plus d’informations, reportez-vous à [stratégies d’accès conditionnel](#conditional-access-policies) et [accès conditionnel : exiger l’authentification multifacteur pour tous les utilisateurs](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-all-users-mfa).</span><span class="sxs-lookup"><span data-stu-id="b3533-212">For more information, see [Conditional access policies](#conditional-access-policies) and [Conditional Access: Require MFA for all users](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-all-users-mfa).</span></span>

<span data-ttu-id="b3533-213">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-213">**Advisory**</span></span>

<span data-ttu-id="b3533-214">Assurez-vous que toutes les stratégies d’accès conditionnel qui requièrent l’authentification MFA excluent le groupe **de travail moderne-tous les** groupes Azure ad.</span><span class="sxs-lookup"><span data-stu-id="b3533-214">Make sure that any conditional access policies that require MFA exclude the **Modern Workplace -All** Azure AD group.</span></span> <span data-ttu-id="b3533-215">Pour plus d’informations, reportez-vous à [stratégies d’accès conditionnel](#conditional-access-policies) et [accès conditionnel : exiger l’authentification multifacteur pour tous les utilisateurs](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-all-users-mfa).</span><span class="sxs-lookup"><span data-stu-id="b3533-215">For more information, see [Conditional access policies](#conditional-access-policies) and [Conditional Access: Require MFA for all users](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-all-users-mfa).</span></span> <span data-ttu-id="b3533-216">Le groupe de **travail moderne-tous les** groupes Azure AD est un groupe dynamique que nous créons lors de l’inscription au bureau géré Microsoft, de sorte que vous devez revenir à l’exclusion de ce groupe après l’inscription.</span><span class="sxs-lookup"><span data-stu-id="b3533-216">The **Modern Workplace -All** Azure AD group is a dynamic group that we create when you enroll in Microsoft Managed Desktop, so you'll have to come back to exclude this group after enrollment.</span></span>

<span data-ttu-id="b3533-217">**Error**</span><span class="sxs-lookup"><span data-stu-id="b3533-217">**Error**</span></span>

<span data-ttu-id="b3533-218">Le rôle d’administrateur Intune ne dispose pas des autorisations suffisantes pour cette vérification.</span><span class="sxs-lookup"><span data-stu-id="b3533-218">The Intune Administrator role doesn't have sufficient permissions for this check.</span></span> <span data-ttu-id="b3533-219">Vous aurez également besoin de ces rôles Azure AD pour exécuter cette vérification :</span><span class="sxs-lookup"><span data-stu-id="b3533-219">You'll also need any of these Azure AD roles assigned to run this check:</span></span>

- <span data-ttu-id="b3533-220">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="b3533-220">Security Reader</span></span>
- <span data-ttu-id="b3533-221">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="b3533-221">Security Administrator</span></span>
- <span data-ttu-id="b3533-222">Administrateur d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="b3533-222">Conditional Access Administrator</span></span>
- <span data-ttu-id="b3533-223">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="b3533-223">Global Reader</span></span>
- <span data-ttu-id="b3533-224">Administrateur de périphériques</span><span class="sxs-lookup"><span data-stu-id="b3533-224">Devices Administrator</span></span>


### <a name="powershell-scripts"></a><span data-ttu-id="b3533-225">Scripts PowerShell</span><span class="sxs-lookup"><span data-stu-id="b3533-225">PowerShell scripts</span></span>

<span data-ttu-id="b3533-226">Les scripts Windows PowerShell ne peuvent pas être affectés de manière à cibler les périphériques de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-226">Windows PowerShell scripts can't be assigned in a way that would target Microsoft Managed Desktop devices.</span></span>  

<span data-ttu-id="b3533-227">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-227">**Advisory**</span></span>

<span data-ttu-id="b3533-228">Assurez-vous que les scripts Windows PowerShell de votre organisation Azure AD ne ciblent pas les utilisateurs ou les appareils de bureau Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-228">Make sure that Windows PowerShell scripts in your Azure AD organization don't target any Microsoft Manage Desktop devices or users.</span></span> <span data-ttu-id="b3533-229">N’affectez pas de script PowerShell pour cibler tous les utilisateurs, tous les appareils ou les deux.</span><span class="sxs-lookup"><span data-stu-id="b3533-229">Do not assign a PowerShell script to target all users, all devices, or both.</span></span> <span data-ttu-id="b3533-230">Modifiez la stratégie de façon à utiliser une affectation ciblant un groupe Azure AD spécifique qui n’inclut aucun périphérique de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-230">Change the policy to use an Assignment that targets a specific Azure AD group that doesn't include any Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="b3533-231">Pour plus d’informations, reportez-vous à [utiliser des scripts PowerShell sur des appareils Windows 10 dans Intune](https://docs.microsoft.com/mem/intune/apps/intune-management-extension).</span><span class="sxs-lookup"><span data-stu-id="b3533-231">For more information, see [Use PowerShell scripts on Windows 10 devices in Intune](https://docs.microsoft.com/mem/intune/apps/intune-management-extension).</span></span>

### <a name="region"></a><span data-ttu-id="b3533-232">Région</span><span class="sxs-lookup"><span data-stu-id="b3533-232">Region</span></span>

<span data-ttu-id="b3533-233">Votre région doit être prise en charge par le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-233">Your region must be supported by Microsoft Managed Desktop.</span></span>

<span data-ttu-id="b3533-234">**Non prêt**</span><span class="sxs-lookup"><span data-stu-id="b3533-234">**Not ready**</span></span>

<span data-ttu-id="b3533-235">La région de votre organisation Azure AD n’est actuellement pas prise en charge par le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-235">Your Azure AD organization region isn't currently supported by Microsoft Managed Desktop.</span></span> <span data-ttu-id="b3533-236">Pour plus d’informations, voir [régions et langues prises en charge par Microsoft Managed Desktop](../service-description/regions-languages.md).</span><span class="sxs-lookup"><span data-stu-id="b3533-236">For more information, see [Microsoft Managed Desktop supported regions and languages](../service-description/regions-languages.md).</span></span>

<span data-ttu-id="b3533-237">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-237">**Advisory**</span></span>

<span data-ttu-id="b3533-238">Un ou plusieurs des pays de votre organisation Azure AD ne sont pas pris en charge par le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-238">One or more of the countries where your Azure AD organization is located isn't supported by Microsoft Managed Desktop.</span></span> <span data-ttu-id="b3533-239">Pour plus d’informations, voir [régions et langues prises en charge par Microsoft Managed Desktop](../service-description/regions-languages.md).</span><span class="sxs-lookup"><span data-stu-id="b3533-239">For more information, see [Microsoft Managed Desktop supported regions and languages](../service-description/regions-languages.md).</span></span>


### <a name="security-baselines"></a><span data-ttu-id="b3533-240">Lignes de base de sécurité</span><span class="sxs-lookup"><span data-stu-id="b3533-240">Security baselines</span></span>

<span data-ttu-id="b3533-241">Les stratégies de base de sécurité ne doivent pas viser les appareils de bureau gérés Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-241">Security baseline policies should not target any Microsoft Managed Desktop devices.</span></span>

<span data-ttu-id="b3533-242">**Non prêt**</span><span class="sxs-lookup"><span data-stu-id="b3533-242">**Not ready**</span></span>

<span data-ttu-id="b3533-243">Vous disposez d’un profil de base de sécurité ciblant tous les utilisateurs, tous les périphériques ou les deux.</span><span class="sxs-lookup"><span data-stu-id="b3533-243">You have a security baseline profile that targets all users, all devices or both.</span></span> <span data-ttu-id="b3533-244">Modifiez la stratégie de façon à utiliser une affectation ciblant un groupe Azure AD spécifique qui n’inclut aucun périphérique de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-244">Change the policy to use an Assignment that targets a specific Azure AD group that doesn't include any Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="b3533-245">Pour connaître les étapes à suivre, voir [Use Security baselines to configure Windows 10 Devices in Intune](https://docs.microsoft.com/mem/intune/protect/security-baselines).</span><span class="sxs-lookup"><span data-stu-id="b3533-245">For steps, see [Use security baselines to configure Windows 10 devices in Intune](https://docs.microsoft.com/mem/intune/protect/security-baselines).</span></span>

<span data-ttu-id="b3533-246">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-246">**Advisory**</span></span>

<span data-ttu-id="b3533-247">Assurez-vous que toutes les stratégies de base de sécurité que vous avez excluent les appareils de bureau gérés Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-247">Make sure that any security baseline policies you have exclude Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="b3533-248">Pour connaître les étapes à suivre, voir [Use Security baselines to configure Windows 10 Devices in Intune](https://docs.microsoft.com/mem/intune/protect/security-baselines).</span><span class="sxs-lookup"><span data-stu-id="b3533-248">For steps, see [Use security baselines to configure Windows 10 devices in Intune](https://docs.microsoft.com/mem/intune/protect/security-baselines).</span></span> <span data-ttu-id="b3533-249">Les **appareils de travail modernes-tous les** groupes Azure ad sont un groupe dynamique que nous créons lors de l’inscription au bureau géré Microsoft, de sorte que vous devrez revenir pour exclure ce groupe après l’inscription.</span><span class="sxs-lookup"><span data-stu-id="b3533-249">The **Modern Workplace Devices -All** Azure AD group is a dynamic group that we create when you enroll in Microsoft Managed Desktop, so you'll have to come back to exclude this group after enrollment.</span></span>


### <a name="windows-apps"></a><span data-ttu-id="b3533-250">Applications Windows</span><span class="sxs-lookup"><span data-stu-id="b3533-250">Windows apps</span></span>

<span data-ttu-id="b3533-251">Passez en revue les applications que les utilisateurs de bureau géré Microsoft doivent disposer.</span><span class="sxs-lookup"><span data-stu-id="b3533-251">Review apps you want your Microsoft Managed Desktop users to have.</span></span>

<span data-ttu-id="b3533-252">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-252">**Advisory**</span></span>

<span data-ttu-id="b3533-253">Vous devez préparer un inventaire des applications que vos utilisateurs de bureau géré Microsoft doivent disposer.</span><span class="sxs-lookup"><span data-stu-id="b3533-253">You should prepare an inventory of the apps that you want your Microsoft Managed Desktop users to have.</span></span> <span data-ttu-id="b3533-254">Assurez-vous que ces applications peuvent être déployées par Intune.</span><span class="sxs-lookup"><span data-stu-id="b3533-254">Make sure these apps can be deployed by Intune.</span></span> <span data-ttu-id="b3533-255">Pour plus d’informations, consultez la rubrique [applications in Microsoft Managed Desktop](apps.md).</span><span class="sxs-lookup"><span data-stu-id="b3533-255">For more information, see [Apps in Microsoft Managed Desktop](apps.md).</span></span>

<span data-ttu-id="b3533-256">Vous pouvez demander à votre responsable de compte Microsoft une requête dans le gestionnaire de configuration de point de terminaison Microsoft pour identifier les applications qui sont prêtes à migrer vers Intune ou qui ont besoin d’un ajustement.</span><span class="sxs-lookup"><span data-stu-id="b3533-256">You can ask your Microsoft account representative for a query in Microsoft Endpoint Configuration Manager to identify those apps that are ready to migrate to Intune or need adjustment.</span></span>


### <a name="windows-hello-for-business"></a><span data-ttu-id="b3533-257">Windows Hello Entreprise</span><span class="sxs-lookup"><span data-stu-id="b3533-257">Windows Hello for Business</span></span>

<span data-ttu-id="b3533-258">Microsoft Managed Desktop requiert l’activation de Windows Hello entreprise.</span><span class="sxs-lookup"><span data-stu-id="b3533-258">Microsoft Managed Desktop requires Windows Hello for Business to be enabled.</span></span>

<span data-ttu-id="b3533-259">**Non prêt**</span><span class="sxs-lookup"><span data-stu-id="b3533-259">**Not ready**</span></span>

<span data-ttu-id="b3533-260">Windows Hello entreprise est désactivé.</span><span class="sxs-lookup"><span data-stu-id="b3533-260">Windows Hello for Business is disabled.</span></span> <span data-ttu-id="b3533-261">Activez-le en suivant les étapes de la procédure [créer une stratégie Windows Hello entreprise](https://docs.microsoft.com/mem/intune/protect/windows-hello#create-a-windows-hello-for-business-policy)</span><span class="sxs-lookup"><span data-stu-id="b3533-261">Enable it by following the steps in [Create a Windows Hello for Business policy](https://docs.microsoft.com/mem/intune/protect/windows-hello#create-a-windows-hello-for-business-policy)</span></span>

<span data-ttu-id="b3533-262">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-262">**Advisory**</span></span>

<span data-ttu-id="b3533-263">Windows Hello entreprise n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="b3533-263">Windows Hello for Business is not set up.</span></span> <span data-ttu-id="b3533-264">Activez-le en suivant les étapes de la procédure [créer une stratégie Windows Hello entreprise](https://docs.microsoft.com/mem/intune/protect/windows-hello#create-a-windows-hello-for-business-policy).</span><span class="sxs-lookup"><span data-stu-id="b3533-264">Enable it by following the steps in [Create a Windows Hello for Business policy](https://docs.microsoft.com/mem/intune/protect/windows-hello#create-a-windows-hello-for-business-policy).</span></span>


### <a name="windows-10-update-rings"></a><span data-ttu-id="b3533-265">Sonneries de mise à jour de Windows 10</span><span class="sxs-lookup"><span data-stu-id="b3533-265">Windows 10 update rings</span></span>

<span data-ttu-id="b3533-266">Votre stratégie « Windows 10 Update Ring » dans Intune ne doit pas cibler les appareils de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-266">Your "Windows 10 update ring" policy in Intune must not target any Microsoft Managed Desktop devices.</span></span>

<span data-ttu-id="b3533-267">**Non prêt**</span><span class="sxs-lookup"><span data-stu-id="b3533-267">**Not ready**</span></span>

<span data-ttu-id="b3533-268">Vous disposez d’une stratégie de mise à jour circulaire qui cible tous les périphériques, tous les utilisateurs ou les deux.</span><span class="sxs-lookup"><span data-stu-id="b3533-268">You have an "update ring" policy that targets all devices, all users, or both.</span></span> <span data-ttu-id="b3533-269">Modifiez la stratégie de façon à utiliser une affectation ciblant un groupe Azure AD spécifique qui n’inclut aucun périphérique de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-269">Change the policy to use an Assignment that targets a specific Azure AD group that doesn't include any Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="b3533-270">Pour connaître les étapes à suivre, voir [Manage Windows 10 Software Updates in Intune](https://docs.microsoft.com/mem/intune/protect/windows-update-for-business-configure).</span><span class="sxs-lookup"><span data-stu-id="b3533-270">For steps, see [Manage Windows 10 software updates in Intune](https://docs.microsoft.com/mem/intune/protect/windows-update-for-business-configure).</span></span>

<span data-ttu-id="b3533-271">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-271">**Advisory**</span></span>

<span data-ttu-id="b3533-272">Assurez-vous que toutes les stratégies Ring de mise à jour que vous avez excluent le groupe **de travail moderne-tous les** groupes Azure ad.</span><span class="sxs-lookup"><span data-stu-id="b3533-272">Make sure that any update ring policies you have exclude the **Modern Workplace -All** Azure AD group.</span></span> <span data-ttu-id="b3533-273">Pour connaître les étapes à suivre, voir [Manage Windows 10 Software Updates in Intune](https://docs.microsoft.com/mem/intune/protect/windows-update-for-business-configure).</span><span class="sxs-lookup"><span data-stu-id="b3533-273">For steps, see [Manage Windows 10 software updates in Intune](https://docs.microsoft.com/mem/intune/protect/windows-update-for-business-configure).</span></span> <span data-ttu-id="b3533-274">Les **appareils de travail modernes-tous les** groupes Azure ad sont un groupe dynamique que nous créons lors de l’inscription au bureau géré Microsoft, de sorte que vous devrez revenir pour exclure ce groupe après l’inscription.</span><span class="sxs-lookup"><span data-stu-id="b3533-274">The **Modern Workplace Devices -All** Azure AD group is a dynamic group that we create when you enroll in Microsoft Managed Desktop, so you'll have to come back to exclude this group after enrollment.</span></span>


## <a name="azure-active-directory-settings"></a><span data-ttu-id="b3533-275">Paramètres Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b3533-275">Azure Active Directory settings</span></span>


### <a name="ad-hoc-subscriptions"></a><span data-ttu-id="b3533-276">Abonnements ad hoc</span><span class="sxs-lookup"><span data-stu-id="b3533-276">Ad hoc subscriptions</span></span>

<span data-ttu-id="b3533-277">Indique comment vérifier un paramètre qui (si sa valeur est définie sur "false") peut empêcher le fonctionnement correct de l’état d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="b3533-277">Advises how to check a setting that (if set to "false") might prevent Enterprise State Roaming from working correctly.</span></span>

<span data-ttu-id="b3533-278">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-278">**Advisory**</span></span>

<span data-ttu-id="b3533-279">Assurez-vous que **AllowAdHocSubscriptions** est défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="b3533-279">Ensure that **AllowAdHocSubscriptions** is set to **True**.</span></span> <span data-ttu-id="b3533-280">Dans le cas contraire, l’itinérance de l’état de l’entreprise peut ne pas fonctionner.</span><span class="sxs-lookup"><span data-stu-id="b3533-280">Otherwise, Enterprise State Roaming might not work.</span></span> <span data-ttu-id="b3533-281">Pour plus d’informations, consultez la rubrique [Set-MsolCompanySettings](https://docs.microsoft.com/powershell/module/msonline/set-msolcompanysettings?view=azureadps-1.0).</span><span class="sxs-lookup"><span data-stu-id="b3533-281">For more information, see [Set-MsolCompanySettings](https://docs.microsoft.com/powershell/module/msonline/set-msolcompanysettings?view=azureadps-1.0).</span></span>


### <a name="enterprise-state-roaming"></a><span data-ttu-id="b3533-282">Itinérance du statut Entreprise</span><span class="sxs-lookup"><span data-stu-id="b3533-282">Enterprise State Roaming</span></span>

<span data-ttu-id="b3533-283">L’itinérance de l’état de l’entreprise doit être activée.</span><span class="sxs-lookup"><span data-stu-id="b3533-283">Enterprise State Roaming should be enabled.</span></span>

<span data-ttu-id="b3533-284">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-284">**Advisory**</span></span>

<span data-ttu-id="b3533-285">Assurez-vous que l’itinérance de l’état de l’entreprise est activée pour **tous les** groupes ou pour ceux **sélectionnés** .</span><span class="sxs-lookup"><span data-stu-id="b3533-285">Make sure that Enterprise State Roaming is enabled for **All** or for **Selected** groups.</span></span> <span data-ttu-id="b3533-286">Pour plus d’informations, consultez la rubrique [Enable Enterprise State Roaming in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-enable).</span><span class="sxs-lookup"><span data-stu-id="b3533-286">For more information, see [Enable Enterprise State Roaming in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-enable).</span></span>

### <a name="licenses"></a><span data-ttu-id="b3533-287">Licences</span><span class="sxs-lookup"><span data-stu-id="b3533-287">Licenses</span></span>

<span data-ttu-id="b3533-288">Un certain nombre de licences sont requises pour utiliser Microsoft Managed Desktop.</span><span class="sxs-lookup"><span data-stu-id="b3533-288">A number of licenses are required to use Microsoft Managed Desktop.</span></span>

<span data-ttu-id="b3533-289">**Non prêt**</span><span class="sxs-lookup"><span data-stu-id="b3533-289">**Not Ready**</span></span>

<span data-ttu-id="b3533-290">Vous ne disposez pas de toutes les licences dont vous avez besoin pour utiliser le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-290">You don't have all the licenses you need to use Microsoft Managed Desktop.</span></span> <span data-ttu-id="b3533-291">Pour plus d’informations, consultez la rubrique [Microsoft Managed Desktop Technologies](../intro/technologies.md) et en [savoir plus sur les licences](prerequisites.md#more-about-licenses).</span><span class="sxs-lookup"><span data-stu-id="b3533-291">For more information, see [Microsoft Managed Desktop technologies](../intro/technologies.md) and [More about licenses](prerequisites.md#more-about-licenses).</span></span>


### <a name="security-account-names"></a><span data-ttu-id="b3533-292">Noms des comptes de sécurité</span><span class="sxs-lookup"><span data-stu-id="b3533-292">Security account names</span></span>

<span data-ttu-id="b3533-293">Certains noms de compte de sécurité peuvent entrer en conflit avec ceux créés par Microsoft Managed Desktop.</span><span class="sxs-lookup"><span data-stu-id="b3533-293">Certain security account names could conflict with ones created by Microsoft Managed Desktop.</span></span>

<span data-ttu-id="b3533-294">**Non prêt**</span><span class="sxs-lookup"><span data-stu-id="b3533-294">**Not ready**</span></span>

<span data-ttu-id="b3533-295">Vous avez au moins un nom de compte qui sera en conflit avec ceux créés par Microsoft Managed Desktop.</span><span class="sxs-lookup"><span data-stu-id="b3533-295">You have at least one account name that will conflict with ones created by Microsoft Managed Desktop.</span></span> <span data-ttu-id="b3533-296">Collaborez avec votre représentant Microsoft pour exclure ces noms de compte.</span><span class="sxs-lookup"><span data-stu-id="b3533-296">Work with your Microsoft account representative to exclude these account names.</span></span>


### <a name="security-administrator-roles"></a><span data-ttu-id="b3533-297">Rôles d’administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="b3533-297">Security administrator roles</span></span>

<span data-ttu-id="b3533-298">Les utilisateurs disposant de certains rôles de sécurité doivent disposer de ceux qui sont attribués à Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b3533-298">Users with certain security roles must have those assigned in Microsoft Defender for Endpoint.</span></span>

<span data-ttu-id="b3533-299">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-299">**Advisory**</span></span>

<span data-ttu-id="b3533-300">Si l’un de ces rôles est affecté dans votre organisation Azure AD, assurez-vous que ces rôles sont également attribués à Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b3533-300">If you have any of these roles assigned in your Azure AD organization, make sure they also have these roles assigned in Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="b3533-301">Dans le cas contraire, les administrateurs disposant de ces rôles ne pourront pas accéder au portail d’administration.</span><span class="sxs-lookup"><span data-stu-id="b3533-301">Otherwise, administrators with these roles won't be able to access the Admin portal.</span></span>

- <span data-ttu-id="b3533-302">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="b3533-302">Security Reader</span></span>
- <span data-ttu-id="b3533-303">Opérateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="b3533-303">Security Operator</span></span>
- <span data-ttu-id="b3533-304">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="b3533-304">Global Reader</span></span>

<span data-ttu-id="b3533-305">Pour plus d’informations, consultez la rubrique [créer et gérer des rôles pour le contrôle d’accès basé sur un rôle](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/user-roles).</span><span class="sxs-lookup"><span data-stu-id="b3533-305">For more information, see [Create and manage roles for role-based access control](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/user-roles).</span></span>


### <a name="security-default"></a><span data-ttu-id="b3533-306">Sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="b3533-306">Security default</span></span>

<span data-ttu-id="b3533-307">Les paramètres de sécurité par défaut dans Azure Active Directory empêchent Microsoft Managed Desktop de gérer vos appareils.</span><span class="sxs-lookup"><span data-stu-id="b3533-307">Security defaults in Azure Active Directory will prevent Microsoft Managed Desktop from managing your devices.</span></span>

<span data-ttu-id="b3533-308">**Non prêt**</span><span class="sxs-lookup"><span data-stu-id="b3533-308">**Not ready**</span></span>

<span data-ttu-id="b3533-309">Les paramètres de sécurité par défaut sont activés.</span><span class="sxs-lookup"><span data-stu-id="b3533-309">You have Security defaults turned on.</span></span> <span data-ttu-id="b3533-310">Désactivez les paramètres de sécurité par défaut et configurez les stratégies d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="b3533-310">Turn off Security defaults and set up conditional access policies.</span></span> <span data-ttu-id="b3533-311">Pour plus d’informations, consultez la rubrique [stratégies d’accès conditionnel courantes](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-conditional-access-policy-common).</span><span class="sxs-lookup"><span data-stu-id="b3533-311">For more information, see [Common Conditional Access policies](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-conditional-access-policy-common).</span></span>

### <a name="self-service-password-reset"></a><span data-ttu-id="b3533-312">Réinitialisation du mot de passe en libre-service</span><span class="sxs-lookup"><span data-stu-id="b3533-312">Self-service Password Reset</span></span>

<span data-ttu-id="b3533-313">La réinitialisation du mot de passe en libre-service (SSPR) doit être activée pour tous les utilisateurs, à l’exception des comptes de service de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-313">Self-service Password Reset (SSPR) should be enabled for all users excluding Microsoft Managed Desktop service accounts.</span></span> <span data-ttu-id="b3533-314">Pour plus d’informations, consultez [la rubrique Tutorial : autoriser les utilisateurs à déverrouiller leur compte ou réinitialiser les mots de passe à l’aide de la réinitialisation du mot de passe en libre-service Azure Active Directory](https://docs.microsoft.com/azure/active-directory/authentication/tutorial-enable-sspr).</span><span class="sxs-lookup"><span data-stu-id="b3533-314">For more information, see [Tutorial: Enable users to unlock their account or reset passwords using Azure Active Directory self-service password reset](https://docs.microsoft.com/azure/active-directory/authentication/tutorial-enable-sspr).</span></span>

<span data-ttu-id="b3533-315">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-315">**Advisory**</span></span>

<span data-ttu-id="b3533-316">Assurez-vous que le paramètre **sélectionné** SSPR inclut Microsoft Managed Desktop Devices, mais exclut les comptes Microsoft Managed Desktop service.</span><span class="sxs-lookup"><span data-stu-id="b3533-316">Make sure that the SSPR **Selected** setting includes Microsoft Managed Desktop devices but excludes Microsoft Managed Desktop service accounts.</span></span> <span data-ttu-id="b3533-317">Les comptes de service de bureau géré Microsoft ne peuvent pas fonctionner comme prévu lorsque SSPR est activé.</span><span class="sxs-lookup"><span data-stu-id="b3533-317">Microsoft Managed Desktop service accounts cannot work as expected when SSPR is enabled.</span></span>  


### <a name="standard-user-role"></a><span data-ttu-id="b3533-318">Rôle d’utilisateur standard</span><span class="sxs-lookup"><span data-stu-id="b3533-318">Standard user role</span></span>

<span data-ttu-id="b3533-319">À l’exception des utilisateurs auxquels sont attribués les rôles Azure AD attribués aux administrateurs généraux et aux appareils, les utilisateurs de bureau gérés Microsoft seront des utilisateurs standard sans privilèges d’administrateur local.</span><span class="sxs-lookup"><span data-stu-id="b3533-319">Other than those users who are assigned Azure AD roles of Global administrator and Device administrator, Microsoft Managed Desktop users will be standard users without local administrator privileges.</span></span> <span data-ttu-id="b3533-320">Tous les autres utilisateurs se verront attribuer un rôle d’utilisateur standard lorsqu’ils démarreront leur périphérique de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-320">All other users will be assigned a standard user role when they start their Microsoft Managed Desktop device.</span></span>

<span data-ttu-id="b3533-321">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-321">**Advisory**</span></span>

<span data-ttu-id="b3533-322">Les utilisateurs de bureau géré Microsoft ne disposeront pas des privilèges d’administrateur local sur leurs appareils de bureau gérés Microsoft après l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b3533-322">Microsoft Managed Desktop users will not have local administrator privileges on their Microsoft Managed Desktop devices after enrolling.</span></span>

## <a name="microsoft-365-apps-for-enterprise"></a><span data-ttu-id="b3533-323">Applications Microsoft 365 for entreprise</span><span class="sxs-lookup"><span data-stu-id="b3533-323">Microsoft 365 Apps for enterprise</span></span>

### <a name="onedrive-for-business"></a><span data-ttu-id="b3533-324">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="b3533-324">OneDrive for Business</span></span>

<span data-ttu-id="b3533-325">Le paramètre **autoriser la synchronisation uniquement sur des PC joints à des domaines spécifiques** entre en conflit avec le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3533-325">The **Allow syncing only on PCs joined to specific domains** setting will conflict with Microsoft Managed Desktop.</span></span>

<span data-ttu-id="b3533-326">**OpenSSL**</span><span class="sxs-lookup"><span data-stu-id="b3533-326">**Advisory**</span></span>

<span data-ttu-id="b3533-327">Vous utilisez le paramètre **autoriser la synchronisation uniquement sur des PC joints à des domaines spécifiques** .</span><span class="sxs-lookup"><span data-stu-id="b3533-327">You're using the **Allow syncing only on PCs joined to specific domains** setting.</span></span> <span data-ttu-id="b3533-328">Ce paramètre ne fonctionne pas avec Microsoft Managed Desktop.</span><span class="sxs-lookup"><span data-stu-id="b3533-328">This setting won't work with Microsoft Managed Desktop.</span></span> <span data-ttu-id="b3533-329">Désactivez ce paramètre, puis configurez OneDrive entreprise pour qu’il utilise une stratégie d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="b3533-329">Disable this setting, and instead set up OneDrive for Business to use a conditional access policy.</span></span> <span data-ttu-id="b3533-330">Voir [planifier un déploiement d’accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="b3533-330">See [Plan a Conditional Access deployment](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) for help.</span></span>


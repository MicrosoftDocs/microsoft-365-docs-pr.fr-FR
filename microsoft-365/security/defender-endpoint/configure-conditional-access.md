---
title: Configurer l'accès conditionnel dans Microsoft Defender pour le point de terminaison
description: Découvrez les étapes à suivre dans Intune, le Centre de sécurité Microsoft Defender et Azure pour implémenter l'accès conditionnel
keywords: accès conditionnel, conditionnel, accès, risque d'appareil, niveau de risque, intégration, intégration intune
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: e68a8c35fb1028fa8e60cf52a8e8bb411a534b19
ms.sourcegitcommit: 13ce4b31303a1a21ca53700a54bcf8d91ad2f8c1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51903777"
---
# <a name="configure-conditional-access-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="f9d6d-104">Configurer l'accès conditionnel dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f9d6d-104">Configure Conditional Access in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f9d6d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f9d6d-105">**Applies to:**</span></span>
- [<span data-ttu-id="f9d6d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f9d6d-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="f9d6d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f9d6d-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="f9d6d-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="f9d6d-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="f9d6d-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="f9d6d-110">Cette section vous guide à travers toutes les étapes à suivre pour implémenter correctement l'accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-110">This section guides you through all the steps you need to take to properly implement Conditional Access.</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="f9d6d-111">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="f9d6d-111">Before you begin</span></span>
>[!WARNING]
><span data-ttu-id="f9d6d-112">Il est important de noter que les appareils enregistrés dans Azure AD ne sont pas pris en charge dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-112">It's important to note that Azure AD registered devices is not supported in this scenario.</span></span></br>
><span data-ttu-id="f9d6d-113">Seuls les appareils inscrits à Intune sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-113">Only Intune enrolled devices are supported.</span></span>


<span data-ttu-id="f9d6d-114">Vous devez vous assurer que tous vos appareils sont inscrits dans Intune.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-114">You need to make sure that all your devices are enrolled in Intune.</span></span> <span data-ttu-id="f9d6d-115">Vous pouvez utiliser l'une des options suivantes pour inscrire des appareils dans Intune :</span><span class="sxs-lookup"><span data-stu-id="f9d6d-115">You can use any of the following options to enroll devices in Intune:</span></span>


- <span data-ttu-id="f9d6d-116">Administrateur informatique : pour plus d'informations sur l'activation de l'inscription automatique, voir [Inscription Windows](https://docs.microsoft.com/intune/windows-enroll#enable-windows-10-automatic-enrollment)</span><span class="sxs-lookup"><span data-stu-id="f9d6d-116">IT Admin: For more information on how to enabling auto-enrollment, see [Windows Enrollment](https://docs.microsoft.com/intune/windows-enroll#enable-windows-10-automatic-enrollment)</span></span>
- <span data-ttu-id="f9d6d-117">Utilisateur final : pour plus d'informations sur l'inscription de votre appareil Windows 10 dans Intune, voir Inscrire votre appareil [Windows 10 dans Intune](https://docs.microsoft.com/intune/quickstart-enroll-windows-device)</span><span class="sxs-lookup"><span data-stu-id="f9d6d-117">End-user: For more information on how to enroll your Windows 10 device in Intune, see [Enroll your Windows 10 device in Intune](https://docs.microsoft.com/intune/quickstart-enroll-windows-device)</span></span>
- <span data-ttu-id="f9d6d-118">Alternative pour l'utilisateur final : pour plus d'informations sur la jointation d'un domaine Azure AD, voir Comment : planifier votre implémentation de jointage [Azure AD.](https://docs.microsoft.com/azure/active-directory/devices/azureadjoin-plan)</span><span class="sxs-lookup"><span data-stu-id="f9d6d-118">End-user alternative: For more information on joining an Azure AD domain, see [How to: Plan your Azure AD join implementation](https://docs.microsoft.com/azure/active-directory/devices/azureadjoin-plan).</span></span>



<span data-ttu-id="f9d6d-119">Vous devez suivre les étapes à suivre dans le Centre de sécurité Microsoft Defender, le portail Intune et le portail Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-119">There are steps you'll need to take in Microsoft Defender Security Center, the Intune portal, and Azure AD portal.</span></span>

<span data-ttu-id="f9d6d-120">Il est important de noter les rôles requis pour accéder à ces portails et implémenter l'accès conditionnel :</span><span class="sxs-lookup"><span data-stu-id="f9d6d-120">It's important to note the required roles to access these portals and implement Conditional access:</span></span>
- <span data-ttu-id="f9d6d-121">**Centre de sécurité Microsoft Defender** : vous devez vous inscrire au portail avec un rôle d'administrateur général pour activer l'intégration.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-121">**Microsoft Defender Security Center** - You'll need to sign into the portal with a global administrator role to turn on the integration.</span></span>
- <span data-ttu-id="f9d6d-122">**Intune** : vous devez vous connectez au portail avec des droits d'administrateur de sécurité avec des autorisations de gestion.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-122">**Intune** - You'll need to sign in to the portal with security administrator rights with management permissions.</span></span> 
- <span data-ttu-id="f9d6d-123">**Portail Azure AD** : vous devez vous inscrire en tant qu'administrateur général, administrateur de sécurité ou administrateur d'accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-123">**Azure AD portal** - You'll need to sign in as a global administrator, security administrator, or Conditional Access administrator.</span></span>


> [!NOTE]
> <span data-ttu-id="f9d6d-124">Vous aurez besoin d'un environnement Microsoft Intune, avec des appareils Windows 10 gérés par Intune et joints à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-124">You'll need a Microsoft Intune environment, with Intune managed and Azure AD joined Windows 10 devices.</span></span>

<span data-ttu-id="f9d6d-125">Pour activer l'accès conditionnel, prenez les mesures suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9d6d-125">Take the following steps to enable Conditional Access:</span></span>
- <span data-ttu-id="f9d6d-126">Étape 1 : Activer la connexion Microsoft Intune à partir du Centre de sécurité Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="f9d6d-126">Step 1: Turn on the Microsoft Intune connection from Microsoft Defender Security Center</span></span>
- <span data-ttu-id="f9d6d-127">Étape 2 : Activer l'intégration de Defender for Endpoint dans Intune</span><span class="sxs-lookup"><span data-stu-id="f9d6d-127">Step 2: Turn on the Defender for Endpoint integration in Intune</span></span>
- <span data-ttu-id="f9d6d-128">Étape 3 : Créer la stratégie de conformité dans Intune</span><span class="sxs-lookup"><span data-stu-id="f9d6d-128">Step 3: Create the compliance policy in Intune</span></span>
- <span data-ttu-id="f9d6d-129">Étape 4 : Attribuer la stratégie</span><span class="sxs-lookup"><span data-stu-id="f9d6d-129">Step 4: Assign the policy</span></span> 
- <span data-ttu-id="f9d6d-130">Étape 5 : Créer une stratégie d'accès conditionnel Azure AD</span><span class="sxs-lookup"><span data-stu-id="f9d6d-130">Step 5: Create an Azure AD Conditional Access policy</span></span>


### <a name="step-1-turn-on-the-microsoft-intune-connection"></a><span data-ttu-id="f9d6d-131">Étape 1 : Activer la connexion Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="f9d6d-131">Step 1: Turn on the Microsoft Intune connection</span></span>
1. <span data-ttu-id="f9d6d-132">Dans le volet de navigation, sélectionnez **Paramètres**  >  **avancés fonctionnalités**  >  **Microsoft Intune connexion**.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-132">In the navigation pane, select **Settings** > **Advanced features** > **Microsoft Intune connection**.</span></span>
2. <span data-ttu-id="f9d6d-133">Basculez le paramètre Microsoft Intune sur **Sur**.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-133">Toggle the Microsoft Intune setting to **On**.</span></span>
3. <span data-ttu-id="f9d6d-134">Cliquez **sur Enregistrer les préférences.**</span><span class="sxs-lookup"><span data-stu-id="f9d6d-134">Click **Save preferences**.</span></span>


### <a name="step-2-turn-on-the-defender-for-endpoint-integration-in-intune"></a><span data-ttu-id="f9d6d-135">Étape 2 : Activer l'intégration de Defender for Endpoint dans Intune</span><span class="sxs-lookup"><span data-stu-id="f9d6d-135">Step 2: Turn on the Defender for Endpoint integration in Intune</span></span>
1. <span data-ttu-id="f9d6d-136">Connectez-vous au [portail Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f9d6d-136">Sign in to the [Azure portal](https://portal.azure.com).</span></span>
2. <span data-ttu-id="f9d6d-137">Sélectionnez **La conformité de**  >  **l'appareil Microsoft Defender ATP**.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-137">Select **Device compliance** > **Microsoft Defender ATP**.</span></span>
3. <span data-ttu-id="f9d6d-138">Définissez **Connecter des appareils Windows 10.0.15063+** à Microsoft Defender - Protection avancée contre les **menaces** sur On .</span><span class="sxs-lookup"><span data-stu-id="f9d6d-138">Set **Connect Windows 10.0.15063+ devices to Microsoft Defender Advanced Threat Protection** to **On**.</span></span>
4. <span data-ttu-id="f9d6d-139">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-139">Click **Save**.</span></span>


### <a name="step-3-create-the-compliance-policy-in-intune"></a><span data-ttu-id="f9d6d-140">Étape 3 : Créer la stratégie de conformité dans Intune</span><span class="sxs-lookup"><span data-stu-id="f9d6d-140">Step 3: Create the compliance policy in Intune</span></span>
1. <span data-ttu-id="f9d6d-141">Dans le [portail Azure,](https://portal.azure.com) **sélectionnez Tous les services,** filtrez **sur Intune** et **sélectionnez Microsoft Intune.**</span><span class="sxs-lookup"><span data-stu-id="f9d6d-141">In the [Azure portal](https://portal.azure.com), select **All services**, filter on **Intune**, and select **Microsoft Intune**.</span></span>
2. <span data-ttu-id="f9d6d-142">Sélectionnez **Stratégies de conformité**  >  **des appareils** Créer une  >  **stratégie.**</span><span class="sxs-lookup"><span data-stu-id="f9d6d-142">Select **Device compliance** > **Policies** > **Create policy**.</span></span>
3. <span data-ttu-id="f9d6d-143">Entrez un **nom et** une **description.**</span><span class="sxs-lookup"><span data-stu-id="f9d6d-143">Enter a **Name** and **Description**.</span></span>
4. <span data-ttu-id="f9d6d-144">Dans **Plateforme,** **sélectionnez Windows 10 et les ultérieures.**</span><span class="sxs-lookup"><span data-stu-id="f9d6d-144">In **Platform**, select **Windows 10 and later**.</span></span>
5. <span data-ttu-id="f9d6d-145">Dans les paramètres **d'état** de l'appareil, définissez Exiger que l'appareil soit à ou sous le niveau de menace de l'appareil **à** votre niveau préféré :</span><span class="sxs-lookup"><span data-stu-id="f9d6d-145">In the **Device Health** settings, set **Require the device to be at or under the Device Threat Level** to your preferred level:</span></span>

   - <span data-ttu-id="f9d6d-146">**Sécurisé :** ce niveau est le plus sécurisé.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-146">**Secured**: This level is the most secure.</span></span> <span data-ttu-id="f9d6d-147">L'appareil ne peut pas avoir de menaces existantes et accéder aux ressources de l'entreprise.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-147">The device cannot have any existing threats and still access company resources.</span></span> <span data-ttu-id="f9d6d-148">Si des menaces sont trouvées, l'appareil est évalué comme non conforme.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-148">If any threats are found, the device is evaluated as noncompliant.</span></span>
   - <span data-ttu-id="f9d6d-149">**Faible**: l'appareil est conforme si seules les menaces de bas niveau existent.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-149">**Low**: The device is compliant if only low-level threats exist.</span></span> <span data-ttu-id="f9d6d-150">Les appareils avec des niveaux de menace moyen ou élevé ne sont pas conformes.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-150">Devices with medium or high threat levels are not compliant.</span></span>
   - <span data-ttu-id="f9d6d-151">**Moyen**: l'appareil est conforme si les menaces trouvées sur l'appareil sont faibles ou moyennes.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-151">**Medium**: The device is compliant if the threats found on the device are low or medium.</span></span> <span data-ttu-id="f9d6d-152">Si des menaces de haut niveau sont détectées, l'appareil est déterminé comme non conforme.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-152">If high-level threats are detected, the device is determined as noncompliant.</span></span>
   - <span data-ttu-id="f9d6d-153">**Élevé**: ce niveau est le moins sécurisé et autorise tous les niveaux de menace.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-153">**High**: This level is the least secure, and allows all threat levels.</span></span> <span data-ttu-id="f9d6d-154">Ainsi, les appareils dont les niveaux de menace sont élevés, moyens ou faibles sont considérés comme conformes.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-154">So devices that with high, medium or low threat levels are considered compliant.</span></span>

6. <span data-ttu-id="f9d6d-155">Sélectionnez **OK,** **puis créez pour** enregistrer vos modifications (et créez la stratégie).</span><span class="sxs-lookup"><span data-stu-id="f9d6d-155">Select **OK**, and **Create** to save your changes (and create the policy).</span></span>

### <a name="step-4-assign-the-policy"></a><span data-ttu-id="f9d6d-156">Étape 4 : Attribuer la stratégie</span><span class="sxs-lookup"><span data-stu-id="f9d6d-156">Step 4: Assign the policy</span></span>
1. <span data-ttu-id="f9d6d-157">Dans le [portail Azure,](https://portal.azure.com) **sélectionnez Tous les services,** filtrez **sur Intune,** puis **sélectionnez Microsoft Intune.**</span><span class="sxs-lookup"><span data-stu-id="f9d6d-157">In the [Azure portal](https://portal.azure.com), select **All services**, filter on **Intune**, and select **Microsoft Intune**.</span></span>
2. <span data-ttu-id="f9d6d-158">Sélectionnez   >  **stratégies de** conformité des> sélectionnez votre stratégie de conformité Microsoft Defender pour les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-158">Select **Device compliance** > **Policies**> select your Microsoft Defender for Endpoint compliance policy.</span></span>
3. <span data-ttu-id="f9d6d-159">Sélectionnez **Devoirs**.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-159">Select **Assignments**.</span></span>
4. <span data-ttu-id="f9d6d-160">Incluez ou excluez vos groupes Azure AD pour leur attribuer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-160">Include or exclude your Azure AD groups to assign them the policy.</span></span>
5. <span data-ttu-id="f9d6d-161">Pour déployer la stratégie sur les groupes, sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="f9d6d-161">To deploy the policy to the groups, select **Save**.</span></span> <span data-ttu-id="f9d6d-162">Les appareils utilisateur ciblés par la stratégie sont évalués pour la conformité.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-162">The user devices targeted by the policy are evaluated for compliance.</span></span>

### <a name="step-5-create-an-azure-ad-conditional-access-policy"></a><span data-ttu-id="f9d6d-163">Étape 5 : Créer une stratégie d'accès conditionnel Azure AD</span><span class="sxs-lookup"><span data-stu-id="f9d6d-163">Step 5: Create an Azure AD Conditional Access policy</span></span>
1. <span data-ttu-id="f9d6d-164">Dans le [portail Azure,](https://portal.azure.com)ouvrez la nouvelle stratégie d'accès conditionnel **Azure Active**  >    >  **Directory.**</span><span class="sxs-lookup"><span data-stu-id="f9d6d-164">In the [Azure portal](https://portal.azure.com), open **Azure Active Directory** > **Conditional Access** > **New policy**.</span></span>
2. <span data-ttu-id="f9d6d-165">Entrez un nom **de stratégie,** puis sélectionnez **Utilisateurs et groupes.**</span><span class="sxs-lookup"><span data-stu-id="f9d6d-165">Enter a policy **Name**, and select **Users and groups**.</span></span> <span data-ttu-id="f9d6d-166">Utilisez les options Inclure ou Exclure pour ajouter vos groupes pour la stratégie, puis sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-166">Use the Include or Exclude options to add your groups for the policy, and select **Done**.</span></span>
3. <span data-ttu-id="f9d6d-167">Sélectionnez **les applications cloud** et choisissez les applications à protéger.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-167">Select **Cloud apps**, and choose which apps to protect.</span></span> <span data-ttu-id="f9d6d-168">Par exemple, **sélectionnez Sélectionner des applications,** puis **Sélectionnez Office 365 SharePoint Online** et **Office 365 Exchange Online.**</span><span class="sxs-lookup"><span data-stu-id="f9d6d-168">For example, choose **Select apps**, and select **Office 365 SharePoint Online** and **Office 365 Exchange Online**.</span></span> <span data-ttu-id="f9d6d-169">Sélectionnez **OK** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-169">Select **Done** to save your changes.</span></span>

4. <span data-ttu-id="f9d6d-170">Sélectionnez **Conditions**  >  **Applications clientes** pour appliquer la stratégie aux applications et aux navigateurs.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-170">Select **Conditions** > **Client apps** to apply the policy to apps and browsers.</span></span> <span data-ttu-id="f9d6d-171">Par exemple, sélectionnez **Oui,** puis **activez** les applications mobiles **et de navigateur, ainsi que les clients de bureau.**</span><span class="sxs-lookup"><span data-stu-id="f9d6d-171">For example, select **Yes**, and then enable **Browser** and **Mobile apps and desktop clients**.</span></span> <span data-ttu-id="f9d6d-172">Sélectionnez **OK** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-172">Select **Done** to save your changes.</span></span>

5. <span data-ttu-id="f9d6d-173">Sélectionnez **Accorder pour** appliquer l'accès conditionnel en fonction de la conformité des appareils.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-173">Select **Grant** to apply Conditional Access based on device compliance.</span></span> <span data-ttu-id="f9d6d-174">Par exemple, **sélectionnez Accorder l'accès**  >  **Exiger que l'appareil soit marqué comme conforme.**</span><span class="sxs-lookup"><span data-stu-id="f9d6d-174">For example, select **Grant access** > **Require device to be marked as compliant**.</span></span> <span data-ttu-id="f9d6d-175">Sélectionnez **Sélectionner** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-175">Choose **Select** to save your changes.</span></span>

6. <span data-ttu-id="f9d6d-176">Sélectionnez **Activer la** stratégie, puis **Créez pour** enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-176">Select **Enable policy**, and then **Create** to save your changes.</span></span>

<span data-ttu-id="f9d6d-177">Pour plus d'informations, voir [Enforce compliance for Microsoft Defender for Endpoint with Conditional Access in Intune](https://docs.microsoft.com/intune/advanced-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="f9d6d-177">For more information, see [Enforce compliance for Microsoft Defender for Endpoint with Conditional Access in Intune](https://docs.microsoft.com/intune/advanced-threat-protection).</span></span>

><span data-ttu-id="f9d6d-178">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="f9d6d-178">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="f9d6d-179">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f9d6d-179">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-conditionalaccess-belowfoldlink)

---
title: Chiffrement à double clé (DKE)
description: DKE vous permet de protéger les données hautement sensibles tout en conservant le contrôle total de votre clé.
author: kccross
ms.author: krowley
manager: laurawi
ms.date: 09/22/2020
ms.topic: conceptual
ms.service: information-protection
audience: Admin
ms.reviewer: esaggese
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.openlocfilehash: 39d7933014f1dc71f8c94e467954d36ede4fb451
ms.sourcegitcommit: 1423e08a02d30f0a2b993fb99325c3f499c31787
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2020
ms.locfileid: "48277538"
---
# <a name="double-key-encryption-for-microsoft-365"></a><span data-ttu-id="4e0f0-103">Chiffrement à double clé pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4e0f0-103">Double Key Encryption for Microsoft 365</span></span>

> <span data-ttu-id="4e0f0-104">*S’applique à : chiffrement à double clé pour Microsoft 365, [conformité microsoft 365](https://www.microsoft.com/microsoft-365/business/compliance-management), [Azure information protection](https://azure.microsoft.com/pricing/details/information-protection)*</span><span class="sxs-lookup"><span data-stu-id="4e0f0-104">*Applies to: Double Key Encryption for Microsoft 365, [Microsoft 365 Compliance](https://www.microsoft.com/microsoft-365/business/compliance-management), [Azure Information Protection](https://azure.microsoft.com/pricing/details/information-protection)*</span></span>
>
> <span data-ttu-id="4e0f0-105">*Instructions pour : [client d’étiquetage unifié Azure information protection pour Windows](https://docs.microsoft.com/azure/information-protection/faqs#whats-the-difference-between-the-azure-information-protection-classic-and-unified-labeling-clients)*</span><span class="sxs-lookup"><span data-stu-id="4e0f0-105">*Instructions for: [Azure Information Protection unified labeling client for Windows](https://docs.microsoft.com/azure/information-protection/faqs#whats-the-difference-between-the-azure-information-protection-classic-and-unified-labeling-clients)*</span></span>
>
> <span data-ttu-id="4e0f0-106">*Description du service : [conformité Microsoft 365](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance)*</span><span class="sxs-lookup"><span data-stu-id="4e0f0-106">*Service description for: [Microsoft 365 Compliance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance)*</span></span>

<span data-ttu-id="4e0f0-107">Le chiffrement à clé double (DKE) utilise deux clés ensemble pour accéder au contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-107">Double Key Encryption (DKE) uses two keys together to access protected content.</span></span> <span data-ttu-id="4e0f0-108">Microsoft stocke une clé dans Microsoft Azure et vous conservez l’autre clé.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-108">Microsoft stores one key in Microsoft Azure, and you hold the other key.</span></span> <span data-ttu-id="4e0f0-109">Vous conservez le contrôle total de l’une de vos clés à l’aide du service de chiffrement à clé double.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-109">You maintain full control of one of your keys using the Double Key Encryption service.</span></span> <span data-ttu-id="4e0f0-110">Vous appliquez la protection à l’aide du client d’étiquetage unifié Azure information protection à votre contenu hautement sensible.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-110">You apply protection using The Azure Information Protection unified labeling client to your highly sensitive content.</span></span>

<span data-ttu-id="4e0f0-111">Le chiffrement à double clé prend en charge les déploiements sur le Cloud et sur site.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-111">Double Key Encryption supports both cloud and on-premises deployments.</span></span> <span data-ttu-id="4e0f0-112">Ces déploiements permettent de s’assurer que les données chiffrées restent opaques, où que vous stockez les données protégées.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-112">These deployments help to ensure that encrypted data remains opaque wherever you store the protected data.</span></span>

<span data-ttu-id="4e0f0-113">Pour plus d’informations sur les clés de racine de client par défaut, consultez la rubrique [planification et implémentation de votre clé de client Azure information protection](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key).</span><span class="sxs-lookup"><span data-stu-id="4e0f0-113">For more information about the default, cloud-based tenant root keys, see [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key).</span></span>

## <a name="when-your-organization-should-adopt-dke"></a><span data-ttu-id="4e0f0-114">Quand votre organisation doit adopter DKE</span><span class="sxs-lookup"><span data-stu-id="4e0f0-114">When your organization should adopt DKE</span></span>

<span data-ttu-id="4e0f0-115">Le chiffrement à double clé est destiné à vos données les plus sensibles, sujettes aux exigences de protection les plus strictes.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-115">Double Key Encryption is intended for your most sensitive data that is subject to the strictest protection requirements.</span></span> <span data-ttu-id="4e0f0-116">DKE n’est pas destiné à toutes les données.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-116">DKE is not intended for all data.</span></span> <span data-ttu-id="4e0f0-117">En règle générale, vous utiliserez le chiffrement à double clé pour ne protéger qu’une très petite partie de vos données globales.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-117">In general, you'll be using Double Key Encryption to protect only a very small part of your overall data.</span></span> <span data-ttu-id="4e0f0-118">Vous devez faire diligence pour identifier les bonnes données à traiter avec cette solution avant de procéder au déploiement.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-118">You should do due diligence in identifying the right data to cover with this solution before you deploy.</span></span> <span data-ttu-id="4e0f0-119">Dans certains cas, vous devrez peut-être affiner votre portée et utiliser d’autres solutions pour la majorité de vos données, telles que la protection des informations Microsoft avec des clés gérées par Microsoft ou BYOK.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-119">In some cases, you might need to narrow your scope and make use of other solutions for the majority of your data such as Microsoft Information Protection with Microsoft-managed keys or BYOK.</span></span> <span data-ttu-id="4e0f0-120">Ces solutions sont suffisantes pour les documents qui ne sont pas soumis à des protections améliorées et aux exigences réglementaires.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-120">These solutions are sufficient for documents that aren't subject to enhanced protections and regulatory requirements.</span></span> <span data-ttu-id="4e0f0-121">De plus, ces solutions vous permettent d’utiliser les services Office 365 les plus puissants ; services que vous ne pouvez pas utiliser avec du contenu chiffré DKE.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-121">Also, these solutions enable you to use the most powerful Office 365 services; services that you can't use with DKE encrypted content.</span></span> <span data-ttu-id="4e0f0-122">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-122">For example:</span></span>

- <span data-ttu-id="4e0f0-123">Règles de transport incluant le blocage des programmes malveillants et le courrier indésirable qui nécessitent une visibilité dans la pièce jointe</span><span class="sxs-lookup"><span data-stu-id="4e0f0-123">Transport rules including anti-malware and spam that require visibility into the attachment</span></span>
- <span data-ttu-id="4e0f0-124">Microsoft Delve</span><span class="sxs-lookup"><span data-stu-id="4e0f0-124">Microsoft Delve</span></span>
- <span data-ttu-id="4e0f0-125">eDiscovery</span><span class="sxs-lookup"><span data-stu-id="4e0f0-125">eDiscovery</span></span>
- <span data-ttu-id="4e0f0-126">Recherche et indexation de contenu</span><span class="sxs-lookup"><span data-stu-id="4e0f0-126">Content search and indexing</span></span>
- <span data-ttu-id="4e0f0-127">Office Web Apps, y compris la fonctionnalité de co-création</span><span class="sxs-lookup"><span data-stu-id="4e0f0-127">Office Web Apps including co-authoring functionality</span></span>

<span data-ttu-id="4e0f0-128">Les applications ou services externes qui ne sont pas intégrés à DKE via le kit de développement logiciel MIP ne seront pas en mesure d’effectuer des actions sur les données chiffrées.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-128">Any external applications or services that are not integrated with DKE through the MIP SDK will be unable to perform actions on the encrypted data.</span></span>

<span data-ttu-id="4e0f0-129">Le kit de développement logiciel (SDK) Microsoft information protection 1.7 + prend en charge le chiffrement à double clé ; les applications qui s’intègrent à notre kit de développement logiciel (SDK) seront en mesure de le faire sur ces données avec des autorisations et des intégrations suffisantes.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-129">The Microsoft Information Protection SDK 1.7+ supports Double Key Encryption; applications that integrate with our SDK will be able to reason over this data with sufficient permissions and integrations in place.</span></span>

<span data-ttu-id="4e0f0-130">Nous recommandons aux organisations d’utiliser les fonctionnalités de protection des informations Microsoft (classification et étiquetage) pour protéger la plupart de leurs données sensibles et utiliser DKE pour leurs données critiques.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-130">We recommend organizations use Microsoft Information protection capabilities (classification and labeling) to protect most of their sensitive data and only use DKE for their mission-critical data.</span></span> <span data-ttu-id="4e0f0-131">Le chiffrement à double clé est particulièrement pertinent pour les données extrêmement sensibles dans les secteurs hautement réglementés, tels que les services financiers et le secteur de la santé.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-131">Double Key Encryption is particularly relevant for extremely sensitive data in highly regulated industries such as Financial services and Healthcare.</span></span>

<span data-ttu-id="4e0f0-132">Si votre organisation dispose de l’une des conditions suivantes, vous pouvez utiliser DKE pour sécuriser votre contenu :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-132">If your organizations have any of the following requirements, you can use DKE to help secure your content:</span></span>

- <span data-ttu-id="4e0f0-133">Vous souhaitez vous assurer que *vous* êtes le seul à pouvoir déchiffrer le contenu protégé, dans toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-133">You want to ensure that *only you* can ever decrypt protected content, under all circumstances.</span></span>
- <span data-ttu-id="4e0f0-134">Vous ne souhaitez pas que Microsoft ait accès aux données protégées de façon autonome.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-134">You don't want Microsoft to have access to protected data on its own.</span></span>
- <span data-ttu-id="4e0f0-135">Vous avez des exigences réglementaires à maintenir des clés dans une limite géographique.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-135">You have regulatory requirements to hold keys within a geographical boundary.</span></span> <span data-ttu-id="4e0f0-136">Toutes les clés que vous mettez en attente pour le chiffrement et le déchiffrement des données sont conservées dans votre centre de données.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-136">All of the keys that you hold for data encryption and decryption are maintained in your data center.</span></span>

## <a name="system-and-licensing-requirements-for-dke"></a><span data-ttu-id="4e0f0-137">Exigences en matière de système et de licence pour DKE</span><span class="sxs-lookup"><span data-stu-id="4e0f0-137">System and licensing requirements for DKE</span></span>

<span data-ttu-id="4e0f0-138">Le **chiffrement à double clé pour microsoft 365** est fourni avec Microsoft 365 E5 et Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-138">**Double Key Encryption for Microsoft 365** comes with Microsoft 365 E5 and Office 365 E5.</span></span> <span data-ttu-id="4e0f0-139">Si vous n’avez pas de licence Microsoft 365 E5, vous pouvez vous inscrire pour obtenir une [version d’évaluation](https://aka.ms/M365E5ComplianceTrial).</span><span class="sxs-lookup"><span data-stu-id="4e0f0-139">If you don’t have a Microsoft 365 E5 license, you can sign up for a [trial](https://aka.ms/M365E5ComplianceTrial).</span></span> <span data-ttu-id="4e0f0-140">Pour plus d’informations sur ces licences, consultez [la rubrique Microsoft 365 Licensing Guidance for security & Compliance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).</span><span class="sxs-lookup"><span data-stu-id="4e0f0-140">For more information about these licenses, see [Microsoft 365 licensing guidance for security & compliance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).</span></span>

<span data-ttu-id="4e0f0-141">**Azure information protection**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-141">**Azure Information Protection**.</span></span> <span data-ttu-id="4e0f0-142">DKE fonctionne avec les étiquettes de confidentialité et nécessite Azure information protection.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-142">DKE works with sensitivity labels and requires Azure Information Protection.</span></span>

<span data-ttu-id="4e0f0-143">Les étiquettes de sensibilité DKE sont mises à la disposition des utilisateurs finaux via le ruban de confidentialité dans les applications de bureau Office.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-143">DKE sensitivity labels are made available to end-users through the sensitivity ribbon in Office Desktop Apps.</span></span> <span data-ttu-id="4e0f0-144">Installez ces éléments prérequis sur chaque ordinateur client sur lequel vous souhaitez protéger et consommer des documents protégés.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-144">Install these prerequisites on each client computer where you want to protect and consume protected documents.</span></span>

<span data-ttu-id="4e0f0-145">**Microsoft Office apps pour Enterprise** version \*. 12711 ou version ultérieure (versions de bureau de Word, PowerPoint et Excel) sur Windows.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-145">**Microsoft Office Apps for enterprise** version \*.12711 or later (Desktop versions of Word, PowerPoint, and Excel) on Windows.</span></span>

<span data-ttu-id="4e0f0-146">Versions du **client d’étiquetage unifié Azure information protection** 2.7.93.0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-146">**Azure Information Protection Unified Labeling Client** versions 2.7.93.0 or later.</span></span> <span data-ttu-id="4e0f0-147">Téléchargez et installez le client d’étiquetage unifié à partir du [Centre de téléchargement Microsoft](https://www.microsoft.com/download/details.aspx?id=53018).</span><span class="sxs-lookup"><span data-stu-id="4e0f0-147">Download and install the Unified Labeling client from the [Microsoft download center](https://www.microsoft.com/download/details.aspx?id=53018).</span></span>

## <a name="supported-environments-for-storing-and-viewing-dke-protected-content"></a><span data-ttu-id="4e0f0-148">Environnements pris en charge pour le stockage et l’affichage du contenu protégé par DKE</span><span class="sxs-lookup"><span data-stu-id="4e0f0-148">Supported environments for storing and viewing DKE-protected content</span></span>

<span data-ttu-id="4e0f0-149">**Applications prises en charge**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-149">**Supported applications**.</span></span> <span data-ttu-id="4e0f0-150">[Applications Microsoft 365 pour](https://www.microsoft.com/microsoft-365/business/microsoft-365-apps-for-enterprise-product) les clients d’entreprise sur Windows, y compris Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-150">[Microsoft 365 Apps for enterprise](https://www.microsoft.com/microsoft-365/business/microsoft-365-apps-for-enterprise-product) clients on Windows, including Word, Excel, and PowerPoint.</span></span>

<span data-ttu-id="4e0f0-151">**Prise en charge du contenu en ligne**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-151">**Online content support**.</span></span> <span data-ttu-id="4e0f0-152">Les documents et les fichiers stockés en ligne dans Microsoft SharePoint et OneDrive entreprise sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-152">Documents and files stored online in both Microsoft SharePoint and OneDrive for Business are supported.</span></span> <span data-ttu-id="4e0f0-153">Vous pouvez partager le contenu chiffré par courrier électronique, mais vous ne pouvez pas afficher les documents et fichiers chiffrés en ligne.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-153">You can share encrypted content by email, but you can't view encrypted documents and files online.</span></span> <span data-ttu-id="4e0f0-154">Au lieu de cela, vous devez afficher le contenu protégé à l’aide des applications de bureau sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-154">Instead, you must view protected content using the desktop apps on your local computer.</span></span>

## <a name="overview-of-deploying-dke"></a><span data-ttu-id="4e0f0-155">Vue d’ensemble du déploiement de DKE</span><span class="sxs-lookup"><span data-stu-id="4e0f0-155">Overview of deploying DKE</span></span>

<span data-ttu-id="4e0f0-156">Suivez les étapes générales suivantes pour configurer DKE.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-156">You'll follow these general steps to set up DKE.</span></span> <span data-ttu-id="4e0f0-157">Une fois que vous aurez effectué ces étapes, vos utilisateurs finaux seront en mesure de protéger vos données hautement sensibles à l’aide du chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-157">Once you've completed these steps, your end users will be able to protect your highly sensitive data with Double Key Encryption.</span></span>

1. <span data-ttu-id="4e0f0-158">Déployez le service DKE comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-158">Deploy the DKE service as described in this article.</span></span>

2. <span data-ttu-id="4e0f0-159">Créez une étiquette avec un chiffrement à clé double.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-159">Create a label with Double Key Encryption.</span></span> <span data-ttu-id="4e0f0-160">Accédez à protection des informations sous le [Centre de conformité Microsoft 365](https://compliance.microsoft.com) et créez une nouvelle étiquette avec le chiffrement à clé double.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-160">Navigate to Information protection under the [Microsoft 365 compliance center](https://compliance.microsoft.com) and create a new label with Double Key Encryption.</span></span> <span data-ttu-id="4e0f0-161">[Pour appliquer le chiffrement, voir restreindre l’accès au contenu à l’aide des étiquettes de confidentialité](https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels).</span><span class="sxs-lookup"><span data-stu-id="4e0f0-161">See [Restrict access to content by using sensitivity labels to apply encryption](https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels).</span></span>

3. <span data-ttu-id="4e0f0-162">Utilisez des étiquettes de chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-162">Use Double Key Encryption labels.</span></span> <span data-ttu-id="4e0f0-163">Protégez les données en sélectionnant une étiquette chiffrée à double clé dans le ruban de sensibilité de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-163">Protect data by selecting the Double Key Encrypted label from the Sensitivity ribbon in Microsoft Office.</span></span>

<span data-ttu-id="4e0f0-164">Il existe plusieurs façons de procéder pour déployer le chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-164">There are several ways you can complete some of the steps to deploy Double Key Encryption.</span></span> <span data-ttu-id="4e0f0-165">Cet article fournit des instructions détaillées afin que les administrateurs moins expérimentés déploient correctement le service.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-165">This article provides detailed instructions so that less experienced admins successfully deploy the service.</span></span> <span data-ttu-id="4e0f0-166">Si vous êtes familiarisé, vous pouvez choisir d’utiliser vos propres méthodes.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-166">If you're comfortable doing so, you can choose to use your own methods.</span></span>

## <a name="deploy-dke"></a><span data-ttu-id="4e0f0-167">Déployer DKE</span><span class="sxs-lookup"><span data-stu-id="4e0f0-167">Deploy DKE</span></span>

<span data-ttu-id="4e0f0-168">Cet article et la vidéo de déploiement utilisent Azure comme destination de déploiement pour le service DKE.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-168">This article and the deployment video use Azure as the deployment destination for the DKE service.</span></span> <span data-ttu-id="4e0f0-169">Si vous effectuez le déploiement vers un autre emplacement, vous devez fournir vos propres valeurs.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-169">If you're deploying to another location, you'll need to provide your own values.</span></span>

<span data-ttu-id="4e0f0-170">Regardez la [vidéo sur le déploiement de chiffrement à double clé](https://youtu.be/vDWfHN_kygg) pour voir une présentation détaillée des concepts présentés dans cet article.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-170">Watch the [Double Key Encryption deployment video](https://youtu.be/vDWfHN_kygg) to see a step-by-step overview of the concepts in this article.</span></span> <span data-ttu-id="4e0f0-171">La vidéo prend environ 18 minutes.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-171">The video takes about 18 minutes to complete.</span></span>

<span data-ttu-id="4e0f0-172">Suivez ces étapes générales pour configurer le chiffrement à double clé pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-172">You'll follow these general steps to set up Double Key Encryption for your organization.</span></span>

1. [<span data-ttu-id="4e0f0-173">Installer les composants logiciels requis pour le service DKE</span><span class="sxs-lookup"><span data-stu-id="4e0f0-173">Install software prerequisites for the DKE service</span></span>](#install-software-prerequisites-for-the-dke-service)
1. [<span data-ttu-id="4e0f0-174">Cloner le référentiel GitHub de chiffrement à double clé</span><span class="sxs-lookup"><span data-stu-id="4e0f0-174">Clone the Double Key Encryption GitHub repository</span></span>](#clone-the-dke-github-repository)
1. [<span data-ttu-id="4e0f0-175">Modifier les paramètres d’application</span><span class="sxs-lookup"><span data-stu-id="4e0f0-175">Modify application settings</span></span>](#modify-application-settings)
1. [<span data-ttu-id="4e0f0-176">Générer des clés de test</span><span class="sxs-lookup"><span data-stu-id="4e0f0-176">Generate test keys</span></span>](#generate-test-keys)
1. [<span data-ttu-id="4e0f0-177">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-177">Build the project</span></span>](#build-the-project)
1. [<span data-ttu-id="4e0f0-178">Déployer le service DKE et publier le magasin de clés</span><span class="sxs-lookup"><span data-stu-id="4e0f0-178">Deploy the DKE service and publish the key store</span></span>](#deploy-the-dke-service-and-publish-the-key-store)
1. [<span data-ttu-id="4e0f0-179">Valider votre déploiement</span><span class="sxs-lookup"><span data-stu-id="4e0f0-179">Validate your deployment</span></span>](#validate-your-deployment)
1. [<span data-ttu-id="4e0f0-180">Enregistrer votre magasin de clés</span><span class="sxs-lookup"><span data-stu-id="4e0f0-180">Register your key store</span></span>](#register-your-key-store)
1. [<span data-ttu-id="4e0f0-181">Créer des étiquettes de confidentialité à l’aide de DKE</span><span class="sxs-lookup"><span data-stu-id="4e0f0-181">Create sensitivity labels using DKE</span></span>](#create-sensitivity-labels-using-dke)
1. [<span data-ttu-id="4e0f0-182">Activer DKE dans votre client</span><span class="sxs-lookup"><span data-stu-id="4e0f0-182">Enable DKE in your client</span></span>](#enable-dke-in-your-client)
1. [<span data-ttu-id="4e0f0-183">Migrer des fichiers protégés des étiquettes HYOK vers les étiquettes DKE</span><span class="sxs-lookup"><span data-stu-id="4e0f0-183">Migrate protected files from HYOK labels to DKE labels</span></span>](#migrate-protected-files-from-hyok-labels-to-dke-labels)

<span data-ttu-id="4e0f0-184">Lorsque vous avez fini, vous pouvez chiffrer des documents et des fichiers à l’aide de DKE.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-184">When you're done, you can encrypt documents and files using DKE.</span></span> <span data-ttu-id="4e0f0-185">Pour plus d’informations, consultez [la rubrique appliquer des étiquettes de confidentialité à vos fichiers et à votre messagerie électronique dans Office](https://support.microsoft.com/office/2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9).</span><span class="sxs-lookup"><span data-stu-id="4e0f0-185">For information, see [Apply sensitivity labels to your files and email in Office](https://support.microsoft.com/office/2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9).</span></span>

### <a name="install-software-prerequisites-for-the-dke-service"></a><span data-ttu-id="4e0f0-186">Installer les composants logiciels requis pour le service DKE</span><span class="sxs-lookup"><span data-stu-id="4e0f0-186">Install software prerequisites for the DKE service</span></span>

<span data-ttu-id="4e0f0-187">Installez ces éléments prérequis sur l’ordinateur sur lequel vous souhaitez installer le service DKE.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-187">Install these prerequisites on the computer where you want to install the DKE service.</span></span>

<span data-ttu-id="4e0f0-188">**.Net Core 3,1 SDK**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-188">**.NET Core 3.1 SDK**.</span></span> <span data-ttu-id="4e0f0-189">Téléchargez et installez le kit de développement logiciel (SDK) à partir de [Télécharger .net Core 3,1](https://dotnet.microsoft.com/download/dotnet-core/3.1).</span><span class="sxs-lookup"><span data-stu-id="4e0f0-189">Download and install the SDK from [Download .NET Core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1).</span></span>

<span data-ttu-id="4e0f0-190">**Visual Studio code**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-190">**Visual Studio Code**.</span></span> <span data-ttu-id="4e0f0-191">Téléchargez Visual Studio code à partir de [https://code.visualstudio.com/](https://code.visualstudio.com) .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-191">Download Visual Studio Code from [https://code.visualstudio.com/](https://code.visualstudio.com).</span></span> <span data-ttu-id="4e0f0-192">Une fois installé, exécutez Visual Studio code et sélectionnez **Afficher** les \> **Extensions**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-192">Once installed, run Visual Studio Code and select **View** \> **Extensions**.</span></span> <span data-ttu-id="4e0f0-193">Installez ces extensions.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-193">Install these extensions.</span></span>

- <span data-ttu-id="4e0f0-194">C# pour Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="4e0f0-194">C# for Visual Studio Code</span></span>

- <span data-ttu-id="4e0f0-195">Gestionnaire de package NuGet</span><span class="sxs-lookup"><span data-stu-id="4e0f0-195">NuGet Package Manager</span></span>

<span data-ttu-id="4e0f0-196">**Ressources git**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-196">**Git resources**.</span></span> <span data-ttu-id="4e0f0-197">Téléchargez et installez l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-197">Download and install one of the following.</span></span>

- [<span data-ttu-id="4e0f0-198">Git</span><span class="sxs-lookup"><span data-stu-id="4e0f0-198">Git</span></span>](https://git-scm.com/downloads)

- [<span data-ttu-id="4e0f0-199">Bureau GitHub</span><span class="sxs-lookup"><span data-stu-id="4e0f0-199">GitHub Desktop</span></span>](https://desktop.github.com/)

- [<span data-ttu-id="4e0f0-200">GitHub entreprise</span><span class="sxs-lookup"><span data-stu-id="4e0f0-200">GitHub Enterprise</span></span>](https://github.com/enterprise)

<span data-ttu-id="4e0f0-201">**OpenSSL** [OpenSSL](https://slproweb.com/products/Win32OpenSSL.html) doit être installé pour [générer des clés de test](#generate-test-keys) une fois que vous avez déployé DKE.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-201">**OpenSSL** You must have [OpenSSL](https://slproweb.com/products/Win32OpenSSL.html) installed to [generate test keys](#generate-test-keys) after you deploy DKE.</span></span> <span data-ttu-id="4e0f0-202">Vérifiez que vous l’appelez correctement à partir de votre chemin d’accès aux variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-202">Make sure you're invoking it correctly from your environment variables path.</span></span> <span data-ttu-id="4e0f0-203">Par exemple, pour plus d’informations, consultez la section « ajouter le répertoire d’installation au chemin d’accès » [https://www.osradar.com/install-openssl-windows/](https://www.osradar.com/install-openssl-windows/) .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-203">For example, see "Add the installation directory to PATH" at [https://www.osradar.com/install-openssl-windows/](https://www.osradar.com/install-openssl-windows/) for details.</span></span>

### <a name="clone-the-dke-github-repository"></a><span data-ttu-id="4e0f0-204">Cloner le référentiel DKE GitHub</span><span class="sxs-lookup"><span data-stu-id="4e0f0-204">Clone the DKE GitHub repository</span></span>

<span data-ttu-id="4e0f0-205">Microsoft fournit les fichiers source DKE dans un référentiel GitHub.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-205">Microsoft supplies the DKE source files in a GitHub repository.</span></span> <span data-ttu-id="4e0f0-206">Vous clonez le référentiel pour créer le projet localement pour l’utilisation de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-206">You clone the repository to build the project locally for your organization's use.</span></span> <span data-ttu-id="4e0f0-207">Le référentiel DKE GitHub se trouve à l’emplacement [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService) .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-207">The DKE GitHub repository is located at [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService).</span></span>

<span data-ttu-id="4e0f0-208">Les instructions suivantes sont destinées aux utilisateurs de git ou de code Visual Studio inexpérimentés :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-208">The following instructions are intended for inexperienced git or Visual Studio Code users:</span></span>

1. <span data-ttu-id="4e0f0-209">Dans votre navigateur, accédez à : [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService) .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-209">In your browser, go to: [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService).</span></span>

2. <span data-ttu-id="4e0f0-210">Dans la partie droite de l’écran, sélectionnez **code**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-210">Towards the right side of the screen, select **Code**.</span></span> <span data-ttu-id="4e0f0-211">Votre version de l’interface utilisateur peut afficher un bouton **Clone ou télécharger** .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-211">Your version of the UI might show a **Clone or download** button.</span></span> <span data-ttu-id="4e0f0-212">Ensuite, dans la liste déroulante qui apparaît, sélectionnez l’icône copier pour copier l’URL dans votre presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-212">Then, in the dropdown that appears, select the copy icon to copy the URL to your clipboard.</span></span>

    <span data-ttu-id="4e0f0-213">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-213">For example:</span></span>

   ![Cloner le référentiel du service de chiffrement à clé double à partir de GitHub](../media/dke-clone.png)

3. <span data-ttu-id="4e0f0-215">Dans Visual Studio code, sélectionnez **Afficher** la \> **palette de commandes** et sélectionnez **git : Clone**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-215">In Visual Studio Code, select **View** \> **Command Palette** and select **Git: Clone**.</span></span> <span data-ttu-id="4e0f0-216">Pour accéder à l’option dans la liste, commencez `git: clone` à taper pour filtrer les entrées, puis sélectionnez-la dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-216">To jump to the option in the list, start typing `git: clone` to filter the entries and then select it from the drop-down.</span></span> <span data-ttu-id="4e0f0-217">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-217">For example:</span></span>

   ![Option GIT : clone de Visual Studio code](../media/dke-vscode-clone.png)

4. <span data-ttu-id="4e0f0-219">Dans la zone de texte, collez l’URL que vous avez copiée à partir de git et sélectionnez **Clone dans GitHub**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-219">In the text box, paste the URL that you copied from Git and select **Clone from GitHub**.</span></span>

5. <span data-ttu-id="4e0f0-220">Dans la boîte de dialogue **Sélectionner un dossier** qui s’affiche, accédez à l’emplacement où vous souhaitez stocker le référentiel et sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-220">In the **Select Folder** dialog that appears, browse to and select a location to store the repository.</span></span> <span data-ttu-id="4e0f0-221">À l’invite, sélectionnez **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-221">At the prompt, select **Open**.</span></span>

    <span data-ttu-id="4e0f0-222">Le référentiel s’ouvre dans Visual Studio code et affiche la branche git actuelle en bas à gauche.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-222">The repository opens in Visual Studio Code, and displays the current Git branch at the bottom left.</span></span> <span data-ttu-id="4e0f0-223">La branche doit être **Master**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-223">The branch should be **master**.</span></span>

    <span data-ttu-id="4e0f0-224">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-224">For example:</span></span>

   ![Branche Visual Studio code Master](../media/dke-vscode-master.png)

6. <span data-ttu-id="4e0f0-226">Sélectionnez le **masque** de mots dans la liste des branches.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-226">Select the word **master** from the list of branches.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="4e0f0-227">La sélection de la branche principale garantit que vous disposez des fichiers appropriés pour générer le projet.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-227">Selecting the master branch ensures that you have the correct files to build the project.</span></span> <span data-ttu-id="4e0f0-228">Si vous ne sélectionnez pas la branche appropriée, votre déploiement échouera.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-228">If you do not choose the correct branch your deployment will fail.</span></span>

<span data-ttu-id="4e0f0-229">Votre référentiel source DKE est maintenant configuré localement.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-229">You now have your DKE source repository set up locally.</span></span> <span data-ttu-id="4e0f0-230">Ensuite, [Modifiez les paramètres d’application](#modify-application-settings) pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-230">Next, [modify application settings](#modify-application-settings) for your organization.</span></span>

### <a name="modify-application-settings"></a><span data-ttu-id="4e0f0-231">Modifier les paramètres d’application</span><span class="sxs-lookup"><span data-stu-id="4e0f0-231">Modify application settings</span></span>

<span data-ttu-id="4e0f0-232">Pour déployer le service DKE, vous devez modifier les types de paramètres d’application suivants :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-232">To deploy the DKE service, you must modify the following types of application settings:</span></span>

- [<span data-ttu-id="4e0f0-233">Paramètres d’accès clés</span><span class="sxs-lookup"><span data-stu-id="4e0f0-233">Key access settings</span></span>](#key-access-settings)
- [<span data-ttu-id="4e0f0-234">Paramètres de client et de clé</span><span class="sxs-lookup"><span data-stu-id="4e0f0-234">Tenant and key settings</span></span>](#tenant-and-key-settings)

<span data-ttu-id="4e0f0-235">Vous modifiez les paramètres de l’application dans le fichier appsettings.js.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-235">You modify application settings in the appsettings.json file.</span></span> <span data-ttu-id="4e0f0-236">Ce fichier se trouve dans le DoubleKeyEncryptionService référentiel que vous avez cloné localement sous DoubleKeyEncryptionService\src\customer-key-store.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-236">This file is located in the DoubleKeyEncryptionService repo you cloned locally under DoubleKeyEncryptionService\src\customer-key-store.</span></span> <span data-ttu-id="4e0f0-237">Par exemple, dans Visual Studio code, vous pouvez accéder au fichier comme indiqué dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-237">For example, in Visual Studio Code, you can browse to the file as shown in the following picture.</span></span>

![Recherche de la appsettings.jssur le fichier pour DKE.](../media/dke-appsettingsjson.png)

#### <a name="key-access-settings"></a><span data-ttu-id="4e0f0-239">Paramètres d’accès clés</span><span class="sxs-lookup"><span data-stu-id="4e0f0-239">Key access settings</span></span>

<span data-ttu-id="4e0f0-240">Choisissez d’utiliser ou non l’autorisation de messagerie ou de rôle.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-240">Choose whether to use email or role authorization.</span></span> <span data-ttu-id="4e0f0-241">DKE ne prend en charge qu’une seule de ces méthodes d’authentification à la fois.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-241">DKE supports only one of these authentication methods at a time.</span></span>

- <span data-ttu-id="4e0f0-242">**Autorisation de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-242">**Email authorization**.</span></span> <span data-ttu-id="4e0f0-243">Permet à votre organisation d’autoriser l’accès aux clés en fonction des adresses de messagerie uniquement.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-243">Allows your organization to authorize access to keys based on email addresses only.</span></span>

- <span data-ttu-id="4e0f0-244">**Autorisation de rôle**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-244">**Role authorization**.</span></span> <span data-ttu-id="4e0f0-245">Permet à votre organisation d’autoriser l’accès aux clés en fonction des groupes Active Directory et exige que le service Web interroge LDAP.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-245">Allows your organization to authorize access to keys based on Active Directory groups, and requires that the web service can query LDAP.</span></span>

<span data-ttu-id="4e0f0-246">**Pour définir les paramètres d’accès clés pour DKE à l’aide de l’autorisation de messagerie**</span><span class="sxs-lookup"><span data-stu-id="4e0f0-246">**To set key access settings for DKE using email authorization**</span></span>

1. <span data-ttu-id="4e0f0-247">Ouvrez le fichier **appsettings.js** et localisez le `AuthorizedEmailAddress` paramètre.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-247">Open the **appsettings.json** file and locate the `AuthorizedEmailAddress` setting.</span></span>

2. <span data-ttu-id="4e0f0-248">Ajoutez l’adresse ou les adresses de messagerie que vous souhaitez autoriser.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-248">Add the email address or addresses that you want to authorize.</span></span> <span data-ttu-id="4e0f0-249">Séparez les adresses de messagerie par des guillemets et des virgules.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-249">Separate multiple email addresses with double quotes and commas.</span></span> <span data-ttu-id="4e0f0-250">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-250">For example:</span></span>

   ```json
   "AuthorizedEmailAddress": ["email1@company.com", "email2@company.com ", "email3@company.com"]
   ```

3. <span data-ttu-id="4e0f0-251">Recherchez le `LDAPPath` paramètre et supprimez le texte `If you use role authorization (AuthorizedRoles) then this is the LDAP path.` entre guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-251">Locate the `LDAPPath` setting and remove the text `If you use role authorization (AuthorizedRoles) then this is the LDAP path.` between the double quotes.</span></span> <span data-ttu-id="4e0f0-252">Laissez les guillemets doubles en place.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-252">Leave the double quotes in place.</span></span> <span data-ttu-id="4e0f0-253">Lorsque vous avez terminé, le paramètre doit ressembler à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-253">When you're finished, the setting should look like this.</span></span>

   ```json
   "LDAPPath": ""
   ```

4. <span data-ttu-id="4e0f0-254">Localisez le `AuthorizedRoles` paramètre et supprimez la ligne entière.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-254">Locate the `AuthorizedRoles` setting and delete the entire line.</span></span>

<span data-ttu-id="4e0f0-255">Cette image montre le **appsettings.jssur** un fichier correctement mis en forme pour l’autorisation de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-255">This image shows the **appsettings.json** file correctly formatted for email authorization.</span></span>

   ![appsettings.jssur le fichier affichant la méthode d’autorisation de messagerie](../media/dke-email-accesssetting.png)

<span data-ttu-id="4e0f0-257">**Pour définir les paramètres d’accès clés pour DKE à l’aide de l’autorisation de rôle**</span><span class="sxs-lookup"><span data-stu-id="4e0f0-257">**To set key access settings for DKE using role authorization**</span></span>

1. <span data-ttu-id="4e0f0-258">Ouvrez le fichier **appsettings.js** et localisez le `AuthorizedRoles` paramètre.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-258">Open the **appsettings.json** file and locate the `AuthorizedRoles` setting.</span></span>

2. <span data-ttu-id="4e0f0-259">Ajoutez les noms de groupe Active Directory que vous souhaitez autoriser.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-259">Add the Active Directory group names you want to authorize.</span></span> <span data-ttu-id="4e0f0-260">Séparez les noms de plusieurs groupes par des guillemets et des virgules.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-260">Separate multiple group names with double quotes and commas.</span></span> <span data-ttu-id="4e0f0-261">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-261">For example:</span></span>

   ```json
   "AuthorizedRoles": ["group1", "group2", "group3"]
   ```

3. <span data-ttu-id="4e0f0-262">Localisez le `LDAPPath` paramètre et ajoutez le domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-262">Locate the `LDAPPath` setting and add the Active Directory domain.</span></span> <span data-ttu-id="4e0f0-263">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-263">For example:</span></span>

   ```json
   "LDAPPath": "contoso.com"
   ```

4. <span data-ttu-id="4e0f0-264">Localisez le `AuthorizedEmailAddress` paramètre et supprimez la ligne entière.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-264">Locate the `AuthorizedEmailAddress` setting and delete the entire line.</span></span>

<span data-ttu-id="4e0f0-265">Cette image montre le **appsettings.jssur** un fichier correctement mis en forme pour l’autorisation de rôle.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-265">This image shows the **appsettings.json** file correctly formatted for role authorization.</span></span>

   ![appsettings.jssur le fichier affichant la méthode d’autorisation de rôle](../media/dke-role-accesssetting.png)

#### <a name="tenant-and-key-settings"></a><span data-ttu-id="4e0f0-267">Paramètres de client et de clé</span><span class="sxs-lookup"><span data-stu-id="4e0f0-267">Tenant and key settings</span></span>

<span data-ttu-id="4e0f0-268">Les paramètres de client et de clé DKE se trouvent dans le fichier **appsettings.js** .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-268">DKE tenant and key settings are located in the **appsettings.json** file.</span></span>

<span data-ttu-id="4e0f0-269">**Pour configurer les paramètres de client et de clé pour DKE**</span><span class="sxs-lookup"><span data-stu-id="4e0f0-269">**To configure tenant and key settings for DKE**</span></span>

1. <span data-ttu-id="4e0f0-270">Ouvrez le fichier **appsettings.js** .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-270">Open the **appsettings.json** file.</span></span>

2. <span data-ttu-id="4e0f0-271">Recherchez le `ValidIssuers` paramètre et remplacez-le `<tenantid>` par votre ID de client.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-271">Locate the `ValidIssuers` setting and replace `<tenantid>` with your tenant ID.</span></span> <span data-ttu-id="4e0f0-272">Vous pouvez localiser votre ID de locataire en accédant au portail Azure et en affichant les [Propriétés du client](https://aad.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span><span class="sxs-lookup"><span data-stu-id="4e0f0-272">You can locate your tenant ID by going to the Azure portal and viewing the [tenant properties](https://aad.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span></span> <span data-ttu-id="4e0f0-273">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-273">For example:</span></span>

   ```json
   "ValidIssuers": [
     "https://sts.windows.net/9c99431e-b513-44be-a7d9-e7b500002d4b/"
   ]
   ```

<span data-ttu-id="4e0f0-274">Localisez le `JwtAudience` .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-274">Locate the `JwtAudience`.</span></span> <span data-ttu-id="4e0f0-275">Remplacez `<yourhostname>` par le nom d’hôte de l’ordinateur sur lequel le service DKE s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-275">Replace `<yourhostname>` with the hostname of the machine where the DKE service will run.</span></span> <span data-ttu-id="4e0f0-276">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-276">For example:</span></span>

  > [!IMPORTANT]
  > <span data-ttu-id="4e0f0-277">La valeur de `JwtAudience` doit correspondre *exactement*au nom de votre hôte.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-277">The value for `JwtAudience` must match the name of your host *exactly*.</span></span> <span data-ttu-id="4e0f0-278">Vous pouvez utiliser **localhost : 5001** lors du débogage.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-278">You may use **localhost:5001** while debugging.</span></span> <span data-ttu-id="4e0f0-279">Toutefois, lorsque vous avez fini de déboguer, veillez à mettre à jour cette valeur sur le nom d’hôte du serveur.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-279">However, When you're done debugging, make sure to update this value to the server's hostname.</span></span>

- <span data-ttu-id="4e0f0-280">`TestKeys:Name`.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-280">`TestKeys:Name`.</span></span> <span data-ttu-id="4e0f0-281">Entrez un nom pour votre clé.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-281">Enter a name for your key.</span></span> <span data-ttu-id="4e0f0-282">Par exemple : `TestKey1`</span><span class="sxs-lookup"><span data-stu-id="4e0f0-282">For example: `TestKey1`</span></span>
- <span data-ttu-id="4e0f0-283">`TestKeys:Id`.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-283">`TestKeys:Id`.</span></span> <span data-ttu-id="4e0f0-284">Créez un GUID et entrez-le en tant que `TestKeys:ID` valeur.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-284">Create a GUID and enter it as the `TestKeys:ID` value.</span></span> <span data-ttu-id="4e0f0-285">Par exemple, `DCE1CC21-FF9B-4424-8FF4-9914BD19A1BE`.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-285">For example, `DCE1CC21-FF9B-4424-8FF4-9914BD19A1BE`.</span></span> <span data-ttu-id="4e0f0-286">Vous pouvez utiliser un site comme le [Générateur de GUID en ligne](https://guidgenerator.com/) pour générer un GUID de manière aléatoire.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-286">You can use a site like [Online GUID Generator](https://guidgenerator.com/) to randomly generate a GUID.</span></span>

<span data-ttu-id="4e0f0-287">Cette image indique le format correct pour les paramètres de client et de clé dans **appsettings.jsactivé**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-287">This image shows the correct format for tenant and keys settings in **appsettings.json**.</span></span> <span data-ttu-id="4e0f0-288">`LDAPPath` est configuré pour l’autorisation de rôle.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-288">`LDAPPath` is configured for role authorization.</span></span>

![Indique les paramètres client et clé corrects pour DKE dans le fichier appsettings.js.](../media/dke-appsettingsjson-tenantkeysettings.png)

### <a name="generate-test-keys"></a><span data-ttu-id="4e0f0-290">Générer des clés de test</span><span class="sxs-lookup"><span data-stu-id="4e0f0-290">Generate test keys</span></span>

<span data-ttu-id="4e0f0-291">Une fois que vous avez défini les paramètres de votre application, vous êtes prêt à générer des clés de test publiques et privées.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-291">Once you have your application settings defined, you're ready to generate public and private test keys.</span></span>

<span data-ttu-id="4e0f0-292">Pour générer des clés :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-292">To generate keys:</span></span>

1. <span data-ttu-id="4e0f0-293">Dans le menu Démarrer de Windows, exécutez l’invite de commandes OpenSSL.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-293">From the Windows Start menu, run the OpenSSL Command Prompt.</span></span>

2. <span data-ttu-id="4e0f0-294">Accédez au dossier dans lequel vous souhaitez enregistrer les clés de test.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-294">Change to the folder where you want to save the test keys.</span></span> <span data-ttu-id="4e0f0-295">Les fichiers que vous créez en suivant les étapes de cette tâche sont stockés dans le même dossier.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-295">The files you create by completing the steps in this task are stored in the same folder.</span></span>

3. <span data-ttu-id="4e0f0-296">Générez la nouvelle clé de test.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-296">Generate the new test key.</span></span>

   ```dos
   openssl req -x509 -newkey rsa:2048 -keyout key.pem -out cert.pem -days 365
   ```

4. <span data-ttu-id="4e0f0-297">Générez la clé privée.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-297">Generate the private key.</span></span>

   ```dos
   openssl rsa -in key.pem -out privkeynopass.pem
   ```

5. <span data-ttu-id="4e0f0-298">Générez la clé publique.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-298">Generate the public key.</span></span>

   ```dos
   openssl rsa -in key.pem -pubout > pubkeyonly.pem
   ```

6. <span data-ttu-id="4e0f0-299">Dans un éditeur de texte, ouvrez **pubkeyonly. pem**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-299">In a text editor, open **pubkeyonly.pem**.</span></span> <span data-ttu-id="4e0f0-300">Copiez tout le contenu du fichier **pubkeyonly. pem** , à l’exception de la première et de la dernière ligne, dans la `PublicPem` section du fichier **appsettings.js** .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-300">Copy all of the content in the **pubkeyonly.pem** file, except the first and last lines, into the `PublicPem` section of the **appsettings.json** file.</span></span>

7. <span data-ttu-id="4e0f0-301">Dans un éditeur de texte, ouvrez **privkeynopass. pem**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-301">In a text editor, open **privkeynopass.pem**.</span></span> <span data-ttu-id="4e0f0-302">Copiez tout le contenu du fichier **privkeynopass. pem** , à l’exception de la première et de la dernière ligne, dans la `PrivatePem` section du fichier **appsettings.js** .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-302">Copy all of the content in the **privkeynopass.pem** file, except the first and last lines, into the `PrivatePem` section of the **appsettings.json** file.</span></span>

8. <span data-ttu-id="4e0f0-303">Supprimez tous les espaces et lignes de nouvelle ligne dans les `PublicPem` `PrivatePem` sections et.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-303">Remove all blank spaces and newlines in both the `PublicPem` and `PrivatePem` sections.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="4e0f0-304">Lorsque vous copiez ce contenu, ne supprimez pas les données du PEM.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-304">When you copy this content, do not delete any of the PEM data.</span></span>

9. <span data-ttu-id="4e0f0-305">Dans Visual Studio code, accédez au fichier **Startup.cs** .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-305">In Visual Studio Code, browse to the **Startup.cs** file.</span></span> <span data-ttu-id="4e0f0-306">Ce fichier se trouve dans le DoubleKeyEncryptionService référentiel que vous avez cloné localement sous DoubleKeyEncryptionService\src\customer-key-store\.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-306">This file is located in the DoubleKeyEncryptionService repo you cloned locally under DoubleKeyEncryptionService\src\customer-key-store\.</span></span>

10. <span data-ttu-id="4e0f0-307">Recherchez les lignes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-307">Locate the following lines:</span></span>

   ```c#
        #if USE_TEST_KEYS
        #error !!!!!!!!!!!!!!!!!!!!!! Use of test keys is only supported for testing,
        DO NOT USE FOR PRODUCTION !!!!!!!!!!!!!!!!!!!!!!!!!!!!!
        services.AddSingleton<ippw.IKeyStore, ippw.TestKeyStore>();
        #endif
   ```

11. <span data-ttu-id="4e0f0-308">Remplacez ces lignes par le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-308">Replace these lines with the following text:</span></span>

   ```csharp
   services.AddSingleton<ippw.IKeyStore, ippw.TestKeyStore>();
   ```

   <span data-ttu-id="4e0f0-309">Les résultats finaux doivent ressembler à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-309">The end results should look similar to the following.</span></span>

   ![fichier startup.cs pour la préversion publique](../media/dke-startupcs-usetestkeys.png)

<span data-ttu-id="4e0f0-311">Vous êtes maintenant prêt à [créer votre projet DKE](#build-the-project).</span><span class="sxs-lookup"><span data-stu-id="4e0f0-311">Now you're ready to [build your DKE project](#build-the-project).</span></span>

### <a name="build-the-project"></a><span data-ttu-id="4e0f0-312">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-312">Build the project</span></span>

<span data-ttu-id="4e0f0-313">Suivez les instructions ci-dessous pour générer le projet DKE localement :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-313">Use the following instructions to build the DKE project locally:</span></span>

1. <span data-ttu-id="4e0f0-314">Dans Visual Studio code, dans le référentiel du service DKE, sélectionnez **Afficher** la \> **palette de commandes** , puis tapez **générer** à l’invite.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-314">In Visual Studio Code, in the DKE service repository, select **View** \> **Command Palette** and then type **build** at the prompt.</span></span>

2. <span data-ttu-id="4e0f0-315">Dans la liste, choisissez **tâches : exécuter la tâche de génération**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-315">From the list, choose **Tasks: Run build task**.</span></span>

   <span data-ttu-id="4e0f0-316">Si aucune tâche de génération n’a été trouvée, sélectionnez **configurer la tâche de génération** et créez-en une pour .net Core comme suit.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-316">If there are no build tasks found, select **Configure Build Task** and create one for .NET core as follows.</span></span>

   ![Configurer une tâche de génération manquante pour .NET](../media/dke-configurebuildtask.png)

   1. <span data-ttu-id="4e0f0-318">Choisissez **create tasks.json from template**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-318">Choose **Create tasks.json from template**.</span></span>

      ![Créer tasks.jssur le fichier à partir du modèle pour DKE](../media/dke-createtasksjsonfromtemplate.png)

   2. <span data-ttu-id="4e0f0-320">Dans la liste des types de modèles, sélectionnez **.net Core**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-320">From the list of template types, select **.NET Core**.</span></span>

      ![Sélectionnez le modèle approprié pour DKE](../media/dke-tasksjsontemplate.png)

   3. <span data-ttu-id="4e0f0-322">Dans la section générer, recherchez le chemin d’accès au fichier **customerkeystore. csproj** .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-322">In the build section, locate the path to the **customerkeystore.csproj** file.</span></span> <span data-ttu-id="4e0f0-323">Si ce n’est pas le cas, ajoutez la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-323">If it's not there, add the following line:</span></span>

      ```json
      "${workspaceFolder}/src/customer-key-store/customerkeystore.csproj",
      ```

   4. <span data-ttu-id="4e0f0-324">Exécutez de nouveau la génération.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-324">Run the build again.</span></span>

3. <span data-ttu-id="4e0f0-325">Vérifiez qu’il n’y a pas d’erreurs rouges dans la fenêtre sortie.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-325">Verify that there are no red errors in the output window.</span></span>

   <span data-ttu-id="4e0f0-326">S’il y a des erreurs rouges, vérifiez la sortie de la console.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-326">If there are red errors, check the console output.</span></span> <span data-ttu-id="4e0f0-327">Assurez-vous que vous avez effectué toutes les étapes précédentes correctement et que les versions de build correctes sont présentes.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-327">Ensure that you completed all the previous steps correctly and the correct build versions are present.</span></span>

4. <span data-ttu-id="4e0f0-328">Sélectionnez **exécuter** \> **Démarrer le débogage** pour déboguer le processus.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-328">Select **Run** \> **Start Debugging** to debug the process.</span></span> <span data-ttu-id="4e0f0-329">Si vous êtes invité à sélectionner un environnement, sélectionnez **.net Core**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-329">If you're prompted to select an environment, select **.NET core**.</span></span>

<span data-ttu-id="4e0f0-330">Le débogueur .NET Core se lance généralement vers `https://localhost:5001` .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-330">The .NET core debugger typically launches to `https://localhost:5001`.</span></span> <span data-ttu-id="4e0f0-331">Pour afficher votre clé de test, accédez à `https://localhost:5001` et ajoutez une barre oblique (/) et le nom de votre clé.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-331">To view your test key, go to `https://localhost:5001` and append a forward slash (/) and the name of your key.</span></span> <span data-ttu-id="4e0f0-332">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-332">For example:</span></span>

```https
https://localhost:5001/TestKey1
```

<span data-ttu-id="4e0f0-333">La clé doit s’afficher au format JSON.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-333">The key should display in JSON format.</span></span>

<span data-ttu-id="4e0f0-334">Votre installation est maintenant terminée.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-334">Your setup is now complete.</span></span> <span data-ttu-id="4e0f0-335">Avant de publier le keystore, dans appsettings.jsactivé, pour le paramètre JwtAudience, vérifiez que la valeur de hostname correspond exactement au nom de l’hôte de service de l’application.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-335">Before you publish the keystore, in appsettings.json, for the JwtAudience setting, ensure the value for hostname exactly matches your App Service host name.</span></span> <span data-ttu-id="4e0f0-336">Vous pouvez l’avoir remplacée par localhost pour dépanner la Build.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-336">You may have changed it to localhost to troubleshoot the build.</span></span>

### <a name="deploy-the-dke-service-and-publish-the-key-store"></a><span data-ttu-id="4e0f0-337">Déployer le service DKE et publier le magasin de clés</span><span class="sxs-lookup"><span data-stu-id="4e0f0-337">Deploy the DKE service and publish the key store</span></span>

<span data-ttu-id="4e0f0-338">Pour les déploiements de production, déployez le service dans un nuage tiers ou [publiez-le sur un système local](https://docs.microsoft.com/aspnet/core/tutorials/publish-to-iis?view=aspnetcore-3.1&preserve-view=true&tabs=netcore-cli).</span><span class="sxs-lookup"><span data-stu-id="4e0f0-338">For production deployments, deploy the service either in a third-party cloud or [publish to an on-premises system](https://docs.microsoft.com/aspnet/core/tutorials/publish-to-iis?view=aspnetcore-3.1&preserve-view=true&tabs=netcore-cli).</span></span>

<span data-ttu-id="4e0f0-339">Vous pouvez préférer d’autres méthodes de déploiement de vos clés.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-339">You may prefer other methods to deploy your keys.</span></span> <span data-ttu-id="4e0f0-340">Sélectionnez la méthode qui convient le mieux à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-340">Select the method that works best for your organization.</span></span>

<span data-ttu-id="4e0f0-341">Pour les déploiements pilotes, vous pouvez déployer dans Azure et commencer immédiatement.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-341">For pilot deployments, you can deploy in Azure and get started right away.</span></span>

<span data-ttu-id="4e0f0-342">**Pour créer une instance Azure Web App afin d’héberger votre déploiement DKE**</span><span class="sxs-lookup"><span data-stu-id="4e0f0-342">**To create an Azure Web App instance to host your DKE deployment**</span></span>

<span data-ttu-id="4e0f0-343">Pour publier le magasin de clés, vous allez créer une instance de service d’application Azure pour héberger votre déploiement DKE.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-343">To publish the key store, you'll create an Azure App Service instance to host your DKE deployment.</span></span> <span data-ttu-id="4e0f0-344">Ensuite, vous allez publier vos clés générées dans Azure.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-344">Next, you'll publish your generated keys to Azure.</span></span>

1. <span data-ttu-id="4e0f0-345">Dans votre navigateur, connectez-vous au [portail Microsoft Azure](https://ms.portal.azure.com)et accédez à **app services**  >  **Add**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-345">In your browser, sign in to the [Microsoft Azure portal](https://ms.portal.azure.com), and go to **App Services** > **Add**.</span></span>

2. <span data-ttu-id="4e0f0-346">Sélectionnez votre abonnement et le groupe de ressources, puis définissez les détails de votre instance.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-346">Select your subscription and resource group and define your instance details.</span></span>

    - <span data-ttu-id="4e0f0-347">Entrez le nom d’hôte de l’ordinateur sur lequel vous souhaitez installer le service DKE.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-347">Enter the hostname of the computer where you want to install the DKE service.</span></span> <span data-ttu-id="4e0f0-348">Assurez-vous qu’il s’agit du même nom que celui défini pour le paramètre JwtAudience dans le fichier [**appsettings.js**](#tenant-and-key-settings) .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-348">Make sure it's the same name as the one defined for the JwtAudience setting in the [**appsettings.json**](#tenant-and-key-settings) file.</span></span> <span data-ttu-id="4e0f0-349">La valeur que vous fournissez pour le nom est également WebAppInstanceName.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-349">The value you provide for the name is also the WebAppInstanceName.</span></span>

    - <span data-ttu-id="4e0f0-350">Pour **publier**, sélectionner le **code**et pour la **pile Runtime**, sélectionnez **.net Core 3,1**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-350">For **Publish**, select **code**, and for **Runtime stack**, select **.NET Core 3.1**.</span></span>

    <span data-ttu-id="4e0f0-351">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-351">For example:</span></span>

   ![Ajouter votre service d’application](../media/dke-azure-add-app-service.png)

3. <span data-ttu-id="4e0f0-353">Au bas de la page, sélectionnez **révision + créer**, puis **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-353">At the bottom of the page, select **Review + create**, and then select **Add**.</span></span>

4. <span data-ttu-id="4e0f0-354">Effectuez l’une des opérations suivantes pour publier vos clés générées :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-354">Do one of the following to publish your generated keys:</span></span>

    - [<span data-ttu-id="4e0f0-355">Publier via ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="4e0f0-355">Publish via ZipDeployUI</span></span>](#publish-via-zipdeployui)
    - [<span data-ttu-id="4e0f0-356">Publier via FTP</span><span class="sxs-lookup"><span data-stu-id="4e0f0-356">Publish via FTP</span></span>](#publish-via-ftp)
    - [<span data-ttu-id="4e0f0-357">Publier via Visual Studio 2019 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4e0f0-357">Publish via Visual Studio 2019 or later</span></span>](https://docs.microsoft.com/aspnet/core/tutorials/)

#### <a name="publish-via-zipdeployui"></a><span data-ttu-id="4e0f0-358">Publier via ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="4e0f0-358">Publish via ZipDeployUI</span></span>

1. <span data-ttu-id="4e0f0-359">Accédez à `https://<WebAppInstanceName>.scm.azurewebsites.net/ZipDeployUI`.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-359">Go to `https://<WebAppInstanceName>.scm.azurewebsites.net/ZipDeployUI`.</span></span>

    <span data-ttu-id="4e0f0-360">Par exemple : https://dkeservice.scm.azurewebsites.net/ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="4e0f0-360">For example: https://dkeservice.scm.azurewebsites.net/ZipDeployUI</span></span>

2. <span data-ttu-id="4e0f0-361">Dans la base de code pour le magasin de clés, accédez au dossier **Customer-Key-store\src\customer-Key-Store** et vérifiez que ce dossier contient le fichier **customerkeystore. csproj** .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-361">In the codebase for the key store, go to the **customer-key-store\src\customer-key-store** folder, and verify that this folder contains the **customerkeystore.csproj** file.</span></span>

3. <span data-ttu-id="4e0f0-362">Exécuter : **publication dotnet**</span><span class="sxs-lookup"><span data-stu-id="4e0f0-362">Run: **dotnet publish**</span></span>

     <span data-ttu-id="4e0f0-363">La fenêtre sortie affiche le répertoire dans lequel la publication a été déployée.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-363">The output window displays the directory where the publish was deployed.</span></span>

    <span data-ttu-id="4e0f0-364">Par exemple : `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span><span class="sxs-lookup"><span data-stu-id="4e0f0-364">For example: `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span></span>

4. <span data-ttu-id="4e0f0-365">Envoyez tous les fichiers du répertoire de publication dans un fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-365">Send all files in the publish directory to a .zip file.</span></span> <span data-ttu-id="4e0f0-366">Lors de la création du fichier. zip, assurez-vous que tous les fichiers du répertoire sont au niveau racine du fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-366">When creating the .zip file, make sure that all files in the directory are at the root level of the .zip file.</span></span>

5. <span data-ttu-id="4e0f0-367">Faites glisser et déposez le fichier. zip que vous créez sur le site ZipDeployUI que vous avez ouvert ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-367">Drag and drop the .zip file you create to the ZipDeployUI site you opened above.</span></span> <span data-ttu-id="4e0f0-368">Par exemple : https://dkeservice.scm.azurewebsites.net/ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="4e0f0-368">For example: https://dkeservice.scm.azurewebsites.net/ZipDeployUI</span></span>

<span data-ttu-id="4e0f0-369">DKE est déployé et vous pouvez accéder aux clés de test que vous avez créées.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-369">DKE is deployed and you can browse to the test keys you've created.</span></span> <span data-ttu-id="4e0f0-370">Poursuivez [la validation de votre déploiement](#validate-your-deployment) ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-370">Continue to [Validate your deployment](#validate-your-deployment) below.</span></span>

#### <a name="publish-via-ftp"></a><span data-ttu-id="4e0f0-371">Publier via FTP</span><span class="sxs-lookup"><span data-stu-id="4e0f0-371">Publish via FTP</span></span>

1. <span data-ttu-id="4e0f0-372">Connectez-vous au service d’application que vous avez créé [ci-dessus](#deploy-the-dke-service-and-publish-the-key-store).</span><span class="sxs-lookup"><span data-stu-id="4e0f0-372">Connect to the App Service you created [above](#deploy-the-dke-service-and-publish-the-key-store).</span></span>

    <span data-ttu-id="4e0f0-373">Dans votre navigateur, accédez à : **Azure portal**  >  **App Service**  >  **Centre de déploiement**de  >  **déploiement manuel**  >  **FTP**  >  **Dashboard**du centre de déploiement Azure Portal App.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-373">In your browser, go to: **Azure portal** > **App Service** > **Deployment Center** > **Manual Deployment** > **FTP** > **Dashboard**.</span></span>

2. <span data-ttu-id="4e0f0-374">Copiez les chaînes de connexion affichées dans un fichier local.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-374">Copy the connection strings displayed to a local file.</span></span> <span data-ttu-id="4e0f0-375">Vous utiliserez ces chaînes pour vous connecter au service d’application Web et télécharger des fichiers via FTP.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-375">You'll use these strings to connect to the Web App Service and upload files via FTP.</span></span>

    <span data-ttu-id="4e0f0-376">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-376">For example:</span></span>

   ![Copier des chaînes de connexion à partir du tableau de bord FTP](../media/dke-ftp-dashboard.png)

3. <span data-ttu-id="4e0f0-378">Dans la base de code pour le stockage de clés, accédez au **répertoire Customer-Key-store\src\customer-Key-Store**</span><span class="sxs-lookup"><span data-stu-id="4e0f0-378">In the codebase for the key storage, go to the **customer-key-store\src\customer-key-store directory**.</span></span>

4. <span data-ttu-id="4e0f0-379">Vérifiez que ce répertoire contient le fichier **customerkeystore. csproj** .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-379">Verify that this directory contains the **customerkeystore.csproj** file.</span></span>

5. <span data-ttu-id="4e0f0-380">Exécuter : **publication dotnet**</span><span class="sxs-lookup"><span data-stu-id="4e0f0-380">Run: **dotnet publish**</span></span>

    <span data-ttu-id="4e0f0-381">La sortie contient le répertoire dans lequel la publication a été déployée.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-381">The output contains the directory where the publish was deployed.</span></span>

    <span data-ttu-id="4e0f0-382">Par exemple : `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span><span class="sxs-lookup"><span data-stu-id="4e0f0-382">For example: `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span></span>

6. <span data-ttu-id="4e0f0-383">Envoyez tous les fichiers du répertoire de publication dans un fichier zip.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-383">Send all files in the publish directory to a zip file.</span></span> <span data-ttu-id="4e0f0-384">Lors de la création du fichier. zip, assurez-vous que tous les fichiers du répertoire sont au niveau racine du fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-384">When creating the .zip file, make sure that all files in the directory are at the root level of the .zip file.</span></span>

7. <span data-ttu-id="4e0f0-385">À partir de votre client FTP, utilisez les informations de connexion que vous avez copiées pour vous connecter à votre service d’application.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-385">From your FTP client, use the connection information you copied to connect to your App Service.</span></span> <span data-ttu-id="4e0f0-386">Téléchargez le fichier. zip que vous avez créé à l’étape précédente dans le répertoire racine de votre application Web.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-386">Upload the .zip file you created in the previous step to the root directory of your Web App.</span></span>

<span data-ttu-id="4e0f0-387">DKE est déployé et vous pouvez accéder aux clés de test que vous auriez créées.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-387">DKE is deployed and you can browse to the test keys you'd created.</span></span> <span data-ttu-id="4e0f0-388">Ensuite, [validez votre déploiement](#validate-your-deployment).</span><span class="sxs-lookup"><span data-stu-id="4e0f0-388">Next, [Validate your deployment](#validate-your-deployment).</span></span>

### <a name="validate-your-deployment"></a><span data-ttu-id="4e0f0-389">Valider votre déploiement</span><span class="sxs-lookup"><span data-stu-id="4e0f0-389">Validate your deployment</span></span>

<span data-ttu-id="4e0f0-390">Après avoir déployé DKE à l’aide de l’une des méthodes décrites ci-dessus, validez les principaux paramètres de déploiement et de magasin de clés.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-390">After deploying DKE using one of the methods described above, validate the deployment and the key store settings.</span></span>

<span data-ttu-id="4e0f0-391">Générer</span><span class="sxs-lookup"><span data-stu-id="4e0f0-391">Run:</span></span>

<span data-ttu-id="4e0f0-392">src\customer-key-store\scripts\key_store_tester.ps1 dkeserviceurl/MyKey</span><span class="sxs-lookup"><span data-stu-id="4e0f0-392">src\customer-key-store\scripts\key_store_tester.ps1 dkeserviceurl/mykey</span></span>

<span data-ttu-id="4e0f0-393">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-393">For example:</span></span>

<span data-ttu-id="4e0f0-394">key_store_tester.ps1 https://mydkeservice.com/mykey</span><span class="sxs-lookup"><span data-stu-id="4e0f0-394">key_store_tester.ps1 https://mydkeservice.com/mykey</span></span>

<span data-ttu-id="4e0f0-395">Assurez-vous qu’aucune erreur ne s’affiche dans la sortie.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-395">Ensure that no errors appear in the output.</span></span> <span data-ttu-id="4e0f0-396">Lorsque vous êtes prêt, [Enregistrez votre magasin de clés](#register-your-key-store).</span><span class="sxs-lookup"><span data-stu-id="4e0f0-396">When you're ready, [register your key store](#register-your-key-store).</span></span>

## <a name="register-your-key-store"></a><span data-ttu-id="4e0f0-397">Enregistrer votre magasin de clés</span><span class="sxs-lookup"><span data-stu-id="4e0f0-397">Register your key store</span></span>

<span data-ttu-id="4e0f0-398">Les étapes suivantes vous permettent d’enregistrer votre service DKE.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-398">The following steps enable you to register your DKE service.</span></span> <span data-ttu-id="4e0f0-399">L’inscription de votre service DKE est la dernière étape du déploiement de DKE avant de pouvoir commencer à créer des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-399">Registering your DKE service is the last step in deploying DKE before you can start creating labels.</span></span>

<span data-ttu-id="4e0f0-400">Pour enregistrer le service DKE :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-400">To register the DKE service:</span></span>

1. <span data-ttu-id="4e0f0-401">Dans votre navigateur, ouvrez le [portail Microsoft Azure](https://ms.portal.azure.com/), puis accédez à **toutes les** \> **Identity** \> **inscriptions des applications d'** identité des services.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-401">In your browser, open the [Microsoft Azure portal](https://ms.portal.azure.com/), and go to **All Services** \> **Identity** \> **App Registrations**.</span></span>

2. <span data-ttu-id="4e0f0-402">Sélectionnez **nouvelle inscription**, puis entrez un nom explicite.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-402">Select **New registration**, and enter a meaningful name.</span></span>

3. <span data-ttu-id="4e0f0-403">Sélectionnez un type de compte parmi les options affichées.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-403">Select an account type from the options displayed.</span></span>

    <span data-ttu-id="4e0f0-404">Si vous utilisez Microsoft Azure avec un domaine non personnalisé, tel que **onmicrosoft.com**, sélectionnez **comptes dans cet annuaire d’organisation uniquement (Microsoft uniquement-client unique).**</span><span class="sxs-lookup"><span data-stu-id="4e0f0-404">If you're using Microsoft Azure with a non-custom domain, such as **onmicrosoft.com**, select **Accounts in this organizational directory only (Microsoft only - Single tenant).**</span></span>

    <span data-ttu-id="4e0f0-405">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-405">For example:</span></span>

   ![Inscription de l’application](../media/dke-app-registration.png)

4. <span data-ttu-id="4e0f0-407">Au bas de la page, sélectionnez **Enregistrer** pour créer la nouvelle inscription de l’application.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-407">At the bottom of the page, select **Register** to create the new App Registration.</span></span>

5. <span data-ttu-id="4e0f0-408">Dans la nouvelle inscription de l’application, dans le volet gauche, sous **gérer**, sélectionnez **authentification**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-408">In your new App Registration, in the left pane, under **Manage**, select **Authentication**.</span></span>

6. <span data-ttu-id="4e0f0-409">Sélectionnez **Ajouter une plateforme**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-409">Select **Add a platform**.</span></span>

7. <span data-ttu-id="4e0f0-410">Dans la fenêtre contextuelle **configurer les plateformes** , sélectionnez **Web**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-410">On the **Configure platforms** popup, select **Web**.</span></span>

8. <span data-ttu-id="4e0f0-411">Sous **URI de redirection**, entrez l’URI de votre service de chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-411">Under **Redirect URIs**, enter the URI of your double key encryption service.</span></span> <span data-ttu-id="4e0f0-412">Entrez l’URL du service d’application, y compris le nom d’hôte et le domaine.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-412">Enter the App Service URL, including both the hostname and domain.</span></span>

    <span data-ttu-id="4e0f0-413">Par exemple : https://mydkeservicetest.com</span><span class="sxs-lookup"><span data-stu-id="4e0f0-413">For example: https://mydkeservicetest.com</span></span>

    - <span data-ttu-id="4e0f0-414">L’URL que vous entrez doit correspondre au nom d’hôte dans lequel votre service DKE est déployé.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-414">The URL you enter must match the hostname where your DKE service is deployed.</span></span>
    - <span data-ttu-id="4e0f0-415">Si vous testez localement avec Visual Studio, utilisez **https://localhost:5001** .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-415">If you're testing locally with Visual Studio, use **https://localhost:5001**.</span></span>
    - <span data-ttu-id="4e0f0-416">Dans tous les cas, le modèle doit être **https**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-416">In all cases, the scheme must be **https**.</span></span>

    <span data-ttu-id="4e0f0-417">Vérifiez que le nom d’hôte correspond exactement au nom d’hôte de votre service d’application.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-417">Ensure the hostname exactly matches your App Service hostname.</span></span> <span data-ttu-id="4e0f0-418">Vous pouvez l’avoir modifié sur `localhost` pour dépanner la Build.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-418">You may have changed it to `localhost` to troubleshoot the build.</span></span> <span data-ttu-id="4e0f0-419">Dans **appsettings.jsactivé**, cette valeur est le nom d’hôte que vous avez défini pour `JwtAudience` .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-419">In **appsettings.json**, this value is the hostname you set for `JwtAudience`.</span></span>

9. <span data-ttu-id="4e0f0-420">Sous **attribution implicite**, activez la case à cocher **jetons d’ID** .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-420">Under **Implicit grant**, select the **ID tokens** checkbox.</span></span>

10. <span data-ttu-id="4e0f0-421">Sélectionnez **Enregistrer** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-421">Select **Save** to save your changes.</span></span>

11. <span data-ttu-id="4e0f0-422">Dans le volet de gauche, sélectionnez **exposer une API**, puis en regard de l’ID d’application URI, sélectionnez **Set**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-422">On the left pane, select **Expose an API**, then next to Application ID URI, select **Set**.</span></span>

12. <span data-ttu-id="4e0f0-423">Toujours sur la page **exposer une API** , dans la zone **étendues définies par cette API** , sélectionnez **Ajouter une étendue**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-423">Still on the **Expose an API** page, in the **Scopes defined by this API** area, select **Add a scope**.</span></span> <span data-ttu-id="4e0f0-424">Dans la nouvelle étendue :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-424">In the new scope:</span></span>

    1. <span data-ttu-id="4e0f0-425">Définissez le nom de l’étendue en tant que **user_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-425">Define the scope name as **user_impersonation**.</span></span>

    2. <span data-ttu-id="4e0f0-426">Sélectionnez les administrateurs et les utilisateurs qui peuvent consentir.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-426">Select the administrators and users who can consent.</span></span>

    3. <span data-ttu-id="4e0f0-427">Définissez les valeurs restantes requises.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-427">Define any remaining values required.</span></span>

    4. <span data-ttu-id="4e0f0-428">Sélectionnez **Ajouter une étendue**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-428">Select **Add scope**.</span></span>

    5. <span data-ttu-id="4e0f0-429">Sélectionnez **Enregistrer** dans la partie supérieure pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-429">Select **Save** at the top to save your changes.</span></span>

13. <span data-ttu-id="4e0f0-430">Toujours sur la page **exposer une API** , dans la zone **applications clientes autorisées** , sélectionnez **Ajouter une application cliente**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-430">Still on the **Expose an API** page, in the **Authorized client applications** area, select **Add a client application**.</span></span>

    <span data-ttu-id="4e0f0-431">Dans la nouvelle application cliente :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-431">In the new client application:</span></span>

    1. <span data-ttu-id="4e0f0-432">Définissez l’ID client comme **d3590ed6-52b3-4102-Aeff-aad2292ab01c**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-432">Define the Client ID as **d3590ed6-52b3-4102-aeff-aad2292ab01c**.</span></span> <span data-ttu-id="4e0f0-433">Cette valeur est l’ID client Microsoft Office et permet à Office d’obtenir un jeton d’accès pour votre magasin de clés.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-433">This value is the Microsoft Office client ID, and enables Office to obtain an access token for your key store.</span></span>

    2. <span data-ttu-id="4e0f0-434">Sous **étendues autorisées**, sélectionnez l’étendue **user_impersonation** .</span><span class="sxs-lookup"><span data-stu-id="4e0f0-434">Under **Authorized scopes**, select the **user_impersonation** scope.</span></span>

    3. <span data-ttu-id="4e0f0-435">Sélectionnez **Ajouter une application**.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-435">Select **Add application**.</span></span>

    4. <span data-ttu-id="4e0f0-436">Sélectionnez **Enregistrer** dans la partie supérieure pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-436">Select **Save** at the top to save your changes.</span></span>

<span data-ttu-id="4e0f0-437">Votre service DKE est maintenant enregistré.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-437">Your DKE service is now registered.</span></span> <span data-ttu-id="4e0f0-438">Continuez en [créant des étiquettes à l’aide de DKE](#create-sensitivity-labels-using-dke).</span><span class="sxs-lookup"><span data-stu-id="4e0f0-438">Continue by [creating labels using DKE](#create-sensitivity-labels-using-dke).</span></span>

## <a name="create-sensitivity-labels-using-dke"></a><span data-ttu-id="4e0f0-439">Créer des étiquettes de confidentialité à l’aide de DKE</span><span class="sxs-lookup"><span data-stu-id="4e0f0-439">Create sensitivity labels using DKE</span></span>

<span data-ttu-id="4e0f0-440">Dans le centre de conformité Microsoft 365, créez une étiquette de sensibilité et appliquez le chiffrement comme vous le feriez autrement.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-440">In the Microsoft 365 compliance center, create a new sensitivity label and apply encryption as you would otherwise.</span></span> <span data-ttu-id="4e0f0-441">Sélectionnez **utiliser le chiffrement à double clé** et entrez l’URL du point de terminaison de votre clé.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-441">Select **Use Double Key Encryption** and enter the endpoint URL for your key.</span></span>

<span data-ttu-id="4e0f0-442">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-442">For example:</span></span>

![Sélectionnez utiliser le chiffrement à double clé dans le centre de conformité Microsoft 365](../media/dke-use-dke.png)

<span data-ttu-id="4e0f0-444">Toutes les étiquettes DKE que vous ajoutez commencent à apparaître pour les utilisateurs dans les versions les plus récentes des applications Microsoft 365 pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-444">Any DKE labels you add will start appearing for users in the latest versions of Microsoft 365 Apps for enterprise.</span></span>

> [!NOTE]
> <span data-ttu-id="4e0f0-445">L’actualisation des clients avec les nouvelles étiquettes peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-445">It may take up to 24 hours for the clients to refresh with the new labels.</span></span>

### <a name="enable-dke-in-your-client"></a><span data-ttu-id="4e0f0-446">Activer DKE dans votre client</span><span class="sxs-lookup"><span data-stu-id="4e0f0-446">Enable DKE in your client</span></span>

<span data-ttu-id="4e0f0-447">Si vous êtes un Office Insider, DKE est activé pour vous.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-447">If you're an Office Insider, DKE is enabled for you.</span></span> <span data-ttu-id="4e0f0-448">Dans le cas contraire, activez DKE pour votre client en ajoutant les clés de Registre suivantes :</span><span class="sxs-lookup"><span data-stu-id="4e0f0-448">Otherwise, enable DKE for your client by adding the following registry keys:</span></span>

```properties
    [HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\MSIPC\flighting]
    "DoubleKeyProtection"=dword:00000001

    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\flighting]
    "DoubleKeyProtection"=dword:00000001
```

## <a name="migrate-protected-files-from-hyok-labels-to-dke-labels"></a><span data-ttu-id="4e0f0-449">Migrer des fichiers protégés des étiquettes HYOK vers les étiquettes DKE</span><span class="sxs-lookup"><span data-stu-id="4e0f0-449">Migrate protected files from HYOK labels to DKE labels</span></span>

<span data-ttu-id="4e0f0-450">Si vous le souhaitez, une fois que vous avez terminé la configuration de DKE, vous pouvez migrer le contenu que vous avez protégé à l’aide des étiquettes HYOK vers les étiquettes DKE.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-450">If you want, once you're finished setting up DKE, you can migrate content that you've protected using HYOK labels to DKE labels.</span></span> <span data-ttu-id="4e0f0-451">Pour effectuer la migration, vous utiliserez le scanneur AIP.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-451">To migrate, you'll use the AIP scanner.</span></span> <span data-ttu-id="4e0f0-452">Pour commencer à utiliser le scanneur, voir [qu’est-ce que le scanneur d’étiquetage unifié Azure information protection ?](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner).</span><span class="sxs-lookup"><span data-stu-id="4e0f0-452">To get started using the scanner, see [What is the Azure Information Protection unified labeling scanner?](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner).</span></span>

<span data-ttu-id="4e0f0-453">Si vous ne migrez pas le contenu, votre contenu protégé HYOK restera non affecté.</span><span class="sxs-lookup"><span data-stu-id="4e0f0-453">If you don't migrate content, your HYOK protected content will remain unaffected.</span></span>

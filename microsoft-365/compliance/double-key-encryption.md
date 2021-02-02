---
title: Chiffrement à double clé (DKE)
description: DKE vous permet de protéger les données hautement sensibles tout en conservant un contrôle total de votre clé.
author: kccross
ms.author: krowley
manager: laurawi
ms.date: 01/29/2021
ms.topic: conceptual
ms.service: information-protection
audience: Admin
ms.reviewer: esaggese
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.openlocfilehash: c10a10a5922755db2c901137c3dff8acee5b8445
ms.sourcegitcommit: c550c1b5b9e67398fd95bfb0256c4f5c7930b2be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/01/2021
ms.locfileid: "50066857"
---
# <a name="double-key-encryption-for-microsoft-365"></a><span data-ttu-id="a3f3d-103">Chiffrement à double clé pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a3f3d-103">Double Key Encryption for Microsoft 365</span></span>

> <span data-ttu-id="a3f3d-104">*S’applique à : Chiffrement à double clé pour Microsoft 365, Conformité [Microsoft 365](https://www.microsoft.com/microsoft-365/business/compliance-management), [Azure Information Protection](https://azure.microsoft.com/pricing/details/information-protection)*</span><span class="sxs-lookup"><span data-stu-id="a3f3d-104">*Applies to: Double Key Encryption for Microsoft 365, [Microsoft 365 Compliance](https://www.microsoft.com/microsoft-365/business/compliance-management), [Azure Information Protection](https://azure.microsoft.com/pricing/details/information-protection)*</span></span>
>
> <span data-ttu-id="a3f3d-105">*Instructions pour : Client [d’étiquetage unifié Azure Information Protection pour Windows](https://docs.microsoft.com/azure/information-protection/faqs#whats-the-difference-between-the-azure-information-protection-classic-and-unified-labeling-clients)*</span><span class="sxs-lookup"><span data-stu-id="a3f3d-105">*Instructions for: [Azure Information Protection unified labeling client for Windows](https://docs.microsoft.com/azure/information-protection/faqs#whats-the-difference-between-the-azure-information-protection-classic-and-unified-labeling-clients)*</span></span>
>
> <span data-ttu-id="a3f3d-106">*Description du service pour : [Conformité Microsoft 365](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance)*</span><span class="sxs-lookup"><span data-stu-id="a3f3d-106">*Service description for: [Microsoft 365 Compliance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance)*</span></span>

<span data-ttu-id="a3f3d-107">Le chiffrement à double clé (DKE) utilise deux clés pour accéder au contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-107">Double Key Encryption (DKE) uses two keys together to access protected content.</span></span> <span data-ttu-id="a3f3d-108">Microsoft stocke une clé dans Microsoft Azure, et vous maintenez l’autre clé.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-108">Microsoft stores one key in Microsoft Azure, and you hold the other key.</span></span> <span data-ttu-id="a3f3d-109">Vous conservez le contrôle total de l’une de vos clés à l’aide du service de chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-109">You maintain full control of one of your keys using the Double Key Encryption service.</span></span> <span data-ttu-id="a3f3d-110">Vous appliquez la protection à votre contenu hautement sensible à l’aide du client d’étiquetage unifié Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-110">You apply protection using The Azure Information Protection unified labeling client to your highly sensitive content.</span></span>

<span data-ttu-id="a3f3d-111">Le chiffrement à double clé prend en charge les déploiements sur site et dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-111">Double Key Encryption supports both cloud and on-premises deployments.</span></span> <span data-ttu-id="a3f3d-112">Ces déploiements permettent de s’assurer que les données chiffrées restent opaques partout où vous stockez les données protégées.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-112">These deployments help to ensure that encrypted data remains opaque wherever you store the protected data.</span></span>

<span data-ttu-id="a3f3d-113">Pour plus d’informations sur les clés racines de client basées sur le cloud par défaut, voir Planification et mise en œuvre de votre clé [de client Azure Information Protection.](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-113">For more information about the default, cloud-based tenant root keys, see [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key).</span></span>

## <a name="when-your-organization-should-adopt-dke"></a><span data-ttu-id="a3f3d-114">Quand votre organisation doit adopter DKE</span><span class="sxs-lookup"><span data-stu-id="a3f3d-114">When your organization should adopt DKE</span></span>

<span data-ttu-id="a3f3d-115">Le chiffrement à double clé est destiné à vos données les plus sensibles soumises aux exigences de protection les plus strictes.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-115">Double Key Encryption is intended for your most sensitive data that is subject to the strictest protection requirements.</span></span> <span data-ttu-id="a3f3d-116">DKE n’est pas destiné à toutes les données.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-116">DKE is not intended for all data.</span></span> <span data-ttu-id="a3f3d-117">En règle générale, vous utiliserez le chiffrement à double clé pour protéger uniquement une petite partie de vos données globales.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-117">In general, you'll be using Double Key Encryption to protect only a small part of your overall data.</span></span> <span data-ttu-id="a3f3d-118">Vous devez faire preuve de diligence pour identifier les données à couvrir avec cette solution avant de déployer.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-118">You should do due diligence in identifying the right data to cover with this solution before you deploy.</span></span> <span data-ttu-id="a3f3d-119">Dans certains cas, vous devrez peut-être restreindre votre étendue et utiliser d’autres solutions pour la plupart de vos données, telles que Microsoft Information Protection avec des clés gérées par Microsoft ou BYOK.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-119">In some cases, you might need to narrow your scope and make use of other solutions for most your data such as Microsoft Information Protection with Microsoft-managed keys or BYOK.</span></span> <span data-ttu-id="a3f3d-120">Ces solutions sont suffisantes pour les documents qui ne sont pas soumis à des protections améliorées et à des exigences réglementaires.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-120">These solutions are sufficient for documents that aren't subject to enhanced protections and regulatory requirements.</span></span> <span data-ttu-id="a3f3d-121">En outre, ces solutions vous permettent d’utiliser les services Office 365 les plus puissants ; que vous ne pouvez pas utiliser avec du contenu chiffré DKE.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-121">Also, these solutions enable you to use the most powerful Office 365 services; services that you can't use with DKE encrypted content.</span></span> <span data-ttu-id="a3f3d-122">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-122">For example:</span></span>

- <span data-ttu-id="a3f3d-123">Règles de transport, y compris les logiciels anti-programme malveillant et le courrier indésirable qui nécessitent une visibilité dans la pièce jointe</span><span class="sxs-lookup"><span data-stu-id="a3f3d-123">Transport rules including anti-malware and spam that require visibility into the attachment</span></span>
- <span data-ttu-id="a3f3d-124">Microsoft Delve</span><span class="sxs-lookup"><span data-stu-id="a3f3d-124">Microsoft Delve</span></span>
- <span data-ttu-id="a3f3d-125">eDiscovery</span><span class="sxs-lookup"><span data-stu-id="a3f3d-125">eDiscovery</span></span>
- <span data-ttu-id="a3f3d-126">Recherche et indexation de contenu</span><span class="sxs-lookup"><span data-stu-id="a3f3d-126">Content search and indexing</span></span>
- <span data-ttu-id="a3f3d-127">Office Web Apps, y compris la fonctionnalité de co-auteur</span><span class="sxs-lookup"><span data-stu-id="a3f3d-127">Office Web Apps including coauthoring functionality</span></span>

<span data-ttu-id="a3f3d-128">Les applications ou services externes qui ne sont pas intégrés au DKE via le SDK MIP ne pourront pas effectuer d’actions sur les données chiffrées.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-128">Any external applications or services that are not integrated with DKE through the MIP SDK will be unable to perform actions on the encrypted data.</span></span>

<span data-ttu-id="a3f3d-129">Le SDK Microsoft Information Protection 1.7+ prend en charge le chiffrement à double clé . les applications qui s’intègrent à notre SDK pourront raisonner sur ces données avec des autorisations et des intégrations suffisantes en place.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-129">The Microsoft Information Protection SDK 1.7+ supports Double Key Encryption; applications that integrate with our SDK will be able to reason over this data with sufficient permissions and integrations in place.</span></span>

<span data-ttu-id="a3f3d-130">Nous recommandons aux organisations d’utiliser les fonctionnalités de protection des informations Microsoft (classification et étiquetage) pour protéger la plupart de leurs données sensibles et utiliser uniquement DKE pour leurs données critiques.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-130">We recommend organizations use Microsoft Information protection capabilities (classification and labeling) to protect most of their sensitive data and only use DKE for their mission-critical data.</span></span> <span data-ttu-id="a3f3d-131">Le chiffrement à double clé est pertinent pour les données sensibles dans les secteurs hautement réglementés tels que les services financiers et la santé.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-131">Double Key Encryption is relevant for sensitive data in highly regulated industries such as Financial services and Healthcare.</span></span>

<span data-ttu-id="a3f3d-132">Si vos organisations ont l’une des exigences suivantes, vous pouvez utiliser DKE pour sécuriser votre contenu :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-132">If your organizations have any of the following requirements, you can use DKE to help secure your content:</span></span>

- <span data-ttu-id="a3f3d-133">Vous souhaitez vous assurer *que seul vous* pouvez déchiffrer du contenu protégé, dans toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-133">You want to ensure that *only you* can ever decrypt protected content, under all circumstances.</span></span>
- <span data-ttu-id="a3f3d-134">Vous ne souhaitez pas que Microsoft accède lui-même aux données protégées.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-134">You don't want Microsoft to have access to protected data on its own.</span></span>
- <span data-ttu-id="a3f3d-135">Vous avez des exigences réglementaires pour contenir des clés à l’intérieur d’une limite géographique.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-135">You have regulatory requirements to hold keys within a geographical boundary.</span></span> <span data-ttu-id="a3f3d-136">Toutes les clés que vous conservez pour le chiffrement et le déchiffrement des données sont conservées dans votre centre de données.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-136">All of the keys that you hold for data encryption and decryption are maintained in your data center.</span></span>

## <a name="system-and-licensing-requirements-for-dke"></a><span data-ttu-id="a3f3d-137">Exigences relatives au système et aux licences pour le DKE</span><span class="sxs-lookup"><span data-stu-id="a3f3d-137">System and licensing requirements for DKE</span></span>

<span data-ttu-id="a3f3d-138">**Le chiffrement à double clé pour Microsoft 365** est livré avec Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-138">**Double Key Encryption for Microsoft 365** comes with Microsoft 365 E5.</span></span> <span data-ttu-id="a3f3d-139">Si vous n’avez pas de licence Microsoft 365 E5, vous pouvez vous inscrire à une [version d’essai.](https://aka.ms/M365E5ComplianceTrial)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-139">If you don’t have a Microsoft 365 E5 license, you can sign up for a [trial](https://aka.ms/M365E5ComplianceTrial).</span></span> <span data-ttu-id="a3f3d-140">Pour plus d’informations sur ces licences, consultez les conseils de licence [Microsoft 365](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance)pour la sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-140">For more information about these licenses, see [Microsoft 365 licensing guidance for security & compliance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).</span></span>

<span data-ttu-id="a3f3d-141">**Azure Information Protection**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-141">**Azure Information Protection**.</span></span> <span data-ttu-id="a3f3d-142">DKE fonctionne avec les étiquettes de sensibilité et nécessite Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-142">DKE works with sensitivity labels and requires Azure Information Protection.</span></span>

<span data-ttu-id="a3f3d-143">Les étiquettes de niveau de sensibilité DKE sont disponibles pour les utilisateurs finaux via le ruban de niveau de sensibilité dans les applications de bureau Office.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-143">DKE sensitivity labels are made available to end users through the sensitivity ribbon in Office Desktop Apps.</span></span> <span data-ttu-id="a3f3d-144">Installez ces éléments prérequis sur chaque ordinateur client où vous souhaitez protéger et utiliser des documents protégés.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-144">Install these prerequisites on each client computer where you want to protect and consume protected documents.</span></span>

<span data-ttu-id="a3f3d-145">**Microsoft Office Applications pour** entreprise version \*.12711 ou ultérieure (versions de bureau de Word, PowerPoint et Excel) sur Windows.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-145">**Microsoft Office Apps for enterprise** version \*.12711 or later (Desktop versions of Word, PowerPoint, and Excel) on Windows.</span></span>

<span data-ttu-id="a3f3d-146">**Client d’étiquetage unifié Azure Information Protection** version 2.7.93.0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-146">**Azure Information Protection Unified Labeling Client** versions 2.7.93.0 or later.</span></span> <span data-ttu-id="a3f3d-147">Téléchargez et installez le client d’étiquetage unifié à partir du [Centre de téléchargement Microsoft.](https://www.microsoft.com/download/details.aspx?id=53018)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-147">Download and install the Unified Labeling client from the [Microsoft download center](https://www.microsoft.com/download/details.aspx?id=53018).</span></span>

## <a name="supported-environments-for-storing-and-viewing-dke-protected-content"></a><span data-ttu-id="a3f3d-148">Environnements pris en charge pour le stockage et l’affichage de contenu protégé par le DKE</span><span class="sxs-lookup"><span data-stu-id="a3f3d-148">Supported environments for storing and viewing DKE-protected content</span></span>

<span data-ttu-id="a3f3d-149">**Applications pris en charge.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-149">**Supported applications**.</span></span> <span data-ttu-id="a3f3d-150">[Les applications Microsoft 365 pour les](https://www.microsoft.com/microsoft-365/business/microsoft-365-apps-for-enterprise-product) clients d’entreprise sur Windows, y compris Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-150">[Microsoft 365 Apps for enterprise](https://www.microsoft.com/microsoft-365/business/microsoft-365-apps-for-enterprise-product) clients on Windows, including Word, Excel, and PowerPoint.</span></span>

<span data-ttu-id="a3f3d-151">**Prise en charge du contenu en ligne.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-151">**Online content support**.</span></span> <span data-ttu-id="a3f3d-152">Les documents et fichiers stockés en ligne dans Microsoft SharePoint et OneDrive Entreprise sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-152">Documents and files stored online in both Microsoft SharePoint and OneDrive for Business are supported.</span></span> <span data-ttu-id="a3f3d-153">Vous pouvez partager du contenu chiffré par courrier électronique, mais vous ne pouvez pas afficher les documents et fichiers chiffrés en ligne.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-153">You can share encrypted content by email, but you can't view encrypted documents and files online.</span></span> <span data-ttu-id="a3f3d-154">Au lieu de cela, vous devez afficher le contenu protégé à l’aide des applications de bureau sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-154">Instead, you must view protected content using the desktop apps on your local computer.</span></span>

## <a name="overview-of-deploying-dke"></a><span data-ttu-id="a3f3d-155">Vue d’ensemble du déploiement DKE</span><span class="sxs-lookup"><span data-stu-id="a3f3d-155">Overview of deploying DKE</span></span>

<span data-ttu-id="a3f3d-156">Vous devez suivre ces étapes générales pour configurer DKE.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-156">You'll follow these general steps to set up DKE.</span></span> <span data-ttu-id="a3f3d-157">Une fois ces étapes effectuées, vos utilisateurs finaux peuvent protéger vos données hautement sensibles avec le chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-157">Once you've completed these steps, your end users will can protect your highly sensitive data with Double Key Encryption.</span></span>

1. <span data-ttu-id="a3f3d-158">Déployez le service DKE comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-158">Deploy the DKE service as described in this article.</span></span>

2. <span data-ttu-id="a3f3d-159">Créez une étiquette avec le chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-159">Create a label with Double Key Encryption.</span></span> <span data-ttu-id="a3f3d-160">Accédez à La Protection des informations sous le Centre de conformité [Microsoft 365](https://compliance.microsoft.com) et créez une étiquette avec le chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-160">Navigate to Information protection under the [Microsoft 365 compliance center](https://compliance.microsoft.com) and create a new label with Double Key Encryption.</span></span> <span data-ttu-id="a3f3d-161">Voir [Restreindre l’accès au contenu à l’aide d’étiquettes de sensibilité pour appliquer le chiffrement.](https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-161">See [Restrict access to content by using sensitivity labels to apply encryption](https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels).</span></span>

3. <span data-ttu-id="a3f3d-162">Utilisez des étiquettes de chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-162">Use Double Key Encryption labels.</span></span> <span data-ttu-id="a3f3d-163">Protégez les données en sélectionnant l’étiquette Chiffrement à double clé à partir du ruban Niveau de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-163">Protect data by selecting the Double Key Encrypted label from the Sensitivity ribbon in Microsoft Office.</span></span>

<span data-ttu-id="a3f3d-164">Il existe plusieurs façons d’effectuer certaines des étapes de déploiement du chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-164">There are several ways you can complete some of the steps to deploy Double Key Encryption.</span></span> <span data-ttu-id="a3f3d-165">Cet article fournit des instructions détaillées pour que les administrateurs moins expérimentés déploient correctement le service.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-165">This article provides detailed instructions so that less experienced admins successfully deploy the service.</span></span> <span data-ttu-id="a3f3d-166">Si vous êtes à l’aise avec cette méthode, vous pouvez choisir d’utiliser vos propres méthodes.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-166">If you're comfortable doing so, you can choose to use your own methods.</span></span>

## <a name="deploy-dke"></a><span data-ttu-id="a3f3d-167">Déployer DKE</span><span class="sxs-lookup"><span data-stu-id="a3f3d-167">Deploy DKE</span></span>

<span data-ttu-id="a3f3d-168">Cet article et la vidéo de déploiement utilisent Azure comme destination de déploiement pour le service DKE.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-168">This article and the deployment video use Azure as the deployment destination for the DKE service.</span></span> <span data-ttu-id="a3f3d-169">Si vous déployez vers un autre emplacement, vous devez fournir vos propres valeurs.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-169">If you're deploying to another location, you'll need to provide your own values.</span></span>

<span data-ttu-id="a3f3d-170">Regardez la [vidéo de déploiement](https://youtu.be/vDWfHN_kygg) du chiffrement à double clé pour voir une vue d’ensemble pas à pas des concepts présentés dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-170">Watch the [Double Key Encryption deployment video](https://youtu.be/vDWfHN_kygg) to see a step-by-step overview of the concepts in this article.</span></span> <span data-ttu-id="a3f3d-171">La vidéo prend environ 18 minutes.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-171">The video takes about 18 minutes to complete.</span></span>

<span data-ttu-id="a3f3d-172">Vous devez suivre ces étapes générales pour configurer le chiffrement à double clé pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-172">You'll follow these general steps to set up Double Key Encryption for your organization.</span></span>

1. [<span data-ttu-id="a3f3d-173">Installer les logiciels requis pour le service DKE</span><span class="sxs-lookup"><span data-stu-id="a3f3d-173">Install software prerequisites for the DKE service</span></span>](#install-software-prerequisites-for-the-dke-service)
1. [<span data-ttu-id="a3f3d-174">Cloner le référentiel GitHub de chiffrement à double clé</span><span class="sxs-lookup"><span data-stu-id="a3f3d-174">Clone the Double Key Encryption GitHub repository</span></span>](#clone-the-dke-github-repository)
1. [<span data-ttu-id="a3f3d-175">Modifier les paramètres de l’application</span><span class="sxs-lookup"><span data-stu-id="a3f3d-175">Modify application settings</span></span>](#modify-application-settings)
1. [<span data-ttu-id="a3f3d-176">Générer des clés de test</span><span class="sxs-lookup"><span data-stu-id="a3f3d-176">Generate test keys</span></span>](#generate-test-keys)
1. [<span data-ttu-id="a3f3d-177">Créer le projet</span><span class="sxs-lookup"><span data-stu-id="a3f3d-177">Build the project</span></span>](#build-the-project)
1. [<span data-ttu-id="a3f3d-178">Déployer le service DKE et publier le magasin de clés</span><span class="sxs-lookup"><span data-stu-id="a3f3d-178">Deploy the DKE service and publish the key store</span></span>](#deploy-the-dke-service-and-publish-the-key-store)
1. [<span data-ttu-id="a3f3d-179">Valider votre déploiement</span><span class="sxs-lookup"><span data-stu-id="a3f3d-179">Validate your deployment</span></span>](#validate-your-deployment)
1. [<span data-ttu-id="a3f3d-180">Inscrire votre magasin de clés</span><span class="sxs-lookup"><span data-stu-id="a3f3d-180">Register your key store</span></span>](#register-your-key-store)
1. [<span data-ttu-id="a3f3d-181">Créer des étiquettes de niveau de sensibilité à l’aide du DKE</span><span class="sxs-lookup"><span data-stu-id="a3f3d-181">Create sensitivity labels using DKE</span></span>](#create-sensitivity-labels-using-dke)
1. [<span data-ttu-id="a3f3d-182">Activer le DKE dans votre client</span><span class="sxs-lookup"><span data-stu-id="a3f3d-182">Enable DKE in your client</span></span>](#enable-dke-in-your-client)
1. [<span data-ttu-id="a3f3d-183">Migrer des fichiers protégés des étiquettes HYOK vers des étiquettes DKE</span><span class="sxs-lookup"><span data-stu-id="a3f3d-183">Migrate protected files from HYOK labels to DKE labels</span></span>](#migrate-protected-files-from-hyok-labels-to-dke-labels)

<span data-ttu-id="a3f3d-184">Lorsque vous avez terminé, vous pouvez chiffrer des documents et des fichiers à l’aide de la DKE.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-184">When you're done, you can encrypt documents and files using DKE.</span></span> <span data-ttu-id="a3f3d-185">Pour plus d’informations, voir [Appliquer des étiquettes de niveau de sensibilité à vos fichiers et e-mails dans Office.](https://support.microsoft.com/office/2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-185">For information, see [Apply sensitivity labels to your files and email in Office](https://support.microsoft.com/office/2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9).</span></span>

### <a name="install-software-prerequisites-for-the-dke-service"></a><span data-ttu-id="a3f3d-186">Installer les logiciels requis pour le service DKE</span><span class="sxs-lookup"><span data-stu-id="a3f3d-186">Install software prerequisites for the DKE service</span></span>

<span data-ttu-id="a3f3d-187">Installez ces éléments prérequis sur l’ordinateur sur lequel vous souhaitez installer le service DKE.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-187">Install these prerequisites on the computer where you want to install the DKE service.</span></span>

<span data-ttu-id="a3f3d-188">**SDK .NET Core 3.1**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-188">**.NET Core 3.1 SDK**.</span></span> <span data-ttu-id="a3f3d-189">Téléchargez et installez le SDK à partir [de Download .NET Core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1).</span><span class="sxs-lookup"><span data-stu-id="a3f3d-189">Download and install the SDK from [Download .NET Core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1).</span></span>

<span data-ttu-id="a3f3d-190">**Visual Studio Code**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-190">**Visual Studio Code**.</span></span> <span data-ttu-id="a3f3d-191">Téléchargez Visual Studio code à partir de [https://code.visualstudio.com/](https://code.visualstudio.com) .</span><span class="sxs-lookup"><span data-stu-id="a3f3d-191">Download Visual Studio Code from [https://code.visualstudio.com/](https://code.visualstudio.com).</span></span> <span data-ttu-id="a3f3d-192">Une fois installé, exécutez Visual Studio code et **sélectionnez** \> **Afficher les extensions.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-192">Once installed, run Visual Studio Code and select **View** \> **Extensions**.</span></span> <span data-ttu-id="a3f3d-193">Installez ces extensions.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-193">Install these extensions.</span></span>

- <span data-ttu-id="a3f3d-194">C# pour Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="a3f3d-194">C# for Visual Studio Code</span></span>

- <span data-ttu-id="a3f3d-195">NuGet Gestionnaire de package</span><span class="sxs-lookup"><span data-stu-id="a3f3d-195">NuGet Package Manager</span></span>

<span data-ttu-id="a3f3d-196">**Ressources Git**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-196">**Git resources**.</span></span> <span data-ttu-id="a3f3d-197">Téléchargez et installez l’une des applications suivantes.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-197">Download and install one of the following.</span></span>

- [<span data-ttu-id="a3f3d-198">Git</span><span class="sxs-lookup"><span data-stu-id="a3f3d-198">Git</span></span>](https://git-scm.com/downloads)

- [<span data-ttu-id="a3f3d-199">Bureau GitHub</span><span class="sxs-lookup"><span data-stu-id="a3f3d-199">GitHub Desktop</span></span>](https://desktop.github.com/)

- [<span data-ttu-id="a3f3d-200">GitHub Enterprise</span><span class="sxs-lookup"><span data-stu-id="a3f3d-200">GitHub Enterprise</span></span>](https://github.com/enterprise)

<span data-ttu-id="a3f3d-201">**OpenSSL** [OpenSSL doit être](https://slproweb.com/products/Win32OpenSSL.html) installé pour générer des clés [de test](#generate-test-keys) après avoir déployé DKE.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-201">**OpenSSL** You must have [OpenSSL](https://slproweb.com/products/Win32OpenSSL.html) installed to [generate test keys](#generate-test-keys) after you deploy DKE.</span></span> <span data-ttu-id="a3f3d-202">Assurez-vous que vous l’voquer correctement à partir du chemin d’accès de vos variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-202">Make sure you're invoking it correctly from your environment variables path.</span></span> <span data-ttu-id="a3f3d-203">Par exemple, pour plus d’informations, voir « Ajouter le répertoire d’installation à PATH [https://www.osradar.com/install-openssl-windows/](https://www.osradar.com/install-openssl-windows/) ».</span><span class="sxs-lookup"><span data-stu-id="a3f3d-203">For example, see "Add the installation directory to PATH" at [https://www.osradar.com/install-openssl-windows/](https://www.osradar.com/install-openssl-windows/) for details.</span></span>

### <a name="clone-the-dke-github-repository"></a><span data-ttu-id="a3f3d-204">Cloner le référentiel GitHub DKE</span><span class="sxs-lookup"><span data-stu-id="a3f3d-204">Clone the DKE GitHub repository</span></span>

<span data-ttu-id="a3f3d-205">Microsoft fournit les fichiers sources DKE dans un référentiel GitHub.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-205">Microsoft supplies the DKE source files in a GitHub repository.</span></span> <span data-ttu-id="a3f3d-206">Vous clonez le référentiel pour créer le projet localement pour l’utilisation de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-206">You clone the repository to build the project locally for your organization's use.</span></span> <span data-ttu-id="a3f3d-207">Le référentiel GitHub DKE se trouve à [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService) l’emplacement .</span><span class="sxs-lookup"><span data-stu-id="a3f3d-207">The DKE GitHub repository is located at [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService).</span></span>

<span data-ttu-id="a3f3d-208">Les instructions suivantes sont destinées aux utilisateurs git ou Visual Studio Code :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-208">The following instructions are intended for inexperienced git or Visual Studio Code users:</span></span>

1. <span data-ttu-id="a3f3d-209">Dans votre navigateur, allez à : [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService) .</span><span class="sxs-lookup"><span data-stu-id="a3f3d-209">In your browser, go to: [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService).</span></span>

2. <span data-ttu-id="a3f3d-210">Vers le côté droit de l’écran, sélectionnez **Code**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-210">Towards the right side of the screen, select **Code**.</span></span> <span data-ttu-id="a3f3d-211">Votre version de l’interface utilisateur peut afficher un **bouton Clone ou** télécharger.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-211">Your version of the UI might show a **Clone or download** button.</span></span> <span data-ttu-id="a3f3d-212">Ensuite, dans la liste liste qui s’affiche, sélectionnez l’icône copier pour copier l’URL dans votre Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-212">Then, in the dropdown that appears, select the copy icon to copy the URL to your clipboard.</span></span>

    <span data-ttu-id="a3f3d-213">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-213">For example:</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="a3f3d-214">![Cloner le référentiel du service de chiffrement à double clé à partir de GitHub](../media/dke-clone.png)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-214">![Clone the Double Key Encryption service repository from GitHub](../media/dke-clone.png)</span></span>

3. <span data-ttu-id="a3f3d-215">In Visual Studio Code, select **View** \> **Command Palette** and select **Git: Clone**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-215">In Visual Studio Code, select **View** \> **Command Palette** and select **Git: Clone**.</span></span> <span data-ttu-id="a3f3d-216">Pour passer à l’option dans la liste, commencez à taper pour filtrer les entrées, puis sélectionnez-la dans `git: clone` la liste.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-216">To jump to the option in the list, start typing `git: clone` to filter the entries and then select it from the drop-down.</span></span> <span data-ttu-id="a3f3d-217">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-217">For example:</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="a3f3d-218">![Visual Studio’option GIT:Clone du code](../media/dke-vscode-clone.png)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-218">![Visual Studio Code GIT:Clone option](../media/dke-vscode-clone.png)</span></span>

4. <span data-ttu-id="a3f3d-219">Dans la zone de texte, collez l’URL que vous avez copiée à partir de Git et sélectionnez **Cloner à partir de GitHub.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-219">In the text box, paste the URL that you copied from Git and select **Clone from GitHub**.</span></span>

5. <span data-ttu-id="a3f3d-220">Dans la **boîte de dialogue** Sélectionner un dossier qui s’affiche, recherchez et sélectionnez un emplacement pour stocker le référentiel.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-220">In the **Select Folder** dialog that appears, browse to and select a location to store the repository.</span></span> <span data-ttu-id="a3f3d-221">À l’invite, sélectionnez **Ouvrir.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-221">At the prompt, select **Open**.</span></span>

    <span data-ttu-id="a3f3d-222">Le référentiel s’ouvre dans Visual Studio Code et affiche la branche Git actuelle en bas à gauche.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-222">The repository opens in Visual Studio Code, and displays the current Git branch at the bottom left.</span></span> <span data-ttu-id="a3f3d-223">Par exemple, la branche doit être **principale.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-223">For example,  The branch should be **main**.</span></span> <span data-ttu-id="a3f3d-224">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-224">For example:</span></span>

   ![Capture d’écran du repo DKE dans Visual Studio code affichant la branche principale](../media/dke-vscode-main-branch.jpg)

6. <span data-ttu-id="a3f3d-226">Si vous n’êtes pas sur la branche principale, vous devez la sélectionner.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-226">If you're not on the main branch, you'll need to select it.</span></span> <span data-ttu-id="a3f3d-227">Dans Visual Studio code, sélectionnez la branche et choisissez **principal** dans la liste des branches qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-227">In Visual Studio Code, select the branch and choose **main** from the list of branches that displays.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="a3f3d-228">La sélection de la branche principale garantit que vous avez les fichiers corrects pour créer le projet.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-228">Selecting the main branch ensures that you have the correct files to build the project.</span></span> <span data-ttu-id="a3f3d-229">Si vous ne choisissez pas la branche correcte, votre déploiement échouera.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-229">If you don't choose the correct branch your deployment will fail.</span></span>

<span data-ttu-id="a3f3d-230">Votre référentiel de source DKE est maintenant installé localement.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-230">You now have your DKE source repository set up locally.</span></span> <span data-ttu-id="a3f3d-231">Ensuite, [modifiez les paramètres d’application](#modify-application-settings) de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-231">Next, [modify application settings](#modify-application-settings) for your organization.</span></span>

### <a name="modify-application-settings"></a><span data-ttu-id="a3f3d-232">Modifier les paramètres de l’application</span><span class="sxs-lookup"><span data-stu-id="a3f3d-232">Modify application settings</span></span>

<span data-ttu-id="a3f3d-233">Pour déployer le service DKE, vous devez modifier les types de paramètres d’application suivants :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-233">To deploy the DKE service, you must modify the following types of application settings:</span></span>

- [<span data-ttu-id="a3f3d-234">Paramètres d’accès aux clés</span><span class="sxs-lookup"><span data-stu-id="a3f3d-234">Key access settings</span></span>](#key-access-settings)
- [<span data-ttu-id="a3f3d-235">Paramètres de client et de clé</span><span class="sxs-lookup"><span data-stu-id="a3f3d-235">Tenant and key settings</span></span>](#tenant-and-key-settings)

<span data-ttu-id="a3f3d-236">Vous modifiez les paramètres de l’application dans appsettings.jsfichier on.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-236">You modify application settings in the appsettings.json file.</span></span> <span data-ttu-id="a3f3d-237">Ce fichier se trouve dans le dépôt DoubleKeyEncryptionService que vous avez cloné localement sous DoubleKeyEncryptionService\src\customer-key-store.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-237">This file is located in the DoubleKeyEncryptionService repo you cloned locally under DoubleKeyEncryptionService\src\customer-key-store.</span></span> <span data-ttu-id="a3f3d-238">Par exemple, dans Visual Studio Code, vous pouvez parcourir le fichier comme illustré dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-238">For example, in Visual Studio Code, you can browse to the file as shown in the following picture.</span></span>

![Localisation du fichier appsettings.jssur pour DKE.](../media/dke-appsettingsjson.png)

#### <a name="key-access-settings"></a><span data-ttu-id="a3f3d-240">Paramètres d’accès aux clés</span><span class="sxs-lookup"><span data-stu-id="a3f3d-240">Key access settings</span></span>

<span data-ttu-id="a3f3d-241">Choisissez si vous souhaitez utiliser l’autorisation de messagerie ou de rôle.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-241">Choose whether to use email or role authorization.</span></span> <span data-ttu-id="a3f3d-242">DKE prend en charge une seule de ces méthodes d’authentification à la fois.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-242">DKE supports only one of these authentication methods at a time.</span></span>

- <span data-ttu-id="a3f3d-243">**Autorisation de messagerie** électronique .</span><span class="sxs-lookup"><span data-stu-id="a3f3d-243">**Email authorization**.</span></span> <span data-ttu-id="a3f3d-244">Permet à votre organisation d’autoriser l’accès aux clés en fonction des adresses de messagerie uniquement.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-244">Allows your organization to authorize access to keys based on email addresses only.</span></span>

- <span data-ttu-id="a3f3d-245">**Autorisation de rôle**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-245">**Role authorization**.</span></span> <span data-ttu-id="a3f3d-246">Permet à votre organisation d’autoriser l’accès aux clés basées sur des groupes Active Directory et nécessite que le service web puisse interroger LDAP.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-246">Allows your organization to authorize access to keys based on Active Directory groups, and requires that the web service can query LDAP.</span></span>

<span data-ttu-id="a3f3d-247">**Pour définir des paramètres d’accès clés pour DKE à l’aide de l’autorisation de messagerie**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-247">**To set key access settings for DKE using email authorization**</span></span>

1. <span data-ttu-id="a3f3d-248">Ouvrez le **appsettings.jssur le** fichier et recherchez le `AuthorizedEmailAddress` paramètre.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-248">Open the **appsettings.json** file and locate the `AuthorizedEmailAddress` setting.</span></span>

2. <span data-ttu-id="a3f3d-249">Ajoutez l’adresse de messagerie ou les adresses que vous souhaitez autoriser.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-249">Add the email address or addresses that you want to authorize.</span></span> <span data-ttu-id="a3f3d-250">Séparez les adresses de messagerie par des guillemets et des virgules.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-250">Separate multiple email addresses with double quotes and commas.</span></span> <span data-ttu-id="a3f3d-251">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-251">For example:</span></span>

   ```json
   "AuthorizedEmailAddress": ["email1@company.com", "email2@company.com ", "email3@company.com"]
   ```

3. <span data-ttu-id="a3f3d-252">Recherchez `LDAPPath` le paramètre et supprimez le texte entre `If you use role authorization (AuthorizedRoles) then this is the LDAP path.` guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-252">Locate the `LDAPPath` setting and remove the text `If you use role authorization (AuthorizedRoles) then this is the LDAP path.` between the double quotes.</span></span> <span data-ttu-id="a3f3d-253">Laissez les guillemets doubles en place.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-253">Leave the double quotes in place.</span></span> <span data-ttu-id="a3f3d-254">Lorsque vous avez terminé, le paramètre doit ressembler à ceci.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-254">When you're finished, the setting should look like this.</span></span>

   ```json
   "LDAPPath": ""
   ```

4. <span data-ttu-id="a3f3d-255">Recherchez `AuthorizedRoles` le paramètre et supprimez la ligne entière.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-255">Locate the `AuthorizedRoles` setting and delete the entire line.</span></span>

<span data-ttu-id="a3f3d-256">Cette image montre **l'appsettings.jssur le** fichier correctement formaté pour l’autorisation de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-256">This image shows the **appsettings.json** file correctly formatted for email authorization.</span></span>

   ![L'appsettings.jssur le fichier montrant la méthode d’autorisation de messagerie](../media/dke-email-accesssetting.png)

<span data-ttu-id="a3f3d-258">**Pour définir des paramètres d’accès clés pour DKE à l’aide de l’autorisation de rôle**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-258">**To set key access settings for DKE using role authorization**</span></span>

1. <span data-ttu-id="a3f3d-259">Ouvrez le **appsettings.jssur le** fichier et recherchez le `AuthorizedRoles` paramètre.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-259">Open the **appsettings.json** file and locate the `AuthorizedRoles` setting.</span></span>

2. <span data-ttu-id="a3f3d-260">Ajoutez les noms de groupe Active Directory que vous souhaitez autoriser.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-260">Add the Active Directory group names you want to authorize.</span></span> <span data-ttu-id="a3f3d-261">Séparez les noms de groupes par des guillemets et des virgules.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-261">Separate multiple group names with double quotes and commas.</span></span> <span data-ttu-id="a3f3d-262">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-262">For example:</span></span>

   ```json
   "AuthorizedRoles": ["group1", "group2", "group3"]
   ```

3. <span data-ttu-id="a3f3d-263">Recherchez `LDAPPath` le paramètre et ajoutez le domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-263">Locate the `LDAPPath` setting and add the Active Directory domain.</span></span> <span data-ttu-id="a3f3d-264">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-264">For example:</span></span>

   ```json
   "LDAPPath": "contoso.com"
   ```

4. <span data-ttu-id="a3f3d-265">Recherchez `AuthorizedEmailAddress` le paramètre et supprimez la ligne entière.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-265">Locate the `AuthorizedEmailAddress` setting and delete the entire line.</span></span>

<span data-ttu-id="a3f3d-266">Cette image montre **l'appsettings.jssur le** fichier correctement formaté pour l’autorisation de rôle.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-266">This image shows the **appsettings.json** file correctly formatted for role authorization.</span></span>

   ![appsettings.jsfichier affichant la méthode d’autorisation de rôle](../media/dke-role-accesssetting.png)

#### <a name="tenant-and-key-settings"></a><span data-ttu-id="a3f3d-268">Paramètres de client et de clé</span><span class="sxs-lookup"><span data-stu-id="a3f3d-268">Tenant and key settings</span></span>

<span data-ttu-id="a3f3d-269">Les paramètres de clé et de client DKE se trouvent dans le **appsettings.jsfichier.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-269">DKE tenant and key settings are located in the **appsettings.json** file.</span></span>

<span data-ttu-id="a3f3d-270">**Pour configurer les paramètres de client et de clé pour DKE**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-270">**To configure tenant and key settings for DKE**</span></span>

1. <span data-ttu-id="a3f3d-271">Ouvrez le **appsettings.jsfichier** on.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-271">Open the **appsettings.json** file.</span></span>

2. <span data-ttu-id="a3f3d-272">Recherchez `ValidIssuers` le paramètre et `<tenantid>` remplacez-le par votre ID de client.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-272">Locate the `ValidIssuers` setting and replace `<tenantid>` with your tenant ID.</span></span> <span data-ttu-id="a3f3d-273">Vous pouvez localiser votre ID de client en allant sur le portail Azure et en visualisant les [propriétés du client.](https://aad.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-273">You can locate your tenant ID by going to the Azure portal and viewing the [tenant properties](https://aad.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span></span> <span data-ttu-id="a3f3d-274">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-274">For example:</span></span>

   ```json
   "ValidIssuers": [
     "https://sts.windows.net/9c99431e-b513-44be-a7d9-e7b500002d4b/"
   ]
   ```

<span data-ttu-id="a3f3d-275">Recherchez `JwtAudience` le .</span><span class="sxs-lookup"><span data-stu-id="a3f3d-275">Locate the `JwtAudience`.</span></span> <span data-ttu-id="a3f3d-276">Remplacez `<yourhostname>` par le nom d’hôte de l’ordinateur sur lequel le service DKE s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-276">Replace `<yourhostname>` with the hostname of the machine where the DKE service will run.</span></span> <span data-ttu-id="a3f3d-277">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-277">For example:</span></span>

  > [!IMPORTANT]
  > <span data-ttu-id="a3f3d-278">La valeur doit `JwtAudience` correspondre exactement au nom de votre *hôte.*</span><span class="sxs-lookup"><span data-stu-id="a3f3d-278">The value for `JwtAudience` must match the name of your host *exactly*.</span></span> <span data-ttu-id="a3f3d-279">Vous pouvez utiliser **localhost:5001 lors** du débogage.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-279">You may use **localhost:5001** while debugging.</span></span> <span data-ttu-id="a3f3d-280">Toutefois, lorsque vous avez terminé le débogage, veillez à mettre à jour cette valeur sur le nom d’hôte du serveur.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-280">However, When you're done debugging, make sure to update this value to the server's hostname.</span></span>

- <span data-ttu-id="a3f3d-281">`TestKeys:Name`.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-281">`TestKeys:Name`.</span></span> <span data-ttu-id="a3f3d-282">Entrez un nom pour votre clé.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-282">Enter a name for your key.</span></span> <span data-ttu-id="a3f3d-283">Par exemple : `TestKey1`</span><span class="sxs-lookup"><span data-stu-id="a3f3d-283">For example: `TestKey1`</span></span>
- <span data-ttu-id="a3f3d-284">`TestKeys:Id`.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-284">`TestKeys:Id`.</span></span> <span data-ttu-id="a3f3d-285">Créez un GUID et entrez-le comme `TestKeys:ID` valeur.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-285">Create a GUID and enter it as the `TestKeys:ID` value.</span></span> <span data-ttu-id="a3f3d-286">Par exemple, `DCE1CC21-FF9B-4424-8FF4-9914BD19A1BE`.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-286">For example, `DCE1CC21-FF9B-4424-8FF4-9914BD19A1BE`.</span></span> <span data-ttu-id="a3f3d-287">Vous pouvez utiliser un site tel que [le Générateur de GUID en](https://guidgenerator.com/) ligne pour générer un GUID de manière aléatoire.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-287">You can use a site like [Online GUID Generator](https://guidgenerator.com/) to randomly generate a GUID.</span></span>

<span data-ttu-id="a3f3d-288">Cette image montre le format correct pour les paramètres de client et de clés **dansappsettings.jssur**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-288">This image shows the correct format for tenant and keys settings in **appsettings.json**.</span></span> <span data-ttu-id="a3f3d-289">`LDAPPath` est configuré pour l’autorisation de rôle.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-289">`LDAPPath` is configured for role authorization.</span></span>

![Affiche les paramètres de client et de clé corrects pour DKE dans le fichier appsettings.jssur.](../media/dke-appsettingsjson-tenantkeysettings.png)

### <a name="generate-test-keys"></a><span data-ttu-id="a3f3d-291">Générer des clés de test</span><span class="sxs-lookup"><span data-stu-id="a3f3d-291">Generate test keys</span></span>

<span data-ttu-id="a3f3d-292">Une fois que vous avez défini vos paramètres d’application, vous êtes prêt à générer des clés de test publiques et privées.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-292">Once you have your application settings defined, you're ready to generate public and private test keys.</span></span>

<span data-ttu-id="a3f3d-293">Pour générer des clés :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-293">To generate keys:</span></span>

1. <span data-ttu-id="a3f3d-294">Dans le menu Démarrer de Windows, exécutez l’invite de commandes OpenSSL.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-294">From the Windows Start menu, run the OpenSSL Command Prompt.</span></span>

2. <span data-ttu-id="a3f3d-295">Modifiez le dossier dans lequel vous souhaitez enregistrer les clés de test.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-295">Change to the folder where you want to save the test keys.</span></span> <span data-ttu-id="a3f3d-296">Les fichiers que vous créez en effectuant les étapes de cette tâche sont stockés dans le même dossier.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-296">The files you create by completing the steps in this task are stored in the same folder.</span></span>

3. <span data-ttu-id="a3f3d-297">Générez la nouvelle clé de test.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-297">Generate the new test key.</span></span>

   ```console
   openssl req -x509 -newkey rsa:2048 -keyout key.pem -out cert.pem -days 365
   ```

4. <span data-ttu-id="a3f3d-298">Générer la clé privée.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-298">Generate the private key.</span></span>

   ```console
   openssl rsa -in key.pem -out privkeynopass.pem
   ```

5. <span data-ttu-id="a3f3d-299">Générer la clé publique.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-299">Generate the public key.</span></span>

   ```console
   openssl rsa -in key.pem -pubout > pubkeyonly.pem
   ```

6. <span data-ttu-id="a3f3d-300">Dans un éditeur de texte, ouvrez **pubkeyonly.pem**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-300">In a text editor, open **pubkeyonly.pem**.</span></span> <span data-ttu-id="a3f3d-301">Copiez tout le contenu du fichier **pubkeyonly.pem,** à l’exception des première et dernière lignes, dans la section du fichier `PublicPem` **appsettings.jssur.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-301">Copy all of the content in the **pubkeyonly.pem** file, except the first and last lines, into the `PublicPem` section of the **appsettings.json** file.</span></span>

7. <span data-ttu-id="a3f3d-302">Dans un éditeur de texte, ouvrez **privkeynopass.pem**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-302">In a text editor, open **privkeynopass.pem**.</span></span> <span data-ttu-id="a3f3d-303">Copiez tout le contenu du fichier **privkeynopass.pem,** à l’exception des première et dernière lignes, dans la section du fichier `PrivatePem` **appsettings.jssur.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-303">Copy all of the content in the **privkeynopass.pem** file, except the first and last lines, into the `PrivatePem` section of the **appsettings.json** file.</span></span>

8. <span data-ttu-id="a3f3d-304">Supprimez tous les espaces vides et les nouvelles lignes dans les `PublicPem` `PrivatePem` sections et les espaces.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-304">Remove all blank spaces and newlines in both the `PublicPem` and `PrivatePem` sections.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="a3f3d-305">Lorsque vous copiez ce contenu, ne supprimez aucune donnée PEM.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-305">When you copy this content, do not delete any of the PEM data.</span></span>

9. <span data-ttu-id="a3f3d-306">Dans Visual Studio code, accédez au **Startup.cs** fichier.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-306">In Visual Studio Code, browse to the **Startup.cs** file.</span></span> <span data-ttu-id="a3f3d-307">Ce fichier se trouve dans le dépôt DoubleKeyEncryptionService que vous avez cloné localement sous DoubleKeyEncryptionService\src\customer-key-store\.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-307">This file is located in the DoubleKeyEncryptionService repo you cloned locally under DoubleKeyEncryptionService\src\customer-key-store\.</span></span>

10. <span data-ttu-id="a3f3d-308">Recherchez les lignes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-308">Locate the following lines:</span></span>

    ```csharp
        #if USE_TEST_KEYS
        #error !!!!!!!!!!!!!!!!!!!!!! Use of test keys is only supported for testing,
        DO NOT USE FOR PRODUCTION !!!!!!!!!!!!!!!!!!!!!!!!!!!!!
        services.AddSingleton<ippw.IKeyStore, ippw.TestKeyStore>();
        #endif
    ```

11. <span data-ttu-id="a3f3d-309">Remplacez ces lignes par le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-309">Replace these lines with the following text:</span></span>

    ```csharp
    services.AddSingleton<ippw.IKeyStore, ippw.TestKeyStore>();
    ```

    <span data-ttu-id="a3f3d-310">Les résultats finaux doivent ressembler à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-310">The end results should look similar to the following.</span></span>

    ![startup.cs pour la prévisualisation publique](../media/dke-startupcs-usetestkeys.png)

<span data-ttu-id="a3f3d-312">Vous êtes maintenant prêt à [créer votre projet DKE.](#build-the-project)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-312">Now you're ready to [build your DKE project](#build-the-project).</span></span>

### <a name="build-the-project"></a><span data-ttu-id="a3f3d-313">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-313">Build the project</span></span>

<span data-ttu-id="a3f3d-314">Utilisez les instructions suivantes pour créer le projet DKE localement :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-314">Use the following instructions to build the DKE project locally:</span></span>

1. <span data-ttu-id="a3f3d-315">Dans Visual Studio Code, dans le référentiel du service DKE, sélectionnez **Afficher** la palette de commandes, puis \>  tapez **build** à l’invite.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-315">In Visual Studio Code, in the DKE service repository, select **View** \> **Command Palette** and then type **build** at the prompt.</span></span>

2. <span data-ttu-id="a3f3d-316">Dans la liste, choisissez **Tâches : Exécuter la tâche de build.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-316">From the list, choose **Tasks: Run build task**.</span></span>

   <span data-ttu-id="a3f3d-317">Si aucune tâche de build n’est trouvée, sélectionnez **Configurer** la tâche de création et créez-en une pour .NET Core comme suit.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-317">If there are no build tasks found, select **Configure Build Task** and create one for .NET core as follows.</span></span>

   ![Configurer la tâche de build manquante pour .NET](../media/dke-configurebuildtask.png)

   1. <span data-ttu-id="a3f3d-319">Choose **Create tasks.json from template**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-319">Choose **Create tasks.json from template**.</span></span>

      ![Créer tasks.jsfichier à partir d’un modèle pour DKE](../media/dke-createtasksjsonfromtemplate.png)

   2. <span data-ttu-id="a3f3d-321">Dans la liste des types de modèles, **sélectionnez .NET Core**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-321">From the list of template types, select **.NET Core**.</span></span>

      ![Sélectionner le modèle correct pour DKE](../media/dke-tasksjsontemplate.png)

   3. <span data-ttu-id="a3f3d-323">Dans la section build, recherchez le chemin d’accès au **fichier customerkeystore.csproj.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-323">In the build section, locate the path to the **customerkeystore.csproj** file.</span></span> <span data-ttu-id="a3f3d-324">Si ce n’est pas le cas, ajoutez la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-324">If it's not there, add the following line:</span></span>

      ```json
      "${workspaceFolder}/src/customer-key-store/customerkeystore.csproj",
      ```

   4. <span data-ttu-id="a3f3d-325">Exécutez à nouveau la build.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-325">Run the build again.</span></span>

3. <span data-ttu-id="a3f3d-326">Vérifiez qu’il n’y a aucune erreur rouge dans la fenêtre de sortie.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-326">Verify that there are no red errors in the output window.</span></span>

   <span data-ttu-id="a3f3d-327">En cas d’erreur rouge, vérifiez la sortie de la console.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-327">If there are red errors, check the console output.</span></span> <span data-ttu-id="a3f3d-328">Assurez-vous que toutes les étapes précédentes ont été correctement effectuées et que les versions de build correctes sont présentes.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-328">Ensure that you completed all the previous steps correctly and the correct build versions are present.</span></span>

4. <span data-ttu-id="a3f3d-329">Sélectionnez  \> **Exécuter le débogage démarrer** pour déboguer le processus.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-329">Select **Run** \> **Start Debugging** to debug the process.</span></span> <span data-ttu-id="a3f3d-330">Si vous êtes invité à sélectionner un environnement, sélectionnez **.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-330">If you're prompted to select an environment, select **.NET core**.</span></span>

   <span data-ttu-id="a3f3d-331">Le débogger principal .NET est généralement lancé sur `https://localhost:5001` .</span><span class="sxs-lookup"><span data-stu-id="a3f3d-331">The .NET core debugger typically launches to `https://localhost:5001`.</span></span> <span data-ttu-id="a3f3d-332">Pour afficher votre clé de test, consultez et affichez une barre oblique (/) et le nom `https://localhost:5001` de votre clé.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-332">To view your test key, go to `https://localhost:5001` and append a forward slash (/) and the name of your key.</span></span> <span data-ttu-id="a3f3d-333">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-333">For example:</span></span>

   ```https
   https://localhost:5001/TestKey1
   ```

   <span data-ttu-id="a3f3d-334">La clé doit s’afficher au format JSON.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-334">The key should display in JSON format.</span></span>

<span data-ttu-id="a3f3d-335">Votre configuration est maintenant terminée.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-335">Your setup is now complete.</span></span> <span data-ttu-id="a3f3d-336">Avant de publier le keystore, dans appsettings.js, pour le paramètre JwtAudience, assurez-vous que la valeur du nom d’hôte correspond exactement au nom d’hôte de votre service d’application.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-336">Before you publish the keystore, in appsettings.json, for the JwtAudience setting, ensure the value for hostname exactly matches your App Service host name.</span></span> <span data-ttu-id="a3f3d-337">Vous l’avez peut-être changé en localhost pour résoudre les problèmes de build.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-337">You may have changed it to localhost to troubleshoot the build.</span></span>

### <a name="deploy-the-dke-service-and-publish-the-key-store"></a><span data-ttu-id="a3f3d-338">Déployer le service DKE et publier le magasin de clés</span><span class="sxs-lookup"><span data-stu-id="a3f3d-338">Deploy the DKE service and publish the key store</span></span>

<span data-ttu-id="a3f3d-339">Pour les déploiements de production, déployez le service dans un cloud tiers ou publiez-le sur [un système local.](https://docs.microsoft.com/aspnet/core/tutorials/publish-to-iis?view=aspnetcore-3.1&preserve-view=true&tabs=netcore-cli)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-339">For production deployments, deploy the service either in a third-party cloud or [publish to an on-premises system](https://docs.microsoft.com/aspnet/core/tutorials/publish-to-iis?view=aspnetcore-3.1&preserve-view=true&tabs=netcore-cli).</span></span>

<span data-ttu-id="a3f3d-340">Vous pouvez préférer d’autres méthodes pour déployer vos clés.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-340">You may prefer other methods to deploy your keys.</span></span> <span data-ttu-id="a3f3d-341">Sélectionnez la méthode qui fonctionne le mieux pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-341">Select the method that works best for your organization.</span></span>

<span data-ttu-id="a3f3d-342">Pour les déploiements pilotes, vous pouvez déployer dans Azure et commencer immédiatement.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-342">For pilot deployments, you can deploy in Azure and get started right away.</span></span>

<span data-ttu-id="a3f3d-343">**Pour créer une instance Azure Web App pour héberger votre déploiement DKE**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-343">**To create an Azure Web App instance to host your DKE deployment**</span></span>

<span data-ttu-id="a3f3d-344">Pour publier le magasin de clés, vous allez créer une instance Azure App Service pour héberger votre déploiement DKE.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-344">To publish the key store, you'll create an Azure App Service instance to host your DKE deployment.</span></span> <span data-ttu-id="a3f3d-345">Ensuite, vous allez publier vos clés générées dans Azure.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-345">Next, you'll publish your generated keys to Azure.</span></span>

1. <span data-ttu-id="a3f3d-346">Dans votre navigateur, connectez-vous au portail [Microsoft Azure](https://ms.portal.azure.com)et allez sur Ajouter des **services d’application.**  >  </span><span class="sxs-lookup"><span data-stu-id="a3f3d-346">In your browser, sign in to the [Microsoft Azure portal](https://ms.portal.azure.com), and go to **App Services** > **Add**.</span></span>

2. <span data-ttu-id="a3f3d-347">Sélectionnez votre abonnement et votre groupe de ressources et définissez les détails de votre instance.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-347">Select your subscription and resource group and define your instance details.</span></span>

   - <span data-ttu-id="a3f3d-348">Entrez le nom d’hôte de l’ordinateur sur lequel vous souhaitez installer le service DKE.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-348">Enter the hostname of the computer where you want to install the DKE service.</span></span> <span data-ttu-id="a3f3d-349">Assurez-vous qu’il s’agit du même nom que celui défini pour le paramètre JwtAudience dans le [**fichierappsettings.jssur.**](#tenant-and-key-settings)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-349">Make sure it's the same name as the one defined for the JwtAudience setting in the [**appsettings.json**](#tenant-and-key-settings) file.</span></span> <span data-ttu-id="a3f3d-350">La valeur que vous fournissez pour le nom est également WebAppInstanceName.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-350">The value you provide for the name is also the WebAppInstanceName.</span></span>

   - <span data-ttu-id="a3f3d-351">Pour **publier**, sélectionner **du code** et pour la pile **Runtime**, **sélectionnez .NET Core 3.1**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-351">For **Publish**, select **code**, and for **Runtime stack**, select **.NET Core 3.1**.</span></span>

   <span data-ttu-id="a3f3d-352">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-352">For example:</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="a3f3d-353">![Ajouter votre service d’application](../media/dke-azure-add-app-service.png)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-353">![Add your App Service](../media/dke-azure-add-app-service.png)</span></span>

3. <span data-ttu-id="a3f3d-354">Au bas de la page, sélectionnez **Révision + créer,** puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-354">At the bottom of the page, select **Review + create**, and then select **Add**.</span></span>

4. <span data-ttu-id="a3f3d-355">Pour publier vos clés générées, faites l’une des choses suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-355">Do one of the following to publish your generated keys:</span></span>

   - [<span data-ttu-id="a3f3d-356">Publier via ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="a3f3d-356">Publish via ZipDeployUI</span></span>](#publish-via-zipdeployui)
   - [<span data-ttu-id="a3f3d-357">Publier via FTP</span><span class="sxs-lookup"><span data-stu-id="a3f3d-357">Publish via FTP</span></span>](#publish-via-ftp)
   - [<span data-ttu-id="a3f3d-358">Publier via Visual Studio 2019 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="a3f3d-358">Publish via Visual Studio 2019 or later</span></span>](https://docs.microsoft.com/aspnet/core/tutorials/)

#### <a name="publish-via-zipdeployui"></a><span data-ttu-id="a3f3d-359">Publier via ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="a3f3d-359">Publish via ZipDeployUI</span></span>

1. <span data-ttu-id="a3f3d-360">Accédez à `https://<WebAppInstanceName>.scm.azurewebsites.net/ZipDeployUI`.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-360">Go to `https://<WebAppInstanceName>.scm.azurewebsites.net/ZipDeployUI`.</span></span>

   <span data-ttu-id="a3f3d-361">Par exemple : https://dkeservice.scm.azurewebsites.net/ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="a3f3d-361">For example: https://dkeservice.scm.azurewebsites.net/ZipDeployUI</span></span>

2. <span data-ttu-id="a3f3d-362">Dans le codebase du magasin de clés, allez dans le dossier **customer-key-store\src\customer-key-store** et vérifiez que ce dossier contient le fichier **customerkeystore.csproj.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-362">In the codebase for the key store, go to the **customer-key-store\src\customer-key-store** folder, and verify that this folder contains the **customerkeystore.csproj** file.</span></span>

3. <span data-ttu-id="a3f3d-363">Run: **dotnet publish**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-363">Run: **dotnet publish**</span></span>

   <span data-ttu-id="a3f3d-364">La fenêtre de sortie affiche le répertoire dans lequel la publication a été déployée.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-364">The output window displays the directory where the publish was deployed.</span></span>

   <span data-ttu-id="a3f3d-365">Par exemple : `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span><span class="sxs-lookup"><span data-stu-id="a3f3d-365">For example: `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span></span>

4. <span data-ttu-id="a3f3d-366">Envoyez tous les fichiers du répertoire de publication vers un fichier .zip.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-366">Send all files in the publish directory to a .zip file.</span></span> <span data-ttu-id="a3f3d-367">Lors de la création du fichier .zip, assurez-vous que tous les fichiers du répertoire sont au niveau racine du fichier .zip.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-367">When creating the .zip file, make sure that all files in the directory are at the root level of the .zip file.</span></span>

5. <span data-ttu-id="a3f3d-368">Faites glisser et déposez le fichier .zip que vous créez sur le site ZipDeployUI que vous avez ouvert ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-368">Drag and drop the .zip file you create to the ZipDeployUI site you opened above.</span></span> <span data-ttu-id="a3f3d-369">Par exemple : https://dkeservice.scm.azurewebsites.net/ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="a3f3d-369">For example: https://dkeservice.scm.azurewebsites.net/ZipDeployUI</span></span>

<span data-ttu-id="a3f3d-370">DKE est déployé et vous pouvez parcourir les clés de test que vous avez créées.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-370">DKE is deployed and you can browse to the test keys you've created.</span></span> <span data-ttu-id="a3f3d-371">Continuez à [valider votre déploiement ci-dessous.](#validate-your-deployment)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-371">Continue to [Validate your deployment](#validate-your-deployment) below.</span></span>

#### <a name="publish-via-ftp"></a><span data-ttu-id="a3f3d-372">Publier via FTP</span><span class="sxs-lookup"><span data-stu-id="a3f3d-372">Publish via FTP</span></span>

1. <span data-ttu-id="a3f3d-373">Connectez-vous au service d’application que vous avez créé [ci-dessus.](#deploy-the-dke-service-and-publish-the-key-store)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-373">Connect to the App Service you created [above](#deploy-the-dke-service-and-publish-the-key-store).</span></span>

   <span data-ttu-id="a3f3d-374">Dans votre navigateur, go to: **Azure portal**  >  **App Service** Deployment  >  **Center**  >  **Manual Deployment**  >  **FTP**  >  **Dashboard**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-374">In your browser, go to: **Azure portal** > **App Service** > **Deployment Center** > **Manual Deployment** > **FTP** > **Dashboard**.</span></span>

2. <span data-ttu-id="a3f3d-375">Copiez les chaînes de connexion affichées dans un fichier local.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-375">Copy the connection strings displayed to a local file.</span></span> <span data-ttu-id="a3f3d-376">Vous utiliserez ces chaînes pour vous connecter au service Web App Et charger des fichiers via FTP.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-376">You'll use these strings to connect to the Web App Service and upload files via FTP.</span></span>

   <span data-ttu-id="a3f3d-377">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-377">For example:</span></span>

   ![Copier des chaînes de connexion à partir du tableau de bord FTP](../media/dke-ftp-dashboard.png)

3. <span data-ttu-id="a3f3d-379">Dans le codebase du stockage de clés, allez dans le répertoire **customer-key-store\src\customer-key-store.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-379">In the codebase for the key storage, go to the **customer-key-store\src\customer-key-store directory**.</span></span>

4. <span data-ttu-id="a3f3d-380">Vérifiez que ce répertoire contient le **fichier customerkeystore.csproj.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-380">Verify that this directory contains the **customerkeystore.csproj** file.</span></span>

5. <span data-ttu-id="a3f3d-381">Run: **dotnet publish**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-381">Run: **dotnet publish**</span></span>

   <span data-ttu-id="a3f3d-382">La sortie contient le répertoire dans lequel la publication a été déployée.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-382">The output contains the directory where the publish was deployed.</span></span>

   <span data-ttu-id="a3f3d-383">Par exemple : `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span><span class="sxs-lookup"><span data-stu-id="a3f3d-383">For example: `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span></span>

6. <span data-ttu-id="a3f3d-384">Envoyez tous les fichiers du répertoire de publication vers un fichier zip.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-384">Send all files in the publish directory to a zip file.</span></span> <span data-ttu-id="a3f3d-385">Lors de la création du fichier .zip, assurez-vous que tous les fichiers du répertoire sont au niveau racine du fichier .zip.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-385">When creating the .zip file, make sure that all files in the directory are at the root level of the .zip file.</span></span>

7. <span data-ttu-id="a3f3d-386">À partir de votre client FTP, utilisez les informations de connexion que vous avez copiées pour vous connecter à votre service d’application.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-386">From your FTP client, use the connection information you copied to connect to your App Service.</span></span> <span data-ttu-id="a3f3d-387">Téléchargez le fichier .zip que vous avez créé à l’étape précédente dans le répertoire racine de votre application Web.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-387">Upload the .zip file you created in the previous step to the root directory of your Web App.</span></span>

<span data-ttu-id="a3f3d-388">DKE est déployé et vous pouvez naviguer jusqu’aux clés de test que vous avez créées.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-388">DKE is deployed and you can browse to the test keys you'd created.</span></span> <span data-ttu-id="a3f3d-389">Ensuite, [validez votre déploiement.](#validate-your-deployment)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-389">Next, [Validate your deployment](#validate-your-deployment).</span></span>

### <a name="validate-your-deployment"></a><span data-ttu-id="a3f3d-390">Valider votre déploiement</span><span class="sxs-lookup"><span data-stu-id="a3f3d-390">Validate your deployment</span></span>

<span data-ttu-id="a3f3d-391">Après avoir déployé DKE à l’aide de l’une des méthodes décrites ci-dessus, validez le déploiement et les paramètres du magasin de clés.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-391">After deploying DKE using one of the methods described above, validate the deployment and the key store settings.</span></span>

<span data-ttu-id="a3f3d-392">Exécutez :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-392">Run:</span></span>

```powershell
src\customer-key-store\scripts\key_store_tester.ps1 dkeserviceurl/mykey
```

<span data-ttu-id="a3f3d-393">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-393">For example:</span></span>

```powershell
key_store_tester.ps1 https://mydkeservice.com/mykey
```

<span data-ttu-id="a3f3d-394">Assurez-vous qu’aucune erreur n’apparaît dans la sortie.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-394">Ensure that no errors appear in the output.</span></span> <span data-ttu-id="a3f3d-395">Lorsque vous êtes prêt, inscrivez [votre magasin de clés.](#register-your-key-store)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-395">When you're ready, [register your key store](#register-your-key-store).</span></span>

<span data-ttu-id="a3f3d-396">Le nom de la clé est sensible à la cas.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-396">The key name is case sensitive.</span></span> <span data-ttu-id="a3f3d-397">Entrez le nom de la clé tel qu’il apparaît dans appsettings.jsfichier.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-397">Enter the key name as it appears in the appsettings.json file.</span></span>

## <a name="register-your-key-store"></a><span data-ttu-id="a3f3d-398">Inscrire votre magasin de clés</span><span class="sxs-lookup"><span data-stu-id="a3f3d-398">Register your key store</span></span>

<span data-ttu-id="a3f3d-399">Les étapes suivantes vous permettent d’inscrire votre service DKE.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-399">The following steps enable you to register your DKE service.</span></span> <span data-ttu-id="a3f3d-400">L’inscription de votre service DKE est la dernière étape du déploiement du DKE avant de commencer à créer des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-400">Registering your DKE service is the last step in deploying DKE before you can start creating labels.</span></span>

<span data-ttu-id="a3f3d-401">Pour inscrire le service DKE :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-401">To register the DKE service:</span></span>

1. <span data-ttu-id="a3f3d-402">Dans votre navigateur, ouvrez [le portail Microsoft Azure](https://ms.portal.azure.com/)et go to All **Services** \> **Identity** \> **App Registrations**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-402">In your browser, open the [Microsoft Azure portal](https://ms.portal.azure.com/), and go to **All Services** \> **Identity** \> **App Registrations**.</span></span>

2. <span data-ttu-id="a3f3d-403">Sélectionnez **Nouvelle inscription,** puis entrez un nom significatif.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-403">Select **New registration**, and enter a meaningful name.</span></span>

3. <span data-ttu-id="a3f3d-404">Sélectionnez un type de compte dans les options affichées.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-404">Select an account type from the options displayed.</span></span>

   <span data-ttu-id="a3f3d-405">Si vous utilisez Microsoft Azure avec un domaine non personnalisé, tel que **onmicrosoft.com**, sélectionnez Comptes dans cet annuaire d’organisation uniquement **(Microsoft uniquement -** Client unique).</span><span class="sxs-lookup"><span data-stu-id="a3f3d-405">If you're using Microsoft Azure with a non-custom domain, such as **onmicrosoft.com**, select **Accounts in this organizational directory only (Microsoft only - Single tenant).**</span></span>

   <span data-ttu-id="a3f3d-406">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-406">For example:</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="a3f3d-407">![Nouvelle inscription d’application](../media/dke-app-registration.png)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-407">![New App Registration](../media/dke-app-registration.png)</span></span>

4. <span data-ttu-id="a3f3d-408">Au bas de la page, sélectionnez **Enregistrer** pour créer la nouvelle inscription d’application.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-408">At the bottom of the page, select **Register** to create the new App Registration.</span></span>

5. <span data-ttu-id="a3f3d-409">Dans votre nouvelle inscription d’application, dans le volet gauche, sous **Gérer**, sélectionnez **Authentification**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-409">In your new App Registration, in the left pane, under **Manage**, select **Authentication**.</span></span>

6. <span data-ttu-id="a3f3d-410">Sélectionnez **Ajouter une plateforme.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-410">Select **Add a platform**.</span></span>

7. <span data-ttu-id="a3f3d-411">Dans la **fenêtre popup Configurer les plateformes,** sélectionnez **Web.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-411">On the **Configure platforms** popup, select **Web**.</span></span>

8. <span data-ttu-id="a3f3d-412">Sous **URI de redirection,** entrez l’URI de votre service de chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-412">Under **Redirect URIs**, enter the URI of your double key encryption service.</span></span> <span data-ttu-id="a3f3d-413">Entrez l’URL du service d’application, y compris le nom d’hôte et le domaine.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-413">Enter the App Service URL, including both the hostname and domain.</span></span>

   <span data-ttu-id="a3f3d-414">Par exemple : https://mydkeservicetest.com</span><span class="sxs-lookup"><span data-stu-id="a3f3d-414">For example: https://mydkeservicetest.com</span></span>

   - <span data-ttu-id="a3f3d-415">L’URL que vous entrez doit correspondre au nom d’hôte où votre service DKE est déployé.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-415">The URL you enter must match the hostname where your DKE service is deployed.</span></span>
   - <span data-ttu-id="a3f3d-416">Si vous testez localement avec Visual Studio, utilisez **https://localhost:5001** .</span><span class="sxs-lookup"><span data-stu-id="a3f3d-416">If you're testing locally with Visual Studio, use **https://localhost:5001**.</span></span>
   - <span data-ttu-id="a3f3d-417">Dans tous les cas, le schéma doit être **https**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-417">In all cases, the scheme must be **https**.</span></span>

   <span data-ttu-id="a3f3d-418">Assurez-vous que le nom d’hôte correspond exactement au nom d’hôte de votre service d’application.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-418">Ensure the hostname exactly matches your App Service hostname.</span></span> <span data-ttu-id="a3f3d-419">Vous l’avez peut-être modifié `localhost` pour résoudre les problèmes de la build.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-419">You may have changed it to `localhost` to troubleshoot the build.</span></span> <span data-ttu-id="a3f3d-420">In **appsettings.json**, this value is the hostname you set for `JwtAudience` .</span><span class="sxs-lookup"><span data-stu-id="a3f3d-420">In **appsettings.json**, this value is the hostname you set for `JwtAudience`.</span></span>

9. <span data-ttu-id="a3f3d-421">Sous **Octroi implicite,** cochez la **case des jetons d’ID.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-421">Under **Implicit grant**, select the **ID tokens** checkbox.</span></span>

10. <span data-ttu-id="a3f3d-422">Sélectionnez **Enregistrer** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-422">Select **Save** to save your changes.</span></span>

11. <span data-ttu-id="a3f3d-423">Dans le volet gauche, sélectionnez **Exposer une API,** puis en côté de l’URI ID d’application, sélectionnez **Définir**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-423">On the left pane, select **Expose an API**, then next to Application ID URI, select **Set**.</span></span>

12. <span data-ttu-id="a3f3d-424">Toujours dans la page **Exposer une API,** dans les étendues définies par cette **zone d’API,** **sélectionnez Ajouter une étendue.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-424">Still on the **Expose an API** page, in the **Scopes defined by this API** area, select **Add a scope**.</span></span> <span data-ttu-id="a3f3d-425">Dans la nouvelle étendue :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-425">In the new scope:</span></span>

    1. <span data-ttu-id="a3f3d-426">Définissez le nom de **l’étendue comme user_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-426">Define the scope name as **user_impersonation**.</span></span>

    2. <span data-ttu-id="a3f3d-427">Sélectionnez les administrateurs et les utilisateurs qui peuvent donner leur consentement.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-427">Select the administrators and users who can consent.</span></span>

    3. <span data-ttu-id="a3f3d-428">Définissez les valeurs restantes requises.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-428">Define any remaining values required.</span></span>

    4. <span data-ttu-id="a3f3d-429">Sélectionnez **Ajouter une étendue**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-429">Select **Add scope**.</span></span>

    5. <span data-ttu-id="a3f3d-430">Sélectionnez **Enregistrer** en haut pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-430">Select **Save** at the top to save your changes.</span></span>

13. <span data-ttu-id="a3f3d-431">Toujours dans la page **Exposer une API,** dans la zone **Applications clientes** autorisées, **sélectionnez Ajouter une application cliente.**</span><span class="sxs-lookup"><span data-stu-id="a3f3d-431">Still on the **Expose an API** page, in the **Authorized client applications** area, select **Add a client application**.</span></span>

    <span data-ttu-id="a3f3d-432">Dans la nouvelle application cliente :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-432">In the new client application:</span></span>

    1. <span data-ttu-id="a3f3d-433">Définissez l’ID client comme **d3590ed6-52b3-4102-aeff-aad2292ab01c**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-433">Define the Client ID as **d3590ed6-52b3-4102-aeff-aad2292ab01c**.</span></span> <span data-ttu-id="a3f3d-434">Cette valeur est l’ID Microsoft Office client et permet à Office d’obtenir un jeton d’accès pour votre magasin de clés.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-434">This value is the Microsoft Office client ID, and enables Office to obtain an access token for your key store.</span></span>

    2. <span data-ttu-id="a3f3d-435">Sous **Étendues autorisées,** sélectionnez **l’user_impersonation** étendue.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-435">Under **Authorized scopes**, select the **user_impersonation** scope.</span></span>

    3. <span data-ttu-id="a3f3d-436">Sélectionnez **Ajouter une application**.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-436">Select **Add application**.</span></span>

    4. <span data-ttu-id="a3f3d-437">Sélectionnez **Enregistrer** en haut pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-437">Select **Save** at the top to save your changes.</span></span>

<span data-ttu-id="a3f3d-438">Votre service DKE est maintenant inscrit.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-438">Your DKE service is now registered.</span></span> <span data-ttu-id="a3f3d-439">Continuez en [créant des étiquettes à l’aide de DKE](#create-sensitivity-labels-using-dke).</span><span class="sxs-lookup"><span data-stu-id="a3f3d-439">Continue by [creating labels using DKE](#create-sensitivity-labels-using-dke).</span></span>

## <a name="create-sensitivity-labels-using-dke"></a><span data-ttu-id="a3f3d-440">Créer des étiquettes de niveau de sensibilité à l’aide du DKE</span><span class="sxs-lookup"><span data-stu-id="a3f3d-440">Create sensitivity labels using DKE</span></span>

<span data-ttu-id="a3f3d-441">Dans le Centre de conformité Microsoft 365, créez une étiquette de sensibilité et appliquez le chiffrement comme vous le feriez autrement.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-441">In the Microsoft 365 compliance center, create a new sensitivity label and apply encryption as you would otherwise.</span></span> <span data-ttu-id="a3f3d-442">Sélectionnez **Utiliser le chiffrement à double** clé et entrez l’URL du point de terminaison de votre clé.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-442">Select **Use Double Key Encryption** and enter the endpoint URL for your key.</span></span>

<span data-ttu-id="a3f3d-443">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-443">For example:</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="a3f3d-444">![Sélectionnez Utiliser le chiffrement à double clé dans le Centre de conformité Microsoft 365](../media/dke-use-dke.png)</span><span class="sxs-lookup"><span data-stu-id="a3f3d-444">![Select Use Double Key Encryption in the Microsoft 365 compliance center](../media/dke-use-dke.png)</span></span>

<span data-ttu-id="a3f3d-445">Les étiquettes DKE que vous ajoutez commenceront à apparaître pour les utilisateurs dans les dernières versions de Microsoft 365 Apps for enterprise.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-445">Any DKE labels you add will start appearing for users in the latest versions of Microsoft 365 Apps for enterprise.</span></span>

> [!NOTE]
> <span data-ttu-id="a3f3d-446">L’actualisation des clients avec les nouvelles étiquettes peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-446">It may take up to 24 hours for the clients to refresh with the new labels.</span></span>

### <a name="enable-dke-in-your-client"></a><span data-ttu-id="a3f3d-447">Activer le DKE dans votre client</span><span class="sxs-lookup"><span data-stu-id="a3f3d-447">Enable DKE in your client</span></span>

<span data-ttu-id="a3f3d-448">Si vous êtes un Office Insider, DKE est activé pour vous.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-448">If you're an Office Insider, DKE is enabled for you.</span></span> <span data-ttu-id="a3f3d-449">Sinon, activez DKE pour votre client en ajoutant les clés de Registre suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3f3d-449">Otherwise, enable DKE for your client by adding the following registry keys:</span></span>

```console
   [HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\MSIPC\flighting]
   "DoubleKeyProtection"=dword:00000001

   [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\flighting]
   "DoubleKeyProtection"=dword:00000001
```

## <a name="migrate-protected-files-from-hyok-labels-to-dke-labels"></a><span data-ttu-id="a3f3d-450">Migrer des fichiers protégés des étiquettes HYOK vers des étiquettes DKE</span><span class="sxs-lookup"><span data-stu-id="a3f3d-450">Migrate protected files from HYOK labels to DKE labels</span></span>

<span data-ttu-id="a3f3d-451">Si vous le souhaitez, une fois que vous avez terminé la configuration du DKE, vous pouvez migrer le contenu que vous avez protégé à l’aide d’étiquettes HYOK vers des étiquettes DKE.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-451">If you want, once you're finished setting up DKE, you can migrate content that you've protected using HYOK labels to DKE labels.</span></span> <span data-ttu-id="a3f3d-452">Pour migrer, vous allez utiliser le scanneur AIP.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-452">To migrate, you'll use the AIP scanner.</span></span> <span data-ttu-id="a3f3d-453">Pour commencer à utiliser le scanneur, voir [qu’est-ce](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner)que le scanneur d’étiquetage unifié Azure Information Protection ?</span><span class="sxs-lookup"><span data-stu-id="a3f3d-453">To get started using the scanner, see [What is the Azure Information Protection unified labeling scanner?](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner).</span></span>

<span data-ttu-id="a3f3d-454">Si vous ne migrez pas de contenu, votre contenu protégé HYOK reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-454">If you don't migrate content, your HYOK protected content will remain unaffected.</span></span>

---
title: Chiffrement à double clé (DKE)
description: DKE vous permet de protéger les données hautement sensibles tout en conservant le contrôle total de votre clé.
author: kccross
ms.author: krowley
manager: laurawi
ms.date: 07/21/2020
ms.topic: conceptual
ms.service: information-protection
audience: Admin
ms.reviewer: esaggese
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.openlocfilehash: 47fc4bc47831970ef7a7f2087cf6c86b6fefb8c2
ms.sourcegitcommit: fe20f5ed07f38786c63df0f73659ca472e69e478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/21/2020
ms.locfileid: "45201680"
---
# <a name="double-key-encryption-dke"></a><span data-ttu-id="41b60-103">Chiffrement à double clé (DKE)</span><span class="sxs-lookup"><span data-stu-id="41b60-103">Double Key Encryption (DKE)</span></span>

> <span data-ttu-id="41b60-104">*S’applique à : [conformité Microsoft 365](https://www.microsoft.com/microsoft-365/business/compliance-management), [Azure information protection](https://azure.microsoft.com/pricing/details/information-protection)*</span><span class="sxs-lookup"><span data-stu-id="41b60-104">*Applies to: [Microsoft 365 Compliance](https://www.microsoft.com/microsoft-365/business/compliance-management), [Azure Information Protection](https://azure.microsoft.com/pricing/details/information-protection)*</span></span>
>
> <span data-ttu-id="41b60-105">*Instructions pour : [client d’étiquetage unifié Azure information protection pour Windows](https://docs.microsoft.com/azure/information-protection/faqs.md#whats-the-difference-between-the-azure-information-protection-classic-and-unified-labeling-clients)*</span><span class="sxs-lookup"><span data-stu-id="41b60-105">*Instructions for: [Azure Information Protection unified labeling client for Windows](https://docs.microsoft.com/azure/information-protection/faqs.md#whats-the-difference-between-the-azure-information-protection-classic-and-unified-labeling-clients)*</span></span>
>
> <span data-ttu-id="41b60-106">*Description du service : [conformité Microsoft 365](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance)*</span><span class="sxs-lookup"><span data-stu-id="41b60-106">*Service description for: [Microsoft 365 Compliance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance)*</span></span>

<span data-ttu-id="41b60-107">Cette version préliminaire publique du chiffrement à double clé (DKE) vous permet d’utiliser le client d’étiquetage unifié Azure information protection pour protéger le contenu hautement sensible tout en conservant le contrôle total de votre clé.</span><span class="sxs-lookup"><span data-stu-id="41b60-107">This public preview version of Double Key Encryption (DKE) enables you to use the Azure Information Protection Unified Labeling Client to protect highly sensitive content while maintaining full control of your key.</span></span>

<span data-ttu-id="41b60-108">Le chiffrement à double clé requiert deux clés, utilisées ensemble, pour accéder au contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="41b60-108">Double Key Encryption requires two keys, used together, to access protected content.</span></span> <span data-ttu-id="41b60-109">Vous stockez une clé dans Microsoft Azure et vous la maintenez.</span><span class="sxs-lookup"><span data-stu-id="41b60-109">You store one key in Microsoft Azure, and you hold the other key.</span></span>

<span data-ttu-id="41b60-110">Le chiffrement à double clé prend en charge les déploiements sur le Cloud et sur site.</span><span class="sxs-lookup"><span data-stu-id="41b60-110">Double Key Encryption supports both cloud and on-premises deployments.</span></span> <span data-ttu-id="41b60-111">Ces déploiements permettent de s’assurer que les données chiffrées restent opaques, où que vous stockez les données protégées.</span><span class="sxs-lookup"><span data-stu-id="41b60-111">These deployments help to ensure that encrypted data remains opaque wherever you store the protected data.</span></span>

<span data-ttu-id="41b60-112">Pour plus d’informations sur les clés de racine de client par défaut, consultez la rubrique [planification et implémentation de votre clé de client Azure information protection](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key).</span><span class="sxs-lookup"><span data-stu-id="41b60-112">For more information about the default, cloud-based tenant root keys, see [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key).</span></span>

<span data-ttu-id="41b60-113">Le chiffrement à double clé est similaire à un cadre de dépôt de sécurité qui nécessite à la fois une clé bancaire et une clé client pour accéder.</span><span class="sxs-lookup"><span data-stu-id="41b60-113">Double Key Encryption is similar to a safety deposit box that requires both a bank key and a customer key to gain access.</span></span> <span data-ttu-id="41b60-114">Pour déchiffrer le contenu protégé, vous devez utiliser à la fois la clé gérée Microsoft et la clé détenue par le client.</span><span class="sxs-lookup"><span data-stu-id="41b60-114">To decrypt protected content, you must use both the Microsoft managed key and the customer-held key.</span></span>

<span data-ttu-id="41b60-115">La vidéo suivante montre comment le chiffrement à clé double fonctionne pour sécuriser votre contenu.</span><span class="sxs-lookup"><span data-stu-id="41b60-115">The following video shows how Double Key Encryption works to secure your content.</span></span>

<span data-ttu-id="41b60-116">Si votre organisation dispose de l’une des conditions suivantes, vous pouvez utiliser DKE pour sécuriser votre contenu :</span><span class="sxs-lookup"><span data-stu-id="41b60-116">If your organizations have any of the following requirements, you can use DKE to help secure your content:</span></span>

- <span data-ttu-id="41b60-117">Vous souhaitez vous assurer que *vous* êtes le seul à pouvoir déchiffrer le contenu protégé, dans toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="41b60-117">You want to ensure that *only you* can ever decrypt protected content, under all circumstances.</span></span>
- <span data-ttu-id="41b60-118">Vous ne souhaitez pas que Microsoft ait accès aux données protégées de façon autonome.</span><span class="sxs-lookup"><span data-stu-id="41b60-118">You don't want Microsoft to have access to protected data on its own.</span></span>
- <span data-ttu-id="41b60-119">Vous avez des exigences réglementaires à maintenir des clés dans une limite géographique.</span><span class="sxs-lookup"><span data-stu-id="41b60-119">You have regulatory requirements to hold keys within a geographical boundary.</span></span> <span data-ttu-id="41b60-120">Toutes les clés détenues par le client pour le chiffrement et le déchiffrement des données sont conservées dans votre centre de données.</span><span class="sxs-lookup"><span data-stu-id="41b60-120">All customer-held keys for data encryption and decryption are maintained in your data center.</span></span>

> [!VIDEO https://msit.microsoftstream.com/embed/video/f466a1ff-0400-a936-221c-f1eab45dc756]

## <a name="system-and-licensing-requirements-for-dke"></a><span data-ttu-id="41b60-121">Exigences en matière de système et de licence pour DKE</span><span class="sxs-lookup"><span data-stu-id="41b60-121">System and licensing requirements for DKE</span></span>

<span data-ttu-id="41b60-122">Cette version préliminaire publique du chiffrement à deux clés pour Microsoft 365 est disponible dans le cadre de Microsoft 365 E5 et Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="41b60-122">This public preview release of Double Key Encryption for Microsoft 365 is available as part of Microsoft 365 E5 and Office 365 E5.</span></span> <span data-ttu-id="41b60-123">Si vous n’avez pas de licence Microsoft 365 E5, vous pouvez vous inscrire pour obtenir une [version d’évaluation](https://aka.ms/M365E5ComplianceTrial).</span><span class="sxs-lookup"><span data-stu-id="41b60-123">If you don’t have a Microsoft 365 E5 license, you can sign up for a [trial](https://aka.ms/M365E5ComplianceTrial).</span></span> <span data-ttu-id="41b60-124">Pour plus d’informations sur ces licences, consultez [la rubrique Microsoft 365 Licensing Guidance for security & Compliance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).</span><span class="sxs-lookup"><span data-stu-id="41b60-124">For more information about these licenses, see [Microsoft 365 licensing guidance for security & compliance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).</span></span>

<span data-ttu-id="41b60-125">**Office Insider** Pour utiliser la préversion publique, vous devez être membre du programme Office Insider.</span><span class="sxs-lookup"><span data-stu-id="41b60-125">**Office Insider** To use the public preview, you must be a member of the Office Insider program.</span></span> <span data-ttu-id="41b60-126">Pour rejoindre Office Insider, accédez à [https://insider.office.com](https://insider.office.com) .</span><span class="sxs-lookup"><span data-stu-id="41b60-126">To join Office Insider, go to [https://insider.office.com](https://insider.office.com).</span></span> <span data-ttu-id="41b60-127">Une fois que vous êtes membre, préparez votre environnement pour déployer les builds Office Insider en choisissant la méthode de déploiement appropriée pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="41b60-127">Once you're a member, prepare your environment to deploy Office Insider builds by choosing the right deployment method for your organization.</span></span> <span data-ttu-id="41b60-128">Pour obtenir des instructions, consultez la rubrique [prise en main du déploiement des builds Office Insider](https://insider.office.com/business/deploy).</span><span class="sxs-lookup"><span data-stu-id="41b60-128">For instructions, see [Getting started on deploying Office Insider builds](https://insider.office.com/business/deploy).</span></span>

<span data-ttu-id="41b60-129">**Azure information protection**.</span><span class="sxs-lookup"><span data-stu-id="41b60-129">**Azure Information Protection**.</span></span> <span data-ttu-id="41b60-130">DKE fonctionne avec les étiquettes de confidentialité et nécessite Azure information protection.</span><span class="sxs-lookup"><span data-stu-id="41b60-130">DKE works with sensitivity labels and requires Azure Information Protection.</span></span>

## <a name="supported-environments-for-storing-and-viewing-dke-protected-content"></a><span data-ttu-id="41b60-131">Environnements pris en charge pour le stockage et l’affichage du contenu protégé par DKE</span><span class="sxs-lookup"><span data-stu-id="41b60-131">Supported environments for storing and viewing DKE-protected content</span></span>

<span data-ttu-id="41b60-132">**Applications prises en charge**.</span><span class="sxs-lookup"><span data-stu-id="41b60-132">**Supported applications**.</span></span> <span data-ttu-id="41b60-133">[Applications Microsoft 365 pour](https://www.microsoft.com/microsoft-365/business/microsoft-365-apps-for-enterprise-product) les clients d’entreprise sur Windows, y compris Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="41b60-133">[Microsoft 365 Apps for enterprise](https://www.microsoft.com/microsoft-365/business/microsoft-365-apps-for-enterprise-product) clients on Windows, including Word, Excel, and PowerPoint.</span></span>

<span data-ttu-id="41b60-134">**Prise en charge du contenu en ligne**.</span><span class="sxs-lookup"><span data-stu-id="41b60-134">**Online content support**.</span></span> <span data-ttu-id="41b60-135">Les documents et les fichiers stockés en ligne dans Microsoft SharePoint et OneDrive entreprise sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="41b60-135">Documents and files stored online in both Microsoft SharePoint and OneDrive for Business are supported.</span></span> <span data-ttu-id="41b60-136">Vous pouvez partager le contenu chiffré par courrier électronique, mais vous ne pouvez pas afficher les documents et fichiers chiffrés en ligne.</span><span class="sxs-lookup"><span data-stu-id="41b60-136">You can share encrypted content by email, but you can't view encrypted documents and files online.</span></span> <span data-ttu-id="41b60-137">Au lieu de cela, vous devez afficher le contenu protégé à l’aide des applications de bureau sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="41b60-137">Instead, you must view protected content using the desktop apps on your local computer.</span></span>

## <a name="about-this-public-preview-article"></a><span data-ttu-id="41b60-138">À propos de cet article d’aperçu public</span><span class="sxs-lookup"><span data-stu-id="41b60-138">About this public preview article</span></span>

<span data-ttu-id="41b60-139">Il existe plusieurs façons de procéder pour déployer le chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="41b60-139">There are several ways you can complete some of the steps to deploy Double Key Encryption.</span></span> <span data-ttu-id="41b60-140">Cet article fournit des instructions détaillées afin que les administrateurs moins expérimentés déploient correctement le service.</span><span class="sxs-lookup"><span data-stu-id="41b60-140">This article provides detailed instructions so that less experienced admins successfully deploy the service.</span></span> <span data-ttu-id="41b60-141">Si vous êtes familiarisé avec les technologies communes, telles que git, partagées par les méthodes de déploiement décrites dans cet article, vous pouvez choisir d’utiliser vos propres méthodes.</span><span class="sxs-lookup"><span data-stu-id="41b60-141">If you're experienced with the common technologies, such as git, shared by the deployment methods described in this article, you can choose to use your own methods.</span></span>

<span data-ttu-id="41b60-142">Pour la préversion publique, nous avons inclus des instructions détaillées sur la façon de déployer le service de chiffrement à double clé sur Azure.</span><span class="sxs-lookup"><span data-stu-id="41b60-142">For public preview, we've included step-by-step instructions on how to deploy the Double Key Encryption service to Azure.</span></span> <span data-ttu-id="41b60-143">Ce scénario n’est pas très probable en production.</span><span class="sxs-lookup"><span data-stu-id="41b60-143">This scenario isn't something you'd likely do in production.</span></span> <span data-ttu-id="41b60-144">Pour la préversion publique à l’aide d’Azure, il s’agit d’un moyen rapide de déployer, qui vous permet de commencer à utiliser le chiffrement à clé double immédiatement.</span><span class="sxs-lookup"><span data-stu-id="41b60-144">For public preview using Azure is a quick way to deploy that lets you get started using Double Key Encryption right away.</span></span>

<span data-ttu-id="41b60-145">Vous pouvez choisir de déployer le service où vous le souhaitez, qu’il soit local sur votre réseau ou auprès d’un autre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="41b60-145">You can choose to deploy the service wherever you want, whether it's locally on your network or with another provider.</span></span> <span data-ttu-id="41b60-146">Vous devrez publier le magasin de clés à l’aide des méthodes appropriées pour cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="41b60-146">You'll need to publish the key store using methods appropriate for that location.</span></span>

## <a name="deploy-double-key-encryption"></a><span data-ttu-id="41b60-147">Déployer le chiffrement à double clé</span><span class="sxs-lookup"><span data-stu-id="41b60-147">Deploy Double Key Encryption</span></span>

<span data-ttu-id="41b60-148">Suivez ces étapes générales pour configurer le chiffrement à double clé pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="41b60-148">You'll follow these general steps to set up Double Key Encryption for your organization.</span></span> <span data-ttu-id="41b60-149">L’exemple de cet article utilise Azure comme destination de déploiement pour le service DKE.</span><span class="sxs-lookup"><span data-stu-id="41b60-149">The example in this article uses Azure as the deployment destination for the DKE service.</span></span> <span data-ttu-id="41b60-150">Si vous effectuez le déploiement vers un autre emplacement, vous devez fournir vos propres valeurs.</span><span class="sxs-lookup"><span data-stu-id="41b60-150">If you're deploying to another location, you'll need to provide your own values.</span></span>

1. [<span data-ttu-id="41b60-151">Installer les composants logiciels requis</span><span class="sxs-lookup"><span data-stu-id="41b60-151">Install software prerequisites</span></span>](#install-software-prerequisites)
1. [<span data-ttu-id="41b60-152">Cloner le référentiel GitHub de chiffrement à double clé</span><span class="sxs-lookup"><span data-stu-id="41b60-152">Clone the Double Key Encryption GitHub repository</span></span>](#clone-the-dke-github-repository)
1. [<span data-ttu-id="41b60-153">Modifier les paramètres d’application</span><span class="sxs-lookup"><span data-stu-id="41b60-153">Modify application settings</span></span>](#modify-application-settings)
1. [<span data-ttu-id="41b60-154">Générer des clés de test</span><span class="sxs-lookup"><span data-stu-id="41b60-154">Generate test keys</span></span>](#generate-test-keys)
1. [<span data-ttu-id="41b60-155">Générer le projet</span><span class="sxs-lookup"><span data-stu-id="41b60-155">Build the project</span></span>](#build-the-project)
1. [<span data-ttu-id="41b60-156">Publier le magasin de clés</span><span class="sxs-lookup"><span data-stu-id="41b60-156">Publish the key store</span></span>](#publish-the-key-store)
1. [<span data-ttu-id="41b60-157">Valider votre déploiement</span><span class="sxs-lookup"><span data-stu-id="41b60-157">Validate your deployment</span></span>](#validate-your-deployment)
1. [<span data-ttu-id="41b60-158">Enregistrer votre magasin de clés</span><span class="sxs-lookup"><span data-stu-id="41b60-158">Register your key store</span></span>](#register-your-key-store)
1. [<span data-ttu-id="41b60-159">Créer des étiquettes de sensibilité</span><span class="sxs-lookup"><span data-stu-id="41b60-159">Create sensitivity labels</span></span>](#create-labels-using-dke)

<span data-ttu-id="41b60-160">Lorsque vous avez fini, vous pouvez chiffrer des documents et des fichiers à l’aide de DKE.</span><span class="sxs-lookup"><span data-stu-id="41b60-160">When you're done, you can encrypt documents and files using DKE.</span></span> <span data-ttu-id="41b60-161">Pour plus d’informations, consultez [la rubrique appliquer des étiquettes de confidentialité à vos fichiers et à votre messagerie électronique dans Office](https://support.microsoft.com/office/2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9).</span><span class="sxs-lookup"><span data-stu-id="41b60-161">For information, see [Apply sensitivity labels to your files and email in Office](https://support.microsoft.com/office/2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9).</span></span>

### <a name="install-software-prerequisites"></a><span data-ttu-id="41b60-162">Installer les composants logiciels requis</span><span class="sxs-lookup"><span data-stu-id="41b60-162">Install software prerequisites</span></span>

<span data-ttu-id="41b60-163">Il existe deux types de logiciels requis pour le chiffrement à double clé</span><span class="sxs-lookup"><span data-stu-id="41b60-163">There are two types of software prerequisites for Double Key Encryption</span></span>

- [<span data-ttu-id="41b60-164">Conditions préalables requises pour le service de chiffrement à clé double</span><span class="sxs-lookup"><span data-stu-id="41b60-164">Double Key Encryption service prerequisites</span></span>](#double-key-encryption-service-prerequisites)
- [<span data-ttu-id="41b60-165">Conditions préalables au chiffrement à double clé pour les ordinateurs clients</span><span class="sxs-lookup"><span data-stu-id="41b60-165">Double Key Encryption prerequisites for client computers</span></span>](#double-key-encryption-prerequisites-for-client-computers)

#### <a name="double-key-encryption-service-prerequisites"></a><span data-ttu-id="41b60-166">Conditions préalables requises pour le service de chiffrement à clé double</span><span class="sxs-lookup"><span data-stu-id="41b60-166">Double Key Encryption service prerequisites</span></span>

<span data-ttu-id="41b60-167">Installez ces éléments prérequis sur l’ordinateur sur lequel vous souhaitez installer le service DKE.</span><span class="sxs-lookup"><span data-stu-id="41b60-167">Install these prerequisites on the computer where you want to install the DKE service.</span></span>

<span data-ttu-id="41b60-168">**.Net Core 3,1 SDK**.</span><span class="sxs-lookup"><span data-stu-id="41b60-168">**.NET Core 3.1 SDK**.</span></span> <span data-ttu-id="41b60-169">Téléchargez et installez le kit de développement logiciel (SDK) à partir de [Télécharger .net Core 3,1](https://dotnet.microsoft.com/download/dotnet-core/3.1).</span><span class="sxs-lookup"><span data-stu-id="41b60-169">Download and install the SDK from [Download .NET Core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1).</span></span>

<span data-ttu-id="41b60-170">**Visual Studio code**.</span><span class="sxs-lookup"><span data-stu-id="41b60-170">**Visual Studio Code**.</span></span> <span data-ttu-id="41b60-171">Téléchargez Visual Studio code à partir de [https://code.visualstudio.com/](https://code.visualstudio.com) .</span><span class="sxs-lookup"><span data-stu-id="41b60-171">Download Visual Studio Code from [https://code.visualstudio.com/](https://code.visualstudio.com).</span></span> <span data-ttu-id="41b60-172">Une fois installé, exécutez Visual Studio code et sélectionnez **Afficher** les \> **Extensions**.</span><span class="sxs-lookup"><span data-stu-id="41b60-172">Once installed, run Visual Studio Code and select **View** \> **Extensions**.</span></span> <span data-ttu-id="41b60-173">Installez ces extensions.</span><span class="sxs-lookup"><span data-stu-id="41b60-173">Install these extensions.</span></span>

- <span data-ttu-id="41b60-174">C# pour Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="41b60-174">C# for Visual Studio Code</span></span>

- <span data-ttu-id="41b60-175">Gestionnaire de package NuGet</span><span class="sxs-lookup"><span data-stu-id="41b60-175">NuGet Package Manager</span></span>

<span data-ttu-id="41b60-176">**Microsoft Office Insider**.</span><span class="sxs-lookup"><span data-stu-id="41b60-176">**Microsoft Office Insider**.</span></span> <span data-ttu-id="41b60-177">Configurez au moins une [méthode de déploiement](https://insider.office.com/business/deploy).</span><span class="sxs-lookup"><span data-stu-id="41b60-177">Set up at least one [deployment method](https://insider.office.com/business/deploy).</span></span>

<span data-ttu-id="41b60-178">**Ressources git**.</span><span class="sxs-lookup"><span data-stu-id="41b60-178">**Git resources**.</span></span> <span data-ttu-id="41b60-179">Téléchargez et installez l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="41b60-179">Download and install one of the following.</span></span>

- [<span data-ttu-id="41b60-180">Git</span><span class="sxs-lookup"><span data-stu-id="41b60-180">Git</span></span>](https://git-scm.com/downloads)

- [<span data-ttu-id="41b60-181">Bureau GitHub</span><span class="sxs-lookup"><span data-stu-id="41b60-181">GitHub Desktop</span></span>](https://desktop.github.com/)

- [<span data-ttu-id="41b60-182">GitHub entreprise</span><span class="sxs-lookup"><span data-stu-id="41b60-182">GitHub Enterprise</span></span>](https://github.com/enterprise)

<span data-ttu-id="41b60-183">**OpenSSL** [OpenSSL](https://slproweb.com/products/Win32OpenSSL.html) doit être installé pour [générer des clés de test](#generate-test-keys) une fois que vous avez déployé DKE.</span><span class="sxs-lookup"><span data-stu-id="41b60-183">**OpenSSL** You must have [OpenSSL](https://slproweb.com/products/Win32OpenSSL.html) installed to [generate test keys](#generate-test-keys) after you deploy DKE.</span></span> <span data-ttu-id="41b60-184">Vérifiez que vous l’appelez correctement à partir de votre chemin d’accès aux variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="41b60-184">Make sure you're invoking it correctly from your environment variables path.</span></span> <span data-ttu-id="41b60-185">Par exemple, pour plus d’informations, consultez la section « ajouter le répertoire d’installation au chemin d’accès » https://www.osradar.com/install-openssl-windows/ .</span><span class="sxs-lookup"><span data-stu-id="41b60-185">For example, see "Add the installation directory to PATH" at https://www.osradar.com/install-openssl-windows/ for details.</span></span>

#### <a name="double-key-encryption-prerequisites-for-client-computers"></a><span data-ttu-id="41b60-186">Conditions préalables au chiffrement à double clé pour les ordinateurs clients</span><span class="sxs-lookup"><span data-stu-id="41b60-186">Double Key Encryption prerequisites for client computers</span></span>

<span data-ttu-id="41b60-187">Installez ces éléments prérequis sur chaque ordinateur client sur lequel vous souhaitez protéger et consommer des documents protégés.</span><span class="sxs-lookup"><span data-stu-id="41b60-187">Install these prerequisites on each client computer where you want to protect and consume protected documents.</span></span>

<span data-ttu-id="41b60-188">**Microsoft Office** version \*. 12711 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="41b60-188">**Microsoft Office** version \*.12711 or later.</span></span>

<span data-ttu-id="41b60-189">Versions du **client d’étiquetage unifié Azure information protection** 2.7.93.0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="41b60-189">**Azure Information Protection Unified Labeling Client** versions 2.7.93.0 or later.</span></span> <span data-ttu-id="41b60-190">Téléchargez et installez le client d’étiquetage unifié de [Microsoft](https://www.microsoft.com/download/details.aspx?id=53018).</span><span class="sxs-lookup"><span data-stu-id="41b60-190">Download and install the Unified Labeling client from [Microsoft](https://www.microsoft.com/download/details.aspx?id=53018).</span></span>

### <a name="clone-the-dke-github-repository"></a><span data-ttu-id="41b60-191">Cloner le référentiel DKE GitHub</span><span class="sxs-lookup"><span data-stu-id="41b60-191">Clone the DKE GitHub repository</span></span>

<span data-ttu-id="41b60-192">Microsoft fournit les fichiers source DKE dans un référentiel GitHub.</span><span class="sxs-lookup"><span data-stu-id="41b60-192">Microsoft supplies the DKE source files in a GitHub repository.</span></span> <span data-ttu-id="41b60-193">Vous clonez le référentiel pour créer le projet localement pour l’utilisation de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="41b60-193">You clone the repository to build the project locally for your organization's use.</span></span> <span data-ttu-id="41b60-194">Le référentiel DKE GitHub se trouve à l’emplacement [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService) .</span><span class="sxs-lookup"><span data-stu-id="41b60-194">The DKE GitHub repository is located at [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService).</span></span>

<span data-ttu-id="41b60-195">Les instructions suivantes sont destinées aux utilisateurs de git ou de code Visual Studio inexpérimentés :</span><span class="sxs-lookup"><span data-stu-id="41b60-195">The following instructions are intended for inexperienced git or Visual Studio Code users:</span></span>

1. <span data-ttu-id="41b60-196">Dans votre navigateur, accédez à :[https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService)</span><span class="sxs-lookup"><span data-stu-id="41b60-196">In your browser, go to: [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService)</span></span>

1. <span data-ttu-id="41b60-197">Dans la partie droite de l’écran, sélectionnez **code**.</span><span class="sxs-lookup"><span data-stu-id="41b60-197">Towards the right side of the screen, select **Code**.</span></span> <span data-ttu-id="41b60-198">Votre version de l’interface utilisateur peut afficher un bouton **Clone ou télécharger** .</span><span class="sxs-lookup"><span data-stu-id="41b60-198">Your version of the UI might show a **Clone or download** button.</span></span> <span data-ttu-id="41b60-199">Ensuite, dans la liste déroulante qui apparaît, sélectionnez l’icône copier pour copier l’URL dans votre presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="41b60-199">Then, in the dropdown that appears, select the copy icon to copy the URL to your clipboard.</span></span>

    <span data-ttu-id="41b60-200">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="41b60-200">For example:</span></span>

    :::image type="content" source="../media/dke-clone.png" alt-text="Cloner le référentiel du service de chiffrement à clé double à partir de GitHub":::

3. <span data-ttu-id="41b60-202">Dans Visual Studio code, sélectionnez **Afficher** la \> **palette de commandes** et sélectionnez **git : Clone**.</span><span class="sxs-lookup"><span data-stu-id="41b60-202">In Visual Studio Code, select **View** \> **Command Palette** and select **Git: Clone**.</span></span> <span data-ttu-id="41b60-203">Pour accéder à l’option dans la liste, commencez `git: clone` à taper pour filtrer les entrées, puis sélectionnez-la dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="41b60-203">To jump to the option in the list, start typing `git: clone` to filter the entries and then select it from the drop-down.</span></span> <span data-ttu-id="41b60-204">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="41b60-204">For example:</span></span>

    :::image type="content" source="../media/dke-vscode-clone.png" alt-text="Option GIT : clone de Visual Studio code":::

4. <span data-ttu-id="41b60-206">Dans la zone de texte, collez l’URL que vous avez copiée à partir de git et sélectionnez **Clone dans GitHub**.</span><span class="sxs-lookup"><span data-stu-id="41b60-206">In the text box, paste the URL that you copied from Git and select **Clone from GitHub**.</span></span>

5. <span data-ttu-id="41b60-207">Dans la boîte de dialogue **Sélectionner un dossier** qui s’affiche, accédez à l’emplacement où vous souhaitez stocker le référentiel et sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="41b60-207">In the **Select Folder** dialog that appears, browse to and select a location to store the repository.</span></span> <span data-ttu-id="41b60-208">À l’invite, sélectionnez **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="41b60-208">At the prompt, select **Open**.</span></span>

    <span data-ttu-id="41b60-209">Le référentiel est ouvert dans Visual Studio code et affiche la branche git actuelle en bas à gauche.</span><span class="sxs-lookup"><span data-stu-id="41b60-209">The repository is opened in Visual Studio Code, and displays the current Git branch at the bottom left.</span></span> <span data-ttu-id="41b60-210">Votre branche actuelle doit être **Master**.</span><span class="sxs-lookup"><span data-stu-id="41b60-210">Your current branch should be **master**.</span></span>

    <span data-ttu-id="41b60-211">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="41b60-211">For example:</span></span>

    :::image type="content" source="../media/dke-vscode-master.png" alt-text="Branche Visual Studio code Master":::

6. <span data-ttu-id="41b60-213">Sélectionnez le masque de mots **,** puis sélectionnez **public_preview** dans la liste des branches.</span><span class="sxs-lookup"><span data-stu-id="41b60-213">Select the word **master,** and then select **public_preview** from the list of branches.</span></span> 

   > [!IMPORTANT]
   > <span data-ttu-id="41b60-214">La sélection de la branche public_preview vous permet de vous assurer que vous disposez des fichiers appropriés pour générer le projet.</span><span class="sxs-lookup"><span data-stu-id="41b60-214">Selecting the public_preview branch ensures that you have the correct files to build the project.</span></span> <span data-ttu-id="41b60-215">Si vous ne sélectionnez pas la branche appropriée, votre déploiement échouera.</span><span class="sxs-lookup"><span data-stu-id="41b60-215">If you do not choose the correct branch your deployment will fail.</span></span>

<span data-ttu-id="41b60-216">Votre référentiel source DKE est maintenant configuré localement.</span><span class="sxs-lookup"><span data-stu-id="41b60-216">You now have your DKE source repository set up locally.</span></span> <span data-ttu-id="41b60-217">Ensuite, [Modifiez les paramètres d’application](#modify-application-settings) pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="41b60-217">Next, [modify application settings](#modify-application-settings) for your organization.</span></span>

### <a name="modify-application-settings"></a><span data-ttu-id="41b60-218">Modifier les paramètres d’application</span><span class="sxs-lookup"><span data-stu-id="41b60-218">Modify application settings</span></span>

<span data-ttu-id="41b60-219">Pour déployer le service DKE, vous devez modifier les types de paramètres d’application suivants :</span><span class="sxs-lookup"><span data-stu-id="41b60-219">To deploy the DKE service, you must modify the following types of application settings:</span></span>

- [<span data-ttu-id="41b60-220">Paramètres d’accès clés</span><span class="sxs-lookup"><span data-stu-id="41b60-220">Key access settings</span></span>](#key-access-settings)
- [<span data-ttu-id="41b60-221">Paramètres de client et de clé</span><span class="sxs-lookup"><span data-stu-id="41b60-221">Tenant and key settings</span></span>](#tenant-and-key-settings)

<span data-ttu-id="41b60-222">Vous modifiez les paramètres de l’application dans le fichier appsettings.js.</span><span class="sxs-lookup"><span data-stu-id="41b60-222">You modify application settings in the appsettings.json file.</span></span> <span data-ttu-id="41b60-223">Ce fichier se trouve dans le DoubleKeyEncryptionService référentiel que vous avez cloné localement sous DoubleKeyEncryptionService\src\customer-key-store.</span><span class="sxs-lookup"><span data-stu-id="41b60-223">This file is located in the DoubleKeyEncryptionService repo you cloned locally under DoubleKeyEncryptionService\src\customer-key-store.</span></span> <span data-ttu-id="41b60-224">Par exemple, dans Visual Studio code, vous pouvez accéder au fichier comme indiqué dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="41b60-224">For example, in Visual Studio Code, you can browse to the file as shown in the following picture.</span></span>

:::image type="content" source="../media/dke-appsettingsjson.png" alt-text="Recherche de la appsettings.jssur le fichier pour DKE.":::

#### <a name="key-access-settings"></a><span data-ttu-id="41b60-226">Paramètres d’accès clés</span><span class="sxs-lookup"><span data-stu-id="41b60-226">Key access settings</span></span>

<span data-ttu-id="41b60-227">Choisissez d’utiliser ou non l’autorisation de messagerie ou de rôle.</span><span class="sxs-lookup"><span data-stu-id="41b60-227">Choose whether to use email or role authorization.</span></span> <span data-ttu-id="41b60-228">DKE ne prend en charge qu’une seule de ces méthodes d’authentification à la fois.</span><span class="sxs-lookup"><span data-stu-id="41b60-228">DKE supports only one of these authentication methods at a time.</span></span>

- <span data-ttu-id="41b60-229">**Autorisation de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="41b60-229">**Email authorization**.</span></span> <span data-ttu-id="41b60-230">Permet à votre organisation d’autoriser l’accès aux clés en fonction des adresses de messagerie uniquement.</span><span class="sxs-lookup"><span data-stu-id="41b60-230">Allows your organization to authorize access to keys based on email addresses only.</span></span>

- <span data-ttu-id="41b60-231">**Autorisation de rôle**.</span><span class="sxs-lookup"><span data-stu-id="41b60-231">**Role authorization**.</span></span> <span data-ttu-id="41b60-232">Permet à votre organisation d’autoriser l’accès aux clés en fonction des groupes Active Directory et exige que le service Web interroge LDAP.</span><span class="sxs-lookup"><span data-stu-id="41b60-232">Allows your organization to authorize access to keys based on Active Directory groups, and requires that the web service can query LDAP.</span></span>

<span data-ttu-id="41b60-233">Pour définir les paramètres d’accès à la clé pour DKE :</span><span class="sxs-lookup"><span data-stu-id="41b60-233">To set key access settings for DKE:</span></span>

1. <span data-ttu-id="41b60-234">Dans le fichier **appsettings.js** , définissez un seul des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="41b60-234">In the **appsettings.json** file, define only one of these settings:</span></span>

   - <span data-ttu-id="41b60-235">Pour l’autorisation de messagerie, recherchez le paramètre **AuthorizedEmailAddresses** .</span><span class="sxs-lookup"><span data-stu-id="41b60-235">For email authorization, locate the **AuthorizedEmailAddresses** setting.</span></span> <span data-ttu-id="41b60-236">Ajoutez l’adresse de messagerie que vous souhaitez autoriser.</span><span class="sxs-lookup"><span data-stu-id="41b60-236">Add the email address that you want to authorize.</span></span> <span data-ttu-id="41b60-237">Séparez les adresses de messagerie par des guillemets et des virgules.</span><span class="sxs-lookup"><span data-stu-id="41b60-237">Separate multiple email addresses with double quotes and commas.</span></span> <span data-ttu-id="41b60-238">Par exemple : **"'AuthorizedEmailAddresses'" : ["email1@company.com", "Email2@company.com", Email3@company.com]**</span><span class="sxs-lookup"><span data-stu-id="41b60-238">For example: **" ‘AuthorizedEmailAddresses’ ": ["email1@company.com", "email2@company.com ", email3@company.com]**</span></span>

   :::image type="content" source="../media/dke-email-accesssetting.png" alt-text="appsettings.jsdu fichier affichant la méthode d’autorisation de messagerie":::

   - <span data-ttu-id="41b60-240">Pour l’autorisation de rôle, recherchez le paramètre **AuthorizedRoles** .</span><span class="sxs-lookup"><span data-stu-id="41b60-240">For role authorization, locate the **AuthorizedRoles** setting.</span></span> <span data-ttu-id="41b60-241">Définissez avec les noms de groupe ActiveDirectory que vous souhaitez autoriser.</span><span class="sxs-lookup"><span data-stu-id="41b60-241">Define with the ActiveDirectory group names you want to authorize.</span></span> <span data-ttu-id="41b60-242">Par exemple : **"AuthorizedRoles" : ["group1", "group2", "Group3"]**</span><span class="sxs-lookup"><span data-stu-id="41b60-242">For example: **"AuthorizedRoles": ["group1", "group2", "group3"]**</span></span>

   :::image type="content" source="../media/dke-role-accesssetting.png" alt-text="appsettings.jssur le fichier affichant la méthode d’autorisation de rôle":::

2. <span data-ttu-id="41b60-244">Supprimez le paramètre qui n’est pas pertinent pour la méthode d’autorisation que vous avez choisie.</span><span class="sxs-lookup"><span data-stu-id="41b60-244">Remove the setting that isn't relevant for your chosen authorization method.</span></span>

#### <a name="tenant-and-key-settings"></a><span data-ttu-id="41b60-245">Paramètres de client et de clé</span><span class="sxs-lookup"><span data-stu-id="41b60-245">Tenant and key settings</span></span>

<span data-ttu-id="41b60-246">Les paramètres de client et de clé DKE se trouvent dans le fichier **appsettings.js** et le fichier **Startup.cs** .</span><span class="sxs-lookup"><span data-stu-id="41b60-246">DKE tenant and key settings are located in the **appsettings.json** file and the **startup.cs** file.</span></span>

<span data-ttu-id="41b60-247">Dans le fichier **appsettings.js** , modifiez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="41b60-247">In the **appsettings.json** file, modify the following values:</span></span>

- <span data-ttu-id="41b60-248">**ValidIssuers**.</span><span class="sxs-lookup"><span data-stu-id="41b60-248">**ValidIssuers**.</span></span> <span data-ttu-id="41b60-249">Remplacez `<tenantid>` par le GUID de votre client.</span><span class="sxs-lookup"><span data-stu-id="41b60-249">Replace `<tenantid>` with your tenant GUID.</span></span>
- <span data-ttu-id="41b60-250">**JwtAudience**.</span><span class="sxs-lookup"><span data-stu-id="41b60-250">**JwtAudience**.</span></span> <span data-ttu-id="41b60-251">Remplacez `<yourhostname>` par le nom d’hôte de l’ordinateur sur lequel le service DKE s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="41b60-251">Replace `<yourhostname>` with the hostname of the machine where the DKE service will run.</span></span>

  > [!IMPORTANT]
  > <span data-ttu-id="41b60-252">La valeur de JwtAudience doit correspondre *exactement*au nom de votre hôte.</span><span class="sxs-lookup"><span data-stu-id="41b60-252">The value for JwtAudience must match the name of your host *exactly*.</span></span> <span data-ttu-id="41b60-253">Vous pouvez utiliser **localhost : 5000** lors du débogage.</span><span class="sxs-lookup"><span data-stu-id="41b60-253">You may use **localhost:5000** while debugging.</span></span> <span data-ttu-id="41b60-254">Toutefois, lorsque vous avez fini de déboguer, veillez à mettre à jour cette valeur sur le nom d’hôte du serveur.</span><span class="sxs-lookup"><span data-stu-id="41b60-254">However, When you're done debugging, make sure to update this value to the server's hostname.</span></span>

- <span data-ttu-id="41b60-255">**LDAPPath**.</span><span class="sxs-lookup"><span data-stu-id="41b60-255">**LDAPPath**.</span></span> <span data-ttu-id="41b60-256">Définissez la valeur comme suit :</span><span class="sxs-lookup"><span data-stu-id="41b60-256">Set the value as follows:</span></span>

  - <span data-ttu-id="41b60-257">Si vous utilisez l’autorisation de rôle, entrez le domaine LDAP.</span><span class="sxs-lookup"><span data-stu-id="41b60-257">If you're using role authorization, enter the LDAP domain.</span></span>
  - <span data-ttu-id="41b60-258">Si vous utilisez l’autorisation de messagerie, laissez cette valeur vide.</span><span class="sxs-lookup"><span data-stu-id="41b60-258">If you're using email authorization, leave this value empty.</span></span>

   <span data-ttu-id="41b60-259">Pour plus d’informations, consultez la rubrique [Key Access Settings](#key-access-settings).</span><span class="sxs-lookup"><span data-stu-id="41b60-259">For more information, see [Key access settings](#key-access-settings).</span></span>

- <span data-ttu-id="41b60-260">**TestKeys : nom**.</span><span class="sxs-lookup"><span data-stu-id="41b60-260">**TestKeys:Name**.</span></span> <span data-ttu-id="41b60-261">Entrez un nom pour votre clé.</span><span class="sxs-lookup"><span data-stu-id="41b60-261">Enter a name for your key.</span></span> <span data-ttu-id="41b60-262">Exemple : **TestKey1**</span><span class="sxs-lookup"><span data-stu-id="41b60-262">Example: **TestKey1**</span></span>
- <span data-ttu-id="41b60-263">**TestKeys : ID**. Créez un GUID et entrez-le en tant que valeur **TestKeys : ID** .</span><span class="sxs-lookup"><span data-stu-id="41b60-263">**TestKeys:Id**. Create a GUID and enter it as the **TestKeys:ID** value.</span></span> <span data-ttu-id="41b60-264">Par exemple, **DCE1CC21-FF9B-4424-8FF4-9914BD19A1BE**.</span><span class="sxs-lookup"><span data-stu-id="41b60-264">For example, **DCE1CC21-FF9B-4424-8FF4-9914BD19A1BE**.</span></span> <span data-ttu-id="41b60-265">Vous pouvez utiliser un site comme le [Générateur de GUID en ligne](https://guidgenerator.com/) pour générer un GUID de manière aléatoire.</span><span class="sxs-lookup"><span data-stu-id="41b60-265">You can use a site like [Online GUID Generator](https://guidgenerator.com/) to randomly generate a GUID.</span></span>

### <a name="generate-test-keys"></a><span data-ttu-id="41b60-266">Générer des clés de test</span><span class="sxs-lookup"><span data-stu-id="41b60-266">Generate test keys</span></span>

<span data-ttu-id="41b60-267">Une fois que vous avez défini les paramètres de votre application, vous êtes prêt à générer des clés de test publiques et privées.</span><span class="sxs-lookup"><span data-stu-id="41b60-267">Once you have your application settings defined, you're ready to generate public and private test keys.</span></span>

<span data-ttu-id="41b60-268">Pour générer des clés :</span><span class="sxs-lookup"><span data-stu-id="41b60-268">To generate keys:</span></span>

1. <span data-ttu-id="41b60-269">Dans le menu Démarrer de Windows, exécutez l’invite de commandes OpenSSL.</span><span class="sxs-lookup"><span data-stu-id="41b60-269">From the Windows Start menu, run the OpenSSL Command Prompt.</span></span>

1. <span data-ttu-id="41b60-270">Accédez au dossier dans lequel vous souhaitez enregistrer les clés de test.</span><span class="sxs-lookup"><span data-stu-id="41b60-270">Change to the folder where you want to save the test keys.</span></span> <span data-ttu-id="41b60-271">Les fichiers que vous créez en suivant les étapes de cette tâche sont stockés dans le même dossier.</span><span class="sxs-lookup"><span data-stu-id="41b60-271">The files you create by completing the steps in this task are stored in the same folder.</span></span>

1. <span data-ttu-id="41b60-272">Générez la nouvelle clé de test.</span><span class="sxs-lookup"><span data-stu-id="41b60-272">Generate the new test key.</span></span>

   ```dos
   openssl req -x509 -newkey rsa:2048 -keyout key.pem -out cert.pem -days 365
   ```

2. <span data-ttu-id="41b60-273">Générez la clé privée.</span><span class="sxs-lookup"><span data-stu-id="41b60-273">Generate the private key.</span></span>

   ```dos
   openssl rsa -in key.pem -out privkeynopass.pem
   ```

1. <span data-ttu-id="41b60-274">Générez la clé publique.</span><span class="sxs-lookup"><span data-stu-id="41b60-274">Generate the public key.</span></span>

   ```dos
   openssl rsa -in key.pem -pubout > pubkeyonly.pem
   ```

1. <span data-ttu-id="41b60-275">Dans un éditeur de texte, ouvrez **pubkeyonly. pem**.</span><span class="sxs-lookup"><span data-stu-id="41b60-275">In a text editor, open **pubkeyonly.pem**.</span></span> <span data-ttu-id="41b60-276">Copiez tout le contenu du fichier **pubkeyonly. pem** , à l’exception de la première et de la dernière ligne, dans la section **PublicPem** du fichier **appsettings.js** .</span><span class="sxs-lookup"><span data-stu-id="41b60-276">Copy all of the content in the **pubkeyonly.pem** file, except the first and last lines, into the **PublicPem** section of the **appsettings.json** file.</span></span>

1. <span data-ttu-id="41b60-277">Dans un éditeur de texte, ouvrez **privkeynopass. pem**.</span><span class="sxs-lookup"><span data-stu-id="41b60-277">In a text editor, open **privkeynopass.pem**.</span></span> <span data-ttu-id="41b60-278">Copiez tout le contenu du fichier **privkeynopass. pem** , à l’exception de la première et de la dernière ligne, dans la section **PrivatePem** du fichier **appsettings.js** .</span><span class="sxs-lookup"><span data-stu-id="41b60-278">Copy all of the content in the **privkeynopass.pem** file, except the first and last lines, into the **PrivatePem** section of the **appsettings.json** file.</span></span>

1. <span data-ttu-id="41b60-279">Supprimez tous les espaces et lignes de nouvelle ligne dans les sections **PublicPem** et **PrivatePem** .</span><span class="sxs-lookup"><span data-stu-id="41b60-279">Remove all blank spaces and newlines in both the **PublicPem** and **PrivatePem** sections.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="41b60-280">Lorsque vous copiez ce contenu, ne supprimez pas les données du PEM.</span><span class="sxs-lookup"><span data-stu-id="41b60-280">When you copy this content, do not delete any of the PEM data.</span></span>

1. <span data-ttu-id="41b60-281">Ouvrez le fichier **Startup.cs** et recherchez les lignes suivantes :</span><span class="sxs-lookup"><span data-stu-id="41b60-281">Open the **Startup.cs** file, and locate the following lines:</span></span>

   ```c#
        #if USE_TEST_KEYS
        #error !!!!!!!!!!!!!!!!!!!!!! Use of test keys is only supported for testing,
        DO NOT USE  FOR PRODUCTION !!!!!!!!!!!!!!!!!!!!!!!!!!!!!
        services.AddSingleton<ippw.IKeyStore, ippw.TestKeyStore>();
        #endif
   ```

1. <span data-ttu-id="41b60-282">Remplacez ces lignes par le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="41b60-282">Replace these lines with the following text:</span></span>

   ```csharp
   services.AddSingleton<ippw.IKeyStore, ippw.TestKeyStore>();
   ```

   <span data-ttu-id="41b60-283">Les résultats finaux doivent ressembler à l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="41b60-283">The end results should look similar to the following picture.</span></span>

   :::image type="content" source="../media/dke-startupcs-usetestkeys.png" alt-text="fichier startup.cs pour la préversion publique":::

<span data-ttu-id="41b60-285">Vous êtes maintenant prêt à [créer votre projet DKE](#build-the-project).</span><span class="sxs-lookup"><span data-stu-id="41b60-285">Now you're ready to [build your DKE project](#build-the-project).</span></span>

### <a name="build-the-project"></a><span data-ttu-id="41b60-286">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="41b60-286">Build the project</span></span>

<span data-ttu-id="41b60-287">Suivez les instructions ci-dessous pour générer le projet DKE localement :</span><span class="sxs-lookup"><span data-stu-id="41b60-287">Use the following instructions to build the DKE project locally:</span></span>

1. <span data-ttu-id="41b60-288">Dans Visual Studio code, dans le référentiel du service DKE, sélectionnez **Afficher** la \> **palette de commandes** , puis tapez **générer** à l’invite.</span><span class="sxs-lookup"><span data-stu-id="41b60-288">In Visual Studio Code, in the DKE service repository, select **View** \> **Command Palette** and then type **build** at the prompt.</span></span>

1. <span data-ttu-id="41b60-289">Dans la liste, choisissez **tâches : exécuter la tâche de génération**.</span><span class="sxs-lookup"><span data-stu-id="41b60-289">From the list, choose **Tasks: Run build task**.</span></span>

   <span data-ttu-id="41b60-290">Si aucune tâche de génération n’a été trouvée, sélectionnez **configurer la tâche de génération** et créez-en une pour .net Core comme suit.</span><span class="sxs-lookup"><span data-stu-id="41b60-290">If there are no build tasks found, select **Configure Build Task** and create one for .NET core as follows.</span></span>

   :::image type="content" source="../media/dke-configurebuildtask.png" alt-text="Configurer une tâche de génération manquante pour .NET":::

   1. <span data-ttu-id="41b60-292">Choisissez **create tasks.json from template**.</span><span class="sxs-lookup"><span data-stu-id="41b60-292">Choose **Create tasks.json from template**.</span></span>

   :::image type="content" source="../media/dke-createtasksjsonfromtemplate.png" alt-text="Créer tasks.jssur le fichier à partir du modèle pour DKE":::

   2. <span data-ttu-id="41b60-294">Dans la liste des types de modèles, sélectionnez **.net Core**.</span><span class="sxs-lookup"><span data-stu-id="41b60-294">From the list of template types, select **.NET Core**.</span></span>

   :::image type="content" source="../media/dke-tasksjsontemplate.png" alt-text="Créer tasks.jssur le fichier à partir du modèle pour DKE":::

   3. <span data-ttu-id="41b60-296">Dans la section générer, recherchez le chemin d’accès au fichier **customerkeystore. csproj** .</span><span class="sxs-lookup"><span data-stu-id="41b60-296">In the build section, locate the path to the **customerkeystore.csproj** file.</span></span> <span data-ttu-id="41b60-297">Si ce n’est pas le cas, ajoutez la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="41b60-297">If it's not there, add the following line:</span></span>

      ```json
      "${workspaceFolder}/src/customer-key-store/customerkeystore.csproj",
      ```

  4. <span data-ttu-id="41b60-298">Exécutez de nouveau la génération.</span><span class="sxs-lookup"><span data-stu-id="41b60-298">Run the build again.</span></span>

1. <span data-ttu-id="41b60-299">Vérifiez qu’il n’y a pas d’erreurs rouges dans la fenêtre sortie.</span><span class="sxs-lookup"><span data-stu-id="41b60-299">Verify that there are no red errors in the output window.</span></span>

   <span data-ttu-id="41b60-300">S’il y a des erreurs rouges, vérifiez la sortie de la console.</span><span class="sxs-lookup"><span data-stu-id="41b60-300">If there are red errors, check the console output.</span></span> <span data-ttu-id="41b60-301">Assurez-vous que vous avez effectué toutes les étapes précédentes correctement et que les versions de build correctes sont présentes.</span><span class="sxs-lookup"><span data-stu-id="41b60-301">Ensure that you completed all the previous steps correctly and the correct build versions are present.</span></span>

1. <span data-ttu-id="41b60-302">**Exécuter** \> **Démarrez le débogage** pour déboguer le processus.</span><span class="sxs-lookup"><span data-stu-id="41b60-302">**Run** \> **Start Debugging** to debug the process.</span></span> <span data-ttu-id="41b60-303">Si vous êtes invité à sélectionner un environnement, sélectionnez **.net Core**.</span><span class="sxs-lookup"><span data-stu-id="41b60-303">If you're prompted to select an environment, select **.NET core**.</span></span>

<span data-ttu-id="41b60-304">Le débogueur .NET Core se lance généralement vers **https://localhost:5001** .</span><span class="sxs-lookup"><span data-stu-id="41b60-304">The .NET core debugger typically launches to **https://localhost:5001**.</span></span> <span data-ttu-id="41b60-305">Pour afficher votre clé de test, accédez à **https://localhost:5001** , puis ajoutez une barre oblique (/) et le nom de votre clé.</span><span class="sxs-lookup"><span data-stu-id="41b60-305">To view your test key, go to **https://localhost:5001**, and append a forward slash (/) and the name of your key.</span></span>

<span data-ttu-id="41b60-306">Par exemple :**https://localhost:5001/TestKey1**</span><span class="sxs-lookup"><span data-stu-id="41b60-306">For example: **https://localhost:5001/TestKey1**</span></span>

<span data-ttu-id="41b60-307">La clé doit s’afficher au format JSON.</span><span class="sxs-lookup"><span data-stu-id="41b60-307">The key should display in JSON format.</span></span>

<span data-ttu-id="41b60-308">Votre installation est maintenant terminée.</span><span class="sxs-lookup"><span data-stu-id="41b60-308">Your setup is now complete.</span></span> <span data-ttu-id="41b60-309">Avant de publier le keystore, dans appsettings.jsactivé, pour le paramètre JwtAudience, vérifiez que la valeur de hostname correspond exactement au nom de l’hôte de service de l’application.</span><span class="sxs-lookup"><span data-stu-id="41b60-309">Before you publish the keystore, in appsettings.json, for the JwtAudience setting, ensure the value for hostname exactly matches your App Service host name.</span></span> <span data-ttu-id="41b60-310">Vous pouvez l’avoir remplacée par localhost pour dépanner la Build.</span><span class="sxs-lookup"><span data-stu-id="41b60-310">You may have changed it to localhost to troubleshoot the build.</span></span>

### <a name="publish-the-key-store"></a><span data-ttu-id="41b60-311">Publier le magasin de clés</span><span class="sxs-lookup"><span data-stu-id="41b60-311">Publish the key store</span></span>

<span data-ttu-id="41b60-312">Les étapes suivantes décrivent comment créer une instance Azure App service pour héberger votre déploiement DKE, et comment publier vos clés générées sur Azure.</span><span class="sxs-lookup"><span data-stu-id="41b60-312">The following steps describe how to create an Azure App Service instance to host your DKE deployment, and how to publish your generated keys to Azure.</span></span>

<span data-ttu-id="41b60-313">Pour créer une instance Azure Web App afin d’héberger votre déploiement DKE, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="41b60-313">To create an Azure Web App instance to host your DKE deployment:</span></span>

1. <span data-ttu-id="41b60-314">Dans votre navigateur, connectez-vous au [portail Microsoft Azure](https://ms.portal.azure.com)et accédez à **app services**  >  **Add**.</span><span class="sxs-lookup"><span data-stu-id="41b60-314">In your browser, sign in to the [Microsoft Azure portal](https://ms.portal.azure.com), and go to **App Services** > **Add**.</span></span>

1. <span data-ttu-id="41b60-315">Sélectionnez votre abonnement et le groupe de ressources, puis définissez les détails de votre instance.</span><span class="sxs-lookup"><span data-stu-id="41b60-315">Select your subscription and resource group and define your instance details.</span></span>

    - <span data-ttu-id="41b60-316">Entrez le nom d’hôte de l’ordinateur sur lequel vous souhaitez installer le service DKE.</span><span class="sxs-lookup"><span data-stu-id="41b60-316">Enter the hostname of the computer where you want to install the DKE service.</span></span> <span data-ttu-id="41b60-317">Assurez-vous qu’il s’agit du même nom que celui défini pour le paramètre JwtAudience dans le fichier [**appsettings.js**](#tenant-and-key-settings) .</span><span class="sxs-lookup"><span data-stu-id="41b60-317">Make sure it's the same name as the one defined for the JwtAudience setting in the [**appsettings.json**](#tenant-and-key-settings) file.</span></span> <span data-ttu-id="41b60-318">La valeur que vous fournissez pour le nom est également WebAppInstanceName.</span><span class="sxs-lookup"><span data-stu-id="41b60-318">The value you provide for the name is also the WebAppInstanceName.</span></span>

    - <span data-ttu-id="41b60-319">Pour **publier**, sélectionner le **code**et pour la **pile Runtime**, sélectionnez **.net Core 3,1**.</span><span class="sxs-lookup"><span data-stu-id="41b60-319">For **Publish**, select **code**, and for **Runtime stack**, select **.NET Core 3.1**.</span></span>

    <span data-ttu-id="41b60-320">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="41b60-320">For example:</span></span>

    :::image type="content" source="../media/dke-azure-add-app-service.png" alt-text="Ajouter votre service d’application":::

1. <span data-ttu-id="41b60-322">Au bas de la page, sélectionnez **révision + créer**, puis **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="41b60-322">At the bottom of the page, select **Review + create**, and then select **Add**.</span></span>

1. <span data-ttu-id="41b60-323">Effectuez l’une des opérations suivantes pour publier vos clés générées dans Azure :</span><span class="sxs-lookup"><span data-stu-id="41b60-323">Do one of the following to publish your generated keys to Azure:</span></span>

    - [<span data-ttu-id="41b60-324">Publier via ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="41b60-324">Publish via ZipDeployUI</span></span>](#publish-via-zipdeployui)
    - [<span data-ttu-id="41b60-325">Publier via FTP</span><span class="sxs-lookup"><span data-stu-id="41b60-325">Publish via FTP</span></span>](#publish-via-ftp)
    - [<span data-ttu-id="41b60-326">Publier via Visual Studio 2019 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="41b60-326">Publish via Visual Studio 2019 or later</span></span>](https://docs.microsoft.com/aspnet/core/tutorials/)
    - [<span data-ttu-id="41b60-327">Publier sur un système local</span><span class="sxs-lookup"><span data-stu-id="41b60-327">Publish to an on-premises system</span></span>](https://docs.microsoft.com/aspnet/core/tutorials/publish-to-iis?view=aspnetcore-3.1&tabs=netcore-cli)

    > [!NOTE]
    > <span data-ttu-id="41b60-328">Vous pouvez préférer d’autres méthodes de déploiement de vos clés.</span><span class="sxs-lookup"><span data-stu-id="41b60-328">You may prefer other methods to deploy your keys.</span></span> <span data-ttu-id="41b60-329">Sélectionnez la méthode qui convient le mieux à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="41b60-329">Select the method that works best for your organization.</span></span>

    > [!TIP]
    > <span data-ttu-id="41b60-330">La [publication via Visual Studio](https://docs.microsoft.com/aspnet/core/tutorials/) et un [système local](https://docs.microsoft.com/aspnet/core/tutorials/publish-to-iis?view=aspnetcore-3.1&tabs=netcore-cli) est décrite dans la [documentation ASP.net](https://docs.microsoft.com/aspnet/core/).</span><span class="sxs-lookup"><span data-stu-id="41b60-330">[Publishing via Visual Studio](https://docs.microsoft.com/aspnet/core/tutorials/) and to an [on-premises system](https://docs.microsoft.com/aspnet/core/tutorials/publish-to-iis?view=aspnetcore-3.1&tabs=netcore-cli) is described in the [ASP .NET documentation](https://docs.microsoft.com/aspnet/core/).</span></span> <span data-ttu-id="41b60-331">Si vous utilisez l’une de ces méthodes, ouvrez les instructions dans un onglet distinct afin de pouvoir revenir rapidement une fois que vous avez fini.</span><span class="sxs-lookup"><span data-stu-id="41b60-331">If you use one of these methods, open the instructions in a separate tab so that you can return here easily when you're done.</span></span>

#### <a name="publish-via-zipdeployui"></a><span data-ttu-id="41b60-332">Publier via ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="41b60-332">Publish via ZipDeployUI</span></span>

1. <span data-ttu-id="41b60-333">Accédez à `https://<WebAppInstanceName>.scm.azurewebsites.net/ZipDeployUI`.</span><span class="sxs-lookup"><span data-stu-id="41b60-333">Go to `https://<WebAppInstanceName>.scm.azurewebsites.net/ZipDeployUI`.</span></span>

    <span data-ttu-id="41b60-334">Par exemple : https://customerkeystoreforpublicpreview.scm.azurewebsites.net/ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="41b60-334">For example: https://customerkeystoreforpublicpreview.scm.azurewebsites.net/ZipDeployUI</span></span>

1. <span data-ttu-id="41b60-335">Dans la base de code pour le magasin de clés, accédez au dossier **Customer-Key-store\src\customer-Key-Store** et vérifiez que ce dossier contient le fichier **customerkeystore. csproj** .</span><span class="sxs-lookup"><span data-stu-id="41b60-335">In the codebase for the key store, go to the **customer-key-store\src\customer-key-store** folder, and verify that this folder contains the **customerkeystore.csproj** file.</span></span>

1. <span data-ttu-id="41b60-336">Exécuter : **publication dotnet**</span><span class="sxs-lookup"><span data-stu-id="41b60-336">Run: **dotnet publish**</span></span>

     <span data-ttu-id="41b60-337">La fenêtre sortie affiche le répertoire dans lequel la publication a été déployée.</span><span class="sxs-lookup"><span data-stu-id="41b60-337">The output window displays the directory where the publish was deployed.</span></span>

    <span data-ttu-id="41b60-338">Par exemple : `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span><span class="sxs-lookup"><span data-stu-id="41b60-338">For example: `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span></span>

1. <span data-ttu-id="41b60-339">Envoyez tous les fichiers du répertoire de publication dans un fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="41b60-339">Send all files in the publish directory to a .zip file.</span></span> <span data-ttu-id="41b60-340">Lors de la création du fichier. zip, assurez-vous que tous les fichiers du répertoire sont au niveau racine du fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="41b60-340">When creating the .zip file, make sure that all files in the directory are at the root level of the .zip file.</span></span>

1. <span data-ttu-id="41b60-341">Faites glisser et déposez le fichier. zip que vous créez sur le site ZipDeployUI que vous avez ouvert ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="41b60-341">Drag and drop the .zip file you create to the ZipDeployUI site you opened above.</span></span> <span data-ttu-id="41b60-342">Par exemple : https://customerkeystoreforpublicpreview.scm.azurewebsites.net/ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="41b60-342">For example: https://customerkeystoreforpublicpreview.scm.azurewebsites.net/ZipDeployUI</span></span>

<span data-ttu-id="41b60-343">DKE est déployé et vous pouvez accéder aux clés de test que vous avez créées.</span><span class="sxs-lookup"><span data-stu-id="41b60-343">DKE is deployed and you can browse to the test keys you've created.</span></span> <span data-ttu-id="41b60-344">Poursuivez [la validation de votre déploiement](#validate-your-deployment) ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="41b60-344">Continue to [Validate your deployment](#validate-your-deployment) below.</span></span>

#### <a name="publish-via-ftp"></a><span data-ttu-id="41b60-345">Publier via FTP</span><span class="sxs-lookup"><span data-stu-id="41b60-345">Publish via FTP</span></span>

1. <span data-ttu-id="41b60-346">Connectez-vous au service d’application que vous avez créé [ci-dessus](#publish-the-key-store).</span><span class="sxs-lookup"><span data-stu-id="41b60-346">Connect to the App Service you created [above](#publish-the-key-store).</span></span>

    <span data-ttu-id="41b60-347">Dans votre navigateur, accédez à : **Azure portal**  >  **App Service**  >  **Centre de déploiement**de  >  **déploiement manuel**  >  **FTP**  >  **Dashboard**du centre de déploiement Azure Portal App.</span><span class="sxs-lookup"><span data-stu-id="41b60-347">In your browser, go to: **Azure portal** > **App Service** > **Deployment Center** > **Manual Deployment** > **FTP** > **Dashboard**.</span></span>

1. <span data-ttu-id="41b60-348">Copiez les chaînes de connexion affichées dans un fichier local.</span><span class="sxs-lookup"><span data-stu-id="41b60-348">Copy the connection strings displayed to a local file.</span></span> <span data-ttu-id="41b60-349">Vous utiliserez ces chaînes pour vous connecter au service d’application Web et télécharger des fichiers via FTP.</span><span class="sxs-lookup"><span data-stu-id="41b60-349">You'll use these strings to connect to the Web App Service and upload files via FTP.</span></span>

    <span data-ttu-id="41b60-350">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="41b60-350">For example:</span></span>

    :::image type="content" source="../media/dke-ftp-dashboard.png" alt-text="Copier des chaînes de connexion à partir du tableau de bord FTP":::

1. <span data-ttu-id="41b60-352">Dans la base de code pour le stockage de clés, accédez au **répertoire Customer-Key-store\src\customer-Key-Store**</span><span class="sxs-lookup"><span data-stu-id="41b60-352">In the codebase for the key storage, go to the **customer-key-store\src\customer-key-store directory**.</span></span>

1. <span data-ttu-id="41b60-353">Vérifiez que ce répertoire contient le fichier **customerkeystore. csproj** .</span><span class="sxs-lookup"><span data-stu-id="41b60-353">Verify that this directory contains the **customerkeystore.csproj** file.</span></span>

1. <span data-ttu-id="41b60-354">Exécuter : **publication dotnet**</span><span class="sxs-lookup"><span data-stu-id="41b60-354">Run: **dotnet publish**</span></span>

    <span data-ttu-id="41b60-355">La sortie contient le répertoire dans lequel la publication a été déployée.</span><span class="sxs-lookup"><span data-stu-id="41b60-355">The output contains the directory where the publish was deployed.</span></span>

    <span data-ttu-id="41b60-356">Par exemple : `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span><span class="sxs-lookup"><span data-stu-id="41b60-356">For example: `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span></span>

1. <span data-ttu-id="41b60-357">Envoyez tous les fichiers du répertoire de publication dans un fichier zip.</span><span class="sxs-lookup"><span data-stu-id="41b60-357">Send all files in the publish directory to a zip file.</span></span> <span data-ttu-id="41b60-358">Lors de la création du fichier. zip, assurez-vous que tous les fichiers du répertoire sont au niveau racine du fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="41b60-358">When creating the .zip file, make sure that all files in the directory are at the root level of the .zip file.</span></span>

1. <span data-ttu-id="41b60-359">À partir de votre client FTP, utilisez les informations de connexion que vous avez copiées pour vous connecter à votre service d’application.</span><span class="sxs-lookup"><span data-stu-id="41b60-359">From your FTP client, use the connection information you copied to connect to your App Service.</span></span> <span data-ttu-id="41b60-360">Téléchargez le fichier. zip que vous avez créé à l’étape précédente dans le répertoire racine de votre application Web.</span><span class="sxs-lookup"><span data-stu-id="41b60-360">Upload the .zip file you created in the previous step to the root directory of your Web App.</span></span>

<span data-ttu-id="41b60-361">DKE est déployé et vous pouvez accéder aux clés de test que vous auriez créées.</span><span class="sxs-lookup"><span data-stu-id="41b60-361">DKE is deployed and you can browse to the test keys you'd created.</span></span> <span data-ttu-id="41b60-362">Ensuite, [validez votre déploiement](#validate-your-deployment).</span><span class="sxs-lookup"><span data-stu-id="41b60-362">Next, [Validate your deployment](#validate-your-deployment).</span></span>

### <a name="validate-your-deployment"></a><span data-ttu-id="41b60-363">Valider votre déploiement</span><span class="sxs-lookup"><span data-stu-id="41b60-363">Validate your deployment</span></span>

<span data-ttu-id="41b60-364">Après avoir déployé DKE à l’aide de l’une des méthodes décrites ci-dessus, validez les principaux paramètres de déploiement et de magasin de clés.</span><span class="sxs-lookup"><span data-stu-id="41b60-364">After deploying DKE using one of the methods described above, validate the deployment and the key store settings.</span></span>

<span data-ttu-id="41b60-365">Générer</span><span class="sxs-lookup"><span data-stu-id="41b60-365">Run:</span></span>

<span data-ttu-id="41b60-366">src\customer-key-store\scripts\key_store_tester.ps1 mykeystoreurl/MyKey</span><span class="sxs-lookup"><span data-stu-id="41b60-366">src\customer-key-store\scripts\key_store_tester.ps1 mykeystoreurl/mykey</span></span>

<span data-ttu-id="41b60-367">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="41b60-367">For example:</span></span>

<span data-ttu-id="41b60-368">key_store_tester.ps1https://mycustomerkeystore.com/mykey</span><span class="sxs-lookup"><span data-stu-id="41b60-368">key_store_tester.ps1 https://mycustomerkeystore.com/mykey</span></span>

<span data-ttu-id="41b60-369">Assurez-vous qu’aucune erreur ne s’affiche dans la sortie.</span><span class="sxs-lookup"><span data-stu-id="41b60-369">Ensure that no errors appear in the output.</span></span> <span data-ttu-id="41b60-370">Lorsque vous êtes prêt, [Enregistrez votre magasin de clés](#register-your-key-store).</span><span class="sxs-lookup"><span data-stu-id="41b60-370">When you're ready, [register your key store](#register-your-key-store).</span></span>

## <a name="register-your-key-store"></a><span data-ttu-id="41b60-371">Enregistrer votre magasin de clés</span><span class="sxs-lookup"><span data-stu-id="41b60-371">Register your key store</span></span>

<span data-ttu-id="41b60-372">Les étapes suivantes vous permettent d’enregistrer votre magasin de clés.</span><span class="sxs-lookup"><span data-stu-id="41b60-372">The following steps enable you to register your key store.</span></span> <span data-ttu-id="41b60-373">L’inscription de votre magasin de clés est la dernière étape du déploiement d’DKE avant de commencer à créer des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="41b60-373">Registering your key store is the last step in deploying DKE before you can start creating labels.</span></span>

<span data-ttu-id="41b60-374">Pour enregistrer votre magasin de clés :</span><span class="sxs-lookup"><span data-stu-id="41b60-374">To register your key store:</span></span>

1. <span data-ttu-id="41b60-375">Dans votre navigateur, ouvrez le [portail Microsoft Azure](https://ms.portal.azure.com/), puis accédez à **toutes les** \> **Identity** \> **inscriptions des applications d'** identité des services.</span><span class="sxs-lookup"><span data-stu-id="41b60-375">In your browser, open the [Microsoft Azure portal](https://ms.portal.azure.com/), and go to **All Services** \> **Identity** \> **App Registrations**.</span></span>

2. <span data-ttu-id="41b60-376">Sélectionnez **nouvelle inscription**, puis entrez un nom explicite.</span><span class="sxs-lookup"><span data-stu-id="41b60-376">Select **New registration**, and enter a meaningful name.</span></span>

3. <span data-ttu-id="41b60-377">Sélectionnez un type de compte parmi les options affichées.</span><span class="sxs-lookup"><span data-stu-id="41b60-377">Select an account type from the options displayed.</span></span>

    <span data-ttu-id="41b60-378">Si vous utilisez Microsoft Azure avec un domaine non personnalisé, tel que **onmicrosoft.com**, sélectionnez **comptes dans cet annuaire d’organisation uniquement (Microsoft uniquement-client unique).**</span><span class="sxs-lookup"><span data-stu-id="41b60-378">If you're using Microsoft Azure with a non-custom domain, such as **onmicrosoft.com**, select **Accounts in this organizational directory only (Microsoft only - Single tenant).**</span></span>

    <span data-ttu-id="41b60-379">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="41b60-379">For example:</span></span>

    :::image type="content" source="../media/dke-app-registration.png" alt-text="Inscription de l’application":::

4. <span data-ttu-id="41b60-381">Au bas de la page, sélectionnez **Enregistrer** pour créer la nouvelle inscription de l’application.</span><span class="sxs-lookup"><span data-stu-id="41b60-381">At the bottom of the page, select **Register** to create the new App Registration.</span></span>

5. <span data-ttu-id="41b60-382">Dans la nouvelle inscription de l’application, dans le volet gauche, sous **gérer**, sélectionnez **authentification**.</span><span class="sxs-lookup"><span data-stu-id="41b60-382">In your new App Registration, in the left pane, under **Manage**, select **Authentication**.</span></span>

6. <span data-ttu-id="41b60-383">Sélectionnez **Ajouter une plateforme**.</span><span class="sxs-lookup"><span data-stu-id="41b60-383">Select **Add a platform**.</span></span>
 
7. <span data-ttu-id="41b60-384">Dans le menu **configure plateformes** , sélectionnez **Web**.</span><span class="sxs-lookup"><span data-stu-id="41b60-384">On the **Configure platforms** popup select **Web**.</span></span>
 
8. <span data-ttu-id="41b60-385">Sous **URI de redirection** , entrez l’URI de votre service de chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="41b60-385">Under **Redirect URIs** enter the URI of your double key encryption service.</span></span> <span data-ttu-id="41b60-386">Entrez l’URL du service d’application, y compris le nom d’hôte et le domaine.</span><span class="sxs-lookup"><span data-stu-id="41b60-386">Enter the App Service URL, including both the hostname and domain.</span></span>

    <span data-ttu-id="41b60-387">Par exemple : https://mycustomerkeystoretest.com</span><span class="sxs-lookup"><span data-stu-id="41b60-387">For example: https://mycustomerkeystoretest.com</span></span>

    - <span data-ttu-id="41b60-388">L’URL que vous entrez doit correspondre au nom d’hôte dans lequel votre magasin de clés est déployé.</span><span class="sxs-lookup"><span data-stu-id="41b60-388">The URL you enter must match the hostname where your key store is deployed.</span></span>
    - <span data-ttu-id="41b60-389">Si vous testez localement avec Visual Studio, utilisez **https://localhost:5001** .</span><span class="sxs-lookup"><span data-stu-id="41b60-389">If you're testing locally with Visual Studio, use **https://localhost:5001**.</span></span>
    - <span data-ttu-id="41b60-390">Dans tous les cas, le modèle doit être **https**.</span><span class="sxs-lookup"><span data-stu-id="41b60-390">In all cases, the scheme must be **https**.</span></span>

    <span data-ttu-id="41b60-391">Vérifiez que le nom d’hôte correspond exactement au nom de l’hôte de service de l’application.</span><span class="sxs-lookup"><span data-stu-id="41b60-391">Ensure the hostname exactly matches your App Service host name.</span></span> <span data-ttu-id="41b60-392">Vous pouvez l’avoir remplacée par localhost pour dépanner la Build.</span><span class="sxs-lookup"><span data-stu-id="41b60-392">You may have changed it to localhost to troubleshoot the build.</span></span> <span data-ttu-id="41b60-393">Dans appsettings.jsactivé, il s’agit du nom d’hôte que vous avez identifié comme valeur pour le paramètre JwtAudience.</span><span class="sxs-lookup"><span data-stu-id="41b60-393">In appsettings.json, this is the hostname you identified as the value for the JwtAudience setting.</span></span>

6. <span data-ttu-id="41b60-394">Sous **attribution implicite**, activez la case à cocher **jetons d’ID** .</span><span class="sxs-lookup"><span data-stu-id="41b60-394">Under **Implicit grant**, select the **ID tokens** checkbox.</span></span>

1. <span data-ttu-id="41b60-395">Sélectionnez **Enregistrer** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="41b60-395">Select **Save** to save your changes.</span></span>

7. <span data-ttu-id="41b60-396">Dans le volet de gauche, sélectionnez **exposer une API**, puis en regard de l’ID d’application URI, sélectionnez **Set**.</span><span class="sxs-lookup"><span data-stu-id="41b60-396">On the left pane, select **Expose an API**, then next to Application ID URI, select **Set**.</span></span>

9. <span data-ttu-id="41b60-397">Toujours sur la page **exposer une API** , dans la zone **étendues définies par cette API** , sélectionnez **Ajouter une étendue**.</span><span class="sxs-lookup"><span data-stu-id="41b60-397">Still on the **Expose an API** page, in the **Scopes defined by this API** area, select **Add a scope**.</span></span> <span data-ttu-id="41b60-398">Dans la nouvelle étendue :</span><span class="sxs-lookup"><span data-stu-id="41b60-398">In the new scope:</span></span>

    1. <span data-ttu-id="41b60-399">Définissez le nom de l’étendue en tant que **user_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="41b60-399">Define the scope name as **user_impersonation**.</span></span>

    2. <span data-ttu-id="41b60-400">Sélectionnez les administrateurs et les utilisateurs qui peuvent consentir.</span><span class="sxs-lookup"><span data-stu-id="41b60-400">Select the administrators and users who can consent.</span></span>

    3. <span data-ttu-id="41b60-401">Définissez les valeurs restantes requises.</span><span class="sxs-lookup"><span data-stu-id="41b60-401">Define any remaining values required.</span></span>

    4. <span data-ttu-id="41b60-402">Sélectionnez **Ajouter une étendue.**</span><span class="sxs-lookup"><span data-stu-id="41b60-402">Select **Add scope.**</span></span>

    <span data-ttu-id="41b60-403">Sélectionnez **Enregistrer** dans la partie supérieure pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="41b60-403">Select **Save** at the top to save your changes.</span></span>

10. <span data-ttu-id="41b60-404">Toujours sur la page **exposer une API** , dans la zone **applications clientes autorisées** , sélectionnez **Ajouter une application cliente**.</span><span class="sxs-lookup"><span data-stu-id="41b60-404">Still on the **Expose an API** page, in the **Authorized client applications** area, select **Add a client application**.</span></span>

    <span data-ttu-id="41b60-405">Dans la nouvelle application cliente :</span><span class="sxs-lookup"><span data-stu-id="41b60-405">In the new client application:</span></span>

    1. <span data-ttu-id="41b60-406">Définissez l’ID client comme **d3590ed6-52b3-4102-Aeff-aad2292ab01c**.</span><span class="sxs-lookup"><span data-stu-id="41b60-406">Define the Client ID as **d3590ed6-52b3-4102-aeff-aad2292ab01c**.</span></span> <span data-ttu-id="41b60-407">Cette valeur est l’ID client Microsoft Office et permet à Office d’obtenir un jeton d’accès pour votre magasin de clés.</span><span class="sxs-lookup"><span data-stu-id="41b60-407">This value is the Microsoft Office client ID, and enables Office to obtain an access token for your key store.</span></span>

    2. <span data-ttu-id="41b60-408">Sous **étendues autorisées**, sélectionnez l’étendue **user_impersonation** .</span><span class="sxs-lookup"><span data-stu-id="41b60-408">Under **Authorized scopes**, select the **user_impersonation** scope.</span></span>

    3. <span data-ttu-id="41b60-409">Sélectionnez **Ajouter une application**.</span><span class="sxs-lookup"><span data-stu-id="41b60-409">Select **Add application**.</span></span>

    4. <span data-ttu-id="41b60-410">Sélectionnez **Enregistrer** dans la partie supérieure pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="41b60-410">Select **Save** at the top to save your changes.</span></span>

<span data-ttu-id="41b60-411">Votre magasin de clés DKE est maintenant enregistré.</span><span class="sxs-lookup"><span data-stu-id="41b60-411">Your DKE key store is now registered.</span></span> <span data-ttu-id="41b60-412">Continuez en [créant des étiquettes à l’aide de DKE](#create-labels-using-dke).</span><span class="sxs-lookup"><span data-stu-id="41b60-412">Continue  by [creating labels using DKE](#create-labels-using-dke).</span></span>

## <a name="create-labels-using-dke"></a><span data-ttu-id="41b60-413">Créer des étiquettes à l’aide de DKE</span><span class="sxs-lookup"><span data-stu-id="41b60-413">Create labels using DKE</span></span>

<span data-ttu-id="41b60-414">Une fois que vous avez enregistré votre magasin de clés, configurez les étiquettes de confidentialité dans le centre de conformité Microsoft 365 et appliquez le chiffrement à double clé à ces étiquettes.</span><span class="sxs-lookup"><span data-stu-id="41b60-414">Once you've registered your key store, set up sensitivity labels in the Microsoft 365 compliance center and apply double key encryption to those labels.</span></span>

<span data-ttu-id="41b60-415">Dans l’interface utilisateur de création d’étiquette, sélectionnez l’option **utiliser le chiffrement à double clé** et entrez l’URL du point de terminaison de votre clé.</span><span class="sxs-lookup"><span data-stu-id="41b60-415">In the label creation UI, select the **Use Double Key Encryption** option and enter the endpoint URL for your key.</span></span>

<span data-ttu-id="41b60-416">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="41b60-416">For example:</span></span>

:::image type="content" source="../media/dke-use-dke.png" alt-text="Sélectionnez utiliser le chiffrement à double clé dans le centre de conformité Microsoft 365":::

<span data-ttu-id="41b60-418">Toutes les étiquettes DKE que vous ajoutez commencent à apparaître pour les utilisateurs dans les versions les plus récentes des applications Microsoft 365 pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="41b60-418">Any DKE labels you add will start appearing for users in the latest versions of Microsoft 365 Apps for enterprise.</span></span>

> [!NOTE]
> <span data-ttu-id="41b60-419">L’actualisation des clients avec les nouvelles étiquettes peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="41b60-419">It may take up to 24 hours for the clients to refresh with the new labels.</span></span>

### <a name="enable-dke-in-your-client"></a><span data-ttu-id="41b60-420">Activer DKE dans votre client</span><span class="sxs-lookup"><span data-stu-id="41b60-420">Enable DKE in your client</span></span>

<span data-ttu-id="41b60-421">Si vos étiquettes DKE n’apparaissent pas sous le ruban de sensibilité dans Microsoft Office, il se peut que DKE ne soit pas activé pour votre client.</span><span class="sxs-lookup"><span data-stu-id="41b60-421">If your DKE labels don't appear under the Sensitivity ribbon in Microsoft Office, your client may not have DKE enabled.</span></span>

<span data-ttu-id="41b60-422">Activez DKE pour votre client en ajoutant les clés de Registre suivantes :</span><span class="sxs-lookup"><span data-stu-id="41b60-422">Enable DKE for your client by adding the following registry keys:</span></span>

```ini
    [HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\MSIPC\flighting]
    "DoubleKeyProtection"=dword:00000001

    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\flighting]
    "DoubleKeyProtection"=dword:00000001
```

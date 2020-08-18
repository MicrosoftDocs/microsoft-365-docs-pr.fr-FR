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
ms.openlocfilehash: f36eeeb1f228bff48088cbbf3241d6866d0b3a21
ms.sourcegitcommit: 234726a1795d984c4659da68f852d30a4dda5711
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/18/2020
ms.locfileid: "46794163"
---
# <a name="double-key-encryption-dke"></a><span data-ttu-id="40789-103">Chiffrement à double clé (DKE)</span><span class="sxs-lookup"><span data-stu-id="40789-103">Double Key Encryption (DKE)</span></span>

> <span data-ttu-id="40789-104">*S’applique à : double Key chiffrement pour la version préliminaire publique de Microsoft 365, [conformité microsoft 365](https://www.microsoft.com/microsoft-365/business/compliance-management), [Azure information protection](https://azure.microsoft.com/pricing/details/information-protection)*</span><span class="sxs-lookup"><span data-stu-id="40789-104">*Applies to: Double Key Encryption for Microsoft 365 public preview, [Microsoft 365 Compliance](https://www.microsoft.com/microsoft-365/business/compliance-management), [Azure Information Protection](https://azure.microsoft.com/pricing/details/information-protection)*</span></span>
>
> <span data-ttu-id="40789-105">*Instructions pour : [client d’étiquetage unifié Azure information protection pour Windows](https://docs.microsoft.com/azure/information-protection/faqs#whats-the-difference-between-the-azure-information-protection-classic-and-unified-labeling-clients)*</span><span class="sxs-lookup"><span data-stu-id="40789-105">*Instructions for: [Azure Information Protection unified labeling client for Windows](https://docs.microsoft.com/azure/information-protection/faqs#whats-the-difference-between-the-azure-information-protection-classic-and-unified-labeling-clients)*</span></span>
>
> <span data-ttu-id="40789-106">*Description du service : [conformité Microsoft 365](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance)*</span><span class="sxs-lookup"><span data-stu-id="40789-106">*Service description for: [Microsoft 365 Compliance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance)*</span></span>

<span data-ttu-id="40789-107">Le chiffrement à clé double (DKE) utilise deux clés ensemble pour accéder au contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="40789-107">Double Key Encryption (DKE) uses two keys together to access protected content.</span></span> <span data-ttu-id="40789-108">Vous stockez une clé dans Microsoft Azure et vous la maintenez.</span><span class="sxs-lookup"><span data-stu-id="40789-108">You store one key in Microsoft Azure, and you hold the other key.</span></span> <span data-ttu-id="40789-109">Le client d’étiquetage unifié Azure information Protection protège le contenu hautement sensible tout en conservant le contrôle total de l’une de vos clés.</span><span class="sxs-lookup"><span data-stu-id="40789-109">The Azure Information Protection unified labeling client protects highly sensitive content while you maintain full control of one of your keys.</span></span>

<span data-ttu-id="40789-110">Le chiffrement à double clé prend en charge les déploiements sur le Cloud et sur site.</span><span class="sxs-lookup"><span data-stu-id="40789-110">Double Key Encryption supports both cloud and on-premises deployments.</span></span> <span data-ttu-id="40789-111">Ces déploiements permettent de s’assurer que les données chiffrées restent opaques, où que vous stockez les données protégées.</span><span class="sxs-lookup"><span data-stu-id="40789-111">These deployments help to ensure that encrypted data remains opaque wherever you store the protected data.</span></span>

<span data-ttu-id="40789-112">Pour plus d’informations sur les clés de racine de client par défaut, consultez la rubrique [planification et implémentation de votre clé de client Azure information protection](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key).</span><span class="sxs-lookup"><span data-stu-id="40789-112">For more information about the default, cloud-based tenant root keys, see [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key).</span></span>

<!--
The following video shows how Double Key Encryption works to secure your content.

> [!VIDEO https://msit.microsoftstream.com/embed/video/f466a1ff-0400-a936-221c-f1eab45dc756]
-->

<span data-ttu-id="40789-113">Si votre organisation dispose de l’une des conditions suivantes, vous pouvez utiliser DKE pour sécuriser votre contenu :</span><span class="sxs-lookup"><span data-stu-id="40789-113">If your organizations have any of the following requirements, you can use DKE to help secure your content:</span></span>

- <span data-ttu-id="40789-114">Vous souhaitez vous assurer que *vous* êtes le seul à pouvoir déchiffrer le contenu protégé, dans toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="40789-114">You want to ensure that *only you* can ever decrypt protected content, under all circumstances.</span></span>
- <span data-ttu-id="40789-115">Vous ne souhaitez pas que Microsoft ait accès aux données protégées de façon autonome.</span><span class="sxs-lookup"><span data-stu-id="40789-115">You don't want Microsoft to have access to protected data on its own.</span></span>
- <span data-ttu-id="40789-116">Vous avez des exigences réglementaires à maintenir des clés dans une limite géographique.</span><span class="sxs-lookup"><span data-stu-id="40789-116">You have regulatory requirements to hold keys within a geographical boundary.</span></span> <span data-ttu-id="40789-117">Toutes les clés que vous mettez en attente pour le chiffrement et le déchiffrement des données sont conservées dans votre centre de données.</span><span class="sxs-lookup"><span data-stu-id="40789-117">All of the keys that you hold for data encryption and decryption are maintained in your data center.</span></span>

## <a name="system-and-licensing-requirements-for-dke"></a><span data-ttu-id="40789-118">Exigences en matière de système et de licence pour DKE</span><span class="sxs-lookup"><span data-stu-id="40789-118">System and licensing requirements for DKE</span></span>

<span data-ttu-id="40789-119">Le chiffrement à double clé pour Microsoft 365 est fourni avec Microsoft 365 E5 et Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="40789-119">Double Key Encryption for Microsoft 365 comes with Microsoft 365 E5 and Office 365 E5.</span></span> <span data-ttu-id="40789-120">Si vous n’avez pas de licence Microsoft 365 E5, vous pouvez vous inscrire pour obtenir une [version d’évaluation](https://aka.ms/M365E5ComplianceTrial).</span><span class="sxs-lookup"><span data-stu-id="40789-120">If you don’t have a Microsoft 365 E5 license, you can sign up for a [trial](https://aka.ms/M365E5ComplianceTrial).</span></span> <span data-ttu-id="40789-121">Pour plus d’informations sur ces licences, consultez [la rubrique Microsoft 365 Licensing Guidance for security & Compliance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).</span><span class="sxs-lookup"><span data-stu-id="40789-121">For more information about these licenses, see [Microsoft 365 licensing guidance for security & compliance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).</span></span>

<span data-ttu-id="40789-122">**Office Insider** Pour utiliser la préversion publique, vous devez être membre du programme Office Insider.</span><span class="sxs-lookup"><span data-stu-id="40789-122">**Office Insider** To use the public preview, you must be a member of the Office Insider program.</span></span> <span data-ttu-id="40789-123">Pour rejoindre Office Insider, accédez à [https://insider.office.com](https://insider.office.com) .</span><span class="sxs-lookup"><span data-stu-id="40789-123">To join Office Insider, go to [https://insider.office.com](https://insider.office.com).</span></span> <span data-ttu-id="40789-124">Une fois que vous êtes membre, préparez votre environnement pour déployer les builds Office Insider en choisissant la méthode de déploiement appropriée pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="40789-124">Once you're a member, prepare your environment to deploy Office Insider builds by choosing the right deployment method for your organization.</span></span> <span data-ttu-id="40789-125">Pour obtenir des instructions, consultez la rubrique [prise en main du déploiement des builds Office Insider](https://insider.office.com/business/deploy).</span><span class="sxs-lookup"><span data-stu-id="40789-125">For instructions, see [Getting started on deploying Office Insider builds](https://insider.office.com/business/deploy).</span></span>

<span data-ttu-id="40789-126">**Azure information protection**.</span><span class="sxs-lookup"><span data-stu-id="40789-126">**Azure Information Protection**.</span></span> <span data-ttu-id="40789-127">DKE fonctionne avec les étiquettes de confidentialité et nécessite Azure information protection.</span><span class="sxs-lookup"><span data-stu-id="40789-127">DKE works with sensitivity labels and requires Azure Information Protection.</span></span>

## <a name="supported-environments-for-storing-and-viewing-dke-protected-content"></a><span data-ttu-id="40789-128">Environnements pris en charge pour le stockage et l’affichage du contenu protégé par DKE</span><span class="sxs-lookup"><span data-stu-id="40789-128">Supported environments for storing and viewing DKE-protected content</span></span>

<span data-ttu-id="40789-129">**Applications prises en charge**.</span><span class="sxs-lookup"><span data-stu-id="40789-129">**Supported applications**.</span></span> <span data-ttu-id="40789-130">[Applications Microsoft 365 pour](https://www.microsoft.com/microsoft-365/business/microsoft-365-apps-for-enterprise-product) les clients d’entreprise sur Windows, y compris Word, Excel et PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="40789-130">[Microsoft 365 Apps for enterprise](https://www.microsoft.com/microsoft-365/business/microsoft-365-apps-for-enterprise-product) clients on Windows, including Word, Excel, and PowerPoint.</span></span>

<span data-ttu-id="40789-131">**Prise en charge du contenu en ligne**.</span><span class="sxs-lookup"><span data-stu-id="40789-131">**Online content support**.</span></span> <span data-ttu-id="40789-132">Les documents et les fichiers stockés en ligne dans Microsoft SharePoint et OneDrive entreprise sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="40789-132">Documents and files stored online in both Microsoft SharePoint and OneDrive for Business are supported.</span></span> <span data-ttu-id="40789-133">Vous pouvez partager le contenu chiffré par courrier électronique, mais vous ne pouvez pas afficher les documents et fichiers chiffrés en ligne.</span><span class="sxs-lookup"><span data-stu-id="40789-133">You can share encrypted content by email, but you can't view encrypted documents and files online.</span></span> <span data-ttu-id="40789-134">Au lieu de cela, vous devez afficher le contenu protégé à l’aide des applications de bureau sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="40789-134">Instead, you must view protected content using the desktop apps on your local computer.</span></span>

## <a name="about-this-public-preview-article"></a><span data-ttu-id="40789-135">À propos de cet article d’aperçu public</span><span class="sxs-lookup"><span data-stu-id="40789-135">About this public preview article</span></span>

<span data-ttu-id="40789-136">Il existe plusieurs façons de procéder pour déployer le chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="40789-136">There are several ways you can complete some of the steps to deploy Double Key Encryption.</span></span> <span data-ttu-id="40789-137">Cet article fournit des instructions détaillées afin que les administrateurs moins expérimentés déploient correctement le service.</span><span class="sxs-lookup"><span data-stu-id="40789-137">This article provides detailed instructions so that less experienced admins successfully deploy the service.</span></span> <span data-ttu-id="40789-138">Si vous êtes familiarisé, vous pouvez choisir d’utiliser vos propres méthodes.</span><span class="sxs-lookup"><span data-stu-id="40789-138">If you're comfortable doing so, you can choose to use your own methods.</span></span>

<span data-ttu-id="40789-139">Cet article contient des instructions détaillées sur la façon de déployer le service de chiffrement à double clé sur Azure.</span><span class="sxs-lookup"><span data-stu-id="40789-139">This article includes step-by-step instructions on how to deploy the Double Key Encryption service to Azure.</span></span> <span data-ttu-id="40789-140">Ce scénario n’est pas très probable en production.</span><span class="sxs-lookup"><span data-stu-id="40789-140">This scenario isn't something you'd likely do in production.</span></span> <span data-ttu-id="40789-141">Pour la préversion publique, l’utilisation d’Azure est un moyen rapide de déployer DKE.</span><span class="sxs-lookup"><span data-stu-id="40789-141">For public preview, using Azure is a quick way to deploy DKE.</span></span> <span data-ttu-id="40789-142">Le déploiement vers Azure vous permet de commencer à utiliser le chiffrement à clé double immédiatement.</span><span class="sxs-lookup"><span data-stu-id="40789-142">Deploying to Azure lets you get started using Double Key Encryption right away.</span></span>

<span data-ttu-id="40789-143">Vous pouvez déployer le service localement sur votre réseau ou avec un autre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="40789-143">You can deploy the service locally on your network or with another provider.</span></span> <span data-ttu-id="40789-144">Vous devrez publier le magasin de clés à l’aide de méthodes appropriées pour cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="40789-144">You'll need to publish the key store using methods that are appropriate for that location.</span></span>

## <a name="deploy-double-key-encryption"></a><span data-ttu-id="40789-145">Déployer le chiffrement à double clé</span><span class="sxs-lookup"><span data-stu-id="40789-145">Deploy Double Key Encryption</span></span>

<span data-ttu-id="40789-146">Cet article et la vidéo de déploiement utilisent Azure comme destination de déploiement pour le service DKE.</span><span class="sxs-lookup"><span data-stu-id="40789-146">This article and the deployment video use Azure as the deployment destination for the DKE service.</span></span> <span data-ttu-id="40789-147">Si vous effectuez le déploiement vers un autre emplacement, vous devez fournir vos propres valeurs.</span><span class="sxs-lookup"><span data-stu-id="40789-147">If you're deploying to another location, you'll need to provide your own values.</span></span>

<span data-ttu-id="40789-148">Regardez la [vidéo sur le déploiement de chiffrement à double clé](https://youtu.be/vDWfHN_kygg) pour voir pas à pas la présentation des concepts de l’article.</span><span class="sxs-lookup"><span data-stu-id="40789-148">Watch the [Double Key Encryption deployment video](https://youtu.be/vDWfHN_kygg) to see step-by-step overview of concepts in the article.</span></span> <span data-ttu-id="40789-149">La vidéo prend environ 18 minutes.</span><span class="sxs-lookup"><span data-stu-id="40789-149">The video takes about 18 minutes to complete.</span></span>

<span data-ttu-id="40789-150">Suivez ces étapes générales pour configurer le chiffrement à double clé pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="40789-150">You'll follow these general steps to set up Double Key Encryption for your organization.</span></span>

1. [<span data-ttu-id="40789-151">Installer les composants logiciels requis</span><span class="sxs-lookup"><span data-stu-id="40789-151">Install software prerequisites</span></span>](#install-software-prerequisites)
1. [<span data-ttu-id="40789-152">Cloner le référentiel GitHub de chiffrement à double clé</span><span class="sxs-lookup"><span data-stu-id="40789-152">Clone the Double Key Encryption GitHub repository</span></span>](#clone-the-dke-github-repository)
1. [<span data-ttu-id="40789-153">Modifier les paramètres d’application</span><span class="sxs-lookup"><span data-stu-id="40789-153">Modify application settings</span></span>](#modify-application-settings)
1. [<span data-ttu-id="40789-154">Générer des clés de test</span><span class="sxs-lookup"><span data-stu-id="40789-154">Generate test keys</span></span>](#generate-test-keys)
1. [<span data-ttu-id="40789-155">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="40789-155">Build the project</span></span>](#build-the-project)
1. [<span data-ttu-id="40789-156">Publier le magasin de clés</span><span class="sxs-lookup"><span data-stu-id="40789-156">Publish the key store</span></span>](#publish-the-key-store)
1. [<span data-ttu-id="40789-157">Valider votre déploiement</span><span class="sxs-lookup"><span data-stu-id="40789-157">Validate your deployment</span></span>](#validate-your-deployment)
1. [<span data-ttu-id="40789-158">Enregistrer votre magasin de clés</span><span class="sxs-lookup"><span data-stu-id="40789-158">Register your key store</span></span>](#register-your-key-store)
1. [<span data-ttu-id="40789-159">Créer des étiquettes de sensibilité</span><span class="sxs-lookup"><span data-stu-id="40789-159">Create sensitivity labels</span></span>](#create-labels-using-dke)

<span data-ttu-id="40789-160">Lorsque vous avez fini, vous pouvez chiffrer des documents et des fichiers à l’aide de DKE.</span><span class="sxs-lookup"><span data-stu-id="40789-160">When you're done, you can encrypt documents and files using DKE.</span></span> <span data-ttu-id="40789-161">Pour plus d’informations, consultez [la rubrique appliquer des étiquettes de confidentialité à vos fichiers et à votre messagerie électronique dans Office](https://support.microsoft.com/office/2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9).</span><span class="sxs-lookup"><span data-stu-id="40789-161">For information, see [Apply sensitivity labels to your files and email in Office](https://support.microsoft.com/office/2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9).</span></span>

### <a name="install-software-prerequisites"></a><span data-ttu-id="40789-162">Installer les composants logiciels requis</span><span class="sxs-lookup"><span data-stu-id="40789-162">Install software prerequisites</span></span>

<span data-ttu-id="40789-163">Il existe deux types de logiciels requis pour le chiffrement à double clé</span><span class="sxs-lookup"><span data-stu-id="40789-163">There are two types of software prerequisites for Double Key Encryption</span></span>

- [<span data-ttu-id="40789-164">Conditions préalables requises pour le service de chiffrement à clé double</span><span class="sxs-lookup"><span data-stu-id="40789-164">Double Key Encryption service prerequisites</span></span>](#double-key-encryption-service-prerequisites)
- [<span data-ttu-id="40789-165">Conditions préalables au chiffrement à double clé pour les ordinateurs clients</span><span class="sxs-lookup"><span data-stu-id="40789-165">Double Key Encryption prerequisites for client computers</span></span>](#double-key-encryption-prerequisites-for-client-computers)

#### <a name="double-key-encryption-service-prerequisites"></a><span data-ttu-id="40789-166">Conditions préalables requises pour le service de chiffrement à clé double</span><span class="sxs-lookup"><span data-stu-id="40789-166">Double Key Encryption service prerequisites</span></span>

<span data-ttu-id="40789-167">Installez ces éléments prérequis sur l’ordinateur sur lequel vous souhaitez installer le service DKE.</span><span class="sxs-lookup"><span data-stu-id="40789-167">Install these prerequisites on the computer where you want to install the DKE service.</span></span>

<span data-ttu-id="40789-168">**.Net Core 3,1 SDK**.</span><span class="sxs-lookup"><span data-stu-id="40789-168">**.NET Core 3.1 SDK**.</span></span> <span data-ttu-id="40789-169">Téléchargez et installez le kit de développement logiciel (SDK) à partir de [Télécharger .net Core 3,1](https://dotnet.microsoft.com/download/dotnet-core/3.1).</span><span class="sxs-lookup"><span data-stu-id="40789-169">Download and install the SDK from [Download .NET Core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1).</span></span>

<span data-ttu-id="40789-170">**Visual Studio code**.</span><span class="sxs-lookup"><span data-stu-id="40789-170">**Visual Studio Code**.</span></span> <span data-ttu-id="40789-171">Téléchargez Visual Studio code à partir de [https://code.visualstudio.com/](https://code.visualstudio.com) .</span><span class="sxs-lookup"><span data-stu-id="40789-171">Download Visual Studio Code from [https://code.visualstudio.com/](https://code.visualstudio.com).</span></span> <span data-ttu-id="40789-172">Une fois installé, exécutez Visual Studio code et sélectionnez **Afficher** les \> **Extensions**.</span><span class="sxs-lookup"><span data-stu-id="40789-172">Once installed, run Visual Studio Code and select **View** \> **Extensions**.</span></span> <span data-ttu-id="40789-173">Installez ces extensions.</span><span class="sxs-lookup"><span data-stu-id="40789-173">Install these extensions.</span></span>

- <span data-ttu-id="40789-174">C# pour Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="40789-174">C# for Visual Studio Code</span></span>

- <span data-ttu-id="40789-175">Gestionnaire de package NuGet</span><span class="sxs-lookup"><span data-stu-id="40789-175">NuGet Package Manager</span></span>

<span data-ttu-id="40789-176">**Microsoft Office Insider**.</span><span class="sxs-lookup"><span data-stu-id="40789-176">**Microsoft Office Insider**.</span></span> <span data-ttu-id="40789-177">Configurez au moins une [méthode de déploiement](https://insider.office.com/business/deploy).</span><span class="sxs-lookup"><span data-stu-id="40789-177">Set up at least one [deployment method](https://insider.office.com/business/deploy).</span></span>

<span data-ttu-id="40789-178">**Ressources git**.</span><span class="sxs-lookup"><span data-stu-id="40789-178">**Git resources**.</span></span> <span data-ttu-id="40789-179">Téléchargez et installez l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="40789-179">Download and install one of the following.</span></span>

- [<span data-ttu-id="40789-180">Git</span><span class="sxs-lookup"><span data-stu-id="40789-180">Git</span></span>](https://git-scm.com/downloads)

- [<span data-ttu-id="40789-181">Bureau GitHub</span><span class="sxs-lookup"><span data-stu-id="40789-181">GitHub Desktop</span></span>](https://desktop.github.com/)

- [<span data-ttu-id="40789-182">GitHub entreprise</span><span class="sxs-lookup"><span data-stu-id="40789-182">GitHub Enterprise</span></span>](https://github.com/enterprise)

<span data-ttu-id="40789-183">**OpenSSL** [OpenSSL](https://slproweb.com/products/Win32OpenSSL.html) doit être installé pour [générer des clés de test](#generate-test-keys) une fois que vous avez déployé DKE.</span><span class="sxs-lookup"><span data-stu-id="40789-183">**OpenSSL** You must have [OpenSSL](https://slproweb.com/products/Win32OpenSSL.html) installed to [generate test keys](#generate-test-keys) after you deploy DKE.</span></span> <span data-ttu-id="40789-184">Vérifiez que vous l’appelez correctement à partir de votre chemin d’accès aux variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="40789-184">Make sure you're invoking it correctly from your environment variables path.</span></span> <span data-ttu-id="40789-185">Par exemple, pour plus d’informations, consultez la section « ajouter le répertoire d’installation au chemin d’accès » https://www.osradar.com/install-openssl-windows/ .</span><span class="sxs-lookup"><span data-stu-id="40789-185">For example, see "Add the installation directory to PATH" at https://www.osradar.com/install-openssl-windows/ for details.</span></span>

#### <a name="double-key-encryption-prerequisites-for-client-computers"></a><span data-ttu-id="40789-186">Conditions préalables au chiffrement à double clé pour les ordinateurs clients</span><span class="sxs-lookup"><span data-stu-id="40789-186">Double Key Encryption prerequisites for client computers</span></span>

<span data-ttu-id="40789-187">Installez ces éléments prérequis sur chaque ordinateur client sur lequel vous souhaitez protéger et consommer des documents protégés.</span><span class="sxs-lookup"><span data-stu-id="40789-187">Install these prerequisites on each client computer where you want to protect and consume protected documents.</span></span>

<span data-ttu-id="40789-188">**Microsoft Office** version \*. 12711 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="40789-188">**Microsoft Office** version \*.12711 or later.</span></span>

<span data-ttu-id="40789-189">Versions du **client d’étiquetage unifié Azure information protection** 2.7.93.0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="40789-189">**Azure Information Protection Unified Labeling Client** versions 2.7.93.0 or later.</span></span> <span data-ttu-id="40789-190">Téléchargez et installez le client d’étiquetage unifié de [Microsoft](https://www.microsoft.com/download/details.aspx?id=53018).</span><span class="sxs-lookup"><span data-stu-id="40789-190">Download and install the Unified Labeling client from [Microsoft](https://www.microsoft.com/download/details.aspx?id=53018).</span></span>

### <a name="clone-the-dke-github-repository"></a><span data-ttu-id="40789-191">Cloner le référentiel DKE GitHub</span><span class="sxs-lookup"><span data-stu-id="40789-191">Clone the DKE GitHub repository</span></span>

<span data-ttu-id="40789-192">Microsoft fournit les fichiers source DKE dans un référentiel GitHub.</span><span class="sxs-lookup"><span data-stu-id="40789-192">Microsoft supplies the DKE source files in a GitHub repository.</span></span> <span data-ttu-id="40789-193">Vous clonez le référentiel pour créer le projet localement pour l’utilisation de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="40789-193">You clone the repository to build the project locally for your organization's use.</span></span> <span data-ttu-id="40789-194">Le référentiel DKE GitHub se trouve à l’emplacement [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService) .</span><span class="sxs-lookup"><span data-stu-id="40789-194">The DKE GitHub repository is located at [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService).</span></span>

<span data-ttu-id="40789-195">Les instructions suivantes sont destinées aux utilisateurs de git ou de code Visual Studio inexpérimentés :</span><span class="sxs-lookup"><span data-stu-id="40789-195">The following instructions are intended for inexperienced git or Visual Studio Code users:</span></span>

1. <span data-ttu-id="40789-196">Dans votre navigateur, accédez à : [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService)</span><span class="sxs-lookup"><span data-stu-id="40789-196">In your browser, go to: [https://github.com/Azure-Samples/DoubleKeyEncryptionService](https://github.com/Azure-Samples/DoubleKeyEncryptionService)</span></span>

1. <span data-ttu-id="40789-197">Dans la partie droite de l’écran, sélectionnez **code**.</span><span class="sxs-lookup"><span data-stu-id="40789-197">Towards the right side of the screen, select **Code**.</span></span> <span data-ttu-id="40789-198">Votre version de l’interface utilisateur peut afficher un bouton **Clone ou télécharger** .</span><span class="sxs-lookup"><span data-stu-id="40789-198">Your version of the UI might show a **Clone or download** button.</span></span> <span data-ttu-id="40789-199">Ensuite, dans la liste déroulante qui apparaît, sélectionnez l’icône copier pour copier l’URL dans votre presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="40789-199">Then, in the dropdown that appears, select the copy icon to copy the URL to your clipboard.</span></span>

    <span data-ttu-id="40789-200">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40789-200">For example:</span></span>

   ![Cloner le référentiel du service de chiffrement à clé double à partir de GitHub](../media/dke-clone.png)

3. <span data-ttu-id="40789-202">Dans Visual Studio code, sélectionnez **Afficher** la \> **palette de commandes** et sélectionnez **git : Clone**.</span><span class="sxs-lookup"><span data-stu-id="40789-202">In Visual Studio Code, select **View** \> **Command Palette** and select **Git: Clone**.</span></span> <span data-ttu-id="40789-203">Pour accéder à l’option dans la liste, commencez `git: clone` à taper pour filtrer les entrées, puis sélectionnez-la dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="40789-203">To jump to the option in the list, start typing `git: clone` to filter the entries and then select it from the drop-down.</span></span> <span data-ttu-id="40789-204">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40789-204">For example:</span></span>

   ![Option GIT : clone de Visual Studio code](../media/dke-vscode-clone.png)

4. <span data-ttu-id="40789-206">Dans la zone de texte, collez l’URL que vous avez copiée à partir de git et sélectionnez **Clone dans GitHub**.</span><span class="sxs-lookup"><span data-stu-id="40789-206">In the text box, paste the URL that you copied from Git and select **Clone from GitHub**.</span></span>

5. <span data-ttu-id="40789-207">Dans la boîte de dialogue **Sélectionner un dossier** qui s’affiche, accédez à l’emplacement où vous souhaitez stocker le référentiel et sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="40789-207">In the **Select Folder** dialog that appears, browse to and select a location to store the repository.</span></span> <span data-ttu-id="40789-208">À l’invite, sélectionnez **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="40789-208">At the prompt, select **Open**.</span></span>

    <span data-ttu-id="40789-209">Le référentiel est ouvert dans Visual Studio code et affiche la branche git actuelle en bas à gauche.</span><span class="sxs-lookup"><span data-stu-id="40789-209">The repository is opened in Visual Studio Code, and displays the current Git branch at the bottom left.</span></span> <span data-ttu-id="40789-210">La branche doit être **Master**.</span><span class="sxs-lookup"><span data-stu-id="40789-210">The branch should be **master**.</span></span>

    <span data-ttu-id="40789-211">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40789-211">For example:</span></span>

   ![Branche Visual Studio code Master](../media/dke-vscode-master.png)

6. <span data-ttu-id="40789-213">Sélectionnez le masque de mots **,** puis sélectionnez **public_preview** dans la liste des branches.</span><span class="sxs-lookup"><span data-stu-id="40789-213">Select the word **master,** and then select **public_preview** from the list of branches.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="40789-214">La sélection de la branche public_preview vous permet de vous assurer que vous disposez des fichiers appropriés pour générer le projet.</span><span class="sxs-lookup"><span data-stu-id="40789-214">Selecting the public_preview branch ensures that you have the correct files to build the project.</span></span> <span data-ttu-id="40789-215">Si vous ne sélectionnez pas la branche appropriée, votre déploiement échouera.</span><span class="sxs-lookup"><span data-stu-id="40789-215">If you do not choose the correct branch your deployment will fail.</span></span>

<span data-ttu-id="40789-216">Votre référentiel source DKE est maintenant configuré localement.</span><span class="sxs-lookup"><span data-stu-id="40789-216">You now have your DKE source repository set up locally.</span></span> <span data-ttu-id="40789-217">Ensuite, [Modifiez les paramètres d’application](#modify-application-settings) pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="40789-217">Next, [modify application settings](#modify-application-settings) for your organization.</span></span>

### <a name="modify-application-settings"></a><span data-ttu-id="40789-218">Modifier les paramètres d’application</span><span class="sxs-lookup"><span data-stu-id="40789-218">Modify application settings</span></span>

<span data-ttu-id="40789-219">Pour déployer le service DKE, vous devez modifier les types de paramètres d’application suivants :</span><span class="sxs-lookup"><span data-stu-id="40789-219">To deploy the DKE service, you must modify the following types of application settings:</span></span>

- [<span data-ttu-id="40789-220">Paramètres d’accès clés</span><span class="sxs-lookup"><span data-stu-id="40789-220">Key access settings</span></span>](#key-access-settings)
- [<span data-ttu-id="40789-221">Paramètres de client et de clé</span><span class="sxs-lookup"><span data-stu-id="40789-221">Tenant and key settings</span></span>](#tenant-and-key-settings)

<span data-ttu-id="40789-222">Vous modifiez les paramètres de l’application dans le fichier appsettings.js.</span><span class="sxs-lookup"><span data-stu-id="40789-222">You modify application settings in the appsettings.json file.</span></span> <span data-ttu-id="40789-223">Ce fichier se trouve dans le DoubleKeyEncryptionService référentiel que vous avez cloné localement sous DoubleKeyEncryptionService\src\customer-key-store.</span><span class="sxs-lookup"><span data-stu-id="40789-223">This file is located in the DoubleKeyEncryptionService repo you cloned locally under DoubleKeyEncryptionService\src\customer-key-store.</span></span> <span data-ttu-id="40789-224">Par exemple, dans Visual Studio code, vous pouvez accéder au fichier comme indiqué dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="40789-224">For example, in Visual Studio Code, you can browse to the file as shown in the following picture.</span></span>

![Recherche de la appsettings.jssur le fichier pour DKE.](../media/dke-appsettingsjson.png)

#### <a name="key-access-settings"></a><span data-ttu-id="40789-226">Paramètres d’accès clés</span><span class="sxs-lookup"><span data-stu-id="40789-226">Key access settings</span></span>

<span data-ttu-id="40789-227">Choisissez d’utiliser ou non l’autorisation de messagerie ou de rôle.</span><span class="sxs-lookup"><span data-stu-id="40789-227">Choose whether to use email or role authorization.</span></span> <span data-ttu-id="40789-228">DKE ne prend en charge qu’une seule de ces méthodes d’authentification à la fois.</span><span class="sxs-lookup"><span data-stu-id="40789-228">DKE supports only one of these authentication methods at a time.</span></span>

- <span data-ttu-id="40789-229">**Autorisation de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="40789-229">**Email authorization**.</span></span> <span data-ttu-id="40789-230">Permet à votre organisation d’autoriser l’accès aux clés en fonction des adresses de messagerie uniquement.</span><span class="sxs-lookup"><span data-stu-id="40789-230">Allows your organization to authorize access to keys based on email addresses only.</span></span>

- <span data-ttu-id="40789-231">**Autorisation de rôle**.</span><span class="sxs-lookup"><span data-stu-id="40789-231">**Role authorization**.</span></span> <span data-ttu-id="40789-232">Permet à votre organisation d’autoriser l’accès aux clés en fonction des groupes Active Directory et exige que le service Web interroge LDAP.</span><span class="sxs-lookup"><span data-stu-id="40789-232">Allows your organization to authorize access to keys based on Active Directory groups, and requires that the web service can query LDAP.</span></span>

<span data-ttu-id="40789-233">**Pour définir les paramètres d’accès clés pour DKE à l’aide de l’autorisation de messagerie**</span><span class="sxs-lookup"><span data-stu-id="40789-233">**To set key access settings for DKE using email authorization**</span></span>

1. <span data-ttu-id="40789-234">Ouvrez le fichier **appsettings.js** et localisez le `AuthorizedEmailAddress` paramètre.</span><span class="sxs-lookup"><span data-stu-id="40789-234">Open the **appsettings.json** file and locate the `AuthorizedEmailAddress` setting.</span></span>

2. <span data-ttu-id="40789-235">Ajoutez l’adresse ou les adresses de messagerie que vous souhaitez autoriser.</span><span class="sxs-lookup"><span data-stu-id="40789-235">Add the email address or addresses that you want to authorize.</span></span> <span data-ttu-id="40789-236">Séparez les adresses de messagerie par des guillemets et des virgules.</span><span class="sxs-lookup"><span data-stu-id="40789-236">Separate multiple email addresses with double quotes and commas.</span></span> <span data-ttu-id="40789-237">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40789-237">For example:</span></span>

   ```json
   "AuthorizedEmailAddress": ["email1@company.com", "email2@company.com ", "email3@company.com"]
   ```

3. <span data-ttu-id="40789-238">Recherchez le `LDAPPath` paramètre et supprimez le texte `If role authorization is used then this is the LDAP path` entre guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="40789-238">Locate the `LDAPPath` setting and remove the text `If role authorization is used then this is the LDAP path` between the double quotes.</span></span> <span data-ttu-id="40789-239">Laissez les guillemets doubles en place.</span><span class="sxs-lookup"><span data-stu-id="40789-239">Leave the double quotes in place.</span></span> <span data-ttu-id="40789-240">Lorsque vous avez terminé, le paramètre doit ressembler à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="40789-240">When you're finished, the setting should look like this.</span></span>

   ```json
   "LDAPPath": ""
   ```

4. <span data-ttu-id="40789-241">Localisez le `AuthorizedRoles` paramètre et supprimez la ligne entière.</span><span class="sxs-lookup"><span data-stu-id="40789-241">Locate the `AuthorizedRoles` setting and delete the entire line.</span></span>

<span data-ttu-id="40789-242">Cette image montre le **appsettings.jssur** un fichier correctement mis en forme pour l’autorisation de messagerie.</span><span class="sxs-lookup"><span data-stu-id="40789-242">This image shows the **appsettings.json** file correctly formatted for email authorization.</span></span>

   ![appsettings.jssur le fichier affichant la méthode d’autorisation de messagerie](../media/dke-email-accesssetting.png)

<span data-ttu-id="40789-244">**Pour définir les paramètres d’accès clés pour DKE à l’aide de l’autorisation de rôle**</span><span class="sxs-lookup"><span data-stu-id="40789-244">**To set key access settings for DKE using role authorization**</span></span>

1. <span data-ttu-id="40789-245">Ouvrez le fichier **appsettings.js** et localisez le `AuthorizedRoles` paramètre.</span><span class="sxs-lookup"><span data-stu-id="40789-245">Open the **appsettings.json** file and locate the `AuthorizedRoles` setting.</span></span>

2. <span data-ttu-id="40789-246">Ajoutez les noms de groupe Active Directory que vous souhaitez autoriser.</span><span class="sxs-lookup"><span data-stu-id="40789-246">Add the Active Directory group names you want to authorize.</span></span> <span data-ttu-id="40789-247">Séparez les noms de plusieurs groupes par des guillemets et des virgules.</span><span class="sxs-lookup"><span data-stu-id="40789-247">Separate multiple group names with double quotes and commas.</span></span> <span data-ttu-id="40789-248">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40789-248">For example:</span></span>

   ```json
   "AuthorizedRoles": ["group1", "group2", "group3"]
   ```

3. <span data-ttu-id="40789-249">Localisez le `LDAPPath` paramètre et ajoutez le domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="40789-249">Locate the `LDAPPath` setting and add the Active Directory domain.</span></span> <span data-ttu-id="40789-250">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40789-250">For example:</span></span>

   ```json
   "LDAPPath": "contoso.com"
   ```

4. <span data-ttu-id="40789-251">Localisez le `AuthorizedEmailAddress` paramètre et supprimez la ligne entière.</span><span class="sxs-lookup"><span data-stu-id="40789-251">Locate the `AuthorizedEmailAddress` setting and delete the entire line.</span></span>

<span data-ttu-id="40789-252">Cette image montre le **appsettings.jssur** un fichier correctement mis en forme pour l’autorisation de rôle.</span><span class="sxs-lookup"><span data-stu-id="40789-252">This image shows the **appsettings.json** file correctly formatted for role authorization.</span></span>

   ![appsettings.jssur le fichier affichant la méthode d’autorisation de rôle](../media/dke-role-accesssetting.png)

#### <a name="tenant-and-key-settings"></a><span data-ttu-id="40789-254">Paramètres de client et de clé</span><span class="sxs-lookup"><span data-stu-id="40789-254">Tenant and key settings</span></span>

<span data-ttu-id="40789-255">Les paramètres de client et de clé DKE se trouvent dans le fichier **appsettings.js** .</span><span class="sxs-lookup"><span data-stu-id="40789-255">DKE tenant and key settings are located in the **appsettings.json** file.</span></span>

<span data-ttu-id="40789-256">**Pour configurer les paramètres de client et de clé pour DKE**</span><span class="sxs-lookup"><span data-stu-id="40789-256">**To configure tenant and key settings for DKE**</span></span>

1. <span data-ttu-id="40789-257">Ouvrez le fichier **appsettings.js** .</span><span class="sxs-lookup"><span data-stu-id="40789-257">Open the **appsettings.json** file.</span></span>

2. <span data-ttu-id="40789-258">Recherchez le `ValidIssuers` paramètre et remplacez-le `<tenantid>` par votre ID de client.</span><span class="sxs-lookup"><span data-stu-id="40789-258">Locate the `ValidIssuers` setting and replace `<tenantid>` with your tenant ID.</span></span> <span data-ttu-id="40789-259">Vous pouvez localiser votre ID de locataire en accédant au portail Azure et en affichant les [Propriétés du client](https://aad.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span><span class="sxs-lookup"><span data-stu-id="40789-259">You can locate your tenant ID by going to the Azure portal and viewing the [tenant properties](https://aad.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span></span> <span data-ttu-id="40789-260">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40789-260">For example:</span></span>

   ```json
   "ValidIssuers": [
     "https://sts.windows.net/9c99431e-b513-44be-a7d9-e7b500002d4b/"
   ]
   ```

<span data-ttu-id="40789-261">Localisez le `JwtAudience` .</span><span class="sxs-lookup"><span data-stu-id="40789-261">Locate the `JwtAudience`.</span></span> <span data-ttu-id="40789-262">Remplacez `<yourhostname>` par le nom d’hôte de l’ordinateur sur lequel le service DKE s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="40789-262">Replace `<yourhostname>` with the hostname of the machine where the DKE service will run.</span></span> <span data-ttu-id="40789-263">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40789-263">For example:</span></span>



  > [!IMPORTANT]
  > <span data-ttu-id="40789-264">La valeur de `JwtAudience` doit correspondre *exactement*au nom de votre hôte.</span><span class="sxs-lookup"><span data-stu-id="40789-264">The value for `JwtAudience` must match the name of your host *exactly*.</span></span> <span data-ttu-id="40789-265">Vous pouvez utiliser **localhost : 5001** lors du débogage.</span><span class="sxs-lookup"><span data-stu-id="40789-265">You may use **localhost:5001** while debugging.</span></span> <span data-ttu-id="40789-266">Toutefois, lorsque vous avez fini de déboguer, veillez à mettre à jour cette valeur sur le nom d’hôte du serveur.</span><span class="sxs-lookup"><span data-stu-id="40789-266">However, When you're done debugging, make sure to update this value to the server's hostname.</span></span>

- <span data-ttu-id="40789-267">`TestKeys:Name`.</span><span class="sxs-lookup"><span data-stu-id="40789-267">`TestKeys:Name`.</span></span> <span data-ttu-id="40789-268">Entrez un nom pour votre clé.</span><span class="sxs-lookup"><span data-stu-id="40789-268">Enter a name for your key.</span></span> <span data-ttu-id="40789-269">Par exemple : `TestKey1`</span><span class="sxs-lookup"><span data-stu-id="40789-269">For example: `TestKey1`</span></span>
- <span data-ttu-id="40789-270">`TestKeys:Id`.</span><span class="sxs-lookup"><span data-stu-id="40789-270">`TestKeys:Id`.</span></span> <span data-ttu-id="40789-271">Créez un GUID et entrez-le en tant que `TestKeys:ID` valeur.</span><span class="sxs-lookup"><span data-stu-id="40789-271">Create a GUID and enter it as the `TestKeys:ID` value.</span></span> <span data-ttu-id="40789-272">Par exemple, `DCE1CC21-FF9B-4424-8FF4-9914BD19A1BE`.</span><span class="sxs-lookup"><span data-stu-id="40789-272">For example, `DCE1CC21-FF9B-4424-8FF4-9914BD19A1BE`.</span></span> <span data-ttu-id="40789-273">Vous pouvez utiliser un site comme le [Générateur de GUID en ligne](https://guidgenerator.com/) pour générer un GUID de manière aléatoire.</span><span class="sxs-lookup"><span data-stu-id="40789-273">You can use a site like [Online GUID Generator](https://guidgenerator.com/) to randomly generate a GUID.</span></span>

<span data-ttu-id="40789-274">Cette image indique le format correct pour les paramètres de client et de clé dans **appsettings.jsactivé**.</span><span class="sxs-lookup"><span data-stu-id="40789-274">This image shows the correct format for tenant and keys settings in **appsettings.json**.</span></span> <span data-ttu-id="40789-275">`LDAPPath` est configuré pour l’autorisation de rôle.</span><span class="sxs-lookup"><span data-stu-id="40789-275">`LDAPPath` is configured for role authorization.</span></span>

![Indique les paramètres client et clé corrects pour DKE dans le fichier appsettings.js.](../media/dke-appsettingsjson-tenantkeysettings.png)

### <a name="generate-test-keys"></a><span data-ttu-id="40789-277">Générer des clés de test</span><span class="sxs-lookup"><span data-stu-id="40789-277">Generate test keys</span></span>

<span data-ttu-id="40789-278">Une fois que vous avez défini les paramètres de votre application, vous êtes prêt à générer des clés de test publiques et privées.</span><span class="sxs-lookup"><span data-stu-id="40789-278">Once you have your application settings defined, you're ready to generate public and private test keys.</span></span>

<span data-ttu-id="40789-279">Pour générer des clés :</span><span class="sxs-lookup"><span data-stu-id="40789-279">To generate keys:</span></span>

1. <span data-ttu-id="40789-280">Dans le menu Démarrer de Windows, exécutez l’invite de commandes OpenSSL.</span><span class="sxs-lookup"><span data-stu-id="40789-280">From the Windows Start menu, run the OpenSSL Command Prompt.</span></span>

1. <span data-ttu-id="40789-281">Accédez au dossier dans lequel vous souhaitez enregistrer les clés de test.</span><span class="sxs-lookup"><span data-stu-id="40789-281">Change to the folder where you want to save the test keys.</span></span> <span data-ttu-id="40789-282">Les fichiers que vous créez en suivant les étapes de cette tâche sont stockés dans le même dossier.</span><span class="sxs-lookup"><span data-stu-id="40789-282">The files you create by completing the steps in this task are stored in the same folder.</span></span>

1. <span data-ttu-id="40789-283">Générez la nouvelle clé de test.</span><span class="sxs-lookup"><span data-stu-id="40789-283">Generate the new test key.</span></span>

   ```dos
   openssl req -x509 -newkey rsa:2048 -keyout key.pem -out cert.pem -days 365
   ```

2. <span data-ttu-id="40789-284">Générez la clé privée.</span><span class="sxs-lookup"><span data-stu-id="40789-284">Generate the private key.</span></span>

   ```dos
   openssl rsa -in key.pem -out privkeynopass.pem
   ```

1. <span data-ttu-id="40789-285">Générez la clé publique.</span><span class="sxs-lookup"><span data-stu-id="40789-285">Generate the public key.</span></span>

   ```dos
   openssl rsa -in key.pem -pubout > pubkeyonly.pem
   ```

1. <span data-ttu-id="40789-286">Dans un éditeur de texte, ouvrez **pubkeyonly. pem**.</span><span class="sxs-lookup"><span data-stu-id="40789-286">In a text editor, open **pubkeyonly.pem**.</span></span> <span data-ttu-id="40789-287">Copiez tout le contenu du fichier **pubkeyonly. pem** , à l’exception de la première et de la dernière ligne, dans la `PublicPem` section du fichier **appsettings.js** .</span><span class="sxs-lookup"><span data-stu-id="40789-287">Copy all of the content in the **pubkeyonly.pem** file, except the first and last lines, into the `PublicPem` section of the **appsettings.json** file.</span></span>

1. <span data-ttu-id="40789-288">Dans un éditeur de texte, ouvrez **privkeynopass. pem**.</span><span class="sxs-lookup"><span data-stu-id="40789-288">In a text editor, open **privkeynopass.pem**.</span></span> <span data-ttu-id="40789-289">Copiez tout le contenu du fichier **privkeynopass. pem** , à l’exception de la première et de la dernière ligne, dans la `PrivatePem` section du fichier **appsettings.js** .</span><span class="sxs-lookup"><span data-stu-id="40789-289">Copy all of the content in the **privkeynopass.pem** file, except the first and last lines, into the `PrivatePem` section of the **appsettings.json** file.</span></span>

1. <span data-ttu-id="40789-290">Supprimez tous les espaces et lignes de nouvelle ligne dans les `PublicPem` `PrivatePem` sections et.</span><span class="sxs-lookup"><span data-stu-id="40789-290">Remove all blank spaces and newlines in both the `PublicPem` and `PrivatePem` sections.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="40789-291">Lorsque vous copiez ce contenu, ne supprimez pas les données du PEM.</span><span class="sxs-lookup"><span data-stu-id="40789-291">When you copy this content, do not delete any of the PEM data.</span></span>

1. <span data-ttu-id="40789-292">Dans Visual Studio code, accédez au fichier **Startup.cs** .</span><span class="sxs-lookup"><span data-stu-id="40789-292">In Visual Studio Code, browse to the **Startup.cs** file.</span></span> <span data-ttu-id="40789-293">Ce fichier se trouve dans le DoubleKeyEncryptionService référentiel que vous avez cloné localement sous DoubleKeyEncryptionService\src\customer-key-store\.</span><span class="sxs-lookup"><span data-stu-id="40789-293">This file is located in the DoubleKeyEncryptionService repo you cloned locally under DoubleKeyEncryptionService\src\customer-key-store\.</span></span>

2. <span data-ttu-id="40789-294">Recherchez les lignes suivantes :</span><span class="sxs-lookup"><span data-stu-id="40789-294">Locate the following lines:</span></span>

   ```c#
        #if USE_TEST_KEYS
        #error !!!!!!!!!!!!!!!!!!!!!! Use of test keys is only supported for testing,
        DO NOT USE  FOR PRODUCTION !!!!!!!!!!!!!!!!!!!!!!!!!!!!!
        services.AddSingleton<ippw.IKeyStore, ippw.TestKeyStore>();
        #endif
   ```

3. <span data-ttu-id="40789-295">Remplacez ces lignes par le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="40789-295">Replace these lines with the following text:</span></span>

   ```csharp
   services.AddSingleton<ippw.IKeyStore, ippw.TestKeyStore>();
   ```

   <span data-ttu-id="40789-296">Les résultats finaux doivent ressembler à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="40789-296">The end results should look similar to the following.</span></span>

   ![fichier startup.cs pour la préversion publique](../media/dke-startupcs-usetestkeys.png)

<span data-ttu-id="40789-298">Vous êtes maintenant prêt à [créer votre projet DKE](#build-the-project).</span><span class="sxs-lookup"><span data-stu-id="40789-298">Now you're ready to [build your DKE project](#build-the-project).</span></span>

### <a name="build-the-project"></a><span data-ttu-id="40789-299">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="40789-299">Build the project</span></span>

<span data-ttu-id="40789-300">Suivez les instructions ci-dessous pour générer le projet DKE localement :</span><span class="sxs-lookup"><span data-stu-id="40789-300">Use the following instructions to build the DKE project locally:</span></span>

1. <span data-ttu-id="40789-301">Dans Visual Studio code, dans le référentiel du service DKE, sélectionnez **Afficher** la \> **palette de commandes** , puis tapez **générer** à l’invite.</span><span class="sxs-lookup"><span data-stu-id="40789-301">In Visual Studio Code, in the DKE service repository, select **View** \> **Command Palette** and then type **build** at the prompt.</span></span>

1. <span data-ttu-id="40789-302">Dans la liste, choisissez **tâches : exécuter la tâche de génération**.</span><span class="sxs-lookup"><span data-stu-id="40789-302">From the list, choose **Tasks: Run build task**.</span></span>

   <span data-ttu-id="40789-303">Si aucune tâche de génération n’a été trouvée, sélectionnez **configurer la tâche de génération** et créez-en une pour .net Core comme suit.</span><span class="sxs-lookup"><span data-stu-id="40789-303">If there are no build tasks found, select **Configure Build Task** and create one for .NET core as follows.</span></span>

   ![Configurer une tâche de génération manquante pour .NET](../media/dke-configurebuildtask.png)

   1. <span data-ttu-id="40789-305">Choisissez **create tasks.json from template**.</span><span class="sxs-lookup"><span data-stu-id="40789-305">Choose **Create tasks.json from template**.</span></span>

   ![Créer tasks.jssur le fichier à partir du modèle pour DKE](../media/dke-createtasksjsonfromtemplate.png)

   2. <span data-ttu-id="40789-307">Dans la liste des types de modèles, sélectionnez **.net Core**.</span><span class="sxs-lookup"><span data-stu-id="40789-307">From the list of template types, select **.NET Core**.</span></span>

   ![Créer tasks.jssur le fichier à partir du modèle pour DKE](../media/dke-tasksjsontemplate.png)

   3. <span data-ttu-id="40789-309">Dans la section générer, recherchez le chemin d’accès au fichier **customerkeystore. csproj** .</span><span class="sxs-lookup"><span data-stu-id="40789-309">In the build section, locate the path to the **customerkeystore.csproj** file.</span></span> <span data-ttu-id="40789-310">Si ce n’est pas le cas, ajoutez la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="40789-310">If it's not there, add the following line:</span></span>

      ```json
      "${workspaceFolder}/src/customer-key-store/customerkeystore.csproj",
      ```

  4. <span data-ttu-id="40789-311">Exécutez de nouveau la génération.</span><span class="sxs-lookup"><span data-stu-id="40789-311">Run the build again.</span></span>

1. <span data-ttu-id="40789-312">Vérifiez qu’il n’y a pas d’erreurs rouges dans la fenêtre sortie.</span><span class="sxs-lookup"><span data-stu-id="40789-312">Verify that there are no red errors in the output window.</span></span>

   <span data-ttu-id="40789-313">S’il y a des erreurs rouges, vérifiez la sortie de la console.</span><span class="sxs-lookup"><span data-stu-id="40789-313">If there are red errors, check the console output.</span></span> <span data-ttu-id="40789-314">Assurez-vous que vous avez effectué toutes les étapes précédentes correctement et que les versions de build correctes sont présentes.</span><span class="sxs-lookup"><span data-stu-id="40789-314">Ensure that you completed all the previous steps correctly and the correct build versions are present.</span></span>

2. <span data-ttu-id="40789-315">Sélectionnez **exécuter** \> **Démarrer le débogage** pour déboguer le processus.</span><span class="sxs-lookup"><span data-stu-id="40789-315">Select **Run** \> **Start Debugging** to debug the process.</span></span> <span data-ttu-id="40789-316">Si vous êtes invité à sélectionner un environnement, sélectionnez **.net Core**.</span><span class="sxs-lookup"><span data-stu-id="40789-316">If you're prompted to select an environment, select **.NET core**.</span></span>

<span data-ttu-id="40789-317">Le débogueur .net Core lance généralement vers' ' ' https://localhost:5001 `. To view your test key, go to ` https://localhost:5001 et ajoute une barre oblique (/) et le nom de votre clé.</span><span class="sxs-lookup"><span data-stu-id="40789-317">The .NET core debugger typically launches to \`\`https://localhost:5001`. To view your test key, go to `https://localhost:5001\` and append a forward slash (/) and the name of your key.</span></span> <span data-ttu-id="40789-318">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40789-318">For example:</span></span>

```https
https://localhost:5001/TestKey1
```

<span data-ttu-id="40789-319">La clé doit s’afficher au format JSON.</span><span class="sxs-lookup"><span data-stu-id="40789-319">The key should display in JSON format.</span></span>

<span data-ttu-id="40789-320">Votre installation est maintenant terminée.</span><span class="sxs-lookup"><span data-stu-id="40789-320">Your setup is now complete.</span></span> <span data-ttu-id="40789-321">Avant de publier le keystore, dans appsettings.jsactivé, pour le paramètre JwtAudience, vérifiez que la valeur de hostname correspond exactement au nom de l’hôte de service de l’application.</span><span class="sxs-lookup"><span data-stu-id="40789-321">Before you publish the keystore, in appsettings.json, for the JwtAudience setting, ensure the value for hostname exactly matches your App Service host name.</span></span> <span data-ttu-id="40789-322">Vous pouvez l’avoir remplacée par localhost pour dépanner la Build.</span><span class="sxs-lookup"><span data-stu-id="40789-322">You may have changed it to localhost to troubleshoot the build.</span></span>

### <a name="publish-the-key-store"></a><span data-ttu-id="40789-323">Publier le magasin de clés</span><span class="sxs-lookup"><span data-stu-id="40789-323">Publish the key store</span></span>

<span data-ttu-id="40789-324">Pour publier le magasin de clés, vous allez créer une instance de service d’application Azure pour héberger votre déploiement DKE.</span><span class="sxs-lookup"><span data-stu-id="40789-324">To publish the key store, you'll create an Azure App Service instance to host your DKE deployment.</span></span> <span data-ttu-id="40789-325">Ensuite, vous allez publier vos clés générées dans Azure.</span><span class="sxs-lookup"><span data-stu-id="40789-325">Next, you'll publish your generated keys to Azure.</span></span>

<span data-ttu-id="40789-326">**Pour créer une instance Azure Web App afin d’héberger votre déploiement DKE**</span><span class="sxs-lookup"><span data-stu-id="40789-326">**To create an Azure Web App instance to host your DKE deployment**</span></span>

1. <span data-ttu-id="40789-327">Dans votre navigateur, connectez-vous au [portail Microsoft Azure](https://ms.portal.azure.com)et accédez à **app services**  >  **Add**.</span><span class="sxs-lookup"><span data-stu-id="40789-327">In your browser, sign in to the [Microsoft Azure portal](https://ms.portal.azure.com), and go to **App Services** > **Add**.</span></span>

1. <span data-ttu-id="40789-328">Sélectionnez votre abonnement et le groupe de ressources, puis définissez les détails de votre instance.</span><span class="sxs-lookup"><span data-stu-id="40789-328">Select your subscription and resource group and define your instance details.</span></span>

    - <span data-ttu-id="40789-329">Entrez le nom d’hôte de l’ordinateur sur lequel vous souhaitez installer le service DKE.</span><span class="sxs-lookup"><span data-stu-id="40789-329">Enter the hostname of the computer where you want to install the DKE service.</span></span> <span data-ttu-id="40789-330">Assurez-vous qu’il s’agit du même nom que celui défini pour le paramètre JwtAudience dans le fichier [**appsettings.js**](#tenant-and-key-settings) .</span><span class="sxs-lookup"><span data-stu-id="40789-330">Make sure it's the same name as the one defined for the JwtAudience setting in the [**appsettings.json**](#tenant-and-key-settings) file.</span></span> <span data-ttu-id="40789-331">La valeur que vous fournissez pour le nom est également WebAppInstanceName.</span><span class="sxs-lookup"><span data-stu-id="40789-331">The value you provide for the name is also the WebAppInstanceName.</span></span>

    - <span data-ttu-id="40789-332">Pour **publier**, sélectionner le **code**et pour la **pile Runtime**, sélectionnez **.net Core 3,1**.</span><span class="sxs-lookup"><span data-stu-id="40789-332">For **Publish**, select **code**, and for **Runtime stack**, select **.NET Core 3.1**.</span></span>

    <span data-ttu-id="40789-333">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40789-333">For example:</span></span>

   ![Ajouter votre service d’application](../media/dke-azure-add-app-service.png)

1. <span data-ttu-id="40789-335">Au bas de la page, sélectionnez **révision + créer**, puis **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="40789-335">At the bottom of the page, select **Review + create**, and then select **Add**.</span></span>

1. <span data-ttu-id="40789-336">Effectuez l’une des opérations suivantes pour publier vos clés générées dans Azure :</span><span class="sxs-lookup"><span data-stu-id="40789-336">Do one of the following to publish your generated keys to Azure:</span></span>

    - [<span data-ttu-id="40789-337">Publier via ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="40789-337">Publish via ZipDeployUI</span></span>](#publish-via-zipdeployui)
    - [<span data-ttu-id="40789-338">Publier via FTP</span><span class="sxs-lookup"><span data-stu-id="40789-338">Publish via FTP</span></span>](#publish-via-ftp)
    - [<span data-ttu-id="40789-339">Publier via Visual Studio 2019 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="40789-339">Publish via Visual Studio 2019 or later</span></span>](https://docs.microsoft.com/aspnet/core/tutorials/)
    - [<span data-ttu-id="40789-340">Publier sur un système local</span><span class="sxs-lookup"><span data-stu-id="40789-340">Publish to an on-premises system</span></span>](https://docs.microsoft.com/aspnet/core/tutorials/publish-to-iis?view=aspnetcore-3.1&tabs=netcore-cli)

    > [!NOTE]
    > <span data-ttu-id="40789-341">Vous pouvez préférer d’autres méthodes de déploiement de vos clés.</span><span class="sxs-lookup"><span data-stu-id="40789-341">You may prefer other methods to deploy your keys.</span></span> <span data-ttu-id="40789-342">Sélectionnez la méthode qui convient le mieux à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="40789-342">Select the method that works best for your organization.</span></span>

    > [!TIP]
    > <span data-ttu-id="40789-343">La [publication via Visual Studio](https://docs.microsoft.com/aspnet/core/tutorials/) et un [système local](https://docs.microsoft.com/aspnet/core/tutorials/publish-to-iis?view=aspnetcore-3.1&tabs=netcore-cli) est décrite dans la [documentation ASP.net](https://docs.microsoft.com/aspnet/core/).</span><span class="sxs-lookup"><span data-stu-id="40789-343">[Publishing via Visual Studio](https://docs.microsoft.com/aspnet/core/tutorials/) and to an [on-premises system](https://docs.microsoft.com/aspnet/core/tutorials/publish-to-iis?view=aspnetcore-3.1&tabs=netcore-cli) is described in the [ASP .NET documentation](https://docs.microsoft.com/aspnet/core/).</span></span> <span data-ttu-id="40789-344">Si vous utilisez l’une de ces méthodes, ouvrez les instructions dans un onglet distinct afin de pouvoir revenir rapidement une fois que vous avez fini.</span><span class="sxs-lookup"><span data-stu-id="40789-344">If you use one of these methods, open the instructions in a separate tab so that you can return here easily when you're done.</span></span>

#### <a name="publish-via-zipdeployui"></a><span data-ttu-id="40789-345">Publier via ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="40789-345">Publish via ZipDeployUI</span></span>

1. <span data-ttu-id="40789-346">Accédez à `https://<WebAppInstanceName>.scm.azurewebsites.net/ZipDeployUI`.</span><span class="sxs-lookup"><span data-stu-id="40789-346">Go to `https://<WebAppInstanceName>.scm.azurewebsites.net/ZipDeployUI`.</span></span>

    <span data-ttu-id="40789-347">Par exemple : https://customerkeystoreforpublicpreview.scm.azurewebsites.net/ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="40789-347">For example: https://customerkeystoreforpublicpreview.scm.azurewebsites.net/ZipDeployUI</span></span>

1. <span data-ttu-id="40789-348">Dans la base de code pour le magasin de clés, accédez au dossier **Customer-Key-store\src\customer-Key-Store** et vérifiez que ce dossier contient le fichier **customerkeystore. csproj** .</span><span class="sxs-lookup"><span data-stu-id="40789-348">In the codebase for the key store, go to the **customer-key-store\src\customer-key-store** folder, and verify that this folder contains the **customerkeystore.csproj** file.</span></span>

1. <span data-ttu-id="40789-349">Exécuter : **publication dotnet**</span><span class="sxs-lookup"><span data-stu-id="40789-349">Run: **dotnet publish**</span></span>

     <span data-ttu-id="40789-350">La fenêtre sortie affiche le répertoire dans lequel la publication a été déployée.</span><span class="sxs-lookup"><span data-stu-id="40789-350">The output window displays the directory where the publish was deployed.</span></span>

    <span data-ttu-id="40789-351">Par exemple : `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span><span class="sxs-lookup"><span data-stu-id="40789-351">For example: `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span></span>

1. <span data-ttu-id="40789-352">Envoyez tous les fichiers du répertoire de publication dans un fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="40789-352">Send all files in the publish directory to a .zip file.</span></span> <span data-ttu-id="40789-353">Lors de la création du fichier. zip, assurez-vous que tous les fichiers du répertoire sont au niveau racine du fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="40789-353">When creating the .zip file, make sure that all files in the directory are at the root level of the .zip file.</span></span>

1. <span data-ttu-id="40789-354">Faites glisser et déposez le fichier. zip que vous créez sur le site ZipDeployUI que vous avez ouvert ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="40789-354">Drag and drop the .zip file you create to the ZipDeployUI site you opened above.</span></span> <span data-ttu-id="40789-355">Par exemple : https://customerkeystoreforpublicpreview.scm.azurewebsites.net/ZipDeployUI</span><span class="sxs-lookup"><span data-stu-id="40789-355">For example: https://customerkeystoreforpublicpreview.scm.azurewebsites.net/ZipDeployUI</span></span>

<span data-ttu-id="40789-356">DKE est déployé et vous pouvez accéder aux clés de test que vous avez créées.</span><span class="sxs-lookup"><span data-stu-id="40789-356">DKE is deployed and you can browse to the test keys you've created.</span></span> <span data-ttu-id="40789-357">Poursuivez [la validation de votre déploiement](#validate-your-deployment) ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="40789-357">Continue to [Validate your deployment](#validate-your-deployment) below.</span></span>

#### <a name="publish-via-ftp"></a><span data-ttu-id="40789-358">Publier via FTP</span><span class="sxs-lookup"><span data-stu-id="40789-358">Publish via FTP</span></span>

1. <span data-ttu-id="40789-359">Connectez-vous au service d’application que vous avez créé [ci-dessus](#publish-the-key-store).</span><span class="sxs-lookup"><span data-stu-id="40789-359">Connect to the App Service you created [above](#publish-the-key-store).</span></span>

    <span data-ttu-id="40789-360">Dans votre navigateur, accédez à : **Azure portal**  >  **App Service**  >  **Centre de déploiement**de  >  **déploiement manuel**  >  **FTP**  >  **Dashboard**du centre de déploiement Azure Portal App.</span><span class="sxs-lookup"><span data-stu-id="40789-360">In your browser, go to: **Azure portal** > **App Service** > **Deployment Center** > **Manual Deployment** > **FTP** > **Dashboard**.</span></span>

1. <span data-ttu-id="40789-361">Copiez les chaînes de connexion affichées dans un fichier local.</span><span class="sxs-lookup"><span data-stu-id="40789-361">Copy the connection strings displayed to a local file.</span></span> <span data-ttu-id="40789-362">Vous utiliserez ces chaînes pour vous connecter au service d’application Web et télécharger des fichiers via FTP.</span><span class="sxs-lookup"><span data-stu-id="40789-362">You'll use these strings to connect to the Web App Service and upload files via FTP.</span></span>

    <span data-ttu-id="40789-363">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40789-363">For example:</span></span>

   ![Copier des chaînes de connexion à partir du tableau de bord FTP](../media/dke-ftp-dashboard.png)

1. <span data-ttu-id="40789-365">Dans la base de code pour le stockage de clés, accédez au **répertoire Customer-Key-store\src\customer-Key-Store**</span><span class="sxs-lookup"><span data-stu-id="40789-365">In the codebase for the key storage, go to the **customer-key-store\src\customer-key-store directory**.</span></span>

1. <span data-ttu-id="40789-366">Vérifiez que ce répertoire contient le fichier **customerkeystore. csproj** .</span><span class="sxs-lookup"><span data-stu-id="40789-366">Verify that this directory contains the **customerkeystore.csproj** file.</span></span>

1. <span data-ttu-id="40789-367">Exécuter : **publication dotnet**</span><span class="sxs-lookup"><span data-stu-id="40789-367">Run: **dotnet publish**</span></span>

    <span data-ttu-id="40789-368">La sortie contient le répertoire dans lequel la publication a été déployée.</span><span class="sxs-lookup"><span data-stu-id="40789-368">The output contains the directory where the publish was deployed.</span></span>

    <span data-ttu-id="40789-369">Par exemple : `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span><span class="sxs-lookup"><span data-stu-id="40789-369">For example: `customer-key-store\src\customer-key-store\bin\Debug\netcoreapp3.1\publish\`</span></span>

1. <span data-ttu-id="40789-370">Envoyez tous les fichiers du répertoire de publication dans un fichier zip.</span><span class="sxs-lookup"><span data-stu-id="40789-370">Send all files in the publish directory to a zip file.</span></span> <span data-ttu-id="40789-371">Lors de la création du fichier. zip, assurez-vous que tous les fichiers du répertoire sont au niveau racine du fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="40789-371">When creating the .zip file, make sure that all files in the directory are at the root level of the .zip file.</span></span>

1. <span data-ttu-id="40789-372">À partir de votre client FTP, utilisez les informations de connexion que vous avez copiées pour vous connecter à votre service d’application.</span><span class="sxs-lookup"><span data-stu-id="40789-372">From your FTP client, use the connection information you copied to connect to your App Service.</span></span> <span data-ttu-id="40789-373">Téléchargez le fichier. zip que vous avez créé à l’étape précédente dans le répertoire racine de votre application Web.</span><span class="sxs-lookup"><span data-stu-id="40789-373">Upload the .zip file you created in the previous step to the root directory of your Web App.</span></span>

<span data-ttu-id="40789-374">DKE est déployé et vous pouvez accéder aux clés de test que vous auriez créées.</span><span class="sxs-lookup"><span data-stu-id="40789-374">DKE is deployed and you can browse to the test keys you'd created.</span></span> <span data-ttu-id="40789-375">Ensuite, [validez votre déploiement](#validate-your-deployment).</span><span class="sxs-lookup"><span data-stu-id="40789-375">Next, [Validate your deployment](#validate-your-deployment).</span></span>

### <a name="validate-your-deployment"></a><span data-ttu-id="40789-376">Valider votre déploiement</span><span class="sxs-lookup"><span data-stu-id="40789-376">Validate your deployment</span></span>

<span data-ttu-id="40789-377">Après avoir déployé DKE à l’aide de l’une des méthodes décrites ci-dessus, validez les principaux paramètres de déploiement et de magasin de clés.</span><span class="sxs-lookup"><span data-stu-id="40789-377">After deploying DKE using one of the methods described above, validate the deployment and the key store settings.</span></span>

<span data-ttu-id="40789-378">Exécutez :  </span><span class="sxs-lookup"><span data-stu-id="40789-378">Run:</span></span>

<span data-ttu-id="40789-379">src\customer-key-store\scripts\key_store_tester.ps1 mykeystoreurl/MyKey</span><span class="sxs-lookup"><span data-stu-id="40789-379">src\customer-key-store\scripts\key_store_tester.ps1 mykeystoreurl/mykey</span></span>

<span data-ttu-id="40789-380">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40789-380">For example:</span></span>

<span data-ttu-id="40789-381">key_store_tester.ps1 https://mycustomerkeystore.com/mykey</span><span class="sxs-lookup"><span data-stu-id="40789-381">key_store_tester.ps1 https://mycustomerkeystore.com/mykey</span></span>

<span data-ttu-id="40789-382">Assurez-vous qu’aucune erreur ne s’affiche dans la sortie.</span><span class="sxs-lookup"><span data-stu-id="40789-382">Ensure that no errors appear in the output.</span></span> <span data-ttu-id="40789-383">Lorsque vous êtes prêt, [Enregistrez votre magasin de clés](#register-your-key-store).</span><span class="sxs-lookup"><span data-stu-id="40789-383">When you're ready, [register your key store](#register-your-key-store).</span></span>

## <a name="register-your-key-store"></a><span data-ttu-id="40789-384">Enregistrer votre magasin de clés</span><span class="sxs-lookup"><span data-stu-id="40789-384">Register your key store</span></span>

<span data-ttu-id="40789-385">Les étapes suivantes vous permettent d’enregistrer votre magasin de clés.</span><span class="sxs-lookup"><span data-stu-id="40789-385">The following steps enable you to register your key store.</span></span> <span data-ttu-id="40789-386">L’inscription de votre magasin de clés est la dernière étape du déploiement d’DKE avant de commencer à créer des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="40789-386">Registering your key store is the last step in deploying DKE before you can start creating labels.</span></span>

<span data-ttu-id="40789-387">Pour enregistrer votre magasin de clés :</span><span class="sxs-lookup"><span data-stu-id="40789-387">To register your key store:</span></span>

1. <span data-ttu-id="40789-388">Dans votre navigateur, ouvrez le [portail Microsoft Azure](https://ms.portal.azure.com/), puis accédez à **toutes les** \> **Identity** \> **inscriptions des applications d'** identité des services.</span><span class="sxs-lookup"><span data-stu-id="40789-388">In your browser, open the [Microsoft Azure portal](https://ms.portal.azure.com/), and go to **All Services** \> **Identity** \> **App Registrations**.</span></span>

2. <span data-ttu-id="40789-389">Sélectionnez **nouvelle inscription**, puis entrez un nom explicite.</span><span class="sxs-lookup"><span data-stu-id="40789-389">Select **New registration**, and enter a meaningful name.</span></span>

3. <span data-ttu-id="40789-390">Sélectionnez un type de compte parmi les options affichées.</span><span class="sxs-lookup"><span data-stu-id="40789-390">Select an account type from the options displayed.</span></span>

    <span data-ttu-id="40789-391">Si vous utilisez Microsoft Azure avec un domaine non personnalisé, tel que **onmicrosoft.com**, sélectionnez **comptes dans cet annuaire d’organisation uniquement (Microsoft uniquement-client unique).**</span><span class="sxs-lookup"><span data-stu-id="40789-391">If you're using Microsoft Azure with a non-custom domain, such as **onmicrosoft.com**, select **Accounts in this organizational directory only (Microsoft only - Single tenant).**</span></span>

    <span data-ttu-id="40789-392">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40789-392">For example:</span></span>

   ![Inscription de l’application](../media/dke-app-registration.png)

4. <span data-ttu-id="40789-394">Au bas de la page, sélectionnez **Enregistrer** pour créer la nouvelle inscription de l’application.</span><span class="sxs-lookup"><span data-stu-id="40789-394">At the bottom of the page, select **Register** to create the new App Registration.</span></span>

5. <span data-ttu-id="40789-395">Dans la nouvelle inscription de l’application, dans le volet gauche, sous **gérer**, sélectionnez **authentification**.</span><span class="sxs-lookup"><span data-stu-id="40789-395">In your new App Registration, in the left pane, under **Manage**, select **Authentication**.</span></span>

6. <span data-ttu-id="40789-396">Sélectionnez **Ajouter une plateforme**.</span><span class="sxs-lookup"><span data-stu-id="40789-396">Select **Add a platform**.</span></span>
 
7. <span data-ttu-id="40789-397">Dans la fenêtre contextuelle **configurer les plateformes** , sélectionnez **Web**.</span><span class="sxs-lookup"><span data-stu-id="40789-397">On the **Configure platforms** popup, select **Web**.</span></span>
 
8. <span data-ttu-id="40789-398">Sous **URI de redirection**, entrez l’URI de votre service de chiffrement à double clé.</span><span class="sxs-lookup"><span data-stu-id="40789-398">Under **Redirect URIs**, enter the URI of your double key encryption service.</span></span> <span data-ttu-id="40789-399">Entrez l’URL du service d’application, y compris le nom d’hôte et le domaine.</span><span class="sxs-lookup"><span data-stu-id="40789-399">Enter the App Service URL, including both the hostname and domain.</span></span>

    <span data-ttu-id="40789-400">Par exemple : https://mycustomerkeystoretest.com</span><span class="sxs-lookup"><span data-stu-id="40789-400">For example: https://mycustomerkeystoretest.com</span></span>

    - <span data-ttu-id="40789-401">L’URL que vous entrez doit correspondre au nom d’hôte dans lequel votre magasin de clés est déployé.</span><span class="sxs-lookup"><span data-stu-id="40789-401">The URL you enter must match the hostname where your key store is deployed.</span></span>
    - <span data-ttu-id="40789-402">Si vous testez localement avec Visual Studio, utilisez **https://localhost:5001** .</span><span class="sxs-lookup"><span data-stu-id="40789-402">If you're testing locally with Visual Studio, use **https://localhost:5001**.</span></span>
    - <span data-ttu-id="40789-403">Dans tous les cas, le modèle doit être **https**.</span><span class="sxs-lookup"><span data-stu-id="40789-403">In all cases, the scheme must be **https**.</span></span>

    <span data-ttu-id="40789-404">Vérifiez que le nom d’hôte correspond exactement au nom de l’hôte de service de l’application.</span><span class="sxs-lookup"><span data-stu-id="40789-404">Ensure the hostname exactly matches your App Service host name.</span></span> <span data-ttu-id="40789-405">Vous pouvez l’avoir modifié sur `localhost` pour dépanner la Build.</span><span class="sxs-lookup"><span data-stu-id="40789-405">You may have changed it to `localhost` to troubleshoot the build.</span></span> <span data-ttu-id="40789-406">Dans **appsettings.jsactivé**, cette valeur est le nom d’hôte que vous avez défini pour `JwtAudience` .</span><span class="sxs-lookup"><span data-stu-id="40789-406">In **appsettings.json**, this value is the hostname you set for `JwtAudience`.</span></span>

6. <span data-ttu-id="40789-407">Sous **attribution implicite**, activez la case à cocher **jetons d’ID** .</span><span class="sxs-lookup"><span data-stu-id="40789-407">Under **Implicit grant**, select the **ID tokens** checkbox.</span></span>

1. <span data-ttu-id="40789-408">Sélectionnez **Enregistrer** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="40789-408">Select **Save** to save your changes.</span></span>

7. <span data-ttu-id="40789-409">Dans le volet de gauche, sélectionnez **exposer une API**, puis en regard de l’ID d’application URI, sélectionnez **Set**.</span><span class="sxs-lookup"><span data-stu-id="40789-409">On the left pane, select **Expose an API**, then next to Application ID URI, select **Set**.</span></span>

9. <span data-ttu-id="40789-410">Toujours sur la page **exposer une API** , dans la zone **étendues définies par cette API** , sélectionnez **Ajouter une étendue**.</span><span class="sxs-lookup"><span data-stu-id="40789-410">Still on the **Expose an API** page, in the **Scopes defined by this API** area, select **Add a scope**.</span></span> <span data-ttu-id="40789-411">Dans la nouvelle étendue :</span><span class="sxs-lookup"><span data-stu-id="40789-411">In the new scope:</span></span>

    1. <span data-ttu-id="40789-412">Définissez le nom de l’étendue en tant que **user_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="40789-412">Define the scope name as **user_impersonation**.</span></span>

    2. <span data-ttu-id="40789-413">Sélectionnez les administrateurs et les utilisateurs qui peuvent consentir.</span><span class="sxs-lookup"><span data-stu-id="40789-413">Select the administrators and users who can consent.</span></span>

    3. <span data-ttu-id="40789-414">Définissez les valeurs restantes requises.</span><span class="sxs-lookup"><span data-stu-id="40789-414">Define any remaining values required.</span></span>

    4. <span data-ttu-id="40789-415">Sélectionnez **Ajouter une étendue.**</span><span class="sxs-lookup"><span data-stu-id="40789-415">Select **Add scope.**</span></span>

    <span data-ttu-id="40789-416">Sélectionnez **Enregistrer** dans la partie supérieure pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="40789-416">Select **Save** at the top to save your changes.</span></span>

10. <span data-ttu-id="40789-417">Toujours sur la page **exposer une API** , dans la zone **applications clientes autorisées** , sélectionnez **Ajouter une application cliente**.</span><span class="sxs-lookup"><span data-stu-id="40789-417">Still on the **Expose an API** page, in the **Authorized client applications** area, select **Add a client application**.</span></span>

    <span data-ttu-id="40789-418">Dans la nouvelle application cliente :</span><span class="sxs-lookup"><span data-stu-id="40789-418">In the new client application:</span></span>

    1. <span data-ttu-id="40789-419">Définissez l’ID client comme **d3590ed6-52b3-4102-Aeff-aad2292ab01c**.</span><span class="sxs-lookup"><span data-stu-id="40789-419">Define the Client ID as **d3590ed6-52b3-4102-aeff-aad2292ab01c**.</span></span> <span data-ttu-id="40789-420">Cette valeur est l’ID client Microsoft Office et permet à Office d’obtenir un jeton d’accès pour votre magasin de clés.</span><span class="sxs-lookup"><span data-stu-id="40789-420">This value is the Microsoft Office client ID, and enables Office to obtain an access token for your key store.</span></span>

    2. <span data-ttu-id="40789-421">Sous **étendues autorisées**, sélectionnez l’étendue **user_impersonation** .</span><span class="sxs-lookup"><span data-stu-id="40789-421">Under **Authorized scopes**, select the **user_impersonation** scope.</span></span>

    3. <span data-ttu-id="40789-422">Sélectionnez **Ajouter une application**.</span><span class="sxs-lookup"><span data-stu-id="40789-422">Select **Add application**.</span></span>

    4. <span data-ttu-id="40789-423">Sélectionnez **Enregistrer** dans la partie supérieure pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="40789-423">Select **Save** at the top to save your changes.</span></span>

<span data-ttu-id="40789-424">Votre magasin de clés DKE est maintenant enregistré.</span><span class="sxs-lookup"><span data-stu-id="40789-424">Your DKE key store is now registered.</span></span> <span data-ttu-id="40789-425">Continuez en [créant des étiquettes à l’aide de DKE](#create-labels-using-dke).</span><span class="sxs-lookup"><span data-stu-id="40789-425">Continue by [creating labels using DKE](#create-labels-using-dke).</span></span>

## <a name="create-labels-using-dke"></a><span data-ttu-id="40789-426">Créer des étiquettes à l’aide de DKE</span><span class="sxs-lookup"><span data-stu-id="40789-426">Create labels using DKE</span></span>

<span data-ttu-id="40789-427">Dans le centre de conformité Microsoft 365, créez une étiquette de sensibilité et appliquez le chiffrement comme vous le feriez autrement.</span><span class="sxs-lookup"><span data-stu-id="40789-427">In the Microsoft 365 compliance center, create a new sensitivity label and apply encryption as you would otherwise.</span></span> <span data-ttu-id="40789-428">Sélectionnez **utiliser le chiffrement à double clé** et entrez l’URL du point de terminaison de votre clé.</span><span class="sxs-lookup"><span data-stu-id="40789-428">Select **Use Double Key Encryption** and enter the endpoint URL for your key.</span></span>

<span data-ttu-id="40789-429">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40789-429">For example:</span></span>

![Sélectionnez utiliser le chiffrement à double clé dans le centre de conformité Microsoft 365](../media/dke-use-dke.png)

<span data-ttu-id="40789-431">Toutes les étiquettes DKE que vous ajoutez commencent à apparaître pour les utilisateurs dans les versions les plus récentes des applications Microsoft 365 pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="40789-431">Any DKE labels you add will start appearing for users in the latest versions of Microsoft 365 Apps for enterprise.</span></span>

> [!NOTE]
> <span data-ttu-id="40789-432">L’actualisation des clients avec les nouvelles étiquettes peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="40789-432">It may take up to 24 hours for the clients to refresh with the new labels.</span></span>

### <a name="enable-dke-in-your-client"></a><span data-ttu-id="40789-433">Activer DKE dans votre client</span><span class="sxs-lookup"><span data-stu-id="40789-433">Enable DKE in your client</span></span>

<span data-ttu-id="40789-434">Activez DKE pour votre client en ajoutant les clés de Registre suivantes :</span><span class="sxs-lookup"><span data-stu-id="40789-434">Enable DKE for your client by adding the following registry keys:</span></span>

```properties
    [HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\MSIPC\flighting]
    "DoubleKeyProtection"=dword:00000001

    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\flighting]
    "DoubleKeyProtection"=dword:00000001
```

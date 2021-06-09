---
title: Contrôle des applications
description: Comment utiliser le contrôle d’application et la relation d’confiance avec les applications
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.author: jaimeo
manager: laurawi
audience: ITpro
ms.topic: article
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 6f5cc923b5a18b1f45dd186e88228db8c3a891cc
ms.sourcegitcommit: 83a40facd66e14343ad3ab72591cab9c41ce6ac0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/13/2021
ms.locfileid: "49841302"
---
# <a name="app-control"></a><span data-ttu-id="fee6b-104">Contrôle des applications</span><span class="sxs-lookup"><span data-stu-id="fee6b-104">App control</span></span>

<span data-ttu-id="fee6b-105">Le contrôle d’application est une pratique de sécurité facultative Bureau géré Microsoft qui limite l’exécution du code sur les appareils clients.</span><span class="sxs-lookup"><span data-stu-id="fee6b-105">App control is an optional security practice in Microsoft Managed Desktop that restricts the execution of code on client devices.</span></span> <span data-ttu-id="fee6b-106">Ce contrôle atténue les risques de programmes malveillants ou de scripts malveillants en exigeant que seul le code signé par une liste d’éditeurs approuvés par le client puisse s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="fee6b-106">This control mitigates the risk of malware or malicious scripts by requiring that only code signed by a customer-approved list of publishers can run.</span></span> <span data-ttu-id="fee6b-107">Ce contrôle a de nombreux avantages en matière de sécurité, mais il vise principalement à protéger les données et l’identité contre les exploitations basées sur le client.</span><span class="sxs-lookup"><span data-stu-id="fee6b-107">There are many security benefits from this control, but it primarily aims to protect data and identity from client-based exploits.</span></span>

<span data-ttu-id="fee6b-108">Bureau géré Microsoft simplifie la gestion des stratégies de contrôle des applications en créant une stratégie de base qui permet des scénarios de productivité principaux.</span><span class="sxs-lookup"><span data-stu-id="fee6b-108">Microsoft Managed Desktop simplifies the management of app control policies by creating a base policy that enables core productivity scenarios.</span></span> <span data-ttu-id="fee6b-109">Vous pouvez étendre la confiance à d’autres signataires spécifiques aux applications et aux scripts de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="fee6b-109">You can extend trust to other signers that are specific to the apps and scripts in your environment.</span></span> 


<span data-ttu-id="fee6b-110">Toute technologie de sécurité nécessite un équilibre entre l’expérience utilisateur, la sécurité et les coûts.</span><span class="sxs-lookup"><span data-stu-id="fee6b-110">Any security technology requires a balance among user experience, security, and cost.</span></span> <span data-ttu-id="fee6b-111">Le contrôle d’application réduit les menaces de logiciels malveillants dans votre environnement, mais il en a des conséquences pour l’utilisateur et d’autres actions pour votre administrateur informatique.</span><span class="sxs-lookup"><span data-stu-id="fee6b-111">App control reduces the threat of malicious software in your environment, but there are consequences to the user and further actions for your IT administrator.</span></span>

<span data-ttu-id="fee6b-112">**Sécurité supplémentaire :**</span><span class="sxs-lookup"><span data-stu-id="fee6b-112">**Additional security:**</span></span>

<span data-ttu-id="fee6b-113">L’exécution des applications ou des scripts non fiables par la stratégie de contrôle d’application est bloquée sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="fee6b-113">Apps or scripts that are not trusted by the app control policy are blocked from running on devices.</span></span>

<span data-ttu-id="fee6b-114">**Vos responsabilités supplémentaires :**</span><span class="sxs-lookup"><span data-stu-id="fee6b-114">**Your additional responsibilities:**</span></span>

- <span data-ttu-id="fee6b-115">Vous êtes responsable du test de vos applications pour déterminer si elles seraient bloquées par la stratégie de contrôle d’application.</span><span class="sxs-lookup"><span data-stu-id="fee6b-115">You are responsible for testing your apps to identify whether they would be blocked by the application control policy.</span></span>
- <span data-ttu-id="fee6b-116">Si une application est (ou serait) bloquée, vous êtes responsable de l’identification des détails nécessaires du signataire et de la demande de modification via le portail d’administration.</span><span class="sxs-lookup"><span data-stu-id="fee6b-116">If an app is (or would be) blocked, you are responsible for identifying the needed signer details and requesting a change through the Admin portal.</span></span>

<span data-ttu-id="fee6b-117">**Bureau géré Microsoft responsabilités :**</span><span class="sxs-lookup"><span data-stu-id="fee6b-117">**Microsoft Managed Desktop responsibilities:**</span></span>

- <span data-ttu-id="fee6b-118">Bureau géré Microsoft maintient la stratégie de base qui active les principaux produits Microsoft tels que les applications M365, Windows, Teams, OneDrive, etc.</span><span class="sxs-lookup"><span data-stu-id="fee6b-118">Microsoft Managed Desktop maintains the base policy that enables core Microsoft products like M365 Apps, Windows, Teams, OneDrive, and so on.</span></span>
- <span data-ttu-id="fee6b-119">Bureau géré Microsoft insère vos signataires de confiance et déploie la stratégie mise à jour sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="fee6b-119">Microsoft Managed Desktop inserts your trusted signers and deploys the updated policy to your devices.</span></span>


## <a name="managing-trust-in-applications"></a><span data-ttu-id="fee6b-120">Gestion de l’confiance dans les applications</span><span class="sxs-lookup"><span data-stu-id="fee6b-120">Managing trust in applications</span></span>

<span data-ttu-id="fee6b-121">Bureau géré Microsoft une stratégie de base qui fait confiance aux principaux composants des technologies Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fee6b-121">Microsoft Managed Desktop curates a base policy that trusts the core components of Microsoft technologies.</span></span> <span data-ttu-id="fee6b-122">Vous *ajoutez ensuite* l’confiance pour vos propres applications et scripts en informant Bureau géré Microsoft d’entre eux que vous avez déjà confiance.</span><span class="sxs-lookup"><span data-stu-id="fee6b-122">You then *add* trust for your own applications and scripts by informing Microsoft Managed Desktop which of them you already trust.</span></span>

### <a name="base-policy"></a><span data-ttu-id="fee6b-123">Stratégie de base</span><span class="sxs-lookup"><span data-stu-id="fee6b-123">Base policy</span></span>

<span data-ttu-id="fee6b-124">Bureau géré Microsoft, en collaboration avec des experts microsoft en cybersécurité, crée et maintient une stratégie standard qui permet à la plupart des applications déployées via Microsoft Intune tout en bloquant les activités dangereuses telles que la compilation de code ou l’exécution de fichiers non confiance.</span><span class="sxs-lookup"><span data-stu-id="fee6b-124">Microsoft Managed Desktop, in collaboration with Microsoft cybersecurity experts, creates, and maintains a standard policy that enables most apps deployed through Microsoft Intune while blocking dangerous activities like code compilation or execution of untrusted files.</span></span>

<span data-ttu-id="fee6b-125">La stratégie de base prend l’approche suivante pour restreindre l’exécution des logiciels :</span><span class="sxs-lookup"><span data-stu-id="fee6b-125">The base policy takes the following approach to restricting software execution:</span></span>

- <span data-ttu-id="fee6b-126">Les fichiers exécutés par les administrateurs seront autorisés à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="fee6b-126">Files run by administrators will be allowed to run.</span></span>
- <span data-ttu-id="fee6b-127">Les fichiers des emplacements qui ne *sont* pas accessibles en création par l’utilisateur sont autorisés à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="fee6b-127">Files in locations that are *not* in user-writable directories will be allowed to run.</span></span>
- <span data-ttu-id="fee6b-128">Les fichiers sont signés par un [signataire approuvé.](#signer-requests)</span><span class="sxs-lookup"><span data-stu-id="fee6b-128">Files are signed by a [trusted signer](#signer-requests).</span></span>
- <span data-ttu-id="fee6b-129">La plupart des fichiers signés par Microsoft s’exécutent, mais certains d’entre eux sont bloqués pour empêcher les actions à haut risque telles que la compilation du code.</span><span class="sxs-lookup"><span data-stu-id="fee6b-129">Most files signed by Microsoft will run, however some are blocked to prevent high-risk actions like code compilation.</span></span>


<span data-ttu-id="fee6b-130">Si un utilisateur autre qu’un administrateur aurait pu ajouter une application ou un script à un appareil (autrement dit, dans un répertoire accessible en écriture par l’utilisateur), nous ne l’autoriserons pas à s’exécuter, sauf si elle a déjà été spécifiquement autorisée par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="fee6b-130">If a user other than an administrator could have added an app or script to a device (that is, it's in a user-writable directory), we won't allow it to execute unless it has already been specifically allowed by an administrator.</span></span> <span data-ttu-id="fee6b-131">Si un utilisateur est tenté d’installer un programme malveillant, si une vulnérabilité dans une application l’utilisateur tente d’installer un programme malveillant, ou si un utilisateur tente intentionnellement d’exécuter une application ou un script non autorisé, notre stratégie arrête l’exécution.</span><span class="sxs-lookup"><span data-stu-id="fee6b-131">If a user is tricked into trying to install malware, if a vulnerability in an app the user runs attempts to install malware, or if a user intentionally tries to run an unauthorized app or script, our policy will stop execution.</span></span>

### <a name="signer-requests"></a><span data-ttu-id="fee6b-132">Demandes des signataires</span><span class="sxs-lookup"><span data-stu-id="fee6b-132">Signer requests</span></span>

<span data-ttu-id="fee6b-133">Vous nous informez des applications fournies par les éditeurs de logiciels que vous faites confiance en classant une demande *de signataire.*</span><span class="sxs-lookup"><span data-stu-id="fee6b-133">You inform us of which apps are provided by software publishers you trust by filing a *signer request*.</span></span> <span data-ttu-id="fee6b-134">En ce faisant, nous ajoutons ces informations d’autorisation à la stratégie de contrôle d’application de référence et permettons à tout logiciel signé avec le certificat de cet éditeur de s’exécuter sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="fee6b-134">By doing so, we add that trust information into the baseline application control policy and allow any software signed with that publisher's certificate to run on your devices.</span></span>

## <a name="audit-and-enforced-policies"></a><span data-ttu-id="fee6b-135">Stratégies d’audit et appliquées</span><span class="sxs-lookup"><span data-stu-id="fee6b-135">Audit and Enforced policies</span></span>

<span data-ttu-id="fee6b-136">Bureau géré Microsoft utilise deux stratégies Microsoft Intune pour fournir un contrôle d’application :</span><span class="sxs-lookup"><span data-stu-id="fee6b-136">Microsoft Managed Desktop uses two Microsoft Intune policies to provide app control:</span></span>

### <a name="audit-policy"></a><span data-ttu-id="fee6b-137">Stratégie d’audit</span><span class="sxs-lookup"><span data-stu-id="fee6b-137">Audit policy</span></span>
<span data-ttu-id="fee6b-138">Cette stratégie crée des journaux pour enregistrer si une application ou un script est bloqué par la stratégie Appliquée.</span><span class="sxs-lookup"><span data-stu-id="fee6b-138">This policy creates logs to record whether an app or script would be blocked by the Enforced policy.</span></span> <span data-ttu-id="fee6b-139">Les stratégies d’audit n’appliquent pas de règles de contrôle d’application et sont destinées à des fins de test afin d’identifier si une application nécessitera une exemption d’éditeur.</span><span class="sxs-lookup"><span data-stu-id="fee6b-139">Audit policies don't enforce app control rules and are meant for testing purposes to identify whether an application will require a publisher exemption.</span></span> <span data-ttu-id="fee6b-140">Il enregistre les avertissements (événements 8003 ou 8006) dans l’Observateur d’événements au lieu de bloquer l’exécution ou l’installation d’applications ou de scripts spécifiés.</span><span class="sxs-lookup"><span data-stu-id="fee6b-140">It logs warnings (8003 or 8006 events) in Event Viewer instead of blocking the execution or installation of specified apps or script.</span></span>

### <a name="enforced-policy"></a><span data-ttu-id="fee6b-141">Stratégie appliquée</span><span class="sxs-lookup"><span data-stu-id="fee6b-141">Enforced policy</span></span>
<span data-ttu-id="fee6b-142">Cette stratégie empêche l’exécution d’applications et de scripts non confiances et crée des journaux chaque fois qu’une application ou un script est bloqué.</span><span class="sxs-lookup"><span data-stu-id="fee6b-142">This policy blocks untrusted apps and scripts from running and creates logs whenever an app or script is blocked.</span></span> <span data-ttu-id="fee6b-143">Les stratégies appliquées empêchent les utilisateurs standard d’exécuter des applications ou des scripts stockés dans des répertoires accessibles en écriture par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fee6b-143">Enforced policies prevent standard users from executing apps or scripts stored in user-writable directories.</span></span>

<span data-ttu-id="fee6b-144">Une stratégie d’audit est appliquée aux appareils du groupe test afin que vous pouvez les utiliser pour vérifier si des applications entraîneront des problèmes.</span><span class="sxs-lookup"><span data-stu-id="fee6b-144">Devices in the Test group have an Audit policy applied so that you can use them to validate whether any applications will cause issues.</span></span> <span data-ttu-id="fee6b-145">Tous les autres groupes (First, Fast et Broad) utilisent une stratégie appliquée, afin que les utilisateurs de ces groupes ne puissent pas exécuter d’applications ou de scripts non confiance.</span><span class="sxs-lookup"><span data-stu-id="fee6b-145">All other groups (First, Fast, and Broad) use an Enforced policy, so users in those groups won't be able to run untrusted apps or scripts.</span></span>








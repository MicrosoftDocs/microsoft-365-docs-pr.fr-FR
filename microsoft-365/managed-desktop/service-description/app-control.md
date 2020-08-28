---
title: Contrôle des applications
description: ''
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.author: jaimeo
manager: laurawi
audience: ITpro
ms.topic: article
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 32ed3f95ebb4299796c5ad3eb71802c949701b65
ms.sourcegitcommit: abf63669daf12993ad3353e4b578f41c8910b20f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2020
ms.locfileid: "47289126"
---
# <a name="app-control"></a><span data-ttu-id="3d7dd-103">Contrôle des applications</span><span class="sxs-lookup"><span data-stu-id="3d7dd-103">App control</span></span>

<span data-ttu-id="3d7dd-104">Le contrôle d’application est une pratique de sécurité facultative dans Microsoft Managed Desktop qui limite l’exécution du code sur les appareils clients.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-104">App control is an optional security practice in Microsoft Managed Desktop that restricts the execution of code on client devices.</span></span> <span data-ttu-id="3d7dd-105">Ce contrôle réduit le risque de programmes malveillants ou de scripts malveillants en exigeant que seul le code signé par une liste d’éditeurs approuvés par le client puisse s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-105">This control mitigates the risk of malware or malicious scripts by requiring that only code signed by a customer-approved list of publishers can run.</span></span> <span data-ttu-id="3d7dd-106">Ce contrôle présente de nombreux avantages en matière de sécurité, mais il vise principalement à protéger les données et l’identité des attaques basées sur les clients.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-106">There are many security benefits from this control, but it primarily aims to protect data and identity from client-based exploits.</span></span>

<span data-ttu-id="3d7dd-107">Microsoft Managed Desktop simplifie la gestion des stratégies de contrôle d’application en créant une stratégie de base qui active les scénarios de productivité principaux.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-107">Microsoft Managed Desktop simplifies the management of app control policies by creating a base policy that enables core productivity scenarios.</span></span> <span data-ttu-id="3d7dd-108">Vous pouvez étendre l’approbation à des signataires supplémentaires spécifiques aux applications et aux scripts de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-108">You can extend trust to additional signers that are specific to the apps and scripts in your environment.</span></span> 


<span data-ttu-id="3d7dd-109">Toute technologie de sécurité nécessite un équilibre entre l’expérience utilisateur, la sécurité et les coûts.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-109">Any security technology requires a balance among user experience, security, and cost.</span></span> <span data-ttu-id="3d7dd-110">Le contrôle d’application réduit la menace de logiciels malveillants dans votre environnement, mais il y a des conséquences pour l’utilisateur et des actions supplémentaires pour votre administrateur informatique.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-110">App control reduces the threat of malicious software in your environment, but there are consequences to the user and additional actions for your IT administrator.</span></span>

<span data-ttu-id="3d7dd-111">**Sécurité supplémentaire :**</span><span class="sxs-lookup"><span data-stu-id="3d7dd-111">**Additional security:**</span></span>

<span data-ttu-id="3d7dd-112">Les applications ou les scripts qui ne sont pas approuvés par la stratégie de contrôle d’application ne sont pas exécutés sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-112">Apps or scripts that are not trusted by the app control policy are blocked from running on devices.</span></span>

<span data-ttu-id="3d7dd-113">**Vos responsabilités supplémentaires :**</span><span class="sxs-lookup"><span data-stu-id="3d7dd-113">**Your additional responsibilities:**</span></span>

- <span data-ttu-id="3d7dd-114">Vous êtes chargé de tester vos applications afin de déterminer si elles seraient bloquées par la stratégie de contrôle d’application.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-114">You are responsible for testing your apps to identify whether they would be blocked by the application control policy.</span></span>
- <span data-ttu-id="3d7dd-115">Si une application est bloquée (ou serait), vous devez identifier les informations de signataire nécessaires et demander une modification via le portail d’administration.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-115">If an app is (or would be) blocked, you are responsible for identifying the needed signer details and requesting a change through the Admin portal.</span></span>

<span data-ttu-id="3d7dd-116">**Responsabilités du bureau géré Microsoft :**</span><span class="sxs-lookup"><span data-stu-id="3d7dd-116">**Microsoft Managed Desktop responsibilities:**</span></span>

- <span data-ttu-id="3d7dd-117">Microsoft Managed Desktop gère la stratégie de base qui permet les principaux produits Microsoft tels que les applications M365, Windows, teams, OneDrive, etc.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-117">Microsoft Managed Desktop maintains the base policy that enables core Microsoft products like M365 Apps, Windows, Teams, OneDrive, and so on.</span></span>
- <span data-ttu-id="3d7dd-118">Le bureau géré Microsoft insère vos signataires approuvés et déploie la stratégie mise à jour sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-118">Microsoft Managed Desktop inserts your trusted signers and deploys the updated policy to your devices.</span></span>


## <a name="managing-trust-in-applications"></a><span data-ttu-id="3d7dd-119">Gestion de l’approbation dans les applications</span><span class="sxs-lookup"><span data-stu-id="3d7dd-119">Managing trust in applications</span></span>

<span data-ttu-id="3d7dd-120">Microsoft Managed Desktop organise une stratégie de base qui approuve les principaux composants des technologies Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-120">Microsoft Managed Desktop curates a base policy that trusts the core components of Microsoft technologies.</span></span> <span data-ttu-id="3d7dd-121">Vous pouvez ensuite *Ajouter* une approbation pour vos propres applications et scripts en informant le bureau géré Microsoft, dont vous avez déjà confiance.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-121">You then *add* trust for your own applications and scripts by informing Microsoft Managed Desktop which of them you already trust.</span></span>

### <a name="base-policy"></a><span data-ttu-id="3d7dd-122">Stratégie de base</span><span class="sxs-lookup"><span data-stu-id="3d7dd-122">Base policy</span></span>

<span data-ttu-id="3d7dd-123">Microsoft Managed Desktop, en collaboration avec les experts Microsoft Cybersecurity, crée et gère une stratégie standard qui permet le déploiement de la plupart des applications déployées via Microsoft Intune tout en bloquant les activités dangereuses telles que la compilation du code ou l’exécution de fichiers non approuvés.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-123">Microsoft Managed Desktop, in collaboration with Microsoft cybersecurity experts, creates and maintains a standard policy that enables most apps deployed through Microsoft Intune while blocking dangerous activities like code compilation or execution of untrusted files.</span></span>

<span data-ttu-id="3d7dd-124">La stratégie de base adopte l’approche suivante pour limiter l’exécution des logiciels :</span><span class="sxs-lookup"><span data-stu-id="3d7dd-124">The base policy takes the following approach to restricting software execution:</span></span>

- <span data-ttu-id="3d7dd-125">Les fichiers exécutés par les administrateurs sont autorisés à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-125">Files run by administrators will be allowed to run.</span></span>
- <span data-ttu-id="3d7dd-126">Les fichiers dans les emplacements qui *ne sont pas* dans les répertoires accessibles par l’utilisateur sont autorisés à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-126">Files in locations that are *not* in user-writable directories will be allowed to run.</span></span>
- <span data-ttu-id="3d7dd-127">Les fichiers sont signés par un [signataire approuvé](#signer-requests).</span><span class="sxs-lookup"><span data-stu-id="3d7dd-127">Files are signed by a [trusted signer](#signer-requests).</span></span>
- <span data-ttu-id="3d7dd-128">La plupart des fichiers signés par Microsoft s’exécuteront, mais certains sont bloqués pour empêcher les actions à haut risque telles que la compilation du code.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-128">Most files signed by Microsoft will run, however some are blocked to prevent high-risk actions like code compilation.</span></span>


<span data-ttu-id="3d7dd-129">Si un utilisateur autre qu’un administrateur peut avoir ajouté une application ou un script à un périphérique (c’est-à-dire s’il se trouve dans un répertoire accessible aux utilisateurs), nous ne l’autorisons pas à s’exécuter, sauf s’il a déjà été spécifiquement autorisé par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-129">If a user other than an administrator could have added an app or script to a device (that is, it's in a user-writable directory), we won't allow it to execute unless it has already been specifically allowed by an administrator.</span></span> <span data-ttu-id="3d7dd-130">Si un utilisateur est amené à essayer d’installer des programmes malveillants, si une vulnérabilité dans une application exécutée par l’utilisateur tente de procéder à des tentatives d’installation de programmes malveillants, ou si un utilisateur tente intentionnellement d’exécuter une application ou un script non autorisé, notre stratégie arrête l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-130">If a user is tricked into trying to install malware, if a vulnerability in an app the user runs attempts to install malware, or if a user intentionally tries to run an unauthorized app or script, our policy will stop execution.</span></span>

### <a name="signer-requests"></a><span data-ttu-id="3d7dd-131">Demandes de signataires</span><span class="sxs-lookup"><span data-stu-id="3d7dd-131">Signer requests</span></span>

<span data-ttu-id="3d7dd-132">Vous nous indiquez quelles applications sont fournies par des fournisseurs de logiciels que vous approuvez en *désignant une demande de signataire*.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-132">You inform us of which apps are provided by software vendors you trust by filing a *signer request*.</span></span> <span data-ttu-id="3d7dd-133">En procédant ainsi, nous ajoutons ces informations d’approbation dans la stratégie de contrôle d’application de référence et autorisons tout logiciel signé avec le certificat de cet éditeur à s’exécuter sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-133">By doing so, we add that trust information into the baseline application control policy and allow any software signed with that publisher's certificate to run on your devices.</span></span>

## <a name="audit-and-enforced-policies"></a><span data-ttu-id="3d7dd-134">Stratégies d’audit et appliquées</span><span class="sxs-lookup"><span data-stu-id="3d7dd-134">Audit and Enforced policies</span></span>

<span data-ttu-id="3d7dd-135">Microsoft Managed Desktop utilise deux stratégies Microsoft Intune pour fournir le contrôle de l’application :</span><span class="sxs-lookup"><span data-stu-id="3d7dd-135">Microsoft Managed Desktop uses two Microsoft Intune policies to provide app control:</span></span>

### <a name="audit-policy"></a><span data-ttu-id="3d7dd-136">Stratégie d’audit</span><span class="sxs-lookup"><span data-stu-id="3d7dd-136">Audit policy</span></span>
<span data-ttu-id="3d7dd-137">Cette stratégie crée des journaux pour enregistrer le blocage ou non d’une application ou d’un script par la stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-137">This policy creates logs to record whether an app or script would be blocked by the Enforced policy.</span></span> <span data-ttu-id="3d7dd-138">Les stratégies d’audit n’appliquent pas de règles de contrôle d’application et sont destinées à des fins de test pour déterminer si une application requiert une exemption de publication.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-138">Audit policies don't enforce app control rules and are meant for testing purposes to identify whether an application will require a publisher exemption.</span></span> <span data-ttu-id="3d7dd-139">Il consigne les avertissements (événements 8003 ou 8006) dans l’observateur d’événements au lieu de bloquer l’exécution ou l’installation d’applications ou de scripts spécifiés.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-139">It logs warnings (8003 or 8006 events) in Event Viewer instead of blocking the execution or installation of specified apps or script.</span></span>

### <a name="enforced-policy"></a><span data-ttu-id="3d7dd-140">Stratégie appliquée</span><span class="sxs-lookup"><span data-stu-id="3d7dd-140">Enforced policy</span></span>
<span data-ttu-id="3d7dd-141">Cette stratégie empêche les applications et les scripts non approuvés de s’exécuter et crée des journaux chaque fois qu’une application ou un script est bloqué.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-141">This policy blocks untrusted apps and scripts from running and creates logs whenever an app or script is blocked.</span></span> <span data-ttu-id="3d7dd-142">Les stratégies appliquées empêchent les utilisateurs standard d’exécuter des applications ou des scripts stockés dans des répertoires accessibles par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-142">Enforced policies prevent standard users from executing apps or scripts stored in user-writable directories.</span></span>

<span data-ttu-id="3d7dd-143">Les périphériques du groupe de test ont une stratégie d’audit appliquée afin que vous puissiez les utiliser pour vérifier si des applications génèrent des problèmes.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-143">Devices in the Test group have an Audit policy applied so that you can use them to validate whether any applications will cause issues.</span></span> <span data-ttu-id="3d7dd-144">Tous les autres groupes (First, Fast et large) utilisent une stratégie appliquée, de sorte que les utilisateurs de ces groupes ne puissent pas exécuter des applications ou des scripts non approuvés.</span><span class="sxs-lookup"><span data-stu-id="3d7dd-144">All other groups (First, Fast, and Broad) use an Enforced policy, so users in those groups won't be able to run untrusted apps or scripts.</span></span>








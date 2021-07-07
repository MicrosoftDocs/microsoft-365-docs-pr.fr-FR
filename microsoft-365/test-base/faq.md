---
title: Test Base FAQ
description: Passer en revue les questions fréquemment posées
search.appverid: MET150
author: mansipatel-usl
ms.author: mapatel
manager: rshastri
audience: Software-Vendor
ms.topic: troubleshooting
ms.date: 07/06/2021
ms.service: virtual-desktop
localization_priority: Normal
ms.collection: TestBase-M365
ms.custom: ''
ms.reviewer: mapatel
f1.keywords: NOCSH
ms.openlocfilehash: 9d24ecb807e60733471be60353d12789f19be1b4
ms.sourcegitcommit: b0f464b6300e2977ed51395473a6b2e02b18fc9e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53322924"
---
# <a name="test-base-faq"></a><span data-ttu-id="ffba8-103">Test Base FAQ</span><span class="sxs-lookup"><span data-stu-id="ffba8-103">Test Base FAQ</span></span>

<span data-ttu-id="ffba8-104">**Q : Comment envoyer nos packages à l’équipe de base de test ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-104">**Q: How do we submit our packages to Test Base team?**</span></span>

<span data-ttu-id="ffba8-105">**R :** Envoyez vos packages directement à l’environnement de base de test à l’aide de notre portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="ffba8-105">**A:** Submit your packages directly to the Test Base environment using our self-serve portal.</span></span>

<span data-ttu-id="ffba8-106">Pour soumettre votre package d’application, accédez au portail [Azure](https://www.aka.ms/testbaseportal "Page d’accueil de base de test") et téléchargez un dossier compressé contenant les fichiers binaires, les dépendances et les scripts de test de votre application via le tableau de bord du portail de base de test libre-service.</span><span class="sxs-lookup"><span data-stu-id="ffba8-106">To submit your application package, navigate to the [Azure Portal](https://www.aka.ms/testbaseportal "Test Base Homepage") and upload a zipped folder containing your application's binaries, dependencies, and test scripts via the self-serve Test Base portal dashboard.</span></span> 

<span data-ttu-id="ffba8-107">Consultez le guide de l’utilisateur d’intégration pour plus d’informations ou contactez notre équipe pour obtenir de <testbasepreview@microsoft.com> l’aide et plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ffba8-107">Please see the onboarding user guide for more information or contact our team at <testbasepreview@microsoft.com> for assistance and more information.</span></span>

<span data-ttu-id="ffba8-108">**Q : Que sont les tests OOB ( Out-of-Box) ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-108">**Q: What are Out-of-box (OOB) tests?**</span></span>

<span data-ttu-id="ffba8-109">**R :** Les tests prêts à l’emploi (OOB) sont standardisés, les tests par défaut s’exécutent lorsque les packages d’application sont installés, lancés et fermés trente (30) fois, puis désinstallés.</span><span class="sxs-lookup"><span data-stu-id="ffba8-109">**A:** Out-of-box (OOB) tests are standardized, default test runs where application packages are installed, launched and closed thirty (30) times, and then uninstalled.</span></span> 

<span data-ttu-id="ffba8-110">Les packages créés pour la base de test auront les scripts de test suivants : installer, lancer, fermer et éventuellement le script de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="ffba8-110">The packages created for Test Base will have the following test scripts: install, launch, close, and optionally the uninstall script.</span></span> 

<span data-ttu-id="ffba8-111">Les tests OOB (Out-of-Box) vous fournissent une télémétrie normalisée sur votre application à comparer entre Windows builds.</span><span class="sxs-lookup"><span data-stu-id="ffba8-111">The Out-of-box (OOB) tests provide you with standardized telemetry on your application to compare across Windows builds.</span></span>

<span data-ttu-id="ffba8-112">**Q : Pouvons-nous soumettre des tests en dehors des tests pré-box (installer, lancer, fermer, désinstaller des scripts de test) ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-112">**Q: Can we submit tests outside of the Out-of-box tests (install, launch, close, uninstall test scripts)?**</span></span>

<span data-ttu-id="ffba8-113">**R :** Oui, les clients peuvent également télécharger des packages d’application pour les **tests fonctionnels** via le tableau de bord du portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="ffba8-113">**A:** Yes, customers can also upload application packages for **functional tests** via the self-serve portal dashboard.</span></span>
<span data-ttu-id="ffba8-114">**Les tests fonctionnels** sont des tests qui permettent aux clients d’exécuter leurs scripts pour exécuter des fonctionnalités personnalisées sur leur application.</span><span class="sxs-lookup"><span data-stu-id="ffba8-114">**Functional tests** are tests that enable customers execute their scripts to run custom functionality on their application.</span></span>


## <a name="testing"></a><span data-ttu-id="ffba8-115">Tests</span><span class="sxs-lookup"><span data-stu-id="ffba8-115">Testing</span></span>

<span data-ttu-id="ffba8-116">**Q : Les tests fonctionnels sont-ils nécessaires ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-116">**Q: Do you support functional tests?**</span></span>

<span data-ttu-id="ffba8-117">**R :** Oui, la base de test prend en charge les tests fonctionnels.</span><span class="sxs-lookup"><span data-stu-id="ffba8-117">**A:** Yes, Test Base supports functional tests.</span></span> <span data-ttu-id="ffba8-118">Les tests fonctionnels sont des tests qui permettent à nos clients d’exécuter leurs scripts pour exécuter des fonctionnalités personnalisées sur leur application.</span><span class="sxs-lookup"><span data-stu-id="ffba8-118">Functional tests are tests that enable our customers execute their scripts to run custom functionality on their application.</span></span> 

<span data-ttu-id="ffba8-119">Pour soumettre votre package d’application à des tests fonctionnels, téléchargez simplement le dossier compressé contenant les fichiers binaires, les dépendances et les scripts de test de votre application via notre tableau de bord du portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="ffba8-119">To submit your application package for functional testing, simply upload the zipped folder containing your application's binaries, dependencies, and test scripts via our self-serve portal dashboard.</span></span> 

<span data-ttu-id="ffba8-120">Consultez le guide de l’utilisateur d’intégration pour plus d’informations ou contactez notre équipe pour obtenir de <testbasepreview@microsoft.com> l’aide et plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ffba8-120">Please see the onboarding user guide for more information or contact our team at <testbasepreview@microsoft.com> for assistance and more information.</span></span>

<span data-ttu-id="ffba8-121">**Q : Comment la base de test gère-t-elle nos données de test ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-121">**Q: How does Test Base handle our test data?**</span></span>

<span data-ttu-id="ffba8-122">**R :** Test Base collecte et gère en toute sécurité vos données de test dans l’environnement Azure.</span><span class="sxs-lookup"><span data-stu-id="ffba8-122">**A:** Test Base securely collects and manages your test data on the Azure environment.</span></span> 

<span data-ttu-id="ffba8-123">**Q : La base de test peut-elle prendre en charge nos tests automatisés ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-123">**Q: Can Test Base support our automated tests?**</span></span>

<span data-ttu-id="ffba8-124">Oui, la base de test prend en charge les tests automatisés, mais nous ne prend pas en charge les tests manuels pour le moment en raison des fonctionnalités de service.</span><span class="sxs-lookup"><span data-stu-id="ffba8-124">Yes, Test Base supports automated tests however, we do not support manual tests at this time due to service capabilities.</span></span>

<span data-ttu-id="ffba8-125">**Q : Quelles sont les langues et les frameworks des tests automatisés que vous prisez en charge ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-125">**Q: What languages and frameworks of automated tests do you support?**</span></span>

<span data-ttu-id="ffba8-126">**R :** Nous supportons toutes les langues et toutes les infrastructure.</span><span class="sxs-lookup"><span data-stu-id="ffba8-126">**A:** We support all languages and frameworks.</span></span> <span data-ttu-id="ffba8-127">Nous appelons tous les scripts via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ffba8-127">We invoke all scripts through PowerShell.</span></span> 

<span data-ttu-id="ffba8-128">Vous devez également fournir (télécharger) les fichiers binaires dépendants de l’infrastructure requise.</span><span class="sxs-lookup"><span data-stu-id="ffba8-128">You will also need to provide (upload) the dependent binaries of the required framework.</span></span>

<span data-ttu-id="ffba8-129">**Q : À combien de temps la Base de test fournit-elle les résultats des tests ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-129">**Q: How soon does Test Base provide test results?**</span></span>

<span data-ttu-id="ffba8-130">**R :** Pour chaque test que nous exécuterons sur les builds pré-publiées, nous fournirons des résultats dans les 48 heures sur votre tableau de bord [du portail Azure.](https://www.aka.ms/testbaseportal "Page d’accueil de base de test")</span><span class="sxs-lookup"><span data-stu-id="ffba8-130">**A:** For each test that we run against the pre-release builds, we will provide results within 48 hours on your [Azure Portal](https://www.aka.ms/testbaseportal "Test Base Homepage") dashboard.</span></span>

<span data-ttu-id="ffba8-131">**Q : Pouvez-vous redémarrer après l’installation ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-131">**Q: Can you reboot after install?**</span></span>

<span data-ttu-id="ffba8-132">**R :** Oui, notre processus prend en charge le redémarrage après l’installation.</span><span class="sxs-lookup"><span data-stu-id="ffba8-132">**A:** Yes, our process supports rebooting after installation.</span></span> <span data-ttu-id="ffba8-133">N’oubliez pas de sélectionner cette option dans la liste d’attente « Paramètres facultatifs » lors de la définition de vos tâches **sur** le portail d’intégration.</span><span class="sxs-lookup"><span data-stu-id="ffba8-133">Be sure to select this option from the “Optional settings” drop list when setting your **Tasks** on the onboarding portal.</span></span>

<span data-ttu-id="ffba8-134">Pour les tests OOB (Out-of-Box), vous pouvez spécifier si un redémarrage est nécessaire pour le _script d’installation._</span><span class="sxs-lookup"><span data-stu-id="ffba8-134">For Out-of-box (OOB) tests, you can specify whether a reboot is needed for the _Install script._</span></span>

![Image de redémarrage](Media/reboot.png)

<span data-ttu-id="ffba8-136">Pour les tests fonctionnels, vous pouvez spécifier si un redémarrage est requis pour chaque script ajouté.</span><span class="sxs-lookup"><span data-stu-id="ffba8-136">While for functional tests, you can specify whether a reboot is required for each script that is added.</span></span>

![Comment sélectionner des tests fonctionnels](Media/functionalreboot.png)

<span data-ttu-id="ffba8-138">**Q : Quelles versions Windows-vous prise en charge ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-138">**Q: What Windows versions do you support?**</span></span>

<span data-ttu-id="ffba8-139">**R :** Nous ons actuellement Windows 10 clients, Windows Server 2016, Windows Server 2016 Core version, Windows Server 2019 et Windows Server 2019 Core.</span><span class="sxs-lookup"><span data-stu-id="ffba8-139">**A:** We currently support Windows 10 clients, Windows Server 2016, Windows Server 2016 Core version, Windows Server 2019, and Windows Server 2019 Core version.</span></span>

<span data-ttu-id="ffba8-140">**Q : Quelle est la différence entre les tests de mise à jour de sécurité et les tests de mise à jour des fonctionnalités ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-140">**Q: What is the difference between Security Update tests and Feature Update tests?**</span></span>

<span data-ttu-id="ffba8-141">**R :** Pour les tests de mise à jour de sécurité, nous testons les mises à jour de sécurité mensuelles pré-publiées sur Windows qui sont **<ins>axées</ins>** sur le maintien de la sécurité et de la protection de nos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ffba8-141">**A:** For Security update tests, we test against the **<ins>monthly pre-release security updates</ins>** on Windows which are focused on keeping our users always secure and protected.</span></span> <span data-ttu-id="ffba8-142">Pour les tests de mise à jour des fonctionnalités, nous testons les mises à jour de fonctionnalités de **<ins>pré-publication bi-annuelles</ins>** qui introduisent de nouvelles fonctionnalités et fonctionnalités sur Windows.</span><span class="sxs-lookup"><span data-stu-id="ffba8-142">For the Feature update tests, we test against the **<ins>bi-annual pre-release feature updates</ins>** which introduces new features and capabilities on Windows.</span></span>

## <a name="debugging-options"></a><span data-ttu-id="ffba8-143">Options de débogage</span><span class="sxs-lookup"><span data-stu-id="ffba8-143">Debugging options</span></span>

<span data-ttu-id="ffba8-144">**Q : Avons-nous accès aux machines virtuelles (VM) en cas de défaillance ? Qu’est-ce que le partage de base de test ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-144">**Q: Do we get access to the Virtual Machines (VMs) in case of failures? What does Test Base share?**</span></span>

<span data-ttu-id="ffba8-145">**R :** Pour que le service soit conforme et que les mises à jour pré-publiées soient sécurisées, seule Microsoft a accès aux VM.</span><span class="sxs-lookup"><span data-stu-id="ffba8-145">**A:** For the service to be compliant and the pre-release updates be secure, only Microsoft has access to the VMs.</span></span> <span data-ttu-id="ffba8-146">Toutefois, les clients peuvent afficher les résultats des tests et d’autres mesures de test sur leur tableau de bord du portail, notamment les signaux d’incident et de panne, les mesures de fiabilité, l’utilisation de la mémoire et du processeur, etc. Nous générons et fournissons également les journaux des séries de tests sur le tableau de bord pour téléchargement et analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="ffba8-146">However, customers can view test results and other test metrics on their portal dashboard, including crash and hang signals, reliability metrics, memory and CPU utilization etc. We also generate and provide logs of test runs on the dashboard for download and further analysis.</span></span> 

<span data-ttu-id="ffba8-147">Nous pouvons également fournir des vidages mémoire pour le débogage sur incident si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ffba8-147">We can also provide memory dumps for crash debugging as needed.</span></span>

<span data-ttu-id="ffba8-148">**Q : Si des problèmes se sont produits pendant le test, quelles sont les étapes suivantes pour résoudre ces problèmes ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-148">**Q: If there are issues found during the testing, what are the next steps to resolve these issues?**</span></span>

<span data-ttu-id="ffba8-149">**R :** L’équipe de base de test effectuera un processus de tri initial pour déterminer la cause première de l’erreur, puis en fonction de nos résultats, nous effectuerons un itinéraire vers le client ou les équipes internes au sein de Microsoft pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="ffba8-149">**A:** The Test Base team will perform an initial triage process to determine the root cause of the error, and then depending on our findings, we will route to the customer or internal teams within Microsoft for debugging.</span></span> 

<span data-ttu-id="ffba8-150">Nous travaillons toujours en étroite collaboration avec nos clients pour résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="ffba8-150">We always work closely with our customers in joint remediation to resolve any issues.</span></span> 

<span data-ttu-id="ffba8-151">**Q : Microsoft tient-il la publication du correctif de sécurité jusqu’à ce que le problème soit résolu ? Quelles autres résolutions sont disponibles ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-151">**Q: Does Microsoft hold the release of the security patch until the issue is resolved? What alternate resolutions are available?**</span></span>

<span data-ttu-id="ffba8-152">**R :** L’objectif de la base de test est de s’assurer que nos clients finaux conjoints ne rencontrent aucun problème.</span><span class="sxs-lookup"><span data-stu-id="ffba8-152">**A:** The goal of Test Base is to ensure our joint end customers do not face any issues.</span></span> <span data-ttu-id="ffba8-153">Nous travaillerons en dur avec les éditeurs de logiciels pour résoudre les problèmes avant la publication, mais au cas où le correctif ne serait pas réalisable, nous avons d’autres résolutions telles que les shims et les blocs.</span><span class="sxs-lookup"><span data-stu-id="ffba8-153">We will work hard with Software Vendors to address any issues before the release, but in case the fix is not feasible we have other resolutions such as shims and blocks.</span></span>

## <a name="miscellaneous"></a><span data-ttu-id="ffba8-154">Divers</span><span class="sxs-lookup"><span data-stu-id="ffba8-154">Miscellaneous</span></span>

<span data-ttu-id="ffba8-155">**Q : Comment le service fonctionne-t-il avec un serveur sur place ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-155">**Q: How will the service work with an on-prem server?**</span></span>

<span data-ttu-id="ffba8-156">**R :** Pour l’instant, nous ne donnent pas de prise en charge des serveurs sur site.</span><span class="sxs-lookup"><span data-stu-id="ffba8-156">**A:** We currently do not provide support for on-prem servers.</span></span> <span data-ttu-id="ffba8-157">Toutefois, si le serveur expose le point de terminaison HTTP, nous pouvons nous y connecter via Internet.</span><span class="sxs-lookup"><span data-stu-id="ffba8-157">However, if the server is exposing HTTP endpoint, we can connect to it over the internet.</span></span>

<span data-ttu-id="ffba8-158">**Q : Qui héberger les VM ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-158">**Q: Who hosts the VMs?**</span></span>

<span data-ttu-id="ffba8-159">**R :** Microsoft propose la VM pour ce service, en prenant la charge de cette fonction du client.</span><span class="sxs-lookup"><span data-stu-id="ffba8-159">**A:** Microsoft provisions the VM for this service, taking the load of doing so from the customer.</span></span>

<span data-ttu-id="ffba8-160">**Q : Ce service prend-il en charge les applications web, mobiles ou de bureau ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-160">**Q: Does this service support web, mobile, or desktop applications?**</span></span>

<span data-ttu-id="ffba8-161">**R :** Pour l’instant, nous nous concentrons sur les applications de bureau. Toutefois, nous envisageons d’intégrer des applications web à l’avenir, mais nous ne prisent pas en charge les applications mobiles pour le moment.</span><span class="sxs-lookup"><span data-stu-id="ffba8-161">**A:** Currently, our focus is on desktop applications, however, we have plans to onboard web applications in the future, but we do not support mobile applications at this time.</span></span>

<span data-ttu-id="ffba8-162">**Q : Quelle est la différence entre Test Base et LAPX ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-162">**Q: What is the difference between Test Base and SUVP?**</span></span>

<span data-ttu-id="ffba8-163">**R :** La principale différence entre base de test et LAPSP est que nos partenaires ententent leurs applications dans l’environnement Azure de base de test pour la validation s’exécute sur les mises à jour pré-publiées au lieu d’effectuer les tests eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="ffba8-163">**A:** The biggest difference between Test Base and SUVP is that our partners onboard their applications onto the Test Base Azure environment for validation runs against pre-release updates instead of carrying out the tests themselves.</span></span> 

<span data-ttu-id="ffba8-164">En plus des tests de mises à jour de sécurité pré-publiées, nous prise en charge des tests de mises à jour de fonctionnalités pré-publiées sur notre plateforme.</span><span class="sxs-lookup"><span data-stu-id="ffba8-164">In addition to pre-release security updates testing, we support pre-release feature updates testing on our platform.</span></span> <span data-ttu-id="ffba8-165">Nous avons de nombreux autres types de mises à jour et de tests de système d’exploitation dans notre feuille de route.</span><span class="sxs-lookup"><span data-stu-id="ffba8-165">We have many other types of updates and OS testing on our roadmap.</span></span>

<span data-ttu-id="ffba8-166">**Q : Existe-t-il un coût associé au service ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-166">**Q: Is there a cost associated with the service?**</span></span>

<span data-ttu-id="ffba8-167">**R :** Le service de base de test sera gratuit pour les utilisateurs jusqu’à la disponibilité générale.</span><span class="sxs-lookup"><span data-stu-id="ffba8-167">**A:** The Test Base service will be free to users until General Availability (GA).</span></span> <span data-ttu-id="ffba8-168">À ce moment-là, nous annoncerons une structure de coûts qui sera en vigueur pour tous les clients.</span><span class="sxs-lookup"><span data-stu-id="ffba8-168">At that time, we will announce a cost structure that will be in effect for all customers.</span></span> 

<span data-ttu-id="ffba8-169">**Q : Comment puis-je fournir des commentaires sur la Base de test ?**</span><span class="sxs-lookup"><span data-stu-id="ffba8-169">**Q: How can I provide feedback about Test Base?**</span></span>

<span data-ttu-id="ffba8-170">**R :** Pour partager vos commentaires sur la base de test, sélectionnez l’icône **Commentaires** en bas à gauche du portail.</span><span class="sxs-lookup"><span data-stu-id="ffba8-170">**A:** To share your feedback about Test Base, select the **Feedback** icon at the bottom left of the portal.</span></span> <span data-ttu-id="ffba8-171">Incluez une capture d’écran avec votre soumission pour aider Microsoft à mieux comprendre vos commentaires.</span><span class="sxs-lookup"><span data-stu-id="ffba8-171">Include a screenshot with your submission to help Microsoft better understand your feedback.</span></span> 

<span data-ttu-id="ffba8-172">Vous pouvez également soumettre des suggestions de produit et soumettre d’autres idées sur <testbasepreview@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="ffba8-172">You can also submit product suggestions and upvote other ideas at <testbasepreview@microsoft.com>.</span></span>

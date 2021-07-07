---
title: Analyse de la régression du processeur
description: Comprendre les résultats et les mesures de régression pour la consommation du processeur
search.appverid: MET150
author: mansipatel-usl
ms.author: mapatel
manager: rshastri
audience: Software-Vendor
ms.topic: how-to
ms.date: 07/06/2021
ms.service: virtual-desktop
localization_priority: Normal
ms.collection: TestBase-M365
ms.custom: ''
ms.reviewer: mapatel
f1.keywords: NOCSH
ms.openlocfilehash: bc28c128902ae353fb35c3b6010856ade934a436
ms.sourcegitcommit: b0f464b6300e2977ed51395473a6b2e02b18fc9e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53322718"
---
# <a name="intelligent-cpu-regression-analysis"></a><span data-ttu-id="fc0a4-103">Analyse intelligente de la régression du processeur</span><span class="sxs-lookup"><span data-stu-id="fc0a4-103">Intelligent CPU regression analysis</span></span>

<span data-ttu-id="fc0a4-104">L’utilisation du processeur peut indiquer si une application est affectée par une mise à jour du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-104">CPU utilization can indicate whether an application is affected by an operating system update.</span></span> 

<span data-ttu-id="fc0a4-105">La Base de test pour Microsoft 365 fournit aux développeurs de logiciels un aperçu des régressions des performances du processeur qui se produisent lorsque leur application s’exécute sur différentes versions d’une mise à jour du système d’exploitation Windows à venir.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-105">Test Base for Microsoft 365 provides software developers with an insight into CPU performance regressions which occur when their application is running on different versions of an upcoming Windows Operating System (OS) update.</span></span> 

<span data-ttu-id="fc0a4-106">Ces régressions du processeur permettent aux développeurs de détecter et de résoudre les problèmes d’application (et les échecs potentiels) avant le déploiement de la mise à jour du système d’exploitation à grande étendue, empêchant ainsi une mauvaise expérience pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-106">These CPU regressions enable developers to detect and resolve application issues (and potential failures) before the OS update is deployed broadly, thus preventing a bad experience for the end user.</span></span>


### <a name="how-cpu-regression-analysis-works"></a><span data-ttu-id="fc0a4-107">Fonctionnement de l’analyse de la régression du processeur</span><span class="sxs-lookup"><span data-stu-id="fc0a4-107">How CPU regression analysis works</span></span> ###

<span data-ttu-id="fc0a4-108">En tant qu’utilisateur de base de test, vous pouvez télécharger les fichiers binaires de votre application (dans un seul fichier .zip), ainsi que les scripts de test associés et sélectionner la version du système d’exploitation Windows par rapport à laquelle vous souhaitez tester votre application sur le portail de base de test sur Azure.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-108">As a Test Base user, you can upload your application's binaries (in a single .zip file), along with associated test scripts and select the Windows OS version against which you would like to test your application on the Test Base portal on Azure.</span></span> 

<span data-ttu-id="fc0a4-109">Le service de base de test exécute ensuite les scripts de test et effectue l’analyse de régression **de l’UC.**</span><span class="sxs-lookup"><span data-stu-id="fc0a4-109">The Test Base service then runs the test scripts and performs the **CPU Regression Analysis**.</span></span> 

<span data-ttu-id="fc0a4-110">Le service vérifie si l’utilisation du processeur pour l’application sur la version pré-publiée de la mise à jour du système d’exploitation cible est conforme à l’utilisation du processeur pour la version finale du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-110">The service checks if the CPU utilization for the application on the pre-release version of the update for the target OS is in line with the CPU utilization for the released version of the OS.</span></span> 

<span data-ttu-id="fc0a4-111">L’utilisation du processeur n’est pas une comparaison comparable à 100 %, car les processus en cours d’exécution sur les deux versions du système d’exploitation peuvent ou ne pas correspondre exactement en raison de différentes versions du système d’exploitation . toutefois, l’analyse effectuée par la base de test peut vous montrer si l’utilisation du processeur pour votre application est impactée par une prochaine mise à jour du système d’exploitation et spécifiquement les processus qui ont régressé par rapport aux précédentes séries de tests.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-111">CPU utilization is not a 100% like-for-like comparison because the processes running on the two versions of the OS may or may not be an exact match due to differing OS versions; however, the analysis performed by Test Base can show you whether CPU utilization for your application is impacted by an upcoming OS update and specifically which processes have regressed from previous test runs.</span></span>

<span data-ttu-id="fc0a4-112">Dans la capture instantanée ci-dessous, il existe deux version du système d’exploitation par rapport à laquelle les utilisations processeur sont comparées pour la même application.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-112">In the snapshot below, there are two OS releases against which the CPU utilizations are compared for the same application.</span></span> 
-   <span data-ttu-id="fc0a4-113">L’onglet Utilisation du processeur affiche respectivement les limites supérieure et inférieure de l’utilisation pour les deux sorties au 90e et au 10e centile.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-113">The CPU utilization tab shows the upper and lower bounds of utilization for both releases at 90th and 10th percentiles respectively.</span></span> 
-   <span data-ttu-id="fc0a4-114">Les graphiques indiquent la série de temps d’utilisation du processeur ainsi que l’utilisation moyenne.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-114">The graphs show the time series of CPU utilization along with the average utilization.</span></span> 

<span data-ttu-id="fc0a4-115">Les clients peuvent désormais utiliser cette fonctionnalité pour déterminer si l’utilisation processeur de leur application est impactée par les mises à jour du système d’exploitation et plus précisément les processus qui ont régressé par rapport à leur exécution précédente.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-115">Customers can now use the functionality to determine if their application's CPU utilization is impacted by OS updates and specifically which processes have regressed from their previous execution.</span></span>


![Analyse de la régression du processeur](Media/cpu-regression-analysis.jpg)

### <a name="relevant-process-identification"></a><span data-ttu-id="fc0a4-117">Identification de processus pertinente</span><span class="sxs-lookup"><span data-stu-id="fc0a4-117">Relevant Process Identification</span></span> ###

<span data-ttu-id="fc0a4-118">Ici, nous abordons comment identifier les processus régressés dans l’application.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-118">Here, we discuss how to identify regressed processes in the application.</span></span> 

<span data-ttu-id="fc0a4-119">L’analyse de la régression des performances nécessite le suivi de différents types de compteurs de performance pour chaque processus exécuté sur une machine virtuelle pendant l’exécution du test.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-119">Analyzing performance regression requires tracking different kinds of performance counters for every process running on a virtual machine during the test run.</span></span> 

<span data-ttu-id="fc0a4-120">Cette analyse capture un grand nombre de variables pour un grand nombre de processus pour une application donnée.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-120">Such analysis captures a lot of variables for a lot of processes for a given application.</span></span> <span data-ttu-id="fc0a4-121">Tous les processus ne sont pas associés à une application ou à une application.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-121">Not all processes are associated with a run or application.</span></span> <span data-ttu-id="fc0a4-122">Pour contourner ce problème, un algorithme de classement des informations mutuelle utilisant la probabilité et la théorie de l’information est appliqué pour déterminer les processus les plus pertinents pour une application donnée.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-122">To work around this challenge, a mutual information ranking algorithm using probability and information theory is applied to figure out which processes are most relevant for a given application.</span></span> 

<span data-ttu-id="fc0a4-123">Une application peut être considérée comme un type de variable aléatoire discrète tandis qu’un processus est considéré comme un autre type de variable aléatoire discrète.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-123">An application can be considered one type of discrete random variable while a process is considered another kind of discrete random variable.</span></span> <span data-ttu-id="fc0a4-124">L’association des deux variables aléatoires est mesurée à l’aide de probabilités conditionnelles pour la pertinence.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-124">The association of the two random variables is measured using conditional probabilities for relevance.</span></span> 

<span data-ttu-id="fc0a4-125">Les processus sont ensuite affichés dans l’ordre de leur pertinence pour chaque application.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-125">Processes are then displayed in the order of their relevance for each application.</span></span> <span data-ttu-id="fc0a4-126">Vous pouvez également favori un sous-ensemble de processus qui peuvent être surveillés, par défaut, ainsi que des processus pertinents pour l’analyse de la régression du processeur.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-126">You can also favorite a subset of processes that can be monitored, by default, along with relevant processes for CPU regression analysis.</span></span> <span data-ttu-id="fc0a4-127">Une fois qu’une régression est détectée, vous pouvez télécharger la boîte à outils de l’analyseur de performances Windows et analyser les raisons de la régression des performances du processeur.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-127">Once a regression is detected, you can download the Windows Performance Analyzer toolkit and analyze reasons for CPU performance regressions.</span></span> 

<span data-ttu-id="fc0a4-128">L Windows Performance Analyzer prend le journal de suivi des événements (ETL) comme entrées et ces fichiers .etl sont disponibles dans les fichiers journaux téléchargeables pour les tests s’exécutent sur le portail.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-128">The Windows Performance Analyzer takes event trace log (ETL) as inputs and these .etl files are available in the log files downloadable for test runs on the portal.</span></span> <span data-ttu-id="fc0a4-129">Si vous souhaitez en savoir plus sur le débogage des performances du processeur, consultez la documentation Windows Performance Analyzer.</span><span class="sxs-lookup"><span data-stu-id="fc0a4-129">If you would like to know more about debugging CPU performance, see the Windows Performance Analyzer documentation.</span></span>


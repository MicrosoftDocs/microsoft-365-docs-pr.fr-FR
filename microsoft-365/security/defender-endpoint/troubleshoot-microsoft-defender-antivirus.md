---
title: ID d’événement et codes d’erreur de l’Antivirus Microsoft Defender
description: Rechercher les causes et les solutions pour les erreurs et les ID Antivirus Microsoft Defender événements
keywords: événement, code d’erreur, siem, journalisation, résolution des problèmes, wef, forwarding d’événement Windows
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 09/11/2018
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.topic: article
ms.openlocfilehash: cd222760f3a5cc005c679bf28365237cc70e8950
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52275347"
---
# <a name="review-event-logs-and-error-codes-to-troubleshoot-issues-with-microsoft-defender-antivirus"></a><span data-ttu-id="0096a-104">Consulter les journaux d'événements et les codes d'erreur pour résoudre les problèmes liés à l'antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="0096a-104">Review event logs and error codes to troubleshoot issues with Microsoft Defender Antivirus</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="0096a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0096a-105">**Applies to:**</span></span>

- [<span data-ttu-id="0096a-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0096a-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="0096a-107">Si vous rencontrez un problème avec Antivirus Microsoft Defender, vous pouvez rechercher dans les tableaux de cette rubrique un problème correspondant et une solution potentielle.</span><span class="sxs-lookup"><span data-stu-id="0096a-107">If you encounter a problem with Microsoft Defender Antivirus, you can search the tables in this topic to find a matching issue and potential solution.</span></span>

<span data-ttu-id="0096a-108">La liste des tableaux :</span><span class="sxs-lookup"><span data-stu-id="0096a-108">The tables list:</span></span>

- <span data-ttu-id="0096a-109">[Antivirus Microsoft Defender’événement (s’appliquent](#windows-defender-av-ids) aux deux Windows 10 et Windows Server 2016)</span><span class="sxs-lookup"><span data-stu-id="0096a-109">[Microsoft Defender Antivirus event IDs](#windows-defender-av-ids) (these apply to both Windows 10 and Windows Server 2016)</span></span>
- [<span data-ttu-id="0096a-110">Antivirus Microsoft Defender codes d’erreur client</span><span class="sxs-lookup"><span data-stu-id="0096a-110">Microsoft Defender Antivirus client error codes</span></span>](#error-codes)
- [<span data-ttu-id="0096a-111">Codes d Antivirus Microsoft Defender client interne (utilisés par Microsoft pendant le développement et les tests)</span><span class="sxs-lookup"><span data-stu-id="0096a-111">Internal Microsoft Defender Antivirus client error codes (used by Microsoft during development and testing)</span></span>](#internal-error-codes)

> [!TIP]
> <span data-ttu-id="0096a-112">Vous pouvez également consulter le site web de démonstration microsoft Defender pour points de terminaison [sur demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) pour vérifier que les fonctionnalités suivantes fonctionnent :</span><span class="sxs-lookup"><span data-stu-id="0096a-112">You can also visit the Microsoft Defender for Endpoint demo website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to confirm the following features are working:</span></span>
> 
> - <span data-ttu-id="0096a-113">Protection fournie par le cloud</span><span class="sxs-lookup"><span data-stu-id="0096a-113">Cloud-delivered protection</span></span>
> - <span data-ttu-id="0096a-114">Apprentissage rapide (y compris Bloquer à la première vue)</span><span class="sxs-lookup"><span data-stu-id="0096a-114">Fast learning (including Block at first sight)</span></span>
> - <span data-ttu-id="0096a-115">Blocage d’applications potentiellement indésirables</span><span class="sxs-lookup"><span data-stu-id="0096a-115">Potentially unwanted application blocking</span></span>

<a id="windows-defender-av-ids"></a>
## <a name="microsoft-defender-antivirus-event-ids"></a><span data-ttu-id="0096a-116">Antivirus Microsoft Defender’événement</span><span class="sxs-lookup"><span data-stu-id="0096a-116">Microsoft Defender Antivirus event IDs</span></span>

<span data-ttu-id="0096a-117">Antivirus Microsoft Defender les ID d’événement dans le journal Windows événements.</span><span class="sxs-lookup"><span data-stu-id="0096a-117">Microsoft Defender Antivirus records event IDs in the Windows event log.</span></span>

<span data-ttu-id="0096a-118">Vous pouvez afficher directement le journal des événements, ou si vous avez un outil tiers de gestion des événements et des informations de sécurité (SIEM), vous pouvez également utiliser des ID d’événement client Antivirus Microsoft Defender pour passer en revue des événements et des [erreurs](troubleshoot-microsoft-defender-antivirus.md#windows-defender-av-ids) spécifiques à partir de vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0096a-118">You can directly view the event log, or if you have a third-party security information and event management (SIEM) tool, you can also consume [Microsoft Defender Antivirus client event IDs](troubleshoot-microsoft-defender-antivirus.md#windows-defender-av-ids) to review specific events and errors from your endpoints.</span></span>

<span data-ttu-id="0096a-119">Le tableau de cette section répertorie les principaux ID d’Antivirus Microsoft Defender et, dans la mesure du possible, fournit des solutions suggérées pour corriger ou résoudre l’erreur.</span><span class="sxs-lookup"><span data-stu-id="0096a-119">The table in this section lists the main Microsoft Defender Antivirus event IDs and, where possible, provides suggested solutions to fix or resolve the error.</span></span> 

## <a name="to-view-a-microsoft-defender-antivirus-event"></a><span data-ttu-id="0096a-120">Pour afficher un événement Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="0096a-120">To view a Microsoft Defender Antivirus event</span></span>

1.  <span data-ttu-id="0096a-121">Ouvrez **l’Observateur d’événements.**</span><span class="sxs-lookup"><span data-stu-id="0096a-121">Open **Event Viewer**.</span></span>
2.  <span data-ttu-id="0096a-122">Dans l’arborescence de la console, développez **Journaux des applications** et des services, puis **Microsoft,** **puis Windows**, **puis Windows Defender**.</span><span class="sxs-lookup"><span data-stu-id="0096a-122">In the console tree, expand **Applications and Services Logs**, then **Microsoft**, then **Windows**, then **Windows Defender**.</span></span>
3.  <span data-ttu-id="0096a-123">Double-cliquez sur **Opérationnel**.</span><span class="sxs-lookup"><span data-stu-id="0096a-123">Double-click on **Operational**.</span></span>
4.  <span data-ttu-id="0096a-124">Dans le volet d’informations, affichez la liste des événements individuels pour trouver votre événement.</span><span class="sxs-lookup"><span data-stu-id="0096a-124">In the details pane, view the list of individual events to find your event.</span></span>
5.  <span data-ttu-id="0096a-125">Cliquez sur l’événement pour voir des détails spécifiques  sur un événement dans le volet inférieur, sous les **onglets** Général et Détails.</span><span class="sxs-lookup"><span data-stu-id="0096a-125">Click the event to see specific details about an event in the lower pane, under the **General** and **Details** tabs.</span></span>

<table> 
<tr>
<th colspan="2" ><span data-ttu-id="0096a-126">ID d’événement : 1000</span><span class="sxs-lookup"><span data-stu-id="0096a-126">Event ID: 1000</span></span></th>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-127">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-127">Symbolic name:</span></span>
</td>
<td><span data-ttu-id="0096a-128">
<b>MALWAREPROTECTION_SCAN_STARTED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-128">
<b>MALWAREPROTECTION_SCAN_STARTED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-129">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-129">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-130">
<b>Une analyse anti-programme malveillant a démarré. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-130">
<b>An antimalware scan started. </b>
</span></span></td>
</tr>
<tr>
<td >
<span data-ttu-id="0096a-131">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-131">Description:</span></span>
</td>
<td >
<dl><span data-ttu-id="0096a-132">
<dt>ID d’analyse : &lt; Numéro d’ID de &gt; l’analyse pertinente.</dt> 
<dt> Type d’analyse &lt; : type &gt; d’analyse, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-132">
<dt>Scan ID: &lt;ID number of the relevant scan.&gt;</dt>
<dt>Scan Type: &lt;Scan type&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-133">Antivirus</span><span class="sxs-lookup"><span data-stu-id="0096a-133">Antivirus</span></span></li>
<li><span data-ttu-id="0096a-134">Antispyware</span><span class="sxs-lookup"><span data-stu-id="0096a-134">Antispyware</span></span></li>
<li><span data-ttu-id="0096a-135">Logiciel anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="0096a-135">Antimalware</span></span></li>
</ul><span data-ttu-id="0096a-136">
</dt>
<dt>Paramètres d’analyse &lt; : paramètres d’analyse, &gt; par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-136">
</dt>
<dt>Scan Parameters: &lt;Scan parameters&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-137">Analyse complète</span><span class="sxs-lookup"><span data-stu-id="0096a-137">Full scan</span></span></li>
<li><span data-ttu-id="0096a-138">Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="0096a-138">Quick scan</span></span></li>
<li><span data-ttu-id="0096a-139">Analyse du client</span><span class="sxs-lookup"><span data-stu-id="0096a-139">Customer scan</span></span></li>
</ul><span data-ttu-id="0096a-140">
</dt>
<dt>Analyser les ressources : &lt; Ressources (telles que les fichiers/répertoires/BHO) qui ont été analysées. &gt; </dt> 
<dt>Utilisateur : &lt; Domain &gt; \& lt; Utilisateur &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-140">
</dt>
<dt>Scan Resources: &lt;Resources (such as files/directories/BHO) that were scanned.&gt;</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-141">ID d’événement : 1001</span><span class="sxs-lookup"><span data-stu-id="0096a-141">Event ID: 1001</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-142">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-142">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-143">
<b>MALWAREPROTECTION_SCAN_COMPLETED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-143">
<b>MALWAREPROTECTION_SCAN_COMPLETED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-144">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-144">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-145">
<b>Analyse anti-programme malveillant terminée.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-145">
<b>An antimalware scan finished.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-146">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-146">Description:</span></span>
</td>
<td >
<dl><span data-ttu-id="0096a-147">
<dt>ID d’analyse : &lt; Numéro d’ID de &gt; l’analyse pertinente.</dt> 
<dt> Type d’analyse &lt; : type &gt; d’analyse, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-147">
<dt>Scan ID: &lt;ID number of the relevant scan.&gt;</dt>
<dt>Scan Type: &lt;Scan type&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-148">Antivirus</span><span class="sxs-lookup"><span data-stu-id="0096a-148">Antivirus</span></span></li>
<li><span data-ttu-id="0096a-149">Antispyware</span><span class="sxs-lookup"><span data-stu-id="0096a-149">Antispyware</span></span></li>
<li><span data-ttu-id="0096a-150">Logiciel anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="0096a-150">Antimalware</span></span></li>
</ul><span data-ttu-id="0096a-151">
</dt>
<dt>Paramètres d’analyse &lt; : paramètres d’analyse, &gt; par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-151">
</dt>
<dt>Scan Parameters: &lt;Scan parameters&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-152">Analyse complète</span><span class="sxs-lookup"><span data-stu-id="0096a-152">Full scan</span></span></li>
<li><span data-ttu-id="0096a-153">Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="0096a-153">Quick scan</span></span></li>
<li><span data-ttu-id="0096a-154">Analyse du client</span><span class="sxs-lookup"><span data-stu-id="0096a-154">Customer scan</span></span></li>
</ul><span data-ttu-id="0096a-155">
</dt>
<dt>Utilisateur : &lt; Domain &gt; \& lt; Durée &gt; </dt>
<dt>d’analyse utilisateur &lt; : &gt; durée d’une analyse.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-155">
</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Scan Time: &lt;The duration of a scan.&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-156">ID d’événement : 1002</span><span class="sxs-lookup"><span data-stu-id="0096a-156">Event ID: 1002</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-157">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-157">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-158">
<b>MALWAREPROTECTION_SCAN_CANCELLED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-158">
<b>MALWAREPROTECTION_SCAN_CANCELLED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-159">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-159">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-160">
<b>Une analyse anti-programme malveillant a été arrêtée avant sa fin. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-160">
<b>An antimalware scan was stopped before it finished. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-161">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-161">Description:</span></span>
</td>
<td >
<dl><span data-ttu-id="0096a-162">
<dt>ID d’analyse : &lt; Numéro d’ID de &gt; l’analyse pertinente.</dt> 
<dt> Type d’analyse &lt; : type &gt; d’analyse, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-162">
<dt>Scan ID: &lt;ID number of the relevant scan.&gt;</dt>
<dt>Scan Type: &lt;Scan type&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-163">Antivirus</span><span class="sxs-lookup"><span data-stu-id="0096a-163">Antivirus</span></span></li>
<li><span data-ttu-id="0096a-164">Antispyware</span><span class="sxs-lookup"><span data-stu-id="0096a-164">Antispyware</span></span></li>
<li><span data-ttu-id="0096a-165">Logiciel anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="0096a-165">Antimalware</span></span></li>
</ul><span data-ttu-id="0096a-166">
</dt>
<dt>Paramètres d’analyse &lt; : paramètres d’analyse, &gt; par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-166">
</dt>
<dt>Scan Parameters: &lt;Scan parameters&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-167">Analyse complète</span><span class="sxs-lookup"><span data-stu-id="0096a-167">Full scan</span></span></li>
<li><span data-ttu-id="0096a-168">Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="0096a-168">Quick scan</span></span></li>
<li><span data-ttu-id="0096a-169">Analyse du client</span><span class="sxs-lookup"><span data-stu-id="0096a-169">Customer scan</span></span></li>
</ul><span data-ttu-id="0096a-170">
</dt>
<dt>Utilisateur : &lt; Domain &gt; &amp; lt; Durée &gt; </dt>
<dt>d’analyse utilisateur &lt; : &gt; durée d’une analyse.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-170">
</dt>
<dt>User: &lt;Domain&gt;&amp;lt;User&gt;</dt>
<dt>Scan Time: &lt;The duration of a scan.&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-171">ID d’événement : 1003</span><span class="sxs-lookup"><span data-stu-id="0096a-171">Event ID: 1003</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-172">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-172">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-173">
<b>MALWAREPROTECTION_SCAN_PAUSED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-173">
<b>MALWAREPROTECTION_SCAN_PAUSED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-174">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-174">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-175">
<b>Une analyse anti-programme malveillant a été suspendue. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-175">
<b>An antimalware scan was paused. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-176">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-176">Description:</span></span>
</td>
<td >
<dl><span data-ttu-id="0096a-177">
<dt>ID d’analyse : &lt; Numéro d’ID de &gt; l’analyse pertinente.</dt> 
<dt> Type d’analyse &lt; : type &gt; d’analyse, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-177">
<dt>Scan ID: &lt;ID number of the relevant scan.&gt;</dt>
<dt>Scan Type: &lt;Scan type&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-178">Antivirus</span><span class="sxs-lookup"><span data-stu-id="0096a-178">Antivirus</span></span></li>
<li><span data-ttu-id="0096a-179">Antispyware</span><span class="sxs-lookup"><span data-stu-id="0096a-179">Antispyware</span></span></li>
<li><span data-ttu-id="0096a-180">Logiciel anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="0096a-180">Antimalware</span></span></li>
</ul><span data-ttu-id="0096a-181">
</dt>
<dt>Paramètres d’analyse &lt; : paramètres d’analyse, &gt; par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-181">
</dt>
<dt>Scan Parameters: &lt;Scan parameters&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-182">Analyse complète</span><span class="sxs-lookup"><span data-stu-id="0096a-182">Full scan</span></span></li>
<li><span data-ttu-id="0096a-183">Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="0096a-183">Quick scan</span></span></li>
<li><span data-ttu-id="0096a-184">Analyse du client</span><span class="sxs-lookup"><span data-stu-id="0096a-184">Customer scan</span></span></li>
</ul><span data-ttu-id="0096a-185">
</dt>
<dt>Utilisateur : &lt; Domaine &gt; \& lt; Utilisateur&gt;</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-185">
</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-186">ID d’événement : 1004</span><span class="sxs-lookup"><span data-stu-id="0096a-186">Event ID: 1004</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-187">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-187">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-188">
<b>MALWAREPROTECTION_SCAN_RESUMED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-188">
<b>MALWAREPROTECTION_SCAN_RESUMED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-189">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-189">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-190">
<b>Une analyse anti-programme malveillant a été reprise. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-190">
<b>An antimalware scan was resumed. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-191">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-191">Description:</span></span>
</td>
<td >
<dl><span data-ttu-id="0096a-192">
<dt>ID d’analyse : &lt; Numéro d’ID de &gt; l’analyse pertinente.</dt> 
<dt> Type d’analyse &lt; : type &gt; d’analyse, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-192">
<dt>Scan ID: &lt;ID number of the relevant scan.&gt;</dt>
<dt>Scan Type: &lt;Scan type&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-193">Antivirus</span><span class="sxs-lookup"><span data-stu-id="0096a-193">Antivirus</span></span></li>
<li><span data-ttu-id="0096a-194">Antispyware</span><span class="sxs-lookup"><span data-stu-id="0096a-194">Antispyware</span></span></li>
<li><span data-ttu-id="0096a-195">Logiciel anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="0096a-195">Antimalware</span></span></li>
</ul><span data-ttu-id="0096a-196">
</dt>
<dt>Paramètres d’analyse &lt; : paramètres d’analyse, &gt; par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-196">
</dt>
<dt>Scan Parameters: &lt;Scan parameters&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-197">Analyse complète</span><span class="sxs-lookup"><span data-stu-id="0096a-197">Full scan</span></span></li>
<li><span data-ttu-id="0096a-198">Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="0096a-198">Quick scan</span></span></li>
<li><span data-ttu-id="0096a-199">Analyse du client</span><span class="sxs-lookup"><span data-stu-id="0096a-199">Customer scan</span></span></li>
</ul><span data-ttu-id="0096a-200">
</dt>
<dt>Utilisateur : &lt; Domaine &gt; \& lt; Utilisateur&gt;</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-200">
</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-201">ID d’événement : 1005</span><span class="sxs-lookup"><span data-stu-id="0096a-201">Event ID: 1005</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-202">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-202">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-203">
<b>MALWAREPROTECTION_SCAN_FAILED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-203">
<b>MALWAREPROTECTION_SCAN_FAILED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-204">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-204">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-205">
<b>Échec de l’analyse du logiciel anti-programme malveillant. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-205">
<b>An antimalware scan failed. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-206">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-206">Description:</span></span>
</td>
<td >
<dl><span data-ttu-id="0096a-207">
<dt>ID d’analyse : &lt; Numéro d’ID de &gt; l’analyse pertinente.</dt> 
<dt> Type d’analyse &lt; : type &gt; d’analyse, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-207">
<dt>Scan ID: &lt;ID number of the relevant scan.&gt;</dt>
<dt>Scan Type: &lt;Scan type&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-208">Antivirus</span><span class="sxs-lookup"><span data-stu-id="0096a-208">Antivirus</span></span></li>
<li><span data-ttu-id="0096a-209">Antispyware</span><span class="sxs-lookup"><span data-stu-id="0096a-209">Antispyware</span></span></li>
<li><span data-ttu-id="0096a-210">Logiciel anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="0096a-210">Antimalware</span></span></li>
</ul><span data-ttu-id="0096a-211">
</dt>
<dt>Paramètres d’analyse &lt; : paramètres d’analyse, &gt; par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-211">
</dt>
<dt>Scan Parameters: &lt;Scan parameters&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-212">Analyse complète</span><span class="sxs-lookup"><span data-stu-id="0096a-212">Full scan</span></span></li>
<li><span data-ttu-id="0096a-213">Analyse rapide</span><span class="sxs-lookup"><span data-stu-id="0096a-213">Quick scan</span></span></li>
<li><span data-ttu-id="0096a-214">Analyse du client</span><span class="sxs-lookup"><span data-stu-id="0096a-214">Customer scan</span></span></li>
</ul><span data-ttu-id="0096a-215">
</dt>
<dt>Utilisateur : &lt; Domain &gt; \& lt; Code &gt; </dt>
<dt>d’erreur utilisateur &lt; : code de résultat du code &gt; d’erreur associé à l’état de la menace. Valeurs HRESULT standard.</dt> 
<dt>Description de l’erreur : &lt; Description de &gt; l’erreur.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-215">
</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values.</dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-216">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-216">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-217">Le client antivirus a rencontré une erreur et l’analyse en cours s’est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="0096a-217">The antivirus client encountered an error, and the current scan has stopped.</span></span> <span data-ttu-id="0096a-218">L’analyse peut échouer en raison d’un problème côté client.</span><span class="sxs-lookup"><span data-stu-id="0096a-218">The scan might fail due to a client-side issue.</span></span> <span data-ttu-id="0096a-219">Cet enregistrement d’événement inclut l’ID d’analyse, le type d’analyse (Antivirus Microsoft Defender, antispyware, anti-programme malveillant), les paramètres d’analyse, l’utilisateur qui a démarré l’analyse, le code d’erreur et une description de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="0096a-219">This event record includes the scan ID, type of scan (Microsoft Defender Antivirus, antispyware, antimalware), scan parameters, the user that started the scan, the error code, and a description of the error.</span></span>
<span data-ttu-id="0096a-220">Pour résoudre les problèmes de cet événement :</span><span class="sxs-lookup"><span data-stu-id="0096a-220">To troubleshoot this event:</span></span>
<ol>
<li><span data-ttu-id="0096a-221">Exécutez à nouveau l’analyse.</span><span class="sxs-lookup"><span data-stu-id="0096a-221">Run the scan again.</span></span></li>
<li><span data-ttu-id="0096a-222">Si elle échoue de la même manière, allez sur le <b></b> site de support <a href="https://go.microsoft.com/fwlink/?LinkId=215163">Microsoft</a>, entrez le numéro d’erreur dans la zone de recherche pour rechercher le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0096a-222">If it fails in the same way, go to the <a href="https://go.microsoft.com/fwlink/?LinkId=215163">Microsoft Support site</a>, enter the error number in the <b>Search</b> box to look for the error code.</span></span></li>
<li><span data-ttu-id="0096a-223">Contactez le <a href="https://go.microsoft.com/fwlink/?LinkId=215491">Support technique Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="0096a-223">Contact <a href="https://go.microsoft.com/fwlink/?LinkId=215491">Microsoft Technical Support</a>.</span></span>
</li>
</ol>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-224">ID d’événement : 1006</span><span class="sxs-lookup"><span data-stu-id="0096a-224">Event ID: 1006</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-225">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-225">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-226">
<b>MALWAREPROTECTION_MALWARE_DETECTED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-226">
<b>MALWAREPROTECTION_MALWARE_DETECTED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-227">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-227">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-228">
<b>Le moteur du logiciel anti-programme malveillant a détecté des programmes malveillants ou d’autres logiciels potentiellement indésirables. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-228">
<b>The antimalware engine found malware or other potentially unwanted software. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-229">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-229">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-230">Pour plus d'informations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="0096a-230">For more information, see the following:</span></span>
<dl><span data-ttu-id="0096a-231">
<dt>Nom : &lt; ID &gt; du nom</dt>
<dt>de la menace : Gravité de &lt; l’ID &gt; </dt>de menace : 
<dt> &lt; &gt; Gravité, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-231">
<dt>Name: &lt;Threat name&gt;</dt>
<dt>ID: &lt;Threat ID&gt;</dt>
<dt>Severity: &lt;Severity&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-232">Faible</span><span class="sxs-lookup"><span data-stu-id="0096a-232">Low</span></span></li>
<li><span data-ttu-id="0096a-233">Modéré</span><span class="sxs-lookup"><span data-stu-id="0096a-233">Moderate</span></span></li>
<li><span data-ttu-id="0096a-234">Élevé</span><span class="sxs-lookup"><span data-stu-id="0096a-234">High</span></span></li>
<li><span data-ttu-id="0096a-235">Grave</span><span class="sxs-lookup"><span data-stu-id="0096a-235">Severe</span></span></li>
</ul><span data-ttu-id="0096a-236">
</dt>
<dt>Catégorie : &lt; Description de &gt; catégorie, par exemple, tout type de menace ou de programme malveillant.</dt> 
<dt>Chemin d’accès : &lt; Origine &gt; de la détection</dt> 
<dt> du chemin d’accès &lt; au fichier : origine de la &gt; détection, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-236">
</dt>
<dt>Category: &lt;Category description&gt;, for example, any threat or malware type.</dt>
<dt>Path: &lt;File path&gt;</dt>
<dt>Detection Origin: &lt;Detection origin&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-237">Inconnu</span><span class="sxs-lookup"><span data-stu-id="0096a-237">Unknown</span></span></li>
<li><span data-ttu-id="0096a-238">Ordinateur local</span><span class="sxs-lookup"><span data-stu-id="0096a-238">Local computer</span></span></li>
<li><span data-ttu-id="0096a-239">Partage réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-239">Network share</span></span></li>
<li><span data-ttu-id="0096a-240">Internet</span><span class="sxs-lookup"><span data-stu-id="0096a-240">Internet</span></span></li>
<li><span data-ttu-id="0096a-241">Trafic entrant</span><span class="sxs-lookup"><span data-stu-id="0096a-241">Incoming traffic</span></span></li>
<li><span data-ttu-id="0096a-242">Trafic sortant</span><span class="sxs-lookup"><span data-stu-id="0096a-242">Outgoing traffic</span></span></li>
</ul><span data-ttu-id="0096a-243">
</dt>
<dt>Type de détection &lt; : type de &gt; détection, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-243">
</dt>
<dt>Detection Type: &lt;Detection type&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-244">Heuristics</span><span class="sxs-lookup"><span data-stu-id="0096a-244">Heuristics</span></span></li>
<li><span data-ttu-id="0096a-245">Generic</span><span class="sxs-lookup"><span data-stu-id="0096a-245">Generic</span></span></li>
<li><span data-ttu-id="0096a-246">Concret</span><span class="sxs-lookup"><span data-stu-id="0096a-246">Concrete</span></span></li>
<li><span data-ttu-id="0096a-247">Signature dynamique</span><span class="sxs-lookup"><span data-stu-id="0096a-247">Dynamic signature</span></span></li>
</ul><span data-ttu-id="0096a-248">
</dt>
<dt>Source de détection : &lt; source de détection par exemple &gt; :</span><span class="sxs-lookup"><span data-stu-id="0096a-248">
</dt>
<dt>Detection Source: &lt;Detection source&gt; for example:</span></span><ul>
<li><span data-ttu-id="0096a-249">Utilisateur : initié par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="0096a-249">User: user initiated</span></span></li>
<li><span data-ttu-id="0096a-250">Système : initié par le système</span><span class="sxs-lookup"><span data-stu-id="0096a-250">System: system initiated</span></span></li>
<li><span data-ttu-id="0096a-251">En temps réel : composant en temps réel initié</span><span class="sxs-lookup"><span data-stu-id="0096a-251">Real-time: real-time component initiated</span></span></li>
<li><span data-ttu-id="0096a-252">IOAV : téléchargements d’IE et Outlook pièces jointes Express lancées</span><span class="sxs-lookup"><span data-stu-id="0096a-252">IOAV: IE Downloads and Outlook Express Attachments initiated</span></span></li>
<li><span data-ttu-id="0096a-253">NIS : système d’inspection du réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-253">NIS: Network inspection system</span></span></li>
<li><span data-ttu-id="0096a-254">IEPROTECT : IE - IExtensionValidation ; cela protège contre les contrôles de page web malveillants</span><span class="sxs-lookup"><span data-stu-id="0096a-254">IEPROTECT: IE - IExtensionValidation; this protects against malicious webpage controls</span></span></li>
<li><span data-ttu-id="0096a-255">Logiciel anti-programme malveillant à lancement précoce (ELAM).</span><span class="sxs-lookup"><span data-stu-id="0096a-255">Early Launch Antimalware (ELAM).</span></span> <span data-ttu-id="0096a-256">Cela inclut les programmes malveillants détectés par la séquence de démarrage</span><span class="sxs-lookup"><span data-stu-id="0096a-256">This includes malware detected by the boot sequence</span></span></li>
<li><span data-ttu-id="0096a-257">Attestation à distance</span><span class="sxs-lookup"><span data-stu-id="0096a-257">Remote attestation</span></span></li>
</ul><span data-ttu-id="0096a-258">Interface d’analyse anti-programme malveillant (AMSI).</span><span class="sxs-lookup"><span data-stu-id="0096a-258">Antimalware Scan Interface (AMSI).</span></span> <span data-ttu-id="0096a-259">Principalement utilisé pour protéger les scripts (PS, VBS), bien qu’il puisse également être appelé par des tiers.</span><span class="sxs-lookup"><span data-stu-id="0096a-259">Primarily used to protect scripts (PS, VBS), though it can be invoked by third parties as well.</span></span>
<span data-ttu-id="0096a-260">État du contrôle </dt> 
<dt>d’accès au client : &lt; utilisateur &gt; </dt>
<dt>d’état &lt; : domaine &gt; \& lt; User &gt; </dt>
<dt>Process Name: &lt; Process &gt; in the PID</dt>
<dt>Signature Version: &lt; Definition version &gt; </dt>Engine
<dt>Version: Antimalware Engine &lt; version &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-260">UAC</dt>
<dt>Status: &lt;Status&gt;</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Process Name: &lt;Process in the PID&gt;</dt>
<dt>Signature Version: &lt;Definition version&gt;</dt>
<dt>Engine Version: &lt;Antimalware Engine version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-261">ID d'événement : 1007</span><span class="sxs-lookup"><span data-stu-id="0096a-261">Event ID: 1007</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-262">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-262">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-263">
<b>MALWAREPROTECTION_MALWARE_ACTION_TAKEN </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-263">
<b>MALWAREPROTECTION_MALWARE_ACTION_TAKEN </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-264">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-264">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-265">
<b>La plateforme anti-programme malveillant a effectué une action pour protéger votre système contre les programmes malveillants ou d’autres logiciels potentiellement indésirables. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-265">
<b>The antimalware platform performed an action to protect your system from malware or other potentially unwanted software. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-266">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-266">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-267">Antivirus Microsoft Defender a pris des mesures pour protéger cet ordinateur contre les programmes malveillants ou d’autres logiciels potentiellement indésirables.</span><span class="sxs-lookup"><span data-stu-id="0096a-267">Microsoft Defender Antivirus has taken action to protect this machine from malware or other potentially unwanted software.</span></span> <span data-ttu-id="0096a-268">Pour plus d'informations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="0096a-268">For more information, see the following:</span></span>
<dl><span data-ttu-id="0096a-269">
<dt>Utilisateur : &lt; Domain &gt; \& lt; Nom &gt; </dt>
<dt>d’utilisateur &lt; : &gt; </dt>ID du
<dt>nom de la menace : Gravité de &lt; l’ID &gt; </dt>de menace : Gravité , par exemple 
<dt> &lt; &gt; :</span><span class="sxs-lookup"><span data-stu-id="0096a-269">
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Name: &lt;Threat name&gt;</dt>
<dt>ID: &lt;Threat ID&gt;</dt>
<dt>Severity: &lt;Severity&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-270">Faible</span><span class="sxs-lookup"><span data-stu-id="0096a-270">Low</span></span></li>
<li><span data-ttu-id="0096a-271">Modéré</span><span class="sxs-lookup"><span data-stu-id="0096a-271">Moderate</span></span></li>
<li><span data-ttu-id="0096a-272">Élevé</span><span class="sxs-lookup"><span data-stu-id="0096a-272">High</span></span></li>
<li><span data-ttu-id="0096a-273">Grave</span><span class="sxs-lookup"><span data-stu-id="0096a-273">Severe</span></span></li>
</ul><span data-ttu-id="0096a-274">
</dt>
<dt>Catégorie : &lt; Description de &gt; catégorie, par exemple, tout type de menace ou de programme malveillant.</dt> 
<dt> Action : &lt; &gt; Action, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-274">
</dt>
<dt>Category: &lt;Category description&gt;, for example, any threat or malware type.</dt>
<dt>Action: &lt;Action&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-275">Nettoyer : la ressource a été nettoyée</span><span class="sxs-lookup"><span data-stu-id="0096a-275">Clean: The resource was cleaned</span></span></li>
<li><span data-ttu-id="0096a-276">Quarantaine : la ressource a été mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="0096a-276">Quarantine: The resource was quarantined</span></span></li>
<li><span data-ttu-id="0096a-277">Supprimer : la ressource a été supprimée</span><span class="sxs-lookup"><span data-stu-id="0096a-277">Remove: The resource was deleted</span></span></li>
<li><span data-ttu-id="0096a-278">Autoriser : la ressource a été autorisée à s’exécuter/exister</span><span class="sxs-lookup"><span data-stu-id="0096a-278">Allow: The resource was allowed to execute/exist</span></span></li>
<li><span data-ttu-id="0096a-279">Défini par l’utilisateur : action définie par l’utilisateur qui est normalement une de cette liste d’actions que l’utilisateur a spécifiée</span><span class="sxs-lookup"><span data-stu-id="0096a-279">User defined: User-defined action that is normally one from this list of actions that the user has specified</span></span></li>
<li><span data-ttu-id="0096a-280">Aucune action : aucune action</span><span class="sxs-lookup"><span data-stu-id="0096a-280">No action: No action</span></span></li>
<li><span data-ttu-id="0096a-281">Bloc : l’exécution de la ressource a été bloquée</span><span class="sxs-lookup"><span data-stu-id="0096a-281">Block: The resource was blocked from executing</span></span></li>
</ul><span data-ttu-id="0096a-282">
</dt>
<dt>État : &lt; Version &gt; de</dt>
<dt>la signature d’état &lt; : &gt; version</dt>de définition du moteur : Antimalware Engine
<dt> &lt; version &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-282">
</dt>
<dt>Status: &lt;Status&gt;</dt>
<dt>Signature Version: &lt;Definition version&gt;</dt>
<dt>Engine Version: &lt;Antimalware Engine version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-283">ID d'événement : 1008</span><span class="sxs-lookup"><span data-stu-id="0096a-283">Event ID: 1008</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-284">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-284">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-285">
<b>MALWAREPROTECTION_MALWARE_ACTION_FAILED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-285">
<b>MALWAREPROTECTION_MALWARE_ACTION_FAILED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-286">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-286">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-287">
<b>La plateforme anti-programme malveillant a tenté d’effectuer une action pour protéger votre système contre les programmes malveillants ou d’autres logiciels potentiellement indésirables, mais l’action a échoué.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-287">
<b>The antimalware platform attempted to perform an action to protect your system from malware or other potentially unwanted software, but the action failed.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-288">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-288">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-289">Antivirus Microsoft Defender a rencontré une erreur lors de l’action sur des programmes malveillants ou d’autres logiciels potentiellement indésirables.</span><span class="sxs-lookup"><span data-stu-id="0096a-289">Microsoft Defender Antivirus has encountered an error when taking action on malware or other potentially unwanted software.</span></span> <span data-ttu-id="0096a-290">Pour plus d'informations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="0096a-290">For more information, see the following:</span></span>
<dl><span data-ttu-id="0096a-291">
<dt>Utilisateur : &lt; Domain &gt; \& lt; Nom &gt; </dt>
<dt>d’utilisateur &lt; : &gt; </dt>ID du
<dt>nom de la menace : Gravité de &lt; l’ID &gt; </dt>de menace : Gravité , par exemple 
<dt> &lt; &gt; :</span><span class="sxs-lookup"><span data-stu-id="0096a-291">
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Name: &lt;Threat name&gt;</dt>
<dt>ID: &lt;Threat ID&gt;</dt>
<dt>Severity: &lt;Severity&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-292">Faible</span><span class="sxs-lookup"><span data-stu-id="0096a-292">Low</span></span></li>
<li><span data-ttu-id="0096a-293">Modéré</span><span class="sxs-lookup"><span data-stu-id="0096a-293">Moderate</span></span></li>
<li><span data-ttu-id="0096a-294">Élevé</span><span class="sxs-lookup"><span data-stu-id="0096a-294">High</span></span></li>
<li><span data-ttu-id="0096a-295">Grave</span><span class="sxs-lookup"><span data-stu-id="0096a-295">Severe</span></span></li>
</ul><span data-ttu-id="0096a-296">
</dt>
<dt>Catégorie : &lt; Description de &gt; catégorie, par exemple, tout type de menace ou de programme malveillant.</dt> 
<dt>Chemin d’accès : &lt; Action &gt; du chemin</dt> 
<dt> &lt; d’accès au fichier : &gt; Action, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-296">
</dt>
<dt>Category: &lt;Category description&gt;, for example, any threat or malware type.</dt>
<dt>Path: &lt;File path&gt;</dt>
<dt>Action: &lt;Action&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-297">Nettoyer : la ressource a été nettoyée</span><span class="sxs-lookup"><span data-stu-id="0096a-297">Clean: The resource was cleaned</span></span></li>
<li><span data-ttu-id="0096a-298">Quarantaine : la ressource a été mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="0096a-298">Quarantine: The resource was quarantined</span></span></li>
<li><span data-ttu-id="0096a-299">Supprimer : la ressource a été supprimée</span><span class="sxs-lookup"><span data-stu-id="0096a-299">Remove: The resource was deleted</span></span></li>
<li><span data-ttu-id="0096a-300">Autoriser : la ressource a été autorisée à s’exécuter/exister</span><span class="sxs-lookup"><span data-stu-id="0096a-300">Allow: The resource was allowed to execute/exist</span></span></li>
<li><span data-ttu-id="0096a-301">Défini par l’utilisateur : action définie par l’utilisateur qui est normalement une de cette liste d’actions que l’utilisateur a spécifiée</span><span class="sxs-lookup"><span data-stu-id="0096a-301">User defined: User-defined action that is normally one from this list of actions that the user has specified</span></span></li>
<li><span data-ttu-id="0096a-302">Aucune action : aucune action</span><span class="sxs-lookup"><span data-stu-id="0096a-302">No action: No action</span></span></li>
<li><span data-ttu-id="0096a-303">Bloc : l’exécution de la ressource a été bloquée</span><span class="sxs-lookup"><span data-stu-id="0096a-303">Block: The resource was blocked from executing</span></span></li>
</ul><span data-ttu-id="0096a-304">
</dt>
<dt>Code d’erreur : &lt; Code de résultat du &gt; code d’erreur associé à l’état de la menace. Valeurs HRESULT standard. </dt> 
<dt>Description de &lt; l’erreur : description &gt; de l’erreur.</dt> 
<dt>État : &lt; Version &gt; de</dt>
<dt>la signature d’état &lt; : &gt; version</dt>de définition du moteur : Antimalware Engine
<dt> &lt; version &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-304">
</dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values. </dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
<dt>Status: &lt;Status&gt;</dt>
<dt>Signature Version: &lt;Definition version&gt;</dt>
<dt>Engine Version: &lt;Antimalware Engine version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-305">ID d'événement : 1009</span><span class="sxs-lookup"><span data-stu-id="0096a-305">Event ID: 1009</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-306">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-306">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-307">
<b>MALWAREPROTECTION_QUARANTINE_RESTORE </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-307">
<b>MALWAREPROTECTION_QUARANTINE_RESTORE </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-308">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-308">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-309">
<b>La plateforme anti-programme malveillant a restauré un élément de la quarantaine. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-309">
<b>The antimalware platform restored an item from quarantine. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-310">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-310">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-311">Antivirus Microsoft Defender a restauré un élément de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="0096a-311">Microsoft Defender Antivirus has restored an item from quarantine.</span></span> <span data-ttu-id="0096a-312">Pour plus d'informations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="0096a-312">For more information, see the following:</span></span>
<dl><span data-ttu-id="0096a-313">
<dt>Nom : &lt; ID &gt; du nom</dt>
<dt>de la menace : Gravité de &lt; l’ID &gt; </dt>de menace : 
<dt> &lt; &gt; Gravité, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-313">
<dt>Name: &lt;Threat name&gt;</dt>
<dt>ID: &lt;Threat ID&gt;</dt>
<dt>Severity: &lt;Severity&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-314">Faible</span><span class="sxs-lookup"><span data-stu-id="0096a-314">Low</span></span></li>
<li><span data-ttu-id="0096a-315">Modéré</span><span class="sxs-lookup"><span data-stu-id="0096a-315">Moderate</span></span></li>
<li><span data-ttu-id="0096a-316">Élevé</span><span class="sxs-lookup"><span data-stu-id="0096a-316">High</span></span></li>
<li><span data-ttu-id="0096a-317">Grave</span><span class="sxs-lookup"><span data-stu-id="0096a-317">Severe</span></span></li>
</ul><span data-ttu-id="0096a-318">
</dt>
<dt>Catégorie : &lt; Description de &gt; catégorie, par exemple, tout type de menace ou de programme malveillant.</dt> 
<dt>Chemin d’accès : &lt; File &gt; path</dt>
<dt>User: &lt; Domain &gt; \& lt; Version &gt; de</dt>
<dt>la signature utilisateur : version de &lt; définition &gt; </dt>du moteur : Antimalware Engine
<dt> &lt; version &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-318">
</dt>
<dt>Category: &lt;Category description&gt;, for example, any threat or malware type.</dt>
<dt>Path: &lt;File path&gt;</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Signature Version: &lt;Definition version&gt;</dt>
<dt>Engine Version: &lt;Antimalware Engine version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-319">ID d'événement : 1010</span><span class="sxs-lookup"><span data-stu-id="0096a-319">Event ID: 1010</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-320">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-320">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-321">
<b>MALWAREPROTECTION_QUARANTINE_RESTORE_FAILED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-321">
<b>MALWAREPROTECTION_QUARANTINE_RESTORE_FAILED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-322">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-322">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-323">
<b>La plateforme anti-programme malveillant n’a pas pu restaurer un élément de la quarantaine. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-323">
<b>The antimalware platform could not restore an item from quarantine. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-324">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-324">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-325">Antivirus Microsoft Defender a rencontré une erreur lors de la tentative de restauration d’un élément de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="0096a-325">Microsoft Defender Antivirus has encountered an error trying to restore an item from quarantine.</span></span> <span data-ttu-id="0096a-326">Pour plus d'informations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="0096a-326">For more information, see the following:</span></span>
<dl><span data-ttu-id="0096a-327">
<dt>Nom : &lt; ID &gt; du nom</dt>
<dt>de la menace : Gravité de &lt; l’ID &gt; </dt>de menace : 
<dt> &lt; &gt; Gravité, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-327">
<dt>Name: &lt;Threat name&gt;</dt>
<dt>ID: &lt;Threat ID&gt;</dt>
<dt>Severity: &lt;Severity&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-328">Faible</span><span class="sxs-lookup"><span data-stu-id="0096a-328">Low</span></span></li>
<li><span data-ttu-id="0096a-329">Modéré</span><span class="sxs-lookup"><span data-stu-id="0096a-329">Moderate</span></span></li>
<li><span data-ttu-id="0096a-330">Élevé</span><span class="sxs-lookup"><span data-stu-id="0096a-330">High</span></span></li>
<li><span data-ttu-id="0096a-331">Grave</span><span class="sxs-lookup"><span data-stu-id="0096a-331">Severe</span></span></li>
</ul><span data-ttu-id="0096a-332">
</dt>
<dt>Catégorie : &lt; Description de &gt; catégorie, par exemple, tout type de menace ou de programme malveillant.</dt> 
<dt>Chemin d’accès : &lt; File &gt; path</dt>
<dt>User: &lt; Domain &gt; \& lt; Code &gt; </dt>
<dt>d’erreur utilisateur &lt; : code de résultat du code &gt; d’erreur associé à l’état de la menace. Valeurs HRESULT standard. </dt> 
<dt>Description de &lt; l’erreur : description &gt; de l’erreur.</dt> 
<dt>Version de la signature : &lt; Version &gt; du moteur</dt>
<dt>de définition : Antimalware Engine &lt; version &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-332">
</dt>
<dt>Category: &lt;Category description&gt;, for example, any threat or malware type.</dt>
<dt>Path: &lt;File path&gt;</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values. </dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
<dt>Signature Version: &lt;Definition version&gt;</dt>
<dt>Engine Version: &lt;Antimalware Engine version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-333">ID d’événement : 1011</span><span class="sxs-lookup"><span data-stu-id="0096a-333">Event ID: 1011</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-334">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-334">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-335">
<b>MALWAREPROTECTION_QUARANTINE_DELETE</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-335">
<b>MALWAREPROTECTION_QUARANTINE_DELETE</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-336">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-336">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-337">
<b>La plateforme anti-programme malveillant a supprimé un élément de la quarantaine. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-337">
<b>The antimalware platform deleted an item from quarantine. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-338">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-338">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-339">Antivirus Microsoft Defender a supprimé un élément de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="0096a-339">Microsoft Defender Antivirus has deleted an item from quarantine.</span></span><br/><span data-ttu-id="0096a-340">Pour plus d'informations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="0096a-340">For more information, see the following:</span></span>
<dl><span data-ttu-id="0096a-341">
<dt>Nom : &lt; ID &gt; du nom</dt>
<dt>de la menace : Gravité de &lt; l’ID &gt; </dt>de menace : 
<dt> &lt; &gt; Gravité, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-341">
<dt>Name: &lt;Threat name&gt;</dt>
<dt>ID: &lt;Threat ID&gt;</dt>
<dt>Severity: &lt;Severity&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-342">Faible</span><span class="sxs-lookup"><span data-stu-id="0096a-342">Low</span></span></li>
<li><span data-ttu-id="0096a-343">Modéré</span><span class="sxs-lookup"><span data-stu-id="0096a-343">Moderate</span></span></li>
<li><span data-ttu-id="0096a-344">Élevé</span><span class="sxs-lookup"><span data-stu-id="0096a-344">High</span></span></li>
<li><span data-ttu-id="0096a-345">Grave</span><span class="sxs-lookup"><span data-stu-id="0096a-345">Severe</span></span></li>
</ul><span data-ttu-id="0096a-346">
</dt>
<dt>Catégorie : &lt; Description de &gt; catégorie, par exemple, tout type de menace ou de programme malveillant.</dt> 
<dt>Chemin d’accès : &lt; File &gt; path</dt>
<dt>User: &lt; Domain &gt; \& lt; Version &gt; de</dt>
<dt>la signature utilisateur : version de &lt; définition &gt; </dt>du moteur : Antimalware Engine
<dt> &lt; version &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-346">
</dt>
<dt>Category: &lt;Category description&gt;, for example, any threat or malware type.</dt>
<dt>Path: &lt;File path&gt;</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Signature Version: &lt;Definition version&gt;</dt>
<dt>Engine Version: &lt;Antimalware Engine version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-347">ID d'événement : 1012</span><span class="sxs-lookup"><span data-stu-id="0096a-347">Event ID: 1012</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-348">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-348">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-349">
<b>MALWAREPROTECTION_QUARANTINE_DELETE_FAILED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-349">
<b>MALWAREPROTECTION_QUARANTINE_DELETE_FAILED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-350">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-350">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-351">
<b>La plateforme anti-programme malveillant n’a pas pu supprimer un élément de la quarantaine.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-351">
<b>The antimalware platform could not delete an item from quarantine.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-352">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-352">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-353">Antivirus Microsoft Defender a rencontré une erreur lors de la tentative de suppression d’un élément de la quarantaine.</span><span class="sxs-lookup"><span data-stu-id="0096a-353">Microsoft Defender Antivirus has encountered an error trying to delete an item from quarantine.</span></span>
<span data-ttu-id="0096a-354">Pour plus d'informations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="0096a-354">For more information, see the following:</span></span>
<dl><span data-ttu-id="0096a-355">
<dt>Nom : &lt; ID &gt; du nom</dt>
<dt>de la menace : Gravité de &lt; l’ID &gt; </dt>de menace : 
<dt> &lt; &gt; Gravité, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-355">
<dt>Name: &lt;Threat name&gt;</dt>
<dt>ID: &lt;Threat ID&gt;</dt>
<dt>Severity: &lt;Severity&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-356">Faible</span><span class="sxs-lookup"><span data-stu-id="0096a-356">Low</span></span></li>
<li><span data-ttu-id="0096a-357">Modéré</span><span class="sxs-lookup"><span data-stu-id="0096a-357">Moderate</span></span></li>
<li><span data-ttu-id="0096a-358">Élevé</span><span class="sxs-lookup"><span data-stu-id="0096a-358">High</span></span></li>
<li><span data-ttu-id="0096a-359">Grave</span><span class="sxs-lookup"><span data-stu-id="0096a-359">Severe</span></span></li>
</ul><span data-ttu-id="0096a-360">
</dt>
<dt>Catégorie : &lt; Description de &gt; catégorie, par exemple, tout type de menace ou de programme malveillant.</dt> 
<dt>Chemin d’accès : &lt; File &gt; path</dt>
<dt>User: &lt; Domain &gt; \& lt; Code &gt; </dt>
<dt>d’erreur utilisateur &lt; : code de résultat du code &gt; d’erreur associé à l’état de la menace. Valeurs HRESULT standard. </dt> 
<dt>Description de &lt; l’erreur : description &gt; de l’erreur.</dt> 
<dt>Version de la signature : &lt; Version &gt; du moteur</dt>
<dt>de définition : Antimalware Engine &lt; version &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-360">
</dt>
<dt>Category: &lt;Category description&gt;, for example, any threat or malware type.</dt>
<dt>Path: &lt;File path&gt;</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values. </dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
<dt>Signature Version: &lt;Definition version&gt;</dt>
<dt>Engine Version: &lt;Antimalware Engine version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-361">ID d’événement : 1013</span><span class="sxs-lookup"><span data-stu-id="0096a-361">Event ID: 1013</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-362">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-362">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-363">
<b>MALWAREPROTECTION_MALWARE_HISTORY_DELETE </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-363">
<b>MALWAREPROTECTION_MALWARE_HISTORY_DELETE </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-364">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-364">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-365">
<b>L’historique de suppression de la plateforme anti-programme malveillant des programmes malveillants et d’autres logiciels potentiellement indésirables.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-365">
<b>The antimalware platform deleted history of malware and other potentially unwanted software.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-366">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-366">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-367">Antivirus Microsoft Defender a supprimé l’historique des programmes malveillants et autres logiciels potentiellement indésirables.</span><span class="sxs-lookup"><span data-stu-id="0096a-367">Microsoft Defender Antivirus has removed history of malware and other potentially unwanted software.</span></span>
<dl><span data-ttu-id="0096a-368">
<dt>Heure : heure à quel moment l’événement s’est produit, par exemple lorsque l’historique est purgé. Ce paramètre n’est pas utilisé dans les événements de menace afin qu’il n’y a aucune confusion quant à la durée de correction ou d’infection. Pour ceux-ci, nous les appelons spécifiquement Heure de l’action ou Heure de la détection.</dt> 
<dt>Utilisateur : &lt; Domain &gt; \& lt; Utilisateur &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-368">
<dt>Time: The time when the event occurred, for example when the history is purged. This parameter is not used in threat events so that there is no confusion regarding whether it is remediation time or infection time. For those, we specifically call them as Action Time or Detection Time.</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-369">ID d’événement : 1014</span><span class="sxs-lookup"><span data-stu-id="0096a-369">Event ID: 1014</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-370">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-370">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-371">
<b>MALWAREPROTECTION_MALWARE_HISTORY_DELETE_FAILED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-371">
<b>MALWAREPROTECTION_MALWARE_HISTORY_DELETE_FAILED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-372">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-372">Message:</span></span>
</td>
<td >
<span data-ttu-id="0096a-373">La plateforme anti-programme malveillant n’a pas pu supprimer l’historique des programmes malveillants et autres logiciels potentiellement indésirables.</span><span class="sxs-lookup"><span data-stu-id="0096a-373">The antimalware platform could not delete history of malware and other potentially unwanted software.</span></span>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-374">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-374">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-375">Antivirus Microsoft Defender a rencontré une erreur lors de la tentative de suppression de l’historique des programmes malveillants et d’autres logiciels potentiellement indésirables.</span><span class="sxs-lookup"><span data-stu-id="0096a-375">Microsoft Defender Antivirus has encountered an error trying to remove history of malware and other potentially unwanted software.</span></span>
<dl><span data-ttu-id="0096a-376">
<dt>Heure : heure à quel moment l’événement s’est produit, par exemple lorsque l’historique est purgé. Ce paramètre n’est pas utilisé dans les événements de menace afin qu’il n’y a aucune confusion quant à la durée de correction ou d’infection. Pour ceux-ci, nous les appelons spécifiquement Heure de l’action ou Heure de la détection.</dt> 
<dt>Utilisateur : &lt; Domain &gt; \& lt; Code &gt; </dt>
<dt>d’erreur utilisateur &lt; : code de résultat du code &gt; d’erreur associé à l’état de la menace. Valeurs HRESULT standard. </dt> 
<dt>Description de &lt; l’erreur : description &gt; de l’erreur.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-376">
<dt>Time: The time when the event occurred, for example when the history is purged. This parameter is not used in threat events so that there is no confusion regarding whether it is remediation time or infection time. For those, we specifically call them as Action Time or Detection Time.</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values. </dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-377">ID d’événement : 1015</span><span class="sxs-lookup"><span data-stu-id="0096a-377">Event ID: 1015</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-378">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-378">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-379">
<b>MALWAREPROTECTION_BEHAVIOR_DETECTED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-379">
<b>MALWAREPROTECTION_BEHAVIOR_DETECTED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-380">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-380">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-381">
<b>La plateforme anti-programme malveillant a détecté un comportement suspect.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-381">
<b>The antimalware platform detected suspicious behavior.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-382">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-382">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-383">Antivirus Microsoft Defender a détecté un comportement suspect.</span><span class="sxs-lookup"><span data-stu-id="0096a-383">Microsoft Defender Antivirus has detected a suspicious behavior.</span></span><br/><span data-ttu-id="0096a-384">Pour plus d'informations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="0096a-384">For more information, see the following:</span></span>
<dl><span data-ttu-id="0096a-385">
<dt>Nom : &lt; ID &gt; du nom</dt>
<dt>de la menace : Gravité de &lt; l’ID &gt; </dt>de menace : 
<dt> &lt; &gt; Gravité, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-385">
<dt>Name: &lt;Threat name&gt;</dt>
<dt>ID: &lt;Threat ID&gt;</dt>
<dt>Severity: &lt;Severity&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-386">Faible</span><span class="sxs-lookup"><span data-stu-id="0096a-386">Low</span></span></li>
<li><span data-ttu-id="0096a-387">Modéré</span><span class="sxs-lookup"><span data-stu-id="0096a-387">Moderate</span></span></li>
<li><span data-ttu-id="0096a-388">Élevé</span><span class="sxs-lookup"><span data-stu-id="0096a-388">High</span></span></li>
<li><span data-ttu-id="0096a-389">Grave</span><span class="sxs-lookup"><span data-stu-id="0096a-389">Severe</span></span></li>
</ul><span data-ttu-id="0096a-390">
</dt>
<dt>Catégorie : &lt; Description de &gt; catégorie, par exemple, tout type de menace ou de programme malveillant.</dt> 
<dt>Chemin d’accès : &lt; Origine &gt; de la détection</dt> 
<dt> du chemin d’accès &lt; au fichier : origine de la &gt; détection, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-390">
</dt>
<dt>Category: &lt;Category description&gt;, for example, any threat or malware type.</dt>
<dt>Path: &lt;File path&gt;</dt>
<dt>Detection Origin: &lt;Detection origin&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-391">Inconnu</span><span class="sxs-lookup"><span data-stu-id="0096a-391">Unknown</span></span></li>
<li><span data-ttu-id="0096a-392">Ordinateur local</span><span class="sxs-lookup"><span data-stu-id="0096a-392">Local computer</span></span></li>
<li><span data-ttu-id="0096a-393">Partage réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-393">Network share</span></span></li>
<li><span data-ttu-id="0096a-394">Internet</span><span class="sxs-lookup"><span data-stu-id="0096a-394">Internet</span></span></li>
<li><span data-ttu-id="0096a-395">Trafic entrant</span><span class="sxs-lookup"><span data-stu-id="0096a-395">Incoming traffic</span></span></li>
<li><span data-ttu-id="0096a-396">Trafic sortant</span><span class="sxs-lookup"><span data-stu-id="0096a-396">Outgoing traffic</span></span></li>
</ul><span data-ttu-id="0096a-397">
</dt>
<dt>Type de détection &lt; : type de &gt; détection, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-397">
</dt>
<dt>Detection Type: &lt;Detection type&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-398">Heuristics</span><span class="sxs-lookup"><span data-stu-id="0096a-398">Heuristics</span></span></li>
<li><span data-ttu-id="0096a-399">Generic</span><span class="sxs-lookup"><span data-stu-id="0096a-399">Generic</span></span></li>
<li><span data-ttu-id="0096a-400">Concret</span><span class="sxs-lookup"><span data-stu-id="0096a-400">Concrete</span></span></li>
<li><span data-ttu-id="0096a-401">Signature dynamique</span><span class="sxs-lookup"><span data-stu-id="0096a-401">Dynamic signature</span></span></li>
</ul><span data-ttu-id="0096a-402">
</dt>
<dt>Source de détection : &lt; source de détection par exemple &gt; :</span><span class="sxs-lookup"><span data-stu-id="0096a-402">
</dt>
<dt>Detection Source: &lt;Detection source&gt; for example:</span></span><ul>
<li><span data-ttu-id="0096a-403">Utilisateur : initié par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="0096a-403">User: user initiated</span></span></li>
<li><span data-ttu-id="0096a-404">Système : initié par le système</span><span class="sxs-lookup"><span data-stu-id="0096a-404">System: system initiated</span></span></li>
<li><span data-ttu-id="0096a-405">En temps réel : composant en temps réel initié</span><span class="sxs-lookup"><span data-stu-id="0096a-405">Real-time: real-time component initiated</span></span></li>
<li><span data-ttu-id="0096a-406">IOAV : téléchargements d’IE et Outlook pièces jointes Express lancées</span><span class="sxs-lookup"><span data-stu-id="0096a-406">IOAV: IE Downloads and Outlook Express Attachments initiated</span></span></li>
<li><span data-ttu-id="0096a-407">NIS : système d’inspection du réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-407">NIS: Network inspection system</span></span></li>
<li><span data-ttu-id="0096a-408">IEPROTECT : IE - IExtensionValidation ; cela protège contre les contrôles de page web malveillants</span><span class="sxs-lookup"><span data-stu-id="0096a-408">IEPROTECT: IE - IExtensionValidation; this protects against malicious webpage controls</span></span></li>
<li><span data-ttu-id="0096a-409">Logiciel anti-programme malveillant à lancement précoce (ELAM).</span><span class="sxs-lookup"><span data-stu-id="0096a-409">Early Launch Antimalware (ELAM).</span></span> <span data-ttu-id="0096a-410">Cela inclut les programmes malveillants détectés par la séquence de démarrage</span><span class="sxs-lookup"><span data-stu-id="0096a-410">This includes malware detected by the boot sequence</span></span></li>
<li><span data-ttu-id="0096a-411">Attestation à distance</span><span class="sxs-lookup"><span data-stu-id="0096a-411">Remote attestation</span></span></li>
</ul><span data-ttu-id="0096a-412">Interface d’analyse anti-programme malveillant (AMSI).</span><span class="sxs-lookup"><span data-stu-id="0096a-412">Antimalware Scan Interface (AMSI).</span></span> <span data-ttu-id="0096a-413">Principalement utilisé pour protéger les scripts (PS, VBS), bien qu’il puisse également être appelé par des tiers.</span><span class="sxs-lookup"><span data-stu-id="0096a-413">Primarily used to protect scripts (PS, VBS), though it can be invoked by third parties as well.</span></span>
<span data-ttu-id="0096a-414">État du contrôle </dt> 
<dt>d’accès au client : &lt; utilisateur &gt; </dt>
<dt>d’état &lt; : domaine &gt; \& lt; Nom &gt; </dt>
<dt>du processus utilisateur : processus dans &lt; l’ID &gt; </dt>de signature PID : gravité de correspondance
<dt>d’éumération.</dt> 
<dt>Version de la signature : &lt; Version &gt; de la définition</dt>
<dt>du moteur : Antimalware Engine la &lt; &gt; version</dt>
<dt>Fidelity Label :</dt>Nom de fichier cible : nom de fichier du
<dt> &lt; &gt; fichier.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-414">UAC</dt>
<dt>Status: &lt;Status&gt;</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Process Name: &lt;Process in the PID&gt;</dt>
<dt>Signature ID: Enumeration matching severity.</dt>
<dt>Signature Version: &lt;Definition version&gt;</dt>
<dt>Engine Version: &lt;Antimalware Engine version&gt;</dt>
<dt>Fidelity Label:</dt>
<dt>Target File Name: &lt;File name&gt; Name of the file.</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-415">ID d’événement : 1116</span><span class="sxs-lookup"><span data-stu-id="0096a-415">Event ID: 1116</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-416">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-416">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-417">
<b>MALWAREPROTECTION_STATE_MALWARE_DETECTED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-417">
<b>MALWAREPROTECTION_STATE_MALWARE_DETECTED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-418">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-418">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-419">
<b>La plateforme anti-programme malveillant a détecté des programmes malveillants ou d’autres logiciels potentiellement indésirables. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-419">
<b>The antimalware platform detected malware or other potentially unwanted software. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-420">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-420">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-421">Antivirus Microsoft Defender a détecté des programmes malveillants ou d’autres logiciels potentiellement indésirables.</span><span class="sxs-lookup"><span data-stu-id="0096a-421">Microsoft Defender Antivirus has detected malware or other potentially unwanted software.</span></span><br/><span data-ttu-id="0096a-422">Pour plus d'informations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="0096a-422">For more information, see the following:</span></span>
<dl><span data-ttu-id="0096a-423">
<dt>Nom : &lt; ID &gt; du nom</dt>
<dt>de la menace : Gravité de &lt; l’ID &gt; </dt>de menace : 
<dt> &lt; &gt; Gravité, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-423">
<dt>Name: &lt;Threat name&gt;</dt>
<dt>ID: &lt;Threat ID&gt;</dt>
<dt>Severity: &lt;Severity&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-424">Faible</span><span class="sxs-lookup"><span data-stu-id="0096a-424">Low</span></span></li>
<li><span data-ttu-id="0096a-425">Modéré</span><span class="sxs-lookup"><span data-stu-id="0096a-425">Moderate</span></span></li>
<li><span data-ttu-id="0096a-426">Élevé</span><span class="sxs-lookup"><span data-stu-id="0096a-426">High</span></span></li>
<li><span data-ttu-id="0096a-427">Grave</span><span class="sxs-lookup"><span data-stu-id="0096a-427">Severe</span></span></li>
</ul><span data-ttu-id="0096a-428">
</dt>
<dt>Catégorie : &lt; Description de &gt; catégorie, par exemple, tout type de menace ou de programme malveillant.</dt> 
<dt>Chemin d’accès : &lt; Origine &gt; de la détection</dt> 
<dt> du chemin d’accès &lt; au fichier : origine de la &gt; détection, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-428">
</dt>
<dt>Category: &lt;Category description&gt;, for example, any threat or malware type.</dt>
<dt>Path: &lt;File path&gt;</dt>
<dt>Detection Origin: &lt;Detection origin&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-429">Inconnu</span><span class="sxs-lookup"><span data-stu-id="0096a-429">Unknown</span></span></li>
<li><span data-ttu-id="0096a-430">Ordinateur local</span><span class="sxs-lookup"><span data-stu-id="0096a-430">Local computer</span></span></li>
<li><span data-ttu-id="0096a-431">Partage réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-431">Network share</span></span></li>
<li><span data-ttu-id="0096a-432">Internet</span><span class="sxs-lookup"><span data-stu-id="0096a-432">Internet</span></span></li>
<li><span data-ttu-id="0096a-433">Trafic entrant</span><span class="sxs-lookup"><span data-stu-id="0096a-433">Incoming traffic</span></span></li>
<li><span data-ttu-id="0096a-434">Trafic sortant</span><span class="sxs-lookup"><span data-stu-id="0096a-434">Outgoing traffic</span></span></li>
</ul><span data-ttu-id="0096a-435">
</dt>
<dt>Type de détection &lt; : type de &gt; détection, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-435">
</dt>
<dt>Detection Type: &lt;Detection type&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-436">Heuristics</span><span class="sxs-lookup"><span data-stu-id="0096a-436">Heuristics</span></span></li>
<li><span data-ttu-id="0096a-437">Generic</span><span class="sxs-lookup"><span data-stu-id="0096a-437">Generic</span></span></li>
<li><span data-ttu-id="0096a-438">Concret</span><span class="sxs-lookup"><span data-stu-id="0096a-438">Concrete</span></span></li>
<li><span data-ttu-id="0096a-439">Signature dynamique</span><span class="sxs-lookup"><span data-stu-id="0096a-439">Dynamic signature</span></span></li>
</ul><span data-ttu-id="0096a-440">
</dt>
<dt>Source de détection : &lt; source de détection par exemple &gt; :</span><span class="sxs-lookup"><span data-stu-id="0096a-440">
</dt>
<dt>Detection Source: &lt;Detection source&gt; for example:</span></span><ul>
<li><span data-ttu-id="0096a-441">Utilisateur : initié par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="0096a-441">User: user initiated</span></span></li>
<li><span data-ttu-id="0096a-442">Système : initié par le système</span><span class="sxs-lookup"><span data-stu-id="0096a-442">System: system initiated</span></span></li>
<li><span data-ttu-id="0096a-443">En temps réel : composant en temps réel initié</span><span class="sxs-lookup"><span data-stu-id="0096a-443">Real-time: real-time component initiated</span></span></li>
<li><span data-ttu-id="0096a-444">IOAV : téléchargements d’IE et Outlook pièces jointes Express lancées</span><span class="sxs-lookup"><span data-stu-id="0096a-444">IOAV: IE Downloads and Outlook Express Attachments initiated</span></span></li>
<li><span data-ttu-id="0096a-445">NIS : système d’inspection du réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-445">NIS: Network inspection system</span></span></li>
<li><span data-ttu-id="0096a-446">IEPROTECT : IE - IExtensionValidation ; cela protège contre les contrôles de page web malveillants</span><span class="sxs-lookup"><span data-stu-id="0096a-446">IEPROTECT: IE - IExtensionValidation; this protects against malicious webpage controls</span></span></li>
<li><span data-ttu-id="0096a-447">Logiciel anti-programme malveillant à lancement précoce (ELAM).</span><span class="sxs-lookup"><span data-stu-id="0096a-447">Early Launch Antimalware (ELAM).</span></span> <span data-ttu-id="0096a-448">Cela inclut les programmes malveillants détectés par la séquence de démarrage</span><span class="sxs-lookup"><span data-stu-id="0096a-448">This includes malware detected by the boot sequence</span></span></li>
<li><span data-ttu-id="0096a-449">Attestation à distance</span><span class="sxs-lookup"><span data-stu-id="0096a-449">Remote attestation</span></span></li>
</ul><span data-ttu-id="0096a-450">Interface d’analyse anti-programme malveillant (AMSI).</span><span class="sxs-lookup"><span data-stu-id="0096a-450">Antimalware Scan Interface (AMSI).</span></span> <span data-ttu-id="0096a-451">Principalement utilisé pour protéger les scripts (PS, VBS), bien qu’il puisse également être appelé par des tiers.</span><span class="sxs-lookup"><span data-stu-id="0096a-451">Primarily used to protect scripts (PS, VBS), though it can be invoked by third parties as well.</span></span>
<span data-ttu-id="0096a-452">Utilisateur UAC </dt> 
<dt>: domaine &lt; &gt; \& lt; User &gt; </dt>
<dt>Process Name: &lt; Process &gt; in the PID</dt>
<dt>Signature Version: &lt; Definition version &gt; </dt>Engine
<dt>Version: Antimalware Engine &lt; version &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-452">UAC</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Process Name: &lt;Process in the PID&gt;</dt>
<dt>Signature Version: &lt;Definition version&gt;</dt>
<dt>Engine Version: &lt;Antimalware Engine version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-453">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-453">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-454">Aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="0096a-454">No action is required.</span></span> <span data-ttu-id="0096a-455">Antivirus Microsoft Defender pouvez suspendre et prendre des mesures de routine sur cette menace.</span><span class="sxs-lookup"><span data-stu-id="0096a-455">Microsoft Defender Antivirus can suspend and take routine action on this threat.</span></span> <span data-ttu-id="0096a-456">Si vous souhaitez supprimer la menace manuellement, dans l’interface Antivirus Microsoft Defender, cliquez <b>sur Nettoyer l’ordinateur.</b></span><span class="sxs-lookup"><span data-stu-id="0096a-456">If you want to remove the threat manually, in the Microsoft Defender Antivirus interface, click <b>Clean Computer</b>.</span></span>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-457">ID d’événement : 1117</span><span class="sxs-lookup"><span data-stu-id="0096a-457">Event ID: 1117</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-458">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-458">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-459">
<b>MALWAREPROTECTION_STATE_MALWARE_ACTION_TAKEN </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-459">
<b>MALWAREPROTECTION_STATE_MALWARE_ACTION_TAKEN </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-460">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-460">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-461">
<b>La plateforme anti-programme malveillant a effectué une action pour protéger votre système contre les programmes malveillants ou d’autres logiciels potentiellement indésirables. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-461">
<b>The antimalware platform performed an action to protect your system from malware or other potentially unwanted software. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-462">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-462">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-463">Antivirus Microsoft Defender a pris des mesures pour protéger cet ordinateur contre les programmes malveillants ou d’autres logiciels potentiellement indésirables.</span><span class="sxs-lookup"><span data-stu-id="0096a-463">Microsoft Defender Antivirus has taken action to protect this machine from malware or other potentially unwanted software.</span></span><br/><span data-ttu-id="0096a-464">Pour plus d'informations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="0096a-464">For more information, see the following:</span></span>
<dl><span data-ttu-id="0096a-465">
<dt>Nom : &lt; ID &gt; du nom</dt>
<dt>de la menace : Gravité de &lt; l’ID &gt; </dt>de menace : 
<dt> &lt; &gt; Gravité, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-465">
<dt>Name: &lt;Threat name&gt;</dt>
<dt>ID: &lt;Threat ID&gt;</dt>
<dt>Severity: &lt;Severity&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-466">Faible</span><span class="sxs-lookup"><span data-stu-id="0096a-466">Low</span></span></li>
<li><span data-ttu-id="0096a-467">Modéré</span><span class="sxs-lookup"><span data-stu-id="0096a-467">Moderate</span></span></li>
<li><span data-ttu-id="0096a-468">Élevé</span><span class="sxs-lookup"><span data-stu-id="0096a-468">High</span></span></li>
<li><span data-ttu-id="0096a-469">Grave</span><span class="sxs-lookup"><span data-stu-id="0096a-469">Severe</span></span></li>
</ul><span data-ttu-id="0096a-470">
</dt>
<dt>Catégorie : &lt; Description de &gt; catégorie, par exemple, tout type de menace ou de programme malveillant.</dt> 
<dt>Chemin d’accès : &lt; Origine &gt; de la détection</dt> 
<dt> du chemin d’accès &lt; au fichier : origine de la &gt; détection, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-470">
</dt>
<dt>Category: &lt;Category description&gt;, for example, any threat or malware type.</dt>
<dt>Path: &lt;File path&gt;</dt>
<dt>Detection Origin: &lt;Detection origin&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-471">Inconnu</span><span class="sxs-lookup"><span data-stu-id="0096a-471">Unknown</span></span></li>
<li><span data-ttu-id="0096a-472">Ordinateur local</span><span class="sxs-lookup"><span data-stu-id="0096a-472">Local computer</span></span></li>
<li><span data-ttu-id="0096a-473">Partage réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-473">Network share</span></span></li>
<li><span data-ttu-id="0096a-474">Internet</span><span class="sxs-lookup"><span data-stu-id="0096a-474">Internet</span></span></li>
<li><span data-ttu-id="0096a-475">Trafic entrant</span><span class="sxs-lookup"><span data-stu-id="0096a-475">Incoming traffic</span></span></li>
<li><span data-ttu-id="0096a-476">Trafic sortant</span><span class="sxs-lookup"><span data-stu-id="0096a-476">Outgoing traffic</span></span></li>
</ul><span data-ttu-id="0096a-477">
</dt>
<dt>Type de détection &lt; : type de &gt; détection, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-477">
</dt>
<dt>Detection Type: &lt;Detection type&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-478">Heuristics</span><span class="sxs-lookup"><span data-stu-id="0096a-478">Heuristics</span></span></li>
<li><span data-ttu-id="0096a-479">Generic</span><span class="sxs-lookup"><span data-stu-id="0096a-479">Generic</span></span></li>
<li><span data-ttu-id="0096a-480">Concret</span><span class="sxs-lookup"><span data-stu-id="0096a-480">Concrete</span></span></li>
<li><span data-ttu-id="0096a-481">Signature dynamique</span><span class="sxs-lookup"><span data-stu-id="0096a-481">Dynamic signature</span></span></li>
</ul><span data-ttu-id="0096a-482">
</dt>
<dt>Source de détection : &lt; source de détection par exemple &gt; :</span><span class="sxs-lookup"><span data-stu-id="0096a-482">
</dt>
<dt>Detection Source: &lt;Detection source&gt; for example:</span></span><ul>
<li><span data-ttu-id="0096a-483">Utilisateur : initié par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="0096a-483">User: user initiated</span></span></li>
<li><span data-ttu-id="0096a-484">Système : initié par le système</span><span class="sxs-lookup"><span data-stu-id="0096a-484">System: system initiated</span></span></li>
<li><span data-ttu-id="0096a-485">En temps réel : composant en temps réel initié</span><span class="sxs-lookup"><span data-stu-id="0096a-485">Real-time: real-time component initiated</span></span></li>
<li><span data-ttu-id="0096a-486">IOAV : téléchargements d’IE et Outlook pièces jointes Express lancées</span><span class="sxs-lookup"><span data-stu-id="0096a-486">IOAV: IE Downloads and Outlook Express Attachments initiated</span></span></li>
<li><span data-ttu-id="0096a-487">NIS : système d’inspection du réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-487">NIS: Network inspection system</span></span></li>
<li><span data-ttu-id="0096a-488">IEPROTECT : IE - IExtensionValidation ; cela protège contre les contrôles de page web malveillants</span><span class="sxs-lookup"><span data-stu-id="0096a-488">IEPROTECT: IE - IExtensionValidation; this protects against malicious webpage controls</span></span></li>
<li><span data-ttu-id="0096a-489">Logiciel anti-programme malveillant à lancement précoce (ELAM).</span><span class="sxs-lookup"><span data-stu-id="0096a-489">Early Launch Antimalware (ELAM).</span></span> <span data-ttu-id="0096a-490">Cela inclut les programmes malveillants détectés par la séquence de démarrage</span><span class="sxs-lookup"><span data-stu-id="0096a-490">This includes malware detected by the boot sequence</span></span></li>
<li><span data-ttu-id="0096a-491">Attestation à distance</span><span class="sxs-lookup"><span data-stu-id="0096a-491">Remote attestation</span></span></li>
</ul><span data-ttu-id="0096a-492">Interface d’analyse anti-programme malveillant (AMSI).</span><span class="sxs-lookup"><span data-stu-id="0096a-492">Antimalware Scan Interface (AMSI).</span></span> <span data-ttu-id="0096a-493">Principalement utilisé pour protéger les scripts (PS, VBS), bien qu’il puisse également être appelé par des tiers.</span><span class="sxs-lookup"><span data-stu-id="0096a-493">Primarily used to protect scripts (PS, VBS), though it can be invoked by third parties as well.</span></span>
<span data-ttu-id="0096a-494">Utilisateur UAC </dt> 
<dt>: domaine &lt; &gt; \& lt; Nom &gt; </dt>
<dt>du processus utilisateur : processus dans &lt; l’action &gt; PID</dt>: 
<dt> &lt; &gt; Action, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-494">UAC</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Process Name: &lt;Process in the PID&gt;</dt>
<dt>Action: &lt;Action&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-495">Nettoyer : la ressource a été nettoyée</span><span class="sxs-lookup"><span data-stu-id="0096a-495">Clean: The resource was cleaned</span></span></li>
<li><span data-ttu-id="0096a-496">Quarantaine : la ressource a été mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="0096a-496">Quarantine: The resource was quarantined</span></span></li>
<li><span data-ttu-id="0096a-497">Supprimer : la ressource a été supprimée</span><span class="sxs-lookup"><span data-stu-id="0096a-497">Remove: The resource was deleted</span></span></li>
<li><span data-ttu-id="0096a-498">Autoriser : la ressource a été autorisée à s’exécuter/exister</span><span class="sxs-lookup"><span data-stu-id="0096a-498">Allow: The resource was allowed to execute/exist</span></span></li>
<li><span data-ttu-id="0096a-499">Défini par l’utilisateur : action définie par l’utilisateur qui est normalement une de cette liste d’actions que l’utilisateur a spécifiée</span><span class="sxs-lookup"><span data-stu-id="0096a-499">User defined: User-defined action that is normally one from this list of actions that the user has specified</span></span></li>
<li><span data-ttu-id="0096a-500">Aucune action : aucune action</span><span class="sxs-lookup"><span data-stu-id="0096a-500">No action: No action</span></span></li>
<li><span data-ttu-id="0096a-501">Bloc : l’exécution de la ressource a été bloquée</span><span class="sxs-lookup"><span data-stu-id="0096a-501">Block: The resource was blocked from executing</span></span></li>
</ul><span data-ttu-id="0096a-502">
</dt>
<dt>État de l’action : &lt; Description des &gt; actions supplémentaires Code</dt>
<dt>d’erreur : &lt; code de résultat de code &gt; d’erreur associé à l’état de la menace. Valeurs HRESULT standard.</dt> 
<dt>Description de l’erreur : &lt; Description de &gt; l’erreur.</dt> 
<dt>Version de la signature : &lt; &gt;</dt>Version du moteur de définition :
<dt> &lt; Antimalware Engine version &gt; </dt> REMARQUE : chaque fois que Antivirus Microsoft Defender, Microsoft Security Essentials, outil de suppression de logiciels malveillants ou System Center Endpoint Protection détecte un programme malveillant, il restaure les paramètres et services système suivants qui ont pu être modifiés :</span><span class="sxs-lookup"><span data-stu-id="0096a-502">
</dt>
<dt>Action Status: &lt;Description of additional actions&gt;</dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values.</dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
<dt>Signature Version: &lt;Definition version&gt;</dt>
<dt>Engine Version: &lt;Antimalware Engine version&gt;</dt> NOTE: Whenever Microsoft Defender Antivirus, Microsoft Security Essentials, Malicious Software Removal Tool, or System Center Endpoint Protection detects a malware, it will restore the following system settings and services that the malware might have changed:</span></span><ul>
<li><span data-ttu-id="0096a-503">Paramètre par défaut d’Internet Explorer Microsoft Edge paramètre</span><span class="sxs-lookup"><span data-stu-id="0096a-503">Default Internet Explorer or Microsoft Edge setting</span></span></li>
<li><span data-ttu-id="0096a-504">Paramètres du contrôle d’accès utilisateur</span><span class="sxs-lookup"><span data-stu-id="0096a-504">User Access Control settings</span></span></li>
<li><span data-ttu-id="0096a-505">Paramètres Chrome</span><span class="sxs-lookup"><span data-stu-id="0096a-505">Chrome settings</span></span></li>
<li><span data-ttu-id="0096a-506">Données du contrôle de démarrage</span><span class="sxs-lookup"><span data-stu-id="0096a-506">Boot Control Data</span></span></li>
<li><span data-ttu-id="0096a-507">Paramètres de Registre Regedit et du Gestionnaire des tâches</span><span class="sxs-lookup"><span data-stu-id="0096a-507">Regedit and Task Manager registry settings</span></span></li>
<li><span data-ttu-id="0096a-508">Windows Mise à jour, service de transfert intelligent en arrière-plan et service d’appel de procédure distante</span><span class="sxs-lookup"><span data-stu-id="0096a-508">Windows Update, Background Intelligent Transfer Service, and Remote Procedure Call service</span></span></li>
<li><span data-ttu-id="0096a-509">Windows Fichiers du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="0096a-509">Windows Operating System files</span></span></li></ul>
<span data-ttu-id="0096a-510">Le contexte ci-dessus s’applique aux versions client et serveur suivantes :</span><span class="sxs-lookup"><span data-stu-id="0096a-510">The above context applies to the following client and server versions:</span></span>
<table>
<tr>
<th><span data-ttu-id="0096a-511">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="0096a-511">Operating system</span></span></th>
<th><span data-ttu-id="0096a-512">Version du système d'exploitation</span><span class="sxs-lookup"><span data-stu-id="0096a-512">Operating system version</span></span></th>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-513">Système d’exploitation client</span><span class="sxs-lookup"><span data-stu-id="0096a-513">Client Operating System</span></span>
</td>
<td>
<span data-ttu-id="0096a-514">Windows Vista (Service Pack 1 ou Service Pack 2), Windows 7 et ultérieures</span><span class="sxs-lookup"><span data-stu-id="0096a-514">Windows Vista (Service Pack 1, or Service Pack 2), Windows 7 and later</span></span>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-515">Système d’exploitation du serveur</span><span class="sxs-lookup"><span data-stu-id="0096a-515">Server Operating System</span></span>
</td>
<td>
<span data-ttu-id="0096a-516">Windows Server 2008, Windows Server 2008 R2, Windows Server 2012 et Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0096a-516">Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, and Windows Server 2016</span></span>
</td>
</tr>
</table>
</dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-517">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-517">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-518">Aucune action n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0096a-518">No action is necessary.</span></span> <span data-ttu-id="0096a-519">Antivirus Microsoft Defender une menace est supprimée ou mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="0096a-519">Microsoft Defender Antivirus removed or quarantined a threat.</span></span> 
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-520">ID d’événement : 1118</span><span class="sxs-lookup"><span data-stu-id="0096a-520">Event ID: 1118</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-521">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-521">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-522">
<b>MALWAREPROTECTION_STATE_MALWARE_ACTION_FAILED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-522">
<b>MALWAREPROTECTION_STATE_MALWARE_ACTION_FAILED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-523">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-523">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-524">
<b>La plateforme anti-programme malveillant a tenté d’effectuer une action pour protéger votre système contre les programmes malveillants ou d’autres logiciels potentiellement indésirables, mais l’action a échoué. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-524">
<b>The antimalware platform attempted to perform an action to protect your system from malware or other potentially unwanted software, but the action failed. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-525">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-525">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-526">Antivirus Microsoft Defender a rencontré une erreur non critique lors de l’action sur des programmes malveillants ou d’autres logiciels potentiellement indésirables.</span><span class="sxs-lookup"><span data-stu-id="0096a-526">Microsoft Defender Antivirus has encountered a non-critical error when taking action on malware or other potentially unwanted software.</span></span><br/><span data-ttu-id="0096a-527">Pour plus d'informations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="0096a-527">For more information, see the following:</span></span>
<dl><span data-ttu-id="0096a-528">
<dt>Nom : &lt; ID &gt; du nom</dt>
<dt>de la menace : Gravité de &lt; l’ID &gt; </dt>de menace : 
<dt> &lt; &gt; Gravité, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-528">
<dt>Name: &lt;Threat name&gt;</dt>
<dt>ID: &lt;Threat ID&gt;</dt>
<dt>Severity: &lt;Severity&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-529">Faible</span><span class="sxs-lookup"><span data-stu-id="0096a-529">Low</span></span></li>
<li><span data-ttu-id="0096a-530">Modéré</span><span class="sxs-lookup"><span data-stu-id="0096a-530">Moderate</span></span></li>
<li><span data-ttu-id="0096a-531">Élevé</span><span class="sxs-lookup"><span data-stu-id="0096a-531">High</span></span></li>
<li><span data-ttu-id="0096a-532">Grave</span><span class="sxs-lookup"><span data-stu-id="0096a-532">Severe</span></span></li>
</ul><span data-ttu-id="0096a-533">
</dt>
<dt>Catégorie : &lt; Description de &gt; catégorie, par exemple, tout type de menace ou de programme malveillant.</dt> 
<dt>Chemin d’accès : &lt; Origine &gt; de la détection</dt> 
<dt> du chemin d’accès &lt; au fichier : origine de la &gt; détection, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-533">
</dt>
<dt>Category: &lt;Category description&gt;, for example, any threat or malware type.</dt>
<dt>Path: &lt;File path&gt;</dt>
<dt>Detection Origin: &lt;Detection origin&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-534">Inconnu</span><span class="sxs-lookup"><span data-stu-id="0096a-534">Unknown</span></span></li>
<li><span data-ttu-id="0096a-535">Ordinateur local</span><span class="sxs-lookup"><span data-stu-id="0096a-535">Local computer</span></span></li>
<li><span data-ttu-id="0096a-536">Partage réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-536">Network share</span></span></li>
<li><span data-ttu-id="0096a-537">Internet</span><span class="sxs-lookup"><span data-stu-id="0096a-537">Internet</span></span></li>
<li><span data-ttu-id="0096a-538">Trafic entrant</span><span class="sxs-lookup"><span data-stu-id="0096a-538">Incoming traffic</span></span></li>
<li><span data-ttu-id="0096a-539">Trafic sortant</span><span class="sxs-lookup"><span data-stu-id="0096a-539">Outgoing traffic</span></span></li>
</ul><span data-ttu-id="0096a-540">
</dt>
<dt>Type de détection &lt; : type de &gt; détection, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-540">
</dt>
<dt>Detection Type: &lt;Detection type&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-541">Heuristics</span><span class="sxs-lookup"><span data-stu-id="0096a-541">Heuristics</span></span></li>
<li><span data-ttu-id="0096a-542">Generic</span><span class="sxs-lookup"><span data-stu-id="0096a-542">Generic</span></span></li>
<li><span data-ttu-id="0096a-543">Concret</span><span class="sxs-lookup"><span data-stu-id="0096a-543">Concrete</span></span></li>
<li><span data-ttu-id="0096a-544">Signature dynamique</span><span class="sxs-lookup"><span data-stu-id="0096a-544">Dynamic signature</span></span></li>
</ul><span data-ttu-id="0096a-545">
</dt>
<dt>Source de détection : &lt; source de détection par exemple &gt; :</span><span class="sxs-lookup"><span data-stu-id="0096a-545">
</dt>
<dt>Detection Source: &lt;Detection source&gt; for example:</span></span><ul>
<li><span data-ttu-id="0096a-546">Utilisateur : initié par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="0096a-546">User: user initiated</span></span></li>
<li><span data-ttu-id="0096a-547">Système : initié par le système</span><span class="sxs-lookup"><span data-stu-id="0096a-547">System: system initiated</span></span></li>
<li><span data-ttu-id="0096a-548">En temps réel : composant en temps réel initié</span><span class="sxs-lookup"><span data-stu-id="0096a-548">Real-time: real-time component initiated</span></span></li>
<li><span data-ttu-id="0096a-549">IOAV : téléchargements d’IE et Outlook pièces jointes Express lancées</span><span class="sxs-lookup"><span data-stu-id="0096a-549">IOAV: IE Downloads and Outlook Express Attachments initiated</span></span></li>
<li><span data-ttu-id="0096a-550">NIS : système d’inspection du réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-550">NIS: Network inspection system</span></span></li>
<li><span data-ttu-id="0096a-551">IEPROTECT : IE - IExtensionValidation ; cela protège contre les contrôles de page web malveillants</span><span class="sxs-lookup"><span data-stu-id="0096a-551">IEPROTECT: IE - IExtensionValidation; this protects against malicious webpage controls</span></span></li>
<li><span data-ttu-id="0096a-552">Logiciel anti-programme malveillant à lancement précoce (ELAM).</span><span class="sxs-lookup"><span data-stu-id="0096a-552">Early Launch Antimalware (ELAM).</span></span> <span data-ttu-id="0096a-553">Cela inclut les programmes malveillants détectés par la séquence de démarrage</span><span class="sxs-lookup"><span data-stu-id="0096a-553">This includes malware detected by the boot sequence</span></span></li>
<li><span data-ttu-id="0096a-554">Attestation à distance</span><span class="sxs-lookup"><span data-stu-id="0096a-554">Remote attestation</span></span></li>
</ul><span data-ttu-id="0096a-555">Interface d’analyse anti-programme malveillant (AMSI).</span><span class="sxs-lookup"><span data-stu-id="0096a-555">Antimalware Scan Interface (AMSI).</span></span> <span data-ttu-id="0096a-556">Principalement utilisé pour protéger les scripts (PS, VBS), bien qu’il puisse également être appelé par des tiers.</span><span class="sxs-lookup"><span data-stu-id="0096a-556">Primarily used to protect scripts (PS, VBS), though it can be invoked by third parties as well.</span></span>
<span data-ttu-id="0096a-557">Utilisateur UAC </dt> 
<dt>: domaine &lt; &gt; \& lt; Nom &gt; </dt>
<dt>du processus utilisateur : processus dans &lt; l’action &gt; PID</dt>: 
<dt> &lt; &gt; Action, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-557">UAC</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Process Name: &lt;Process in the PID&gt;</dt>
<dt>Action: &lt;Action&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-558">Nettoyer : la ressource a été nettoyée</span><span class="sxs-lookup"><span data-stu-id="0096a-558">Clean: The resource was cleaned</span></span></li>
<li><span data-ttu-id="0096a-559">Quarantaine : la ressource a été mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="0096a-559">Quarantine: The resource was quarantined</span></span></li>
<li><span data-ttu-id="0096a-560">Supprimer : la ressource a été supprimée</span><span class="sxs-lookup"><span data-stu-id="0096a-560">Remove: The resource was deleted</span></span></li>
<li><span data-ttu-id="0096a-561">Autoriser : la ressource a été autorisée à s’exécuter/exister</span><span class="sxs-lookup"><span data-stu-id="0096a-561">Allow: The resource was allowed to execute/exist</span></span></li>
<li><span data-ttu-id="0096a-562">Défini par l’utilisateur : action définie par l’utilisateur qui est normalement une de cette liste d’actions que l’utilisateur a spécifiée</span><span class="sxs-lookup"><span data-stu-id="0096a-562">User defined: User-defined action that is normally one from this list of actions that the user has specified</span></span></li>
<li><span data-ttu-id="0096a-563">Aucune action : aucune action</span><span class="sxs-lookup"><span data-stu-id="0096a-563">No action: No action</span></span></li>
<li><span data-ttu-id="0096a-564">Bloc : l’exécution de la ressource a été bloquée</span><span class="sxs-lookup"><span data-stu-id="0096a-564">Block: The resource was blocked from executing</span></span></li>
</ul><span data-ttu-id="0096a-565">
</dt>
<dt>État de l’action : &lt; Description des &gt; actions supplémentaires Code</dt>
<dt>d’erreur : &lt; code de résultat de code &gt; d’erreur associé à l’état de la menace. Valeurs HRESULT standard.</dt> 
<dt>Description de l’erreur : &lt; Description de &gt; l’erreur.</dt> 
<dt>Version de la signature : &lt; Version &gt; du moteur</dt>
<dt>de définition : Antimalware Engine &lt; version &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-565">
</dt>
<dt>Action Status: &lt;Description of additional actions&gt;</dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values.</dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
<dt>Signature Version: &lt;Definition version&gt;</dt>
<dt>Engine Version: &lt;Antimalware Engine version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-566">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-566">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-567">Aucune action n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0096a-567">No action is necessary.</span></span> <span data-ttu-id="0096a-568">Antivirus Microsoft Defender n’a pas réussi à effectuer une tâche liée à la correction des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="0096a-568">Microsoft Defender Antivirus failed to complete a task related to the malware remediation.</span></span> <span data-ttu-id="0096a-569">Il ne s’agit pas d’une défaillance critique.</span><span class="sxs-lookup"><span data-stu-id="0096a-569">This is not a critical failure.</span></span>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-570">ID d’événement : 1119</span><span class="sxs-lookup"><span data-stu-id="0096a-570">Event ID: 1119</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-571">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-571">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-572">
<b>MALWAREPROTECTION_STATE_MALWARE_ACTION_CRITICALLY_FAILED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-572">
<b>MALWAREPROTECTION_STATE_MALWARE_ACTION_CRITICALLY_FAILED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-573">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-573">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-574">
<b>La plateforme anti-programme malveillant a rencontré une erreur critique lors de la tentative d’action sur des programmes malveillants ou d’autres logiciels potentiellement indésirables. Le message d’événement est plus détaillé.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-574">
<b>The antimalware platform encountered a critical error when trying to take action on malware or other potentially unwanted software. There are more details in the event message.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-575">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-575">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-576">Antivirus Microsoft Defender a rencontré une erreur critique lors de l’action sur des programmes malveillants ou d’autres logiciels potentiellement indésirables.</span><span class="sxs-lookup"><span data-stu-id="0096a-576">Microsoft Defender Antivirus has encountered a critical error when taking action on malware or other potentially unwanted software.</span></span><br/><span data-ttu-id="0096a-577">Pour plus d'informations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="0096a-577">For more information, see the following:</span></span>
<dl><span data-ttu-id="0096a-578">
<dt>Nom : &lt; ID &gt; du nom</dt>
<dt>de la menace : Gravité de &lt; l’ID &gt; </dt>de menace : 
<dt> &lt; &gt; Gravité, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-578">
<dt>Name: &lt;Threat name&gt;</dt>
<dt>ID: &lt;Threat ID&gt;</dt>
<dt>Severity: &lt;Severity&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-579">Faible</span><span class="sxs-lookup"><span data-stu-id="0096a-579">Low</span></span></li>
<li><span data-ttu-id="0096a-580">Modéré</span><span class="sxs-lookup"><span data-stu-id="0096a-580">Moderate</span></span></li>
<li><span data-ttu-id="0096a-581">Élevé</span><span class="sxs-lookup"><span data-stu-id="0096a-581">High</span></span></li>
<li><span data-ttu-id="0096a-582">Grave</span><span class="sxs-lookup"><span data-stu-id="0096a-582">Severe</span></span></li>
</ul><span data-ttu-id="0096a-583">
</dt>
<dt>Catégorie : &lt; Description de &gt; catégorie, par exemple, tout type de menace ou de programme malveillant.</dt> 
<dt>Chemin d’accès : &lt; Origine &gt; de la détection</dt> 
<dt> du chemin d’accès &lt; au fichier : origine de la &gt; détection, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-583">
</dt>
<dt>Category: &lt;Category description&gt;, for example, any threat or malware type.</dt>
<dt>Path: &lt;File path&gt;</dt>
<dt>Detection Origin: &lt;Detection origin&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-584">Inconnu</span><span class="sxs-lookup"><span data-stu-id="0096a-584">Unknown</span></span></li>
<li><span data-ttu-id="0096a-585">Ordinateur local</span><span class="sxs-lookup"><span data-stu-id="0096a-585">Local computer</span></span></li>
<li><span data-ttu-id="0096a-586">Partage réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-586">Network share</span></span></li>
<li><span data-ttu-id="0096a-587">Internet</span><span class="sxs-lookup"><span data-stu-id="0096a-587">Internet</span></span></li>
<li><span data-ttu-id="0096a-588">Trafic entrant</span><span class="sxs-lookup"><span data-stu-id="0096a-588">Incoming traffic</span></span></li>
<li><span data-ttu-id="0096a-589">Trafic sortant</span><span class="sxs-lookup"><span data-stu-id="0096a-589">Outgoing traffic</span></span></li>
</ul><span data-ttu-id="0096a-590">
</dt>
<dt>Type de détection &lt; : type de &gt; détection, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-590">
</dt>
<dt>Detection Type: &lt;Detection type&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-591">Heuristics</span><span class="sxs-lookup"><span data-stu-id="0096a-591">Heuristics</span></span></li>
<li><span data-ttu-id="0096a-592">Generic</span><span class="sxs-lookup"><span data-stu-id="0096a-592">Generic</span></span></li>
<li><span data-ttu-id="0096a-593">Concret</span><span class="sxs-lookup"><span data-stu-id="0096a-593">Concrete</span></span></li>
<li><span data-ttu-id="0096a-594">Signature dynamique</span><span class="sxs-lookup"><span data-stu-id="0096a-594">Dynamic signature</span></span></li>
</ul><span data-ttu-id="0096a-595">
</dt>
<dt>Source de détection : &lt; source de détection par exemple &gt; :</span><span class="sxs-lookup"><span data-stu-id="0096a-595">
</dt>
<dt>Detection Source: &lt;Detection source&gt; for example:</span></span><ul>
<li><span data-ttu-id="0096a-596">Utilisateur : initié par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="0096a-596">User: user initiated</span></span></li>
<li><span data-ttu-id="0096a-597">Système : initié par le système</span><span class="sxs-lookup"><span data-stu-id="0096a-597">System: system initiated</span></span></li>
<li><span data-ttu-id="0096a-598">En temps réel : composant en temps réel initié</span><span class="sxs-lookup"><span data-stu-id="0096a-598">Real-time: real-time component initiated</span></span></li>
<li><span data-ttu-id="0096a-599">IOAV : téléchargements d’IE et Outlook pièces jointes Express lancées</span><span class="sxs-lookup"><span data-stu-id="0096a-599">IOAV: IE Downloads and Outlook Express Attachments initiated</span></span></li>
<li><span data-ttu-id="0096a-600">NIS : système d’inspection du réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-600">NIS: Network inspection system</span></span></li>
<li><span data-ttu-id="0096a-601">IEPROTECT : IE - IExtensionValidation ; cela protège contre les contrôles de page web malveillants</span><span class="sxs-lookup"><span data-stu-id="0096a-601">IEPROTECT: IE - IExtensionValidation; this protects against malicious webpage controls</span></span></li>
<li><span data-ttu-id="0096a-602">Logiciel anti-programme malveillant à lancement précoce (ELAM).</span><span class="sxs-lookup"><span data-stu-id="0096a-602">Early Launch Antimalware (ELAM).</span></span> <span data-ttu-id="0096a-603">Cela inclut les programmes malveillants détectés par la séquence de démarrage</span><span class="sxs-lookup"><span data-stu-id="0096a-603">This includes malware detected by the boot sequence</span></span></li>
<li><span data-ttu-id="0096a-604">Attestation à distance</span><span class="sxs-lookup"><span data-stu-id="0096a-604">Remote attestation</span></span></li>
</ul><span data-ttu-id="0096a-605">Interface d’analyse anti-programme malveillant (AMSI).</span><span class="sxs-lookup"><span data-stu-id="0096a-605">Antimalware Scan Interface (AMSI).</span></span> <span data-ttu-id="0096a-606">Principalement utilisé pour protéger les scripts (PS, VBS), bien qu’il puisse également être appelé par des tiers.</span><span class="sxs-lookup"><span data-stu-id="0096a-606">Primarily used to protect scripts (PS, VBS), though it can be invoked by third parties as well.</span></span>
<span data-ttu-id="0096a-607">Utilisateur UAC </dt> 
<dt>: domaine &lt; &gt; \& lt; Nom &gt; </dt>
<dt>du processus utilisateur : processus dans &lt; l’action &gt; PID</dt>: 
<dt> &lt; &gt; Action, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-607">UAC</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Process Name: &lt;Process in the PID&gt;</dt>
<dt>Action: &lt;Action&gt;, for example:</span></span><ul>
<li><span data-ttu-id="0096a-608">Nettoyer : la ressource a été nettoyée</span><span class="sxs-lookup"><span data-stu-id="0096a-608">Clean: The resource was cleaned</span></span></li>
<li><span data-ttu-id="0096a-609">Quarantaine : la ressource a été mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="0096a-609">Quarantine: The resource was quarantined</span></span></li>
<li><span data-ttu-id="0096a-610">Supprimer : la ressource a été supprimée</span><span class="sxs-lookup"><span data-stu-id="0096a-610">Remove: The resource was deleted</span></span></li>
<li><span data-ttu-id="0096a-611">Autoriser : la ressource a été autorisée à s’exécuter/exister</span><span class="sxs-lookup"><span data-stu-id="0096a-611">Allow: The resource was allowed to execute/exist</span></span></li>
<li><span data-ttu-id="0096a-612">Défini par l’utilisateur : action définie par l’utilisateur qui est normalement une de cette liste d’actions que l’utilisateur a spécifiée</span><span class="sxs-lookup"><span data-stu-id="0096a-612">User defined: User-defined action that is normally one from this list of actions that the user has specified</span></span></li>
<li><span data-ttu-id="0096a-613">Aucune action : aucune action</span><span class="sxs-lookup"><span data-stu-id="0096a-613">No action: No action</span></span></li>
<li><span data-ttu-id="0096a-614">Bloc : l’exécution de la ressource a été bloquée</span><span class="sxs-lookup"><span data-stu-id="0096a-614">Block: The resource was blocked from executing</span></span></li>
</ul><span data-ttu-id="0096a-615">
</dt>
<dt>État de l’action : &lt; Description des &gt; actions supplémentaires Code</dt>
<dt>d’erreur : &lt; code de résultat de code &gt; d’erreur associé à l’état de la menace. Valeurs HRESULT standard.</dt> 
<dt>Description de l’erreur : &lt; Description de &gt; l’erreur.</dt> 
<dt>Version de la signature : &lt; Version &gt; du moteur</dt>
<dt>de définition : Antimalware Engine &lt; version &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-615">
</dt>
<dt>Action Status: &lt;Description of additional actions&gt;</dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values.</dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
<dt>Signature Version: &lt;Definition version&gt;</dt>
<dt>Engine Version: &lt;Antimalware Engine version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-616">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-616">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-617">Le Antivirus Microsoft Defender client a rencontré cette erreur en raison de problèmes critiques.</span><span class="sxs-lookup"><span data-stu-id="0096a-617">The Microsoft Defender Antivirus client encountered this error due to critical issues.</span></span> <span data-ttu-id="0096a-618">Le point de terminaison peut ne pas être protégé.</span><span class="sxs-lookup"><span data-stu-id="0096a-618">The endpoint might not be protected.</span></span> <span data-ttu-id="0096a-619">Examinez la description de l’erreur, puis suivez les étapes <b>d’action utilisateur appropriées</b> ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="0096a-619">Review the error description then follow the relevant <b>User action</b> steps below.</span></span>
<table>
<tr>
<th><span data-ttu-id="0096a-620">Action</span><span class="sxs-lookup"><span data-stu-id="0096a-620">Action</span></span></th>
<th><span data-ttu-id="0096a-621">Action de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="0096a-621">User action</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="0096a-622">
<b>Supprimer</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-622">
<b>Remove</b>
</span></span></td>
<td>
<span data-ttu-id="0096a-623">Mettez à jour les définitions, puis vérifiez que la suppression a réussi.</span><span class="sxs-lookup"><span data-stu-id="0096a-623">Update the definitions then verify that the removal was successful.</span></span>
</td>
</tr>
<tr>
<td><span data-ttu-id="0096a-624">
<b>Clean</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-624">
<b>Clean</b>
</span></span></td>
<td>
<span data-ttu-id="0096a-625">Mettez à jour les définitions, puis vérifiez que la correction a réussi.</span><span class="sxs-lookup"><span data-stu-id="0096a-625">Update the definitions then verify that the remediation was successful.</span></span>
</td>
</tr>
<tr>
<td><span data-ttu-id="0096a-626">
<b>Quarantaine</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-626">
<b>Quarantine</b>
</span></span></td>
<td>
<span data-ttu-id="0096a-627">Mettez à jour les définitions et vérifiez que l’utilisateur est autorisé à accéder aux ressources nécessaires.</span><span class="sxs-lookup"><span data-stu-id="0096a-627">Update the definitions and verify that the user has permission to access the necessary resources.</span></span>
</td>
</tr>
<tr>
<td><span data-ttu-id="0096a-628">
<b>Autoriser</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-628">
<b>Allow</b>
</span></span></td>
<td>
<span data-ttu-id="0096a-629">Vérifiez que l’utilisateur est autorisé à accéder aux ressources nécessaires.</span><span class="sxs-lookup"><span data-stu-id="0096a-629">Verify that the user has permission to access the necessary resources.</span></span>
</td>
</tr>
</table>

<span data-ttu-id="0096a-630">Si cet événement persiste :</span><span class="sxs-lookup"><span data-stu-id="0096a-630">If this event persists:</span></span><ol>
<li><span data-ttu-id="0096a-631">Exécutez à nouveau l’analyse.</span><span class="sxs-lookup"><span data-stu-id="0096a-631">Run the scan again.</span></span></li>
<li><span data-ttu-id="0096a-632">Si elle échoue de la même manière, allez sur le <b></b> site de support <a href="https://go.microsoft.com/fwlink/?LinkId=215163">Microsoft</a>, entrez le numéro d’erreur dans la zone de recherche pour rechercher le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0096a-632">If it fails in the same way, go to the <a href="https://go.microsoft.com/fwlink/?LinkId=215163">Microsoft Support site</a>, enter the error number in the <b>Search</b> box to look for the error code.</span></span></li>
<li><span data-ttu-id="0096a-633">Contactez le <a href="https://go.microsoft.com/fwlink/?LinkId=215491">Support technique Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="0096a-633">Contact <a href="https://go.microsoft.com/fwlink/?LinkId=215491">Microsoft Technical Support</a>.</span></span>
</li>
</ol>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-634">ID d’événement : 1120</span><span class="sxs-lookup"><span data-stu-id="0096a-634">Event ID: 1120</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-635">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-635">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-636">
<b>MALWAREPROTECTION_THREAT_HASH</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-636">
<b>MALWAREPROTECTION_THREAT_HASH</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-637">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-637">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-638">
<b>Antivirus Microsoft Defender les h biens pour une ressource de menace.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-638">
<b>Microsoft Defender Antivirus has deduced the hashes for a threat resource.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-639">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-639">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-640">Antivirus Microsoft Defender client est opérationnel dans un état sain.</span><span class="sxs-lookup"><span data-stu-id="0096a-640">Microsoft Defender Antivirus client is up and running in a healthy state.</span></span>
<dl><span data-ttu-id="0096a-641">
<dt>Version actuelle de la plateforme : &lt; Chemin d’accès actuel de la &gt; ressource</dt>de la version de la plateforme contre les menaces
<dt> &lt; : &gt; </dt>
<dt>hèses de chemin d’accès : &lt; hchéths &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-641">
<dt>Current Platform Version: &lt;Current platform version&gt;</dt>
<dt>Threat Resource Path: &lt;Path&gt;</dt>
<dt>Hashes: &lt;Hashes&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<td></td>
<td >
<div class="alert"><span data-ttu-id="0096a-642"><b>Remarque : cet événement sera enregistré uniquement si la stratégie suivante est définie : <b>ThreatFileHashLogging non signé.</b></span><span class="sxs-lookup"><span data-stu-id="0096a-642"><b>Note: This event will only be logged if the following policy is set: <b>ThreatFileHashLogging     unsigned</b>.</span></span></div>
<div> </div>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-643">ID d’événement : 1150</span><span class="sxs-lookup"><span data-stu-id="0096a-643">Event ID: 1150</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-644">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-644">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-645">
<b>MALWAREPROTECTION_SERVICE_HEALTHY</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-645">
<b>MALWAREPROTECTION_SERVICE_HEALTHY</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-646">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-646">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-647">
<b>Si votre plateforme anti-programme malveillant signale l’état à une plateforme de surveillance, cet événement indique que la plateforme anti-programme malveillant est en cours d’exécution et dans un état sain. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-647">
<b>If your antimalware platform reports status to a monitoring platform, this event indicates that the antimalware platform is running and in a healthy state. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-648">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-648">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-649">Antivirus Microsoft Defender client est opérationnel dans un état sain.</span><span class="sxs-lookup"><span data-stu-id="0096a-649">Microsoft Defender Antivirus client is up and running in a healthy state.</span></span>
<dl><span data-ttu-id="0096a-650">
<dt>Version de la plateforme : &lt; Version actuelle &gt; de la signature</dt>de la version de la plateforme
<dt>: &lt; &gt; version</dt>de définition
<dt>du moteur : Antimalware Engine &lt; version &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-650">
<dt>Platform Version: &lt;Current platform version&gt;</dt>
<dt>Signature Version: &lt;Definition version&gt;</dt>
<dt>Engine Version: &lt;Antimalware Engine version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-651">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-651">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-652">Aucune action n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0096a-652">No action is necessary.</span></span> <span data-ttu-id="0096a-653">Le Antivirus Microsoft Defender client est dans un état sain.</span><span class="sxs-lookup"><span data-stu-id="0096a-653">The Microsoft Defender Antivirus client is in a healthy state.</span></span> <span data-ttu-id="0096a-654">Cet événement est signalé toutes les heures.</span><span class="sxs-lookup"><span data-stu-id="0096a-654">This event is reported on an hourly basis.</span></span>
</td>
</tr>

<tr>
<th colspan="2"><span data-ttu-id="0096a-655">ID d’événement : 1151</span><span class="sxs-lookup"><span data-stu-id="0096a-655">Event ID: 1151</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-656">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-656">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-657">
<b>MALWAREPROTECTION_SERVICE_HEALTH_REPORT</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-657">
<b>MALWAREPROTECTION_SERVICE_HEALTH_REPORT</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-658">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-658">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-659">
<b>Endpoint Protection d’état du client (heure UTC)</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-659">
<b>Endpoint Protection client health report (time in UTC) </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-660">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-660">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-661">Rapport d’état du client antivirus.</span><span class="sxs-lookup"><span data-stu-id="0096a-661">Antivirus client health report.</span></span>
<dl><span data-ttu-id="0096a-662">
<dt>Version de la plateforme : &lt; &gt;</dt>Version actuelle du moteur de la plateforme : version
<dt> &lt; Antimalware Engine &gt; </dt>
<dt>version &lt; &gt; </dt>du moteur d’inspection en temps réel du réseau : version antivirus du moteur d’inspection du réseau : version de signature
<dt> &lt; &gt; antivirus</dt>version
<dt> &lt; Antispyware &gt; signature version</dt>: version de signature d’inspection réseau en temps réel : état RTP de la
<dt> &lt; signature &gt; </dt>d’inspection du réseau : état de protection en temps réel (activé ou
<dt> &lt; &gt; désactivé)</dt>OA : État d’accès (activé ou
<dt> &lt; &gt; désactivé)</dt>IOAV : IE Téléchargements et Outlook État des pièces
<dt> &lt; jointes rapides &gt; (activé</dt>ou désactivé) BM : état de surveillance du comportement (activé ou
<dt> &lt; &gt; désactivé)</dt>âge de signature antivirus : âge de signature antivirus
<dt> &lt; &gt; (en jours)</dt>Âge de signature antispyware : âge de
<dt>signature &lt; antispyware &gt; (en jours)</dt>Âge de la dernière analyse rapide : Dernière analyse rapide
<dt> &lt; &gt; (en jours)</dt>Âge de la dernière analyse complète : Âge de la dernière analyse complète
<dt> &lt; &gt; (en jours)</dt>Heure de création de la signature antivirus :
<dt>? &lt; Heure de &gt; création de la signature</dt>antivirus Heure de création de
<dt>la signature Antispyware : ? &lt; Heure de création de &gt; signature antispyware Heure</dt>de la dernière
<dt>analyse rapide : ? &lt; Heure de début &gt; de la dernière analyse rapide</dt>Heure de fin de
<dt>l’analyse rapide : ? &lt; &gt;</dt>Heure de fin de la dernière analyse rapide Dernière source d’analyse rapide : Dernière source d’analyse rapide (0 = l’analyse&#39;pas été exécuté, 1 = initié par l’utilisateur, 2 = initié par le
<dt> &lt; &gt; système)</dt>Heure de début de la dernière analyse complète :
<dt>? &lt; Heure de début &gt; de la dernière analyse complète</dt>Heure de fin de
<dt>l’analyse complète : ? &lt; &gt;</dt>Dernière heure de fin de l’analyse complète Dernière source d’analyse complète : Dernière source d’analyse complète (0 = l’analyse&#39;pas été exécuté, 1 = initié par l’utilisateur, 2 = initié par le
<dt> &lt; &gt; système)</dt>État du produit : pour le dépannage interne 
<dt></span><span class="sxs-lookup"><span data-stu-id="0096a-662">
<dt>Platform Version: &lt;Current platform version&gt;</dt>
<dt>Engine Version: &lt;Antimalware Engine version&gt;</dt>
<dt>Network Realtime Inspection engine version: &lt;Network Realtime Inspection engine version&gt;</dt>
<dt>Antivirus signature version: &lt;Antivirus signature version&gt;</dt>
<dt>Antispyware signature version: &lt;Antispyware signature version&gt;</dt>
<dt>Network Realtime Inspection signature version: &lt;Network Realtime Inspection signature version&gt;</dt>
<dt>RTP state: &lt;Realtime protection state&gt; (Enabled or Disabled)</dt>
<dt>OA state: &lt;On Access state&gt; (Enabled or Disabled)</dt>
<dt>IOAV state: &lt;IE Downloads and Outlook Express Attachments state&gt; (Enabled or Disabled)</dt>
<dt>BM state: &lt;Behavior Monitoring state&gt; (Enabled or Disabled)</dt>
<dt>Antivirus signature age: &lt;Antivirus signature age&gt; (in days)</dt>
<dt>Antispyware signature age: &lt;Antispyware signature age&gt; (in days)</dt>
<dt>Last quick scan age: &lt;Last quick scan age&gt; (in days)</dt>
<dt>Last full scan age: &lt;Last full scan age&gt; (in days)</dt>
<dt>Antivirus signature creation time: ?&lt;Antivirus signature creation time&gt;</dt>
<dt>Antispyware signature creation time: ?&lt;Antispyware signature creation time&gt;</dt>
<dt>Last quick scan start time: ?&lt;Last quick scan start time&gt;</dt>
<dt>Last quick scan end time: ?&lt;Last quick scan end time&gt;</dt>
<dt>Last quick scan source: &lt;Last quick scan source&gt; (0 = scan didn&#39;t run, 1 = user initiated, 2 = system initiated)</dt>
<dt>Last full scan start time: ?&lt;Last full scan start time&gt;</dt>
<dt>Last full scan end time: ?&lt;Last full scan end time&gt;</dt>
<dt>Last full scan source: &lt;Last full scan source&gt; (0 = scan didn&#39;t run, 1 = user initiated, 2 = system initiated)</dt>
<dt>Product status: For internal troubleshooting</span></span>
</dl>
</td>
</tr>

<tr><span data-ttu-id="0096a-663">
<th colspan="2">ID d’événement : 2000</span><span class="sxs-lookup"><span data-stu-id="0096a-663">
<th colspan="2">Event ID: 2000</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-664">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-664">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-665">
<b>MALWAREPROTECTION_SIGNATURE_UPDATED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-665">
<b>MALWAREPROTECTION_SIGNATURE_UPDATED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-666">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-666">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-667">
<b>Les définitions du logiciel anti-programme malveillant ont été correctement mises à jour. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-667">
<b>The antimalware definitions updated successfully. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-668">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-668">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-669">La version de signature antivirus a été mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0096a-669">Antivirus signature version has been updated.</span></span>
<dl><span data-ttu-id="0096a-670">
<dt>Version actuelle de la signature : &lt; Version actuelle &gt; de la signature</dt>Version précédente de la signature : type de
<dt>signature &lt; &gt; version précédente</dt>: type de 
<dt> &lt; &gt; signature, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-670">
<dt>Current Signature Version: &lt;Current signature version&gt;</dt>
<dt>Previous Signature Version: &lt;Previous signature version&gt;</dt>
<dt>Signature Type: &lt;Signature type&gt;, for example:</span></span> <ul>
<li><span data-ttu-id="0096a-671">Antivirus</span><span class="sxs-lookup"><span data-stu-id="0096a-671">Antivirus</span></span></li>
<li><span data-ttu-id="0096a-672">Antispyware</span><span class="sxs-lookup"><span data-stu-id="0096a-672">Antispyware</span></span></li>
<li><span data-ttu-id="0096a-673">Logiciel anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="0096a-673">Antimalware</span></span></li>
<li><span data-ttu-id="0096a-674">Système d’inspection du réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-674">Network Inspection System</span></span></li>
</ul><span data-ttu-id="0096a-675">
</dt>
<dt>Type de mise à jour : &lt; Type de &gt; mise à jour , complet ou delta.</dt> 
<dt>Utilisateur : &lt; Domain &gt; \& lt; User &gt; </dt>
<dt>Current Engine Version: &lt; Current engine version &gt; </dt>Previous Engine
<dt>Version: Previous engine &lt; version &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-675">
</dt>
<dt>Update Type: &lt;Update type&gt;, either Full or Delta.</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Current Engine Version: &lt;Current engine version&gt;</dt>
<dt>Previous Engine Version: &lt;Previous engine version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-676">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-676">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-677">Aucune action n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0096a-677">No action is necessary.</span></span> <span data-ttu-id="0096a-678">Le Antivirus Microsoft Defender client est dans un état sain.</span><span class="sxs-lookup"><span data-stu-id="0096a-678">The Microsoft Defender Antivirus client is in a healthy state.</span></span> <span data-ttu-id="0096a-679">Cet événement est signalé lorsque les signatures sont correctement mises à jour.</span><span class="sxs-lookup"><span data-stu-id="0096a-679">This event is reported when signatures are successfully updated.</span></span>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-680">ID d’événement : 2001</span><span class="sxs-lookup"><span data-stu-id="0096a-680">Event ID: 2001</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-681">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-681">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-682">
<b>MALWAREPROTECTION_SIGNATURE_UPDATE_FAILED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-682">
<b>MALWAREPROTECTION_SIGNATURE_UPDATE_FAILED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-683">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-683">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-684">
<b>Échec de la mise à jour des informations de sécurité. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-684">
<b>The security intelligence update failed. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-685">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-685">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-686">Antivirus Microsoft Defender a rencontré une erreur lors de la tentative de mise à jour des signatures.</span><span class="sxs-lookup"><span data-stu-id="0096a-686">Microsoft Defender Antivirus has encountered an error trying to update signatures.</span></span>
<dl><span data-ttu-id="0096a-687">
<dt>Nouvelle version de l’intelligence de la sécurité : &lt; Nouveau numéro &gt; de version</dt>
<dt>Version précédente de l’intelligence de la sécurité : &lt; Version &gt; précédente</dt>Mise à jour Source : Source de mise à 
<dt> &lt; &gt; jour, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-687">
<dt>New security intelligence version: &lt;New version number&gt;</dt>
<dt>Previous security intelligence version: &lt;Previous version&gt;</dt>
<dt>Update Source: &lt;Update source&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-688">Dossier de mise à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="0096a-688">Security intelligence update folder</span></span></li>
<li><span data-ttu-id="0096a-689">Serveur de mise à jour de l’intelligence de sécurité interne</span><span class="sxs-lookup"><span data-stu-id="0096a-689">Internal security intelligence update server</span></span></li>
<li><span data-ttu-id="0096a-690">Microsoft Update Server</span><span class="sxs-lookup"><span data-stu-id="0096a-690">Microsoft Update Server</span></span></li>
<li><span data-ttu-id="0096a-691">Partage de fichiers</span><span class="sxs-lookup"><span data-stu-id="0096a-691">File share</span></span></li>
<li><span data-ttu-id="0096a-692">Centre de protection Microsoft contre les programmes malveillants (MMPC)</span><span class="sxs-lookup"><span data-stu-id="0096a-692">Microsoft Malware Protection Center (MMPC)</span></span></li>
</ul><span data-ttu-id="0096a-693">
</dt>
<dt>Étape de mise à &lt; jour : étape de mise à &gt; jour, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-693">
</dt>
<dt>Update Stage: &lt;Update stage&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-694">Recherche</span><span class="sxs-lookup"><span data-stu-id="0096a-694">Search</span></span></li>
<li><span data-ttu-id="0096a-695">Télécharger</span><span class="sxs-lookup"><span data-stu-id="0096a-695">Download</span></span></li>
<li><span data-ttu-id="0096a-696">Installer</span><span class="sxs-lookup"><span data-stu-id="0096a-696">Install</span></span></li>
</ul><span data-ttu-id="0096a-697">
</dt>Chemin d’accès source : nom de partage de fichiers pour la convention d’attribution de noms universelle (UNC), nom de serveur 
<dt>pour Windows Server Update Services (WSUS)/Microsoft Update/ADL.</dt> 
<dt> Type de signature &lt; : type &gt; de signature, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-697">
</dt>
<dt>Source Path: File share name for Universal Naming Convention (UNC), server name for Windows Server Update Services (WSUS)/Microsoft Update/ADL.</dt>
<dt>Signature Type: &lt;Signature type&gt;, for example:</span></span> <ul>
<li><span data-ttu-id="0096a-698">Antivirus</span><span class="sxs-lookup"><span data-stu-id="0096a-698">Antivirus</span></span></li>
<li><span data-ttu-id="0096a-699">Antispyware</span><span class="sxs-lookup"><span data-stu-id="0096a-699">Antispyware</span></span></li>
<li><span data-ttu-id="0096a-700">Logiciel anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="0096a-700">Antimalware</span></span></li>
<li><span data-ttu-id="0096a-701">Système d’inspection du réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-701">Network Inspection System</span></span></li>
</ul><span data-ttu-id="0096a-702">
</dt>
<dt>Type de mise à jour : &lt; Type de &gt; mise à jour , complet ou delta.</dt> 
<dt>Utilisateur : &lt; Domain &gt; \& lt; Version &gt; du</dt>moteur actuel de l’utilisateur :
<dt> &lt; &gt; version</dt>actuelle du moteur Version précédente du moteur : Code d’erreur
<dt>de la &lt; version &gt; </dt>précédente du moteur : code de résultat du code d’erreur associé
<dt>à &lt; &gt; l’état de la menace. Valeurs HRESULT standard.</dt> 
<dt>Description de l’erreur : &lt; Description de &gt; l’erreur.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-702">
</dt>
<dt>Update Type: &lt;Update type&gt;, either Full or Delta.</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Current Engine Version: &lt;Current engine version&gt;</dt>
<dt>Previous Engine Version: &lt;Previous engine version&gt;</dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values.</dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-703">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-703">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-704">Cette erreur se produit en cas de problème de mise à jour des définitions.</span><span class="sxs-lookup"><span data-stu-id="0096a-704">This error occurs when there is a problem updating definitions.</span></span>
<span data-ttu-id="0096a-705">Pour résoudre les problèmes de cet événement :</span><span class="sxs-lookup"><span data-stu-id="0096a-705">To troubleshoot this event:</span></span>
<ol>
<li><span data-ttu-id="0096a-706"><a href="manage-updates-baselines-microsoft-defender-antivirus.md" data-raw-source="[Update definitions](manage-updates-baselines-microsoft-defender-antivirus.md)">Mettez à jour les définitions</a> et forcez un rescan directement sur le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0096a-706"><a href="manage-updates-baselines-microsoft-defender-antivirus.md" data-raw-source="[Update definitions](manage-updates-baselines-microsoft-defender-antivirus.md)">Update definitions</a> and force a rescan directly on the endpoint.</span></span></li>
<li><span data-ttu-id="0096a-707">Examinez les entrées dans le fichier %Windir%\WindowsUpdate.log pour plus d’informations sur cette erreur.</span><span class="sxs-lookup"><span data-stu-id="0096a-707">Review the entries in the %Windir%\WindowsUpdate.log file for more information about this error.</span></span></li>
<li><span data-ttu-id="0096a-708">Contactez le <a href="https://go.microsoft.com/fwlink/?LinkId=215491">Support technique Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="0096a-708">Contact <a href="https://go.microsoft.com/fwlink/?LinkId=215491">Microsoft Technical Support</a>.</span></span>
</li>
</ol>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-709">ID d’événement : 2002</span><span class="sxs-lookup"><span data-stu-id="0096a-709">Event ID: 2002</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-710">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-710">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-711">
<b>MALWAREPROTECTION_ENGINE_UPDATED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-711">
<b>MALWAREPROTECTION_ENGINE_UPDATED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-712">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-712">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-713">
<b>Le moteur du logiciel anti-programme malveillant a été mis à jour avec succès. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-713">
<b>The antimalware engine updated successfully. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-714">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-714">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-715">Antivirus Microsoft Defender version du moteur a été mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0096a-715">Microsoft Defender Antivirus engine version has been updated.</span></span>
<dl><span data-ttu-id="0096a-716">
<dt>Version actuelle du moteur : &lt; Version actuelle &gt; du moteur</dt>Version précédente du moteur : Type de moteur
<dt> &lt; version &gt; </dt>précédente : type de moteur , moteur anti-programme malveillant ou moteur système d’inspection
<dt>du &lt; &gt; réseau.</dt> 
<dt>Utilisateur : &lt; Domain &gt; \& lt; Utilisateur &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-716">
<dt>Current Engine Version: &lt;Current engine version&gt;</dt>
<dt>Previous Engine Version: &lt;Previous engine version&gt;</dt>
<dt>Engine Type: &lt;Engine type&gt;, either antimalware engine or Network Inspection System engine.</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-717">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-717">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-718">Aucune action n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0096a-718">No action is necessary.</span></span> <span data-ttu-id="0096a-719">Le Antivirus Microsoft Defender client est dans un état sain.</span><span class="sxs-lookup"><span data-stu-id="0096a-719">The Microsoft Defender Antivirus client is in a healthy state.</span></span> <span data-ttu-id="0096a-720">Cet événement est signalé lorsque le moteur du logiciel anti-programme malveillant est correctement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="0096a-720">This event is reported when the antimalware engine is successfully updated.</span></span>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-721">ID d’événement : 2003</span><span class="sxs-lookup"><span data-stu-id="0096a-721">Event ID: 2003</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-722">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-722">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-723">
<b>MALWAREPROTECTION_ENGINE_UPDATE_FAILED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-723">
<b>MALWAREPROTECTION_ENGINE_UPDATE_FAILED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-724">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-724">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-725">
<b>Échec de la mise à jour du moteur du logiciel anti-programme malveillant. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-725">
<b>The antimalware engine update failed. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-726">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-726">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-727">Antivirus Microsoft Defender a rencontré une erreur lors de la tentative de mise à jour du moteur.</span><span class="sxs-lookup"><span data-stu-id="0096a-727">Microsoft Defender Antivirus has encountered an error trying to update the engine.</span></span>
<dl><span data-ttu-id="0096a-728">
<dt>Nouvelle version du moteur :</dt>version précédente du moteur : type de moteur
<dt> &lt; version &gt; </dt>précédente : type de moteur , moteur anti-programme malveillant ou moteur système d’inspection
<dt>du &lt; &gt; réseau.</dt> 
<dt>Utilisateur : &lt; Domain &gt; \& lt; Code &gt; </dt>
<dt>d’erreur utilisateur &lt; : code de résultat du code &gt; d’erreur associé à l’état de la menace. Valeurs HRESULT standard.</dt> 
<dt>Description de l’erreur : &lt; Description de &gt; l’erreur.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-728">
<dt>New Engine Version:</dt>
<dt>Previous Engine Version: &lt;Previous engine version&gt;</dt>
<dt>Engine Type: &lt;Engine type&gt;, either antimalware engine or Network Inspection System engine.</dt>
<dt>User: &lt;Domain&gt;\&lt;User&gt;</dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values.</dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-729">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-729">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-730">La mise à Antivirus Microsoft Defender client a échoué.</span><span class="sxs-lookup"><span data-stu-id="0096a-730">The Microsoft Defender Antivirus client update failed.</span></span> <span data-ttu-id="0096a-731">Cet événement se produit lorsque le client ne parvient pas à se mettre à jour lui-même.</span><span class="sxs-lookup"><span data-stu-id="0096a-731">This event occurs when the client fails to update itself.</span></span> <span data-ttu-id="0096a-732">Cet événement est généralement dû à une interruption de la connectivité réseau pendant une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0096a-732">This event is usually due to an interruption in network connectivity during an update.</span></span>
<span data-ttu-id="0096a-733">Pour résoudre les problèmes de cet événement :</span><span class="sxs-lookup"><span data-stu-id="0096a-733">To troubleshoot this event:</span></span>
<ol>
<li><span data-ttu-id="0096a-734"><a href="manage-updates-baselines-microsoft-defender-antivirus.md" data-raw-source="[Update definitions](manage-updates-baselines-microsoft-defender-antivirus.md)">Mettez à jour les définitions</a> et forcez un rescan directement sur le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0096a-734"><a href="manage-updates-baselines-microsoft-defender-antivirus.md" data-raw-source="[Update definitions](manage-updates-baselines-microsoft-defender-antivirus.md)">Update definitions</a> and force a rescan directly on the endpoint.</span></span></li>
<li><span data-ttu-id="0096a-735">Contactez le <a href="https://go.microsoft.com/fwlink/?LinkId=215491">Support technique Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="0096a-735">Contact <a href="https://go.microsoft.com/fwlink/?LinkId=215491">Microsoft Technical Support</a>.</span></span>
</li>
</ol>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-736">ID d’événement : 2004</span><span class="sxs-lookup"><span data-stu-id="0096a-736">Event ID: 2004</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-737">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-737">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-738">
<b>MALWAREPROTECTION_SIGNATURE_REVERSION</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-738">
<b>MALWAREPROTECTION_SIGNATURE_REVERSION</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-739">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-739">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-740">
<b>Un problème est à l’lors du chargement des définitions de logiciels anti-programme malveillant. Le moteur du logiciel anti-programme malveillant tentera de charger le dernier ensemble connu de définitions.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-740">
<b>There was a problem loading antimalware definitions. The antimalware engine will attempt to load the last-known good set of definitions.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-741">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-741">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-742">Antivirus Microsoft Defender a rencontré une erreur lors de la tentative de chargement des signatures et tente de revenir à un ensemble connu de signatures.</span><span class="sxs-lookup"><span data-stu-id="0096a-742">Microsoft Defender Antivirus has encountered an error trying to load signatures and will attempt reverting back to a known-good set of signatures.</span></span>
<dl><span data-ttu-id="0096a-743">
<dt>Signatures tentées : Code</dt>
<dt>d’erreur : &lt; code de résultat du code &gt; d’erreur associé à l’état de la menace. Valeurs HRESULT standard.</dt> 
<dt>Description de l’erreur : &lt; Description de &gt; l’erreur.</dt> 
<dt>Version de la signature : &lt; Version &gt; du moteur de définition</dt>: version du moteur
<dt> &lt; anti-programme malveillant &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-743">
<dt>Signatures Attempted:</dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values.</dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
<dt>Signature Version: &lt;Definition version&gt;</dt>
<dt>Engine Version: &lt;Antimalware engine version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-744">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-744">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-745">Le Antivirus Microsoft Defender a tenté de télécharger et d’installer le fichier de définitions le plus récent et a échoué.</span><span class="sxs-lookup"><span data-stu-id="0096a-745">The Microsoft Defender Antivirus client attempted to download and install the latest definitions file and failed.</span></span> <span data-ttu-id="0096a-746">Cette erreur peut se produire lorsque le client rencontre une erreur lors de la tentative de chargement des définitions, ou si le fichier est endommagé.</span><span class="sxs-lookup"><span data-stu-id="0096a-746">This error can occur when the client encounters an error while trying to load the definitions, or if the file is corrupt.</span></span> <span data-ttu-id="0096a-747">Antivirus Microsoft Defender tenteront de revenir à un ensemble de définitions connu.</span><span class="sxs-lookup"><span data-stu-id="0096a-747">Microsoft Defender Antivirus will attempt to revert back to a known-good set of definitions.</span></span>
<span data-ttu-id="0096a-748">Pour résoudre les problèmes de cet événement :</span><span class="sxs-lookup"><span data-stu-id="0096a-748">To troubleshoot this event:</span></span>
<ol>
<li><span data-ttu-id="0096a-749">Redémarrez l’ordinateur et réessayez.</span><span class="sxs-lookup"><span data-stu-id="0096a-749">Restart the computer and try again.</span></span></li>
<li><span data-ttu-id="0096a-750">Téléchargez les dernières définitions à partir <a href="https://aka.ms/wdsi">du site Renseignement de sécurité Microsoft.</a></span><span class="sxs-lookup"><span data-stu-id="0096a-750">Download the latest definitions from the <a href="https://aka.ms/wdsi">Microsoft Security Intelligence site</a>.</span></span>
<span data-ttu-id="0096a-751">Remarque : la taille du fichier de définitions téléchargé à partir du site peut dépasser 60 Mo et ne doit pas être utilisée comme solution à long terme pour la mise à jour des définitions.</span><span class="sxs-lookup"><span data-stu-id="0096a-751">Note: The size of the definitions file downloaded from the site can exceed 60 MB and should not be used as a long-term solution for updating definitions.</span></span>
</li>
<li><span data-ttu-id="0096a-752">Contactez le <a href="https://go.microsoft.com/fwlink/?LinkId=215491">Support technique Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="0096a-752">Contact <a href="https://go.microsoft.com/fwlink/?LinkId=215491">Microsoft Technical Support</a>.</span></span>
</li>
</ol>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-753">ID d’événement : 2005</span><span class="sxs-lookup"><span data-stu-id="0096a-753">Event ID: 2005</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-754">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-754">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-755">
<b>MALWAREPROTECTION_ENGINE_UPDATE_PLATFORMOUTOFDATE</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-755">
<b>MALWAREPROTECTION_ENGINE_UPDATE_PLATFORMOUTOFDATE</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-756">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-756">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-757">
<b>Le moteur du logiciel anti-programme malveillant n’a pas réussi à se charger car la plateforme anti-programme malveillant est hors de la date. La plateforme anti-programme malveillant charge le dernier moteur anti-programme malveillant connu et tente de la mettre à jour.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-757">
<b>The antimalware engine failed to load because the antimalware platform is out of date. The antimalware platform will load the last-known good antimalware engine and attempt to update.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-758">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-758">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-759">Antivirus Microsoft Defender n’a pas pu charger le moteur du logiciel anti-programme malveillant, car la version actuelle de la plateforme n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0096a-759">Microsoft Defender Antivirus could not load antimalware engine because current platform version is not supported.</span></span> <span data-ttu-id="0096a-760">Antivirus Microsoft Defender revenir au dernier moteur connu et une tentative de mise à jour de plateforme sera tentée.</span><span class="sxs-lookup"><span data-stu-id="0096a-760">Microsoft Defender Antivirus will revert back to the last known-good engine and a platform update will be attempted.</span></span>
<dl><span data-ttu-id="0096a-761">
<dt>Version actuelle de la plateforme : &lt; version actuelle de la plateforme&gt;</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-761">
<dt>Current Platform Version: &lt;Current platform version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-762">ID d’événement : 2006</span><span class="sxs-lookup"><span data-stu-id="0096a-762">Event ID: 2006</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-763">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-763">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-764">
<b>MALWAREPROTECTION_PLATFORM_UPDATE_FAILED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-764">
<b>MALWAREPROTECTION_PLATFORM_UPDATE_FAILED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-765">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-765">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-766">
<b>Échec de la mise à jour de la plateforme. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-766">
<b>The platform update failed. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-767">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-767">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-768">Antivirus Microsoft Defender a rencontré une erreur lors de la tentative de mise à jour de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="0096a-768">Microsoft Defender Antivirus has encountered an error trying to update the platform.</span></span>
<dl><span data-ttu-id="0096a-769">
<dt>Version actuelle de la plateforme : &lt; Code d’erreur de la version actuelle &gt; </dt>de la plateforme : code de résultat du code
<dt> &lt; &gt; d’erreur associé à l’état de la menace. Valeurs HRESULT standard.</dt> 
<dt>Description de l’erreur : &lt; Description de &gt; l’erreur.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-769">
<dt>Current Platform Version: &lt;Current platform version&gt;</dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values.</dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-770">ID d’événement : 2007</span><span class="sxs-lookup"><span data-stu-id="0096a-770">Event ID: 2007</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-771">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-771">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-772">
<b>MALWAREPROTECTION_PLATFORM_ALMOSTOUTOFDATE</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-772">
<b>MALWAREPROTECTION_PLATFORM_ALMOSTOUTOFDATE</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-773">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-773">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-774">
<b>La plateforme sera bientôt à jour. Téléchargez la dernière plateforme pour maintenir une protection à jour.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-774">
<b>The platform will soon be out of date. Download the latest platform to maintain up-to-date protection.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-775">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-775">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-776">Antivirus Microsoft Defender nécessitera bientôt une version plus récente de la plateforme pour prendre en charge les futures versions du moteur anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="0096a-776">Microsoft Defender Antivirus will soon require a newer platform version to support future versions of the antimalware engine.</span></span> <span data-ttu-id="0096a-777">Téléchargez la dernière plateforme Antivirus Microsoft Defender pour maintenir le meilleur niveau de protection disponible.</span><span class="sxs-lookup"><span data-stu-id="0096a-777">Download the latest Microsoft Defender Antivirus platform to maintain the best level of protection available.</span></span>
<dl><span data-ttu-id="0096a-778">
<dt>Version actuelle de la plateforme : &lt; version actuelle de la plateforme&gt;</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-778">
<dt>Current Platform Version: &lt;Current platform version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-779">ID d’événement : 2010</span><span class="sxs-lookup"><span data-stu-id="0096a-779">Event ID: 2010</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-780">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-780">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-781">
<b>MALWAREPROTECTION_SIGNATURE_FASTPATH_UPDATED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-781">
<b>MALWAREPROTECTION_SIGNATURE_FASTPATH_UPDATED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-782">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-782">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-783">
<b>Le moteur du logiciel anti-programme malveillant a utilisé le service signature dynamique pour obtenir des définitions supplémentaires. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-783">
<b>The antimalware engine used the Dynamic Signature Service to get additional definitions. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-784">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-784">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-785">Antivirus Microsoft Defender service <i>signature dynamique pour récupérer</i> des signatures supplémentaires afin de protéger votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0096a-785">Microsoft Defender Antivirus used <i>Dynamic Signature Service</i> to retrieve additional signatures to help protect your machine.</span></span>
<dl><span data-ttu-id="0096a-786">
<dt>Version actuelle de la signature : &lt; Type de &gt; signature de la version</dt>actuelle de la signature : type de 
<dt> &lt; &gt; signature, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-786">
<dt>Current Signature Version: &lt;Current signature version&gt;</dt>
<dt>Signature Type: &lt;Signature type&gt;, for example:</span></span> <ul>
<li><span data-ttu-id="0096a-787">Antivirus</span><span class="sxs-lookup"><span data-stu-id="0096a-787">Antivirus</span></span></li>
<li><span data-ttu-id="0096a-788">Antispyware</span><span class="sxs-lookup"><span data-stu-id="0096a-788">Antispyware</span></span></li>
<li><span data-ttu-id="0096a-789">Logiciel anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="0096a-789">Antimalware</span></span></li>
<li><span data-ttu-id="0096a-790">Système d’inspection du réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-790">Network Inspection System</span></span></li>
</ul><span data-ttu-id="0096a-791">
</dt>
<dt>Version actuelle du moteur : &lt; Type de &gt; signature</dt>dynamique de la version actuelle du moteur 
<dt> : type de signature &lt; &gt; dynamique, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-791">
</dt>
<dt>Current Engine Version: &lt;Current engine version&gt;</dt>
<dt>Dynamic Signature Type: &lt;Dynamic signature type&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-792">Version</span><span class="sxs-lookup"><span data-stu-id="0096a-792">Version</span></span></li>
<li><span data-ttu-id="0096a-793">Timestamp</span><span class="sxs-lookup"><span data-stu-id="0096a-793">Timestamp</span></span></li>
<li><span data-ttu-id="0096a-794">Sans limite</span><span class="sxs-lookup"><span data-stu-id="0096a-794">No limit</span></span></li>
<li><span data-ttu-id="0096a-795">Duration</span><span class="sxs-lookup"><span data-stu-id="0096a-795">Duration</span></span></li>
</ul><span data-ttu-id="0096a-796">
</dt>
<dt>Chemin d’accès de persistance : &lt; Version &gt; </dt>de signature dynamique du chemin d’accès : timestamp de compilation de signature dynamique de numéro de
<dt> &lt; version &gt; </dt>: Type limite de persistance d’timestamp
<dt> &lt; &gt; </dt>: type de limite 
<dt> de &lt; &gt; persistance, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-796">
</dt>
<dt>Persistence Path: &lt;Path&gt;</dt>
<dt>Dynamic Signature Version: &lt;Version number&gt;</dt>
<dt>Dynamic Signature Compilation Timestamp: &lt;Timestamp&gt;</dt>
<dt>Persistence Limit Type: &lt;Persistence limit type&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-797">Version VDM</span><span class="sxs-lookup"><span data-stu-id="0096a-797">VDM version</span></span></li>
<li><span data-ttu-id="0096a-798">Timestamp</span><span class="sxs-lookup"><span data-stu-id="0096a-798">Timestamp</span></span></li>
<li><span data-ttu-id="0096a-799">Sans limite</span><span class="sxs-lookup"><span data-stu-id="0096a-799">No limit</span></span></li>
</ul><span data-ttu-id="0096a-800">
</dt>
<dt>Limite de persistance : limite de persistance de la signature fastpath.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-800">
</dt>
<dt>Persistence Limit: Persistence limit of the fastpath signature.</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-801">ID d'événement : 2011</span><span class="sxs-lookup"><span data-stu-id="0096a-801">Event ID: 2011</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-802">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-802">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-803">
<b>MALWAREPROTECTION_SIGNATURE_FASTPATH_DELETED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-803">
<b>MALWAREPROTECTION_SIGNATURE_FASTPATH_DELETED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-804">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-804">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-805">
<b>Le service signature dynamique a supprimé les définitions dynamiques hors date. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-805">
<b>The Dynamic Signature Service deleted the out-of-date dynamic definitions. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-806">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-806">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-807">Antivirus Microsoft Defender service <i>signature dynamique pour</i> ignorer les signatures obsolètes.</span><span class="sxs-lookup"><span data-stu-id="0096a-807">Microsoft Defender Antivirus used <i>Dynamic Signature Service</i> to discard obsolete signatures.</span></span>
<dl><span data-ttu-id="0096a-808">
<dt>Version actuelle de la signature : &lt; Type de &gt; signature de la version</dt>actuelle de la signature : type de 
<dt> &lt; &gt; signature, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-808">
<dt>Current Signature Version: &lt;Current signature version&gt;</dt>
<dt>Signature Type: &lt;Signature type&gt;, for example:</span></span> <ul>
<li><span data-ttu-id="0096a-809">Antivirus</span><span class="sxs-lookup"><span data-stu-id="0096a-809">Antivirus</span></span></li>
<li><span data-ttu-id="0096a-810">Antispyware</span><span class="sxs-lookup"><span data-stu-id="0096a-810">Antispyware</span></span></li>
<li><span data-ttu-id="0096a-811">Logiciel anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="0096a-811">Antimalware</span></span></li>
<li><span data-ttu-id="0096a-812">Système d’inspection du réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-812">Network Inspection System</span></span></li>
</ul><span data-ttu-id="0096a-813">
</dt>
<dt>Version actuelle du moteur : &lt; Type de &gt; signature</dt>dynamique de la version actuelle du moteur 
<dt> : type de signature &lt; &gt; dynamique, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-813">
</dt>
<dt>Current Engine Version: &lt;Current engine version&gt;</dt>
<dt>Dynamic Signature Type: &lt;Dynamic signature type&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-814">Version</span><span class="sxs-lookup"><span data-stu-id="0096a-814">Version</span></span></li>
<li><span data-ttu-id="0096a-815">Timestamp</span><span class="sxs-lookup"><span data-stu-id="0096a-815">Timestamp</span></span></li>
<li><span data-ttu-id="0096a-816">Sans limite</span><span class="sxs-lookup"><span data-stu-id="0096a-816">No limit</span></span></li>
<li><span data-ttu-id="0096a-817">Duration</span><span class="sxs-lookup"><span data-stu-id="0096a-817">Duration</span></span></li>
</ul><span data-ttu-id="0096a-818">
</dt>
<dt>Chemin d’accès de persistance : &lt; Version &gt; </dt>de signature dynamique du chemin d’accès : timestamp de compilation de signature dynamique de numéro de
<dt> &lt; version &gt; </dt>: Motif de suppression de l’timestamp
<dt> &lt; &gt; </dt>: Type de limite de persistance : type de limite de
<dt></dt> 
<dt> &lt; &gt; persistance, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-818">
</dt>
<dt>Persistence Path: &lt;Path&gt;</dt>
<dt>Dynamic Signature Version: &lt;Version number&gt;</dt>
<dt>Dynamic Signature Compilation Timestamp: &lt;Timestamp&gt;</dt>
<dt>Removal Reason:</dt>
<dt>Persistence Limit Type: &lt;Persistence limit type&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-819">Version VDM</span><span class="sxs-lookup"><span data-stu-id="0096a-819">VDM version</span></span></li>
<li><span data-ttu-id="0096a-820">Timestamp</span><span class="sxs-lookup"><span data-stu-id="0096a-820">Timestamp</span></span></li>
<li><span data-ttu-id="0096a-821">Sans limite</span><span class="sxs-lookup"><span data-stu-id="0096a-821">No limit</span></span></li>
</ul><span data-ttu-id="0096a-822">
</dt>
<dt>Limite de persistance : limite de persistance de la signature fastpath.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-822">
</dt>
<dt>Persistence Limit: Persistence limit of the fastpath signature.</dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-823">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-823">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-824">Aucune action n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0096a-824">No action is necessary.</span></span> <span data-ttu-id="0096a-825">Le Antivirus Microsoft Defender client est dans un état sain.</span><span class="sxs-lookup"><span data-stu-id="0096a-825">The Microsoft Defender Antivirus client is in a healthy state.</span></span> <span data-ttu-id="0096a-826">Cet événement est signalé lorsque le service Signature dynamique supprime correctement les définitions dynamiques hors date.</span><span class="sxs-lookup"><span data-stu-id="0096a-826">This event is reported when the Dynamic Signature Service successfully deletes out-of-date dynamic definitions.</span></span>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-827">ID d’événement : 2012</span><span class="sxs-lookup"><span data-stu-id="0096a-827">Event ID: 2012</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-828">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-828">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-829">
<b>MALWAREPROTECTION_SIGNATURE_FASTPATH_UPDATE_FAILED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-829">
<b>MALWAREPROTECTION_SIGNATURE_FASTPATH_UPDATE_FAILED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-830">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-830">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-831">
<b>Le moteur du logiciel anti-programme malveillant a rencontré une erreur lors de la tentative d’utilisation du service signature dynamique. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-831">
<b>The antimalware engine encountered an error when trying to use the Dynamic Signature Service. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-832">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-832">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-833">Antivirus Microsoft Defender a rencontré une erreur lors de la tentative d’utilisation <i>du service signature dynamique.</i></span><span class="sxs-lookup"><span data-stu-id="0096a-833">Microsoft Defender Antivirus has encountered an error trying to use <i>Dynamic Signature Service</i>.</span></span>
<dl><span data-ttu-id="0096a-834">
<dt>Version actuelle de la signature : &lt; Type de &gt; signature de la version</dt>actuelle de la signature : type de 
<dt> &lt; &gt; signature, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-834">
<dt>Current Signature Version: &lt;Current signature version&gt;</dt>
<dt>Signature Type: &lt;Signature type&gt;, for example:</span></span> <ul>
<li><span data-ttu-id="0096a-835">Antivirus</span><span class="sxs-lookup"><span data-stu-id="0096a-835">Antivirus</span></span></li>
<li><span data-ttu-id="0096a-836">Antispyware</span><span class="sxs-lookup"><span data-stu-id="0096a-836">Antispyware</span></span></li>
<li><span data-ttu-id="0096a-837">Logiciel anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="0096a-837">Antimalware</span></span></li>
<li><span data-ttu-id="0096a-838">Système d’inspection du réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-838">Network Inspection System</span></span></li>
</ul><span data-ttu-id="0096a-839">
</dt>
<dt>Version actuelle du moteur : &lt; Code d’erreur de la version &gt; </dt>actuelle du moteur : code de résultat du code
<dt> &lt; &gt; d’erreur associé à l’état de la menace. Valeurs HRESULT standard.</dt> 
<dt>Description de l’erreur : &lt; Description de &gt; l’erreur.</dt> 
<dt> Type de signature dynamique : &lt; type de signature &gt; dynamique, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-839">
</dt>
<dt>Current Engine Version: &lt;Current engine version&gt;</dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values.</dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
<dt>Dynamic Signature Type: &lt;Dynamic signature type&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-840">Version</span><span class="sxs-lookup"><span data-stu-id="0096a-840">Version</span></span></li>
<li><span data-ttu-id="0096a-841">Timestamp</span><span class="sxs-lookup"><span data-stu-id="0096a-841">Timestamp</span></span></li>
<li><span data-ttu-id="0096a-842">Sans limite</span><span class="sxs-lookup"><span data-stu-id="0096a-842">No limit</span></span></li>
<li><span data-ttu-id="0096a-843">Duration</span><span class="sxs-lookup"><span data-stu-id="0096a-843">Duration</span></span></li>
</ul><span data-ttu-id="0096a-844">
</dt>
<dt>Chemin d’accès de persistance : &lt; Version &gt; </dt>de signature dynamique du chemin d’accès : timestamp de compilation de signature dynamique de numéro de
<dt> &lt; version &gt; </dt>: Type limite de persistance d’timestamp
<dt> &lt; &gt; </dt>: type de limite 
<dt> de &lt; &gt; persistance, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-844">
</dt>
<dt>Persistence Path: &lt;Path&gt;</dt>
<dt>Dynamic Signature Version: &lt;Version number&gt;</dt>
<dt>Dynamic Signature Compilation Timestamp: &lt;Timestamp&gt;</dt>
<dt>Persistence Limit Type: &lt;Persistence limit type&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-845">Version VDM</span><span class="sxs-lookup"><span data-stu-id="0096a-845">VDM version</span></span></li>
<li><span data-ttu-id="0096a-846">Timestamp</span><span class="sxs-lookup"><span data-stu-id="0096a-846">Timestamp</span></span></li>
<li><span data-ttu-id="0096a-847">Sans limite</span><span class="sxs-lookup"><span data-stu-id="0096a-847">No limit</span></span></li>
</ul><span data-ttu-id="0096a-848">
</dt>
<dt>Limite de persistance : limite de persistance de la signature fastpath.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-848">
</dt>
<dt>Persistence Limit: Persistence limit of the fastpath signature.</dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-849">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-849">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-850">Vérifiez vos paramètres de connectivité Internet.</span><span class="sxs-lookup"><span data-stu-id="0096a-850">Check your Internet connectivity settings.</span></span>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-851">ID d’événement : 2013</span><span class="sxs-lookup"><span data-stu-id="0096a-851">Event ID: 2013</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-852">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-852">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-853">
<b>MALWAREPROTECTION_SIGNATURE_FASTPATH_DELETED_ALL </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-853">
<b>MALWAREPROTECTION_SIGNATURE_FASTPATH_DELETED_ALL </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-854">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-854">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-855">
<b>Le service signature dynamique a supprimé toutes les définitions dynamiques. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-855">
<b>The Dynamic Signature Service deleted all dynamic definitions. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-856">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-856">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-857">Antivirus Microsoft Defender toutes les signatures <i>du service signature</i> dynamique.</span><span class="sxs-lookup"><span data-stu-id="0096a-857">Microsoft Defender Antivirus discarded all <i>Dynamic Signature Service</i> signatures.</span></span>
<dl><span data-ttu-id="0096a-858">
<dt>Version actuelle de la signature : &lt; version actuelle de la signature&gt;</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-858">
<dt>Current Signature Version: &lt;Current signature version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-859">ID d’événement : 2020</span><span class="sxs-lookup"><span data-stu-id="0096a-859">Event ID: 2020</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-860">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-860">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-861">
<b>MALWAREPROTECTION_CLOUD_CLEAN_RESTORE_FILE_DOWNLOADED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-861">
<b>MALWAREPROTECTION_CLOUD_CLEAN_RESTORE_FILE_DOWNLOADED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-862">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-862">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-863">
<b>Le moteur du logiciel anti-programme malveillant a téléchargé un fichier propre. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-863">
<b>The antimalware engine downloaded a clean file. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-864">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-864">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-865">Antivirus Microsoft Defender téléchargé un fichier propre.</span><span class="sxs-lookup"><span data-stu-id="0096a-865">Microsoft Defender Antivirus downloaded a clean file.</span></span>
<dl><span data-ttu-id="0096a-866">
<dt>Nom du fichier : &lt; Nom de &gt; fichier du fichier.</dt> 
<dt>Version actuelle de la signature : &lt; Version actuelle &gt; de la signature</dt>
<dt>Version actuelle du moteur : version actuelle du &lt; moteur &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-866">
<dt>Filename: &lt;File name&gt; Name of the file.</dt>
<dt>Current Signature Version: &lt;Current signature version&gt;</dt>
<dt>Current Engine Version: &lt;Current engine version&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-867">ID d’événement : 2021</span><span class="sxs-lookup"><span data-stu-id="0096a-867">Event ID: 2021</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-868">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-868">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-869">
<b>MALWAREPROTECTION_CLOUD_CLEAN_RESTORE_FILE_DOWNLOAD_FAILED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-869">
<b>MALWAREPROTECTION_CLOUD_CLEAN_RESTORE_FILE_DOWNLOAD_FAILED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-870">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-870">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-871">
<b>Le moteur du logiciel anti-programme malveillant n’a pas réussi à télécharger un fichier propre. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-871">
<b>The antimalware engine failed to download a clean file. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-872">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-872">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-873">Antivirus Microsoft Defender a rencontré une erreur lors de la tentative de téléchargement d’un fichier propre.</span><span class="sxs-lookup"><span data-stu-id="0096a-873">Microsoft Defender Antivirus has encountered an error trying to download a clean file.</span></span>
<dl><span data-ttu-id="0096a-874">
<dt>Nom du fichier : &lt; Nom de &gt; fichier du fichier.</dt> 
<dt>Version actuelle de la signature : &lt; Version actuelle &gt; du moteur de la signature</dt>: code d’erreur de la
<dt> &lt; version &gt; </dt>actuelle du moteur : code de résultat du code d’erreur
<dt>associé à &lt; &gt; l’état de la menace. Valeurs HRESULT standard.</dt> 
<dt>Description de l’erreur : &lt; Description de &gt; l’erreur.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-874">
<dt>Filename: &lt;File name&gt; Name of the file.</dt>
<dt>Current Signature Version: &lt;Current signature version&gt;</dt>
<dt>Current Engine Version: &lt;Current engine version&gt;</dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values.</dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-875">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-875">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-876">Vérifiez vos paramètres de connectivité Internet.</span><span class="sxs-lookup"><span data-stu-id="0096a-876">Check your Internet connectivity settings.</span></span>
<span data-ttu-id="0096a-877">Le client Antivirus Microsoft Defender a rencontré une erreur lors de l’utilisation du service signature dynamique pour télécharger les dernières définitions d’une menace spécifique.</span><span class="sxs-lookup"><span data-stu-id="0096a-877">The Microsoft Defender Antivirus client encountered an error when using the Dynamic Signature Service to download the latest definitions to a specific threat.</span></span> <span data-ttu-id="0096a-878">Cette erreur est probablement due à un problème de connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="0096a-878">This error is likely caused by a network connectivity issue.</span></span> 
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-879">ID d’événement : 2030</span><span class="sxs-lookup"><span data-stu-id="0096a-879">Event ID: 2030</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-880">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-880">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-881">
<b>MALWAREPROTECTION_OFFLINE_SCAN_INSTALLED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-881">
<b>MALWAREPROTECTION_OFFLINE_SCAN_INSTALLED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-882">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-882">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-883">
<b>Le moteur du logiciel anti-programme malveillant a été téléchargé et est configuré pour s’exécuter hors connexion lors du redémarrage suivant du système.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-883">
<b>The antimalware engine was downloaded and is configured to run offline on the next system restart.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-884">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-884">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-885">Antivirus Microsoft Defender un antivirus hors connexion téléchargé et configuré pour s’exécuter au prochain redémarrage.</span><span class="sxs-lookup"><span data-stu-id="0096a-885">Microsoft Defender Antivirus downloaded and configured offline antivirus to run on the next reboot.</span></span>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-886">ID d’événement : 2031</span><span class="sxs-lookup"><span data-stu-id="0096a-886">Event ID: 2031</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-887">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-887">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-888">
<b>MALWAREPROTECTION_OFFLINE_SCAN_INSTALL_FAILED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-888">
<b>MALWAREPROTECTION_OFFLINE_SCAN_INSTALL_FAILED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-889">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-889">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-890">
<b>Le moteur du logiciel anti-programme malveillant n’a pas pu télécharger et configurer une analyse hors connexion.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-890">
<b>The antimalware engine was unable to download and configure an offline scan.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-891">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-891">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-892">Antivirus Microsoft Defender a rencontré une erreur lors de la tentative de téléchargement et de configuration de l’antivirus hors connexion.</span><span class="sxs-lookup"><span data-stu-id="0096a-892">Microsoft Defender Antivirus has encountered an error trying to download and configure offline antivirus.</span></span>
<dl><span data-ttu-id="0096a-893">
<dt>Code d’erreur : &lt; Code de résultat du &gt; code d’erreur associé à l’état de la menace. Valeurs HRESULT standard.</dt> 
<dt>Description de l’erreur : &lt; Description de &gt; l’erreur.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-893">
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values.</dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-894">ID d’événement : 2040</span><span class="sxs-lookup"><span data-stu-id="0096a-894">Event ID: 2040</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-895">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-895">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-896">
<b>MALWAREPROTECTION_OS_EXPIRING </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-896">
<b>MALWAREPROTECTION_OS_EXPIRING </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-897">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-897">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-898">
<b>La prise en charge du logiciel anti-programme malveillant pour cette version du système d’exploitation va bientôt se terminer. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-898">
<b>Antimalware support for this operating system version will soon end. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-899">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-899">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-900">La prise en charge de votre système d’exploitation expirera prochainement.</span><span class="sxs-lookup"><span data-stu-id="0096a-900">The support for your operating system will expire shortly.</span></span> <span data-ttu-id="0096a-901">L’Antivirus Microsoft Defender sur un système d’exploitation hors prise en charge n’est pas une solution adéquate pour se protéger contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="0096a-901">Running Microsoft Defender Antivirus on an out of support operating system is not an adequate solution to protect against threats.</span></span>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-902">ID d'événement : 2041</span><span class="sxs-lookup"><span data-stu-id="0096a-902">Event ID: 2041</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-903">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-903">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-904">
<b>MALWAREPROTECTION_OS_EOL </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-904">
<b>MALWAREPROTECTION_OS_EOL </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-905">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-905">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-906">
<b>La prise en charge du logiciel anti-programme malveillant pour ce système d’exploitation est terminée. Vous devez mettre à niveau le système d’exploitation pour une prise en charge continue. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-906">
<b>Antimalware support for this operating system has ended. You must upgrade the operating system for continued support. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-907">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-907">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-908">La prise en charge de votre système d’exploitation a expiré.</span><span class="sxs-lookup"><span data-stu-id="0096a-908">The support for your operating system has expired.</span></span> <span data-ttu-id="0096a-909">L’Antivirus Microsoft Defender sur un système d’exploitation hors prise en charge n’est pas une solution adéquate pour se protéger contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="0096a-909">Running Microsoft Defender Antivirus on an out of support operating system is not an adequate solution to protect against threats.</span></span>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-910">ID d’événement : 2042</span><span class="sxs-lookup"><span data-stu-id="0096a-910">Event ID: 2042</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-911">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-911">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-912">
<b>MALWAREPROTECTION_PROTECTION_EOL </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-912">
<b>MALWAREPROTECTION_PROTECTION_EOL </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-913">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-913">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-914">
<b>Le moteur du logiciel anti-programme malveillant ne prend plus en charge ce système d’exploitation et ne protège plus votre système contre les programmes malveillants. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-914">
<b>The antimalware engine no longer supports this operating system, and is no longer protecting your system from malware. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-915">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-915">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-916">La prise en charge de votre système d’exploitation a expiré.</span><span class="sxs-lookup"><span data-stu-id="0096a-916">The support for your operating system has expired.</span></span> <span data-ttu-id="0096a-917">Antivirus Microsoft Defender n’est plus pris en charge sur votre système d’exploitation, a cessé de fonctionner et ne protège pas contre les menaces de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="0096a-917">Microsoft Defender Antivirus is no longer supported on your operating system, has stopped functioning, and is not protecting against malware threats.</span></span>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-918">ID d’événement : 3002</span><span class="sxs-lookup"><span data-stu-id="0096a-918">Event ID: 3002</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-919">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-919">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-920">
<b>MALWAREPROTECTION_RTP_FEATURE_FAILURE </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-920">
<b>MALWAREPROTECTION_RTP_FEATURE_FAILURE </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-921">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-921">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-922">
<b>La protection en temps réel a rencontré une erreur et a échoué.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-922">
<b>Real-time protection encountered an error and failed.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-923">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-923">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-924">Antivirus Microsoft Defender Real-Time protection des données a rencontré une erreur et a échoué.</span><span class="sxs-lookup"><span data-stu-id="0096a-924">Microsoft Defender Antivirus Real-Time Protection feature has encountered an error and failed.</span></span>
<dl><span data-ttu-id="0096a-925">
<dt>Fonctionnalité : &lt; &gt; fonctionnalité, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-925">
<dt>Feature: &lt;Feature&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-926">Sur Access</span><span class="sxs-lookup"><span data-stu-id="0096a-926">On Access</span></span></li>
<li><span data-ttu-id="0096a-927">Téléchargements Internet Explorer et pièces jointes Microsoft Outlook Express</span><span class="sxs-lookup"><span data-stu-id="0096a-927">Internet Explorer downloads and Microsoft Outlook Express attachments</span></span></li>
<li><span data-ttu-id="0096a-928">Surveillance du comportement</span><span class="sxs-lookup"><span data-stu-id="0096a-928">Behavior monitoring</span></span></li>
<li><span data-ttu-id="0096a-929">Système d’inspection du réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-929">Network Inspection System</span></span></li>
</ul><span data-ttu-id="0096a-930">
</dt>
<dt>Code d’erreur : &lt; Code de résultat du &gt; code d’erreur associé à l’état de la menace. Valeurs HRESULT standard.</dt> 
<dt>Description de l’erreur : &lt; Description de &gt; l’erreur.</dt> Raison : la raison Antivirus Microsoft Defender protection en temps réel 
<dt>a redémarré une fonctionnalité.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-930">
</dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values.</dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
<dt>Reason: The reason Microsoft Defender Antivirus real-time protection has restarted a feature.</dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-931">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-931">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-932">Vous devez redémarrer le système, puis exécuter une analyse complète, car il est&#39;le système n’a pas été protégé pendant un certain temps.</span><span class="sxs-lookup"><span data-stu-id="0096a-932">You should restart the system then run a full scan because it&#39;s possible the system was not protected for some time.</span></span>
<span data-ttu-id="0096a-933">La Antivirus Microsoft Defender client&#39;fonctionnalité de protection en temps réel a rencontré une erreur, car l’un des services n’a pas réussi à démarrer.</span><span class="sxs-lookup"><span data-stu-id="0096a-933">The Microsoft Defender Antivirus client&#39;s real-time protection feature encountered an error because one of the services failed to start.</span></span> <span data-ttu-id="0096a-934">S’il est suivi d’un ID d’événement 3007, l’échec était temporaire et le client anti-programme malveillant a récupéré après l’échec.</span><span class="sxs-lookup"><span data-stu-id="0096a-934">If it is followed by a 3007 event ID, the failure was temporary and the antimalware client recovered from the failure.</span></span> 
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-935">ID d’événement : 3007</span><span class="sxs-lookup"><span data-stu-id="0096a-935">Event ID: 3007</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-936">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-936">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-937">
<b>MALWAREPROTECTION_RTP_FEATURE_RECOVERED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-937">
<b>MALWAREPROTECTION_RTP_FEATURE_RECOVERED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-938">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-938">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-939">
<b>La protection en temps réel a récupéré après une défaillance. Nous vous recommandons d’exécution d’une analyse système complète lorsque vous voyez cette erreur. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-939">
<b>Real-time protection recovered from a failure. We recommend running a full system scan when you see this error. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-940">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-940">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-941">Antivirus Microsoft Defender La protection en temps réel a redémarré une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="0096a-941">Microsoft Defender Antivirus Real-time Protection has restarted a feature.</span></span> <span data-ttu-id="0096a-942">Il est recommandé d’exécuter une analyse système complète pour détecter les éléments qui ont pu être manqués pendant que cet agent était en panne.</span><span class="sxs-lookup"><span data-stu-id="0096a-942">It is recommended that you run a full system scan to detect any items that may have been missed while this agent was down.</span></span>
<dl><span data-ttu-id="0096a-943">
<dt>Fonctionnalité : &lt; &gt; fonctionnalité, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-943">
<dt>Feature: &lt;Feature&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-944">Sur Access</span><span class="sxs-lookup"><span data-stu-id="0096a-944">On Access</span></span></li>
<li><span data-ttu-id="0096a-945">Téléchargements d’IE et Outlook Express</span><span class="sxs-lookup"><span data-stu-id="0096a-945">IE downloads and Outlook Express attachments</span></span></li>
<li><span data-ttu-id="0096a-946">Surveillance du comportement</span><span class="sxs-lookup"><span data-stu-id="0096a-946">Behavior monitoring</span></span></li>
<li><span data-ttu-id="0096a-947">Système d’inspection du réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-947">Network Inspection System</span></span></li>
</ul><span data-ttu-id="0096a-948">
</dt>
<dt>Raison : la raison Antivirus Microsoft Defender protection en temps réel a redémarré une fonctionnalité.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-948">
</dt>
<dt>Reason: The reason Microsoft Defender Antivirus real-time protection has restarted a feature.</dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-949">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-949">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-950">La fonctionnalité de protection en temps réel a redémarré.</span><span class="sxs-lookup"><span data-stu-id="0096a-950">The real-time protection feature has restarted.</span></span> <span data-ttu-id="0096a-951">Si cet événement se produit à nouveau, contactez <a href="https://go.microsoft.com/fwlink/?LinkId=215491">le support technique Microsoft.</a></span><span class="sxs-lookup"><span data-stu-id="0096a-951">If this event happens again, contact <a href="https://go.microsoft.com/fwlink/?LinkId=215491">Microsoft Technical Support</a>.</span></span> 
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-952">ID d’événement : 5000</span><span class="sxs-lookup"><span data-stu-id="0096a-952">Event ID: 5000</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-953">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-953">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-954">
<b>MALWAREPROTECTION_RTP_ENABLED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-954">
<b>MALWAREPROTECTION_RTP_ENABLED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-955">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-955">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-956">
<b>La protection en temps réel est activée. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-956">
<b>Real-time protection is enabled. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-957">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-957">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-958">Antivirus Microsoft Defender’analyse de la protection en temps réel pour les programmes malveillants et d’autres logiciels potentiellement indésirables a été activé.</span><span class="sxs-lookup"><span data-stu-id="0096a-958">Microsoft Defender Antivirus real-time protection scanning for malware and other potentially unwanted software was enabled.</span></span>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-959">ID d’événement : 5001</span><span class="sxs-lookup"><span data-stu-id="0096a-959">Event ID: 5001</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-960">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-960">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-961">
<b>MALWAREPROTECTION_RTP_DISABLED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-961">
<b>MALWAREPROTECTION_RTP_DISABLED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-962">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-962">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-963">
<b>La protection en temps réel est désactivée. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-963">
<b>Real-time protection is disabled. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-964">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-964">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-965">Antivirus Microsoft Defender’analyse de la protection en temps réel pour les programmes malveillants et d’autres logiciels potentiellement indésirables a été désactivé.</span><span class="sxs-lookup"><span data-stu-id="0096a-965">Microsoft Defender Antivirus real-time protection scanning for malware and other potentially unwanted software was disabled.</span></span> 
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-966">ID d’événement : 5004</span><span class="sxs-lookup"><span data-stu-id="0096a-966">Event ID: 5004</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-967">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-967">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-968">
<b>MALWAREPROTECTION_RTP_FEATURE_CONFIGURED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-968">
<b>MALWAREPROTECTION_RTP_FEATURE_CONFIGURED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-969">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-969">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-970">
<b>La configuration de la protection en temps réel a changé. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-970">
<b>The real-time protection configuration changed. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-971">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-971">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-972">Antivirus Microsoft Defender configuration des fonctionnalités de protection en temps réel a changé.</span><span class="sxs-lookup"><span data-stu-id="0096a-972">Microsoft Defender Antivirus real-time protection feature configuration has changed.</span></span>
<dl><span data-ttu-id="0096a-973">
<dt>Fonctionnalité : &lt; &gt; fonctionnalité, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0096a-973">
<dt>Feature: &lt;Feature&gt;, for example:</span></span>
<ul>
<li><span data-ttu-id="0096a-974">Sur Access</span><span class="sxs-lookup"><span data-stu-id="0096a-974">On Access</span></span></li>
<li><span data-ttu-id="0096a-975">Téléchargements d’IE et Outlook Express</span><span class="sxs-lookup"><span data-stu-id="0096a-975">IE downloads and Outlook Express attachments</span></span></li>
<li><span data-ttu-id="0096a-976">Surveillance du comportement</span><span class="sxs-lookup"><span data-stu-id="0096a-976">Behavior monitoring</span></span></li>
<li><span data-ttu-id="0096a-977">Système d’inspection du réseau</span><span class="sxs-lookup"><span data-stu-id="0096a-977">Network Inspection System</span></span></li>
</ul><span data-ttu-id="0096a-978">
</dt>
<dt>Configuration : </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-978">
</dt>
<dt>Configuration: </dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-979">ID d’événement : 5007</span><span class="sxs-lookup"><span data-stu-id="0096a-979">Event ID: 5007</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-980">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-980">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-981">
<b>MALWAREPROTECTION_CONFIG_CHANGED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-981">
<b>MALWAREPROTECTION_CONFIG_CHANGED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-982">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-982">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-983">
<b>La configuration de la plateforme anti-programme malveillant a été modifiée.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-983">
<b>The antimalware platform configuration changed.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-984">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-984">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-985">Antivirus Microsoft Defender configuration a changé.</span><span class="sxs-lookup"><span data-stu-id="0096a-985">Microsoft Defender Antivirus configuration has changed.</span></span> <span data-ttu-id="0096a-986">S’il s’agit d’un événement inattendu, vous devez passer en revue les paramètres, car cela peut être le résultat d’un programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="0096a-986">If this is an unexpected event, you should review the settings as this may be the result of malware.</span></span>
<dl><span data-ttu-id="0096a-987">
<dt>Ancienne valeur : &lt; Old value number &gt; Old antivirus configuration value.</dt> 
<dt>Nouvelle valeur : &lt; Nouvelle valeur nombre &gt; Nouvelle valeur de configuration antivirus.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-987">
<dt>Old value: &lt;Old value number&gt; Old antivirus configuration value.</dt>
<dt>New value: &lt;New value number&gt; New antivirus configuration value.</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-988">ID d’événement : 5008</span><span class="sxs-lookup"><span data-stu-id="0096a-988">Event ID: 5008</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-989">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-989">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-990">
<b>MALWAREPROTECTION_ENGINE_FAILURE</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-990">
<b>MALWAREPROTECTION_ENGINE_FAILURE</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-991">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-991">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-992">
<b>Le moteur du logiciel anti-programme malveillant a rencontré une erreur et a échoué.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-992">
<b>The antimalware engine encountered an error and failed.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-993">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-993">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-994">Antivirus Microsoft Defender moteur a été interrompu en raison d’une erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="0096a-994">Microsoft Defender Antivirus engine has been terminated due to an unexpected error.</span></span>
<dl><span data-ttu-id="0096a-995">
<dt>Type d’échec : &lt; Type &gt; d’échec, par exemple : Code d’exception</dt>d’incident ou de hang : ressource de
<dt> &lt; code &gt; </dt>
<dt>d’erreur : &lt; ressource &gt; </dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-995">
<dt>Failure Type: &lt;Failure type&gt;, for example: Crash or Hang</dt>
<dt>Exception Code: &lt;Error code&gt;</dt>
<dt>Resource: &lt;Resource&gt;</dt>
</span></span></dl>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-996">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-996">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-997">Pour résoudre les problèmes de cet événement :</span><span class="sxs-lookup"><span data-stu-id="0096a-997">To troubleshoot this event:</span></span><ol>
<li><span data-ttu-id="0096a-998">Essayez de redémarrer le service.</span><span class="sxs-lookup"><span data-stu-id="0096a-998">Try to restart the service.</span></span><ul>
<li><span data-ttu-id="0096a-999">Pour les logiciels anti-programme malveillant, antivirus et logiciels espions, à une invite de commandes avec élévation de niveaux, tapez <b>net stop msmpsvc,</b>puis tapez <b>net start msmpsvc</b> pour redémarrer le moteur de logiciel anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="0096a-999">For antimalware, antivirus and spyware, at an elevated command prompt, type <b>net stop msmpsvc</b>, and then type <b>net start msmpsvc</b> to restart the antimalware engine.</span></span></li>
<li><span data-ttu-id="0096a-1000">Pour le système <i>d’inspection</i>du réseau, à une invite de commandes avec élévation de niveaux, tapez <b>net start nissrv,</b>puis tapez <b>net start nissrv</b> pour redémarrer le moteur du système d’inspection du réseau à l’aide du fichier NiSSRV.exe. <i></i></span><span class="sxs-lookup"><span data-stu-id="0096a-1000">For the <i>Network Inspection System</i>, at an elevated command prompt, type <b>net start nissrv</b>, and then type <b>net start nissrv</b> to restart the <i>Network Inspection System</i> engine by using the NiSSRV.exe file.</span></span>
</li>
</ul>
</li>
<li><span data-ttu-id="0096a-1001">Si elle échoue de la même manière, recherchez le code d’erreur en <b></b> accédant au Site de support <a href="https://go.microsoft.com/fwlink/?LinkId=215163">Microsoft</a> et en entrant le numéro d’erreur dans la zone de recherche, puis contactez le support <a href="https://go.microsoft.com/fwlink/?LinkId=215491">technique Microsoft.</a></span><span class="sxs-lookup"><span data-stu-id="0096a-1001">If it fails in the same way, look up the error code by accessing the <a href="https://go.microsoft.com/fwlink/?LinkId=215163">Microsoft Support Site</a>  and entering the error number in the <b>Search</b> box, and contact <a href="https://go.microsoft.com/fwlink/?LinkId=215491">Microsoft Technical Support</a>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1002">Action de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0096a-1002">User action:</span></span>
</td>
<td >
<span data-ttu-id="0096a-1003">Le moteur Antivirus Microsoft Defender client est arrêté en raison d’une erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="0096a-1003">The Microsoft Defender Antivirus client engine stopped due to an unexpected error.</span></span>
<span data-ttu-id="0096a-1004">Pour résoudre les problèmes de cet événement :</span><span class="sxs-lookup"><span data-stu-id="0096a-1004">To troubleshoot this event:</span></span>
<ol>
<li><span data-ttu-id="0096a-1005">Exécutez à nouveau l’analyse.</span><span class="sxs-lookup"><span data-stu-id="0096a-1005">Run the scan again.</span></span></li>
<li><span data-ttu-id="0096a-1006">Si elle échoue de la même manière, allez sur le <b></b> site de support <a href="https://go.microsoft.com/fwlink/?LinkId=215163">Microsoft</a>, entrez le numéro d’erreur dans la zone de recherche pour rechercher le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0096a-1006">If it fails in the same way, go to the <a href="https://go.microsoft.com/fwlink/?LinkId=215163">Microsoft Support site</a>, enter the error number in the <b>Search</b> box to look for the error code.</span></span></li>
<li><span data-ttu-id="0096a-1007">Contactez le <a href="https://go.microsoft.com/fwlink/?LinkId=215491">Support technique Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="0096a-1007">Contact <a href="https://go.microsoft.com/fwlink/?LinkId=215491">Microsoft Technical Support</a>.</span></span>
</li>
</ol>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1008">ID d’événement : 5009</span><span class="sxs-lookup"><span data-stu-id="0096a-1008">Event ID: 5009</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-1009">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-1009">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-1010">
<b>MALWAREPROTECTION_ANTISPYWARE_ENABLED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1010">
<b>MALWAREPROTECTION_ANTISPYWARE_ENABLED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1011">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-1011">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-1012">
<b>L’analyse des programmes malveillants et autres logiciels potentiellement indésirables est activée. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1012">
<b>Scanning for malware and other potentially unwanted software is enabled. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1013">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-1013">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-1014">Antivirus Microsoft Defender recherche de programmes malveillants et d’autres logiciels potentiellement indésirables a été activée.</span><span class="sxs-lookup"><span data-stu-id="0096a-1014">Microsoft Defender Antivirus scanning for malware and other potentially unwanted software has been enabled.</span></span>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1015">ID d’événement : 5010</span><span class="sxs-lookup"><span data-stu-id="0096a-1015">Event ID: 5010</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-1016">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-1016">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-1017">
<b>MALWAREPROTECTION_ANTISPYWARE_DISABLED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1017">
<b>MALWAREPROTECTION_ANTISPYWARE_DISABLED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1018">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-1018">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-1019">
<b>L’analyse des programmes malveillants et autres logiciels potentiellement indésirables est désactivée.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1019">
<b>Scanning for malware and other potentially unwanted software is disabled.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1020">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-1020">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-1021">Antivirus Microsoft Defender recherche de programmes malveillants et d’autres logiciels potentiellement indésirables est désactivée.</span><span class="sxs-lookup"><span data-stu-id="0096a-1021">Microsoft Defender Antivirus scanning for malware and other potentially unwanted software is disabled.</span></span>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1022">ID d’événement : 5011</span><span class="sxs-lookup"><span data-stu-id="0096a-1022">Event ID: 5011</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-1023">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-1023">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-1024">
<b>MALWAREPROTECTION_ANTIVIRUS_ENABLED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1024">
<b>MALWAREPROTECTION_ANTIVIRUS_ENABLED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1025">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-1025">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-1026">
<b>L’analyse des virus est activée.</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1026">
<b>Scanning for viruses is enabled.</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1027">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-1027">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-1028">Antivirus Microsoft Defender recherche de virus a été activée.</span><span class="sxs-lookup"><span data-stu-id="0096a-1028">Microsoft Defender Antivirus scanning for viruses has been enabled.</span></span> 
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1029">ID d’événement : 5012</span><span class="sxs-lookup"><span data-stu-id="0096a-1029">Event ID: 5012</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-1030">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-1030">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-1031">
<b>MALWAREPROTECTION_ANTIVIRUS_DISABLED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1031">
<b>MALWAREPROTECTION_ANTIVIRUS_DISABLED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1032">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-1032">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-1033">
<b>L’analyse des virus est désactivée. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1033">
<b>Scanning for viruses is disabled. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1034">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-1034">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-1035">Antivirus Microsoft Defender recherche de virus est désactivée.</span><span class="sxs-lookup"><span data-stu-id="0096a-1035">Microsoft Defender Antivirus scanning for viruses is disabled.</span></span> 
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1036">ID d’événement : 5100</span><span class="sxs-lookup"><span data-stu-id="0096a-1036">Event ID: 5100</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-1037">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-1037">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-1038">
<b>MALWAREPROTECTION_EXPIRATION_WARNING_STATE </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1038">
<b>MALWAREPROTECTION_EXPIRATION_WARNING_STATE </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1039">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-1039">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-1040">
<b>La plateforme anti-programme malveillant expirera bientôt. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1040">
<b>The antimalware platform will expire soon. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1041">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-1041">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-1042">Antivirus Microsoft Defender a entré une période de grâce et va bientôt expirer.</span><span class="sxs-lookup"><span data-stu-id="0096a-1042">Microsoft Defender Antivirus has entered a grace period and will soon expire.</span></span> <span data-ttu-id="0096a-1043">Après l’expiration, ce programme désactive la protection contre les virus, les logiciels espions et d’autres logiciels potentiellement indésirables.</span><span class="sxs-lookup"><span data-stu-id="0096a-1043">After expiration, this program will disable protection against viruses, spyware, and other potentially unwanted software.</span></span>
<dl><span data-ttu-id="0096a-1044">
<dt>Raison de l’expiration : la raison Antivirus Microsoft Defender’expirera.</dt> 
<dt>Date d’expiration : date Antivirus Microsoft Defender date d’expiration.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1044">
<dt>Expiration Reason: The reason Microsoft Defender Antivirus will expire.</dt>
<dt>Expiration Date: The date Microsoft Defender Antivirus will expire.</dt>
</span></span></dl>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1045">ID d’événement : 5101</span><span class="sxs-lookup"><span data-stu-id="0096a-1045">Event ID: 5101</span></span></th>
</tr>
<tr><td>
<span data-ttu-id="0096a-1046">Nom symbolique :</span><span class="sxs-lookup"><span data-stu-id="0096a-1046">Symbolic name:</span></span>
</td>
<td ><span data-ttu-id="0096a-1047">
<b>MALWAREPROTECTION_DISABLED_EXPIRED_STATE </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1047">
<b>MALWAREPROTECTION_DISABLED_EXPIRED_STATE </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1048">Message :</span><span class="sxs-lookup"><span data-stu-id="0096a-1048">Message:</span></span>
</td>
<td ><span data-ttu-id="0096a-1049">
<b>La plateforme anti-programme malveillant a expiré. </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1049">
<b>The antimalware platform is expired. </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1050">Description :</span><span class="sxs-lookup"><span data-stu-id="0096a-1050">Description:</span></span>
</td>
<td >
<span data-ttu-id="0096a-1051">Antivirus Microsoft Defender période de grâce a expiré.</span><span class="sxs-lookup"><span data-stu-id="0096a-1051">Microsoft Defender Antivirus grace period has expired.</span></span> <span data-ttu-id="0096a-1052">La protection contre les virus, logiciels espions et autres logiciels potentiellement indésirables est désactivée.</span><span class="sxs-lookup"><span data-stu-id="0096a-1052">Protection against viruses, spyware, and other potentially unwanted software is disabled.</span></span>
<dl><span data-ttu-id="0096a-1053">
<dt>Raison de l’expiration :</dt>
<dt>Date d’expiration : </dt>Code 
<dt>d’erreur : code de résultat du code &lt; &gt; d’erreur associé à l’état de la menace. Valeurs HRESULT standard.</dt> 
<dt>Description de l’erreur : &lt; Description de &gt; l’erreur.</dt>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1053">
<dt>Expiration Reason:</dt>
<dt>Expiration Date: </dt>
<dt>Error Code: &lt;Error code&gt; Result code associated with threat status. Standard HRESULT values.</dt>
<dt>Error Description: &lt;Error description&gt; Description of the error. </dt>
</span></span></dl>
</td>
</tr><span data-ttu-id="0096a-1054">
</table>

<a id="error-codes"></a>
##Antivirus Microsoft Defender codes d’erreur du client si Antivirus Microsoft Defender des problèmes, il vous donne généralement un code d’erreur pour vous aider à résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="0096a-1054">
</table>

<a id="error-codes"></a>
## Microsoft Defender Antivirus client error codes If Microsoft Defender Antivirus experiences any issues it will usually give you an error code to help you troubleshoot the issue.</span></span> <span data-ttu-id="0096a-1055">Le plus souvent, une erreur signifie qu’il y a eu un problème d’installation d’une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0096a-1055">Most often an error means there was a problem installing an update.</span></span>
<span data-ttu-id="0096a-1056">Cette section fournit les informations suivantes sur les erreurs Antivirus Microsoft Defender client.</span><span class="sxs-lookup"><span data-stu-id="0096a-1056">This section provides the following information about Microsoft Defender Antivirus client errors.</span></span>
<span data-ttu-id="0096a-1057">-   Le code -   d’erreur La raison possible de l’erreur -   Conseils sur ce qu’il faut faire maintenant</span><span class="sxs-lookup"><span data-stu-id="0096a-1057">-   The error code -   The possible reason for the error -   Advice on what to do now</span></span>

<span data-ttu-id="0096a-1058">Utilisez les informations de ces tableaux pour résoudre les problèmes Antivirus Microsoft Defender codes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0096a-1058">Use the information in these tables to help troubleshoot Microsoft Defender Antivirus error codes.</span></span>


<table> 
<tr>
<th colspan="2"><span data-ttu-id="0096a-1059">Code d’erreur : 0x80508007</span><span class="sxs-lookup"><span data-stu-id="0096a-1059">Error code: 0x80508007</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="0096a-1060">Message</span><span class="sxs-lookup"><span data-stu-id="0096a-1060">Message</span></span></td>
<td><span data-ttu-id="0096a-1061">
<b>ERR_MP_NO_MEMORY </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1061">
<b>ERR_MP_NO_MEMORY </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1062">Raison possible</span><span class="sxs-lookup"><span data-stu-id="0096a-1062">Possible reason</span></span>
</td>
<td>
<span data-ttu-id="0096a-1063">Cette erreur indique que vous n’avez peut-être plus de mémoire.</span><span class="sxs-lookup"><span data-stu-id="0096a-1063">This error indicates that you might have run out of memory.</span></span> 
</td>
</tr>
<tr>
<td><span data-ttu-id="0096a-1064">Résolution</span><span class="sxs-lookup"><span data-stu-id="0096a-1064">Resolution</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0096a-1065">Vérifiez la mémoire disponible sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="0096a-1065">Check the available memory on your device.</span></span></li>
<li><span data-ttu-id="0096a-1066">Fermez les applications inutilisées en cours d’exécution pour libérer de la mémoire sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="0096a-1066">Close any unused applications that are running to free up memory on your device.</span></span></li>
<li><span data-ttu-id="0096a-1067">Redémarrez l’appareil et ré-exécutez l’analyse.</span><span class="sxs-lookup"><span data-stu-id="0096a-1067">Restart the device and run the scan again.</span></span> 
</li>
</ol>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1068">Code d’erreur : 0x8050800C</span><span class="sxs-lookup"><span data-stu-id="0096a-1068">Error code: 0x8050800C</span></span></th>
</tr><tr><td><span data-ttu-id="0096a-1069">Message</span><span class="sxs-lookup"><span data-stu-id="0096a-1069">Message</span></span></td>
<td><span data-ttu-id="0096a-1070"><b>ERR_MP_BAD_INPUT_DATA</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1070"><b>ERR_MP_BAD_INPUT_DATA</b>
</span></span></td></tr><tr><td><span data-ttu-id="0096a-1071">Raison possible</span><span class="sxs-lookup"><span data-stu-id="0096a-1071">Possible reason</span></span></td>
<td>
<span data-ttu-id="0096a-1072">Cette erreur indique qu’il peut y avoir un problème avec votre produit de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0096a-1072">This error indicates that there might be a problem with your security product.</span></span>
</td>
</tr><tr><td><span data-ttu-id="0096a-1073">Résolution</span><span class="sxs-lookup"><span data-stu-id="0096a-1073">Resolution</span></span></td><td>
<ol>
<li><span data-ttu-id="0096a-1074">Mettez à jour les définitions.</span><span class="sxs-lookup"><span data-stu-id="0096a-1074">Update the definitions.</span></span> <span data-ttu-id="0096a-1075">Les deux :</span><span class="sxs-lookup"><span data-stu-id="0096a-1075">Either:</span></span><ol>
<li><span data-ttu-id="0096a-1076">Cliquez sur le <b>bouton Mettre à jour les définitions</b> sous <b>l’onglet</b> Mettre à jour Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="0096a-1076">Click the <b>Update definitions</b> button on the <b>Update</b> tab in Microsoft Defender Antivirus.</span></span> <img src="images/defender-updatedefs2.png" alt="Update definitions in Microsoft Defender Antivirus"/><span data-ttu-id="0096a-1077">Ou,</span><span class="sxs-lookup"><span data-stu-id="0096a-1077">Or,</span></span>
</li>
<li><span data-ttu-id="0096a-1078">Téléchargez les dernières définitions à partir <a href="https://aka.ms/wdsi">du site Renseignement de sécurité Microsoft.</a></span><span class="sxs-lookup"><span data-stu-id="0096a-1078">Download the latest definitions from the <a href="https://aka.ms/wdsi">Microsoft Security Intelligence site</a>.</span></span>
<span data-ttu-id="0096a-1079">Remarque : la taille du fichier de définitions téléchargé à partir du site peut dépasser 60 Mo et ne doit pas être utilisée comme solution à long terme pour la mise à jour des définitions.</span><span class="sxs-lookup"><span data-stu-id="0096a-1079">Note: The size of the definitions file downloaded from the site can exceed 60 MB and should not be used as a long-term solution for updating definitions.</span></span>
</li>
</ol>
</li>
<li><span data-ttu-id="0096a-1080">Exécutez une analyse complète.</span><span class="sxs-lookup"><span data-stu-id="0096a-1080">Run a full scan.</span></span>
</li>
<li><span data-ttu-id="0096a-1081">Redémarrez l’appareil et réessayez.</span><span class="sxs-lookup"><span data-stu-id="0096a-1081">Restart the device and try again.</span></span></li>
</ol>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1082">Code d’erreur : 0x80508020</span><span class="sxs-lookup"><span data-stu-id="0096a-1082">Error code: 0x80508020</span></span></th>
</tr><tr><td><span data-ttu-id="0096a-1083">Message</span><span class="sxs-lookup"><span data-stu-id="0096a-1083">Message</span></span></td>
<td><span data-ttu-id="0096a-1084"><b>ERR_MP_BAD_CONFIGURATION </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1084"><b>ERR_MP_BAD_CONFIGURATION </b>
</span></span></td></tr><tr><td><span data-ttu-id="0096a-1085">Raison possible</span><span class="sxs-lookup"><span data-stu-id="0096a-1085">Possible reason</span></span></td>
<td>
<span data-ttu-id="0096a-1086">Cette erreur indique qu’il peut y avoir une erreur de configuration du moteur ; En commun, cela est lié aux données d’entrée qui ne permettent pas au moteur de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="0096a-1086">This error indicates that there might be an engine configuration error; commonly, this is related to input data that does not allow the engine to function properly.</span></span> 
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1087">Code d’erreur : 0x805080211</span><span class="sxs-lookup"><span data-stu-id="0096a-1087">Error code: 0x805080211</span></span>
</th>
</tr><tr><td><span data-ttu-id="0096a-1088">Message</span><span class="sxs-lookup"><span data-stu-id="0096a-1088">Message</span></span></td>
<td><span data-ttu-id="0096a-1089"><b>ERR_MP_QUARANTINE_FAILED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1089"><b>ERR_MP_QUARANTINE_FAILED </b>
</span></span></td></tr><tr><td><span data-ttu-id="0096a-1090">Raison possible</span><span class="sxs-lookup"><span data-stu-id="0096a-1090">Possible reason</span></span></td>
<td>
<span data-ttu-id="0096a-1091">Cette erreur indique qu’une Antivirus Microsoft Defender mise en quarantaine d’une menace a échoué.</span><span class="sxs-lookup"><span data-stu-id="0096a-1091">This error indicates that Microsoft Defender Antivirus failed to quarantine a threat.</span></span> 
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1092">Code d’erreur : 0x80508022</span><span class="sxs-lookup"><span data-stu-id="0096a-1092">Error code: 0x80508022</span></span>
</th>
</tr><tr><td><span data-ttu-id="0096a-1093">Message</span><span class="sxs-lookup"><span data-stu-id="0096a-1093">Message</span></span></td>
<td><span data-ttu-id="0096a-1094"><b>ERR_MP_REBOOT_REQUIRED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1094"><b>ERR_MP_REBOOT_REQUIRED </b>
</span></span></td></tr><tr><td><span data-ttu-id="0096a-1095">Raison possible</span><span class="sxs-lookup"><span data-stu-id="0096a-1095">Possible reason</span></span></td>
<td>
<span data-ttu-id="0096a-1096">Cette erreur indique qu’un redémarrage est nécessaire pour terminer la suppression des menaces.</span><span class="sxs-lookup"><span data-stu-id="0096a-1096">This error indicates that a reboot is required to complete threat removal.</span></span> 
</td>
</tr>
<tr>
<th colspan="2">
<span data-ttu-id="0096a-1097">0x80508023</span><span class="sxs-lookup"><span data-stu-id="0096a-1097">0x80508023</span></span>
</th>
</tr><tr><td><span data-ttu-id="0096a-1098">Message</span><span class="sxs-lookup"><span data-stu-id="0096a-1098">Message</span></span></td>
<td><span data-ttu-id="0096a-1099"><b>ERR_MP_THREAT_NOT_FOUND </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1099"><b>ERR_MP_THREAT_NOT_FOUND </b>
</span></span></td></tr><tr><td><span data-ttu-id="0096a-1100">Raison possible</span><span class="sxs-lookup"><span data-stu-id="0096a-1100">Possible reason</span></span></td>
<td>
<span data-ttu-id="0096a-1101">Cette erreur indique que la menace n’est peut-être plus présente sur le média ou que des programmes malveillants peuvent vous empêcher d’analyser votre appareil.</span><span class="sxs-lookup"><span data-stu-id="0096a-1101">This error indicates that the threat might no longer be present on the media, or malware might be stopping you from scanning your device.</span></span> 
</tr><tr><td><span data-ttu-id="0096a-1102">Résolution</span><span class="sxs-lookup"><span data-stu-id="0096a-1102">Resolution</span></span>
</td>
<td>
<span data-ttu-id="0096a-1103">Exécutez le <a href="https://www.microsoft.com/security/scanner/default.aspx">Scanner de sécurité Microsoft</a> puis mettez à jour votre logiciel de sécurité et essayez à nouveau.</span><span class="sxs-lookup"><span data-stu-id="0096a-1103">Run the <a href="https://www.microsoft.com/security/scanner/default.aspx">Microsoft Safety Scanner</a> then update your security software and try again.</span></span> 
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1104">Code d’erreur : 0x80508024</span><span class="sxs-lookup"><span data-stu-id="0096a-1104">Error code: 0x80508024</span></span> </th></tr>
<tr>
<td><span data-ttu-id="0096a-1105">Message</span><span class="sxs-lookup"><span data-stu-id="0096a-1105">Message</span></span></td>
<td><span data-ttu-id="0096a-1106"><b>ERR_MP_FULL_SCAN_REQUIRED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1106"><b>ERR_MP_FULL_SCAN_REQUIRED </b>
</span></span></td></tr><tr><td><span data-ttu-id="0096a-1107">Raison possible</span><span class="sxs-lookup"><span data-stu-id="0096a-1107">Possible reason</span></span></td>
<td>
<span data-ttu-id="0096a-1108">Cette erreur indique qu’une analyse complète du système peut être nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0096a-1108">This error indicates that a full system scan might be required.</span></span> 
</td></tr>
<tr>
<td><span data-ttu-id="0096a-1109">Résolution</span><span class="sxs-lookup"><span data-stu-id="0096a-1109">Resolution</span></span></td><td>
<span data-ttu-id="0096a-1110">Exécutez une analyse système complète.</span><span class="sxs-lookup"><span data-stu-id="0096a-1110">Run a full system scan.</span></span> 
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1111">Code d’erreur : 0x80508025</span><span class="sxs-lookup"><span data-stu-id="0096a-1111">Error code: 0x80508025</span></span>
</th>
</tr><tr><td><span data-ttu-id="0096a-1112">Message</span><span class="sxs-lookup"><span data-stu-id="0096a-1112">Message</span></span></td>
<td><span data-ttu-id="0096a-1113"><b>ERR_MP_MANUAL_STEPS_REQUIRED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1113"><b>ERR_MP_MANUAL_STEPS_REQUIRED </b>
</span></span></td></tr><tr><td><span data-ttu-id="0096a-1114">Raison possible</span><span class="sxs-lookup"><span data-stu-id="0096a-1114">Possible reason</span></span></td>
<td>
<span data-ttu-id="0096a-1115">Cette erreur indique que des étapes manuelles sont nécessaires pour terminer la suppression des menaces.</span><span class="sxs-lookup"><span data-stu-id="0096a-1115">This error indicates that manual steps are required to complete threat removal.</span></span> 
</td></tr><tr><td><span data-ttu-id="0096a-1116">Résolution</span><span class="sxs-lookup"><span data-stu-id="0096a-1116">Resolution</span></span></td><td>
<span data-ttu-id="0096a-1117">Suivez les étapes de correction manuelle décrites dans le Programme d’aide à la protection microsoft contre les programmes <a href="https://www.microsoft.com/security/portal/threat/Threats.aspx">malveillants.</a></span><span class="sxs-lookup"><span data-stu-id="0096a-1117">Follow the manual remediation steps outlined in the <a href="https://www.microsoft.com/security/portal/threat/Threats.aspx">Microsoft Malware Protection Encyclopedia</a>.</span></span> <span data-ttu-id="0096a-1118">Vous pouvez trouver un lien spécifique aux menaces dans l’historique des événements.</span><span class="sxs-lookup"><span data-stu-id="0096a-1118">You can find a threat-specific link in the event history.</span></span><br/></td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1119">Code d’erreur : 0x80508026</span><span class="sxs-lookup"><span data-stu-id="0096a-1119">Error code: 0x80508026</span></span>
</th>
</tr><tr><td><span data-ttu-id="0096a-1120">Message</span><span class="sxs-lookup"><span data-stu-id="0096a-1120">Message</span></span></td>
<td><span data-ttu-id="0096a-1121"><b>ERR_MP_REMOVE_NOT_SUPPORTED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1121"><b>ERR_MP_REMOVE_NOT_SUPPORTED </b>
</span></span></td></tr><tr><td><span data-ttu-id="0096a-1122">Raison possible</span><span class="sxs-lookup"><span data-stu-id="0096a-1122">Possible reason</span></span></td>
<td>
<span data-ttu-id="0096a-1123">Cette erreur indique que la suppression à l’intérieur du type de conteneur n’est peut-être pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0096a-1123">This error indicates that removal inside the container type might not be not supported.</span></span> 
</td></tr><tr><td><span data-ttu-id="0096a-1124">Résolution</span><span class="sxs-lookup"><span data-stu-id="0096a-1124">Resolution</span></span></td><td>
<span data-ttu-id="0096a-1125">Antivirus Microsoft Defender’est pas en mesure de corriger les menaces détectées à l’intérieur de l’archive.</span><span class="sxs-lookup"><span data-stu-id="0096a-1125">Microsoft Defender Antivirus is not able to remediate threats detected inside the archive.</span></span> <span data-ttu-id="0096a-1126">Envisagez de supprimer manuellement les ressources détectées.</span><span class="sxs-lookup"><span data-stu-id="0096a-1126">Consider manually removing the detected resources.</span></span> 
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1127">Code d’erreur : 0x80508027</span><span class="sxs-lookup"><span data-stu-id="0096a-1127">Error code: 0x80508027</span></span>
</th>
</tr><tr><td><span data-ttu-id="0096a-1128">Message</span><span class="sxs-lookup"><span data-stu-id="0096a-1128">Message</span></span></td>
<td><span data-ttu-id="0096a-1129"><b>ERR_MP_REMOVE_LOW_MEDIUM_DISABLED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1129"><b>ERR_MP_REMOVE_LOW_MEDIUM_DISABLED </b>
</span></span></td></tr><tr><td><span data-ttu-id="0096a-1130">Raison possible</span><span class="sxs-lookup"><span data-stu-id="0096a-1130">Possible reason</span></span></td>
<td>
<span data-ttu-id="0096a-1131">Cette erreur indique que la suppression des menaces faibles et moyennes peut être désactivée.</span><span class="sxs-lookup"><span data-stu-id="0096a-1131">This error indicates that removal of low and medium threats might be disabled.</span></span> 
</td></tr><tr><td><span data-ttu-id="0096a-1132">Résolution</span><span class="sxs-lookup"><span data-stu-id="0096a-1132">Resolution</span></span></td><td>
<span data-ttu-id="0096a-1133">Vérifiez les menaces détectées et résolvez-les selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="0096a-1133">Check the detected threats and resolve them as required.</span></span> 
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1134">Code d’erreur : 0x80508029</span><span class="sxs-lookup"><span data-stu-id="0096a-1134">Error code: 0x80508029</span></span>
</th>
</tr><tr><td><span data-ttu-id="0096a-1135">Message</span><span class="sxs-lookup"><span data-stu-id="0096a-1135">Message</span></span></td>
<td><span data-ttu-id="0096a-1136"><b>ERROR_MP_RESCAN_REQUIRED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1136"><b>ERROR_MP_RESCAN_REQUIRED </b>
</span></span></td></tr><tr><td><span data-ttu-id="0096a-1137">Raison possible</span><span class="sxs-lookup"><span data-stu-id="0096a-1137">Possible reason</span></span></td>
<td>
<span data-ttu-id="0096a-1138">Cette erreur indique qu’une nouvelle recherche de la menace est requise.</span><span class="sxs-lookup"><span data-stu-id="0096a-1138">This error indicates a rescan of the threat is required.</span></span> 
</td></tr><tr><td><span data-ttu-id="0096a-1139">Résolution</span><span class="sxs-lookup"><span data-stu-id="0096a-1139">Resolution</span></span></td><td>
<span data-ttu-id="0096a-1140">Exécutez une analyse système complète.</span><span class="sxs-lookup"><span data-stu-id="0096a-1140">Run a full system scan.</span></span> 
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1141">Code d’erreur : 0x80508030</span><span class="sxs-lookup"><span data-stu-id="0096a-1141">Error code: 0x80508030</span></span>
</th>
</tr><tr><td><span data-ttu-id="0096a-1142">Message</span><span class="sxs-lookup"><span data-stu-id="0096a-1142">Message</span></span></td>
<td><span data-ttu-id="0096a-1143"><b>ERROR_MP_CALLISTO_REQUIRED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1143"><b>ERROR_MP_CALLISTO_REQUIRED </b>
</span></span></td></tr><tr><td><span data-ttu-id="0096a-1144">Raison possible</span><span class="sxs-lookup"><span data-stu-id="0096a-1144">Possible reason</span></span></td>
<td>
<span data-ttu-id="0096a-1145">Cette erreur indique qu’une analyse hors connexion est requise.</span><span class="sxs-lookup"><span data-stu-id="0096a-1145">This error indicates that an offline scan is required.</span></span> 
</td></tr><tr><td><span data-ttu-id="0096a-1146">Résolution</span><span class="sxs-lookup"><span data-stu-id="0096a-1146">Resolution</span></span></td><td>
<span data-ttu-id="0096a-1147">Exécutez le Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="0096a-1147">Run offline Microsoft Defender Antivirus.</span></span> <span data-ttu-id="0096a-1148">Vous pouvez en savoir plus sur la façon de le faire dans <a href="https://windows.microsoft.com/windows/what-is-windows-defender-offline">l’article Antivirus Microsoft Defender hors connexion.</a></span><span class="sxs-lookup"><span data-stu-id="0096a-1148">You can read about how to do this in the <a href="https://windows.microsoft.com/windows/what-is-windows-defender-offline">offline Microsoft Defender Antivirus article</a>.</span></span>
</td>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0096a-1149">Code d’erreur : 0x80508031</span><span class="sxs-lookup"><span data-stu-id="0096a-1149">Error code: 0x80508031</span></span>
</th>
</tr><tr><td><span data-ttu-id="0096a-1150">Message</span><span class="sxs-lookup"><span data-stu-id="0096a-1150">Message</span></span></td>
<td><span data-ttu-id="0096a-1151"><b>ERROR_MP_PLATFORM_OUTDATED</span><span class="sxs-lookup"><span data-stu-id="0096a-1151"><b>ERROR_MP_PLATFORM_OUTDATED</span></span><br/></b>
</td></tr><tr><td><span data-ttu-id="0096a-1152">Raison possible</span><span class="sxs-lookup"><span data-stu-id="0096a-1152">Possible reason</span></span></td>
<td>
<span data-ttu-id="0096a-1153">Cette erreur indique que Antivirus Microsoft Defender ne prend pas en charge la version actuelle de la plateforme et nécessite une nouvelle version de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="0096a-1153">This error indicates that Microsoft Defender Antivirus does not support the current version of the platform and requires a new version of the platform.</span></span> 
</td></tr><tr><td><span data-ttu-id="0096a-1154">Résolution</span><span class="sxs-lookup"><span data-stu-id="0096a-1154">Resolution</span></span></td><td>
<span data-ttu-id="0096a-1155">Vous ne pouvez utiliser les Antivirus Microsoft Defender que dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0096a-1155">You can only use Microsoft Defender Antivirus in Windows 10.</span></span> <span data-ttu-id="0096a-1156">Pour Windows 8, Windows 7 et Windows Vista, vous pouvez utiliser <a href="https://www.microsoft.com/server-cloud/system-center/endpoint-protection-2012.aspx">System Center Endpoint Protection</a>.</span><span class="sxs-lookup"><span data-stu-id="0096a-1156">For Windows 8, Windows 7 and Windows Vista, you can use <a href="https://www.microsoft.com/server-cloud/system-center/endpoint-protection-2012.aspx">System Center Endpoint Protection</a>.</span></span><br/></td>
</tr>
</table><span data-ttu-id="0096a-1157">

<a id="internal-error-codes"></a>Les codes d’erreur suivants sont utilisés lors des tests internes de Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="0096a-1157">

<a id="internal-error-codes"></a> The following error codes are used during internal testing of Microsoft Defender Antivirus.</span></span>

<span data-ttu-id="0096a-1158">Si vous voyez ces erreurs, vous pouvez essayer de mettre à jour les [définitions](manage-updates-baselines-microsoft-defender-antivirus.md) et de forcer une nouvelle mise à jour directement sur le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0096a-1158">If you see these errors, you can try to [update definitions](manage-updates-baselines-microsoft-defender-antivirus.md) and force a rescan directly on the endpoint.</span></span>


<table> 
<tr>
<th colspan="3"><span data-ttu-id="0096a-1159">Codes d’erreur internes</span><span class="sxs-lookup"><span data-stu-id="0096a-1159">Internal error codes</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0096a-1160"><b>Code d’erreur</b></span><span class="sxs-lookup"><span data-stu-id="0096a-1160"><b>Error code</b></span></span></th>
<th><span data-ttu-id="0096a-1161">Message affiché</span><span class="sxs-lookup"><span data-stu-id="0096a-1161">Message displayed</span></span></th>
<th><span data-ttu-id="0096a-1162">Raison possible de l’erreur et de la résolution</span><span class="sxs-lookup"><span data-stu-id="0096a-1162">Possible reason for error and resolution</span></span></th>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1163">0x80501004</span><span class="sxs-lookup"><span data-stu-id="0096a-1163">0x80501004</span></span>
</td>
<td><span data-ttu-id="0096a-1164">
<b>ERROR_MP_NO_INTERNET_CONN </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1164">
<b>ERROR_MP_NO_INTERNET_CONN </b>
</span></span></td>
<td>
<span data-ttu-id="0096a-1165">Vérifiez votre connexion Internet, puis exécutez à nouveau l’analyse.</span><span class="sxs-lookup"><span data-stu-id="0096a-1165">Check your Internet connection, then run the scan again.</span></span>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1166">0x80501000</span><span class="sxs-lookup"><span data-stu-id="0096a-1166">0x80501000</span></span>
</td>
<td><span data-ttu-id="0096a-1167">
<b>ERROR_MP_UI_CONSOLIDATION_BAS</b> E</span><span class="sxs-lookup"><span data-stu-id="0096a-1167">
<b>ERROR_MP_UI_CONSOLIDATION_BAS</b>E</span></span>
</td>
<td rowspan="34">
<span data-ttu-id="0096a-1168">Il s’agit d’une erreur interne.</span><span class="sxs-lookup"><span data-stu-id="0096a-1168">This is an internal error.</span></span> <span data-ttu-id="0096a-1169">La cause n’est pas clairement définie.</span><span class="sxs-lookup"><span data-stu-id="0096a-1169">The cause is not clearly defined.</span></span>
</td>
<td rowspan="36">

</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1170">0x80501001</span><span class="sxs-lookup"><span data-stu-id="0096a-1170">0x80501001</span></span>
</td>
<td><span data-ttu-id="0096a-1171">
<b>ERROR_MP_ACTIONS_FAILED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1171">
<b>ERROR_MP_ACTIONS_FAILED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1172">0x80501002</span><span class="sxs-lookup"><span data-stu-id="0096a-1172">0x80501002</span></span>
</td>
<td><span data-ttu-id="0096a-1173">
<b>ERROR_MP_NOENGINE</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1173">
<b>ERROR_MP_NOENGINE</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1174">0x80501003</span><span class="sxs-lookup"><span data-stu-id="0096a-1174">0x80501003</span></span>
</td>
<td><span data-ttu-id="0096a-1175">
<b>ERROR_MP_ACTIVE_THREATS</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1175">
<b>ERROR_MP_ACTIVE_THREATS</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1176">0x805011011</span><span class="sxs-lookup"><span data-stu-id="0096a-1176">0x805011011</span></span>
</td>
<td><span data-ttu-id="0096a-1177">
<b>MP_ERROR_CODE_LUA_CANCELLED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1177">
<b>MP_ERROR_CODE_LUA_CANCELLED </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1178">0x80501101</span><span class="sxs-lookup"><span data-stu-id="0096a-1178">0x80501101</span></span>
</td>
<td><span data-ttu-id="0096a-1179">
<b>ERROR_LUA_CANCELLATION </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1179">
<b>ERROR_LUA_CANCELLATION </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1180">0x80501102</span><span class="sxs-lookup"><span data-stu-id="0096a-1180">0x80501102</span></span>
</td>
<td><span data-ttu-id="0096a-1181">
<b>MP_ERROR_CODE_ALREADY_SHUTDOWN</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1181">
<b>MP_ERROR_CODE_ALREADY_SHUTDOWN</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1182">0x80501103</span><span class="sxs-lookup"><span data-stu-id="0096a-1182">0x80501103</span></span>
</td>
<td><span data-ttu-id="0096a-1183">
<b>MP_ERROR_CODE_RDEVICE_S_ASYNC_CALL_PENDING </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1183">
<b>MP_ERROR_CODE_RDEVICE_S_ASYNC_CALL_PENDING </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1184">0x80501104</span><span class="sxs-lookup"><span data-stu-id="0096a-1184">0x80501104</span></span>
</td>
<td><span data-ttu-id="0096a-1185">
<b>MP_ERROR_CODE_CANCELLED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1185">
<b>MP_ERROR_CODE_CANCELLED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1186">0x80501105</span><span class="sxs-lookup"><span data-stu-id="0096a-1186">0x80501105</span></span>
</td>
<td><span data-ttu-id="0096a-1187">
<b>MP_ERROR_CODE_NO_TARGETOS</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1187">
<b>MP_ERROR_CODE_NO_TARGETOS</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1188">0x80501106</span><span class="sxs-lookup"><span data-stu-id="0096a-1188">0x80501106</span></span>
</td>
<td><span data-ttu-id="0096a-1189">
<b>MP_ERROR_CODE_BAD_REGEXP</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1189">
<b>MP_ERROR_CODE_BAD_REGEXP</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1190">0x80501107</span><span class="sxs-lookup"><span data-stu-id="0096a-1190">0x80501107</span></span>
</td>
<td><span data-ttu-id="0096a-1191">
<b>MP_ERROR_TEST_INDUCED_ERROR</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1191">
<b>MP_ERROR_TEST_INDUCED_ERROR</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1192">0x80501108</span><span class="sxs-lookup"><span data-stu-id="0096a-1192">0x80501108</span></span>
</td>
<td><span data-ttu-id="0096a-1193">
<b>MP_ERROR_SIG_BACKUP_DISABLED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1193">
<b>MP_ERROR_SIG_BACKUP_DISABLED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1194">0x80508001</span><span class="sxs-lookup"><span data-stu-id="0096a-1194">0x80508001</span></span>
</td>
<td><span data-ttu-id="0096a-1195">
<b>ERR_MP_BAD_INIT_MODULES</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1195">
<b>ERR_MP_BAD_INIT_MODULES</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1196">0x80508002</span><span class="sxs-lookup"><span data-stu-id="0096a-1196">0x80508002</span></span>
</td>
<td><span data-ttu-id="0096a-1197">
<b>ERR_MP_BAD_DATABASE</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1197">
<b>ERR_MP_BAD_DATABASE</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1198">0x80508004</span><span class="sxs-lookup"><span data-stu-id="0096a-1198">0x80508004</span></span>
</td>
<td><span data-ttu-id="0096a-1199">
<b>ERR_MP_BAD_UFS </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1199">
<b>ERR_MP_BAD_UFS </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1200">0x8050800C</span><span class="sxs-lookup"><span data-stu-id="0096a-1200">0x8050800C</span></span>
</td>
<td><span data-ttu-id="0096a-1201">
<b>ERR_MP_BAD_INPUT_DATA</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1201">
<b>ERR_MP_BAD_INPUT_DATA</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1202">0x8050800D</span><span class="sxs-lookup"><span data-stu-id="0096a-1202">0x8050800D</span></span>
</td>
<td><span data-ttu-id="0096a-1203">
<b>ERR_MP_BAD_GLOBAL_STORAGE</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1203">
<b>ERR_MP_BAD_GLOBAL_STORAGE</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1204">0x8050800E</span><span class="sxs-lookup"><span data-stu-id="0096a-1204">0x8050800E</span></span>
</td>
<td><span data-ttu-id="0096a-1205">
<b>ERR_MP_OBSOLETE</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1205">
<b>ERR_MP_OBSOLETE</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1206">0x8050800F</span><span class="sxs-lookup"><span data-stu-id="0096a-1206">0x8050800F</span></span>
</td>
<td><span data-ttu-id="0096a-1207">
<b>ERR_MP_NOT_SUPPORTED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1207">
<b>ERR_MP_NOT_SUPPORTED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1208">0x8050800F 0x80508010</span><span class="sxs-lookup"><span data-stu-id="0096a-1208">0x8050800F 0x80508010</span></span>
</td>
<td><span data-ttu-id="0096a-1209">
<b>ERR_MP_NO_MORE_ITEMS </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1209">
<b>ERR_MP_NO_MORE_ITEMS </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1210">0x80508011</span><span class="sxs-lookup"><span data-stu-id="0096a-1210">0x80508011</span></span>
</td>
<td><span data-ttu-id="0096a-1211">
<b>ERR_MP_DUPLICATE_SCANID</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1211">
<b>ERR_MP_DUPLICATE_SCANID</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1212">0x80508012</span><span class="sxs-lookup"><span data-stu-id="0096a-1212">0x80508012</span></span>
</td>
<td><span data-ttu-id="0096a-1213">
<b>ERR_MP_BAD_SCANID</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1213">
<b>ERR_MP_BAD_SCANID</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1214">0x80508013</span><span class="sxs-lookup"><span data-stu-id="0096a-1214">0x80508013</span></span>
</td>
<td><span data-ttu-id="0096a-1215">
<b>ERR_MP_BAD_USERDB_VERSION</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1215">
<b>ERR_MP_BAD_USERDB_VERSION</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1216">0x80508014</span><span class="sxs-lookup"><span data-stu-id="0096a-1216">0x80508014</span></span>
</td>
<td><span data-ttu-id="0096a-1217">
<b>ERR_MP_RESTORE_FAILED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1217">
<b>ERR_MP_RESTORE_FAILED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1218">0x80508016</span><span class="sxs-lookup"><span data-stu-id="0096a-1218">0x80508016</span></span>
</td>
<td><span data-ttu-id="0096a-1219">
<b>ERR_MP_BAD_ACTION</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1219">
<b>ERR_MP_BAD_ACTION</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1220">0x80508019</span><span class="sxs-lookup"><span data-stu-id="0096a-1220">0x80508019</span></span>
</td>
<td><span data-ttu-id="0096a-1221">
<b>ERR_MP_NOT_FOUND</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1221">
<b>ERR_MP_NOT_FOUND</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1222">0x80509001</span><span class="sxs-lookup"><span data-stu-id="0096a-1222">0x80509001</span></span>
</td>
<td><span data-ttu-id="0096a-1223">
<b>ERR_RELO_BAD_EHANDLE</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1223">
<b>ERR_RELO_BAD_EHANDLE</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1224">0x80509003</span><span class="sxs-lookup"><span data-stu-id="0096a-1224">0x80509003</span></span>
</td>
<td><span data-ttu-id="0096a-1225">
<b>ERR_RELO_KERNEL_NOT_LOADED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1225">
<b>ERR_RELO_KERNEL_NOT_LOADED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1226">0x8050A001</span><span class="sxs-lookup"><span data-stu-id="0096a-1226">0x8050A001</span></span>
</td>
<td><span data-ttu-id="0096a-1227">
<b>ERR_MP_BADDB_OPEN</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1227">
<b>ERR_MP_BADDB_OPEN</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1228">0x8050A002</span><span class="sxs-lookup"><span data-stu-id="0096a-1228">0x8050A002</span></span>
</td>
<td><span data-ttu-id="0096a-1229">
<b>ERR_MP_BADDB_HEADER</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1229">
<b>ERR_MP_BADDB_HEADER</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1230">0x8050A003</span><span class="sxs-lookup"><span data-stu-id="0096a-1230">0x8050A003</span></span>
</td>
<td><span data-ttu-id="0096a-1231">
<b>ERR_MP_BADDB_OLDENGINE</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1231">
<b>ERR_MP_BADDB_OLDENGINE</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1232">0x8050A004</span><span class="sxs-lookup"><span data-stu-id="0096a-1232">0x8050A004</span></span>
</td>
<td><span data-ttu-id="0096a-1233">
<b>ERR_MP_BADDB_CONTENT </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1233">
<b>ERR_MP_BADDB_CONTENT </b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1234">0x8050A005</span><span class="sxs-lookup"><span data-stu-id="0096a-1234">0x8050A005</span></span>
</td>
<td><span data-ttu-id="0096a-1235">
<b>ERR_MP_BADDB_NOTSIGNED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1235">
<b>ERR_MP_BADDB_NOTSIGNED</b>
</span></span></td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1236">0x8050801</span><span class="sxs-lookup"><span data-stu-id="0096a-1236">0x8050801</span></span>
</td>
<td><span data-ttu-id="0096a-1237">
<b>ERR_MP_REMOVE_FAILED</b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1237">
<b>ERR_MP_REMOVE_FAILED</b>
</span></span></td>
<td>
<span data-ttu-id="0096a-1238">Il s’agit d’une erreur interne.</span><span class="sxs-lookup"><span data-stu-id="0096a-1238">This is an internal error.</span></span> <span data-ttu-id="0096a-1239">Elle peut être déclenchée lorsque la suppression des programmes malveillants ne réussit pas.</span><span class="sxs-lookup"><span data-stu-id="0096a-1239">It might be triggered when malware removal is not successful.</span></span> 
</td>
</tr>
<tr>
<td>
<span data-ttu-id="0096a-1240">0x80508018</span><span class="sxs-lookup"><span data-stu-id="0096a-1240">0x80508018</span></span>
</td>
<td><span data-ttu-id="0096a-1241">
<b>ERR_MP_SCAN_ABORTED </b>
</span><span class="sxs-lookup"><span data-stu-id="0096a-1241">
<b>ERR_MP_SCAN_ABORTED </b>
</span></span></td>
<td>
<span data-ttu-id="0096a-1242">Il s’agit d’une erreur interne.</span><span class="sxs-lookup"><span data-stu-id="0096a-1242">This is an internal error.</span></span> <span data-ttu-id="0096a-1243">Il se peut qu’il se soit déclenché lorsqu’une analyse échoue.</span><span class="sxs-lookup"><span data-stu-id="0096a-1243">It might have triggered when a scan fails to complete.</span></span> 
</td>
</tr>
</table>

## <a name="related-topics"></a><span data-ttu-id="0096a-1244">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0096a-1244">Related topics</span></span>

- [<span data-ttu-id="0096a-1245">Rapport sur la protection Antivirus Microsoft Defender de données</span><span class="sxs-lookup"><span data-stu-id="0096a-1245">Report on Microsoft Defender Antivirus protection</span></span>](report-monitor-microsoft-defender-antivirus.md)
- [<span data-ttu-id="0096a-1246">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="0096a-1246">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
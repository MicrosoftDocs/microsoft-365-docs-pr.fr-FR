---
title: Créer des enregistrements DNS sur easyDNS pour Microsoft
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
- Adm_O365_Setup
ms.custom: AdminSurgePortfolio
search.appverid:
- MET150
- MOE150
ms.assetid: 446babfe-2e08-4cc2-bbfb-c05b854933ac
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur easyDNS pour Microsoft.
ms.openlocfilehash: 24f477d240af936975141c53d382e114a24c0ac5
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44400231"
---
# <a name="create-dns-records-at-easydns-for-microsoft"></a><span data-ttu-id="81dee-103">Créer des enregistrements DNS sur easyDNS pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="81dee-103">Create DNS records at easyDNS for Microsoft</span></span>

<span data-ttu-id="81dee-104">[Consultez le Forum aux questions sur les domaines](../setup/domains-faq.md) si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="81dee-104">[Check the Domains FAQ ](../setup/domains-faq.md) if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="81dee-105">Vous devrez ajouter tous les enregistrements DNS suivants sur le site Web de votre registraire pour acheminer le courrier vers Microsoft, utiliser votre domaine pour teams et Skype entreprise, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="81dee-105">You'll need to add all of the following DNS records at your registrar's website to route mail to Microsoft, use your domain for Teams and Skype for Business, and so on.</span></span>
  
<span data-ttu-id="81dee-106">Remarque : les enregistrements SRV ne sont actuellement pas disponibles dans tous les packages de service easyDNS.</span><span class="sxs-lookup"><span data-stu-id="81dee-106">NOTE: SRV Records are currently NOT available under all easyDNS service packages.</span></span> <span data-ttu-id="81dee-107">Vous devrez peut-être effectuer une mise à niveau vers un niveau de service supérieur avec easyDNS pour ajouter des enregistrements SRV qui sont requis pour Skype entreprise.</span><span class="sxs-lookup"><span data-stu-id="81dee-107">You may need to upgrade to a higher service level with easyDNS to add SRV records which are required for Skype for Business.</span></span>
  
## <a name="verify-that-you-own-the-domain-with-a-txt-record"></a><span data-ttu-id="81dee-108">Vérifier que vous êtes propriétaire du domaine avec un enregistrement TXT</span><span class="sxs-lookup"><span data-stu-id="81dee-108">Verify that you own the domain with a TXT record</span></span>

1. <span data-ttu-id="81dee-109">Accédez à [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) et connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="81dee-109">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="81dee-110">Sous l’en-tête **tous les domaines** , sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="81dee-110">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="81dee-111">Sous l’en-tête **txt Records (enregistrements TXT** ), cliquez sur le bouton modifier (icône de clé).</span><span class="sxs-lookup"><span data-stu-id="81dee-111">Under the **TXT records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="81dee-112">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="81dee-112">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="81dee-113">**Hôte**</span><span class="sxs-lookup"><span data-stu-id="81dee-113">**Host**</span></span>|<span data-ttu-id="81dee-114">**Text**</span><span class="sxs-lookup"><span data-stu-id="81dee-114">**Text**</span></span>|
    |:-----|:-----|
    |@  <br/> |<span data-ttu-id="81dee-115">MS = msXXXXXXXX (utilisez la valeur fournie dans la page domaines du centre d’administration)</span><span class="sxs-lookup"><span data-stu-id="81dee-115">MS=msXXXXXXXX (Use the value provided to you on the admin center Domains page)</span></span>  <br/> |
   
5. <span data-ttu-id="81dee-116">Sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="81dee-116">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="81dee-117">Vérifiez que l’enregistrement est correct, puis sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="81dee-117">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
7. <span data-ttu-id="81dee-118">Patientez quelques minutes avant de poursuivre, afin que l’enregistrement que vous venez de créer puisse se propager sur Internet et soit détecté par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="81dee-118">Wait a few minutes before you continue, so that the record you just created can propagate across the Internet and be detected by Microsoft.</span></span>
    
8. <span data-ttu-id="81dee-119">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="81dee-119">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
    
9. <span data-ttu-id="81dee-120">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="81dee-120">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
10. <span data-ttu-id="81dee-121">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="81dee-121">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
11. <span data-ttu-id="81dee-122">Sur la page **installation** , sélectionnez **Démarrer l’installation.**</span><span class="sxs-lookup"><span data-stu-id="81dee-122">On the **Setup** page, select **Start setup.**</span></span>
    
12. <span data-ttu-id="81dee-123">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="81dee-123">On the **Verify domain** page, select **Verify**.</span></span> 
    
## <a name="add-an-mx-record-to-route-email-to-microsoft"></a><span data-ttu-id="81dee-124">Ajouter un enregistrement MX pour acheminer le courrier électronique vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="81dee-124">Add an MX record to route email to Microsoft</span></span>

1. <span data-ttu-id="81dee-125">Accédez à [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) et connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="81dee-125">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="81dee-126">Sous l’en-tête **tous les domaines** , sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="81dee-126">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="81dee-127">Sous l’en-tête **MX Records (enregistrements MX** ), cliquez sur le bouton modifier (icône de clé).</span><span class="sxs-lookup"><span data-stu-id="81dee-127">Under the **MX records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="81dee-128">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="81dee-128">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="81dee-129">**COURRIER POUR LA ZONE**</span><span class="sxs-lookup"><span data-stu-id="81dee-129">**MAIL FOR ZONE**</span></span>|<span data-ttu-id="81dee-130">**SERVEUR DE MESSAGERIE**</span><span class="sxs-lookup"><span data-stu-id="81dee-130">**MAIL SERVER**</span></span>|<span data-ttu-id="81dee-131">**PRÉFÉRENCES**</span><span class="sxs-lookup"><span data-stu-id="81dee-131">**PREF**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="81dee-132">\<domain-key\>. mail.protection.outlook.com (obtenir votre \<domain-key\> valeur à partir de la page domaines du centre d’administration)</span><span class="sxs-lookup"><span data-stu-id="81dee-132">\<domain-key\>.mail.protection.outlook.com (Get your \<domain-key\> value from the admin center Domains page)</span></span>  <br/> |<span data-ttu-id="81dee-133">0</span><span class="sxs-lookup"><span data-stu-id="81dee-133">0</span></span>  <br/> |
   
2. <span data-ttu-id="81dee-134">Si vous souhaitez enregistrer vos autres enregistrements MX à des fins de sauvegarde, copiez-les quelque part.</span><span class="sxs-lookup"><span data-stu-id="81dee-134">If you want to save your other MX records for backup purposes, copy them down somewhere.</span></span> <span data-ttu-id="81dee-135">Avant de poursuivre, supprimez tous les autres enregistrements MX ici.</span><span class="sxs-lookup"><span data-stu-id="81dee-135">Before moving on, remove all other MX records here.</span></span>
    
5. <span data-ttu-id="81dee-136">Sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="81dee-136">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="81dee-137">Vérifiez que l’enregistrement est correct, puis sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="81dee-137">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
## <a name="add-the-required-cname-records"></a><span data-ttu-id="81dee-138">Ajouter les enregistrements CNAMe requis</span><span class="sxs-lookup"><span data-stu-id="81dee-138">Add the required CNAME records</span></span>

1. <span data-ttu-id="81dee-139">Accédez à [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) et connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="81dee-139">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="81dee-140">Sous l’en-tête **tous les domaines** , sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="81dee-140">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="81dee-141">Sous le titre **CNAME/alias Records** , cliquez sur le bouton modifier (icône de clé).</span><span class="sxs-lookup"><span data-stu-id="81dee-141">Under the **CNAME/Alias records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="81dee-142">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="81dee-142">Enter the following records in the text fields:</span></span>


    |<span data-ttu-id="81dee-143">**HOST (HÔTE)**</span><span class="sxs-lookup"><span data-stu-id="81dee-143">**HOST**</span></span>|<span data-ttu-id="81dee-144">**Address (doit se terminer par un « . »)**</span><span class="sxs-lookup"><span data-stu-id="81dee-144">**Address (Must end with a ".")**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="81dee-145">autodiscover</span><span class="sxs-lookup"><span data-stu-id="81dee-145">autodiscover</span></span>  <br/> |<span data-ttu-id="81dee-146">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="81dee-146">autodiscover.outlook.com.</span></span>  <br/> |
    |<span data-ttu-id="81dee-147">sip</span><span class="sxs-lookup"><span data-stu-id="81dee-147">sip</span></span>  <br/> |<span data-ttu-id="81dee-148">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="81dee-148">sipdir.online.lync.com.</span></span>  <br/> |
    |<span data-ttu-id="81dee-149">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="81dee-149">lyncdiscover</span></span>  <br/> |<span data-ttu-id="81dee-150">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="81dee-150">webdir.online.lync.com.</span></span>  <br/> |
    |<span data-ttu-id="81dee-151">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="81dee-151">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="81dee-152">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="81dee-152">enterpriseregistration.windows.net.</span></span>  <br/> |
    |<span data-ttu-id="81dee-153">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="81dee-153">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="81dee-154">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="81dee-154">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> |
   
5. <span data-ttu-id="81dee-155">Sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="81dee-155">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="81dee-156">Vérifiez que l’enregistrement est correct, puis sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="81dee-156">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="81dee-157">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="81dee-157">Add a TXT record for SPF to help prevent email spam</span></span>

1. <span data-ttu-id="81dee-158">Accédez à [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) et connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="81dee-158">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="81dee-159">Sous l’en-tête **tous les domaines** , sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="81dee-159">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="81dee-160">Sous l’en-tête **txt Records (enregistrements TXT** ), cliquez sur le bouton modifier (icône de clé).</span><span class="sxs-lookup"><span data-stu-id="81dee-160">Under the **TXT records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="81dee-161">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="81dee-161">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="81dee-162">**Hôte**</span><span class="sxs-lookup"><span data-stu-id="81dee-162">**Host**</span></span>|<span data-ttu-id="81dee-163">**Text**</span><span class="sxs-lookup"><span data-stu-id="81dee-163">**Text**</span></span>|
    |:-----|:-----|
    |@  <br/> |<span data-ttu-id="81dee-164">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="81dee-164">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> |
   
5. <span data-ttu-id="81dee-165">Sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="81dee-165">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="81dee-166">Vérifiez que l’enregistrement est correct, puis sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="81dee-166">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="81dee-167">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="81dee-167">Add the two SRV records that are required for Microsoft</span></span>

<span data-ttu-id="81dee-168">Remarque : les enregistrements SRV ne sont actuellement pas disponibles dans easyDNS’domaine plus niveau de service.</span><span class="sxs-lookup"><span data-stu-id="81dee-168">NOTE: SRV Records are currently NOT available under easyDNS' Domain Plus service level.</span></span> <span data-ttu-id="81dee-169">Vous devrez peut-être effectuer une mise à niveau vers un niveau de service supérieur avec easyDNS pour ajouter des enregistrements SRV</span><span class="sxs-lookup"><span data-stu-id="81dee-169">You may need to upgrade to a higher service level with easyDNS to add SRV records</span></span> 
  
1. <span data-ttu-id="81dee-170">Accédez à [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) et connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="81dee-170">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="81dee-171">Sous l’en-tête **tous les domaines** , sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="81dee-171">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="81dee-172">Sous l’en-tête **SRV Records (enregistrements SRV** ), cliquez sur le bouton modifier (icône de clé).</span><span class="sxs-lookup"><span data-stu-id="81dee-172">Under the **SRV records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="81dee-173">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="81dee-173">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="81dee-174">**SERVICE**</span><span class="sxs-lookup"><span data-stu-id="81dee-174">**SERVICE**</span></span>|<span data-ttu-id="81dee-175">**DEST**</span><span class="sxs-lookup"><span data-stu-id="81dee-175">**PROTO**</span></span>|<span data-ttu-id="81dee-176">**HOST (HÔTE)**</span><span class="sxs-lookup"><span data-stu-id="81dee-176">**HOST**</span></span>|<span data-ttu-id="81dee-177">**PRI**</span><span class="sxs-lookup"><span data-stu-id="81dee-177">**PRI**</span></span>|<span data-ttu-id="81dee-178">**WGT**</span><span class="sxs-lookup"><span data-stu-id="81dee-178">**WGT**</span></span>|<span data-ttu-id="81dee-179">**PORT**</span><span class="sxs-lookup"><span data-stu-id="81dee-179">**PORT**</span></span>|<span data-ttu-id="81dee-180">**CIBLE (doit se terminer par un « . »)**</span><span class="sxs-lookup"><span data-stu-id="81dee-180">**TARGET(Must end with a ".")**</span></span>|<span data-ttu-id="81dee-181">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="81dee-181">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="81dee-182">_sip</span><span class="sxs-lookup"><span data-stu-id="81dee-182">_sip</span></span>  <br/> |<span data-ttu-id="81dee-183">TLS</span><span class="sxs-lookup"><span data-stu-id="81dee-183">TLS</span></span>  <br/> |@  <br/> |<span data-ttu-id="81dee-184">100</span><span class="sxs-lookup"><span data-stu-id="81dee-184">100</span></span>  <br/> |<span data-ttu-id="81dee-185">1 </span><span class="sxs-lookup"><span data-stu-id="81dee-185">1</span></span>  <br/> |<span data-ttu-id="81dee-186">443</span><span class="sxs-lookup"><span data-stu-id="81dee-186">443</span></span>  <br/> |<span data-ttu-id="81dee-187">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="81dee-187">sipdir.online.lync.com.</span></span>  <br/> |<span data-ttu-id="81dee-188">1800</span><span class="sxs-lookup"><span data-stu-id="81dee-188">1800</span></span>  <br/> |
    |<span data-ttu-id="81dee-189">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="81dee-189">_sipfederationtls</span></span>  <br/> |<span data-ttu-id="81dee-190">TCP</span><span class="sxs-lookup"><span data-stu-id="81dee-190">TCP</span></span>  <br/> |@  <br/> |<span data-ttu-id="81dee-191">100</span><span class="sxs-lookup"><span data-stu-id="81dee-191">100</span></span>  <br/> |<span data-ttu-id="81dee-192">1 </span><span class="sxs-lookup"><span data-stu-id="81dee-192">1</span></span>  <br/> |<span data-ttu-id="81dee-193">5061</span><span class="sxs-lookup"><span data-stu-id="81dee-193">5061</span></span>  <br/> |<span data-ttu-id="81dee-194">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="81dee-194">sipfed.online.lync.com.</span></span>  <br/> |<span data-ttu-id="81dee-195">1800</span><span class="sxs-lookup"><span data-stu-id="81dee-195">1800</span></span>  <br/> |
   
5. <span data-ttu-id="81dee-196">Sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="81dee-196">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="81dee-197">Vérifiez que l’enregistrement est correct, puis sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="81dee-197">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    


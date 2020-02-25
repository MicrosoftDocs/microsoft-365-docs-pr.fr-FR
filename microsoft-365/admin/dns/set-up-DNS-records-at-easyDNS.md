---
title: Créer des enregistrements DNS sur easyDNS pour Office 365
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
- Adm_O365_Setup
search.appverid:
- MET150
- MOE150
ms.assetid: 446babfe-2e08-4cc2-bbfb-c05b854933ac
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur easyDNS pour Office 365.
ms.openlocfilehash: f55f39f36b8abaee2d500c87ccf1e0089caecc9d
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42253132"
---
# <a name="create-dns-records-at-easydns-for-office-365"></a><span data-ttu-id="785bd-103">Créer des enregistrements DNS sur easyDNS pour Office 365</span><span class="sxs-lookup"><span data-stu-id="785bd-103">Create DNS records at easyDNS for Office 365</span></span>

<span data-ttu-id="785bd-104">[Consultez le Forum aux questions sur les domaines](../setup/domains-faq.md) si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="785bd-104">[Check the Domains FAQ ](../setup/domains-faq.md) if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="785bd-105">Vous devrez ajouter tous les enregistrements DNS suivants sur le site Web de votre registraire pour acheminer le courrier vers Office 365, utiliser votre domaine pour teams et Skype entreprise, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="785bd-105">You'll need to add all of the following DNS records at your registrar's website to route mail to Office 365, use your domain for Teams and Skype for Business, and so on.</span></span>
  
<span data-ttu-id="785bd-106">Remarque : les enregistrements SRV ne sont actuellement pas disponibles dans tous les packages de service easyDNS.</span><span class="sxs-lookup"><span data-stu-id="785bd-106">NOTE: SRV Records are currently NOT available under all easyDNS service packages.</span></span> <span data-ttu-id="785bd-107">Vous devrez peut-être effectuer une mise à niveau vers un niveau de service supérieur avec easyDNS pour ajouter des enregistrements SRV requis pour Office 365 Skype entreprise.</span><span class="sxs-lookup"><span data-stu-id="785bd-107">You may need to upgrade to a higher service level with easyDNS to add SRV records which are required for Office 365 Skype for Business.</span></span>
  
## <a name="verify-that-you-own-the-domain-with-a-txt-record"></a><span data-ttu-id="785bd-108">Vérifier que vous êtes propriétaire du domaine avec un enregistrement TXT</span><span class="sxs-lookup"><span data-stu-id="785bd-108">Verify that you own the domain with a TXT record</span></span>

1. <span data-ttu-id="785bd-109">Accédez à [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) et connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="785bd-109">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="785bd-110">Sous l’en-tête **tous les domaines** , sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="785bd-110">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="785bd-111">Sous l’en-tête **txt Records (enregistrements TXT** ), cliquez sur le bouton modifier (icône de clé).</span><span class="sxs-lookup"><span data-stu-id="785bd-111">Under the **TXT records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="785bd-112">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="785bd-112">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="785bd-113">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="785bd-113">**Host**</span></span>|<span data-ttu-id="785bd-114">**Text**</span><span class="sxs-lookup"><span data-stu-id="785bd-114">**Text**</span></span>|
    |:-----|:-----|
    |@  <br/> |<span data-ttu-id="785bd-115">MS = msXXXXXXXX (utilisez la valeur fournie dans la page domaines du centre d’administration)</span><span class="sxs-lookup"><span data-stu-id="785bd-115">MS=msXXXXXXXX (Use the value provided to you on the admin center Domains page)</span></span>  <br/> |
   
5. <span data-ttu-id="785bd-116">Sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="785bd-116">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="785bd-117">Vérifiez que l’enregistrement est correct, puis sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="785bd-117">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
7. <span data-ttu-id="785bd-118">Patientez quelques minutes avant de poursuivre, afin que l’enregistrement que vous venez de créer puisse se propager sur Internet et soit détecté par Office 365.</span><span class="sxs-lookup"><span data-stu-id="785bd-118">Wait a few minutes before you continue, so that the record you just created can propagate across the Internet and be detected by Office 365.</span></span>
    
8. <span data-ttu-id="785bd-119">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span><span class="sxs-lookup"><span data-stu-id="785bd-119">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
    
9. <span data-ttu-id="785bd-120">Dans le centre d’administration, accédez à la page **paramètres** \> des <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="785bd-120">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
10. <span data-ttu-id="785bd-121">Dans la page **domaines** , sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="785bd-121">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
11. <span data-ttu-id="785bd-122">Sur la page **installation** , sélectionnez **Démarrer l’installation.**</span><span class="sxs-lookup"><span data-stu-id="785bd-122">On the **Setup** page, select **Start setup.**</span></span>
    
12. <span data-ttu-id="785bd-123">Sur la page **vérifier le domaine** , sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="785bd-123">On the **Verify domain** page, select **Verify**.</span></span> 
    
## <a name="add-an-mx-record-to-route-email-to-office-365"></a><span data-ttu-id="785bd-124">Ajouter un enregistrement MX pour acheminer le courrier électronique vers Office 365</span><span class="sxs-lookup"><span data-stu-id="785bd-124">Add an MX record to route email to Office 365</span></span>

1. <span data-ttu-id="785bd-125">Accédez à [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) et connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="785bd-125">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="785bd-126">Sous l’en-tête **tous les domaines** , sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="785bd-126">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="785bd-127">Sous l’en-tête **MX Records (enregistrements MX** ), cliquez sur le bouton modifier (icône de clé).</span><span class="sxs-lookup"><span data-stu-id="785bd-127">Under the **MX records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="785bd-128">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="785bd-128">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="785bd-129">**COURRIER POUR LA ZONE**</span><span class="sxs-lookup"><span data-stu-id="785bd-129">**MAIL FOR ZONE**</span></span>|<span data-ttu-id="785bd-130">**SERVEUR DE MESSAGERIE**</span><span class="sxs-lookup"><span data-stu-id="785bd-130">**MAIL SERVER**</span></span>|<span data-ttu-id="785bd-131">**PRÉFÉRENCES**</span><span class="sxs-lookup"><span data-stu-id="785bd-131">**PREF**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="785bd-132">\<Key\>. mail.protection.Outlook.com (obtenir votre \<valeur de clé\> de domaine à partir de la page domaines du centre d’administration)</span><span class="sxs-lookup"><span data-stu-id="785bd-132">\<domain-key\>.mail.protection.outlook.com (Get your \<domain-key\> value from the admin center Domains page)</span></span>  <br/> |<span data-ttu-id="785bd-133">0</span><span class="sxs-lookup"><span data-stu-id="785bd-133">0</span></span>  <br/> |
   
2. <span data-ttu-id="785bd-134">Si vous souhaitez enregistrer vos autres enregistrements MX à des fins de sauvegarde, copiez-les quelque part.</span><span class="sxs-lookup"><span data-stu-id="785bd-134">If you want to save your other MX records for backup purposes, copy them down somewhere.</span></span> <span data-ttu-id="785bd-135">Avant de poursuivre, supprimez tous les autres enregistrements MX ici.</span><span class="sxs-lookup"><span data-stu-id="785bd-135">Before moving on, remove all other MX records here.</span></span>
    
5. <span data-ttu-id="785bd-136">Sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="785bd-136">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="785bd-137">Vérifiez que l’enregistrement est correct, puis sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="785bd-137">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
## <a name="add-the-required-cname-records"></a><span data-ttu-id="785bd-138">Ajouter les enregistrements CNAMe requis</span><span class="sxs-lookup"><span data-stu-id="785bd-138">Add the required CNAME records</span></span>

1. <span data-ttu-id="785bd-139">Accédez à [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) et connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="785bd-139">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="785bd-140">Sous l’en-tête **tous les domaines** , sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="785bd-140">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="785bd-141">Sous le titre **CNAME/alias Records** , cliquez sur le bouton modifier (icône de clé).</span><span class="sxs-lookup"><span data-stu-id="785bd-141">Under the **CNAME/Alias records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="785bd-142">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="785bd-142">Enter the following records in the text fields:</span></span>


    |<span data-ttu-id="785bd-143">**HOST (HÔTE)**</span><span class="sxs-lookup"><span data-stu-id="785bd-143">**HOST**</span></span>|<span data-ttu-id="785bd-144">**Address (doit se terminer par un « . »)**</span><span class="sxs-lookup"><span data-stu-id="785bd-144">**Address (Must end with a ".")**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="785bd-145">autodiscover</span><span class="sxs-lookup"><span data-stu-id="785bd-145">autodiscover</span></span>  <br/> |<span data-ttu-id="785bd-146">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="785bd-146">autodiscover.outlook.com.</span></span>  <br/> |
    |<span data-ttu-id="785bd-147">sip</span><span class="sxs-lookup"><span data-stu-id="785bd-147">sip</span></span>  <br/> |<span data-ttu-id="785bd-148">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="785bd-148">sipdir.online.lync.com.</span></span>  <br/> |
    |<span data-ttu-id="785bd-149">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="785bd-149">lyncdiscover</span></span>  <br/> |<span data-ttu-id="785bd-150">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="785bd-150">webdir.online.lync.com.</span></span>  <br/> |
    |<span data-ttu-id="785bd-151">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="785bd-151">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="785bd-152">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="785bd-152">enterpriseregistration.windows.net.</span></span>  <br/> |
    |<span data-ttu-id="785bd-153">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="785bd-153">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="785bd-154">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="785bd-154">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> |
   
5. <span data-ttu-id="785bd-155">Sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="785bd-155">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="785bd-156">Vérifiez que l’enregistrement est correct, puis sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="785bd-156">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="785bd-157">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="785bd-157">Add a TXT record for SPF to help prevent email spam</span></span>

1. <span data-ttu-id="785bd-158">Accédez à [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) et connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="785bd-158">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="785bd-159">Sous l’en-tête **tous les domaines** , sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="785bd-159">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="785bd-160">Sous l’en-tête **txt Records (enregistrements TXT** ), cliquez sur le bouton modifier (icône de clé).</span><span class="sxs-lookup"><span data-stu-id="785bd-160">Under the **TXT records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="785bd-161">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="785bd-161">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="785bd-162">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="785bd-162">**Host**</span></span>|<span data-ttu-id="785bd-163">**Text**</span><span class="sxs-lookup"><span data-stu-id="785bd-163">**Text**</span></span>|
    |:-----|:-----|
    |@  <br/> |<span data-ttu-id="785bd-164">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="785bd-164">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> |
   
5. <span data-ttu-id="785bd-165">Sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="785bd-165">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="785bd-166">Vérifiez que l’enregistrement est correct, puis sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="785bd-166">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="785bd-167">Ajouter les deux enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="785bd-167">Add the two SRV records that are required for Office 365</span></span>

<span data-ttu-id="785bd-168">Remarque : les enregistrements SRV ne sont actuellement pas disponibles dans easyDNS’domaine plus niveau de service.</span><span class="sxs-lookup"><span data-stu-id="785bd-168">NOTE: SRV Records are currently NOT available under easyDNS' Domain Plus service level.</span></span> <span data-ttu-id="785bd-169">Vous devrez peut-être effectuer une mise à niveau vers un niveau de service supérieur avec easyDNS pour ajouter des enregistrements SRV</span><span class="sxs-lookup"><span data-stu-id="785bd-169">You may need to upgrade to a higher service level with easyDNS to add SRV records</span></span> 
  
1. <span data-ttu-id="785bd-170">Accédez à [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) et connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="785bd-170">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="785bd-171">Sous l’en-tête **tous les domaines** , sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="785bd-171">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="785bd-172">Sous l’en-tête **SRV Records (enregistrements SRV** ), cliquez sur le bouton modifier (icône de clé).</span><span class="sxs-lookup"><span data-stu-id="785bd-172">Under the **SRV records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="785bd-173">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="785bd-173">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="785bd-174">**SERVICE**</span><span class="sxs-lookup"><span data-stu-id="785bd-174">**SERVICE**</span></span>|<span data-ttu-id="785bd-175">**DEST**</span><span class="sxs-lookup"><span data-stu-id="785bd-175">**PROTO**</span></span>|<span data-ttu-id="785bd-176">**HOST (HÔTE)**</span><span class="sxs-lookup"><span data-stu-id="785bd-176">**HOST**</span></span>|<span data-ttu-id="785bd-177">**PRI**</span><span class="sxs-lookup"><span data-stu-id="785bd-177">**PRI**</span></span>|<span data-ttu-id="785bd-178">**WGT**</span><span class="sxs-lookup"><span data-stu-id="785bd-178">**WGT**</span></span>|<span data-ttu-id="785bd-179">**PORT**</span><span class="sxs-lookup"><span data-stu-id="785bd-179">**PORT**</span></span>|<span data-ttu-id="785bd-180">**CIBLE (doit se terminer par un « . »)**</span><span class="sxs-lookup"><span data-stu-id="785bd-180">**TARGET(Must end with a ".")**</span></span>|<span data-ttu-id="785bd-181">**TTL**</span><span class="sxs-lookup"><span data-stu-id="785bd-181">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="785bd-182">_sip</span><span class="sxs-lookup"><span data-stu-id="785bd-182">_sip</span></span>  <br/> |<span data-ttu-id="785bd-183">TLS</span><span class="sxs-lookup"><span data-stu-id="785bd-183">TLS</span></span>  <br/> |@  <br/> |<span data-ttu-id="785bd-184">100</span><span class="sxs-lookup"><span data-stu-id="785bd-184">100</span></span>  <br/> |<span data-ttu-id="785bd-185">0,1</span><span class="sxs-lookup"><span data-stu-id="785bd-185">1</span></span>  <br/> |<span data-ttu-id="785bd-186">443</span><span class="sxs-lookup"><span data-stu-id="785bd-186">443</span></span>  <br/> |<span data-ttu-id="785bd-187">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="785bd-187">sipdir.online.lync.com.</span></span>  <br/> |<span data-ttu-id="785bd-188">1800</span><span class="sxs-lookup"><span data-stu-id="785bd-188">1800</span></span>  <br/> |
    |<span data-ttu-id="785bd-189">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="785bd-189">_sipfederationtls</span></span>  <br/> |<span data-ttu-id="785bd-190">TCP</span><span class="sxs-lookup"><span data-stu-id="785bd-190">TCP</span></span>  <br/> |@  <br/> |<span data-ttu-id="785bd-191">100</span><span class="sxs-lookup"><span data-stu-id="785bd-191">100</span></span>  <br/> |<span data-ttu-id="785bd-192">0,1</span><span class="sxs-lookup"><span data-stu-id="785bd-192">1</span></span>  <br/> |<span data-ttu-id="785bd-193">5061</span><span class="sxs-lookup"><span data-stu-id="785bd-193">5061</span></span>  <br/> |<span data-ttu-id="785bd-194">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="785bd-194">sipfed.online.lync.com.</span></span>  <br/> |<span data-ttu-id="785bd-195">1800</span><span class="sxs-lookup"><span data-stu-id="785bd-195">1800</span></span>  <br/> |
   
5. <span data-ttu-id="785bd-196">Sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="785bd-196">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="785bd-197">Vérifiez que l’enregistrement est correct, puis sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="785bd-197">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    


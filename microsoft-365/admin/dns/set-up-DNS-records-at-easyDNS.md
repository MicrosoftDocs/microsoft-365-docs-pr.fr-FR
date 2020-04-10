---
title: Créer des enregistrements DNS sur easyDNS pour Office 365
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
search.appverid:
- MET150
- MOE150
ms.assetid: 446babfe-2e08-4cc2-bbfb-c05b854933ac
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur easyDNS pour Office 365.
ms.openlocfilehash: 9d48896de8f841863e25929a46b2f1d2e1b3ced2
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "43210551"
---
# <a name="create-dns-records-at-easydns-for-office-365"></a><span data-ttu-id="fc70d-103">Créer des enregistrements DNS sur easyDNS pour Office 365</span><span class="sxs-lookup"><span data-stu-id="fc70d-103">Create DNS records at easyDNS for Office 365</span></span>

<span data-ttu-id="fc70d-104">[Consultez le Forum aux questions sur les domaines](../setup/domains-faq.md) si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="fc70d-104">[Check the Domains FAQ ](../setup/domains-faq.md) if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="fc70d-105">Vous devrez ajouter tous les enregistrements DNS suivants sur le site Web de votre registraire pour acheminer le courrier vers Office 365, utiliser votre domaine pour teams et Skype entreprise, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="fc70d-105">You'll need to add all of the following DNS records at your registrar's website to route mail to Office 365, use your domain for Teams and Skype for Business, and so on.</span></span>
  
<span data-ttu-id="fc70d-106">Remarque : les enregistrements SRV ne sont actuellement pas disponibles dans tous les packages de service easyDNS.</span><span class="sxs-lookup"><span data-stu-id="fc70d-106">NOTE: SRV Records are currently NOT available under all easyDNS service packages.</span></span> <span data-ttu-id="fc70d-107">Vous devrez peut-être effectuer une mise à niveau vers un niveau de service supérieur avec easyDNS pour ajouter des enregistrements SRV requis pour Office 365 Skype entreprise.</span><span class="sxs-lookup"><span data-stu-id="fc70d-107">You may need to upgrade to a higher service level with easyDNS to add SRV records which are required for Office 365 Skype for Business.</span></span>
  
## <a name="verify-that-you-own-the-domain-with-a-txt-record"></a><span data-ttu-id="fc70d-108">Vérifier que vous êtes propriétaire du domaine avec un enregistrement TXT</span><span class="sxs-lookup"><span data-stu-id="fc70d-108">Verify that you own the domain with a TXT record</span></span>

1. <span data-ttu-id="fc70d-109">Accédez à [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) et connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="fc70d-109">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="fc70d-110">Sous l’en-tête **tous les domaines** , sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="fc70d-110">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="fc70d-111">Sous l’en-tête **txt Records (enregistrements TXT** ), cliquez sur le bouton modifier (icône de clé).</span><span class="sxs-lookup"><span data-stu-id="fc70d-111">Under the **TXT records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="fc70d-112">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="fc70d-112">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="fc70d-113">**Host**</span><span class="sxs-lookup"><span data-stu-id="fc70d-113">**Host**</span></span>|<span data-ttu-id="fc70d-114">**Text**</span><span class="sxs-lookup"><span data-stu-id="fc70d-114">**Text**</span></span>|
    |:-----|:-----|
    |@  <br/> |<span data-ttu-id="fc70d-115">MS = msXXXXXXXX (utilisez la valeur fournie dans la page domaines du centre d’administration)</span><span class="sxs-lookup"><span data-stu-id="fc70d-115">MS=msXXXXXXXX (Use the value provided to you on the admin center Domains page)</span></span>  <br/> |
   
5. <span data-ttu-id="fc70d-116">Sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="fc70d-116">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="fc70d-117">Vérifiez que l’enregistrement est correct, puis sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="fc70d-117">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
7. <span data-ttu-id="fc70d-118">Patientez quelques minutes avant de poursuivre, afin que l’enregistrement que vous venez de créer puisse se propager sur Internet et soit détecté par Office 365.</span><span class="sxs-lookup"><span data-stu-id="fc70d-118">Wait a few minutes before you continue, so that the record you just created can propagate across the Internet and be detected by Office 365.</span></span>
    
8. <span data-ttu-id="fc70d-119">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="fc70d-119">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
    
9. <span data-ttu-id="fc70d-120">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="fc70d-120">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
10. <span data-ttu-id="fc70d-121">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="fc70d-121">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
11. <span data-ttu-id="fc70d-122">Sur la page **installation** , sélectionnez **Démarrer l’installation.**</span><span class="sxs-lookup"><span data-stu-id="fc70d-122">On the **Setup** page, select **Start setup.**</span></span>
    
12. <span data-ttu-id="fc70d-123">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="fc70d-123">On the **Verify domain** page, select **Verify**.</span></span> 
    
## <a name="add-an-mx-record-to-route-email-to-office-365"></a><span data-ttu-id="fc70d-124">Ajouter un enregistrement MX pour acheminer le courrier électronique vers Office 365</span><span class="sxs-lookup"><span data-stu-id="fc70d-124">Add an MX record to route email to Office 365</span></span>

1. <span data-ttu-id="fc70d-125">Accédez à [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) et connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="fc70d-125">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="fc70d-126">Sous l’en-tête **tous les domaines** , sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="fc70d-126">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="fc70d-127">Sous l’en-tête **MX Records (enregistrements MX** ), cliquez sur le bouton modifier (icône de clé).</span><span class="sxs-lookup"><span data-stu-id="fc70d-127">Under the **MX records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="fc70d-128">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="fc70d-128">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="fc70d-129">**COURRIER POUR LA ZONE**</span><span class="sxs-lookup"><span data-stu-id="fc70d-129">**MAIL FOR ZONE**</span></span>|<span data-ttu-id="fc70d-130">**SERVEUR DE MESSAGERIE**</span><span class="sxs-lookup"><span data-stu-id="fc70d-130">**MAIL SERVER**</span></span>|<span data-ttu-id="fc70d-131">**PRÉFÉRENCES**</span><span class="sxs-lookup"><span data-stu-id="fc70d-131">**PREF**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="fc70d-132">\<Key\>. mail.protection.Outlook.com (obtenir votre \<valeur de clé\> de domaine à partir de la page domaines du centre d’administration)</span><span class="sxs-lookup"><span data-stu-id="fc70d-132">\<domain-key\>.mail.protection.outlook.com (Get your \<domain-key\> value from the admin center Domains page)</span></span>  <br/> |<span data-ttu-id="fc70d-133">0</span><span class="sxs-lookup"><span data-stu-id="fc70d-133">0</span></span>  <br/> |
   
2. <span data-ttu-id="fc70d-134">Si vous souhaitez enregistrer vos autres enregistrements MX à des fins de sauvegarde, copiez-les quelque part.</span><span class="sxs-lookup"><span data-stu-id="fc70d-134">If you want to save your other MX records for backup purposes, copy them down somewhere.</span></span> <span data-ttu-id="fc70d-135">Avant de poursuivre, supprimez tous les autres enregistrements MX ici.</span><span class="sxs-lookup"><span data-stu-id="fc70d-135">Before moving on, remove all other MX records here.</span></span>
    
5. <span data-ttu-id="fc70d-136">Sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="fc70d-136">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="fc70d-137">Vérifiez que l’enregistrement est correct, puis sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="fc70d-137">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
## <a name="add-the-required-cname-records"></a><span data-ttu-id="fc70d-138">Ajouter les enregistrements CNAMe requis</span><span class="sxs-lookup"><span data-stu-id="fc70d-138">Add the required CNAME records</span></span>

1. <span data-ttu-id="fc70d-139">Accédez à [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) et connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="fc70d-139">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="fc70d-140">Sous l’en-tête **tous les domaines** , sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="fc70d-140">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="fc70d-141">Sous le titre **CNAME/alias Records** , cliquez sur le bouton modifier (icône de clé).</span><span class="sxs-lookup"><span data-stu-id="fc70d-141">Under the **CNAME/Alias records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="fc70d-142">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="fc70d-142">Enter the following records in the text fields:</span></span>


    |<span data-ttu-id="fc70d-143">**HOST (HÔTE)**</span><span class="sxs-lookup"><span data-stu-id="fc70d-143">**HOST**</span></span>|<span data-ttu-id="fc70d-144">**Address (doit se terminer par un « . »)**</span><span class="sxs-lookup"><span data-stu-id="fc70d-144">**Address (Must end with a ".")**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="fc70d-145">autodiscover</span><span class="sxs-lookup"><span data-stu-id="fc70d-145">autodiscover</span></span>  <br/> |<span data-ttu-id="fc70d-146">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="fc70d-146">autodiscover.outlook.com.</span></span>  <br/> |
    |<span data-ttu-id="fc70d-147">sip</span><span class="sxs-lookup"><span data-stu-id="fc70d-147">sip</span></span>  <br/> |<span data-ttu-id="fc70d-148">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="fc70d-148">sipdir.online.lync.com.</span></span>  <br/> |
    |<span data-ttu-id="fc70d-149">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="fc70d-149">lyncdiscover</span></span>  <br/> |<span data-ttu-id="fc70d-150">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="fc70d-150">webdir.online.lync.com.</span></span>  <br/> |
    |<span data-ttu-id="fc70d-151">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="fc70d-151">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="fc70d-152">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="fc70d-152">enterpriseregistration.windows.net.</span></span>  <br/> |
    |<span data-ttu-id="fc70d-153">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="fc70d-153">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="fc70d-154">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="fc70d-154">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> |
   
5. <span data-ttu-id="fc70d-155">Sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="fc70d-155">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="fc70d-156">Vérifiez que l’enregistrement est correct, puis sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="fc70d-156">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="fc70d-157">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="fc70d-157">Add a TXT record for SPF to help prevent email spam</span></span>

1. <span data-ttu-id="fc70d-158">Accédez à [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) et connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="fc70d-158">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="fc70d-159">Sous l’en-tête **tous les domaines** , sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="fc70d-159">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="fc70d-160">Sous l’en-tête **txt Records (enregistrements TXT** ), cliquez sur le bouton modifier (icône de clé).</span><span class="sxs-lookup"><span data-stu-id="fc70d-160">Under the **TXT records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="fc70d-161">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="fc70d-161">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="fc70d-162">**Host**</span><span class="sxs-lookup"><span data-stu-id="fc70d-162">**Host**</span></span>|<span data-ttu-id="fc70d-163">**Text**</span><span class="sxs-lookup"><span data-stu-id="fc70d-163">**Text**</span></span>|
    |:-----|:-----|
    |@  <br/> |<span data-ttu-id="fc70d-164">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="fc70d-164">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> |
   
5. <span data-ttu-id="fc70d-165">Sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="fc70d-165">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="fc70d-166">Vérifiez que l’enregistrement est correct, puis sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="fc70d-166">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="fc70d-167">Ajoutez les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="fc70d-167">Add the two SRV records that are required for Office 365</span></span>

<span data-ttu-id="fc70d-168">Remarque : les enregistrements SRV ne sont actuellement pas disponibles dans easyDNS’domaine plus niveau de service.</span><span class="sxs-lookup"><span data-stu-id="fc70d-168">NOTE: SRV Records are currently NOT available under easyDNS' Domain Plus service level.</span></span> <span data-ttu-id="fc70d-169">Vous devrez peut-être effectuer une mise à niveau vers un niveau de service supérieur avec easyDNS pour ajouter des enregistrements SRV</span><span class="sxs-lookup"><span data-stu-id="fc70d-169">You may need to upgrade to a higher service level with easyDNS to add SRV records</span></span> 
  
1. <span data-ttu-id="fc70d-170">Accédez à [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) et connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="fc70d-170">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="fc70d-171">Sous l’en-tête **tous les domaines** , sélectionnez **DNS.**</span><span class="sxs-lookup"><span data-stu-id="fc70d-171">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="fc70d-172">Sous l’en-tête **SRV Records (enregistrements SRV** ), cliquez sur le bouton modifier (icône de clé).</span><span class="sxs-lookup"><span data-stu-id="fc70d-172">Under the **SRV records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="fc70d-173">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="fc70d-173">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="fc70d-174">**SERVICE**</span><span class="sxs-lookup"><span data-stu-id="fc70d-174">**SERVICE**</span></span>|<span data-ttu-id="fc70d-175">**DEST**</span><span class="sxs-lookup"><span data-stu-id="fc70d-175">**PROTO**</span></span>|<span data-ttu-id="fc70d-176">**HOST (HÔTE)**</span><span class="sxs-lookup"><span data-stu-id="fc70d-176">**HOST**</span></span>|<span data-ttu-id="fc70d-177">**PRI**</span><span class="sxs-lookup"><span data-stu-id="fc70d-177">**PRI**</span></span>|<span data-ttu-id="fc70d-178">**WGT**</span><span class="sxs-lookup"><span data-stu-id="fc70d-178">**WGT**</span></span>|<span data-ttu-id="fc70d-179">**PORT**</span><span class="sxs-lookup"><span data-stu-id="fc70d-179">**PORT**</span></span>|<span data-ttu-id="fc70d-180">**CIBLE (doit se terminer par un « . »)**</span><span class="sxs-lookup"><span data-stu-id="fc70d-180">**TARGET(Must end with a ".")**</span></span>|<span data-ttu-id="fc70d-181">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="fc70d-181">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="fc70d-182">_sip</span><span class="sxs-lookup"><span data-stu-id="fc70d-182">_sip</span></span>  <br/> |<span data-ttu-id="fc70d-183">TLS</span><span class="sxs-lookup"><span data-stu-id="fc70d-183">TLS</span></span>  <br/> |@  <br/> |<span data-ttu-id="fc70d-184">100</span><span class="sxs-lookup"><span data-stu-id="fc70d-184">100</span></span>  <br/> |<span data-ttu-id="fc70d-185">0,1</span><span class="sxs-lookup"><span data-stu-id="fc70d-185">1</span></span>  <br/> |<span data-ttu-id="fc70d-186">443</span><span class="sxs-lookup"><span data-stu-id="fc70d-186">443</span></span>  <br/> |<span data-ttu-id="fc70d-187">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="fc70d-187">sipdir.online.lync.com.</span></span>  <br/> |<span data-ttu-id="fc70d-188">1800</span><span class="sxs-lookup"><span data-stu-id="fc70d-188">1800</span></span>  <br/> |
    |<span data-ttu-id="fc70d-189">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="fc70d-189">_sipfederationtls</span></span>  <br/> |<span data-ttu-id="fc70d-190">TCP</span><span class="sxs-lookup"><span data-stu-id="fc70d-190">TCP</span></span>  <br/> |@  <br/> |<span data-ttu-id="fc70d-191">100</span><span class="sxs-lookup"><span data-stu-id="fc70d-191">100</span></span>  <br/> |<span data-ttu-id="fc70d-192">0,1</span><span class="sxs-lookup"><span data-stu-id="fc70d-192">1</span></span>  <br/> |<span data-ttu-id="fc70d-193">5061</span><span class="sxs-lookup"><span data-stu-id="fc70d-193">5061</span></span>  <br/> |<span data-ttu-id="fc70d-194">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="fc70d-194">sipfed.online.lync.com.</span></span>  <br/> |<span data-ttu-id="fc70d-195">1800</span><span class="sxs-lookup"><span data-stu-id="fc70d-195">1800</span></span>  <br/> |
   
5. <span data-ttu-id="fc70d-196">Sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="fc70d-196">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="fc70d-197">Vérifiez que l’enregistrement est correct, puis sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="fc70d-197">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    


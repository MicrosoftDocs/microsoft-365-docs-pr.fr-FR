---
title: Créer des enregistrements DNS sur easyDNS pour Microsoft
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: scotv
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
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype Entreprise Online et d’autres services via easyDNS pour Microsoft.
ms.openlocfilehash: a971a722f071ef5df9ce0fba387cfacfeb409f5b
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49656818"
---
# <a name="create-dns-records-at-easydns-for-microsoft"></a><span data-ttu-id="63e6d-103">Créer des enregistrements DNS sur easyDNS pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="63e6d-103">Create DNS records at easyDNS for Microsoft</span></span>

<span data-ttu-id="63e6d-104">[Consultez la FAQ sur ](../setup/domains-faq.yml) les domaines si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="63e6d-104">[Check the Domains FAQ ](../setup/domains-faq.yml) if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="63e6d-105">Vous devez ajouter tous les enregistrements DNS suivants sur le site web de votre bureau d’enregistrement pour router le courrier vers Microsoft, utiliser votre domaine pour Teams et Skype Entreprise, etc.</span><span class="sxs-lookup"><span data-stu-id="63e6d-105">You'll need to add all of the following DNS records at your registrar's website to route mail to Microsoft, use your domain for Teams and Skype for Business, and so on.</span></span>
  
<span data-ttu-id="63e6d-106">REMARQUE : les enregistrements SRV ne sont actuellement PAS disponibles sous tous les packages de service easyDNS.</span><span class="sxs-lookup"><span data-stu-id="63e6d-106">NOTE: SRV Records are currently NOT available under all easyDNS service packages.</span></span> <span data-ttu-id="63e6d-107">Vous devrez peut-être passer à un niveau de service supérieur avec easyDNS pour ajouter des enregistrements SRV requis pour Skype Entreprise.</span><span class="sxs-lookup"><span data-stu-id="63e6d-107">You may need to upgrade to a higher service level with easyDNS to add SRV records which are required for Skype for Business.</span></span>
  
## <a name="verify-that-you-own-the-domain-with-a-txt-record"></a><span data-ttu-id="63e6d-108">Vérifiez que vous êtes propriétaire du domaine avec un enregistrement TXT</span><span class="sxs-lookup"><span data-stu-id="63e6d-108">Verify that you own the domain with a TXT record</span></span>

1. <span data-ttu-id="63e6d-109">[https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/)Connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="63e6d-109">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="63e6d-110">Sous **l’en-tête Tous** les domaines, sélectionnez **dns.**</span><span class="sxs-lookup"><span data-stu-id="63e6d-110">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="63e6d-111">Sous le **titre Des enregistrements TXT,** sélectionnez le bouton d’édition (icône clé à clé).</span><span class="sxs-lookup"><span data-stu-id="63e6d-111">Under the **TXT records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="63e6d-112">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="63e6d-112">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="63e6d-113">**Host**</span><span class="sxs-lookup"><span data-stu-id="63e6d-113">**Host**</span></span>|<span data-ttu-id="63e6d-114">**Texte**</span><span class="sxs-lookup"><span data-stu-id="63e6d-114">**Text**</span></span>|
    |:-----|:-----|
    |@  <br/> |<span data-ttu-id="63e6d-115">MS=msXXXXXXXX (Utilisez la valeur qui vous est fournie dans la page Domaines du centre d’administration)</span><span class="sxs-lookup"><span data-stu-id="63e6d-115">MS=msXXXXXXXX (Use the value provided to you on the admin center Domains page)</span></span>  <br/> |
   
5. <span data-ttu-id="63e6d-116">Sélectionnez **NEXT**.</span><span class="sxs-lookup"><span data-stu-id="63e6d-116">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="63e6d-117">Vérifiez que l’enregistrement est correct, puis sélectionnez **CONFIRMER**.</span><span class="sxs-lookup"><span data-stu-id="63e6d-117">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
7. <span data-ttu-id="63e6d-118">Patientez quelques minutes avant de continuer, afin que l’enregistrement que vous venons de créer puisse se propager sur Internet et être détecté par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="63e6d-118">Wait a few minutes before you continue, so that the record you just created can propagate across the Internet and be detected by Microsoft.</span></span>
    
8. <span data-ttu-id="63e6d-119">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="63e6d-119">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
    
9. <span data-ttu-id="63e6d-120">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="63e6d-120">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
10. <span data-ttu-id="63e6d-121">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="63e6d-121">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
11. <span data-ttu-id="63e6d-122">Dans la page **Installation,** sélectionnez **Démarrer l’installation.**</span><span class="sxs-lookup"><span data-stu-id="63e6d-122">On the **Setup** page, select **Start setup.**</span></span>
    
12. <span data-ttu-id="63e6d-123">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="63e6d-123">On the **Verify domain** page, select **Verify**.</span></span> 
    
## <a name="add-an-mx-record-to-route-email-to-microsoft"></a><span data-ttu-id="63e6d-124">Ajouter un enregistrement MX pour router le courrier électronique vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="63e6d-124">Add an MX record to route email to Microsoft</span></span>

1. <span data-ttu-id="63e6d-125">Connectez-vous [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="63e6d-125">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="63e6d-126">Sous **l’en-tête Tous** les domaines, sélectionnez **dns.**</span><span class="sxs-lookup"><span data-stu-id="63e6d-126">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="63e6d-127">Sous **l’en-tête Des enregistrements MX,** sélectionnez le bouton d’édition (icône de clé à clé).</span><span class="sxs-lookup"><span data-stu-id="63e6d-127">Under the **MX records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="63e6d-128">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="63e6d-128">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="63e6d-129">**MAIL FOR ZONE**</span><span class="sxs-lookup"><span data-stu-id="63e6d-129">**MAIL FOR ZONE**</span></span>|<span data-ttu-id="63e6d-130">**SERVEUR DE MESSAGERIE**</span><span class="sxs-lookup"><span data-stu-id="63e6d-130">**MAIL SERVER**</span></span>|<span data-ttu-id="63e6d-131">**PREF**</span><span class="sxs-lookup"><span data-stu-id="63e6d-131">**PREF**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="63e6d-132">\<domain-key\>.mail.protection.outlook.com (Obtenir votre \<domain-key\> valeur à partir de la page Domaines du centre d’administration)</span><span class="sxs-lookup"><span data-stu-id="63e6d-132">\<domain-key\>.mail.protection.outlook.com (Get your \<domain-key\> value from the admin center Domains page)</span></span>  <br/> |<span data-ttu-id="63e6d-133">0</span><span class="sxs-lookup"><span data-stu-id="63e6d-133">0</span></span>  <br/> |
   
2. <span data-ttu-id="63e6d-134">Si vous souhaitez enregistrer vos autres enregistrements MX à des fins de sauvegarde, copiez-les quelque part.</span><span class="sxs-lookup"><span data-stu-id="63e6d-134">If you want to save your other MX records for backup purposes, copy them down somewhere.</span></span> <span data-ttu-id="63e6d-135">Avant de passer à autre chose, supprimez tous les autres enregistrements MX ici.</span><span class="sxs-lookup"><span data-stu-id="63e6d-135">Before moving on, remove all other MX records here.</span></span>
    
5. <span data-ttu-id="63e6d-136">Sélectionnez **NEXT**.</span><span class="sxs-lookup"><span data-stu-id="63e6d-136">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="63e6d-137">Vérifiez que l’enregistrement est correct, puis sélectionnez **CONFIRMER**.</span><span class="sxs-lookup"><span data-stu-id="63e6d-137">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
## <a name="add-the-required-cname-records"></a><span data-ttu-id="63e6d-138">Ajouter les enregistrements CNAME requis</span><span class="sxs-lookup"><span data-stu-id="63e6d-138">Add the required CNAME records</span></span>

1. <span data-ttu-id="63e6d-139">[https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/)Connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="63e6d-139">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="63e6d-140">Sous **l’en-tête Tous** les domaines, sélectionnez **dns.**</span><span class="sxs-lookup"><span data-stu-id="63e6d-140">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="63e6d-141">Sous **l’en-tête Enregistrements CNAME/Alias,** sélectionnez le bouton d’édition (icône clé à clé).</span><span class="sxs-lookup"><span data-stu-id="63e6d-141">Under the **CNAME/Alias records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="63e6d-142">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="63e6d-142">Enter the following records in the text fields:</span></span>


    |<span data-ttu-id="63e6d-143">**HOST (HÔTE)**</span><span class="sxs-lookup"><span data-stu-id="63e6d-143">**HOST**</span></span>|<span data-ttu-id="63e6d-144">**Adresse (doit se terminer par un « . »)**</span><span class="sxs-lookup"><span data-stu-id="63e6d-144">**Address (Must end with a ".")**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="63e6d-145">autodiscover</span><span class="sxs-lookup"><span data-stu-id="63e6d-145">autodiscover</span></span>  <br/> |<span data-ttu-id="63e6d-146">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="63e6d-146">autodiscover.outlook.com.</span></span>  <br/> |
    |<span data-ttu-id="63e6d-147">sip</span><span class="sxs-lookup"><span data-stu-id="63e6d-147">sip</span></span>  <br/> |<span data-ttu-id="63e6d-148">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="63e6d-148">sipdir.online.lync.com.</span></span>  <br/> |
    |<span data-ttu-id="63e6d-149">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="63e6d-149">lyncdiscover</span></span>  <br/> |<span data-ttu-id="63e6d-150">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="63e6d-150">webdir.online.lync.com.</span></span>  <br/> |
    |<span data-ttu-id="63e6d-151">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="63e6d-151">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="63e6d-152">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="63e6d-152">enterpriseregistration.windows.net.</span></span>  <br/> |
    |<span data-ttu-id="63e6d-153">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="63e6d-153">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="63e6d-154">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="63e6d-154">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> |
   
5. <span data-ttu-id="63e6d-155">Sélectionnez **NEXT**.</span><span class="sxs-lookup"><span data-stu-id="63e6d-155">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="63e6d-156">Vérifiez que l’enregistrement est correct, puis sélectionnez **CONFIRMER**.</span><span class="sxs-lookup"><span data-stu-id="63e6d-156">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="63e6d-157">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="63e6d-157">Add a TXT record for SPF to help prevent email spam</span></span>

1. <span data-ttu-id="63e6d-158">[https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/)Connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="63e6d-158">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="63e6d-159">Sous **l’en-tête Tous** les domaines, sélectionnez **dns.**</span><span class="sxs-lookup"><span data-stu-id="63e6d-159">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="63e6d-160">Sous le **titre Des enregistrements TXT,** sélectionnez le bouton d’édition (icône clé à clé).</span><span class="sxs-lookup"><span data-stu-id="63e6d-160">Under the **TXT records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="63e6d-161">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="63e6d-161">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="63e6d-162">**Host**</span><span class="sxs-lookup"><span data-stu-id="63e6d-162">**Host**</span></span>|<span data-ttu-id="63e6d-163">**Texte**</span><span class="sxs-lookup"><span data-stu-id="63e6d-163">**Text**</span></span>|
    |:-----|:-----|
    |@  <br/> |<span data-ttu-id="63e6d-164">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="63e6d-164">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> |
   
5. <span data-ttu-id="63e6d-165">Sélectionnez **NEXT**.</span><span class="sxs-lookup"><span data-stu-id="63e6d-165">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="63e6d-166">Vérifiez que l’enregistrement est correct, puis sélectionnez **CONFIRMER**.</span><span class="sxs-lookup"><span data-stu-id="63e6d-166">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="63e6d-167">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="63e6d-167">Add the two SRV records that are required for Microsoft</span></span>

<span data-ttu-id="63e6d-168">REMARQUE : les enregistrements SRV ne sont actuellement PAS disponibles sous le niveau de service Domain Plus de easyDNS.</span><span class="sxs-lookup"><span data-stu-id="63e6d-168">NOTE: SRV Records are currently NOT available under easyDNS' Domain Plus service level.</span></span> <span data-ttu-id="63e6d-169">Vous devrez peut-être passer à un niveau de service supérieur avec easyDNS pour ajouter des enregistrements SRV</span><span class="sxs-lookup"><span data-stu-id="63e6d-169">You may need to upgrade to a higher service level with easyDNS to add SRV records</span></span> 
  
1. <span data-ttu-id="63e6d-170">[https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/)Connectez-vous avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="63e6d-170">Go to [https://cp.easydns.com/manage/domains/](https://cp.easydns.com/manage/domains/) and log in with your credentials.</span></span> 
    
2. <span data-ttu-id="63e6d-171">Sous **l’en-tête Tous** les domaines, sélectionnez **dns.**</span><span class="sxs-lookup"><span data-stu-id="63e6d-171">Under the **all domains** heading, select **dns.**</span></span>
    
3. <span data-ttu-id="63e6d-172">Sous le **titre Des enregistrements SRV,** sélectionnez le bouton d’édition (icône de clé à clé).</span><span class="sxs-lookup"><span data-stu-id="63e6d-172">Under the **SRV records** heading, select the edit button (wrench icon).</span></span> 
    
4. <span data-ttu-id="63e6d-173">Entrez les enregistrements suivants dans les champs de texte :</span><span class="sxs-lookup"><span data-stu-id="63e6d-173">Enter the following records in the text fields:</span></span>
    
    |<span data-ttu-id="63e6d-174">**SERVICE**</span><span class="sxs-lookup"><span data-stu-id="63e6d-174">**SERVICE**</span></span>|<span data-ttu-id="63e6d-175">**PROTO**</span><span class="sxs-lookup"><span data-stu-id="63e6d-175">**PROTO**</span></span>|<span data-ttu-id="63e6d-176">**HOST (HÔTE)**</span><span class="sxs-lookup"><span data-stu-id="63e6d-176">**HOST**</span></span>|<span data-ttu-id="63e6d-177">**PRI**</span><span class="sxs-lookup"><span data-stu-id="63e6d-177">**PRI**</span></span>|<span data-ttu-id="63e6d-178">**WGT**</span><span class="sxs-lookup"><span data-stu-id="63e6d-178">**WGT**</span></span>|<span data-ttu-id="63e6d-179">**PORT**</span><span class="sxs-lookup"><span data-stu-id="63e6d-179">**PORT**</span></span>|<span data-ttu-id="63e6d-180">**TARGET(Must end with a « . »)**</span><span class="sxs-lookup"><span data-stu-id="63e6d-180">**TARGET(Must end with a ".")**</span></span>|<span data-ttu-id="63e6d-181">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="63e6d-181">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="63e6d-182">_sip</span><span class="sxs-lookup"><span data-stu-id="63e6d-182">_sip</span></span>  <br/> |<span data-ttu-id="63e6d-183">TLS</span><span class="sxs-lookup"><span data-stu-id="63e6d-183">TLS</span></span>  <br/> |@  <br/> |<span data-ttu-id="63e6d-184">100</span><span class="sxs-lookup"><span data-stu-id="63e6d-184">100</span></span>  <br/> |<span data-ttu-id="63e6d-185">1 </span><span class="sxs-lookup"><span data-stu-id="63e6d-185">1</span></span>  <br/> |<span data-ttu-id="63e6d-186">443</span><span class="sxs-lookup"><span data-stu-id="63e6d-186">443</span></span>  <br/> |<span data-ttu-id="63e6d-187">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="63e6d-187">sipdir.online.lync.com.</span></span>  <br/> |<span data-ttu-id="63e6d-188">1800</span><span class="sxs-lookup"><span data-stu-id="63e6d-188">1800</span></span>  <br/> |
    |<span data-ttu-id="63e6d-189">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="63e6d-189">_sipfederationtls</span></span>  <br/> |<span data-ttu-id="63e6d-190">TCP</span><span class="sxs-lookup"><span data-stu-id="63e6d-190">TCP</span></span>  <br/> |@  <br/> |<span data-ttu-id="63e6d-191">100</span><span class="sxs-lookup"><span data-stu-id="63e6d-191">100</span></span>  <br/> |<span data-ttu-id="63e6d-192">1 </span><span class="sxs-lookup"><span data-stu-id="63e6d-192">1</span></span>  <br/> |<span data-ttu-id="63e6d-193">5061</span><span class="sxs-lookup"><span data-stu-id="63e6d-193">5061</span></span>  <br/> |<span data-ttu-id="63e6d-194">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="63e6d-194">sipfed.online.lync.com.</span></span>  <br/> |<span data-ttu-id="63e6d-195">1800</span><span class="sxs-lookup"><span data-stu-id="63e6d-195">1800</span></span>  <br/> |
   
5. <span data-ttu-id="63e6d-196">Sélectionnez **NEXT**.</span><span class="sxs-lookup"><span data-stu-id="63e6d-196">Select **NEXT**.</span></span> 
    
6. <span data-ttu-id="63e6d-197">Vérifiez que l’enregistrement est correct, puis sélectionnez **CONFIRMER**.</span><span class="sxs-lookup"><span data-stu-id="63e6d-197">Check to make sure the record is correct, and then select **CONFIRM**.</span></span> 
    


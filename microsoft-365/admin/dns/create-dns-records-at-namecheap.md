---
title: Créer des enregistrements DNS chez Namecheap pour Microsoft
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
- BCS160
- MET150
- MOE150
ms.assetid: 54ae2002-b38e-43a1-82fa-3e49d78fda56
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype Entreprise Online et d’autres services chez Namecheap pour Microsoft.
ms.openlocfilehash: 3de8c4fb7809423848564590193e00537362c034
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50910149"
---
# <a name="create-dns-records-at-namecheap-for-microsoft"></a><span data-ttu-id="719db-103">Créer des enregistrements DNS chez Namecheap pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="719db-103">Create DNS records at Namecheap for Microsoft</span></span>

 <span data-ttu-id="719db-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="719db-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="719db-105">Si Namecheap est votre fournisseur d’hébergement DNS, suivez les étapes de cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="719db-105">If Namecheap is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="719db-106">Une fois ces enregistrements ajoutés sur Namecheap, votre domaine est installé pour fonctionner avec les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="719db-106">After you add these records at Namecheap, your domain will be set up to work with Microsoft services.</span></span>
  
> [!NOTE]
> <span data-ttu-id="719db-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="719db-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="719db-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="719db-110">Add a TXT record for verification</span></span>
<span data-ttu-id="719db-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="719db-111"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="719db-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="719db-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="719db-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="719db-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
<span data-ttu-id="719db-116">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="719db-116">Follow the steps below.</span></span>
  
1. <span data-ttu-id="719db-117">To get started, go to your domains page at Namecheap by using [this link](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f).</span><span class="sxs-lookup"><span data-stu-id="719db-117">To get started, go to your domains page at Namecheap by using [this link](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f).</span></span> <span data-ttu-id="719db-118">You’ll be prompted to Sign in and Continue.</span><span class="sxs-lookup"><span data-stu-id="719db-118">You'll be prompted to Sign in and Continue.</span></span>
    
    ![Namecheap-BP-Configure-1-1](../../media/1827f9fc-4dc9-4f9d-a392-7817c47b00b3.png)
  
2. <span data-ttu-id="719db-120">Dans la page **d’accueil,** sous **Compte,** choisissez **Liste** des domaines dans la liste liste liste.</span><span class="sxs-lookup"><span data-stu-id="719db-120">On the **Landing** page, under **Account**, choose **Domain List** from the drop-down list.</span></span> 
    
    ![Namecheap-BP-Configure-1-2](../../media/3f457d64-4589-422c-ae34-fc24b0e819eb.png)
  
3. <span data-ttu-id="719db-122">Dans la page **Liste des** domaines, recherchez le nom du domaine à modifier, puis sélectionnez **Gérer.**</span><span class="sxs-lookup"><span data-stu-id="719db-122">On the **Domain List** page, find the name of the domain that you want to edit, and then select **Manage**.</span></span>
    
    ![Namecheap-BP-Configure-1-3](../../media/fb2020d8-707c-4148-835e-304ac6244d66.png)
  
4. <span data-ttu-id="719db-124">Sélectionnez **DNS avancé.**</span><span class="sxs-lookup"><span data-stu-id="719db-124">Select **Advanced DNS**.</span></span>
    
    ![Namecheap-BP-Configure-1-4](../../media/05a4f0b9-1d27-448e-9954-2b23304c5f65.png)
  
5. <span data-ttu-id="719db-126">Dans la section **ENREGISTREMENTS HÔTES,** **sélectionnez AJOUTER UN NOUVEL ENREGISTREMENT.**</span><span class="sxs-lookup"><span data-stu-id="719db-126">In the **HOST RECORDS** section, select **ADD NEW RECORD**.</span></span>
    
    ![Namecheap-BP-Configure-1-5](../../media/8849abfe-deb6-4f6a-b56d-e69be9a28b0f.png)
  
6. <span data-ttu-id="719db-128">Dans la **baisse type,** sélectionnez **Enregistrement TXT.**</span><span class="sxs-lookup"><span data-stu-id="719db-128">In the **Type** drop-down, select **TXT Record**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="719db-129">La **drop-down** Type s’affiche automatiquement lorsque vous sélectionnez **AJOUTER UN NOUVEL ENREGISTREMENT.**</span><span class="sxs-lookup"><span data-stu-id="719db-129">The **Type** drop-down automatically appears when you select **ADD NEW RECORD**.</span></span> 
  
    ![Namecheap-BP-Verify-1-1](../../media/a5b40973-19b5-4c32-8e1b-1521aa971836.png)
  
7. <span data-ttu-id="719db-131">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="719db-131">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="719db-132">(Choisissez la **valeur TTL** dans la liste.)</span><span class="sxs-lookup"><span data-stu-id="719db-132">(Choose the **TTL** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="719db-133">**Type**</span><span class="sxs-lookup"><span data-stu-id="719db-133">**Type**</span></span>|<span data-ttu-id="719db-134">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="719db-134">**Host**</span></span>|<span data-ttu-id="719db-135">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="719db-135">**Value**</span></span>|<span data-ttu-id="719db-136">**TTL**</span><span class="sxs-lookup"><span data-stu-id="719db-136">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="719db-137">TXT</span><span class="sxs-lookup"><span data-stu-id="719db-137">TXT</span></span>  <br/> |@  <br/> |<span data-ttu-id="719db-138">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="719db-138">MS=ms *XXXXXXXX*</span></span>  <br/><span data-ttu-id="719db-139">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="719db-139">**Note:** This is an example.</span></span> <span data-ttu-id="719db-140">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="719db-140">Use your specific **Destination or Points to Address** value here, from the table.</span></span>  [<span data-ttu-id="719db-141">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="719db-141">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="719db-142">30 min</span><span class="sxs-lookup"><span data-stu-id="719db-142">30 min</span></span>  <br/> |
       
    ![Namecheap-BP-Verify-1-2](../../media/fe75c0fd-f85c-4bef-8068-edaf9779b7f1.png)
  
8. <span data-ttu-id="719db-144">Sélectionnez **le contrôle Enregistrer les modifications** (coche).</span><span class="sxs-lookup"><span data-stu-id="719db-144">Select the **Save Changes** (check mark) control.</span></span> 
    
    ![Namecheap-BP-Verify-1-3](../../media/b48d2c67-66b5-4aa4-8e59-0c764f236fac.png)
  
9. <span data-ttu-id="719db-146">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="719db-146">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="719db-147">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="719db-147">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="719db-148">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="719db-148">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="719db-149">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="719db-149">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="719db-150">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="719db-150">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="719db-151">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="719db-151">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="719db-152">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="719db-152">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
> <span data-ttu-id="719db-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="719db-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 

  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="719db-156">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="719db-156">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="719db-157"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="719db-157"><a name="BKMK_add_MX"> </a></span></span>

<span data-ttu-id="719db-158">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="719db-158">Follow the steps below.</span></span>
  
1. <span data-ttu-id="719db-159">To get started, go to your domains page at Namecheap by using [this link](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f).</span><span class="sxs-lookup"><span data-stu-id="719db-159">To get started, go to your domains page at Namecheap by using [this link](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f).</span></span> <span data-ttu-id="719db-160">You’ll be prompted to Sign in and Continue.</span><span class="sxs-lookup"><span data-stu-id="719db-160">You'll be prompted to Sign in and Continue.</span></span>
    
    ![Namecheap-BP-Configure-1-1](../../media/1827f9fc-4dc9-4f9d-a392-7817c47b00b3.png)
  
2. <span data-ttu-id="719db-162">Dans la page **d’accueil,** sous **Compte,** choisissez **Liste** des domaines dans la liste liste liste.</span><span class="sxs-lookup"><span data-stu-id="719db-162">On the **Landing** page, under **Account**, choose **Domain List** from the drop-down list.</span></span> 
    
    ![Namecheap-BP-Configure-1-2](../../media/3f457d64-4589-422c-ae34-fc24b0e819eb.png)
  
3. <span data-ttu-id="719db-164">Dans la page **Liste des** domaines, recherchez le nom du domaine à modifier, puis sélectionnez **Gérer.**</span><span class="sxs-lookup"><span data-stu-id="719db-164">On the **Domain List** page, find the name of the domain that you want to edit, and then select **Manage**.</span></span>
    
    ![Namecheap-BP-Configure-1-3](../../media/fb2020d8-707c-4148-835e-304ac6244d66.png)
  
4. <span data-ttu-id="719db-166">Sélectionnez **DNS avancé.**</span><span class="sxs-lookup"><span data-stu-id="719db-166">Select **Advanced DNS**.</span></span>
    
    ![Namecheap-BP-Configure-1-4](../../media/05a4f0b9-1d27-448e-9954-2b23304c5f65.png)
  
5. <span data-ttu-id="719db-168">Dans la section **PARAMÈTRES DU COURRIER,** sélectionnez  **MX personnalisé** dans la liste de listes de listes bas de courrier.</span><span class="sxs-lookup"><span data-stu-id="719db-168">In the **MAIL SETTINGS** section, select **Custom MX** from the **Email Forwarding** drop-down list.</span></span> 
    
    <span data-ttu-id="719db-169">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="719db-169">(You may have to scroll down.)</span></span>
    
    ![Namecheap-BP-Configure-2-1](../../media/40199e2c-42cf-4c3f-9936-3cbe5d4e81a4.png)
  
6. <span data-ttu-id="719db-171">Sélectionnez **Ajouter un nouvel enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="719db-171">Select **Add New Record**.</span></span>
    
    ![Namecheap-BP-Configure-2-2-1](../../media/8d169b81-ba48-4d51-84ea-a08fa1616457.png)
  
7. <span data-ttu-id="719db-173">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="719db-173">In the boxes for the new record, type or copy and paste the values, from the following table.</span></span>
    
    <span data-ttu-id="719db-174">(La **zone** Priorité est la zone sans nom à droite de la **zone** Valeur.</span><span class="sxs-lookup"><span data-stu-id="719db-174">(The **Priority** box is the unnamed box to the right of the **Value** box.</span></span> <span data-ttu-id="719db-175">Choisissez la **valeur TTL** dans la liste.)</span><span class="sxs-lookup"><span data-stu-id="719db-175">Choose the **TTL** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="719db-176">**Type**</span><span class="sxs-lookup"><span data-stu-id="719db-176">**Type**</span></span>|<span data-ttu-id="719db-177">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="719db-177">**Host**</span></span>|<span data-ttu-id="719db-178">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="719db-178">**Value**</span></span>|<span data-ttu-id="719db-179">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="719db-179">**Priority**</span></span>|<span data-ttu-id="719db-180">**TTL**</span><span class="sxs-lookup"><span data-stu-id="719db-180">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="719db-181">MX Record (Enregistrement MX)</span><span class="sxs-lookup"><span data-stu-id="719db-181">MX Record</span></span>  <br/> |@  <br/> |<span data-ttu-id="719db-182">\<*domain-key*\>.mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="719db-182">\<*domain-key*\>.mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="719db-183">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="719db-183">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="719db-184">**Remarque :** Obtenez votre *\<domain-key\>* depuis votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="719db-184">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>  [<span data-ttu-id="719db-185">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="719db-185">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="719db-186">0</span><span class="sxs-lookup"><span data-stu-id="719db-186">0</span></span>  <br/> <span data-ttu-id="719db-187">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](../setup/domains-faq.yml).</span><span class="sxs-lookup"><span data-stu-id="719db-187">For more information about priority, see [What is MX priority?](../setup/domains-faq.yml)</span></span> <br/> |<span data-ttu-id="719db-188">30 min</span><span class="sxs-lookup"><span data-stu-id="719db-188">30 min</span></span>  <br/> |
       
    ![Namecheap-BP-Configure-2-2-2](../../media/f3b76d62-5022-48c1-901b-8615a8571309.png)
  
8. <span data-ttu-id="719db-190">Sélectionnez **le contrôle Enregistrer les modifications** (coche).</span><span class="sxs-lookup"><span data-stu-id="719db-190">Select the **Save Changes** (check mark) control.</span></span> 
    
    ![Namecheap-BP-Configure-2-3](../../media/ef4e3112-36d2-47c8-a478-136a565dd71d.png)
  
9. <span data-ttu-id="719db-192">S'il existe d'autres enregistrements MX, utilisez le processus en deux étapes suivant pour supprimer chacun d'eux :</span><span class="sxs-lookup"><span data-stu-id="719db-192">If there are any other MX records, use the following two-step process to remove each of them:</span></span>
    
    <span data-ttu-id="719db-193">Tout d’abord, **sélectionnez l’icône Supprimer** (corbeille) de l’enregistrement à supprimer.</span><span class="sxs-lookup"><span data-stu-id="719db-193">First, select the **Delete icon** (trash can) for the record that you want to remove.</span></span> 
    
    ![Namecheap-BP-Configure-2-4](../../media/7a7a751f-29c2-495f-8f55-98ca37ce555a.png)
  
    <span data-ttu-id="719db-195">Ensuite, **sélectionnez Oui** pour confirmer la suppression.</span><span class="sxs-lookup"><span data-stu-id="719db-195">Second, select **Yes** to confirm the deletion.</span></span> 
    
    ![Namecheap-BP-Configure-2-5](../../media/85ebc0c7-8787-43ee-9e7b-647375b3345c.png)
  
    <span data-ttu-id="719db-197">Supprimez tous les enregistrements MX à l’exception de celui que vous avez ajouté précédemment dans cette procédure.</span><span class="sxs-lookup"><span data-stu-id="719db-197">Remove all MX records except for the one that you added earlier in this procedure.</span></span>

  
## <a name="add-the-six-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="719db-198">Ajouter les six enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="719db-198">Add the six CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="719db-199"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="719db-199"><a name="BKMK_add_CNAME"> </a></span></span>

<span data-ttu-id="719db-200">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="719db-200">Follow the steps below.</span></span>
  
1. <span data-ttu-id="719db-201">To get started, go to your domains page at Namecheap by using [this link](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f).</span><span class="sxs-lookup"><span data-stu-id="719db-201">To get started, go to your domains page at Namecheap by using [this link](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f).</span></span> <span data-ttu-id="719db-202">You’ll be prompted to Sign in and Continue.</span><span class="sxs-lookup"><span data-stu-id="719db-202">You'll be prompted to Sign in and Continue.</span></span>
    
    ![Namecheap-BP-Configure-1-1](../../media/1827f9fc-4dc9-4f9d-a392-7817c47b00b3.png)
  
2. <span data-ttu-id="719db-204">Dans la page **d’accueil,** sous **Compte,** choisissez **Liste** des domaines dans la liste liste liste.</span><span class="sxs-lookup"><span data-stu-id="719db-204">On the **Landing** page, under **Account**, choose **Domain List** from the drop-down list.</span></span> 
    
    ![Namecheap-BP-Configure-1-2](../../media/3f457d64-4589-422c-ae34-fc24b0e819eb.png)
  
3. <span data-ttu-id="719db-206">Dans la page **Liste des** domaines, recherchez le nom du domaine à modifier, puis sélectionnez **Gérer.**</span><span class="sxs-lookup"><span data-stu-id="719db-206">On the **Domain List** page, find the name of the domain that you want to edit, and then select **Manage**.</span></span>
    
    ![Namecheap-BP-Configure-1-3](../../media/fb2020d8-707c-4148-835e-304ac6244d66.png)
  
4. <span data-ttu-id="719db-208">Sélectionnez **DNS avancé.**</span><span class="sxs-lookup"><span data-stu-id="719db-208">Select **Advanced DNS**.</span></span>
    
    ![Namecheap-BP-Configure-1-4](../../media/05a4f0b9-1d27-448e-9954-2b23304c5f65.png)
  
5. <span data-ttu-id="719db-210">Dans la section **ENREGISTREMENTS HÔTES,** **sélectionnez AJOUTER UN NOUVEL ENREGISTREMENT.**</span><span class="sxs-lookup"><span data-stu-id="719db-210">In the **HOST RECORDS** section, select **ADD NEW RECORD**.</span></span>
    
    ![Namecheap-BP-Configure-1-5](../../media/8849abfe-deb6-4f6a-b56d-e69be9a28b0f.png)
  
6. <span data-ttu-id="719db-212">Dans la **boîte de** drop-down Type, sélectionnez **Enregistrement CNAME.**</span><span class="sxs-lookup"><span data-stu-id="719db-212">In the **Type** drop-down, select **CNAME Record**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="719db-213">La **drop-down** Type s’affiche automatiquement lorsque vous sélectionnez **AJOUTER UN NOUVEL ENREGISTREMENT.**</span><span class="sxs-lookup"><span data-stu-id="719db-213">The **Type** drop-down automatically appears when you select **ADD NEW RECORD**.</span></span> 
  
    ![Namecheap-BP-Configure-3-1](../../media/0898f3b2-06ab-4364-a86a-a603a25b39f4.png)
  
7. <span data-ttu-id="719db-215">Dans les zones vides du nouvel enregistrement, sélectionnez le **Type d'enregistrement** **CNAME**, puis tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="719db-215">In the empty boxes for the new record, select **CNAME** for the **Record Type**, and then type or copy and paste the values from the first row in the following table.</span></span>
    
    |<span data-ttu-id="719db-216">**Type**</span><span class="sxs-lookup"><span data-stu-id="719db-216">**Type**</span></span>|<span data-ttu-id="719db-217">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="719db-217">**Host**</span></span>|<span data-ttu-id="719db-218">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="719db-218">**Value**</span></span>|<span data-ttu-id="719db-219">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="719db-219">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="719db-220">CNAME</span><span class="sxs-lookup"><span data-stu-id="719db-220">CNAME</span></span>  <br/> |<span data-ttu-id="719db-221">autodiscover</span><span class="sxs-lookup"><span data-stu-id="719db-221">autodiscover</span></span>  <br/> |<span data-ttu-id="719db-222">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="719db-222">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="719db-223">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="719db-223">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="719db-224">3600</span><span class="sxs-lookup"><span data-stu-id="719db-224">3600</span></span>  <br/> |
    |<span data-ttu-id="719db-225">CNAME</span><span class="sxs-lookup"><span data-stu-id="719db-225">CNAME</span></span>  <br/> |<span data-ttu-id="719db-226">sip</span><span class="sxs-lookup"><span data-stu-id="719db-226">sip</span></span>  <br/> |<span data-ttu-id="719db-227">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="719db-227">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="719db-228">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="719db-228">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="719db-229">3600</span><span class="sxs-lookup"><span data-stu-id="719db-229">3600</span></span>  <br/> |
    |<span data-ttu-id="719db-230">CNAME</span><span class="sxs-lookup"><span data-stu-id="719db-230">CNAME</span></span>  <br/> |<span data-ttu-id="719db-231">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="719db-231">lyncdiscover</span></span>  <br/> |<span data-ttu-id="719db-232">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="719db-232">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="719db-233">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="719db-233">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="719db-234">3600</span><span class="sxs-lookup"><span data-stu-id="719db-234">3600</span></span>  <br/> |
    |<span data-ttu-id="719db-235">CNAME</span><span class="sxs-lookup"><span data-stu-id="719db-235">CNAME</span></span>  <br/> |<span data-ttu-id="719db-236">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="719db-236">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="719db-237">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="719db-237">enterpriseregistration.windows.net.</span></span>  <br/> <span data-ttu-id="719db-238">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="719db-238">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="719db-239">3600</span><span class="sxs-lookup"><span data-stu-id="719db-239">3600</span></span>  <br/> |
    |<span data-ttu-id="719db-240">CNAME</span><span class="sxs-lookup"><span data-stu-id="719db-240">CNAME</span></span>  <br/> |<span data-ttu-id="719db-241">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="719db-241">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="719db-242">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="719db-242">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> <span data-ttu-id="719db-243">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="719db-243">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="719db-244">3600</span><span class="sxs-lookup"><span data-stu-id="719db-244">3600</span></span>  <br/> |
       
    ![Namecheap-BP-Configure-3-2](../../media/f79c5679-34eb-4544-8517-caa2e8a4111a.png)
  
8. <span data-ttu-id="719db-246">Sélectionnez **le contrôle Enregistrer les modifications** (coche).</span><span class="sxs-lookup"><span data-stu-id="719db-246">Select the **Save Changes** (check mark) control.</span></span> 
    
    ![Namecheap-BP-Configure-3-3](../../media/91a5cce4-ca41-41ec-b976-aafe681a4d68.png)
  
9. <span data-ttu-id="719db-248">En utilisant les quatre étapes précédentes et les valeurs des cinq autres lignes du tableau, ajoutez chacun des cinq autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="719db-248">Using the preceding four steps and the values from the other five rows in the table, add each of the other five CNAME records.</span></span>

  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="719db-249">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="719db-249">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="719db-250"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="719db-250"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="719db-251">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="719db-251">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="719db-252">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="719db-252">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="719db-253">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="719db-253">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="719db-254">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel de manière à n’avoir *qu’un seul* enregistrement SPF incluant les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="719db-254">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 

<span data-ttu-id="719db-255">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="719db-255">Follow the steps below.</span></span>
  
1. <span data-ttu-id="719db-256">To get started, go to your domains page at Namecheap by using [this link](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f).</span><span class="sxs-lookup"><span data-stu-id="719db-256">To get started, go to your domains page at Namecheap by using [this link](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f).</span></span> <span data-ttu-id="719db-257">You’ll be prompted to Sign in and Continue.</span><span class="sxs-lookup"><span data-stu-id="719db-257">You'll be prompted to Sign in and Continue.</span></span>
    
2. <span data-ttu-id="719db-258">Dans la page **d’accueil,** sous **Compte,** choisissez **Liste** des domaines dans la liste liste liste.</span><span class="sxs-lookup"><span data-stu-id="719db-258">On the **Landing** page, under **Account**, choose **Domain List** from the drop-down list.</span></span> 
    
    ![Namecheap-BP-Configure-1-2](../../media/3f457d64-4589-422c-ae34-fc24b0e819eb.png)
  
3. <span data-ttu-id="719db-260">Dans la page **Liste des** domaines, recherchez le nom du domaine à modifier, puis sélectionnez **Gérer.**</span><span class="sxs-lookup"><span data-stu-id="719db-260">On the **Domain List** page, find the name of the domain that you want to edit and then select **Manage**.</span></span>
    
    ![Namecheap-BP-Configure-1-3](../../media/fb2020d8-707c-4148-835e-304ac6244d66.png)
  
4. <span data-ttu-id="719db-262">Sélectionnez **DNS avancé.**</span><span class="sxs-lookup"><span data-stu-id="719db-262">Select **Advanced DNS**.</span></span>
    
    ![Namecheap-BP-Configure-1-4](../../media/05a4f0b9-1d27-448e-9954-2b23304c5f65.png)
  
5. <span data-ttu-id="719db-264">Dans la section **ENREGISTREMENTS HÔTES,** **sélectionnez AJOUTER UN NOUVEL ENREGISTREMENT.**</span><span class="sxs-lookup"><span data-stu-id="719db-264">In the **HOST RECORDS** section, select **ADD NEW RECORD**.</span></span>
    
    ![Namecheap-BP-Configure-1-5](../../media/8849abfe-deb6-4f6a-b56d-e69be9a28b0f.png)
  
6. <span data-ttu-id="719db-266">Dans la **baisse type,** sélectionnez **Enregistrement TXT.**</span><span class="sxs-lookup"><span data-stu-id="719db-266">In the **Type** drop-down, select **TXT Record**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="719db-267">La **drop-down** Type s’affiche automatiquement lorsque vous sélectionnez **AJOUTER UN NOUVEL ENREGISTREMENT.**</span><span class="sxs-lookup"><span data-stu-id="719db-267">The **Type** drop-down automatically appears when you select **ADD NEW RECORD**.</span></span> 
  
    ![Namecheap-BP-Configure-4-1](../../media/c5d1fddb-28b5-48ec-91c9-3e5d3955ac80.png)
  
7. <span data-ttu-id="719db-269">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs suivantes du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="719db-269">In the boxes for the new record, type or copy and paste the following values from the following table.</span></span>
    
    <span data-ttu-id="719db-270">(Choisissez la **valeur TTL** dans la liste.)</span><span class="sxs-lookup"><span data-stu-id="719db-270">(Choose the **TTL** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="719db-271">**Type**</span><span class="sxs-lookup"><span data-stu-id="719db-271">**Type**</span></span>|<span data-ttu-id="719db-272">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="719db-272">**Host**</span></span>|<span data-ttu-id="719db-273">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="719db-273">**Value**</span></span>|<span data-ttu-id="719db-274">**TTL**</span><span class="sxs-lookup"><span data-stu-id="719db-274">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="719db-275">TXT</span><span class="sxs-lookup"><span data-stu-id="719db-275">TXT</span></span>  <br/> |@  <br/> |<span data-ttu-id="719db-276">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="719db-276">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="719db-277">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="719db-277">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |<span data-ttu-id="719db-278">30 min</span><span class="sxs-lookup"><span data-stu-id="719db-278">30 min</span></span>  <br/> |
       
    ![Namecheap-BP-Configure-4-2](../../media/ea0829f1-990b-424b-b26e-9859468318dd.png)
  
8. <span data-ttu-id="719db-280">Sélectionnez **le contrôle Enregistrer les modifications** (coche).</span><span class="sxs-lookup"><span data-stu-id="719db-280">Select the **Save Changes** (check mark) control.</span></span> 
    
    ![Namecheap-BP-Configure-4-3](../../media/f2846c36-ace3-43d8-be5d-a65e2c267619.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="719db-282">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="719db-282">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="719db-283"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="719db-283"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="719db-284">To get started, go to your domains page at Namecheap by using [this link](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f).</span><span class="sxs-lookup"><span data-stu-id="719db-284">To get started, go to your domains page at Namecheap by using [this link](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f).</span></span> <span data-ttu-id="719db-285">You'll be prompted to sign in.</span><span class="sxs-lookup"><span data-stu-id="719db-285">You'll be prompted to sign in.</span></span>
    
    ![Namecheap-BP-Configure-1-1](../../media/1827f9fc-4dc9-4f9d-a392-7817c47b00b3.png)
  
2. <span data-ttu-id="719db-287">Dans la page **d’accueil,** sous **Compte,** choisissez **Liste** des domaines dans la liste liste liste.</span><span class="sxs-lookup"><span data-stu-id="719db-287">On the **Landing** page, under **Account**, choose **Domain List** from the drop-down list.</span></span> 
    
    ![Namecheap-BP-Configure-1-2](../../media/3f457d64-4589-422c-ae34-fc24b0e819eb.png)
  
3. <span data-ttu-id="719db-289">Dans la page **Liste des** domaines, recherchez le nom du domaine à modifier, puis sélectionnez **Gérer.**</span><span class="sxs-lookup"><span data-stu-id="719db-289">On the **Domain List** page, find the name of the domain that you want to edit and then select **Manage**.</span></span>
    
    ![Namecheap-BP-Configure-1-3](../../media/fb2020d8-707c-4148-835e-304ac6244d66.png)
  
4. <span data-ttu-id="719db-291">Sélectionnez **DNS avancé.**</span><span class="sxs-lookup"><span data-stu-id="719db-291">Select **Advanced DNS**.</span></span>
    
    ![Namecheap-BP-Configure-1-4](../../media/05a4f0b9-1d27-448e-9954-2b23304c5f65.png)
  
5. <span data-ttu-id="719db-293">Dans la section **ENREGISTREMENTS HÔTES,** **sélectionnez AJOUTER UN NOUVEL ENREGISTREMENT.**</span><span class="sxs-lookup"><span data-stu-id="719db-293">In the **HOST RECORDS** section, select **ADD NEW RECORD**.</span></span>
    
    ![Namecheap-BP-Configure-1-5](../../media/8849abfe-deb6-4f6a-b56d-e69be9a28b0f.png)
  
6. <span data-ttu-id="719db-295">Dans la **drop-down Type,** sélectionnez **Enregistrement SRV.**</span><span class="sxs-lookup"><span data-stu-id="719db-295">In the **Type** drop-down, select **SRV Record**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="719db-296">La **drop-down** Type s’affiche automatiquement lorsque vous sélectionnez **AJOUTER UN NOUVEL ENREGISTREMENT.**</span><span class="sxs-lookup"><span data-stu-id="719db-296">The **Type** drop-down automatically appears when you select **ADD NEW RECORD**.</span></span> 
  
    ![Namecheap-BP-Configure-5-1](../../media/fd55cd7c-2243-4de1-8d39-2c3f7ea3ae51.png)
  
7. <span data-ttu-id="719db-298">Dans les zones vides des nouveaux enregistrements, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="719db-298">In the empty boxes for the new records, type or copy and paste the values from the first row in the following table.</span></span>
    
    |<span data-ttu-id="719db-299">**Service**</span><span class="sxs-lookup"><span data-stu-id="719db-299">**Service**</span></span>|<span data-ttu-id="719db-300">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="719db-300">**Protocol**</span></span>|<span data-ttu-id="719db-301">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="719db-301">**Priority**</span></span>|<span data-ttu-id="719db-302">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="719db-302">**Weight**</span></span>|<span data-ttu-id="719db-303">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="719db-303">**Port**</span></span>|<span data-ttu-id="719db-304">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="719db-304">**Target**</span></span>|<span data-ttu-id="719db-305">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="719db-305">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="719db-306">_sip</span><span class="sxs-lookup"><span data-stu-id="719db-306">_sip</span></span>  <br/> |<span data-ttu-id="719db-307">_tls</span><span class="sxs-lookup"><span data-stu-id="719db-307">_tls</span></span>  <br/> |<span data-ttu-id="719db-308">100</span><span class="sxs-lookup"><span data-stu-id="719db-308">100</span></span>  <br/> |<span data-ttu-id="719db-309">1</span><span class="sxs-lookup"><span data-stu-id="719db-309">1</span></span>  <br/> |<span data-ttu-id="719db-310">443</span><span class="sxs-lookup"><span data-stu-id="719db-310">443</span></span>  <br/> |<span data-ttu-id="719db-311">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="719db-311">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="719db-312">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="719db-312">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="719db-313">30 min</span><span class="sxs-lookup"><span data-stu-id="719db-313">30 min</span></span>  <br/> |
    |<span data-ttu-id="719db-314">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="719db-314">_sipfederationtls</span></span>  <br/> |<span data-ttu-id="719db-315">_tcp</span><span class="sxs-lookup"><span data-stu-id="719db-315">_tcp</span></span>  <br/> |<span data-ttu-id="719db-316">100</span><span class="sxs-lookup"><span data-stu-id="719db-316">100</span></span>  <br/> |<span data-ttu-id="719db-317">1</span><span class="sxs-lookup"><span data-stu-id="719db-317">1</span></span>  <br/> |<span data-ttu-id="719db-318">5061</span><span class="sxs-lookup"><span data-stu-id="719db-318">5061</span></span>  <br/> |<span data-ttu-id="719db-319">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="719db-319">sipfed.online.lync.com.</span></span>  <br/> <span data-ttu-id="719db-320">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="719db-320">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="719db-321">30 min</span><span class="sxs-lookup"><span data-stu-id="719db-321">30 min</span></span>  <br/> |
       
    ![Namecheap-BP-Configure-5-2](../../media/ff9566ea-0096-4b7f-873c-027080a23b56.png)
  
8. <span data-ttu-id="719db-323">Sélectionnez **le contrôle Enregistrer les modifications** (coche).</span><span class="sxs-lookup"><span data-stu-id="719db-323">Select the **Save Changes** (check mark) control.</span></span> 
    
    ![Namecheap-BP-Configure-5-3](../../media/48a8dee4-c66d-449d-8759-9e9784c82b13.png)
  
9. <span data-ttu-id="719db-325">En utilisant les quatre étapes précédentes et les valeurs de la deuxième ligne du tableau, ajoutez l’autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="719db-325">Using the preceding four steps and the values from the second row in the table, add the other SRV record.</span></span>
    
> [!NOTE]
> <span data-ttu-id="719db-p114">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="719db-p114">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  


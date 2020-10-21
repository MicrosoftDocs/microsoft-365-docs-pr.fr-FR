---
title: Modifier les serveurs de noms pour configurer Microsoft avec NameCheap
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
ms.assetid: 84f467f6-28cf-40f0-94d0-a2a27ddfc2e7
description: 'Apprenez à configurer votre domaine personnalisé Microsoft avec NameCheap si vous souhaitez que Microsoft gère vos enregistrements DNS. '
ms.openlocfilehash: e305abb7768b286dbd24336c1dab39d919f9a0ac
ms.sourcegitcommit: 628f195cbe3c00910f7350d8b09997a675dde989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "48646450"
---
# <a name="change-nameservers-to-set-up-microsoft-with-namecheap"></a><span data-ttu-id="c93e3-103">Modifier les serveurs de noms pour configurer Microsoft avec NameCheap</span><span class="sxs-lookup"><span data-stu-id="c93e3-103">Change nameservers to set up Microsoft with Namecheap</span></span>

 <span data-ttu-id="c93e3-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="c93e3-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span>
  
<span data-ttu-id="c93e3-105">Suivez ces instructions si vous voulez que Microsoft gère vos enregistrements DNS pour vous.</span><span class="sxs-lookup"><span data-stu-id="c93e3-105">Follow these instructions if you want Microsoft to manage your DNS records for you.</span></span> <span data-ttu-id="c93e3-106">(Si vous préférez, vous pouvez [gérer tous vos enregistrements DNS Microsoft sur NameCheap](create-dns-records-at-namecheap.md).)</span><span class="sxs-lookup"><span data-stu-id="c93e3-106">(If you prefer, you can [manage all your Microsoft DNS records at Namecheap](create-dns-records-at-namecheap.md).)</span></span>
  
    
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="c93e3-107">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="c93e3-107">Add a TXT record for verification</span></span>

1. <span data-ttu-id="c93e3-108">Pour commencer, accédez à la page de vos domaines sur NameCheap à l’aide de [ce lien](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f).</span><span class="sxs-lookup"><span data-stu-id="c93e3-108">To get started, go to your domains page at Namecheap by using [this link](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f).</span></span> <span data-ttu-id="c93e3-109">Vous serez invité à vous connecter et à continuer.</span><span class="sxs-lookup"><span data-stu-id="c93e3-109">You'll be prompted to Sign in and Continue.</span></span>
    
    ![NameCheap-BP-configure-1-1](../../media/1827f9fc-4dc9-4f9d-a392-7817c47b00b3.png)
  
2. <span data-ttu-id="c93e3-111">Sur la page d' **Accueil** , sous **compte**, sélectionnez **liste de domaines** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="c93e3-111">On the **Landing** page, under **Account**, choose **Domain List** from the drop-down list.</span></span> 
    
    ![NameCheap-BP-configure-1-2](../../media/3f457d64-4589-422c-ae34-fc24b0e819eb.png)
  
3. <span data-ttu-id="c93e3-113">Dans la page **liste des domaines** , recherchez le nom du domaine que vous souhaitez modifier, puis sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="c93e3-113">On the **Domain List** page, find the name of the domain that you want to edit, and then select **Manage**.</span></span>
    
    ![NameCheap-BP-configure-1-3](../../media/fb2020d8-707c-4148-835e-304ac6244d66.png)
  
4. <span data-ttu-id="c93e3-115">Sélectionnez **DNS avancé**.</span><span class="sxs-lookup"><span data-stu-id="c93e3-115">Select **Advanced DNS**.</span></span>
    
    ![NameCheap-BP-configure-1-4](../../media/05a4f0b9-1d27-448e-9954-2b23304c5f65.png)
  
5. <span data-ttu-id="c93e3-117">Dans la section **Host Records (enregistrements d’hôte** ), sélectionnez **Add New Record (ajouter un nouvel enregistrement**).</span><span class="sxs-lookup"><span data-stu-id="c93e3-117">In the **HOST RECORDS** section, select **ADD NEW RECORD**.</span></span>
    
    ![NameCheap-BP-configure-1-5](../../media/8849abfe-deb6-4f6a-b56d-e69be9a28b0f.png)
  
6. <span data-ttu-id="c93e3-119">Dans la liste déroulante **type** , sélectionnez **enregistrement txt**.</span><span class="sxs-lookup"><span data-stu-id="c93e3-119">In the **Type** drop-down, select **TXT Record**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="c93e3-120">La liste déroulante **type** s’affiche automatiquement lorsque vous sélectionnez **Ajouter un nouvel enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="c93e3-120">The **Type** drop-down automatically appears when you select **ADD NEW RECORD**.</span></span>
  
    ![NameCheap-BP-Verify-1-1](../../media/a5b40973-19b5-4c32-8e1b-1521aa971836.png)
  
7. <span data-ttu-id="c93e3-122">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c93e3-122">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="c93e3-123">(Choisissez la valeur **TTL (durée de vie** ) dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="c93e3-123">(Choose the **TTL** value from the drop-down list.)</span></span> 
    
|<span data-ttu-id="c93e3-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="c93e3-124">**Type**</span></span>|<span data-ttu-id="c93e3-125">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="c93e3-125">**Host**</span></span>|<span data-ttu-id="c93e3-126">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c93e3-126">**Value**</span></span>|<span data-ttu-id="c93e3-127">**TTL**</span><span class="sxs-lookup"><span data-stu-id="c93e3-127">**TTL**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c93e3-128">TXT</span><span class="sxs-lookup"><span data-stu-id="c93e3-128">TXT</span></span>  <br/> |@  <br/> |<span data-ttu-id="c93e3-129">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="c93e3-129">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="c93e3-130">**Remarque**: Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="c93e3-130">**Note**: This is an example.</span></span> <span data-ttu-id="c93e3-131">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="c93e3-131">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="c93e3-132">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="c93e3-132">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="c93e3-133">30 min</span><span class="sxs-lookup"><span data-stu-id="c93e3-133">30 min</span></span>  <br/> |
   
   ![NameCheap-BP-Verify-1-2](../../media/fe75c0fd-f85c-4bef-8068-edaf9779b7f1.png)
  
8. <span data-ttu-id="c93e3-135">Sélectionnez le contrôle **enregistrer les modifications** (coche).</span><span class="sxs-lookup"><span data-stu-id="c93e3-135">Select the **Save Changes** (check mark) control.</span></span> 
    
    ![NameCheap-BP-Verify-1-3](../../media/b48d2c67-66b5-4aa4-8e59-0c764f236fac.png)
  
9. <span data-ttu-id="c93e3-137">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="c93e3-137">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="c93e3-138">À présent que vous avez ajouté l’enregistrement sur le site de votre bureau d’enregistrement de domaines, vous allez retourner à Microsoft et demander une recherche pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c93e3-138">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request a search for the record.</span></span>
  
<span data-ttu-id="c93e3-139">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="c93e3-139">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="c93e3-140">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="c93e3-140">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="c93e3-141">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="c93e3-141">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="c93e3-142">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="c93e3-142">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="c93e3-143">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="c93e3-143">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="c93e3-p104">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="c93e3-p104">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="c93e3-147">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="c93e3-147">Change your domain's nameserver (NS) records</span></span>

<span data-ttu-id="c93e3-148">Pour terminer la configuration de votre domaine avec Microsoft, vous devez modifier les enregistrements de serveur de noms de votre domaine au niveau de votre bureau d’enregistrement de domaines afin de pointer vers les serveurs de noms principaux et secondaires Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c93e3-148">To complete setting up your domain with Microsoft, you change your domain's NS records at your domain registrar to point to the Microsoft primary and secondary name servers.</span></span> <span data-ttu-id="c93e3-149">Cela permet à Microsoft de mettre à jour les enregistrements DNS du domaine pour vous.</span><span class="sxs-lookup"><span data-stu-id="c93e3-149">This sets up Microsoft to update the domain's DNS records for you.</span></span> <span data-ttu-id="c93e3-150">Pour finaliser la configuration, nous ajouterons tous les enregistrements de façon à ce que vous puissiez utiliser la messagerie, Skype Entreprise Online et votre site web public avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="c93e3-150">We'll add all records so that email, Skype for Business Online, and your public website work with your domain, and you'll be all set.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="c93e3-151">Lorsque vous modifiez les enregistrements de serveur de noms de votre domaine pour qu’ils pointent vers les serveurs de noms Microsoft, tous les services actuellement associés à votre domaine sont affectés.</span><span class="sxs-lookup"><span data-stu-id="c93e3-151">When you change your domain's NS records to point to the Microsoft name servers, all the services that are currently associated with your domain are affected.</span></span> <span data-ttu-id="c93e3-152">Par exemple, tous les messages électroniques envoyés à votre domaine (par exemple, rob@ *your_domain*  . com) débuteront à Microsoft après avoir effectué cette modification.</span><span class="sxs-lookup"><span data-stu-id="c93e3-152">For example, all email sent to your domain (like rob@ *your_domain*  .com) will start coming to Microsoft after you make this change.</span></span> 
  
> [!IMPORTANT]
>  <span data-ttu-id="c93e3-153">Une fois les étapes décrites dans cette section accomplies, les  *seuls*  serveurs de noms qui doivent être répertoriés sont les quatre suivants : >  ns1.bdm.microsoftonline.com >  ns2.bdm.microsoftonline.com >  ns3.bdm.microsoftonline.com >  ns4.bdm.microsoftonline.com >  La procédure suivante décrit comment supprimer tout autre serveur de noms indésirable de la liste, et y ajouter les serveurs de noms  *corrects*  qui n'y figurent pas encore.</span><span class="sxs-lookup"><span data-stu-id="c93e3-153">When you have completed the steps in this section, the  *only*  nameservers that should be listed are these four: >  ns1.bdm.microsoftonline.com >  ns2.bdm.microsoftonline.com >  ns3.bdm.microsoftonline.com >  ns4.bdm.microsoftonline.com >  The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the  *correct*  nameservers if they are not already in the list.</span></span> 
  
1. <span data-ttu-id="c93e3-154">Pour commencer, accédez à la page de vos domaines sur NameCheap à l’aide de [ce lien](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f).</span><span class="sxs-lookup"><span data-stu-id="c93e3-154">To get started, go to your domains page at Namecheap by using [this link](https://www.namecheap.com/myaccount/login.aspx?ReturnUrl=%2f).</span></span> <span data-ttu-id="c93e3-155">Vous serez invité à vous connecter et à continuer.</span><span class="sxs-lookup"><span data-stu-id="c93e3-155">You'll be prompted to Sign in and Continue.</span></span>
    
    ![NameCheap-BP-configure-1-1](../../media/1827f9fc-4dc9-4f9d-a392-7817c47b00b3.png)
  
2. <span data-ttu-id="c93e3-157">Sur la page d' **Accueil** , sous **compte**, sélectionnez **liste de domaines** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="c93e3-157">On the **Landing** page, under **Account**, choose **Domain List** from the drop-down list.</span></span> 
    
    ![NameCheap-BP-configure-1-2](../../media/3f457d64-4589-422c-ae34-fc24b0e819eb.png)
  
3. <span data-ttu-id="c93e3-159">Dans la page **liste des domaines** , recherchez le nom du domaine que vous souhaitez modifier, puis sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="c93e3-159">On the **Domain List** page, find the name of the domain that you want to edit, and then select **Manage**.</span></span>
    
    ![NameCheap-BP-configure-1-3](../../media/fb2020d8-707c-4148-835e-304ac6244d66.png)
  
4. <span data-ttu-id="c93e3-161">Sélectionnez **domaine**.</span><span class="sxs-lookup"><span data-stu-id="c93e3-161">Select **Domain**.</span></span>
    
    ![NameCheap-BP-redelegate-1-1](../../media/59588406-794e-4ae4-8526-35e3111b5791.png)
  
5. <span data-ttu-id="c93e3-163">Recherchez la section serveurs de **noms** , puis sélectionnez **personnalisée** dans la liste déroulante **NameCheap par défaut** .</span><span class="sxs-lookup"><span data-stu-id="c93e3-163">Find the **NAMESERVERS** section, and then select **Custom** from the **Namecheap Default** drop-down list.</span></span> 
    
    ![NameCheap-BP-redelegate-1-2](../../media/7df56295-fdb3-472f-9442-13f780c2c93e.png)
  
6. <span data-ttu-id="c93e3-165">Selon qu’il y a déjà ou non des serveurs de noms répertoriés dans la page qui s’affiche maintenant, passez à l’une des deux procédures suivantes.</span><span class="sxs-lookup"><span data-stu-id="c93e3-165">Depending on whether or not there are already nameservers listed on the page that is displayed now, continue to one of the two following procedures.</span></span>
    
### <a name="if-there-are-no-nameservers-already-listed"></a><span data-ttu-id="c93e3-166">Si AUCUN serveur de noms n'est encore répertorié</span><span class="sxs-lookup"><span data-stu-id="c93e3-166">If there are NO nameservers already listed</span></span>
<span data-ttu-id="c93e3-167"><a name="BKMK_ProcedureWithOUT"> </a></span><span class="sxs-lookup"><span data-stu-id="c93e3-167"><a name="BKMK_ProcedureWithOUT"> </a></span></span>

1. <span data-ttu-id="c93e3-168">Sélectionnez **Ajouter** un serveur de noms à deux reprises pour ajouter deux nouvelles lignes.</span><span class="sxs-lookup"><span data-stu-id="c93e3-168">Select **ADD NAMESERVER** twice to add two new rows.</span></span>
    
    ![NameCheap-BP-redelegate-1-3-1](../../media/e8816bf5-bb59-49d5-bfca-43e502242dc3.png)
  
2. <span data-ttu-id="c93e3-170">Dans les zones serveur de **noms** , tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c93e3-170">In the **Nameserver** boxes, type or copy and paste the values from the following table.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="c93e3-171">**Nameserver 1 (Serveur de noms 1)**</span><span class="sxs-lookup"><span data-stu-id="c93e3-171">**Nameserver 1**</span></span> <br/> |<span data-ttu-id="c93e3-172">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="c93e3-172">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="c93e3-173">**Nameserver 2 (Serveur de noms 2)**</span><span class="sxs-lookup"><span data-stu-id="c93e3-173">**Nameserver 2**</span></span> <br/> |<span data-ttu-id="c93e3-174">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="c93e3-174">ns2.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="c93e3-175">**Nameserver 3 (Serveur de noms 3)**</span><span class="sxs-lookup"><span data-stu-id="c93e3-175">**Nameserver 3**</span></span> <br/> |<span data-ttu-id="c93e3-176">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="c93e3-176">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="c93e3-177">**Nameserver 4 (Serveur de noms 4)**</span><span class="sxs-lookup"><span data-stu-id="c93e3-177">**Nameserver 4**</span></span> <br/> |<span data-ttu-id="c93e3-178">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="c93e3-178">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
   ![NameCheap-BP-redelegate-1-3-2](../../media/21d681b7-4f96-4e96-ac27-9534c388537c.png)
  
3. <span data-ttu-id="c93e3-180">Sélectionnez le contrôle **Enregistrer** (case à cocher).</span><span class="sxs-lookup"><span data-stu-id="c93e3-180">Select the **Save** (check mark) control.</span></span> 
    
    ![NameCheap-BP-redelegate-1-5](../../media/07aaf1e5-c24f-4c51-bfe0-f99868b3bf35.png)
  
> [!NOTE]
> <span data-ttu-id="c93e3-182">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="c93e3-182">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span></span> <span data-ttu-id="c93e3-183">Votre messagerie Microsoft et les autres services seront tous configurés pour fonctionner avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="c93e3-183">Then your Microsoft email and other services will be all set to work with your domain.</span></span> 
  
### <a name="if-there-are-nameservers-already-listed"></a><span data-ttu-id="c93e3-184">Si DES serveurs de noms sont déjà répertoriés</span><span class="sxs-lookup"><span data-stu-id="c93e3-184">If there ARE nameservers already listed</span></span>

> [!CAUTION]
> <span data-ttu-id="c93e3-p109">Suivez ces étapes  *uniquement*  si vous avez des serveurs de noms existants autres que les quatre serveurs de noms  *corrects*  . Autrement dit, ne supprimez  *que*  les serveurs de noms  *qui ne sont pas*  nommés **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com** ou **ns4.bdm.microsoftonline.com**.</span><span class="sxs-lookup"><span data-stu-id="c93e3-p109">Follow these steps  *only*  if you have existing nameservers other than the four  *correct*  nameservers. (That is, delete  *only*  any current nameservers that are  *not*  named **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, or **ns4.bdm.microsoftonline.com**.)</span></span> 
  
1. <span data-ttu-id="c93e3-187">Si d’autres serveurs de noms sont répertoriés dans les zones serveur de **noms** , supprimez-les en les sélectionnant et en appuyant sur la touche **Suppr** du clavier.</span><span class="sxs-lookup"><span data-stu-id="c93e3-187">If there are any other nameservers listed in the **Nameserver** boxes, delete each one by selecting it and then pressing the **Delete** key on your keyboard.</span></span> 
    
    ![NameCheap-BP-redelegate-1-4](../../media/3270603a-c4f4-40b7-acad-733d56e2f53c.png)
  
2. <span data-ttu-id="c93e3-189">Sélectionnez **Ajouter** un serveur de noms à deux reprises pour ajouter deux nouvelles lignes.</span><span class="sxs-lookup"><span data-stu-id="c93e3-189">Select **ADD NAMESERVER** twice to add two new rows.</span></span> 
    
    ![NameCheap-BP-redelegate-1-3-1](../../media/e8816bf5-bb59-49d5-bfca-43e502242dc3.png)
  
3. <span data-ttu-id="c93e3-191">Dans les zones serveur de **noms** , tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c93e3-191">In the **Nameserver** boxes, type or copy and paste the values from the following table.</span></span>
 
    
|||
|:-----|:-----|
|<span data-ttu-id="c93e3-192">**Name Server 1 (Serveur de noms 1)**</span><span class="sxs-lookup"><span data-stu-id="c93e3-192">**Name Server 1**</span></span> <br/> |<span data-ttu-id="c93e3-193">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="c93e3-193">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="c93e3-194">**Name Server 2 (Serveur de noms 2)**</span><span class="sxs-lookup"><span data-stu-id="c93e3-194">**Name Server 2**</span></span> <br/> |<span data-ttu-id="c93e3-195">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="c93e3-195">ns2.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="c93e3-196">**Nameserver 3 (Serveur de noms 3)**</span><span class="sxs-lookup"><span data-stu-id="c93e3-196">**Nameserver 3**</span></span> <br/> |<span data-ttu-id="c93e3-197">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="c93e3-197">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="c93e3-198">**Nameserver 4 (Serveur de noms 4)**</span><span class="sxs-lookup"><span data-stu-id="c93e3-198">**Nameserver 4**</span></span> <br/> |<span data-ttu-id="c93e3-199">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="c93e3-199">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
   ![NameCheap-BP-redelegate-1-3-2](../../media/21d681b7-4f96-4e96-ac27-9534c388537c.png)
  
4. <span data-ttu-id="c93e3-201">Sélectionnez le contrôle **Enregistrer** (case à cocher).</span><span class="sxs-lookup"><span data-stu-id="c93e3-201">Select the **Save** (check mark) control.</span></span> 
    
    ![NameCheap-BP-redelegate-1-5](../../media/07aaf1e5-c24f-4c51-bfe0-f99868b3bf35.png)
  
> [!NOTE]
> <span data-ttu-id="c93e3-203">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="c93e3-203">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span></span> <span data-ttu-id="c93e3-204">Votre messagerie Microsoft et les autres services seront tous configurés pour fonctionner avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="c93e3-204">Then your Microsoft email and other services will be all set to work with your domain.</span></span>

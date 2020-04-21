---
title: Créer des enregistrements DNS lorsque votre domaine est géré par Google (eNom)
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
- BCS160
- MET150
- MOE150
ms.assetid: 3c490fbf-7833-4e43-be34-ed0dc3cce5e3
description: Apprenez à accéder à eNom et à créer un DNS via la page Google Domains.
ms.openlocfilehash: 7d79350f163d1b120d3dd45bc7bbb3e57583bf05
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43629130"
---
# <a name="create-dns-records-when-your-domain-is-managed-by-google-enom"></a><span data-ttu-id="2ab89-103">Créer des enregistrements DNS lorsque votre domaine est géré par Google (eNom)</span><span class="sxs-lookup"><span data-stu-id="2ab89-103">Create DNS records when your domain is managed by Google (eNom)</span></span>

 <span data-ttu-id="2ab89-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="2ab89-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="2ab89-105">Pour migrer vos comptes de messagerie vers Microsoft, vous devez créer un enregistrement DNS au niveau de votre bureau d’enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="2ab89-105">To migrate your mail accounts to Microsoft, you need to create a DNS record at your domain registrar.</span></span>
  
<span data-ttu-id="2ab89-106">Si vous avez acheté votre domaine par le biais de Google lors de votre inscription à votre compte **Google Apps for Work** , vos enregistrements DNS sont gérés par Google, mais enregistrés auprès de eNom.</span><span class="sxs-lookup"><span data-stu-id="2ab89-106">If you purchased your domain through Google while signing up for your **Google Apps for Work** account, your DNS records are managed by Google but registered with eNom.</span></span> 
  
<span data-ttu-id="2ab89-107">Vous pouvez accéder à eNom et créer DNS, via la page Google **Domains** .</span><span class="sxs-lookup"><span data-stu-id="2ab89-107">You can access eNom, and create DNS, through the Google **Domains** page.</span></span> <span data-ttu-id="2ab89-108">Suivez simplement les étapes décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="2ab89-108">Just follow the steps in this article.</span></span> 
  
## <a name="create-the-dns-record"></a><span data-ttu-id="2ab89-109">Créer l'enregistrement DNS</span><span class="sxs-lookup"><span data-stu-id="2ab89-109">Create the DNS record</span></span>

1. <span data-ttu-id="2ab89-110">Dans la [console d’administration Google](https://www.google.com/work/apps/business), sélectionnez **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="2ab89-110">At the [Google Admin console](https://www.google.com/work/apps/business), select **Sign In**.</span></span>
    
    ![Google-Apps-Configure-1-1-0](../../media/37a6e9f6-319e-4c02-aa18-d8d06df7953d.png)
  
2. <span data-ttu-id="2ab89-112">Entrez votre nom de domaine, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="2ab89-112">Enter your domain name, and then select **Go**.</span></span>
    
    ![Google-Apps-Configure-1-1-1](../../media/2caf8dcb-4d40-4cfa-bc40-d634e454e699.png)
  
3. <span data-ttu-id="2ab89-114">Au bas de la page, sélectionnez **autres contrôles**.</span><span class="sxs-lookup"><span data-stu-id="2ab89-114">At the bottom of the page, select **More controls**.</span></span>
    
    ![Google-Apps-Configure-1-2-0](../../media/1518ff78-035b-423e-85a3-c16d7faa0968.png)
  
4. <span data-ttu-id="2ab89-116">Sélectionnez **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="2ab89-116">Select **Domains**.</span></span>
    
    ![Google-Apps-Configure-1-2-1](../../media/c2972c06-9bca-43bd-9876-2cee63043bf1.png)
  
5. <span data-ttu-id="2ab89-118">Dans la page **domaines** , sélectionnez **Ajouter/supprimer des domaines**.</span><span class="sxs-lookup"><span data-stu-id="2ab89-118">On the **Domains** page, select **Add/remove domains**.</span></span>
    
    ![Google-Apps-Configure-1-2-2](../../media/07b8068f-9a05-40aa-a041-fc495c729a18.png)
  
6. <span data-ttu-id="2ab89-120">Dans la page **domaines** , sélectionnez **paramètres DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="2ab89-120">On the **Domains** page, select **Advanced DNS settings**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="2ab89-121">Si vous n'avez pas acheté un nom de domaine via Google lors de la création de votre compte **Google Apps for Work**, vous n'aurez de **Paramètres DNS avancés** sur votre page **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="2ab89-121">If you didn't purchase a domain name through Google while signing up for your **Google Apps for Work** account, you won't have **Advanced DNS settings** on your **Domains** page.</span></span> <span data-ttu-id="2ab89-122">Au lieu de cela, vous devez aller directement au site web de l'hôte de votre domaine pour accéder à vos paramètres DNS et effectuer cette étape ainsi que les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="2ab89-122">Instead, you must go directly to your domain host's web site to access your DNS settings and to perform this and the following steps.</span></span> <span data-ttu-id="2ab89-123">Pour plus d’informations, consultez [la rubrique accéder aux paramètres de votre domaine G suite](https://support.google.com/a/answer/54693?hl=en) .</span><span class="sxs-lookup"><span data-stu-id="2ab89-123">See [Access your G Suite domain settings](https://support.google.com/a/answer/54693?hl=en) for more information.</span></span> 
  
    ![Google-Apps-eNom-configure-1-3](../../media/b244b29c-e479-40be-b380-4ffa0f74b421.png)
  
7. <span data-ttu-id="2ab89-125">Sur la page **paramètres DNS avancés** , sélectionnez **se connecter à la console DNS**.</span><span class="sxs-lookup"><span data-stu-id="2ab89-125">On the **Advanced DNS settings** page, select **Sign in to DNS Console**.</span></span> <span data-ttu-id="2ab89-126">Notez les informations **Nom de connexion** et **Mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="2ab89-126">Note the **Sign-in name** and **Password** information.</span></span> <span data-ttu-id="2ab89-127">Vous en aurez besoin à l'étape suivante.</span><span class="sxs-lookup"><span data-stu-id="2ab89-127">You'll need it in the next step.</span></span> 
    
    ![Google-Apps-eNom-configure-1-4](../../media/056a2767-462f-4847-acee-d01e3f773add.png)
  
8. <span data-ttu-id="2ab89-129">Connectez-vous au **Gestionnaire de domaine** Google en utilisant les **Nom de connexion** et **Mot de passe** mentionnés dans la page **Paramètres DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="2ab89-129">Log in to the Google **Domain Manager** using the **Sign-in name** and **Password** from the **Advanced DNS settings** page.</span></span> 
    
    ![Google-Apps-eNom-configure-1-5](../../media/08b74652-8cdb-4560-a5fd-0899f86deee8.png)
  
9. <span data-ttu-id="2ab89-131">Sur la page ***domain_name*** , dans la section **Host Records (enregistrements d’hôte** ), sélectionnez Edit ( **modifier**).</span><span class="sxs-lookup"><span data-stu-id="2ab89-131">On the ***domain_name*** page, in the **Host Records** section, select **Edit**.</span></span>
    
    ![Google-Apps-eNom-configure-1-6](../../media/d54fec18-b9d1-4796-8397-0393c964eade.png)
  
10. <span data-ttu-id="2ab89-133">Dans la section **Host Records (enregistrements d’hôte** ), sélectionnez **Add New (Ajouter nouveau**).</span><span class="sxs-lookup"><span data-stu-id="2ab89-133">In the **Host Records** section, select **Add New**.</span></span>
    
    ![Google-Apps-eNom-configure-1-7](../../media/3562806a-4328-4e60-a717-0566841204cf.png)
  
11. <span data-ttu-id="2ab89-135">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2ab89-135">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="2ab89-136">**HOST (HÔTE)**</span><span class="sxs-lookup"><span data-stu-id="2ab89-136">**HOST**</span></span>|<span data-ttu-id="2ab89-137">**TXT VALUE**</span><span class="sxs-lookup"><span data-stu-id="2ab89-137">**TXT VALUE**</span></span>|<span data-ttu-id="2ab89-138">**TYPE D’ENREGISTREMENT**</span><span class="sxs-lookup"><span data-stu-id="2ab89-138">**RECORD TYPE**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> ||<span data-ttu-id="2ab89-139">TXT</span><span class="sxs-lookup"><span data-stu-id="2ab89-139">TXT</span></span>  <br/> |

    > [!NOTE]
    > <span data-ttu-id="2ab89-140">This is an example.</span><span class="sxs-lookup"><span data-stu-id="2ab89-140">This is an example.</span></span> <span data-ttu-id="2ab89-141">Utilisez votre **adresse de destination ou de pointage** spécifique ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="2ab89-141">Use your specific **Destination or Points to Address** value here, from the table.</span></span> 
  
    [<span data-ttu-id="2ab89-142">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="2ab89-142">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)
  
12. <span data-ttu-id="2ab89-143">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2ab89-143">Select **Save**.</span></span>
    
    ![Google-Apps-eNom-configure-1-9](../../media/7a6f7b45-8f79-487b-afe4-05949c2c04e8.png)
  
13. <span data-ttu-id="2ab89-145">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="2ab89-145">Select **Save Changes**.</span></span>
    
    ![Google-Apps-Configure-1-11](../../media/7f321236-33fb-4a7d-9d03-26605e9e558c.png)
  
> [!NOTE]
>  <span data-ttu-id="2ab89-p105">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="2ab89-p105">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  

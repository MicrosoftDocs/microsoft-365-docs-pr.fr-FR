---
title: Ajouter un domaine à Office 365
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
- Adm_O365_Setup
- Adm_O365
- Adm_TOC
ms.custom:
- TopSMBIssues
- SaRA
- MSStore_Link
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 6383f56d-3d09-4dcb-9b41-b5f5a5efd611
description: Ajoutez votre domaine à Office 365 dans le centre d’administration Microsoft 365 en ajoutant un enregistrement DNS au niveau de votre hôte DNS. L’Assistant installation vous guide tout au long du processus.
ms.openlocfilehash: bab4da6e4a8191d91ccdd38dd54f62f4d790c3b8
ms.sourcegitcommit: 7ff75a0f45371b247d975fc61cfa286f5b6f42f6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2020
ms.locfileid: "44140774"
---
# <a name="add-a-domain-to-office-365"></a><span data-ttu-id="de8b5-104">Ajouter un domaine à Office 365</span><span class="sxs-lookup"><span data-stu-id="de8b5-104">Add a domain to Office 365</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="de8b5-105">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="de8b5-105">The admin center is changing.</span></span> <span data-ttu-id="de8b5-106">Si votre expérience ne correspond pas aux détails présentés ici, reportez-vous [à la rubrique à propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="de8b5-106">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

 <span data-ttu-id="de8b5-107">**[Consultez les Forums aux questions sur les domaines](domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="de8b5-107">**[Check the Domains FAQ](domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
 <span data-ttu-id="de8b5-108">*Pour ajouter, modifier ou supprimer des domaines, vous **devez** être **administrateur général** d’un [plan d’entreprise ou d’entreprise](https://products.office.com/business/office). Ces modifications affectent l’ensemble du client, les *administrateurs personnalisés* ou *les utilisateurs réguliers* ne peuvent pas effectuer ces modifications.*</span><span class="sxs-lookup"><span data-stu-id="de8b5-108">*To Add, modify or remove domains you **must** be a **Global Administrator** of a [business or enterprise plan](https://products.office.com/business/office). These changes affect the whole tenant, *Customized administrators* or *regular users* won't be able to make these changes.*</span></span>  

 <span data-ttu-id="de8b5-109">Procédez comme suit pour ajouter, configurer ou continuer à configurer un domaine.</span><span class="sxs-lookup"><span data-stu-id="de8b5-109">Follow these steps to add, set up, or continue setting up a domain.</span></span> 

::: moniker range="o365-worldwide"
  
::: moniker-end

::: moniker range="o365-germany"

> [!VIDEO https://www.microsoft.com/videoplayer/embed/dda6df6d-37b0-41ff-905b-089448355a31?autoplay=false]
  
::: moniker-end

::: moniker range="o365-worldwide"

1. <span data-ttu-id="de8b5-110">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span><span class="sxs-lookup"><span data-stu-id="de8b5-110">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

::: moniker-end
::: moniker range="o365-germany"

1. <span data-ttu-id="de8b5-111">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">https://portal.office.de/adminportal</a>.</span><span class="sxs-lookup"><span data-stu-id="de8b5-111">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">https://portal.office.de/adminportal</a>.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="de8b5-112">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">https://portal.partner.microsoftonline.cn</a>.</span><span class="sxs-lookup"><span data-stu-id="de8b5-112">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">https://portal.partner.microsoftonline.cn</a>.</span></span>

::: moniker-end
    
2. <span data-ttu-id="de8b5-113">Accédez à la page**domaines** **d’installation** > .</span><span class="sxs-lookup"><span data-stu-id="de8b5-113">Go to the **Setup** > **Domains** page.</span></span> 

3. <span data-ttu-id="de8b5-114">Sélectionnez **Ajouter un domaine**.</span><span class="sxs-lookup"><span data-stu-id="de8b5-114">Select **Add domain**.</span></span>
    
4. <span data-ttu-id="de8b5-115">Entrez le nom du domaine que vous souhaitez ajouter, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="de8b5-115">Enter the name of the domain you want to add, then select **Next**.</span></span>
    
5. <span data-ttu-id="de8b5-116">Choisissez la manière dont vous souhaitez vérifier que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="de8b5-116">Choose how you want to verify that you own the domain.</span></span>
    
    1. <span data-ttu-id="de8b5-117">Si votre domaine est inscrit sur GoDaddy ou 1&amp;1, sélectionnez **connexion** > **suivante** et Microsoft[configure automatiquement vos enregistrements](../get-help-with-domains/domain-connect.md).</span><span class="sxs-lookup"><span data-stu-id="de8b5-117">If your domain is registered at GoDaddy or 1&amp;1, select **Sign in** > **Next** and Microsoft[will set up your records automatically](../get-help-with-domains/domain-connect.md).</span></span>
    
    2. <span data-ttu-id="de8b5-118">Vous pouvez demander à ce qu'un courrier incluant un code de vérification soit envoyé au contact enregistré pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="de8b5-118">You can have an email sent to the registered contact for the domain with a verification code.</span></span> <span data-ttu-id="de8b5-119">Si vous ne reconnaissez pas ou n’avez pas accès au courrier électronique, vous pouvez utiliser la troisième option.</span><span class="sxs-lookup"><span data-stu-id="de8b5-119">If you don't recognize or have access to the email on record, you can use the third option.</span></span>
    
    3. <span data-ttu-id="de8b5-120">Vous pouvez utiliser un enregistrement TXT pour vérifier votre domaine.</span><span class="sxs-lookup"><span data-stu-id="de8b5-120">You can use a TXT record to verify your domain.</span></span> <span data-ttu-id="de8b5-121">Sélectionnez-le et cliquez sur **suivant** pour obtenir des instructions sur la façon d’ajouter cet enregistrement DNS au site Web de votre registraire.</span><span class="sxs-lookup"><span data-stu-id="de8b5-121">Select this and select **Next** to see instructions for how to add this DNS record to your registrar's website.</span></span> <span data-ttu-id="de8b5-122">La vérification peut prendre jusqu’à 30 minutes après l’ajout de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="de8b5-122">This can take up to 30 minutes to verify after you've added the record.</span></span> 
    
6. <span data-ttu-id="de8b5-123">Choisissez comment vous souhaitez appliquer les modifications DNS requises pour Office pour utiliser votre domaine.</span><span class="sxs-lookup"><span data-stu-id="de8b5-123">Choose how you want to make the DNS changes required for Office to use your domain.</span></span>
    
    1. <span data-ttu-id="de8b5-124">Sélectionnez **Ajouter les enregistrements DNS pour moi** si vous souhaitez qu’Office configure votre DNS automatiquement.</span><span class="sxs-lookup"><span data-stu-id="de8b5-124">Choose **Add the DNS records for me** if you want Office to configure your DNS automatically.</span></span> 
    
  
    2. <span data-ttu-id="de8b5-125">Sélectionnez **j’aurai ajouté les enregistrements DNS moi-même** si vous voulez joindre uniquement des services Office 365 spécifiques à votre domaine ou si vous souhaitez ignorer cette opération pour le moment et effectuer cette opération plus tard.</span><span class="sxs-lookup"><span data-stu-id="de8b5-125">Choose **I'll add the DNS records myself** if you want to attach only specific Office 365 services to your domain or if you want to skip this for now and do this later.</span></span> <span data-ttu-id="de8b5-126">**Choisissez cette option si vous savez exactement ce que vous faites.**</span><span class="sxs-lookup"><span data-stu-id="de8b5-126">**Choose this option if you know exactly what you're doing.**</span></span>
    
7. <span data-ttu-id="de8b5-127">Si vous décidez d' *Ajouter des enregistrements DNS vous-même* , sélectionnez **suivant** et vous verrez une page contenant tous les enregistrements que vous devez ajouter à votre site Web des registres pour configurer votre domaine.</span><span class="sxs-lookup"><span data-stu-id="de8b5-127">If you chose to  *add DNS records yourself*  , select **Next** and you'll see a page with all the records that you need to add to your registrars website to set up your domain.</span></span> 
    
  
  
    <span data-ttu-id="de8b5-128">Si le portail ne reconnaît pas votre bureau d'enregistrement, vous pouvez [suivre ces instructions générales](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md).</span><span class="sxs-lookup"><span data-stu-id="de8b5-128">If the portal doesn't recognize your registrar, you can [follow these general instructions.](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md)</span></span>
    
    <span data-ttu-id="de8b5-129">Consultez notre liste d’[instructions spécifiques selon l’hôte](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions) pour rechercher votre hôte et suivre les étapes d’ajout des enregistrements dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="de8b5-129">Check our list of [host-specific instructions](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions) to find your host and follow the steps to add all the records you need.</span></span> 
    
    <span data-ttu-id="de8b5-130">Si vous ne connaissez pas le fournisseur d'hébergement DNS ou le bureau d'enregistrement pour votre domaine, voir [Rechercher mon bureau d'enregistrement de domaines ou mon fournisseur d'hébergement DNS](../get-help-with-domains/find-your-domain-registrar.md).</span><span class="sxs-lookup"><span data-stu-id="de8b5-130">If you don't know the DNS hosting provider or domain registrar for your domain, see [Find your domain registrar or DNS hosting provider](../get-help-with-domains/find-your-domain-registrar.md).</span></span>
    
    <span data-ttu-id="de8b5-131">Si vous souhaitez attendre plus tard, faites défiler la liste vers le bas et sélectionnez **ignorer cette étape**.</span><span class="sxs-lookup"><span data-stu-id="de8b5-131">If you want to wait for later, scroll to the bottom and select **Skip this step**.</span></span>
    
8. <span data-ttu-id="de8b5-132">Sélectionnez **Terminer** -vous avez terminé !</span><span class="sxs-lookup"><span data-stu-id="de8b5-132">Select **Finish** - you're done!</span></span> 

## <a name="add-or-edit-custom-dns-records"></a><span data-ttu-id="de8b5-133">Ajouter ou modifier des enregistrements DNS personnalisés</span><span class="sxs-lookup"><span data-stu-id="de8b5-133">Add or edit custom DNS records</span></span>

<span data-ttu-id="de8b5-134">Suivez les étapes ci-dessous pour ajouter un enregistrement personnalisé pour un site Web ou un service tiers.</span><span class="sxs-lookup"><span data-stu-id="de8b5-134">Follow the steps below to add a custom record for a website or 3rd party service.</span></span>

1. <span data-ttu-id="de8b5-135">Connectez-vous au centre d’administration Microsoft <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>à l’adresse.</span><span class="sxs-lookup"><span data-stu-id="de8b5-135">Sign in to the Microsoft admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

2. <span data-ttu-id="de8b5-136">Accédez à la page **paramètres**  > des**domaines** .</span><span class="sxs-lookup"><span data-stu-id="de8b5-136">Go to the **Settings**  > **Domains** page.</span></span>

3. <span data-ttu-id="de8b5-137">Dans la page **Domaines**, sélectionnez un domaine.</span><span class="sxs-lookup"><span data-stu-id="de8b5-137">On the **Domains** page, select a domain.</span></span> 
    
4. <span data-ttu-id="de8b5-138">Sous **paramètres DNS**, sélectionnez **enregistrements personnalisés**; Ensuite, sélectionnez **nouvel enregistrement personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="de8b5-138">Under **DNS settings**, select **Custom Records**; then select **New custom record**.</span></span>

5. <span data-ttu-id="de8b5-139">Sélectionnez le type d’enregistrement DNS que vous souhaitez ajouter et tapez les informations pour le nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="de8b5-139">Select the type of DNS record you want to add and type the information for the new record.</span></span>
    
6. <span data-ttu-id="de8b5-140">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="de8b5-140">Select **Save**.</span></span>

## <a name="registrars-with-domain-connect"></a><span data-ttu-id="de8b5-141">Bureaux d’inscriptions avec connexion au domaine</span><span class="sxs-lookup"><span data-stu-id="de8b5-141">Registrars with Domain Connect</span></span>

<span data-ttu-id="de8b5-142">Les bureaux d’accès activés pour la [connexion au domaine](https://www.domainconnect.org/) vous permettent d’ajouter votre domaine à Microsoft 365 dans un processus en trois étapes qui prend quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="de8b5-142">[Domain Connect](https://www.domainconnect.org/) enabled registrars let you add your domain to Microsoft 365 in a three-step process that takes minutes.</span></span> 
  
<span data-ttu-id="de8b5-143">Dans l’Assistant, nous confirmons que vous êtes propriétaire du domaine, puis vous configurez automatiquement les enregistrements de votre domaine, de sorte que le courrier électronique est envoyé à Microsoft 365 et d’autres services Microsoft 365, comme Teams, travaillez avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="de8b5-143">In the wizard, we'll just confirm that you own the domain, and then automatically set up your domain's records, so email comes to Microsoft 365 and other Microsoft 365 services, like Teams, work with your domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="de8b5-144">Veillez à désactiver les bloqueurs de fenêtres contextuelles dans votre navigateur avant de démarrer l'Assistant de configuration.</span><span class="sxs-lookup"><span data-stu-id="de8b5-144">Make sure you disable any popup blockers in your browser before you start the setup wizard.</span></span>
  
### <a name="domain-connect-registrars-integrating-with-microsoft-365"></a><span data-ttu-id="de8b5-145">Bureaux de connexion au domaine intégration à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="de8b5-145">Domain Connect registrars integrating with Microsoft 365</span></span>

- [<span data-ttu-id="de8b5-146">1&amp;1 Ionos</span><span class="sxs-lookup"><span data-stu-id="de8b5-146">1&amp;1 IONOS</span></span>](https://www.1and1.com/)
- [<span data-ttu-id="de8b5-147">123Reg</span><span class="sxs-lookup"><span data-stu-id="de8b5-147">123Reg</span></span>](https://www.123-reg.co.uk/)
- [<span data-ttu-id="de8b5-148">GoDaddy</span><span class="sxs-lookup"><span data-stu-id="de8b5-148">GoDaddy</span></span>](https://www.godaddy.com/)
- [<span data-ttu-id="de8b5-149">WordPress</span><span class="sxs-lookup"><span data-stu-id="de8b5-149">WordPress</span></span>](https://wordpress.com/)
- [<span data-ttu-id="de8b5-150">Plesk</span><span class="sxs-lookup"><span data-stu-id="de8b5-150">Plesk</span></span>](https://www.plesk.com/)
- [<span data-ttu-id="de8b5-151">MediaTemple</span><span class="sxs-lookup"><span data-stu-id="de8b5-151">MediaTemple</span></span>](https://mediatemple.net/)
- <span data-ttu-id="de8b5-152">SecureServer ou WildWestDomains (revendeurs GoDaddy utilisant SecureServer hébergement DNS)</span><span class="sxs-lookup"><span data-stu-id="de8b5-152">SecureServer or WildWestDomains (GoDaddy resellers using SecureServer DNS hosting)</span></span>
    - [<span data-ttu-id="de8b5-153">Domaines MadDog</span><span class="sxs-lookup"><span data-stu-id="de8b5-153">MadDog Domains</span></span>](https://www.maddogdomains.com/)
    - [<span data-ttu-id="de8b5-154">CheapNames</span><span class="sxs-lookup"><span data-stu-id="de8b5-154">CheapNames</span></span>](https://www.cheapnames.com)

### <a name="what-happens-to-my-email-and-website"></a><span data-ttu-id="de8b5-155">Qu’arrive-t-il à mon courrier électronique et à mon site Web ?</span><span class="sxs-lookup"><span data-stu-id="de8b5-155">What happens to my email and website?</span></span>

<span data-ttu-id="de8b5-156">Une fois que vous avez terminé l’installation, l’enregistrement MX de votre domaine est mis à jour pour pointer vers Microsoft 365 et tous les messages électroniques pour votre domaine vont débuter vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="de8b5-156">After you finish setup, the MX record for your domain is updated to point to Microsoft 365 and all email for your domain will start coming to Microsoft 365.</span></span> <span data-ttu-id="de8b5-157">Vérifiez que vous avez ajouté les utilisateurs et configuré les boîtes aux lettres dans Office 365 de toutes les personnes qui reçoivent du courrier électronique sur votre domaine.</span><span class="sxs-lookup"><span data-stu-id="de8b5-157">Make sure you've added users and set up mailboxes in Office 365 for everyone who gets email on your domain!</span></span>
  
<span data-ttu-id="de8b5-158">Si vous avez un site web que vous utilisez dans le cadre de votre activité, il continuera à fonctionner là où il se trouve.</span><span class="sxs-lookup"><span data-stu-id="de8b5-158">If you have a website that you use with your business, it will keep working where it is.</span></span> <span data-ttu-id="de8b5-159">Les étapes de configuration de la connexion au domaine n’affectent pas votre site Web.</span><span class="sxs-lookup"><span data-stu-id="de8b5-159">The Domain Connect setup steps don't affect your website.</span></span>

## <a name="related-articles"></a><span data-ttu-id="de8b5-160">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="de8b5-160">Related articles</span></span>

[<span data-ttu-id="de8b5-161">Foire aux questions domaines</span><span class="sxs-lookup"><span data-stu-id="de8b5-161">Domains FAQ</span></span>](domains-faq.md)

[<span data-ttu-id="de8b5-162">Qu’est-ce qu’un domaine ?</span><span class="sxs-lookup"><span data-stu-id="de8b5-162">What is a domain?</span></span>](../get-help-with-domains/what-is-a-domain.md)

[<span data-ttu-id="de8b5-163">Acheter un nom de domaine dans Office 365</span><span class="sxs-lookup"><span data-stu-id="de8b5-163">Buy a domain name in Office 365</span></span>](../get-help-with-domains/buy-a-domain-name.md)

[<span data-ttu-id="de8b5-164">Configurer votre domaine (instructions spécifiques de l’hôte)</span><span class="sxs-lookup"><span data-stu-id="de8b5-164">Set up your domain (host-specific instructions)</span></span>](../get-help-with-domains/set-up-your-domain-host-specific-instructions.md)

[<span data-ttu-id="de8b5-165">Obtenir de l’aide sur les domaines</span><span class="sxs-lookup"><span data-stu-id="de8b5-165">Get help with domains</span></span>](../get-help-with-domains/get-help-with-domains.md)

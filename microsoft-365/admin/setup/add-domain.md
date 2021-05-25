---
title: Ajouter un domaine à Microsoft 365
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
- Adm_O365_Setup
- Adm_O365
- Adm_TOC
ms.custom:
- TopSMBIssues
- SaRA
- MSStore_Link
- okr_smb
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 6383f56d-3d09-4dcb-9b41-b5f5a5efd611
description: Utilisez l’Assistant Installation pour ajouter votre domaine à Microsoft 365 dans le centre d’administration Microsoft 365 en ajoutant un enregistrement DNS à votre hôte DNS.
ms.openlocfilehash: 152144737b0ff8cb8b0c27db2a4fc1051fb2a8a7
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52635677"
---
# <a name="add-a-domain-to-microsoft-365"></a><span data-ttu-id="bfceb-103">Ajouter un domaine à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bfceb-103">Add a domain to Microsoft 365</span></span>

 <span data-ttu-id="bfceb-104">**[Consultez les Forums aux questions sur les domaines](domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="bfceb-104">**[Check the Domains FAQ](domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
 <span data-ttu-id="bfceb-105">*Pour ajouter, modifier ou supprimer des domaines, vous **devez** être administrateur **général** d’un [plan d’entreprise ou d’entreprise.](https://products.office.com/business/office) Ces modifications affectent l’ensemble du  client, *les administrateurs personnalisés* ou les utilisateurs réguliers ne pourront pas effectuer ces modifications.*</span><span class="sxs-lookup"><span data-stu-id="bfceb-105">*To Add, modify or remove domains you **must** be a **Global Administrator** of a [business or enterprise plan](https://products.office.com/business/office). These changes affect the whole tenant, *Customized administrators* or *regular users* won't be able to make these changes.*</span></span>  

 ## <a name="add-a-domain"></a><span data-ttu-id="bfceb-106">Ajouter un domaine</span><span class="sxs-lookup"><span data-stu-id="bfceb-106">Add a domain</span></span>

<span data-ttu-id="bfceb-107">Suivez ces étapes pour ajouter, configurer ou poursuivre la configuration d’un domaine.</span><span class="sxs-lookup"><span data-stu-id="bfceb-107">Follow these steps to add, set up, or continue setting up a domain.</span></span> 

::: moniker range="o365-worldwide"

1. <span data-ttu-id="bfceb-108">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span><span class="sxs-lookup"><span data-stu-id="bfceb-108">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

::: moniker-end
::: moniker range="o365-germany"

1. <span data-ttu-id="bfceb-109">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">https://portal.office.de/adminportal</a>.</span><span class="sxs-lookup"><span data-stu-id="bfceb-109">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">https://portal.office.de/adminportal</a>.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="bfceb-110">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">https://portal.partner.microsoftonline.cn</a>.</span><span class="sxs-lookup"><span data-stu-id="bfceb-110">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">https://portal.partner.microsoftonline.cn</a>.</span></span>

::: moniker-end
    
2. <span data-ttu-id="bfceb-111">Go to the **Paramètres**  >  **Domains** page.</span><span class="sxs-lookup"><span data-stu-id="bfceb-111">Go to the **Settings** > **Domains** page.</span></span> 

3. <span data-ttu-id="bfceb-112">Sélectionnez **Ajouter un domaine**.</span><span class="sxs-lookup"><span data-stu-id="bfceb-112">Select **Add domain**.</span></span>
    
4. <span data-ttu-id="bfceb-113">Entrez le nom du domaine que vous souhaitez ajouter, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bfceb-113">Enter the name of the domain you want to add, then select **Next**.</span></span>
    
5. <span data-ttu-id="bfceb-114">Choisissez la façon dont vous souhaitez vérifier que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="bfceb-114">Choose how you want to verify that you own the domain.</span></span>
    
    1. <span data-ttu-id="bfceb-115">Si votre bureau d’enregistrement de domaines utilise [domain Connecter](#domain-connect-registrars-integrating-with-microsoft-365), [Microsoft](../get-help-with-domains/domain-connect.md) configurera automatiquement vos enregistrements en vous connectant à votre bureau d’enregistrement et en confirmant la connexion à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bfceb-115">If your domain registrar uses [Domain Connect](#domain-connect-registrars-integrating-with-microsoft-365), Microsoft [will set up your records automatically](../get-help-with-domains/domain-connect.md) by having you sign in to your registrar and confirm the connection to Microsoft 365.</span></span> <span data-ttu-id="bfceb-116">Vous serez renvoyé au Centre d’administration et Microsoft vérifiera ensuite automatiquement votre domaine.</span><span class="sxs-lookup"><span data-stu-id="bfceb-116">You'll be returned to the admin center and Microsoft will then automatically verify your domain.</span></span>
    2. <span data-ttu-id="bfceb-117">Vous pouvez utiliser un enregistrement TXT pour vérifier votre domaine.</span><span class="sxs-lookup"><span data-stu-id="bfceb-117">You can use a TXT record to verify your domain.</span></span> <span data-ttu-id="bfceb-118">Sélectionnez ceci et **sélectionnez Suivant** pour voir les instructions d’ajout de cet enregistrement DNS au site web de votre bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bfceb-118">Select this and select **Next** to see instructions for how to add this DNS record to your registrar's website.</span></span> <span data-ttu-id="bfceb-119">La vérification peut prendre jusqu’à 30 minutes après l’ajout de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bfceb-119">This can take up to 30 minutes to verify after you've added the record.</span></span> 
    3. <span data-ttu-id="bfceb-120">Vous pouvez ajouter un fichier texte au site web de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="bfceb-120">You can add a text file to your domain's website.</span></span> <span data-ttu-id="bfceb-121">Sélectionnez et téléchargez le .txt à partir de l’Assistant Installation, puis téléchargez le fichier dans le dossier de niveau supérieur de votre site web.</span><span class="sxs-lookup"><span data-stu-id="bfceb-121">Select and download the .txt file from the setup wizard, then upload the file to your website's top level folder.</span></span> <span data-ttu-id="bfceb-122">Le chemin d’accès au fichier doit ressembler à : `http://mydomain.com/ms39978200.txt` .</span><span class="sxs-lookup"><span data-stu-id="bfceb-122">The path to the file should look similar to: `http://mydomain.com/ms39978200.txt`.</span></span> <span data-ttu-id="bfceb-123">Nous vous confirmerons que vous êtes propriétaire du domaine en trouvant le fichier sur votre site web.</span><span class="sxs-lookup"><span data-stu-id="bfceb-123">We'll confirm you own the domain by finding the file on your website.</span></span>
    
6. <span data-ttu-id="bfceb-124">Choisissez la façon dont vous souhaitez apporter les modifications DNS requises pour que Microsoft utilise votre domaine.</span><span class="sxs-lookup"><span data-stu-id="bfceb-124">Choose how you want to make the DNS changes required for Microsoft to use your domain.</span></span>
    
    1. <span data-ttu-id="bfceb-125">Choisissez Ajouter les enregistrements **DNS** pour moi si votre bureau d’enregistrement prend en charge [domain Connecter](#domain-connect-registrars-integrating-with-microsoft-365)et [Microsoft](../get-help-with-domains/domain-connect.md) configurera vos enregistrements automatiquement en vous connectant à votre bureau d’enregistrement et en confirmant la connexion à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bfceb-125">Choose **Add the DNS records for me** if your registrar supports [Domain Connect](#domain-connect-registrars-integrating-with-microsoft-365), and Microsoft [will set up your records automatically](../get-help-with-domains/domain-connect.md) by having you sign in to your registrar and confirm the connection to Microsoft 365.</span></span>
    2. <span data-ttu-id="bfceb-126">Choisissez **J’ajouterai** les enregistrements DNS moi-même si vous souhaitez joindre uniquement des services Microsoft 365 spécifiques à votre domaine ou si vous souhaitez ignorer cette étape pour le moment et le faire ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="bfceb-126">Choose **I'll add the DNS records myself** if you want to attach only specific Microsoft 365 services to your domain or if you want to skip this for now and do this later.</span></span> <span data-ttu-id="bfceb-127">**Choisissez cette option si vous savez exactement ce que vous faites.**</span><span class="sxs-lookup"><span data-stu-id="bfceb-127">**Choose this option if you know exactly what you're doing.**</span></span>

7. <span data-ttu-id="bfceb-128">Si vous avez choisi d’ajouter vous-même des enregistrements *DNS,*  sélectionnez **Suivant** et vous verrez une page avec tous les enregistrements que vous devez ajouter à votre site web de bureau d’enregistrement pour configurer votre domaine.</span><span class="sxs-lookup"><span data-stu-id="bfceb-128">If you chose to *add DNS records yourself*  , select **Next** and you'll see a page with all the records that you need to add to your registrars website to set up your domain.</span></span> 

    <span data-ttu-id="bfceb-129">Si le portail ne reconnaît pas votre bureau d'enregistrement, vous pouvez [suivre ces instructions générales](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md).</span><span class="sxs-lookup"><span data-stu-id="bfceb-129">If the portal doesn't recognize your registrar, you can [follow these general instructions.](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md)</span></span>
    
    <span data-ttu-id="bfceb-130">Consultez notre liste d’[instructions spécifiques selon l’hôte](../get-help-with-domains/set-up-your-domain-host-specific-instructions.md) pour rechercher votre hôte et suivre les étapes d’ajout des enregistrements dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="bfceb-130">Check our list of [host-specific instructions](../get-help-with-domains/set-up-your-domain-host-specific-instructions.md) to find your host and follow the steps to add all the records you need.</span></span> 
    
    <span data-ttu-id="bfceb-131">Si vous ne connaissez pas le fournisseur d'hébergement DNS ou le bureau d'enregistrement pour votre domaine, voir [Rechercher mon bureau d'enregistrement de domaines ou mon fournisseur d'hébergement DNS](../get-help-with-domains/find-your-domain-registrar.md).</span><span class="sxs-lookup"><span data-stu-id="bfceb-131">If you don't know the DNS hosting provider or domain registrar for your domain, see [Find your domain registrar or DNS hosting provider](../get-help-with-domains/find-your-domain-registrar.md).</span></span>
    
    <span data-ttu-id="bfceb-132">Si vous souhaitez attendre plus tard, désélectionnez tous les services et cliquez sur **Continuer,** ou à l’étape précédente de connexion de domaine, sélectionnez Plus **d’options** et sélectionnez Ignorer cette option **pour le moment.**</span><span class="sxs-lookup"><span data-stu-id="bfceb-132">If you want to wait for later, either unselect all the services and click **Continue**, or in the previous domain connection step choose **More Options** and select **Skip this for now**.</span></span>
    
8. <span data-ttu-id="bfceb-133">Select **Finish** - you’re done!</span><span class="sxs-lookup"><span data-stu-id="bfceb-133">Select **Finish** - you're done!</span></span>

## <a name="add-or-edit-custom-dns-records"></a><span data-ttu-id="bfceb-134">Ajouter ou modifier des enregistrements DNS personnalisés</span><span class="sxs-lookup"><span data-stu-id="bfceb-134">Add or edit custom DNS records</span></span>

<span data-ttu-id="bfceb-135">Suivez les étapes ci-dessous pour ajouter un enregistrement personnalisé pour un site web ou un service tiers.</span><span class="sxs-lookup"><span data-stu-id="bfceb-135">Follow the steps below to add a custom record for a website or 3rd party service.</span></span>

1. <span data-ttu-id="bfceb-136">Connectez-vous au Centre d’administration Microsoft à <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> l’adresse .</span><span class="sxs-lookup"><span data-stu-id="bfceb-136">Sign in to the Microsoft admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

2. <span data-ttu-id="bfceb-137">Go to the **Paramètres**   >  **Domains** page.</span><span class="sxs-lookup"><span data-stu-id="bfceb-137">Go to the **Settings**  > **Domains** page.</span></span>

3. <span data-ttu-id="bfceb-138">Dans la page **Domaines**, sélectionnez un domaine.</span><span class="sxs-lookup"><span data-stu-id="bfceb-138">On the **Domains** page, select a domain.</span></span> 
    
4. <span data-ttu-id="bfceb-139">Sous **paramètres DNS**, sélectionnez **Enregistrements personnalisés**; puis **sélectionnez Nouvel enregistrement personnalisé.**</span><span class="sxs-lookup"><span data-stu-id="bfceb-139">Under **DNS settings**, select **Custom Records**; then select **New custom record**.</span></span>

5. <span data-ttu-id="bfceb-140">Sélectionnez le type d’enregistrement DNS à ajouter et tapez les informations du nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bfceb-140">Select the type of DNS record you want to add and type the information for the new record.</span></span>
    
6. <span data-ttu-id="bfceb-141">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="bfceb-141">Select **Save**.</span></span>

## <a name="registrars-with-domain-connect"></a><span data-ttu-id="bfceb-142">Bureaux d’enregistrement avec Connecter</span><span class="sxs-lookup"><span data-stu-id="bfceb-142">Registrars with Domain Connect</span></span>

<span data-ttu-id="bfceb-143">[Les Connecter](https://www.domainconnect.org/) bureaux d’enregistrement activés vous permettent d’ajouter votre domaine à Microsoft 365 dans un processus en trois étapes qui prend quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="bfceb-143">[Domain Connect](https://www.domainconnect.org/) enabled registrars let you add your domain to Microsoft 365 in a three-step process that takes minutes.</span></span> 
  
<span data-ttu-id="bfceb-144">Dans l’Assistant, nous allons simplement confirmer que vous êtes propriétaire du domaine, puis configurer automatiquement les enregistrements de votre domaine, afin que le courrier électronique soit envoyé à Microsoft 365 et d’autres services Microsoft 365, tels que Teams, fonctionnent avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="bfceb-144">In the wizard, we'll just confirm that you own the domain, and then automatically set up your domain's records, so email comes to Microsoft 365 and other Microsoft 365 services, like Teams, work with your domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bfceb-145">Veillez à désactiver les bloqueurs de fenêtres contextuelles dans votre navigateur avant de démarrer l'Assistant de configuration.</span><span class="sxs-lookup"><span data-stu-id="bfceb-145">Make sure you disable any popup blockers in your browser before you start the setup wizard.</span></span>
  
### <a name="domain-connect-registrars-integrating-with-microsoft-365"></a><span data-ttu-id="bfceb-146">Intégration Connecter bureaux d’enregistrement de domaines Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bfceb-146">Domain Connect registrars integrating with Microsoft 365</span></span>

- [<span data-ttu-id="bfceb-147">1 &amp; 1 IONOS</span><span class="sxs-lookup"><span data-stu-id="bfceb-147">1&amp;1 IONOS</span></span>](https://www.1and1.com/)
- [<span data-ttu-id="bfceb-148">EuroDNS</span><span class="sxs-lookup"><span data-stu-id="bfceb-148">EuroDNS</span></span>](https://www.eurodns.com/)
- [<span data-ttu-id="bfceb-149">Cloudflare</span><span class="sxs-lookup"><span data-stu-id="bfceb-149">Cloudflare</span></span>](https://www.cloudflare.com/)
- [<span data-ttu-id="bfceb-150">GoDaddy</span><span class="sxs-lookup"><span data-stu-id="bfceb-150">GoDaddy</span></span>](https://www.godaddy.com/)
- [<span data-ttu-id="bfceb-151">WordPress.com</span><span class="sxs-lookup"><span data-stu-id="bfceb-151">WordPress.com</span></span>](https://wordpress.com/)
- [<span data-ttu-id="bfceb-152">Iquésk</span><span class="sxs-lookup"><span data-stu-id="bfceb-152">Plesk</span></span>](https://www.plesk.com/)
- [<span data-ttu-id="bfceb-153">MediaTemple</span><span class="sxs-lookup"><span data-stu-id="bfceb-153">MediaTemple</span></span>](https://mediatemple.net/)
- <span data-ttu-id="bfceb-154">SecureServer ou WildWestDomains (revendeurs GoDaddy utilisant l’hébergement DNS SecureServer)</span><span class="sxs-lookup"><span data-stu-id="bfceb-154">SecureServer or WildWestDomains (GoDaddy resellers using SecureServer DNS hosting)</span></span>
    - <span data-ttu-id="bfceb-155">Exemples :</span><span class="sxs-lookup"><span data-stu-id="bfceb-155">Examples:</span></span>
        - [<span data-ttu-id="bfceb-156">DomainsPricedRight</span><span class="sxs-lookup"><span data-stu-id="bfceb-156">DomainsPricedRight</span></span>](https://www.domainspricedright.com/products/domain-registration)
        - [<span data-ttu-id="bfceb-157">DomainRightNow</span><span class="sxs-lookup"><span data-stu-id="bfceb-157">DomainRightNow</span></span>](https://www.domainrightnow.com/)

### <a name="what-happens-to-my-email-and-website"></a><span data-ttu-id="bfceb-158">Qu’advient-il de mon courrier électronique et de mon site web ?</span><span class="sxs-lookup"><span data-stu-id="bfceb-158">What happens to my email and website?</span></span>

<span data-ttu-id="bfceb-159">Une fois l’installation terminé, l’enregistrement MX de votre domaine est mis à jour pour pointer vers Microsoft 365 et tous les e-mails de votre domaine commenceront à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bfceb-159">After you finish setup, the MX record for your domain is updated to point to Microsoft 365 and all email for your domain will start coming to Microsoft 365.</span></span> <span data-ttu-id="bfceb-160">Assurez-vous d’avoir ajouté des utilisateurs et de configurer des boîtes aux lettres dans Microsoft 365 pour toutes les personnes qui reçoit du courrier électronique sur votre domaine !</span><span class="sxs-lookup"><span data-stu-id="bfceb-160">Make sure you've added users and set up mailboxes in Microsoft 365 for everyone who gets email on your domain!</span></span>
  
<span data-ttu-id="bfceb-161">Si vous avez un site web que vous utilisez dans le cadre de votre activité, il continuera à fonctionner là où il se trouve.</span><span class="sxs-lookup"><span data-stu-id="bfceb-161">If you have a website that you use with your business, it will keep working where it is.</span></span> <span data-ttu-id="bfceb-162">Les étapes de Connecter domaine n’affectent pas votre site web.</span><span class="sxs-lookup"><span data-stu-id="bfceb-162">The Domain Connect setup steps don't affect your website.</span></span>

## <a name="related-content"></a><span data-ttu-id="bfceb-163">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="bfceb-163">Related content</span></span>

<span data-ttu-id="bfceb-164">[Forum aux questions sur les domaines](domains-faq.yml) (article)</span><span class="sxs-lookup"><span data-stu-id="bfceb-164">[Domains FAQ](domains-faq.yml) (article)</span></span>\
[<span data-ttu-id="bfceb-165">Qu’est-ce qu’un domaine ?</span><span class="sxs-lookup"><span data-stu-id="bfceb-165">What is a domain?</span></span>](../get-help-with-domains/what-is-a-domain.md) <span data-ttu-id="bfceb-166">(article)</span><span class="sxs-lookup"><span data-stu-id="bfceb-166">(article)</span></span>\
<span data-ttu-id="bfceb-167">[Acheter un nom de domaine dans Microsoft 365](../get-help-with-domains/buy-a-domain-name.md) (article)</span><span class="sxs-lookup"><span data-stu-id="bfceb-167">[Buy a domain name in Microsoft 365](../get-help-with-domains/buy-a-domain-name.md) (article)</span></span>\
<span data-ttu-id="bfceb-168">[Configurer votre domaine](../get-help-with-domains/set-up-your-domain-host-specific-instructions.md) (article)</span><span class="sxs-lookup"><span data-stu-id="bfceb-168">[Set up your domain](../get-help-with-domains/set-up-your-domain-host-specific-instructions.md) (article)</span></span>
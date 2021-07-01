---
title: Ajouter un domaine à Microsoft 365
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
description: Utilisez l’Assistant Installation pour ajouter votre domaine à Microsoft 365 dans le Centre d’administration Microsoft 365 en ajoutant un enregistrement DNS à votre hôte DNS.
ms.openlocfilehash: 547a3bf242130993522b00f53819908b10c9e4d1
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53227834"
---
# <a name="add-a-domain-to-microsoft-365"></a><span data-ttu-id="a884b-103">Ajouter un domaine à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a884b-103">Add a domain to Microsoft 365</span></span>

 <span data-ttu-id="a884b-104">**[Consultez les Forums aux questions sur les domaines](domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="a884b-104">**[Check the Domains FAQ](domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
 <span data-ttu-id="a884b-105">*Pour ajouter, modifier ou supprimer des domaines, vous **devez** être administrateur **général** d’un [plan d’entreprise ou d’entreprise.](https://products.office.com/business/office) Ces modifications affectent l’ensemble du  client, *les administrateurs personnalisés* ou les utilisateurs réguliers ne pourront pas effectuer ces modifications.*</span><span class="sxs-lookup"><span data-stu-id="a884b-105">*To Add, modify or remove domains you **must** be a **Global Administrator** of a [business or enterprise plan](https://products.office.com/business/office). These changes affect the whole tenant, *Customized administrators* or *regular users* won't be able to make these changes.*</span></span>  

 ## <a name="add-a-domain"></a><span data-ttu-id="a884b-106">Ajouter un domaine</span><span class="sxs-lookup"><span data-stu-id="a884b-106">Add a domain</span></span>

<span data-ttu-id="a884b-107">Suivez ces étapes pour ajouter, configurer ou continuer à configurer un domaine.</span><span class="sxs-lookup"><span data-stu-id="a884b-107">Follow these steps to add, set up, or continue setting up a domain.</span></span> 

::: moniker range="o365-worldwide"

1. <span data-ttu-id="a884b-108">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span><span class="sxs-lookup"><span data-stu-id="a884b-108">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

::: moniker-end
::: moniker range="o365-germany"

1. <span data-ttu-id="a884b-109">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">https://portal.office.de/adminportal</a>.</span><span class="sxs-lookup"><span data-stu-id="a884b-109">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">https://portal.office.de/adminportal</a>.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="a884b-110">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">https://portal.partner.microsoftonline.cn</a>.</span><span class="sxs-lookup"><span data-stu-id="a884b-110">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">https://portal.partner.microsoftonline.cn</a>.</span></span>

::: moniker-end
    
2. <span data-ttu-id="a884b-111">Go to the **Paramètres**  >  **Domains** page.</span><span class="sxs-lookup"><span data-stu-id="a884b-111">Go to the **Settings** > **Domains** page.</span></span> 

3. <span data-ttu-id="a884b-112">Sélectionnez **Ajouter un domaine**.</span><span class="sxs-lookup"><span data-stu-id="a884b-112">Select **Add domain**.</span></span>
    
4. <span data-ttu-id="a884b-113">Entrez le nom du domaine que vous souhaitez ajouter, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a884b-113">Enter the name of the domain you want to add, then select **Next**.</span></span>
    
5. <span data-ttu-id="a884b-114">Choisissez la façon dont vous souhaitez vérifier que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="a884b-114">Choose how you want to verify that you own the domain.</span></span>
    
    1. <span data-ttu-id="a884b-115">Si votre bureau d’enregistrement de domaines utilise [domain Connecter](#domain-connect-registrars-integrating-with-microsoft-365), [Microsoft](../get-help-with-domains/domain-connect.md) configurera automatiquement vos enregistrements en vous connectant à votre bureau d’enregistrement et en confirmant la connexion à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a884b-115">If your domain registrar uses [Domain Connect](#domain-connect-registrars-integrating-with-microsoft-365), Microsoft [will set up your records automatically](../get-help-with-domains/domain-connect.md) by having you sign in to your registrar and confirm the connection to Microsoft 365.</span></span> <span data-ttu-id="a884b-116">Vous êtes renvoyé au Centre d’administration et Microsoft vérifie automatiquement votre domaine.</span><span class="sxs-lookup"><span data-stu-id="a884b-116">You'll be returned to the admin center and Microsoft will then automatically verify your domain.</span></span>
    2. <span data-ttu-id="a884b-117">Vous pouvez utiliser un enregistrement TXT pour vérifier votre domaine.</span><span class="sxs-lookup"><span data-stu-id="a884b-117">You can use a TXT record to verify your domain.</span></span> <span data-ttu-id="a884b-118">Sélectionnez ceci et **sélectionnez Suivant** pour voir les instructions d’ajout de cet enregistrement DNS au site web de votre bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a884b-118">Select this and select **Next** to see instructions for how to add this DNS record to your registrar's website.</span></span> <span data-ttu-id="a884b-119">La vérification peut prendre jusqu’à 30 minutes après l’ajout de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a884b-119">This can take up to 30 minutes to verify after you've added the record.</span></span> 
    3. <span data-ttu-id="a884b-120">Vous pouvez ajouter un fichier texte au site web de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="a884b-120">You can add a text file to your domain's website.</span></span> <span data-ttu-id="a884b-121">Sélectionnez et téléchargez le .txt à partir de l’Assistant Installation, puis téléchargez le fichier dans le dossier de niveau supérieur de votre site web.</span><span class="sxs-lookup"><span data-stu-id="a884b-121">Select and download the .txt file from the setup wizard, then upload the file to your website's top level folder.</span></span> <span data-ttu-id="a884b-122">Le chemin d’accès au fichier doit ressembler à : `http://mydomain.com/ms39978200.txt` .</span><span class="sxs-lookup"><span data-stu-id="a884b-122">The path to the file should look similar to: `http://mydomain.com/ms39978200.txt`.</span></span> <span data-ttu-id="a884b-123">Nous vous confirmerons que vous êtes propriétaire du domaine en trouvant le fichier sur votre site web.</span><span class="sxs-lookup"><span data-stu-id="a884b-123">We'll confirm you own the domain by finding the file on your website.</span></span>
    
6. <span data-ttu-id="a884b-124">Choisissez la façon dont vous souhaitez apporter les modifications DNS requises pour que Microsoft utilise votre domaine.</span><span class="sxs-lookup"><span data-stu-id="a884b-124">Choose how you want to make the DNS changes required for Microsoft to use your domain.</span></span>
    
    1. <span data-ttu-id="a884b-125">Choisissez Ajouter les enregistrements **DNS** pour moi si votre bureau d’enregistrement prend en charge [domain Connecter](#domain-connect-registrars-integrating-with-microsoft-365)et [Microsoft](../get-help-with-domains/domain-connect.md) configurera vos enregistrements automatiquement en vous connectant à votre bureau d’enregistrement et en confirmant la connexion à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a884b-125">Choose **Add the DNS records for me** if your registrar supports [Domain Connect](#domain-connect-registrars-integrating-with-microsoft-365), and Microsoft [will set up your records automatically](../get-help-with-domains/domain-connect.md) by having you sign in to your registrar and confirm the connection to Microsoft 365.</span></span>
    2. <span data-ttu-id="a884b-126">Choisissez **J’ajouterai** les enregistrements DNS moi-même si vous souhaitez joindre uniquement des services Microsoft 365 spécifiques à votre domaine ou si vous souhaitez ignorer cette étape pour l’instant et le faire ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="a884b-126">Choose **I'll add the DNS records myself** if you want to attach only specific Microsoft 365 services to your domain or if you want to skip this for now and do this later.</span></span> <span data-ttu-id="a884b-127">**Choisissez cette option si vous savez exactement ce que vous faites.**</span><span class="sxs-lookup"><span data-stu-id="a884b-127">**Choose this option if you know exactly what you're doing.**</span></span>

7. <span data-ttu-id="a884b-128">Si vous avez choisi d’ajouter vous-même des enregistrements *DNS,*  sélectionnez **Suivant** et vous verrez une page avec tous les enregistrements que vous devez ajouter à votre site web de bureau d’enregistrement pour configurer votre domaine.</span><span class="sxs-lookup"><span data-stu-id="a884b-128">If you chose to *add DNS records yourself*  , select **Next** and you'll see a page with all the records that you need to add to your registrars website to set up your domain.</span></span> 

    <span data-ttu-id="a884b-129">Si le portail ne reconnaît pas votre bureau d'enregistrement, vous pouvez [suivre ces instructions générales](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a884b-129">If the portal doesn't recognize your registrar, you can [follow these general instructions.](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md)</span></span>
    
    <span data-ttu-id="a884b-130">Si vous ne connaissez pas le fournisseur d'hébergement DNS ou le bureau d'enregistrement pour votre domaine, voir [Rechercher mon bureau d'enregistrement de domaines ou mon fournisseur d'hébergement DNS](../get-help-with-domains/find-your-domain-registrar.md).</span><span class="sxs-lookup"><span data-stu-id="a884b-130">If you don't know the DNS hosting provider or domain registrar for your domain, see [Find your domain registrar or DNS hosting provider](../get-help-with-domains/find-your-domain-registrar.md).</span></span>
    
    <span data-ttu-id="a884b-131">Si vous souhaitez attendre plus tard, désélectionnez tous les services et cliquez sur **Continuer,** ou à l’étape précédente de connexion de domaine, sélectionnez Plus **d’options** et sélectionnez Ignorer cette option **pour le moment.**</span><span class="sxs-lookup"><span data-stu-id="a884b-131">If you want to wait for later, either unselect all the services and click **Continue**, or in the previous domain connection step choose **More Options** and select **Skip this for now**.</span></span>
    
8. <span data-ttu-id="a884b-132">Select **Finish** - you’re done!</span><span class="sxs-lookup"><span data-stu-id="a884b-132">Select **Finish** - you're done!</span></span>

## <a name="add-or-edit-custom-dns-records"></a><span data-ttu-id="a884b-133">Ajouter ou modifier des enregistrements DNS personnalisés</span><span class="sxs-lookup"><span data-stu-id="a884b-133">Add or edit custom DNS records</span></span>

<span data-ttu-id="a884b-134">Suivez les étapes ci-dessous pour ajouter un enregistrement personnalisé pour un site web ou un service tiers.</span><span class="sxs-lookup"><span data-stu-id="a884b-134">Follow the steps below to add a custom record for a website or 3rd party service.</span></span>

1. <span data-ttu-id="a884b-135">Connectez-vous au Centre d’administration Microsoft à <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> l’adresse .</span><span class="sxs-lookup"><span data-stu-id="a884b-135">Sign in to the Microsoft admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

2. <span data-ttu-id="a884b-136">Go to the **Paramètres**   >  **Domains** page.</span><span class="sxs-lookup"><span data-stu-id="a884b-136">Go to the **Settings**  > **Domains** page.</span></span>

3. <span data-ttu-id="a884b-137">Dans la page **Domaines**, sélectionnez un domaine.</span><span class="sxs-lookup"><span data-stu-id="a884b-137">On the **Domains** page, select a domain.</span></span> 
    
4. <span data-ttu-id="a884b-138">Sous **paramètres DNS,** sélectionnez **Enregistrements personnalisés**; puis **sélectionnez Nouvel enregistrement personnalisé.**</span><span class="sxs-lookup"><span data-stu-id="a884b-138">Under **DNS settings**, select **Custom Records**; then select **New custom record**.</span></span>

5. <span data-ttu-id="a884b-139">Sélectionnez le type d’enregistrement DNS à ajouter et tapez les informations du nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a884b-139">Select the type of DNS record you want to add and type the information for the new record.</span></span>
    
6. <span data-ttu-id="a884b-140">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a884b-140">Select **Save**.</span></span>

## <a name="registrars-with-domain-connect"></a><span data-ttu-id="a884b-141">Bureaux d’enregistrement avec Connecter</span><span class="sxs-lookup"><span data-stu-id="a884b-141">Registrars with Domain Connect</span></span>

<span data-ttu-id="a884b-142">[Les Connecter](https://www.domainconnect.org/) bureaux d’enregistrement activés vous permettent d’ajouter votre domaine à Microsoft 365 dans un processus en trois étapes qui prend quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="a884b-142">[Domain Connect](https://www.domainconnect.org/) enabled registrars let you add your domain to Microsoft 365 in a three-step process that takes minutes.</span></span> 
  
<span data-ttu-id="a884b-143">Dans l’Assistant, nous allons simplement confirmer que vous êtes propriétaire du domaine, puis configurer automatiquement les enregistrements de votre domaine, afin que le courrier électronique soit envoyé à Microsoft 365 et d’autres services Microsoft 365, tels que Teams, fonctionnent avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="a884b-143">In the wizard, we'll just confirm that you own the domain, and then automatically set up your domain's records, so email comes to Microsoft 365 and other Microsoft 365 services, like Teams, work with your domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a884b-144">Veillez à désactiver les bloqueurs de fenêtres contextuelles dans votre navigateur avant de démarrer l'Assistant de configuration.</span><span class="sxs-lookup"><span data-stu-id="a884b-144">Make sure you disable any popup blockers in your browser before you start the setup wizard.</span></span>
  
### <a name="domain-connect-registrars-integrating-with-microsoft-365"></a><span data-ttu-id="a884b-145">Intégration Connecter bureaux d’enregistrement de domaines Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a884b-145">Domain Connect registrars integrating with Microsoft 365</span></span>

- [<span data-ttu-id="a884b-146">1 &amp; 1 IONOS</span><span class="sxs-lookup"><span data-stu-id="a884b-146">1&amp;1 IONOS</span></span>](https://www.1and1.com/)
- [<span data-ttu-id="a884b-147">EuroDNS</span><span class="sxs-lookup"><span data-stu-id="a884b-147">EuroDNS</span></span>](https://www.eurodns.com/)
- [<span data-ttu-id="a884b-148">Cloudflare</span><span class="sxs-lookup"><span data-stu-id="a884b-148">Cloudflare</span></span>](https://www.cloudflare.com/)
- [<span data-ttu-id="a884b-149">GoDaddy</span><span class="sxs-lookup"><span data-stu-id="a884b-149">GoDaddy</span></span>](https://www.godaddy.com/)
- [<span data-ttu-id="a884b-150">WordPress.com</span><span class="sxs-lookup"><span data-stu-id="a884b-150">WordPress.com</span></span>](https://wordpress.com/)
- [<span data-ttu-id="a884b-151">Iquésk</span><span class="sxs-lookup"><span data-stu-id="a884b-151">Plesk</span></span>](https://www.plesk.com/)
- [<span data-ttu-id="a884b-152">MediaTemple</span><span class="sxs-lookup"><span data-stu-id="a884b-152">MediaTemple</span></span>](https://mediatemple.net/)
- <span data-ttu-id="a884b-153">SecureServer ou WildWestDomains (revendeurs GoDaddy utilisant l’hébergement DNS SecureServer)</span><span class="sxs-lookup"><span data-stu-id="a884b-153">SecureServer or WildWestDomains (GoDaddy resellers using SecureServer DNS hosting)</span></span>
    - <span data-ttu-id="a884b-154">Exemples :</span><span class="sxs-lookup"><span data-stu-id="a884b-154">Examples:</span></span>
        - [<span data-ttu-id="a884b-155">DomainsPricedRight</span><span class="sxs-lookup"><span data-stu-id="a884b-155">DomainsPricedRight</span></span>](https://www.domainspricedright.com/products/domain-registration)
        - [<span data-ttu-id="a884b-156">DomainRightNow</span><span class="sxs-lookup"><span data-stu-id="a884b-156">DomainRightNow</span></span>](https://www.domainrightnow.com/)

### <a name="what-happens-to-my-email-and-website"></a><span data-ttu-id="a884b-157">Qu’arrive-t-il à mon courrier électronique et mon site web ?</span><span class="sxs-lookup"><span data-stu-id="a884b-157">What happens to my email and website?</span></span>

<span data-ttu-id="a884b-158">Une fois que vous avez terminé l’installation, l’enregistrement MX de votre domaine est mis à jour pour pointer vers Microsoft 365 et tous les e-mails de votre domaine commenceront à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a884b-158">After you finish setup, the MX record for your domain is updated to point to Microsoft 365 and all email for your domain will start coming to Microsoft 365.</span></span> <span data-ttu-id="a884b-159">Assurez-vous d’avoir ajouté des utilisateurs et de configurer des boîtes aux lettres dans Microsoft 365 pour toutes les personnes qui reçoit du courrier électronique sur votre domaine !</span><span class="sxs-lookup"><span data-stu-id="a884b-159">Make sure you've added users and set up mailboxes in Microsoft 365 for everyone who gets email on your domain!</span></span>
  
<span data-ttu-id="a884b-160">Si vous avez un site web que vous utilisez dans le cadre de votre activité, il continuera à fonctionner là où il se trouve.</span><span class="sxs-lookup"><span data-stu-id="a884b-160">If you have a website that you use with your business, it will keep working where it is.</span></span> <span data-ttu-id="a884b-161">Les étapes de Connecter domaine n’affectent pas votre site web.</span><span class="sxs-lookup"><span data-stu-id="a884b-161">The Domain Connect setup steps don't affect your website.</span></span>

## <a name="related-content"></a><span data-ttu-id="a884b-162">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="a884b-162">Related content</span></span>

<span data-ttu-id="a884b-163">[FAQ sur les domaines](domains-faq.yml) (article)</span><span class="sxs-lookup"><span data-stu-id="a884b-163">[Domains FAQ](domains-faq.yml) (article)</span></span>\
[<span data-ttu-id="a884b-164">Qu’est-ce qu’un domaine ?</span><span class="sxs-lookup"><span data-stu-id="a884b-164">What is a domain?</span></span>](../get-help-with-domains/what-is-a-domain.md) <span data-ttu-id="a884b-165">(article)</span><span class="sxs-lookup"><span data-stu-id="a884b-165">(article)</span></span>\
<span data-ttu-id="a884b-166">[Acheter un nom de domaine dans Microsoft 365](../get-help-with-domains/buy-a-domain-name.md) (article)</span><span class="sxs-lookup"><span data-stu-id="a884b-166">[Buy a domain name in Microsoft 365](../get-help-with-domains/buy-a-domain-name.md) (article)</span></span>\
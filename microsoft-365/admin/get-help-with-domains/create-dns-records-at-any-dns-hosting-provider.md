---
title: Ajouter des enregistrements DNS pour connecter votre domaine
f1.keywords:
- CSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- Adm_O365_Setup
search.appverid:
- MET150
description: Apprenez à vérifier votre domaine et à créer des enregistrements DNS auprès d’un fournisseur d'hébergement DNS pour Microsoft 365.
ms.custom:
- okr_smb
- AdminSurgePortfolio
ms.openlocfilehash: d3a9e3787afc30b33122edf91c1cf9e3dd84b847
ms.sourcegitcommit: 7c1b34205746ff0690ffc774a74bdfd434256cf5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2020
ms.locfileid: "45049665"
---
# <a name="add-dns-records-to-connect-your-domain"></a><span data-ttu-id="2fd6e-103">Ajouter des enregistrements DNS pour connecter votre domaine</span><span class="sxs-lookup"><span data-stu-id="2fd6e-103">Add DNS records to connect your domain</span></span>

<span data-ttu-id="2fd6e-104">Si vous avez acheté un domaine auprès d’un fournisseur d’hébergement tiers, vous pouvez le connecter à Microsoft 365 en mettant à jour les enregistrements DNS dans le compte de votre bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-104">If you purchased a domain from a third-party hosting provider, you can connect it to Microsoft 365 by updating the DNS records in your registrar’s account.</span></span>

<span data-ttu-id="2fd6e-105">À la fin de ces étapes, votre domaine reste enregistré auprès de l’hôte à qui vous avez acheté le domaine, mais Microsoft 365 peut l’utiliser pour vos adresses de messagerie (telles que utilisateur@votredomaine.com) et d’autres services.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-105">At the end of these steps, your domain will stay registered with the host that you purchased the domain from, but Microsoft 365 can use it for you email addresses (like user@yourdomain.com) and other services.</span></span>

<span data-ttu-id="2fd6e-106">Si vous n’ajoutez pas de domaine, les membres de votre organisation utiliseront le domaine onmicrosoft.com pour leur adresse de messagerie jusqu’à ce que vous le fassiez.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-106">If you don't add a domain, people in your organization will use the onmicrosoft.com domain for their email addresses until you do.</span></span> <span data-ttu-id="2fd6e-107">Il est important d’ajouter votre domaine avant d’ajouter des utilisateurs, de sorte que vous n’ayez pas à les reconfigurer.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-107">It's important to add your domain before you add users, so you don't have to set them up twice.</span></span>

<span data-ttu-id="2fd6e-108">[Consultez la FAQ dédiée aux domaines](../setup/domains-faq.md) si vous ne trouvez pas ci-dessous ce que vous recherchez .</span><span class="sxs-lookup"><span data-stu-id="2fd6e-108">[Check the Domains FAQ](../setup/domains-faq.md) if you don't find what you're looking for below.</span></span>

## <a name="step-1-add-a-txt-record-to-verify-you-own-the-domain"></a><span data-ttu-id="2fd6e-109">Étape 1 : Ajouter un enregistrement TXT pour vérifier que vous êtes propriétaire du domaine</span><span class="sxs-lookup"><span data-stu-id="2fd6e-109">Step 1: Add a TXT record to verify you own the domain</span></span>

<span data-ttu-id="2fd6e-110">Vous devez tout d’abord prouver que vous êtes le propriétaire du domaine que vous voulez ajouter à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-110">First, you need to prove you own the domain you want to add to Microsoft 365.</span></span>

1. <span data-ttu-id="2fd6e-111">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com/), puis sélectionnez **Afficher tout** > **Paramètres** > **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-111">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/) and select **Show all** > **Settings** > **Domains**.</span></span>
2. <span data-ttu-id="2fd6e-112">Dans un nouvel onglet ou une nouvelle fenêtre de navigateur, connectez-vous à votre fournisseur d’hébergement DNS, puis recherchez l’emplacement où vous gérez vos paramètres DNS (par exemple, Paramètres de fichier de zone, Gérer les domaines, Gestionnaire de domaine, Gestionnaire DNS).</span><span class="sxs-lookup"><span data-stu-id="2fd6e-112">In a new browser tab or window, sign in to your DNS hosting provider, and then find where you manage your DNS settings (e.g., Zone File Settings, Manage Domains, Domain Manager, DNS Manager).</span></span>
3. <span data-ttu-id="2fd6e-113">Accédez à la page Gestionnaire DNS de votre fournisseur et ajoutez à votre domaine l’enregistrement TXT indiqué dans le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-113">Go to your provider's DNS Manager page, and add the TXT record indicated in the admin center to your domain.</span></span>

<span data-ttu-id="2fd6e-114">L’ajout de cet enregistrement n’affecte pas votre e-mail ou les autres services existants, et vous pouvez le supprimer de façon sécurisée une fois que votre domaine est connecté à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-114">Adding this record won't affect your existing email or other services and you can safely remove it once your domain is connected to Microsoft 365.</span></span>

<span data-ttu-id="2fd6e-115">Exemple :</span><span class="sxs-lookup"><span data-stu-id="2fd6e-115">Example:</span></span>
- <span data-ttu-id="2fd6e-116">Nom TXT : `@`</span><span class="sxs-lookup"><span data-stu-id="2fd6e-116">TXT Name: `@`</span></span>
- <span data-ttu-id="2fd6e-117">Valeur TXT : MS = MS # # # # # # # # (ID unique du centre d’administration)</span><span class="sxs-lookup"><span data-stu-id="2fd6e-117">TXT Value: MS=ms######## (unique ID from the admin center)</span></span>
- <span data-ttu-id="2fd6e-118">TTL : `3600‎` (ou votre fournisseur par défaut)</span><span class="sxs-lookup"><span data-stu-id="2fd6e-118">TTL: `3600‎` (or your provider default)</span></span>

4. <span data-ttu-id="2fd6e-119">Sauvegardez l’enregistrement, revenez au centre d’administration, puis sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-119">Save the record, go back to the admin center, and then select **Verify**.</span></span> <span data-ttu-id="2fd6e-120">Il faut généralement 15 minutes pour que les modifications apportées aux enregistrements soient enregistrées, mais cela peut prendre plus de temps.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-120">It typically takes around 15 minutes for record changes to register, but sometimes it can take longer.</span></span> <span data-ttu-id="2fd6e-121">Accordez un peu de temps et quelques tentatives pour récupérer la modification.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-121">Give it some time and a few tries to pick up the change.</span></span>

<span data-ttu-id="2fd6e-122">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-122">When Microsoft finds the correct TXT record, your domain is verified.</span></span>


## <a name="step-2-add-dns-records-to-connect-microsoft-services"></a><span data-ttu-id="2fd6e-123">Étape 2 : ajouter des enregistrements DNS pour connecter les services Microsoft</span><span class="sxs-lookup"><span data-stu-id="2fd6e-123">Step 2: Add DNS records to connect Microsoft services</span></span>

<span data-ttu-id="2fd6e-124">Dans un nouvel onglet ou une nouvelle fenêtre de navigateur, connectez-vous à votre fournisseur d’hébergement DNS, puis recherchez l’emplacement où vous gérez vos paramètres DNS (par exemple, Paramètres de fichier de zone, Gérer les domaines, Gestionnaire de domaine, Gestionnaire DNS).</span><span class="sxs-lookup"><span data-stu-id="2fd6e-124">In a new browser tab or window, sign in to your DNS hosting provider, and find where you manage your DNS settings (e.g., Zone File Settings, Manage Domains, Domain Manager, DNS Manager).</span></span>

<span data-ttu-id="2fd6e-125">Vous pourrez ajouter plusieurs types d’enregistrements DNS selon les services que vous voulez activer.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-125">You'll be adding several different types of DNS records depending on the services you want to enable.</span></span> 

### <a name="add-an-mx-record-for-email-outlook-exchange-online"></a><span data-ttu-id="2fd6e-126">Ajouter un enregistrement MX pour la messagerie électronique (Outlook, Exchange Online)</span><span class="sxs-lookup"><span data-stu-id="2fd6e-126">Add an MX record for email (Outlook, Exchange Online)</span></span>
<span data-ttu-id="2fd6e-127">**Avant de commencer :** si les utilisateurs disposent déjà d’une adresse de messagerie avec votre domaine (par exemple, utilisateur@votredomaine.com), créez leur compte dans le centre d’administration avant de configurer vos enregistrements MX.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-127">**Before you begin:** If users already have email with your domain (such as user@yourdomain.com), create their accounts in the admin center before you set up your MX records.</span></span> <span data-ttu-id="2fd6e-128">Ainsi, ils continueront à recevoir du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-128">That way, they’ll continue to receive email.</span></span> <span data-ttu-id="2fd6e-129">Lorsque vous mettez à jour l’enregistrement MX de votre domaine, tout nouveau message électronique adressé à une personne utilisant votre domaine mène désormais vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-129">When you update your domain's MX record, all new email for anyone who uses your domain will now come to Microsoft 365.</span></span> <span data-ttu-id="2fd6e-130">Un courrier électronique que vous avez déjà reste chez votre hôte de courrier actuel, sauf si vous décidez de [migrer les courriers électroniques et contacts vers Microsoft 365.](../setup/migrate-email-and-contacts-admin.md)</span><span class="sxs-lookup"><span data-stu-id="2fd6e-130">Any email you already have will stay at your current email host, unless you decide to [migrate email and contacts to Microsoft 365.](../setup/migrate-email-and-contacts-admin.md)</span></span>

<span data-ttu-id="2fd6e-131">Vous obtiendrez les informations relatives à l’enregistrement MX à partir de l’Assistant Configuration du domaine du centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-131">You'll get the information for the MX record from the admin center domain setup wizard.</span></span>

<span data-ttu-id="2fd6e-132">Sur le site Web de votre fournisseur d’hébergement, créez un nouvel enregistrement MX.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-132">On your hosting provider's website, add a new MX record.</span></span>
<span data-ttu-id="2fd6e-133">Vérifiez que les champs sont définis par les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2fd6e-133">Make sure that the fields are set to the following values:</span></span>

- <span data-ttu-id="2fd6e-134">Type d’enregistrement : `MX`</span><span class="sxs-lookup"><span data-stu-id="2fd6e-134">Record Type: `MX`</span></span>
- <span data-ttu-id="2fd6e-135">Priorité : sélectionnez la valeur la plus élevée disponible, généralement `0`.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-135">Priority: Set to the highest value available, typically `0`.</span></span>
- <span data-ttu-id="2fd6e-136">Nom de l’hôte : `@`</span><span class="sxs-lookup"><span data-stu-id="2fd6e-136">Host Name: `@`</span></span>
- <span data-ttu-id="2fd6e-137">Adresse de pointage : copiez la valeur à partir du centre d’administration et collez-la ici.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-137">Points to address: Copy the value from the admin center and paste it here.</span></span>
- <span data-ttu-id="2fd6e-138">TTL : `3600‎` (ou votre fournisseur par défaut)</span><span class="sxs-lookup"><span data-stu-id="2fd6e-138">TTL: `3600‎` (or your provider default)</span></span>

<span data-ttu-id="2fd6e-139">Sauvegardez l’enregistrement et supprimez tous les autres enregistrements MX.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-139">Save the record, and then remove any other MX records.</span></span>

### <a name="add-cname-records-to-connect-other-services-teams-exchange-online-aad-mdm"></a><span data-ttu-id="2fd6e-140">Ajouter des enregistrements CNAME pour connecter d’autres services (Teams, Exchange Online, AAD, MDM)</span><span class="sxs-lookup"><span data-stu-id="2fd6e-140">Add CNAME records to connect other services (Teams, Exchange Online, AAD, MDM)</span></span>
<span data-ttu-id="2fd6e-141">Vous obtiendrez les informations relatives aux enregistrements CNAME à partir de l’Assistant Configuration du domaine du centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-141">You'll get the information for the CNAME records from the admin center domain setup wizard.</span></span>

<span data-ttu-id="2fd6e-142">Sur le site Web de votre fournisseur d’hébergement, ajoutez les enregistrements CNAME pour chaque service auquel vous voulez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-142">On your hosting provider's website, add CNAME records for each service that you want to connect.</span></span>
<span data-ttu-id="2fd6e-143">Dans le nouvel enregistrement, vérifiez que chacun des champs sont définis par les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2fd6e-143">Make sure that the fields are set to the following values for each:</span></span>

- <span data-ttu-id="2fd6e-144">Type d’enregistrement : `CNAME (Alias)`</span><span class="sxs-lookup"><span data-stu-id="2fd6e-144">Record Type: `CNAME (Alias)`</span></span>
- <span data-ttu-id="2fd6e-145">Hôte : collez les valeurs que vous copiez à partir du centre d’administration ici.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-145">Host: Paste the values you copy from the admin center here.</span></span>
- <span data-ttu-id="2fd6e-146">Adresse de pointage : copiez la valeur à partir du centre d’administration et collez-la ici.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-146">Points to address: Copy the value from the admin center and paste it here.</span></span>
- <span data-ttu-id="2fd6e-147">TTL : `3600‎` (ou votre fournisseur par défaut)</span><span class="sxs-lookup"><span data-stu-id="2fd6e-147">TTL: `3600‎` (or your provider default)</span></span>


### <a name="add-or-edit-an-spf-txt-record-to-help-prevent-email-spam-outlook-exchange-online"></a><span data-ttu-id="2fd6e-148">Ajouter ou modifier un enregistrement TXT SPF afin d’éviter les courriers indésirables (Outlook, Exchange Online)</span><span class="sxs-lookup"><span data-stu-id="2fd6e-148">Add or edit an SPF TXT record to help prevent email spam (Outlook, Exchange Online)</span></span>
<span data-ttu-id="2fd6e-149">**Avant de commencer :** Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-149">**Before you begin:** If you already have an SPF record for your domain, don't create a new one for Microsoft 365.</span></span> <span data-ttu-id="2fd6e-150">Ajoutez plutôt les valeurs Microsoft 365 requises à l’enregistrement actuel sur le site Web de votre fournisseur d’hébergement de manière à n’avoir qu’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-150">Instead, add the required Microsoft 365 values to the current record on your hosting providers website so that you have a *single* SPF record that includes both sets of values.</span></span>

<span data-ttu-id="2fd6e-151">Sur le site web de votre fournisseur d’hébergement, modifiez l'enregistrement SPF existant ou créez un enregistrement SPF.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-151">On your hosting provider's website, edit the existing SPF record or create an SPF record.</span></span>
<span data-ttu-id="2fd6e-152">Vérifiez que les champs sont définis par les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2fd6e-152">Make sure that the fields are set to the following values:</span></span>

- <span data-ttu-id="2fd6e-153">Type d’enregistrement : `TXT (Text)`</span><span class="sxs-lookup"><span data-stu-id="2fd6e-153">Record Type: `TXT (Text)`</span></span>
- <span data-ttu-id="2fd6e-154">Hôte : `@`</span><span class="sxs-lookup"><span data-stu-id="2fd6e-154">Host: `@`</span></span>
- <span data-ttu-id="2fd6e-155">Valeur TXT :`v=spf1 include:spf.protection.outlook.com -all`</span><span class="sxs-lookup"><span data-stu-id="2fd6e-155">TXT Value: `v=spf1 include:spf.protection.outlook.com -all`</span></span>
- <span data-ttu-id="2fd6e-156">TTL : `3600‎` (ou votre fournisseur par défaut)</span><span class="sxs-lookup"><span data-stu-id="2fd6e-156">TTL: `3600‎` (or your provider default)</span></span>

<span data-ttu-id="2fd6e-157">Enregistrez l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-157">Save the record.</span></span>

<span data-ttu-id="2fd6e-158">Validez votre enregistrement SPF en utilisant l'un des [Outils de validation SPF](https://docs.microsoft.com/office365/admin/setup/domains-faq#how-can-i-validate-spf-records-for-my-domain) suivants</span><span class="sxs-lookup"><span data-stu-id="2fd6e-158">Validate your SPF record by using one of these [SPF validation tools](https://docs.microsoft.com/office365/admin/setup/domains-faq#how-can-i-validate-spf-records-for-my-domain)</span></span>

<span data-ttu-id="2fd6e-159">SPF est conçu pour lutter contre l’usurpation d’adresse, mais il existe des techniques d’usurpation d’adresse contre lesquelles SPF ne peut rien faire.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-159">SPF is designed to help prevent spoofing, but there are spoofing techniques that SPF cannot protect against.</span></span> <span data-ttu-id="2fd6e-160">Pour vous protéger contre ces techniques, une fois que vous avez configuré votre SPF, vous devez également configurer DKIM et DMARC pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-160">To protect against these, once you've set up SPF, you should also set up DKIM and DMARC for Microsoft 365.</span></span> 

<span data-ttu-id="2fd6e-161">Pour commencer, consultez la rubrique [Utilisation du DKIM pour valider les e-mails sortants envoyés à partir de votre domaine dans Microsoft 365](https://technet.microsoft.com/library/mt695945%28v=exchg.150%29.aspx) et [Utilisation du DMARC pour valider les e-mails dans Microsoft 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2fd6e-161">To get started, see [Use DKIM to validate outbound email sent from your domain in Microsoft 365](https://technet.microsoft.com/library/mt695945%28v=exchg.150%29.aspx) and [Use DMARC to validate email in Microsoft 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).</span></span>

### <a name="add-srv-records-for-communications-services-teams-skype-for-business"></a><span data-ttu-id="2fd6e-162">Ajouter des enregistrements SRV pour les services de communications (Teams, Skype Entreprise)</span><span class="sxs-lookup"><span data-stu-id="2fd6e-162">Add SRV records for communications services (Teams, Skype for Business)</span></span>

<span data-ttu-id="2fd6e-163">Sur le site Web de votre fournisseur d’hébergement, ajoutez les enregistrements SRV pour chaque service auquel vous voulez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-163">On your hosting provider's website, add SRV records for each service you want to connect.</span></span>
<span data-ttu-id="2fd6e-164">Dans le nouvel enregistrement, vérifiez que chacun des champs sont définis par les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2fd6e-164">Make sure that the fields are set to the following values for each:</span></span>

- <span data-ttu-id="2fd6e-165">Type d’enregistrement : `SRV (Service)`</span><span class="sxs-lookup"><span data-stu-id="2fd6e-165">Record Type: `SRV (Service)`</span></span>
- <span data-ttu-id="2fd6e-166">Nom : `@`</span><span class="sxs-lookup"><span data-stu-id="2fd6e-166">Name: `@`</span></span>
- <span data-ttu-id="2fd6e-167">Cible : copiez la valeur à partir du centre d’administration et collez-la ici.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-167">Target: Copy the value from the admin center and paste it here.</span></span>
- <span data-ttu-id="2fd6e-168">Protocole : copiez la valeur à partir du centre d’administration et collez-la ici.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-168">Protocol: Copy the value from the admin center and paste it here.</span></span>
- <span data-ttu-id="2fd6e-169">Service : copiez la valeur à partir du centre d’administration et collez-la ici.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-169">Service: Copy the value from the admin center and paste it here.</span></span>
- <span data-ttu-id="2fd6e-170">Priorité : `100`</span><span class="sxs-lookup"><span data-stu-id="2fd6e-170">Priority: `100`</span></span>
- <span data-ttu-id="2fd6e-171">Poids : `1`</span><span class="sxs-lookup"><span data-stu-id="2fd6e-171">Weight: `1`</span></span>
- <span data-ttu-id="2fd6e-172">Port : copiez la valeur à partir du centre d’administration et collez-la ici.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-172">Port: Copy the value from the admin center and paste it here.</span></span>
- <span data-ttu-id="2fd6e-173">TTL : `3600‎` (ou votre fournisseur par défaut)</span><span class="sxs-lookup"><span data-stu-id="2fd6e-173">TTL: `3600‎` (or your provider default)</span></span>

<span data-ttu-id="2fd6e-174">Enregistrez l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-174">Save the record.</span></span>

#### <a name="srv-record-field-restrictions-and-workarounds"></a><span data-ttu-id="2fd6e-175">Restrictions relatives aux champs d’enregistrement SRV et solutions de contournement</span><span class="sxs-lookup"><span data-stu-id="2fd6e-175">SRV record field restrictions and workarounds</span></span>
<span data-ttu-id="2fd6e-176">Certains fournisseurs d’hébergement imposent des restrictions sur les valeurs de champs dans les enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-176">Some hosting providers impose restrictions on field values within SRV records.</span></span> <span data-ttu-id="2fd6e-177">Voici quelques solutions de contournement courantes pour ces restrictions.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-177">Here are some common workarounds for these restrictions.</span></span>

##### <a name="name"></a><span data-ttu-id="2fd6e-178">Nom</span><span class="sxs-lookup"><span data-stu-id="2fd6e-178">Name</span></span>
<span data-ttu-id="2fd6e-179">Si votre fournisseur d’hébergement n’autorise pas la définition de ce champ sur **@**, laissez ce champ vide.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-179">If your hosting provider doesn't allow setting this field to **@**, leave it blank.</span></span> <span data-ttu-id="2fd6e-180">Utilisez cette approche *uniquement* lorsque votre fournisseur d’hébergement utilise des champs distincts pour les valeurs Service et Protocole.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-180">Use this approach *only* when your hosting provider has separate fields for the Service and Protocol values.</span></span> <span data-ttu-id="2fd6e-181">Dans le cas contraire, consultez les notes sur les valeurs Service et Protocole ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-181">Otherwise, see the Service and Protocol notes below.</span></span>

##### <a name="service-and-protocol"></a><span data-ttu-id="2fd6e-182">Service et Protocole</span><span class="sxs-lookup"><span data-stu-id="2fd6e-182">Service and Protocol</span></span>
<span data-ttu-id="2fd6e-183">Si votre fournisseur d’hébergement ne fournit pas ces champs pour les enregistrements SRV, vous devez spécifier les valeurs de **Service** et **Protocole**dans le champ **Nom** de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-183">If your hosting provider doesn't provide these fields for SRV records, you must specify the **Service** and **Protocol** values in the record's **Name** field.</span></span> <span data-ttu-id="2fd6e-184">Remarque : suivant votre fournisseur d’hébergement, le champ **Nom** peut avoir une autre appellation, comme **Hôte**, **Nom de l’hôte** ou **Sous-domaine**. Pour ajouter ces valeurs, vous devez créer une seule chaîne, en séparant les valeurs par un point.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-184">(Note: Depending on your hosting provider, the **Name** field might be called something else, like: **Host**, **Hostname**, or **Subdomain**.) To add these values, you create a single string, separating the values with a dot.</span></span> 

<span data-ttu-id="2fd6e-185">Exemple : `_sip._tls`</span><span class="sxs-lookup"><span data-stu-id="2fd6e-185">Example: `_sip._tls`</span></span>

##### <a name="priority-weight-and-port-br"></a><span data-ttu-id="2fd6e-186">Priorité, Poids, et Port</span><span class="sxs-lookup"><span data-stu-id="2fd6e-186">Priority, Weight, and Port</span></span> <br>
<span data-ttu-id="2fd6e-187">Si votre fournisseur d’hébergement ne fournit pas ces champs pour les enregistrements SRV, vous devez spécifier ces valeurs dans le champs **Cible** de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-187">If your hosting provider doesn't provide these fields for SRV records, you must specify them in the record's **Target** field.</span></span> <span data-ttu-id="2fd6e-188">Remarque : selon votre fournisseur d’hébergement, le champ **Cible** peut être appelé différemment, comme **Contenu**, **Adresse IP**ou **Hôte cible**.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-188">(Note: Depending on your hosting provider, the **Target** field might be called something else, like: **Content**, **IP Address**, or **Target Host**.)</span></span> 

<span data-ttu-id="2fd6e-189">Pour ajouter ces valeurs, créez une seule chaîne, en séparant les valeurs par des espaces, *ou parfois par un point*. Si vous n’êtes pas sûr, consultez votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-189">To add these values, create a single string, separating the values with spaces and *sometimes ending with a dot* (check with your provider if you are unsure).</span></span> <span data-ttu-id="2fd6e-190">Les valeurs doivent être incluses dans l’ordre suivant : Priority (Priorité), Weight (Poids), Port (Port), Target (Cible).</span><span class="sxs-lookup"><span data-stu-id="2fd6e-190">The values must be included in this order: Priority, Weight, Port, Target.</span></span> 

- <span data-ttu-id="2fd6e-191">Exemple 1 : `100 1 443 sipdir.online.lync.com.`</span><span class="sxs-lookup"><span data-stu-id="2fd6e-191">Example 1: `100 1 443 sipdir.online.lync.com.`</span></span>
- <span data-ttu-id="2fd6e-192">Exemple 2 : `100 1 443 sipdir.online.lync.com`</span><span class="sxs-lookup"><span data-stu-id="2fd6e-192">Example 2: `100 1 443 sipdir.online.lync.com`</span></span>

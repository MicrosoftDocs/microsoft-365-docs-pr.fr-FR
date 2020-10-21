---
title: Ajouter des enregistrements DNS pour connecter votre domaine
f1.keywords:
- CSH
ms.author: pebaum
author: pebaum
manager: scotv
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
ms.openlocfilehash: 6c2359cbf2da24fa7e2cd579d61216d948e0cb83
ms.sourcegitcommit: 628f195cbe3c00910f7350d8b09997a675dde989
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "48645370"
---
# <a name="add-dns-records-to-connect-your-domain"></a><span data-ttu-id="10775-103">Ajouter des enregistrements DNS pour connecter votre domaine</span><span class="sxs-lookup"><span data-stu-id="10775-103">Add DNS records to connect your domain</span></span>

<span data-ttu-id="10775-104">Si vous avez acheté un domaine auprès d’un fournisseur d’hébergement tiers, vous pouvez le connecter à Microsoft 365 en mettant à jour les enregistrements DNS dans le compte de votre bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="10775-104">If you purchased a domain from a third-party hosting provider, you can connect it to Microsoft 365 by updating the DNS records in your registrar’s account.</span></span>

<span data-ttu-id="10775-105">À la fin de ces étapes, votre domaine reste enregistré auprès de l’hôte à qui vous avez acheté le domaine, mais Microsoft 365 peut l’utiliser pour vos adresses de messagerie (telles que utilisateur@votredomaine.com) et d’autres services.</span><span class="sxs-lookup"><span data-stu-id="10775-105">At the end of these steps, your domain will stay registered with the host that you purchased the domain from, but Microsoft 365 can use it for you email addresses (like user@yourdomain.com) and other services.</span></span>

<span data-ttu-id="10775-106">Si vous n’ajoutez pas de domaine, les membres de votre organisation utiliseront le domaine onmicrosoft.com pour leur adresse de messagerie jusqu’à ce que vous le fassiez.</span><span class="sxs-lookup"><span data-stu-id="10775-106">If you don't add a domain, people in your organization will use the onmicrosoft.com domain for their email addresses until you do.</span></span> <span data-ttu-id="10775-107">Il est important d’ajouter votre domaine avant d’ajouter des utilisateurs, de sorte que vous n’ayez pas à les reconfigurer.</span><span class="sxs-lookup"><span data-stu-id="10775-107">It's important to add your domain before you add users, so you don't have to set them up twice.</span></span>

<span data-ttu-id="10775-108">[Consultez la FAQ dédiée aux domaines](../setup/domains-faq.md) si vous ne trouvez pas ci-dessous ce que vous recherchez .</span><span class="sxs-lookup"><span data-stu-id="10775-108">[Check the Domains FAQ](../setup/domains-faq.md) if you don't find what you're looking for below.</span></span>

## <a name="step-1-add-a-txt-or-mx-record-to-verify-you-own-the-domain"></a><span data-ttu-id="10775-109">Étape 1 : Ajouter un enregistrement TXT ou MX pour vérifier que vous êtes propriétaire du domaine</span><span class="sxs-lookup"><span data-stu-id="10775-109">Step 1: Add a TXT or MX record to verify you own the domain</span></span>

### <a name="recommended-verify-with-a-txt-record"></a><span data-ttu-id="10775-110">Recommandé : vérifier avec un enregistrement TXT</span><span class="sxs-lookup"><span data-stu-id="10775-110">Recommended: Verify with a TXT record</span></span>

<span data-ttu-id="10775-111">Vous devez tout d’abord prouver que vous êtes le propriétaire du domaine que vous voulez ajouter à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="10775-111">First, you need to prove you own the domain you want to add to Microsoft 365.</span></span>

1. <span data-ttu-id="10775-112">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com/), puis sélectionnez **Afficher tout** > **Paramètres** > **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="10775-112">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/) and select **Show all** > **Settings** > **Domains**.</span></span>
2. <span data-ttu-id="10775-113">Dans un nouvel onglet ou une nouvelle fenêtre de navigateur, connectez-vous à votre fournisseur d’hébergement DNS, puis recherchez l’emplacement où vous gérez vos paramètres DNS (par exemple, Paramètres de fichier de zone, Gérer les domaines, Gestionnaire de domaine, Gestionnaire DNS).</span><span class="sxs-lookup"><span data-stu-id="10775-113">In a new browser tab or window, sign in to your DNS hosting provider, and then find where you manage your DNS settings (e.g., Zone File Settings, Manage Domains, Domain Manager, DNS Manager).</span></span>
3. <span data-ttu-id="10775-114">Accédez à la page Gestionnaire DNS de votre fournisseur et ajoutez à votre domaine l’enregistrement TXT indiqué dans le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="10775-114">Go to your provider's DNS Manager page, and add the TXT record indicated in the admin center to your domain.</span></span>

<span data-ttu-id="10775-115">L’ajout de cet enregistrement n’affecte pas votre e-mail ou les autres services existants, et vous pouvez le supprimer de façon sécurisée une fois que votre domaine est connecté à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="10775-115">Adding this record won't affect your existing email or other services and you can safely remove it once your domain is connected to Microsoft 365.</span></span>

<span data-ttu-id="10775-116">Exemple :</span><span class="sxs-lookup"><span data-stu-id="10775-116">Example:</span></span>
- <span data-ttu-id="10775-117">Nom TXT : `@`</span><span class="sxs-lookup"><span data-stu-id="10775-117">TXT Name: `@`</span></span>
- <span data-ttu-id="10775-118">Valeur TXT : MS = MS # # # # # # # # (ID unique du centre d’administration)</span><span class="sxs-lookup"><span data-stu-id="10775-118">TXT Value: MS=ms######## (unique ID from the admin center)</span></span>
- <span data-ttu-id="10775-119">TTL : `3600‎` (ou votre fournisseur par défaut)</span><span class="sxs-lookup"><span data-stu-id="10775-119">TTL: `3600‎` (or your provider default)</span></span>

4. <span data-ttu-id="10775-120">Sauvegardez l’enregistrement, revenez au centre d’administration, puis sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="10775-120">Save the record, go back to the admin center, and then select **Verify**.</span></span> <span data-ttu-id="10775-121">Il faut généralement 15 minutes pour que les modifications apportées aux enregistrements soient enregistrées, mais cela peut prendre plus de temps.</span><span class="sxs-lookup"><span data-stu-id="10775-121">It typically takes around 15 minutes for record changes to register, but sometimes it can take longer.</span></span> <span data-ttu-id="10775-122">Accordez un peu de temps et quelques tentatives pour récupérer la modification.</span><span class="sxs-lookup"><span data-stu-id="10775-122">Give it some time and a few tries to pick up the change.</span></span>

<span data-ttu-id="10775-123">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="10775-123">When Microsoft finds the correct TXT record, your domain is verified.</span></span>

### <a name="verify-with-an-mx-record"></a><span data-ttu-id="10775-124">Vérifier avec un enregistrement MX</span><span class="sxs-lookup"><span data-stu-id="10775-124">Verify with an MX record</span></span>

<span data-ttu-id="10775-125">Si votre bureau d’enregistrement ne prend pas en charge l’ajout d'enregistrements TXT, vous pouvez procéder à la vérification en ajoutant un enregistrement MX.</span><span class="sxs-lookup"><span data-stu-id="10775-125">If your registrar doesn't support adding TXT records, you can verify by adding an MX record.</span></span>

1. <span data-ttu-id="10775-126">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com/), puis sélectionnez **Afficher tout** > **Paramètres** > **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="10775-126">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/) and select **Show all** > **Settings** > **Domains**.</span></span>
2. <span data-ttu-id="10775-127">Dans un nouvel onglet ou une nouvelle fenêtre de navigateur, connectez-vous à votre fournisseur d’hébergement DNS, puis recherchez l’emplacement où vous gérez vos paramètres DNS (par exemple, Paramètres de fichier de zone, Gérer les domaines, Gestionnaire de domaine, Gestionnaire DNS).</span><span class="sxs-lookup"><span data-stu-id="10775-127">In a new browser tab or window, sign in to your DNS hosting provider, and then find where you manage your DNS settings (e.g., Zone File Settings, Manage Domains, Domain Manager, DNS Manager).</span></span>
3. <span data-ttu-id="10775-128">Accédez à la page Gestionnaire DNS de votre fournisseur et ajoutez à votre domaine l’enregistrement MX indiqué dans le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="10775-128">Go to your provider's DNS Manager page, and add the MX record indicated in the admin center to your domain.</span></span>

<span data-ttu-id="10775-129">La **Priorité** de cet enregistrement MX doit être la plus élevée de tous les enregistrements MX existants pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="10775-129">This MX record's **Priority** must be the highest of all existing MX records for the domain.</span></span> <span data-ttu-id="10775-130">Sinon, il peut interférer avec l'envoi et la réception d'e-mails.</span><span class="sxs-lookup"><span data-stu-id="10775-130">Otherwise, it can interfere with sending and receiving email.</span></span> <span data-ttu-id="10775-131">Vous devez supprimer ces enregistrements dès que la vérification du domaine est terminée.</span><span class="sxs-lookup"><span data-stu-id="10775-131">You should delete this records as soon as domain verification is complete.</span></span>

<span data-ttu-id="10775-132">Vérifiez que les champs sont définis par les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="10775-132">Make sure that the fields are set to the following values:</span></span>

- <span data-ttu-id="10775-133">Type d’enregistrement : `MX`</span><span class="sxs-lookup"><span data-stu-id="10775-133">Record Type: `MX`</span></span>
- <span data-ttu-id="10775-134">Priorité : sélectionnez la valeur la plus élevée disponible, généralement `0`.</span><span class="sxs-lookup"><span data-stu-id="10775-134">Priority: Set to the highest value available, typically `0`.</span></span>
- <span data-ttu-id="10775-135">Nom de l’hôte : `@`</span><span class="sxs-lookup"><span data-stu-id="10775-135">Host Name: `@`</span></span>
- <span data-ttu-id="10775-136">Adresse de pointage : copiez la valeur à partir du centre d’administration et collez-la ici.</span><span class="sxs-lookup"><span data-stu-id="10775-136">Points to address: Copy the value from the admin center and paste it here.</span></span>
- <span data-ttu-id="10775-137">TTL : `3600‎` (ou votre fournisseur par défaut)</span><span class="sxs-lookup"><span data-stu-id="10775-137">TTL: `3600‎` (or your provider default)</span></span>

<span data-ttu-id="10775-138">Lorsque Microsoft trouve l’enregistrement MX approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="10775-138">When Microsoft finds the correct MX record, your domain is verified.</span></span>

## <a name="step-2-add-dns-records-to-connect-microsoft-services"></a><span data-ttu-id="10775-139">Étape 2 : ajouter des enregistrements DNS pour connecter les services Microsoft</span><span class="sxs-lookup"><span data-stu-id="10775-139">Step 2: Add DNS records to connect Microsoft services</span></span>

<span data-ttu-id="10775-140">Dans un nouvel onglet ou une nouvelle fenêtre de navigateur, connectez-vous à votre fournisseur d’hébergement DNS, puis recherchez l’emplacement où vous gérez vos paramètres DNS (par exemple, Paramètres de fichier de zone, Gérer les domaines, Gestionnaire de domaine, Gestionnaire DNS).</span><span class="sxs-lookup"><span data-stu-id="10775-140">In a new browser tab or window, sign in to your DNS hosting provider, and find where you manage your DNS settings (e.g., Zone File Settings, Manage Domains, Domain Manager, DNS Manager).</span></span>

<span data-ttu-id="10775-141">Vous pourrez ajouter plusieurs types d’enregistrements DNS selon les services que vous voulez activer.</span><span class="sxs-lookup"><span data-stu-id="10775-141">You'll be adding several different types of DNS records depending on the services you want to enable.</span></span> 

### <a name="add-an-mx-record-for-email-outlook-exchange-online"></a><span data-ttu-id="10775-142">Ajouter un enregistrement MX pour la messagerie électronique (Outlook, Exchange Online)</span><span class="sxs-lookup"><span data-stu-id="10775-142">Add an MX record for email (Outlook, Exchange Online)</span></span>
<span data-ttu-id="10775-143">**Avant de commencer :** si les utilisateurs disposent déjà d’une adresse de messagerie avec votre domaine (par exemple, utilisateur@votredomaine.com), créez leur compte dans le centre d’administration avant de configurer vos enregistrements MX.</span><span class="sxs-lookup"><span data-stu-id="10775-143">**Before you begin:** If users already have email with your domain (such as user@yourdomain.com), create their accounts in the admin center before you set up your MX records.</span></span> <span data-ttu-id="10775-144">Ainsi, ils continueront à recevoir du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="10775-144">That way, they’ll continue to receive email.</span></span> <span data-ttu-id="10775-145">Lorsque vous mettez à jour l’enregistrement MX de votre domaine, tout nouveau message électronique adressé à une personne utilisant votre domaine mène désormais vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="10775-145">When you update your domain's MX record, all new email for anyone who uses your domain will now come to Microsoft 365.</span></span> <span data-ttu-id="10775-146">Un courrier électronique que vous avez déjà reste chez votre hôte de courrier actuel, sauf si vous décidez de [migrer les courriers électroniques et contacts vers Microsoft 365.](../setup/migrate-email-and-contacts-admin.md)</span><span class="sxs-lookup"><span data-stu-id="10775-146">Any email you already have will stay at your current email host, unless you decide to [migrate email and contacts to Microsoft 365.](../setup/migrate-email-and-contacts-admin.md)</span></span>

<span data-ttu-id="10775-147">Vous obtiendrez les informations relatives à l’enregistrement MX à partir de l’Assistant Configuration du domaine du centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="10775-147">You'll get the information for the MX record from the admin center domain setup wizard.</span></span>

<span data-ttu-id="10775-148">Sur le site Web de votre fournisseur d’hébergement, créez un nouvel enregistrement MX.</span><span class="sxs-lookup"><span data-stu-id="10775-148">On your hosting provider's website, add a new MX record.</span></span>
<span data-ttu-id="10775-149">Vérifiez que les champs sont définis par les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="10775-149">Make sure that the fields are set to the following values:</span></span>

- <span data-ttu-id="10775-150">Type d’enregistrement : `MX`</span><span class="sxs-lookup"><span data-stu-id="10775-150">Record Type: `MX`</span></span>
- <span data-ttu-id="10775-151">Priorité : sélectionnez la valeur la plus élevée disponible, généralement `0`.</span><span class="sxs-lookup"><span data-stu-id="10775-151">Priority: Set to the highest value available, typically `0`.</span></span>
- <span data-ttu-id="10775-152">Nom de l’hôte : `@`</span><span class="sxs-lookup"><span data-stu-id="10775-152">Host Name: `@`</span></span>
- <span data-ttu-id="10775-153">Adresse de pointage : copiez la valeur à partir du centre d’administration et collez-la ici.</span><span class="sxs-lookup"><span data-stu-id="10775-153">Points to address: Copy the value from the admin center and paste it here.</span></span>
- <span data-ttu-id="10775-154">TTL : `3600‎` (ou votre fournisseur par défaut)</span><span class="sxs-lookup"><span data-stu-id="10775-154">TTL: `3600‎` (or your provider default)</span></span>

<span data-ttu-id="10775-155">Sauvegardez l’enregistrement et supprimez tous les autres enregistrements MX.</span><span class="sxs-lookup"><span data-stu-id="10775-155">Save the record, and then remove any other MX records.</span></span>

### <a name="add-cname-records-to-connect-other-services-teams-exchange-online-aad-mdm"></a><span data-ttu-id="10775-156">Ajouter des enregistrements CNAME pour connecter d’autres services (Teams, Exchange Online, AAD, MDM)</span><span class="sxs-lookup"><span data-stu-id="10775-156">Add CNAME records to connect other services (Teams, Exchange Online, AAD, MDM)</span></span>
<span data-ttu-id="10775-157">Vous obtiendrez les informations relatives aux enregistrements CNAME à partir de l’Assistant Configuration du domaine du centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="10775-157">You'll get the information for the CNAME records from the admin center domain setup wizard.</span></span>

<span data-ttu-id="10775-158">Sur le site Web de votre fournisseur d’hébergement, ajoutez les enregistrements CNAME pour chaque service auquel vous voulez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="10775-158">On your hosting provider's website, add CNAME records for each service that you want to connect.</span></span>
<span data-ttu-id="10775-159">Dans le nouvel enregistrement, vérifiez que chacun des champs sont définis par les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="10775-159">Make sure that the fields are set to the following values for each:</span></span>

- <span data-ttu-id="10775-160">Type d’enregistrement : `CNAME (Alias)`</span><span class="sxs-lookup"><span data-stu-id="10775-160">Record Type: `CNAME (Alias)`</span></span>
- <span data-ttu-id="10775-161">Hôte : collez les valeurs que vous copiez à partir du centre d’administration ici.</span><span class="sxs-lookup"><span data-stu-id="10775-161">Host: Paste the values you copy from the admin center here.</span></span>
- <span data-ttu-id="10775-162">Adresse de pointage : copiez la valeur à partir du centre d’administration et collez-la ici.</span><span class="sxs-lookup"><span data-stu-id="10775-162">Points to address: Copy the value from the admin center and paste it here.</span></span>
- <span data-ttu-id="10775-163">TTL : `3600‎` (ou votre fournisseur par défaut)</span><span class="sxs-lookup"><span data-stu-id="10775-163">TTL: `3600‎` (or your provider default)</span></span>


### <a name="add-or-edit-an-spf-txt-record-to-help-prevent-email-spam-outlook-exchange-online"></a><span data-ttu-id="10775-164">Ajouter ou modifier un enregistrement TXT SPF afin d’éviter les courriers indésirables (Outlook, Exchange Online)</span><span class="sxs-lookup"><span data-stu-id="10775-164">Add or edit an SPF TXT record to help prevent email spam (Outlook, Exchange Online)</span></span>
<span data-ttu-id="10775-165">**Avant de commencer :** Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="10775-165">**Before you begin:** If you already have an SPF record for your domain, don't create a new one for Microsoft 365.</span></span> <span data-ttu-id="10775-166">Ajoutez plutôt les valeurs Microsoft 365 requises à l’enregistrement actuel sur le site Web de votre fournisseur d’hébergement de manière à n’avoir qu’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="10775-166">Instead, add the required Microsoft 365 values to the current record on your hosting providers website so that you have a *single* SPF record that includes both sets of values.</span></span>

<span data-ttu-id="10775-167">Sur le site web de votre fournisseur d’hébergement, modifiez l'enregistrement SPF existant ou créez un enregistrement SPF.</span><span class="sxs-lookup"><span data-stu-id="10775-167">On your hosting provider's website, edit the existing SPF record or create an SPF record.</span></span>
<span data-ttu-id="10775-168">Vérifiez que les champs sont définis par les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="10775-168">Make sure that the fields are set to the following values:</span></span>

- <span data-ttu-id="10775-169">Type d’enregistrement : `TXT (Text)`</span><span class="sxs-lookup"><span data-stu-id="10775-169">Record Type: `TXT (Text)`</span></span>
- <span data-ttu-id="10775-170">Hôte : `@`</span><span class="sxs-lookup"><span data-stu-id="10775-170">Host: `@`</span></span>
- <span data-ttu-id="10775-171">Valeur TXT :`v=spf1 include:spf.protection.outlook.com -all`</span><span class="sxs-lookup"><span data-stu-id="10775-171">TXT Value: `v=spf1 include:spf.protection.outlook.com -all`</span></span>
- <span data-ttu-id="10775-172">TTL : `3600‎` (ou votre fournisseur par défaut)</span><span class="sxs-lookup"><span data-stu-id="10775-172">TTL: `3600‎` (or your provider default)</span></span>

<span data-ttu-id="10775-173">Enregistrez l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="10775-173">Save the record.</span></span>

<span data-ttu-id="10775-174">Validez votre enregistrement SPF en utilisant l'un des [Outils de validation SPF](https://docs.microsoft.com/office365/admin/setup/domains-faq#how-can-i-validate-spf-records-for-my-domain) suivants</span><span class="sxs-lookup"><span data-stu-id="10775-174">Validate your SPF record by using one of these [SPF validation tools](https://docs.microsoft.com/office365/admin/setup/domains-faq#how-can-i-validate-spf-records-for-my-domain)</span></span>

<span data-ttu-id="10775-175">SPF est conçu pour lutter contre l’usurpation d’adresse, mais il existe des techniques d’usurpation d’adresse contre lesquelles SPF ne peut rien faire.</span><span class="sxs-lookup"><span data-stu-id="10775-175">SPF is designed to help prevent spoofing, but there are spoofing techniques that SPF cannot protect against.</span></span> <span data-ttu-id="10775-176">Pour vous protéger contre ces techniques, une fois que vous avez configuré votre SPF, vous devez également configurer DKIM et DMARC pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="10775-176">To protect against these, once you've set up SPF, you should also set up DKIM and DMARC for Microsoft 365.</span></span> 

<span data-ttu-id="10775-177">Pour commencer, consultez la rubrique [Utilisation du DKIM pour valider les e-mails sortants envoyés à partir de votre domaine dans Microsoft 365](https://technet.microsoft.com/library/mt695945%28v=exchg.150%29.aspx) et [Utilisation du DMARC pour valider les e-mails dans Microsoft 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="10775-177">To get started, see [Use DKIM to validate outbound email sent from your domain in Microsoft 365](https://technet.microsoft.com/library/mt695945%28v=exchg.150%29.aspx) and [Use DMARC to validate email in Microsoft 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).</span></span>

### <a name="add-srv-records-for-communications-services-teams-skype-for-business"></a><span data-ttu-id="10775-178">Ajouter des enregistrements SRV pour les services de communications (Teams, Skype Entreprise)</span><span class="sxs-lookup"><span data-stu-id="10775-178">Add SRV records for communications services (Teams, Skype for Business)</span></span>

<span data-ttu-id="10775-179">Sur le site Web de votre fournisseur d’hébergement, ajoutez les enregistrements SRV pour chaque service auquel vous voulez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="10775-179">On your hosting provider's website, add SRV records for each service you want to connect.</span></span>
<span data-ttu-id="10775-180">Dans le nouvel enregistrement, vérifiez que chacun des champs sont définis par les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="10775-180">Make sure that the fields are set to the following values for each:</span></span>

- <span data-ttu-id="10775-181">Type d’enregistrement : `SRV (Service)`</span><span class="sxs-lookup"><span data-stu-id="10775-181">Record Type: `SRV (Service)`</span></span>
- <span data-ttu-id="10775-182">Nom : `@`</span><span class="sxs-lookup"><span data-stu-id="10775-182">Name: `@`</span></span>
- <span data-ttu-id="10775-183">Cible : copiez la valeur à partir du centre d’administration et collez-la ici.</span><span class="sxs-lookup"><span data-stu-id="10775-183">Target: Copy the value from the admin center and paste it here.</span></span>
- <span data-ttu-id="10775-184">Protocole : copiez la valeur à partir du centre d’administration et collez-la ici.</span><span class="sxs-lookup"><span data-stu-id="10775-184">Protocol: Copy the value from the admin center and paste it here.</span></span>
- <span data-ttu-id="10775-185">Service : copiez la valeur à partir du centre d’administration et collez-la ici.</span><span class="sxs-lookup"><span data-stu-id="10775-185">Service: Copy the value from the admin center and paste it here.</span></span>
- <span data-ttu-id="10775-186">Priorité : `100`</span><span class="sxs-lookup"><span data-stu-id="10775-186">Priority: `100`</span></span>
- <span data-ttu-id="10775-187">Poids : `1`</span><span class="sxs-lookup"><span data-stu-id="10775-187">Weight: `1`</span></span>
- <span data-ttu-id="10775-188">Port : copiez la valeur à partir du centre d’administration et collez-la ici.</span><span class="sxs-lookup"><span data-stu-id="10775-188">Port: Copy the value from the admin center and paste it here.</span></span>
- <span data-ttu-id="10775-189">TTL : `3600‎` (ou votre fournisseur par défaut)</span><span class="sxs-lookup"><span data-stu-id="10775-189">TTL: `3600‎` (or your provider default)</span></span>

<span data-ttu-id="10775-190">Enregistrez l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="10775-190">Save the record.</span></span>

#### <a name="srv-record-field-restrictions-and-workarounds"></a><span data-ttu-id="10775-191">Restrictions relatives aux champs d’enregistrement SRV et solutions de contournement</span><span class="sxs-lookup"><span data-stu-id="10775-191">SRV record field restrictions and workarounds</span></span>
<span data-ttu-id="10775-192">Certains fournisseurs d’hébergement imposent des restrictions sur les valeurs de champs dans les enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="10775-192">Some hosting providers impose restrictions on field values within SRV records.</span></span> <span data-ttu-id="10775-193">Voici quelques solutions de contournement courantes pour ces restrictions.</span><span class="sxs-lookup"><span data-stu-id="10775-193">Here are some common workarounds for these restrictions.</span></span>

##### <a name="name"></a><span data-ttu-id="10775-194">Nom</span><span class="sxs-lookup"><span data-stu-id="10775-194">Name</span></span>
<span data-ttu-id="10775-195">Si votre fournisseur d’hébergement n’autorise pas la définition de ce champ sur **@**, laissez ce champ vide.</span><span class="sxs-lookup"><span data-stu-id="10775-195">If your hosting provider doesn't allow setting this field to **@**, leave it blank.</span></span> <span data-ttu-id="10775-196">Utilisez cette approche *uniquement* lorsque votre fournisseur d’hébergement utilise des champs distincts pour les valeurs Service et Protocole.</span><span class="sxs-lookup"><span data-stu-id="10775-196">Use this approach *only* when your hosting provider has separate fields for the Service and Protocol values.</span></span> <span data-ttu-id="10775-197">Dans le cas contraire, consultez les notes sur les valeurs Service et Protocole ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="10775-197">Otherwise, see the Service and Protocol notes below.</span></span>

##### <a name="service-and-protocol"></a><span data-ttu-id="10775-198">Service et Protocole</span><span class="sxs-lookup"><span data-stu-id="10775-198">Service and Protocol</span></span>
<span data-ttu-id="10775-199">Si votre fournisseur d’hébergement ne fournit pas ces champs pour les enregistrements SRV, vous devez spécifier les valeurs de **Service** et **Protocole**dans le champ **Nom** de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="10775-199">If your hosting provider doesn't provide these fields for SRV records, you must specify the **Service** and **Protocol** values in the record's **Name** field.</span></span> <span data-ttu-id="10775-200">Remarque : suivant votre fournisseur d’hébergement, le champ **Nom** peut avoir une autre appellation, comme **Hôte**, **Nom de l’hôte** ou **Sous-domaine**. Pour ajouter ces valeurs, vous devez créer une seule chaîne, en séparant les valeurs par un point.</span><span class="sxs-lookup"><span data-stu-id="10775-200">(Note: Depending on your hosting provider, the **Name** field might be called something else, like: **Host**, **Hostname**, or **Subdomain**.) To add these values, you create a single string, separating the values with a dot.</span></span> 

<span data-ttu-id="10775-201">Exemple : `_sip._tls`</span><span class="sxs-lookup"><span data-stu-id="10775-201">Example: `_sip._tls`</span></span>

##### <a name="priority-weight-and-port-br"></a><span data-ttu-id="10775-202">Priorité, Poids, et Port</span><span class="sxs-lookup"><span data-stu-id="10775-202">Priority, Weight, and Port</span></span> <br>
<span data-ttu-id="10775-203">Si votre fournisseur d’hébergement ne fournit pas ces champs pour les enregistrements SRV, vous devez spécifier ces valeurs dans le champs **Cible** de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="10775-203">If your hosting provider doesn't provide these fields for SRV records, you must specify them in the record's **Target** field.</span></span> <span data-ttu-id="10775-204">Remarque : selon votre fournisseur d’hébergement, le champ **Cible** peut être appelé différemment, comme **Contenu**, **Adresse IP**ou **Hôte cible**.</span><span class="sxs-lookup"><span data-stu-id="10775-204">(Note: Depending on your hosting provider, the **Target** field might be called something else, like: **Content**, **IP Address**, or **Target Host**.)</span></span> 

<span data-ttu-id="10775-205">Pour ajouter ces valeurs, créez une seule chaîne, en séparant les valeurs par des espaces, *ou parfois par un point*. Si vous n’êtes pas sûr, consultez votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="10775-205">To add these values, create a single string, separating the values with spaces and *sometimes ending with a dot* (check with your provider if you are unsure).</span></span> <span data-ttu-id="10775-206">Les valeurs doivent être incluses dans l’ordre suivant : Priority (Priorité), Weight (Poids), Port (Port), Target (Cible).</span><span class="sxs-lookup"><span data-stu-id="10775-206">The values must be included in this order: Priority, Weight, Port, Target.</span></span> 

- <span data-ttu-id="10775-207">Exemple 1 : `100 1 443 sipdir.online.lync.com.`</span><span class="sxs-lookup"><span data-stu-id="10775-207">Example 1: `100 1 443 sipdir.online.lync.com.`</span></span>
- <span data-ttu-id="10775-208">Exemple 2 : `100 1 443 sipdir.online.lync.com`</span><span class="sxs-lookup"><span data-stu-id="10775-208">Example 2: `100 1 443 sipdir.online.lync.com`</span></span>

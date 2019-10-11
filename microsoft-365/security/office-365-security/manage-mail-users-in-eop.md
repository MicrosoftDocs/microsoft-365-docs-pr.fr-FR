---
title: Gestion des utilisateurs de messagerie dans EOP
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 4bfaf2ab-e633-4227-8bde-effefb41a3db
description: La définition des utilisateurs de messagerie constitue une partie importante de la gestion du service Exchange Online Protection (EOP).
ms.openlocfilehash: 85a2c3ee278af36b9743fd9ff70ea9ab21437de8
ms.sourcegitcommit: cbf117a4cd92a907115c9f10752f3c557361e586
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/10/2019
ms.locfileid: "37441241"
---
# <a name="manage-mail-users-in-eop"></a><span data-ttu-id="e2048-103">Gestion des utilisateurs de messagerie dans EOP</span><span class="sxs-lookup"><span data-stu-id="e2048-103">Manage mail users in EOP</span></span>

<span data-ttu-id="e2048-p101">La définition des utilisateurs de messagerie constitue une partie importante de la gestion du service Exchange Online Protection (EOP). Vous pouvez gérer les utilisateurs de différentes manières dans EOP.</span><span class="sxs-lookup"><span data-stu-id="e2048-p101">Defining mail users is an important part of managing the Exchange Online Protection (EOP) service. There are several ways that you can manage users in EOP:</span></span>

- <span data-ttu-id="e2048-p102">**Utilisation de la synchronisation d'annuaires pour gérer les utilisateurs de messagerie** : si votre entreprise dispose de comptes d'utilisateur dans un environnement Active Directory local, vous pouvez synchroniser ces comptes sur Azure Active Directory (AD), où des copies des comptes sont stockées dans le nuage. Lorsque vous synchronisez vos comptes d'utilisateur sur Azure Active Directory, vous pouvez consulter ces utilisateurs dans le volet **Destinataires** du Centre d'administration Exchange (CAE). L'utilisation de la synchronisation d'annuaires est recommandée.</span><span class="sxs-lookup"><span data-stu-id="e2048-p102">**Use directory synchronization to manage mail users**: If your company has existing user accounts in an on-premises Active Directory environment, you can synchronize those accounts to Azure Active Directory (AD), where a copy of the accounts is stored in the cloud. When you synchronize your existing user accounts to Azure Active Directory, you can view those users in the **Recipients** pane of the Exchange admin center (EAC). Using directory synchronization is recommended.</span></span>

- <span data-ttu-id="e2048-p103">**Utilisation du CAE pour gérer les utilisateurs de messagerie** : ajoutez et gérez les utilisateurs de messagerie directement dans le CAE. Il s'agit du moyen le plus facile pour ajouter des utilisateurs de messagerie et cette méthode est également utile pour ajouter un utilisateur à la fois.</span><span class="sxs-lookup"><span data-stu-id="e2048-p103">**Use the EAC to manage mail users**: Add and manage mail users directly in the EAC. This is the easiest way to add mail users and is useful for adding one user at a time.</span></span>

- <span data-ttu-id="e2048-111">**Utiliser PowerShell pour gérer les utilisateurs de messagerie**: ajoutez et gérez les utilisateurs de messagerie dans Exchange Online Protection PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e2048-111">**Use PowerShell to manage mail users**: Add and manage mail users by in Exchange Online Protection PowerShell.</span></span> <span data-ttu-id="e2048-112">Cette méthode est utile pour ajouter plusieurs enregistrements et pour la création de scripts.</span><span class="sxs-lookup"><span data-stu-id="e2048-112">This method is useful for adding multiple records and creating scripts.</span></span>

> [!NOTE]
> <span data-ttu-id="e2048-113">Vous pouvez ajouter des utilisateurs dans le centre d’administration 365 de Microsoft, mais ces utilisateurs ne peuvent pas être utilisés comme destinataires de courrier.</span><span class="sxs-lookup"><span data-stu-id="e2048-113">You can add users in the Microsoft 365 admin center, however these users can't be used as mail recipients.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="e2048-114">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="e2048-114">Before you begin</span></span>

- <span data-ttu-id="e2048-115">Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="e2048-115">To open the Exchange admin center, see [Exchange admin center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="e2048-p105">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Utilisateurs, contacts et groupes de rôles » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="e2048-p105">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in [Feature permissions in EOP](feature-permissions-in-eop.md).</span></span>

- <span data-ttu-id="e2048-118">N’oubliez pas que lors de la création d’utilisateurs de messagerie à l’aide des cmdlets PowerShell d’Exchange Online Protection, vous pouvez rencontrer des limitations.</span><span class="sxs-lookup"><span data-stu-id="e2048-118">Be aware that when creating mail users by using Exchange Online Protection PowerShell cmdlets, you may encounter throttling.</span></span>

- <span data-ttu-id="e2048-119">Les commandes PowerShell de cette rubrique utilisent une méthode de traitement par lots qui entraîne un délai de propagation de quelques minutes avant que les résultats des commandes soient visibles.</span><span class="sxs-lookup"><span data-stu-id="e2048-119">The PowerShell commands in this topic use a batch processing method that results in a propagation delay of a few minutes before the results of the commands are visible.</span></span>

- <span data-ttu-id="e2048-120">Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online Protection, consultez la rubrique [Connexion à Exchange Online PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span><span class="sxs-lookup"><span data-stu-id="e2048-120">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span></span>

- <span data-ttu-id="e2048-121">Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span><span class="sxs-lookup"><span data-stu-id="e2048-121">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="e2048-122">Vous rencontrez des difficultés ?</span><span class="sxs-lookup"><span data-stu-id="e2048-122">Having problems?</span></span> <span data-ttu-id="e2048-123">Demandez de l’aide dans le forum [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) .</span><span class="sxs-lookup"><span data-stu-id="e2048-123">Ask for help in the [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) forum.</span></span>

## <a name="use-directory-synchronization-to-manage-mail-users"></a><span data-ttu-id="e2048-124">Utilisation de la synchronisation d’annuaires pour gérer les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="e2048-124">Use directory synchronization to manage mail users</span></span>

<span data-ttu-id="e2048-125">Cette section fournit des informations sur la gestion des utilisateurs de messagerie électronique à l’aide de la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="e2048-125">This section provides information about managing email users by using directory synchronization.</span></span>

<span data-ttu-id="e2048-126">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="e2048-126">**Notes**:</span></span>

- <span data-ttu-id="e2048-127">Si vous utilisez la synchronisation d’annuaires pour gérer vos destinataires, vous pouvez toujours ajouter et gérer des utilisateurs dans le centre d’administration 365 de Microsoft, mais ils ne seront pas synchronisés avec votre annuaire Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="e2048-127">If you use directory synchronization to manage your recipients, you can still add and manage users in the Microsoft 365 admin center, but they will not be synchronized with your on-premises Active Directory.</span></span> <span data-ttu-id="e2048-128">Cela est dû au fait que la synchronisation d’annuaires ne synchronise que les destinataires **de** votre annuaire Active Directory local **vers** le Cloud.</span><span class="sxs-lookup"><span data-stu-id="e2048-128">This is because directory synchronization only syncs recipients **from** your on-premises Active Directory **to** the cloud.</span></span>

- <span data-ttu-id="e2048-129">La synchronisation d’annuaires est recommandée pour une utilisation avec les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2048-129">Directory synchronization is recommended for use with the following features:</span></span>

  - <span data-ttu-id="e2048-130">**Listes des expéditeurs autorisés et des expéditeurs bloqués Outlook**: lorsqu’ils sont synchronisés avec le service, ces listes prévalent sur le filtrage du courrier indésirable dans le service.</span><span class="sxs-lookup"><span data-stu-id="e2048-130">**Outlook safe sender and blocked sender lists**: When synchronized to the service, these lists will take precedence over spam filtering in the service.</span></span> <span data-ttu-id="e2048-131">Cela permet aux utilisateurs de gérer leurs propres listes d’expéditeurs autorisés et bloqués en fonction de l’utilisateur et du domaine.</span><span class="sxs-lookup"><span data-stu-id="e2048-131">This lets users manage their own safe sender and blocked sender lists on a per-user or per-domain basis.</span></span>

  - <span data-ttu-id="e2048-132">**Blocage du périmètre basé sur l’annuaire (DBEB)**: pour plus d’informations sur DBEB, voir [use Directory based Edge Blocking to Reject messages sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span><span class="sxs-lookup"><span data-stu-id="e2048-132">**Directory Based Edge Blocking (DBEB)**: For more information about DBEB, see [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span></span>

  - <span data-ttu-id="e2048-133">**Mise en quarantaine du courrier indésirable**de l’utilisateur final : pour accéder à la mise en quarantaine du courrier indésirable de l’utilisateur final, les utilisateurs finaux doivent avoir un ID d’utilisateur et un mot de passe Office 365 valide.</span><span class="sxs-lookup"><span data-stu-id="e2048-133">**End user spam quarantine**: In order to access the end user spam quarantine, end users must have a valid Office 365 user ID and password.</span></span> <span data-ttu-id="e2048-134">Les clients qui utilisent EOP pour la protection des boîtes aux lettres locales doivent être des utilisateurs de messagerie électronique valides.</span><span class="sxs-lookup"><span data-stu-id="e2048-134">EOP customers protecting on-premises mailboxes must be valid email users.</span></span>
 
  - <span data-ttu-id="e2048-135">**Règles de flux de messagerie**: lorsque vous utilisez la synchronisation d’annuaires, vos utilisateurs et groupes Active Directory existants sont automatiquement téléchargés dans le Cloud, puis vous pouvez créer des règles de flux de messagerie (également appelées règles de transport) qui ciblent des utilisateurs spécifiques et/ou groupes sans avoir à les ajouter manuellement via le centre d’administration Exchange ou Exchange Online Protection PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e2048-135">**Mail flow rules**: When you use directory synchronization, your existing Active Directory users and groups are automatically uploaded to the cloud, and you can then create mail flow rules (also known as transport rules) that target specific users and/or groups without having to manually add them via the the EAC or Exchange Online Protection PowerShell.</span></span> <span data-ttu-id="e2048-136">Notez que les [groupes de distribution dynamique](https://go.microsoft.com/fwlink/?LinkId=507569) ne peuvent pas être synchronisés via la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="e2048-136">Note that [dynamic distribution groups](https://go.microsoft.com/fwlink/?LinkId=507569) can't be synchronized via directory synchronization.</span></span>

<span data-ttu-id="e2048-137">Obtenez les autorisations nécessaires et préparez la synchronisation d'annuaires, comme décrit dans la rubrique [Préparer la synchronisation d'annuaires](https://go.microsoft.com/fwlink/p/?LinkId=308908).</span><span class="sxs-lookup"><span data-stu-id="e2048-137">Get the necessary permissions and prepare for directory synchronization, as described in [Prepare for directory synchronization](https://go.microsoft.com/fwlink/p/?LinkId=308908).</span></span>

### <a name="to-synchronize-user-directories-with-azure-active-directory-connect-aad-connect"></a><span data-ttu-id="e2048-138">Pour synchroniser les annuaires d’utilisateurs avec Azure Active Directory Connect (AAD Connect)</span><span class="sxs-lookup"><span data-stu-id="e2048-138">To synchronize user directories with Azure Active Directory Connect (AAD Connect)</span></span>

<span data-ttu-id="e2048-139">Pour synchroniser les utilisateurs avec Azure Active Directory (AAD), vous devez d’abord **activer la synchronisation d’annuaires**, comme décrit dans la rubrique activation de la [synchronisation d’annuaires](https://go.microsoft.com/fwlink/p/?LinkId=308909).</span><span class="sxs-lookup"><span data-stu-id="e2048-139">To synchronize users to Azure Active Directory (AAD) you first have to **activate directory synchronization**, as described in [Activate directory synchronization](https://go.microsoft.com/fwlink/p/?LinkId=308909).</span></span>

<span data-ttu-id="e2048-140">Ensuite, l’installation et la configuration d’un ordinateur local pour exécuter AAD Connect (si vous n’avez pas encore besoin de vérifier à l’avance).</span><span class="sxs-lookup"><span data-stu-id="e2048-140">Next is the installation and configuration of an on-premises computer to run AAD Connect (if you don't already have one -- something worth checking ahead of time).</span></span> <span data-ttu-id="e2048-141">La rubrique [configuration de AAD Connect, la rubrique relative à la méthode rapide](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express) vous indique comment configurer et synchroniser vos comptes de l’organisation locale vers Azure ad avec AAD Connect.</span><span class="sxs-lookup"><span data-stu-id="e2048-141">The [Setting up AAD Connect, the express way](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express) topic tells you how to setup and synchronize your accounts from on-premises to Azure AD with AAD Connect.</span></span>

<span data-ttu-id="e2048-142">Mais avant cela, [vous devez vous assurer que vous répondez aux conditions préalables](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites)et [Choisissez votre type d’installation](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-select-installation).</span><span class="sxs-lookup"><span data-stu-id="e2048-142">But before you do that work, make certain [you meet prerequisites](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites), and [choose your installation type](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-select-installation).</span></span> <span data-ttu-id="e2048-143">Le lien précédent est un petit article pour les installations rapides.</span><span class="sxs-lookup"><span data-stu-id="e2048-143">The earlier link is to a short article for express installs.</span></span> <span data-ttu-id="e2048-144">Vous pouvez également trouver des articles sur les [installations personnalisées](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-custom)ou [l’authentification directe](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-pta-quick-start) si elles sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="e2048-144">You can also find articles on [custom installations](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-custom), or [pass-through authentication](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-pta-quick-start) if they're needed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2048-p113">Après exécution de l'Assistant Configuration de l'outil de synchronisation Azure Active Directory, le compte **MSOL_AD_SYNC** est créé dans votre forêt Active Directory. Ce compte permet de lire et de synchroniser vos informations Active Directory sur site. Pour que la synchronisation d'annuaires fonctionne correctement, assurez-vous que le port TCP 443 est ouvert sur votre serveur de synchronisation d'annuaires sur site.</span><span class="sxs-lookup"><span data-stu-id="e2048-p113">When you finish the Azure Active Directory Sync Tool Configuration Wizard, the **MSOL_AD_SYNC** account is created in your Active Directory forest. This account is used to read and synchronize your on-premises Active Directory information. In order for directory synchronization to work correctly, make sure that TCP 443 on your local directory synchronization server is open.</span></span>

<span data-ttu-id="e2048-148">Après avoir configuré votre synchronisation, assurez-vous de vérifier que EOP effectue une synchronisation correcte.</span><span class="sxs-lookup"><span data-stu-id="e2048-148">After configuring your sync, be sure to verify that EOP is synchronizing correctly.</span></span> <span data-ttu-id="e2048-149">Dans le CAE, accédez à **Destinataires** \> **Contacts** et vérifiez que la liste des utilisateurs a été correctement synchronisée à partir de votre environnement local.</span><span class="sxs-lookup"><span data-stu-id="e2048-149">In the EAC, go to **Recipients** \> **Contacts** and view that the list of users was correctly synchronized from your on-premises environment.</span></span>

## <a name="use-the-eac-to-manage-mail-users"></a><span data-ttu-id="e2048-150">Utilisation du CAE pour gérer les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="e2048-150">Use the EAC to manage mail users</span></span>

<span data-ttu-id="e2048-151">Cette section fournit des informations sur l’ajout et la gestion des utilisateurs de messagerie directement dans le CAE.</span><span class="sxs-lookup"><span data-stu-id="e2048-151">This section provides information about adding and managing email users directly in the EAC.</span></span>

### <a name="use-the-eac-to-add-a-mail-user"></a><span data-ttu-id="e2048-152">Utiliser le centre d’administration Exchange pour ajouter un utilisateur de messagerie</span><span class="sxs-lookup"><span data-stu-id="e2048-152">Use the EAC to add a mail user</span></span>

1. <span data-ttu-id="e2048-153">Créez un utilisateur de messagerie électronique en accédant à **Destinataires** \> **Contacts** dans le CAE, puis cliquez sur **Nouveau +**.</span><span class="sxs-lookup"><span data-stu-id="e2048-153">Create an email user by going to go to **Recipients** \> **Contacts** in the EAC, and then clicking **New +**.</span></span>

2. <span data-ttu-id="e2048-154">Sur la page **Nouvel utilisateur de messagerie**, saisissez les informations de l'utilisateur, notamment les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e2048-154">On the **New mail user** page, enter the user's information, including the following:</span></span>

   ****

   |<span data-ttu-id="e2048-155">**Propriété d'utilisateur de messagerie**</span><span class="sxs-lookup"><span data-stu-id="e2048-155">**Mail user property**</span></span>|<span data-ttu-id="e2048-156">**Description**</span><span class="sxs-lookup"><span data-stu-id="e2048-156">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="e2048-157">**Prénom**, **Initiales** et **Nom de famille**</span><span class="sxs-lookup"><span data-stu-id="e2048-157">**First name**, **Initials**, and **Last name**</span></span>|<span data-ttu-id="e2048-158">Dans les zones appropriées, saisissez le nom de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e2048-158">Type the user's full name in the appropriate boxes.</span></span>|
   |<span data-ttu-id="e2048-159">**Nom complet**</span><span class="sxs-lookup"><span data-stu-id="e2048-159">**Display name**</span></span>|<span data-ttu-id="e2048-p115">Saisissez le nom (64 caractères maximum). Par défaut, cette zone est renseignée avec les noms que vous avez entrés dans les champs **Prénom**, **Initiales** et **Nom de famille**, le cas échéant. Le nom complet est requis.  </span><span class="sxs-lookup"><span data-stu-id="e2048-p115">Type a name, using up to 64 characters. By default, this box shows the names in the **First name**, **Initials**, and **Last name** boxes if any. The display name is required.</span></span>|
   |<span data-ttu-id="e2048-163">**Alias**</span><span class="sxs-lookup"><span data-stu-id="e2048-163">**Alias**</span></span>|<span data-ttu-id="e2048-p116">Saisissez un alias unique pour l'utilisateur (64 caractères maximum). L'alias est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e2048-p116">Type a unique alias, using up to 64 characters, for the user. The alias is required.</span></span>|
   |<span data-ttu-id="e2048-166">**Adresse de messagerie externe**</span><span class="sxs-lookup"><span data-stu-id="e2048-166">**External email address**</span></span>|<span data-ttu-id="e2048-167">Saisissez l'adresse de messagerie électronique externe de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e2048-167">Type the external email address of the user.</span></span>|
   |<span data-ttu-id="e2048-168">**ID utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e2048-168">**User id**</span></span>|<span data-ttu-id="e2048-p117">Saisissez le nom que l'utilisateur de messagerie utilisera pour se connecter au service. Le nom de connexion de l'utilisateur est constitué du nom d'utilisateur à gauche du symbole (@) et d'un suffixe à droite. Généralement, le suffixe est le nom du domaine dans lequel le compte d'utilisateur réside.</span><span class="sxs-lookup"><span data-stu-id="e2048-p117">Type the name that the mail user will use to sign in to the service. The user sign-in name consists of a user name on the left side of the at (@) symbol and a suffix on the right side. Typically, the suffix is the domain name in which the user account resides.</span></span>|
   |<span data-ttu-id="e2048-172">**Nouveau mot de passe**</span><span class="sxs-lookup"><span data-stu-id="e2048-172">**New password**</span></span>|<span data-ttu-id="e2048-p118">Saisissez le mot de passe que l'utilisateur de messagerie utilisera pour se connecter au service. Assurez-vous que le mot de passe que vous saisissez est conforme aux exigences de longueur, de complexité et d'historique de mot de passe du domaine dans lequel vous créez le compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e2048-p118">Type the password that the mail user will use to sign in to the service. Make sure that the password you supply complies with the password length, complexity, and history requirements of the domain in which you're creating the user account.</span></span>|
   |<span data-ttu-id="e2048-175">**Confirmer le mot de passe**</span><span class="sxs-lookup"><span data-stu-id="e2048-175">**Confirm password**</span></span>|<span data-ttu-id="e2048-176">Ressaisissez le mot de passe pour le confirmer.</span><span class="sxs-lookup"><span data-stu-id="e2048-176">Retype the password to confirm it.</span></span>|

3. <span data-ttu-id="e2048-p119">Cliquez sur **Nouveau** pour créer l'utilisateur de messagerie. Le nouvel utilisateur doit apparaître dans la liste des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e2048-p119">Click **Save** to create the new email user. The new user should appear in the list of users.</span></span>

### <a name="use-the-eac-to-edit-or-remove-a-mail-user"></a><span data-ttu-id="e2048-179">Utiliser le centre d’administration Exchange pour modifier ou supprimer un utilisateur de messagerie</span><span class="sxs-lookup"><span data-stu-id="e2048-179">Use the EAC to edit or remove a mail user</span></span>

- <span data-ttu-id="e2048-180">Dans le CAE, accédez à **Destinataires** \> **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="e2048-180">In the EAC, go to **Recipients** \> **Contacts**.</span></span> <span data-ttu-id="e2048-181">Dans la liste des utilisateurs, cliquez sur l’utilisateur que vous souhaitez afficher ou modifier, puis sélectionnez **modifier** ![l’icône](../media/ITPro-EAC-EditIcon.gif) modifier pour mettre à jour les paramètres utilisateur selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="e2048-181">In the list of users, click the user that you want to view or change, and then select **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif) to update the user settings as needed.</span></span> <span data-ttu-id="e2048-182">Vous pouvez modifier le nom, l'alias ou les coordonnées de l'utilisateur et vous pouvez enregistrer des informations détaillées sur le rôle de l'utilisateur dans l'organisation.</span><span class="sxs-lookup"><span data-stu-id="e2048-182">You can change the user's name, alias, or contact information, and you can record detailed information about the user's role in the organization.</span></span> <span data-ttu-id="e2048-183">Vous pouvez également sélectionner un utilisateur, puis cliquer sur **supprimer** ![l'](../media/ITPro-EAC-RemoveIcon.gif) icône Supprimer pour le supprimer.</span><span class="sxs-lookup"><span data-stu-id="e2048-183">You can also select a user and then choose **Remove** ![Remove icon](../media/ITPro-EAC-RemoveIcon.gif) to delete it.</span></span>

## <a name="use-exchange-online-protection-powershell-to-manage-mail-users"></a><span data-ttu-id="e2048-184">Utiliser Exchange Online Protection PowerShell pour gérer les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="e2048-184">Use Exchange Online Protection PowerShell to manage mail users</span></span>

<span data-ttu-id="e2048-185">Cette section fournit des informations sur l'ajout et la gestion des utilisateurs de messagerie à l'aide de Windows PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="e2048-185">This section provides information about adding and managing mail users by using remote Windows PowerShell.</span></span>

### <a name="use-eop-powershell-to-add-a-mail-user"></a><span data-ttu-id="e2048-186">Utiliser EOP PowerShell pour ajouter un utilisateur de messagerie</span><span class="sxs-lookup"><span data-stu-id="e2048-186">Use EOP PowerShell to add a mail user</span></span>

<span data-ttu-id="e2048-187">Cet exemple illustre la création d'un compte d'utilisateur à extension messagerie avec la cmdlet [New-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/new-eopmailuser) pour l'utilisateur Jeffrey Zeng, avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2048-187">This example uses the [New-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/new-eopmailuser) cmdlet to create a mail-enabled user account for Jeffrey Zeng in EOP with the following details:</span></span>

- <span data-ttu-id="e2048-188">Le prénom est Jeffrey et le nom est Zeng.</span><span class="sxs-lookup"><span data-stu-id="e2048-188">The first name is Jeffrey and the last name is Zeng.</span></span>

- <span data-ttu-id="e2048-189">Le nom est Jeffrey et le nom d'affichage est Jeffrey Zeng.</span><span class="sxs-lookup"><span data-stu-id="e2048-189">The name is Jeffrey and the display name is Jeffrey Zeng.</span></span>

- <span data-ttu-id="e2048-190">L'alias est jeffreyz.</span><span class="sxs-lookup"><span data-stu-id="e2048-190">The alias is jeffreyz.</span></span>

- <span data-ttu-id="e2048-191">L'adresse de messagerie externe est jzeng@tailspintoys.com.</span><span class="sxs-lookup"><span data-stu-id="e2048-191">The external email address is jzeng@tailspintoys.com.</span></span>

- <span data-ttu-id="e2048-192">Le nom de connexion à Office 365 est jeffreyz@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="e2048-192">The Office 365 sign in name is jeffreyz@contoso.onmicrosoft.com.</span></span>

- <span data-ttu-id="e2048-193">Le mot de passe est Pa$$word1.</span><span class="sxs-lookup"><span data-stu-id="e2048-193">The password is Pa$$word1.</span></span>

```PowerShell
New-EOPMailUser -LastName Zeng -FirstName Jeffrey -DisplayName "Jeffrey Zeng" -Name Jeffrey -Alias jeffreyz -MicrosoftOnlineServicesID jeffreyz@contoso.onmicrosoft.com -ExternalEmailAddress jeffreyz@tailspintoys.com -Password (ConvertTo-SecureString -String 'Pa$$word1' -AsPlainText -Force)
```

<span data-ttu-id="e2048-194">Pour vérifier qu’elle a fonctionné, exécutez la commande suivante pour afficher les informations sur le nouvel utilisateur de messagerie Jeffrey Zeng :</span><span class="sxs-lookup"><span data-stu-id="e2048-194">To verify that this worked, run the following command to display information about new mail user Jeffrey Zeng:</span></span>

```PowerShell
Get-User -Identity "Jeffrey Zeng"
```

<span data-ttu-id="e2048-195">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-User](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-user).</span><span class="sxs-lookup"><span data-stu-id="e2048-195">For detailed syntax and parameter information, see [Get-User](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-user).</span></span>

### <a name="use-eop-powershell-to-edit-the-properties-of-a-mail-user"></a><span data-ttu-id="e2048-196">Utiliser EOP PowerShell pour modifier les propriétés d’un utilisateur de messagerie</span><span class="sxs-lookup"><span data-stu-id="e2048-196">Use EOP PowerShell to edit the properties of a mail user</span></span>

<span data-ttu-id="e2048-197">Utilisez les cmdlets [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) et [Set-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/set-eopmailuser) pour afficher et modifier les propriétés des utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="e2048-197">Use the [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) and [Set-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/set-eopmailuser) cmdlets to view or change properties for mail users.</span></span>

<span data-ttu-id="e2048-198">Cet exemple illustre la configuration de l'adresse de messagerie externe pour Pilar Pinilla.</span><span class="sxs-lookup"><span data-stu-id="e2048-198">This example sets the external email address for Pilar Pinilla.</span></span>

```PowerShell
Set-EOPMailUser -Identity "Pilar Pinilla" -EmailAddresses pilarp@tailspintoys.com
```

<span data-ttu-id="e2048-199">Cet exemple illustre la définition de la propriété Company sur Contoso pour tous les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="e2048-199">This example sets the Company property for all mail users to Contoso.</span></span>

```PowerShell
$Recip = Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')}
$Recip | foreach {Set-EOPUser -Identity $_.Alias -Company Contoso}
```

<span data-ttu-id="e2048-200">Pour vérifier que cela a fonctionné, utilisez la cmdlet [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) pour vérifier les modifications.</span><span class="sxs-lookup"><span data-stu-id="e2048-200">To verify that this worked, use the [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) cmdlet to verify the changes.</span></span> <span data-ttu-id="e2048-201">(Vous pouvez afficher plusieurs propriétés pour plusieurs contacts de messagerie.)</span><span class="sxs-lookup"><span data-stu-id="e2048-201">(Note that you can view multiple properties for multiple mail contacts.)</span></span>

```PowerShell
Get-Recipient -Identity "Pilar Pinilla" | Format-List
```

<span data-ttu-id="e2048-202">Dans l'exemple précédent où la propriété Company a été définie sur Contoso pour tous les utilisateurs de messagerie, exécutez la commande suivante pour vérifier les modifications :</span><span class="sxs-lookup"><span data-stu-id="e2048-202">In the previous example where the Company property was set to Contoso for all mail users, run the following command to verify the changes:</span></span>

```PowerShell
Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')} | Format-List Name,Company
```

> [!IMPORTANT]
> <span data-ttu-id="e2048-203">Cette cmdlet utilise une méthode de traitement par lots qui se traduit par un retard de propagation de quelques minutes avant que les résultats de la cmdlet ne soient visibles.</span><span class="sxs-lookup"><span data-stu-id="e2048-203">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span>

### <a name="use-eop-powershell-to-remove-a-mail-user"></a><span data-ttu-id="e2048-204">Utiliser EOP PowerShell pour supprimer un utilisateur de messagerie</span><span class="sxs-lookup"><span data-stu-id="e2048-204">Use EOP PowerShell to remove a mail user</span></span>

<span data-ttu-id="e2048-205">Cet exemple utilise la cmdlet [Remove-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient/remove-eopmailuser) pour supprimer l'utilisateur Jeffrey Zeng :</span><span class="sxs-lookup"><span data-stu-id="e2048-205">This example uses the [Remove-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient/remove-eopmailuser) cmdlet to delete user Jeffrey Zeng:</span></span>

```PowerShell
Remove-EOPMailUser -Identity Jeffrey
```
<span data-ttu-id="e2048-206">Pour vérifier que cela a fonctionné, exécutez la cmdlet [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) pour vérifier que l’utilisateur de messagerie n’existe plus.</span><span class="sxs-lookup"><span data-stu-id="e2048-206">To verify that this worked, run the [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-recipient) cmdlet to verify that the mail user no longer exists.</span></span>

```PowerShell
Get-Recipient Jeffrey | Format-List
```

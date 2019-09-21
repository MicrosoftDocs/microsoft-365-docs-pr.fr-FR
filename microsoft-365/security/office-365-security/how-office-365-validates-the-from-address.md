---
title: Comment Office 365 valide l’adresse de pour empêcher le hameçonnage
ms.author: tracyp
author: MSFTTracyp
manager: dansimp
ms.date: 10/11/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- OWC150
- MET150
ms.assetid: eef8408b-54d3-4d7d-9cf7-ad2af10b2e0e
ms.collection:
- M365-security-compliance
description: 'Pour éviter les attaques par hameçonnage, Office 365 et Outlook.com requièrent désormais une conformité RFC pour from : Addresses.'
ms.openlocfilehash: 39c9898a31c715487f3bc934ad0986e9a7b3679d
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079043"
---
# <a name="how-office-365-validates-the-from-address-to-prevent-phishing"></a><span data-ttu-id="bdf24-103">Comment Office 365 valide l’adresse de pour empêcher le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="bdf24-103">How Office 365 validates the From address to prevent phishing</span></span>

<span data-ttu-id="bdf24-104">Les comptes de messagerie Office 365 et Outlook.com reçoivent un nombre plus élevé d’attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="bdf24-104">Office 365 and Outlook.com email accounts receive an increasingly large number of phishing attacks.</span></span> <span data-ttu-id="bdf24-105">L’une des techniques utilisées par les auteurs de phishing est d’envoyer des messages dont la valeur pour l’adresse de : n’est pas conforme à la norme [RFC 5322](https://tools.ietf.org/html/rfc5322).</span><span class="sxs-lookup"><span data-stu-id="bdf24-105">One technique phishers use is to send messages that have values for the From: address that are not compliant with [RFC 5322](https://tools.ietf.org/html/rfc5322).</span></span> <span data-ttu-id="bdf24-106">L’adresse from : est également appelée l’adresse 5322. from.</span><span class="sxs-lookup"><span data-stu-id="bdf24-106">The From: address is also called the 5322.From address.</span></span> <span data-ttu-id="bdf24-107">Pour éviter ce type de hameçonnage, Office 365 et Outlook.com requièrent que les messages reçus par le service incluent une adresse à partir de la RFC telle que décrite dans cet article.</span><span class="sxs-lookup"><span data-stu-id="bdf24-107">To help prevent this type of phishing, Office 365 and Outlook.com require messages received by the service to include an RFC-compliant From: address as described in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bdf24-108">Les informations contenues dans cet article vous obligent à comprendre le format général des adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bdf24-108">The information in this article requires you to have a basic understanding of the general format of email addresses.</span></span> <span data-ttu-id="bdf24-109">Pour plus d’informations, reportez-vous à [rfc 5322](https://tools.ietf.org/html/rfc5322) (en particulier les sections 3.2.3, 3,4 et 3.4.1), [RFC 5321](https://tools.ietf.org/html/rfc5321), ainsi que [RFC 3696](https://tools.ietf.org/html/rfc3696).</span><span class="sxs-lookup"><span data-stu-id="bdf24-109">For more information, see [RFC 5322](https://tools.ietf.org/html/rfc5322) (particularly sections 3.2.3, 3.4, and 3.4.1), [RFC 5321](https://tools.ietf.org/html/rfc5321), as well as [RFC 3696](https://tools.ietf.org/html/rfc3696).</span></span> <span data-ttu-id="bdf24-110">Cet article traite de l’application de la stratégie pour l’adresse 5322. from.</span><span class="sxs-lookup"><span data-stu-id="bdf24-110">This article is about policy enforcement for the 5322.From address.</span></span> <span data-ttu-id="bdf24-111">Cet article ne traite pas de l’adresse 5321. MailFrom.</span><span class="sxs-lookup"><span data-stu-id="bdf24-111">This article is not about the 5321.MailFrom address.</span></span> 
  
<span data-ttu-id="bdf24-112">Malheureusement, il existe toujours des serveurs de messagerie hérités sur Internet qui continuent à envoyer des messages électroniques « légitimes » dont l’adresse est manquante ou incorrecte :.</span><span class="sxs-lookup"><span data-stu-id="bdf24-112">Unfortunately, there are still some legacy email servers on the Internet that continue to send "legitimate" email messages that have a missing or malformed From: address.</span></span> <span data-ttu-id="bdf24-113">Si vous recevez régulièrement du courrier électronique d’organisations qui utilisent ces systèmes hérités, encouragez ces organisations à mettre à jour leurs serveurs de messagerie afin de se conformer aux normes de sécurité modernes.</span><span class="sxs-lookup"><span data-stu-id="bdf24-113">If you regularly receive email from organizations that use these legacy systems, encourage those organizations to update their mail servers to comply with modern security standards.</span></span>
  
<span data-ttu-id="bdf24-114">Microsoft commencera à déployer la mise en œuvre des stratégies décrites dans cet article le 9 novembre 2017.</span><span class="sxs-lookup"><span data-stu-id="bdf24-114">Microsoft will start rolling out enforcement of the policies described in this article on November 9, 2017.</span></span>
  
## <a name="how-office-365-enforces-the-use-of-a-valid-from-address-to-prevent-phishing-attacks"></a><span data-ttu-id="bdf24-115">Comment Office 365 applique l’utilisation d’une adresse valide from : pour éviter les attaques par hameçonnage</span><span class="sxs-lookup"><span data-stu-id="bdf24-115">How Office 365 enforces the use of a valid From: address to prevent phishing attacks</span></span>

<span data-ttu-id="bdf24-116">Office 365 apporte des modifications à la façon dont il applique l’utilisation de l’adresse de : dans les messages qu’il reçoit afin de mieux vous protéger contre les attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="bdf24-116">Office 365 is making changes to the way it enforces the use of the From: address in messages it receives in order to better protect you from phishing attacks.</span></span> <span data-ttu-id="bdf24-117">Contenu de cet article :</span><span class="sxs-lookup"><span data-stu-id="bdf24-117">In this article:</span></span>
  
- [<span data-ttu-id="bdf24-118">Tous les messages doivent inclure une adresse valide :</span><span class="sxs-lookup"><span data-stu-id="bdf24-118">All messages must include a valid From: address</span></span>](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [<span data-ttu-id="bdf24-119">Format de l’adresse de : Si vous n’incluez pas de nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="bdf24-119">Format of the From: address if you don't include a display name</span></span>](how-office-365-validates-the-from-address.md#FormatNoDisplayName)
    
- [<span data-ttu-id="bdf24-120">Format de l’adresse de : Si vous incluez un nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="bdf24-120">Format of the From: address if you include a display name</span></span>](how-office-365-validates-the-from-address.md#FormatDisplayName)
    
- [<span data-ttu-id="bdf24-121">Exemples supplémentaires d’adresses valides et non valides :</span><span class="sxs-lookup"><span data-stu-id="bdf24-121">Additional examples of valid and invalid From: addresses</span></span>](how-office-365-validates-the-from-address.md#Examples)
    
- [<span data-ttu-id="bdf24-122">Supprimer les réponses automatiques à votre domaine personnalisé sans rompre la stratégie de :</span><span class="sxs-lookup"><span data-stu-id="bdf24-122">Suppress auto-replies to your custom domain without breaking the From: policy</span></span>](how-office-365-validates-the-from-address.md#SuppressAutoReply)
    
- [<span data-ttu-id="bdf24-123">Remplacement d’Office 365 de : stratégie de mise en œuvre des adresses</span><span class="sxs-lookup"><span data-stu-id="bdf24-123">Overriding the Office 365 From: address enforcement policy</span></span>](how-office-365-validates-the-from-address.md#Override)
    
- [<span data-ttu-id="bdf24-124">Autres méthodes pour prévenir et protéger contre les cybercriminels dans Office 365</span><span class="sxs-lookup"><span data-stu-id="bdf24-124">Other ways to prevent and protect against cybercrimes in Office 365</span></span>](how-office-365-validates-the-from-address.md#OtherProtection)
    
<span data-ttu-id="bdf24-125">L’envoi de la part d’un autre utilisateur n’est pas affecté par cette modification, pour plus d’informations, consultez le blog de Thierry Zink «[que dois-je dire lorsque nous faisons référence à l’expéditeur d’un e-mail ?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)».</span><span class="sxs-lookup"><span data-stu-id="bdf24-125">Sending on behalf of another user is not affected by this change, for more details, read Terry Zink's blog "[What do we mean when we refer to the 'sender' of an email?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)".</span></span>
  
### <a name="all-messages-must-include-a-valid-from-address"></a><span data-ttu-id="bdf24-126">Tous les messages doivent inclure une adresse valide :</span><span class="sxs-lookup"><span data-stu-id="bdf24-126">All messages must include a valid From: address</span></span>
<span data-ttu-id="bdf24-127"><a name="MustIncludeFromAddress"> </a></span><span class="sxs-lookup"><span data-stu-id="bdf24-127"></span></span>

<span data-ttu-id="bdf24-128">Certains messages automatisés n’incluent pas une adresse de : lorsqu’ils sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="bdf24-128">Some automated messages don't include a From: address when they are sent.</span></span> <span data-ttu-id="bdf24-129">Dans le passé, lorsque Office 365 ou Outlook.com a reçu un message sans l’adresse de l’adresse :, le service a ajouté l’adresse suivante : par défaut du message afin de le faire livrer :</span><span class="sxs-lookup"><span data-stu-id="bdf24-129">In the past, when Office 365 or Outlook.com received a message without a From: address, the service added the following default From: address to the message in order to make it deliverable:</span></span>
  
```
From: <>
```

<span data-ttu-id="bdf24-130">À partir du 9 novembre 2017, Office 365 effectuera le déploiement des modifications apportées à ses centres de messages et serveurs de messagerie, ce qui appliquera une nouvelle règle lorsque les messages sans adresse de l’expéditeur ne seront plus acceptés par Office 365 ou Outlook.com.</span><span class="sxs-lookup"><span data-stu-id="bdf24-130">Starting November 9, 2017, Office 365 will be rolling out changes to its datacenters and mail servers which will enforce a new rule where messages without a From: address will no longer be accepted by Office 365 or Outlook.com.</span></span> <span data-ttu-id="bdf24-131">Au lieu de cela, tous les messages reçus par Office 365 doivent déjà contenir une adresse valide :.</span><span class="sxs-lookup"><span data-stu-id="bdf24-131">Instead, all messages received by Office 365 must already contain a valid From: address.</span></span> <span data-ttu-id="bdf24-132">Dans le cas contraire, le message est envoyé vers le dossier courrier indésirable ou éléments supprimés dans Outlook.com et Office 365.</span><span class="sxs-lookup"><span data-stu-id="bdf24-132">Otherwise, the message will be sent to either the Junk Email or Deleted Items folders in Outlook.com and Office 365.</span></span> 
  
### <a name="syntax-overview-valid-format-for-the-from-address-for-office-365"></a><span data-ttu-id="bdf24-133">Vue d’ensemble de la syntaxe : format valide pour l’adresse de : pour Office 365</span><span class="sxs-lookup"><span data-stu-id="bdf24-133">Syntax overview: Valid format for the From: address for Office 365</span></span>
<span data-ttu-id="bdf24-134"><a name="SyntaxOverviewFromAddress"> </a></span><span class="sxs-lookup"><span data-stu-id="bdf24-134"></span></span>

<span data-ttu-id="bdf24-135">Le format de la valeur de l’adresse de : est défini en détail dans plusieurs RFC.</span><span class="sxs-lookup"><span data-stu-id="bdf24-135">The format for the value of the From: address is defined in detail across several RFCs.</span></span> <span data-ttu-id="bdf24-136">Il existe de nombreuses variantes de l’adressage et ce qui peut être considéré comme valide ou non valide.</span><span class="sxs-lookup"><span data-stu-id="bdf24-136">There are many variations on addressing and what may be considered valid or invalid.</span></span> <span data-ttu-id="bdf24-137">Pour simplifier, Microsoft vous recommande d’utiliser le format et les définitions suivants :</span><span class="sxs-lookup"><span data-stu-id="bdf24-137">To keep it simple, Microsoft recommends that you use the following format and definitions:</span></span>
  
```
From: "displayname " <emailaddress >
```

<span data-ttu-id="bdf24-138">Où :</span><span class="sxs-lookup"><span data-stu-id="bdf24-138">Where:</span></span>
  
- <span data-ttu-id="bdf24-139">Module  *DisplayName* est une expression qui décrit le propriétaire de l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bdf24-139">(Optional)  *displayname*  is a phrase that describes the owner of the email address.</span></span> <span data-ttu-id="bdf24-140">Par exemple, il peut s’agir d’un nom plus convivial pour décrire l’expéditeur que le nom de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="bdf24-140">For example, this might be a more user-friendly name to describe the sender than the name of the mailbox.</span></span> <span data-ttu-id="bdf24-141">L’utilisation d’un nom complet est facultative.</span><span class="sxs-lookup"><span data-stu-id="bdf24-141">Using a display name is optional.</span></span> <span data-ttu-id="bdf24-142">Toutefois, si vous choisissez d’utiliser un nom complet, Microsoft vous recommande de toujours le placer entre guillemets comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="bdf24-142">However, if you choose to use a display name, Microsoft recommends that you always enclose it within quotation marks as shown.</span></span> 
    
- <span data-ttu-id="bdf24-143">Exige  *EmailAddress* est constituée des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="bdf24-143">(Required)  *emailaddress*  is made up of:</span></span> 
    
  ```
  local-part @domain
  ```

    <span data-ttu-id="bdf24-144">Où :</span><span class="sxs-lookup"><span data-stu-id="bdf24-144">Where:</span></span>
    
  - <span data-ttu-id="bdf24-145">Exige  le *composant local* est une chaîne qui identifie la boîte aux lettres associée à l’adresse.</span><span class="sxs-lookup"><span data-stu-id="bdf24-145">(Required)  *local-part*  is a string that identifies the mailbox associated with the address.</span></span> <span data-ttu-id="bdf24-146">Cela est unique au sein du domaine.</span><span class="sxs-lookup"><span data-stu-id="bdf24-146">This is unique within the domain.</span></span> <span data-ttu-id="bdf24-147">Souvent, le nom d’utilisateur ou le GUID du propriétaire de la boîte aux lettres est utilisé comme valeur de la partie locale.</span><span class="sxs-lookup"><span data-stu-id="bdf24-147">Often, the mailbox owner's username or GUID is used as the value for the local-part.</span></span> 
    
  - <span data-ttu-id="bdf24-148">Exige  *Domain* est le nom de domaine complet (FQDN) du serveur de messagerie qui héberge la boîte aux lettres identifiée par la partie locale de l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bdf24-148">(Required)  *domain*  is the fully-qualified domain name (FQDN) of the mail server that hosts the mailbox identified by the local-part of the email address.</span></span> 
    
### <a name="format-of-the-from-address-if-you-dont-include-a-display-name"></a><span data-ttu-id="bdf24-149">Format de l’adresse de : Si vous n’incluez pas de nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="bdf24-149">Format of the From: address if you don't include a display name</span></span>
<span data-ttu-id="bdf24-150"><a name="FormatNoDisplayName"> </a></span><span class="sxs-lookup"><span data-stu-id="bdf24-150"></span></span>

<span data-ttu-id="bdf24-151">Une adresse à partir de la mise en forme : l’adresse qui n’inclut pas de nom d’affichage n’inclut qu’une seule adresse de messagerie avec ou sans chevrons.</span><span class="sxs-lookup"><span data-stu-id="bdf24-151">A properly formatted From: address that does not include a display name includes only a single email address with or without angle brackets.</span></span> <span data-ttu-id="bdf24-152">Microsoft recommande de ne pas séparer les chevrons avec des espaces.</span><span class="sxs-lookup"><span data-stu-id="bdf24-152">Microsoft recommends that you do not separate the angle brackets with spaces.</span></span> <span data-ttu-id="bdf24-153">En outre, n’incluez rien après l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bdf24-153">In addition, don't include anything after the email address.</span></span>
  
<span data-ttu-id="bdf24-154">Les exemples suivants sont valides :</span><span class="sxs-lookup"><span data-stu-id="bdf24-154">The following examples are valid:</span></span>
  
```
From: sender@contoso.com
```

```
From: <sender@contoso.com>
```

<span data-ttu-id="bdf24-155">L’exemple suivant est valide mais pas recommandé, car il contient des espaces entre les chevrons et l’adresse de messagerie :</span><span class="sxs-lookup"><span data-stu-id="bdf24-155">The following example is valid but not recommended because it contains spaces between the angle brackets and the email address:</span></span>
  
```
From: < sender@contoso.com >
```

<span data-ttu-id="bdf24-156">L’exemple suivant n’est pas valide, car il contient du texte après l’adresse de messagerie :</span><span class="sxs-lookup"><span data-stu-id="bdf24-156">The following example is invalid because it contains text after the email address:</span></span>
  
```
From: "Office 365" <sender@contoso.com> (Sent by a process)
```

### <a name="format-of-the-from-address-if-you-include-a-display-name"></a><span data-ttu-id="bdf24-157">Format de l’adresse de : Si vous incluez un nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="bdf24-157">Format of the From: address if you include a display name</span></span>
<span data-ttu-id="bdf24-158"><a name="FormatDisplayName"> </a></span><span class="sxs-lookup"><span data-stu-id="bdf24-158"></span></span>

<span data-ttu-id="bdf24-159">Pour from : les adresses qui incluent une valeur pour le nom d’affichage, les règles suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="bdf24-159">For From: addresses that include a value for the display name, the following rules apply:</span></span>
  
- <span data-ttu-id="bdf24-160">Si l’adresse de l’expéditeur inclut un nom complet et que le nom d’affichage inclut une virgule, le nom d’affichage doit être placé entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="bdf24-160">If the sender address includes a display name, and the display name includes a comma, then the display name must be enclosed within quotation marks.</span></span> <span data-ttu-id="bdf24-161">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="bdf24-161">For example:</span></span>
    
    <span data-ttu-id="bdf24-162">L’exemple suivant est valide :</span><span class="sxs-lookup"><span data-stu-id="bdf24-162">The following example is valid:</span></span>
    
  ```
  From: "Sender, Example" <sender.example@contoso.com>
  ```

    <span data-ttu-id="bdf24-163">L’exemple suivant n’est pas valide :</span><span class="sxs-lookup"><span data-stu-id="bdf24-163">The following example is not valid:</span></span>
    
  ```
  From: Sender, Example <sender.example@contoso.com>
  ```

    <span data-ttu-id="bdf24-164">Ne pas placer le nom d’affichage entre guillemets si ce nom d’affichage inclut une virgule n’est pas valide conformément à la norme RFC 5322.</span><span class="sxs-lookup"><span data-stu-id="bdf24-164">Not enclosing the display name in quotation marks if that display name includes a comma is invalid according to RFC 5322.</span></span>
    
    <span data-ttu-id="bdf24-165">Il est recommandé de placer les guillemets entourant le nom d’affichage, qu’il y ait ou non une virgule dans le nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="bdf24-165">As a best practice, put quote marks around the display name regardless of whether or not there is a comma within the display name.</span></span>
    
- <span data-ttu-id="bdf24-166">Si l’adresse de l’expéditeur inclut un nom complet, l’adresse de messagerie doit être placée entre crochets pointus.</span><span class="sxs-lookup"><span data-stu-id="bdf24-166">If the sender address includes a display name, then the email address must be enclosed within angle brackets.</span></span>
    
    <span data-ttu-id="bdf24-167">Nous vous recommandons vivement d’insérer un espace entre le nom d’affichage et l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bdf24-167">As a best practice, Microsoft strongly recommends that you insert a space between the display name and the email address.</span></span>
    
### <a name="additional-examples-of-valid-and-invalid-from-addresses"></a><span data-ttu-id="bdf24-168">Exemples supplémentaires d’adresses valides et non valides :</span><span class="sxs-lookup"><span data-stu-id="bdf24-168">Additional examples of valid and invalid From: addresses</span></span>
<span data-ttu-id="bdf24-169"><a name="Examples"> </a></span><span class="sxs-lookup"><span data-stu-id="bdf24-169"></span></span>

- <span data-ttu-id="bdf24-170">Validation</span><span class="sxs-lookup"><span data-stu-id="bdf24-170">Valid:</span></span>
    
  ```
  From: "Office 365" <sender@contoso.com>
  ```

- <span data-ttu-id="bdf24-171">Non valide.</span><span class="sxs-lookup"><span data-stu-id="bdf24-171">Invalid.</span></span> <span data-ttu-id="bdf24-172">L’adresse de messagerie n’est pas entourée de crochets pointus :</span><span class="sxs-lookup"><span data-stu-id="bdf24-172">The email address is not enclosed with angle brackets:</span></span>
    
  ```
  From: Office 365 sender@contoso.com
  ```

- <span data-ttu-id="bdf24-173">Valide, mais pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="bdf24-173">Valid, but not recommended.</span></span> <span data-ttu-id="bdf24-174">Le nom d’affichage n’est pas entouré de guillemets.</span><span class="sxs-lookup"><span data-stu-id="bdf24-174">The display name is not in quotes.</span></span> <span data-ttu-id="bdf24-175">Pour une meilleure pratique, placez toujours le nom d’affichage entre guillemets :</span><span class="sxs-lookup"><span data-stu-id="bdf24-175">As a best practice, always put quotation marks around the display name:</span></span>
    
  ```
  From: Office 365 <sender@contoso.com>
  ```

- <span data-ttu-id="bdf24-176">Non valide.</span><span class="sxs-lookup"><span data-stu-id="bdf24-176">Invalid.</span></span> <span data-ttu-id="bdf24-177">Tout est placé entre guillemets, pas seulement le nom d’affichage :</span><span class="sxs-lookup"><span data-stu-id="bdf24-177">Everything is enclosed within quotation marks, not just the display name:</span></span>
    
  ```
  From: "Office 365 <sender@contoso.com>"
  ```

- <span data-ttu-id="bdf24-178">Non valide.</span><span class="sxs-lookup"><span data-stu-id="bdf24-178">Invalid.</span></span> <span data-ttu-id="bdf24-179">Il n’y a pas d’équerre entourant l’adresse de messagerie :</span><span class="sxs-lookup"><span data-stu-id="bdf24-179">There are no angle brackets around the email address:</span></span>
    
  ```
  From: "Office 365 <sender@contoso.com>" sender@contoso.com
  ```

- <span data-ttu-id="bdf24-180">Non valide.</span><span class="sxs-lookup"><span data-stu-id="bdf24-180">Invalid.</span></span> <span data-ttu-id="bdf24-181">Il n’y a pas d’espace entre le nom d’affichage et le crochet pointu gauche :</span><span class="sxs-lookup"><span data-stu-id="bdf24-181">There is no space between the display name and left angle bracket:</span></span>
    
  ```
  From: Office 365<sender@contoso.com>
  ```

- <span data-ttu-id="bdf24-182">Non valide.</span><span class="sxs-lookup"><span data-stu-id="bdf24-182">Invalid.</span></span> <span data-ttu-id="bdf24-183">Il n’y a pas d’espace entre le guillemet de fermeture entourant le nom d’affichage et le crochet pointu gauche.</span><span class="sxs-lookup"><span data-stu-id="bdf24-183">There is no space between the closing quotation mark around the display name and the left angle bracket.</span></span>
    
  ```
  From: "Office 365"<sender@contoso.com>
  ```

### <a name="suppress-auto-replies-to-your-custom-domain-without-breaking-the-from-policy"></a><span data-ttu-id="bdf24-184">Supprimer les réponses automatiques à votre domaine personnalisé sans rompre la stratégie de :</span><span class="sxs-lookup"><span data-stu-id="bdf24-184">Suppress auto-replies to your custom domain without breaking the From: policy</span></span>
<span data-ttu-id="bdf24-185"><a name="SuppressAutoReply"> </a></span><span class="sxs-lookup"><span data-stu-id="bdf24-185"></span></span>

<span data-ttu-id="bdf24-186">Avec la nouvelle from : application de stratégie, vous ne pouvez plus utiliser from \< \> : pour supprimer les réponses automatiques.</span><span class="sxs-lookup"><span data-stu-id="bdf24-186">With the new From: policy enforcement, you can no longer use From: \<\> to suppress auto-replies.</span></span> <span data-ttu-id="bdf24-187">Au lieu de cela, vous devez configurer un enregistrement MX null pour votre domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="bdf24-187">Instead, you need to set up a null MX record for your custom domain.</span></span>
  
<span data-ttu-id="bdf24-188">L’enregistrement de serveur de messagerie (MX) est un enregistrement de ressource dans le DNS qui identifie le serveur de messagerie qui reçoit les messages pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="bdf24-188">The mail exchanger (MX) record is a resource record in DNS that identifies the mail server that receives mail for your domain.</span></span> <span data-ttu-id="bdf24-189">Les réponses automatiques (et toutes les réponses) sont naturellement supprimées car il n’existe aucune adresse publiée à laquelle le serveur de réponse peut envoyer des messages.</span><span class="sxs-lookup"><span data-stu-id="bdf24-189">Auto-replies (and all replies) are naturally suppressed because there is no published address to which the responding server can send messages.</span></span>
  
<span data-ttu-id="bdf24-190">Lorsque vous configurez un enregistrement MX null pour votre domaine personnalisé :</span><span class="sxs-lookup"><span data-stu-id="bdf24-190">When you set up a null MX record for your custom domain:</span></span>
  
- <span data-ttu-id="bdf24-191">Choisissez un domaine à partir duquel envoyer des messages qui n’acceptent pas (recevoir) des courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="bdf24-191">Choose a domain from which to send messages that doesn't accept (receive) email.</span></span> <span data-ttu-id="bdf24-192">Par exemple, si votre domaine principal est contoso.com, vous pouvez choisir noreply.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="bdf24-192">For example, if your primary domain is contoso.com, you might choose noreply.contoso.com.</span></span>
    
- <span data-ttu-id="bdf24-193">Configurez l’enregistrement MX null pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="bdf24-193">Set up the null MX record for your domain.</span></span> <span data-ttu-id="bdf24-194">Un enregistrement MX null se compose d’un point unique, par exemple :</span><span class="sxs-lookup"><span data-stu-id="bdf24-194">A null MX record consists of a single dot, for example:</span></span>
    
  ```
  noreply.contoso.com IN MX .
  ```

<span data-ttu-id="bdf24-195">Pour plus d’informations sur la publication d’une valeur null MX, voir [RFC 7505](https://tools.ietf.org/html/rfc7505).</span><span class="sxs-lookup"><span data-stu-id="bdf24-195">For more information about publishing a null MX, see [RFC 7505](https://tools.ietf.org/html/rfc7505).</span></span>
  
### <a name="overriding-the-office-365-from-address-enforcement-policy"></a><span data-ttu-id="bdf24-196">Remplacement d’Office 365 de : stratégie de mise en œuvre des adresses</span><span class="sxs-lookup"><span data-stu-id="bdf24-196">Overriding the Office 365 From: address enforcement policy</span></span>
<span data-ttu-id="bdf24-197"><a name="Override"> </a></span><span class="sxs-lookup"><span data-stu-id="bdf24-197"></span></span>

<span data-ttu-id="bdf24-198">Une fois le déploiement de la nouvelle stratégie terminé, vous pouvez uniquement contourner cette stratégie pour le courrier entrant que vous recevez d’Office 365 à l’aide de l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="bdf24-198">Once roll out of the new policy is complete, you can only bypass this policy for inbound mail you receive from Office 365 by using one of the following methods:</span></span> 
  
- <span data-ttu-id="bdf24-199">Listes d’adresses IP autorisées</span><span class="sxs-lookup"><span data-stu-id="bdf24-199">IP allow lists</span></span>
    
- <span data-ttu-id="bdf24-200">Règles de flux de messagerie Exchange Online</span><span class="sxs-lookup"><span data-stu-id="bdf24-200">Exchange Online mail flow rules</span></span>
    
<span data-ttu-id="bdf24-201">Microsoft recommande fortement de remplacer l’application de la stratégie from :.</span><span class="sxs-lookup"><span data-stu-id="bdf24-201">Microsoft strongly recommends against overriding the enforcement of the From: policy.</span></span> <span data-ttu-id="bdf24-202">Le remplacement de cette stratégie peut augmenter le risque d’exposition de votre organisation au courrier indésirable, au hameçonnage et à d’autres crimes.</span><span class="sxs-lookup"><span data-stu-id="bdf24-202">Overriding this policy can increase your organization's risk of exposure to spam, phishing, and other cybercrimes.</span></span>
  
<span data-ttu-id="bdf24-203">Vous ne pouvez pas remplacer cette stratégie pour les messages sortants que vous envoyez dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="bdf24-203">You cannot override this policy for outbound mail you send in Office 365.</span></span> <span data-ttu-id="bdf24-204">De plus, Outlook.com n’autorisera pas les remplacements, même via la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="bdf24-204">In addition, Outlook.com will not allow overrides of any kind, even through support.</span></span> 
  
### <a name="other-ways-to-prevent-and-protect-against-cybercrimes-in-office-365"></a><span data-ttu-id="bdf24-205">Autres méthodes pour prévenir et protéger contre les cybercriminels dans Office 365</span><span class="sxs-lookup"><span data-stu-id="bdf24-205">Other ways to prevent and protect against cybercrimes in Office 365</span></span>
<span data-ttu-id="bdf24-206"><a name="OtherProtection"> </a></span><span class="sxs-lookup"><span data-stu-id="bdf24-206"></span></span>

<span data-ttu-id="bdf24-207">Pour plus d’informations sur la façon dont vous pouvez renforcer votre organisation contre les cybercriminels, tels que le hameçonnage, le courrier indésirable, les violations de données et d’autres menaces, consultez la rubrique [meilleures pratiques en matière de sécurité pour Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).</span><span class="sxs-lookup"><span data-stu-id="bdf24-207">For more information on how you can strengthen your organization against cybercrimes like phishing, spamming, data breaches, and other threats, see [Security best practices for Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="bdf24-208">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bdf24-208">Related Topics</span></span>

[<span data-ttu-id="bdf24-209">Messages de rétrodiffusion et EOP</span><span class="sxs-lookup"><span data-stu-id="bdf24-209">Backscatter messages and EOP</span></span>](https://technet.microsoft.com/en-us/library/dn499795%28v=exchg.150%29.aspx)
  


---
title: Référence des conseils de stratégie de protection contre la perte de données
f1.keywords: CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MET150
ms.assetid: 6501b5ef-6bf7-43df-b60d-f65781847d6c
ms.collection:
- M365-security-compliance
- SPO_Content
description: Découvrez comment ajouter un conseil de stratégie à une stratégie de protection contre la perte de données (DLP) pour informer un utilisateur qu'il travaille avec du contenu en conflit avec une stratégie DLP.
ms.custom: seo-marvel-apr2021
ms.openlocfilehash: 693f511b6303fb07d393c62efb4a61631b844474
ms.sourcegitcommit: 2655bb0ccd66279c35be2fadbd893c937d084109
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2021
ms.locfileid: "51876811"
---
# <a name="data-loss-prevention-policy-tips-reference"></a><span data-ttu-id="705af-103">Informations de référence sur les conseils de stratégie de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="705af-103">Data Loss Prevention policy tips reference</span></span>

<span data-ttu-id="705af-104">Les conseils de stratégie DLP dans Outlook Web Access sont pris en charge pour toutes les conditions, exceptions et actions applicables sur la charge de travail Exchange dans une stratégie DLP, sauf les suivantes :</span><span class="sxs-lookup"><span data-stu-id="705af-104">DLP policy tips in Outlook Web Access is supported for all the conditions, exceptions and actions that are applicable on Exchange workload in a DLP policy except the following:</span></span>

<span data-ttu-id="705af-105">**Conditions :**</span><span class="sxs-lookup"><span data-stu-id="705af-105">**Conditions:**</span></span>

- <span data-ttu-id="705af-106">L'expéditeur est</span><span class="sxs-lookup"><span data-stu-id="705af-106">Sender Is</span></span>
- <span data-ttu-id="705af-107">Le domaine de l'expéditeur est</span><span class="sxs-lookup"><span data-stu-id="705af-107">Sender Domain Is</span></span>
- <span data-ttu-id="705af-108">Le destinataire est membre de</span><span class="sxs-lookup"><span data-stu-id="705af-108">Recipient is a member of</span></span>
- <span data-ttu-id="705af-109">L'en-tête contient des mots ou des expressions</span><span class="sxs-lookup"><span data-stu-id="705af-109">Header contains words or phrases</span></span>
- <span data-ttu-id="705af-110">L'en-tête correspond aux modèles</span><span class="sxs-lookup"><span data-stu-id="705af-110">Header matches patterns</span></span>
- <span data-ttu-id="705af-111">La taille du document est égale ou supérieure à</span><span class="sxs-lookup"><span data-stu-id="705af-111">Document size equals or is greater than</span></span>
- <span data-ttu-id="705af-112">Le type de message est</span><span class="sxs-lookup"><span data-stu-id="705af-112">Message type is</span></span>
- <span data-ttu-id="705af-113">L'importance du message est</span><span class="sxs-lookup"><span data-stu-id="705af-113">Message importance is</span></span>
- <span data-ttu-id="705af-114">Le jeu de caractères de contenu contient des mots</span><span class="sxs-lookup"><span data-stu-id="705af-114">Content character set contains words</span></span>
- <span data-ttu-id="705af-115">L'objet ou le corps contient des mots ou des expressions</span><span class="sxs-lookup"><span data-stu-id="705af-115">Subject or body contains words or phrases</span></span>
- <span data-ttu-id="705af-116">L'objet ou le corps correspond aux modèles</span><span class="sxs-lookup"><span data-stu-id="705af-116">Subject or body matches patterns</span></span>
- <span data-ttu-id="705af-117">Le jeu de caractères de contenu contient des mots</span><span class="sxs-lookup"><span data-stu-id="705af-117">Content character set contains words</span></span>
- <span data-ttu-id="705af-118">Le contenu est reçu de</span><span class="sxs-lookup"><span data-stu-id="705af-118">Content is received from</span></span>
- <span data-ttu-id="705af-119">L'expéditeur a-t-il surchargé le conseil de stratégie</span><span class="sxs-lookup"><span data-stu-id="705af-119">Has sender overridden the policy tip</span></span>
- <span data-ttu-id="705af-120">La taille du message est égale ou supérieure à</span><span class="sxs-lookup"><span data-stu-id="705af-120">Message size equals or is greater than</span></span>
- <span data-ttu-id="705af-121">L'attribut AD de l'expéditeur contient des mots ou des expressions</span><span class="sxs-lookup"><span data-stu-id="705af-121">Sender AD attribute contains words or phrases</span></span>
- <span data-ttu-id="705af-122">L'attribut AD de l'expéditeur correspond aux modèles</span><span class="sxs-lookup"><span data-stu-id="705af-122">Sender AD attribute matches patterns</span></span>
- <span data-ttu-id="705af-123">Le contenu du document contient des mots ou des expressions</span><span class="sxs-lookup"><span data-stu-id="705af-123">Document content contains words or phrases</span></span>
- <span data-ttu-id="705af-124">Le contenu du document correspond aux modèles</span><span class="sxs-lookup"><span data-stu-id="705af-124">Document content matches patterns</span></span>

<span data-ttu-id="705af-125">**Actions :**</span><span class="sxs-lookup"><span data-stu-id="705af-125">**Actions:**</span></span>

- <span data-ttu-id="705af-126">Transmettre le message pour approbation au responsable de l'expéditeur</span><span class="sxs-lookup"><span data-stu-id="705af-126">Forward the message for approval to sender’s manager</span></span>
- <span data-ttu-id="705af-127">Transmettre le message pour approbation à des approuveurs spécifiques</span><span class="sxs-lookup"><span data-stu-id="705af-127">Forward the message for approval to specific approvers</span></span>
- <span data-ttu-id="705af-128">Rediriger le message vers des utilisateurs spécifiques</span><span class="sxs-lookup"><span data-stu-id="705af-128">Redirect the message to specific users</span></span>
- <span data-ttu-id="705af-129">Ajouter des destinataires à la zone À</span><span class="sxs-lookup"><span data-stu-id="705af-129">Add recipients to the To Box</span></span>
- <span data-ttu-id="705af-130">Ajouter des destinataires à la zone Cc</span><span class="sxs-lookup"><span data-stu-id="705af-130">Add recipients to the Cc Box</span></span>
- <span data-ttu-id="705af-131">Ajouter des destinataires à la zone Bcc</span><span class="sxs-lookup"><span data-stu-id="705af-131">Add recipients to the Bcc Box</span></span>
- <span data-ttu-id="705af-132">Ajouter le responsable de l'expéditeur en tant que destinataire</span><span class="sxs-lookup"><span data-stu-id="705af-132">Add the sender’s manager as recipient</span></span>
- <span data-ttu-id="705af-133">Ajouter une clause d'exclusion de responsabilité HTML</span><span class="sxs-lookup"><span data-stu-id="705af-133">Add HTML disclaimer</span></span>
- <span data-ttu-id="705af-134">Prédépender l'objet de l'e-mail</span><span class="sxs-lookup"><span data-stu-id="705af-134">Prepend email subject</span></span>
- <span data-ttu-id="705af-135">Supprimer le chiffrement de messages O365 et la protection des droits</span><span class="sxs-lookup"><span data-stu-id="705af-135">Remove O365 Message Encryption and rights protection</span></span>
- <span data-ttu-id="705af-136">Supprimer</span><span class="sxs-lookup"><span data-stu-id="705af-136">Remove</span></span>

## <a name="outlook-2013-and-later-supports-showing-policy-tips-for-only-some-conditions-and-exceptions"></a><span data-ttu-id="705af-137">Outlook 2013 et les ultérieures prend en charge l'affichage de conseils de stratégie uniquement pour certaines conditions et exceptions</span><span class="sxs-lookup"><span data-stu-id="705af-137">Outlook 2013 and later supports showing policy tips for only some conditions and exceptions</span></span>

<span data-ttu-id="705af-138">Actuellement, Outlook 2013 et les ultérieures prend en charge l'affichage de conseils de stratégie pour les stratégies qui ne contiennent aucune condition ou exception à part les conditions mentionnées ci-dessous et les exceptions correspondantes :</span><span class="sxs-lookup"><span data-stu-id="705af-138">Currently, Outlook 2013 and later supports showing policy tips for policies which do not contain any condition or exception apart from the below mentioned conditions and corresponding exceptions :</span></span>

- <span data-ttu-id="705af-139">Le contenu contient (fonctionne uniquement pour les types d'informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="705af-139">Content contains (works only for Sensitive information types.</span></span> <span data-ttu-id="705af-140">Les étiquettes de niveau de sensibilité ne sont pas pris en charge)</span><span class="sxs-lookup"><span data-stu-id="705af-140">Sensitivity labels are not supported)</span></span>
- <span data-ttu-id="705af-141">Le contenu est partagé</span><span class="sxs-lookup"><span data-stu-id="705af-141">Content is shared</span></span>

<span data-ttu-id="705af-142">Notez que toutes les conditions fonctionnent pour les e-mails rédigés dans l’application cliente Outlook, où ils correspondent au contenu et appliquent des actions de protection sur le contenu.</span><span class="sxs-lookup"><span data-stu-id="705af-142">Note that all the conditions work for emails authored in Outlook client app, where they will match content and enforce protective actions on content.</span></span> <span data-ttu-id="705af-143">Toutefois, l’affichage des conseils de stratégie aux utilisateurs n’est pas encore pris en charge pour les conditions qui sont utilisées en dehors de celle mentionnée ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="705af-143">However, showing policy tips to users is not yet supported for any conditions that are used apart from the ones mentioned above.</span></span>

## <a name="outlook-2013-and-later-supports-showing-policy-tips-for-only-some-sensitive-information-types"></a><span data-ttu-id="705af-144">Outlook 2013 et les ultérieures prend en charge l’affichage de conseils de stratégie pour certains types d’informations sensibles uniquement</span><span class="sxs-lookup"><span data-stu-id="705af-144">Outlook 2013 and later supports showing policy tips for only some sensitive information types</span></span>

<span data-ttu-id="705af-145">La liste des types d’informations sensibles pré-détectés pour l’affichage des conseils de stratégie DLP dans Outlook sur bureau (2013 et version ultérieure) est la suivante :</span><span class="sxs-lookup"><span data-stu-id="705af-145">The list of out-of-the-box sensitive information types that will be detected for showing DLP policy tips in Outlook on Desktop (2013 and later) are the following :</span></span>

- <span data-ttu-id="705af-146">Numéro de routage ABA</span><span class="sxs-lookup"><span data-stu-id="705af-146">ABA Routing Number</span></span>
- <span data-ttu-id="705af-147">Numéro d’identité nationale (DNI) pour l’Argentine</span><span class="sxs-lookup"><span data-stu-id="705af-147">Argentina National Identity (DNI) Number</span></span>
- <span data-ttu-id="705af-148">Numéro de compte bancaire Australie</span><span class="sxs-lookup"><span data-stu-id="705af-148">Australia Bank Account Number</span></span>
- <span data-ttu-id="705af-149">Numéro de dossier médical Australie</span><span class="sxs-lookup"><span data-stu-id="705af-149">Australia Medical Account Number</span></span>
- <span data-ttu-id="705af-150">Numéro de passeport Australie</span><span class="sxs-lookup"><span data-stu-id="705af-150">Australia Passport Number</span></span>
- <span data-ttu-id="705af-151">Numéro de dossier fiscal Australie</span><span class="sxs-lookup"><span data-stu-id="705af-151">Australia Tax File Number</span></span>
- <span data-ttu-id="705af-152">Clé d’th Azure DocumentDB</span><span class="sxs-lookup"><span data-stu-id="705af-152">Azure DocumentDB Auth Key</span></span>  
- <span data-ttu-id="705af-153">Chaîne de connexion de base de données IAAS Azure et chaîne SQL connexion Azure</span><span class="sxs-lookup"><span data-stu-id="705af-153">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>  
- <span data-ttu-id="705af-154">Chaîne de connexion Azure IoT</span><span class="sxs-lookup"><span data-stu-id="705af-154">Azure IoT Connection String</span></span>  
- <span data-ttu-id="705af-155">Mot de passe de paramètre de publication Azure</span><span class="sxs-lookup"><span data-stu-id="705af-155">Azure Publish Setting Password</span></span>  
- <span data-ttu-id="705af-156">Chaîne de connexion du cache Azure Redis</span><span class="sxs-lookup"><span data-stu-id="705af-156">Azure Redis Cache Connection String</span></span>  
- <span data-ttu-id="705af-157">Azure SAS</span><span class="sxs-lookup"><span data-stu-id="705af-157">Azure SAS</span></span>  
- <span data-ttu-id="705af-158">Chaîne de connexion Azure Service Bus</span><span class="sxs-lookup"><span data-stu-id="705af-158">Azure Service Bus Connection String</span></span>  
- <span data-ttu-id="705af-159">Clé de compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="705af-159">Azure Storage Account Key</span></span>  
- <span data-ttu-id="705af-160">Clé de compte de stockage Azure (générique)</span><span class="sxs-lookup"><span data-stu-id="705af-160">Azure Storage Account Key (Generic)</span></span>  
- <span data-ttu-id="705af-161">Numéro national belge</span><span class="sxs-lookup"><span data-stu-id="705af-161">Belgium National Number</span></span>
- <span data-ttu-id="705af-162">Numéro CPF Brésil</span><span class="sxs-lookup"><span data-stu-id="705af-162">Brazil CPF Number</span></span>
- <span data-ttu-id="705af-163">Numéro d’entité juridique (CNPJ) Brésil</span><span class="sxs-lookup"><span data-stu-id="705af-163">Brazil Legal Entity Number (CNPJ)</span></span>
- <span data-ttu-id="705af-164">	Brazil National ID Card (RG)</span><span class="sxs-lookup"><span data-stu-id="705af-164">Brazil National ID Card (RG)</span></span>
- <span data-ttu-id="705af-165">Numéro de compte bancaire Canada</span><span class="sxs-lookup"><span data-stu-id="705af-165">Canada Bank Account Number</span></span>
- <span data-ttu-id="705af-166">Numéro de permis de conduire Canada</span><span class="sxs-lookup"><span data-stu-id="705af-166">Canada Driver's License Number</span></span>
- <span data-ttu-id="705af-167">Numéro de service de santé Canada</span><span class="sxs-lookup"><span data-stu-id="705af-167">Canada Health Service Number</span></span>
- <span data-ttu-id="705af-168">Numéro de passeport Canada</span><span class="sxs-lookup"><span data-stu-id="705af-168">Canada Passport Number</span></span>
- <span data-ttu-id="705af-169">NIMP (numéro d’identification médicale personnel) Canada</span><span class="sxs-lookup"><span data-stu-id="705af-169">Canada Personal Health Identification Number (PHIN)</span></span>
- <span data-ttu-id="705af-170">Numéro d'assurance sociale Canada</span><span class="sxs-lookup"><span data-stu-id="705af-170">Canada Social Insurance Number</span></span>
- <span data-ttu-id="705af-171">	Numéro de carte d’identité Chili</span><span class="sxs-lookup"><span data-stu-id="705af-171">Chile Identity Card Number</span></span>
- <span data-ttu-id="705af-172">	Numéro de carte d’identité de résident Chine (RPC)</span><span class="sxs-lookup"><span data-stu-id="705af-172">China Resident Identity Card (PRC) Number</span></span>
- <span data-ttu-id="705af-173">Numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="705af-173">Credit Card Number</span></span>
- <span data-ttu-id="705af-174">Numéro de carte d’identité croate</span><span class="sxs-lookup"><span data-stu-id="705af-174">Croatia Identity Card Number</span></span>  
- <span data-ttu-id="705af-175">Numéro d’identification personnelle croate (OIB)</span><span class="sxs-lookup"><span data-stu-id="705af-175">Croatia Personal Identification (OIB) Number</span></span>  
- <span data-ttu-id="705af-176">Numéro d’identité personnel tchèque</span><span class="sxs-lookup"><span data-stu-id="705af-176">Czech Personal Identity Number</span></span>  
- <span data-ttu-id="705af-177">Numéro d’identification personnelle danois</span><span class="sxs-lookup"><span data-stu-id="705af-177">Denmark Personal Identification Number</span></span>
- <span data-ttu-id="705af-178">Numéro de la Drug Enforcement Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="705af-178">Drug Enforcement Agency (DEA) Number</span></span>
- <span data-ttu-id="705af-179">Numéro de carte de crédit de l'U.E.</span><span class="sxs-lookup"><span data-stu-id="705af-179">EU Debit Card Number</span></span>
- <span data-ttu-id="705af-180">Numéro de permis de conduire de l’UE</span><span class="sxs-lookup"><span data-stu-id="705af-180">EU Driver's License Number</span></span>  
- <span data-ttu-id="705af-181">Numéro d’identification national de l’UE</span><span class="sxs-lookup"><span data-stu-id="705af-181">EU National Identification Number</span></span>  
- <span data-ttu-id="705af-182">Numéro de passeport de l’UE</span><span class="sxs-lookup"><span data-stu-id="705af-182">EU Passport Number</span></span>  
- <span data-ttu-id="705af-183">Numéro de sécurité sociale de l’UE (SSN) ou ID équivalent</span><span class="sxs-lookup"><span data-stu-id="705af-183">EU Social Security Number (SSN) or Equivalent ID</span></span>  
- <span data-ttu-id="705af-184">Numéro d’identification fiscale de l’UE (TIN)</span><span class="sxs-lookup"><span data-stu-id="705af-184">EU Tax Identification Number (TIN)</span></span>  
- <span data-ttu-id="705af-185">Numéro d'identification national finlandais</span><span class="sxs-lookup"><span data-stu-id="705af-185">Finland National ID</span></span>
- <span data-ttu-id="705af-186">Numéro de passeport finlandais</span><span class="sxs-lookup"><span data-stu-id="705af-186">Finland Passport Number</span></span>
- <span data-ttu-id="705af-187">Numéro de permis de conduire français</span><span class="sxs-lookup"><span data-stu-id="705af-187">France Driver's License Number</span></span>
- <span data-ttu-id="705af-188">Carte nationale d'identité (CNI) française</span><span class="sxs-lookup"><span data-stu-id="705af-188">France National ID Card (CNI)</span></span>
- <span data-ttu-id="705af-189">Numéro de passeport français</span><span class="sxs-lookup"><span data-stu-id="705af-189">France Passport Number</span></span>
- <span data-ttu-id="705af-190">Numéro de sécurité sociale (INSEE) français</span><span class="sxs-lookup"><span data-stu-id="705af-190">France Social Security Number (INSEE)</span></span>
- <span data-ttu-id="705af-191">Numéro de permis de conduire allemand</span><span class="sxs-lookup"><span data-stu-id="705af-191">German Driver's License Number</span></span>
- <span data-ttu-id="705af-192">Numéro de passeport allemand</span><span class="sxs-lookup"><span data-stu-id="705af-192">German Passport Number</span></span>
- <span data-ttu-id="705af-193">Numéro de carte d’identité allemand</span><span class="sxs-lookup"><span data-stu-id="705af-193">Germany Identity Card Number</span></span>
- <span data-ttu-id="705af-194">Carte d’identité nationale grecque</span><span class="sxs-lookup"><span data-stu-id="705af-194">Greece National ID Card</span></span>  
- <span data-ttu-id="705af-195">Numéro de carte d’identité (HKID) Hong Kong</span><span class="sxs-lookup"><span data-stu-id="705af-195">Hong Kong Identity Card (HKID) Number</span></span>
- <span data-ttu-id="705af-196">Numéro de compte permanent Inde</span><span class="sxs-lookup"><span data-stu-id="705af-196">India Permanent Account Number (PAN)</span></span>
- <span data-ttu-id="705af-197">Numéro d’identification unique (Aadhaar) Inde</span><span class="sxs-lookup"><span data-stu-id="705af-197">India Unique Identification (Aadhaar) Number</span></span>
- <span data-ttu-id="705af-198">Numéro de carte d’identité (KTP) Indonésie</span><span class="sxs-lookup"><span data-stu-id="705af-198">Indonesia Identity Card (KTP) Number</span></span>
- <span data-ttu-id="705af-199">Numéro de compte international (IBAN)</span><span class="sxs-lookup"><span data-stu-id="705af-199">International Banking Account Number (IBAN)</span></span>
- <span data-ttu-id="705af-200">Classification internationale des maladie (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="705af-200">International Classification of Diseases (ICD-10-CM)</span></span>  
- <span data-ttu-id="705af-201">Classification internationale des maladie (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="705af-201">International Classification of Diseases (ICD-9-CM)</span></span>  
- <span data-ttu-id="705af-202">Adresse IP</span><span class="sxs-lookup"><span data-stu-id="705af-202">IP Address</span></span>
- <span data-ttu-id="705af-203">Numéro personnel pour le service public irlandais (PPS)</span><span class="sxs-lookup"><span data-stu-id="705af-203">Ireland Personal Public Service (PPS) Number</span></span> 
- <span data-ttu-id="705af-204">Numéro de compte bancaire Israël</span><span class="sxs-lookup"><span data-stu-id="705af-204">Israel Bank Account Number</span></span>
- <span data-ttu-id="705af-205">Carte nationale d’identité Israël</span><span class="sxs-lookup"><span data-stu-id="705af-205">Israel National ID</span></span>
- <span data-ttu-id="705af-206">Numéro de permis de conduire Italie</span><span class="sxs-lookup"><span data-stu-id="705af-206">Italy Driver's License Number</span></span>
- <span data-ttu-id="705af-207">Numéro de compte bancaire Japon</span><span class="sxs-lookup"><span data-stu-id="705af-207">Japan Bank Account Number</span></span>
- <span data-ttu-id="705af-208">Numéro de permis de conduire Japon</span><span class="sxs-lookup"><span data-stu-id="705af-208">Japan Driver's License Number</span></span>
- <span data-ttu-id="705af-209">Numéro de passeport Japon</span><span class="sxs-lookup"><span data-stu-id="705af-209">Japan Passport Number</span></span>
- <span data-ttu-id="705af-210">Matricule de résident Japon</span><span class="sxs-lookup"><span data-stu-id="705af-210">Japan Resident Registration Number</span></span>
- <span data-ttu-id="705af-211">Numéro d’assurance sociale Japon</span><span class="sxs-lookup"><span data-stu-id="705af-211">Japan Social Insurance Number (SIN)</span></span>
- <span data-ttu-id="705af-212">Numéro de carte de résidence (japonais)</span><span class="sxs-lookup"><span data-stu-id="705af-212">Japanese Residence Card Number</span></span>
- <span data-ttu-id="705af-213">Numéro de carte d’identité Malaisie</span><span class="sxs-lookup"><span data-stu-id="705af-213">Malaysia Identity Card Number</span></span>
- <span data-ttu-id="705af-214">Numéro de service du citoyen (BSN) néerlandais</span><span class="sxs-lookup"><span data-stu-id="705af-214">Netherlands Citizen's Service (BSN) Number</span></span>  
- <span data-ttu-id="705af-215">Numéro du Ministère de la santé Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="705af-215">New Zealand Ministry of Health Number</span></span>
- <span data-ttu-id="705af-216">Numéro d’identité norvégien</span><span class="sxs-lookup"><span data-stu-id="705af-216">Norway Identity Number</span></span>  
- <span data-ttu-id="705af-217">Numéro d’identification multifonction unifié Philippines</span><span class="sxs-lookup"><span data-stu-id="705af-217">Philippines Unified Multi-Purpose ID Number</span></span>
- <span data-ttu-id="705af-218">Carte d'identité polonaise</span><span class="sxs-lookup"><span data-stu-id="705af-218">Poland Identity Card</span></span>
- <span data-ttu-id="705af-219">Numéro d'identification national polonais (PESEL)</span><span class="sxs-lookup"><span data-stu-id="705af-219">Poland National ID (PESEL)</span></span>
- <span data-ttu-id="705af-220">Numéro de passeport polonais</span><span class="sxs-lookup"><span data-stu-id="705af-220">Poland Passport</span></span>
- <span data-ttu-id="705af-221">Numéro de carte de citoyen portugais</span><span class="sxs-lookup"><span data-stu-id="705af-221">Portugal Citizen Card Number</span></span>
- <span data-ttu-id="705af-222">ID national Arabie saoudite</span><span class="sxs-lookup"><span data-stu-id="705af-222">Saudi Arabia National ID</span></span>
- <span data-ttu-id="705af-223">Numéro de carte d’identité d’enregistrement national (NRIC) Singapour</span><span class="sxs-lookup"><span data-stu-id="705af-223">Singapore National Registration Identity Card (NRIC) Number</span></span>
- <span data-ttu-id="705af-224">Numéro d’identification Afrique du Sud</span><span class="sxs-lookup"><span data-stu-id="705af-224">South Africa Identification Number</span></span>  
- <span data-ttu-id="705af-225">Matricule de résident Corée du Sud</span><span class="sxs-lookup"><span data-stu-id="705af-225">South Korea Resident Registration Number</span></span>
- <span data-ttu-id="705af-226">Numéro de sécurité sociale (N° S.S.) espagnol</span><span class="sxs-lookup"><span data-stu-id="705af-226">Spain Social Security Number (SSN)</span></span>
- <span data-ttu-id="705af-227">SQL Server Connection String</span><span class="sxs-lookup"><span data-stu-id="705af-227">SQL Server Connection String</span></span>  
- <span data-ttu-id="705af-228">ID national suédois</span><span class="sxs-lookup"><span data-stu-id="705af-228">Sweden National ID</span></span>
- <span data-ttu-id="705af-229">Numéro de passeport suédois</span><span class="sxs-lookup"><span data-stu-id="705af-229">Sweden Passport Number</span></span>
- <span data-ttu-id="705af-230">Code SWIFT</span><span class="sxs-lookup"><span data-stu-id="705af-230">SWIFT Code</span></span>
- <span data-ttu-id="705af-231">ID national à Taïwan</span><span class="sxs-lookup"><span data-stu-id="705af-231">Taiwan National ID</span></span>
- <span data-ttu-id="705af-232">	Numéro de passeport Taïwan</span><span class="sxs-lookup"><span data-stu-id="705af-232">Taiwan Passport Number</span></span>
- <span data-ttu-id="705af-233">Certificat de résident Taïwan (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="705af-233">Taiwan Resident Certificate (ARC/TARC)</span></span>
- <span data-ttu-id="705af-234">Code d’identification de la population thaï</span><span class="sxs-lookup"><span data-stu-id="705af-234">Thai Population Identification Code</span></span>
- <span data-ttu-id="705af-235">Numéro d’identification nationale turc</span><span class="sxs-lookup"><span data-stu-id="705af-235">Turkish National Identification number</span></span>
- <span data-ttu-id="705af-p103">Numéro de permis de conduire du Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="705af-p103">U.K. Driver's License Number</span></span>
- <span data-ttu-id="705af-p104">Numéro de liste électorale du Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="705af-p104">U.K. Electoral Roll Number</span></span>
- <span data-ttu-id="705af-p105">Numéro du service de santé national (NHS) du Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="705af-p105">U.K. National Health Service Number</span></span>
- <span data-ttu-id="705af-p106">Numéro d'assurance national (NINO) du Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="705af-p106">U.K. National Insurance Number (NINO)</span></span>
- <span data-ttu-id="705af-244">États-Unis/Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="705af-244">U.S. / U.K.</span></span> <span data-ttu-id="705af-245">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="705af-245">Passport Number</span></span>
- <span data-ttu-id="705af-246">Numéro de compte bancaire États-Unis</span><span class="sxs-lookup"><span data-stu-id="705af-246">U.S. Bank Account Number</span></span>
- <span data-ttu-id="705af-247">Numéro de permis de conduire États-Unis</span><span class="sxs-lookup"><span data-stu-id="705af-247">U.S. Driver's License Number</span></span>
- <span data-ttu-id="705af-248">Numéro d’identification fiscale individuel (ITIN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="705af-248">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="705af-249">Numéro de sécurité sociale (SSN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="705af-249">U.S. Social Security Number (SSN)</span></span>

<span data-ttu-id="705af-250">Notez que les types d’informations sensibles personnalisés sont également pris en charge pour les conseils de stratégie DLP en plus des types d’informations sensibles pré-personnalisés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="705af-250">Please note that custom sensitive information types are also supported for DLP policy tips in addition to the above out-of-the-box sensitive information types.</span></span>

## <a name="data-loss-prevention-on-endpoint-supports-policy-tips-for-only-some-sensitive-information-types"></a><span data-ttu-id="705af-251">La protection contre la perte de données sur le point de terminaison prend en charge les conseils de stratégie pour certains types d’informations sensibles uniquement</span><span class="sxs-lookup"><span data-stu-id="705af-251">Data Loss Prevention on Endpoint supports policy tips for only some sensitive information types</span></span>

<span data-ttu-id="705af-252">La liste des types d’informations sensibles pré-utilisés qui seront détectés dans les documents résidant sur les appareils de point de terminaison est la suivante :</span><span class="sxs-lookup"><span data-stu-id="705af-252">The list of out-of-the-box sensitive information types that will be detected in documents residing on endpoint devices are the following :</span></span>

- <span data-ttu-id="705af-253">Numéro de routage ABA</span><span class="sxs-lookup"><span data-stu-id="705af-253">ABA Routing Number</span></span> 
- <span data-ttu-id="705af-254">Numéro d’identité nationale (DNI) pour l’Argentine</span><span class="sxs-lookup"><span data-stu-id="705af-254">Argentina National Identity (DNI) Number</span></span> 
- <span data-ttu-id="705af-255">Numéro de compte bancaire Australie</span><span class="sxs-lookup"><span data-stu-id="705af-255">Australia Bank Account Number</span></span> 
- <span data-ttu-id="705af-256">Numéro de dossier médical Australie</span><span class="sxs-lookup"><span data-stu-id="705af-256">Australia Medical Account Number</span></span> 
- <span data-ttu-id="705af-257">Numéro de passeport Australie</span><span class="sxs-lookup"><span data-stu-id="705af-257">Australia Passport Number</span></span> 
- <span data-ttu-id="705af-258">Numéro de dossier fiscal Australie</span><span class="sxs-lookup"><span data-stu-id="705af-258">Australia Tax File Number</span></span> 
- <span data-ttu-id="705af-259">Numéro d’entreprise australien</span><span class="sxs-lookup"><span data-stu-id="705af-259">Australian Business Number</span></span> 
- <span data-ttu-id="705af-260">Numéro de société australien</span><span class="sxs-lookup"><span data-stu-id="705af-260">Australian Company Number</span></span> 
- <span data-ttu-id="705af-261">Numéro de permis de conduire Autriche</span><span class="sxs-lookup"><span data-stu-id="705af-261">Austria Driver's License Number</span></span> 
- <span data-ttu-id="705af-262">Carte d’identité Autriche</span><span class="sxs-lookup"><span data-stu-id="705af-262">Austria Identity Card</span></span> 
- <span data-ttu-id="705af-263">Numéro de passeport Autriche</span><span class="sxs-lookup"><span data-stu-id="705af-263">Austria Passport Number</span></span> 
- <span data-ttu-id="705af-264">Numéro de sécurité sociale d’Autriche</span><span class="sxs-lookup"><span data-stu-id="705af-264">Austria Social Security Number</span></span> 
- <span data-ttu-id="705af-265">Numéro d’identification fiscale autrichen</span><span class="sxs-lookup"><span data-stu-id="705af-265">Austria Tax Identification Number</span></span> 
- <span data-ttu-id="705af-266">Numéro de TVA (Austria Value Added Tax)</span><span class="sxs-lookup"><span data-stu-id="705af-266">Austria Value Added Tax (VAT) Number</span></span> 
- <span data-ttu-id="705af-267">Clé d’th Azure DocumentDB</span><span class="sxs-lookup"><span data-stu-id="705af-267">Azure DocumentDB Auth Key</span></span> 
- <span data-ttu-id="705af-268">Chaîne de connexion de base de données IAAS Azure et chaîne SQL connexion Azure</span><span class="sxs-lookup"><span data-stu-id="705af-268">Azure IAAS Database Connection String and Azure SQL Connection String</span></span> 
- <span data-ttu-id="705af-269">Chaîne de connexion Azure IoT</span><span class="sxs-lookup"><span data-stu-id="705af-269">Azure IoT Connection String</span></span> 
- <span data-ttu-id="705af-270">Mot de passe de paramètre de publication Azure</span><span class="sxs-lookup"><span data-stu-id="705af-270">Azure Publish Setting Password</span></span> 
- <span data-ttu-id="705af-271">Chaîne de connexion du cache Azure Redis</span><span class="sxs-lookup"><span data-stu-id="705af-271">Azure Redis Cache Connection String</span></span> 
- <span data-ttu-id="705af-272">Azure SAS</span><span class="sxs-lookup"><span data-stu-id="705af-272">Azure SAS</span></span> 
- <span data-ttu-id="705af-273">Chaîne de connexion Azure Service Bus</span><span class="sxs-lookup"><span data-stu-id="705af-273">Azure Service Bus Connection String</span></span> 
- <span data-ttu-id="705af-274">Clé de compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="705af-274">Azure Storage Account Key</span></span> 
- <span data-ttu-id="705af-275">Clé de compte de stockage Azure (générique)</span><span class="sxs-lookup"><span data-stu-id="705af-275">Azure Storage Account Key (Generic)</span></span> 
- <span data-ttu-id="705af-276">Numéro de permis de conduire belgique</span><span class="sxs-lookup"><span data-stu-id="705af-276">Belgium Driver's License Number</span></span> 
- <span data-ttu-id="705af-277">Numéro national belge</span><span class="sxs-lookup"><span data-stu-id="705af-277">Belgium National Number</span></span> 
- <span data-ttu-id="705af-278">Numéro de passeport belgique</span><span class="sxs-lookup"><span data-stu-id="705af-278">Belgium Passport Number</span></span> 
- <span data-ttu-id="705af-279">Numéro de taxe sur la valeur ajoutée en Belgique</span><span class="sxs-lookup"><span data-stu-id="705af-279">Belgium Value Added Tax Number</span></span> 
- <span data-ttu-id="705af-280">Numéro CPF Brésil</span><span class="sxs-lookup"><span data-stu-id="705af-280">Brazil CPF Number</span></span> 
- <span data-ttu-id="705af-281">Numéro d’entité juridique (CNPJ) Brésil</span><span class="sxs-lookup"><span data-stu-id="705af-281">Brazil Legal Entity Number (CNPJ)</span></span> 
- <span data-ttu-id="705af-282">	Brazil National ID Card (RG)</span><span class="sxs-lookup"><span data-stu-id="705af-282">Brazil National ID Card (RG)</span></span> 
- <span data-ttu-id="705af-283">Numéro de permis de conduire bulgare</span><span class="sxs-lookup"><span data-stu-id="705af-283">Bulgaria Driver's License Number</span></span> 
- <span data-ttu-id="705af-284">Numéro de passeport bulgare</span><span class="sxs-lookup"><span data-stu-id="705af-284">Bulgaria Passport Number</span></span> 
- <span data-ttu-id="705af-285">Numéro civile uniforme de Bulgarie</span><span class="sxs-lookup"><span data-stu-id="705af-285">Bulgaria Uniform Civil Number</span></span> 
- <span data-ttu-id="705af-286">Numéro de compte bancaire Canada</span><span class="sxs-lookup"><span data-stu-id="705af-286">Canada Bank Account Number</span></span> 
- <span data-ttu-id="705af-287">Numéro de permis de conduire Canada</span><span class="sxs-lookup"><span data-stu-id="705af-287">Canada Driver's License Number</span></span> 
- <span data-ttu-id="705af-288">Numéro de service de santé Canada</span><span class="sxs-lookup"><span data-stu-id="705af-288">Canada Health Service Number</span></span> 
- <span data-ttu-id="705af-289">Numéro de passeport Canada</span><span class="sxs-lookup"><span data-stu-id="705af-289">Canada Passport Number</span></span> 
- <span data-ttu-id="705af-290">NIMP (numéro d’identification médicale personnel) Canada</span><span class="sxs-lookup"><span data-stu-id="705af-290">Canada Personal Health Identification Number (PHIN)</span></span> 
- <span data-ttu-id="705af-291">Numéro d'assurance sociale Canada</span><span class="sxs-lookup"><span data-stu-id="705af-291">Canada Social Insurance Number</span></span> 
- <span data-ttu-id="705af-292">	Numéro de carte d’identité Chili</span><span class="sxs-lookup"><span data-stu-id="705af-292">Chile Identity Card Number</span></span> 
- <span data-ttu-id="705af-293">	Numéro de carte d’identité de résident Chine (RPC)</span><span class="sxs-lookup"><span data-stu-id="705af-293">China Resident Identity Card (PRC) Number</span></span> 
- <span data-ttu-id="705af-294">Numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="705af-294">Credit Card Number</span></span> 
- <span data-ttu-id="705af-295">Numéro de permis de conduire Croate</span><span class="sxs-lookup"><span data-stu-id="705af-295">Croatia Driver's License Number</span></span> 
- <span data-ttu-id="705af-296">Numéro de carte d’identité croate</span><span class="sxs-lookup"><span data-stu-id="705af-296">Croatia Identity Card Number</span></span> 
- <span data-ttu-id="705af-297">Numéro de carte d’identité nationale croate</span><span class="sxs-lookup"><span data-stu-id="705af-297">Croatia National ID Card Number</span></span> 
- <span data-ttu-id="705af-298">Numéro de passeport croate</span><span class="sxs-lookup"><span data-stu-id="705af-298">Croatia Passport Number</span></span> 
- <span data-ttu-id="705af-299">Numéro d’identification personnelle croate (OIB)</span><span class="sxs-lookup"><span data-stu-id="705af-299">Croatia Personal Identification (OIB) Number</span></span> 
- <span data-ttu-id="705af-300">CSCAN-AZURE0060 Azure Storage Account Shared Access Signature</span><span class="sxs-lookup"><span data-stu-id="705af-300">CSCAN-AZURE0060 Azure Storage Account Shared Access Signature</span></span> 
- <span data-ttu-id="705af-301">Clé symétrique générale CSCAN-GENERAL0140</span><span class="sxs-lookup"><span data-stu-id="705af-301">CSCAN-GENERAL0140 General Symmetric Key</span></span> 
- <span data-ttu-id="705af-302">Numéro de permis de conduire de Chypre</span><span class="sxs-lookup"><span data-stu-id="705af-302">Cyprus Driver's License Number</span></span> 
- <span data-ttu-id="705af-303">Carte d’identité Chypre</span><span class="sxs-lookup"><span data-stu-id="705af-303">Cyprus Identity Card</span></span> 
- <span data-ttu-id="705af-304">Numéro de passeport de Chypre</span><span class="sxs-lookup"><span data-stu-id="705af-304">Cyprus Passport Number</span></span> 
- <span data-ttu-id="705af-305">Numéro d’identification fiscale à Chypre</span><span class="sxs-lookup"><span data-stu-id="705af-305">Cyprus Tax Identification Number</span></span> 
- <span data-ttu-id="705af-306">Numéro de permis de conduire tchèque</span><span class="sxs-lookup"><span data-stu-id="705af-306">Czech Driver's License Number</span></span> 
- <span data-ttu-id="705af-307">Numéro d’identité personnel tchèque</span><span class="sxs-lookup"><span data-stu-id="705af-307">Czech Personal Identity Number</span></span> 
- <span data-ttu-id="705af-308">Numéro de passeport de la République tchèque</span><span class="sxs-lookup"><span data-stu-id="705af-308">Czech Republic Passport Number</span></span> 
- <span data-ttu-id="705af-309">Numéro de permis de conduire danemark</span><span class="sxs-lookup"><span data-stu-id="705af-309">Denmark Driver's License Number</span></span> 
- <span data-ttu-id="705af-310">Numéro de passeport danemark</span><span class="sxs-lookup"><span data-stu-id="705af-310">Denmark Passport Number</span></span> 
- <span data-ttu-id="705af-311">Numéro d’identification personnelle danois</span><span class="sxs-lookup"><span data-stu-id="705af-311">Denmark Personal Identification Number</span></span> 
- <span data-ttu-id="705af-312">Numéro de la Drug Enforcement Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="705af-312">Drug Enforcement Agency (DEA) Number</span></span> 
- <span data-ttu-id="705af-313">Numéro de permis de conduire Estonie</span><span class="sxs-lookup"><span data-stu-id="705af-313">Estonia Driver's License Number</span></span> 
- <span data-ttu-id="705af-314">Numéro de passeport estonien</span><span class="sxs-lookup"><span data-stu-id="705af-314">Estonia Passport Number</span></span> 
- <span data-ttu-id="705af-315">Code d’identification personnelle estonien</span><span class="sxs-lookup"><span data-stu-id="705af-315">Estonia Personal Identification Code</span></span> 
- <span data-ttu-id="705af-316">Numéro de carte de crédit de l'U.E.</span><span class="sxs-lookup"><span data-stu-id="705af-316">EU Debit Card Number</span></span> 
- <span data-ttu-id="705af-317">Numéro de permis de conduire de l’UE</span><span class="sxs-lookup"><span data-stu-id="705af-317">EU Driver's License Number</span></span> 
- <span data-ttu-id="705af-318">Numéro d’identification national de l’UE</span><span class="sxs-lookup"><span data-stu-id="705af-318">EU National Identification Number</span></span> 
- <span data-ttu-id="705af-319">Numéro de passeport de l’UE</span><span class="sxs-lookup"><span data-stu-id="705af-319">EU Passport Number</span></span> 
- <span data-ttu-id="705af-320">Numéro de sécurité sociale de l’UE (SSN) ou ID équivalent</span><span class="sxs-lookup"><span data-stu-id="705af-320">EU Social Security Number (SSN) or Equivalent ID</span></span> 
- <span data-ttu-id="705af-321">Numéro d’identification fiscale de l’UE (TIN)</span><span class="sxs-lookup"><span data-stu-id="705af-321">EU Tax Identification Number (TIN)</span></span> 
- <span data-ttu-id="705af-322">Numéro de permis de conduire Finlande</span><span class="sxs-lookup"><span data-stu-id="705af-322">Finland Driver's License Number</span></span> 
- <span data-ttu-id="705af-323">Numéro d’assurance santé européen (Finlande)</span><span class="sxs-lookup"><span data-stu-id="705af-323">Finland European Health Insurance Number</span></span> 
- <span data-ttu-id="705af-324">Numéro d'identification national finlandais</span><span class="sxs-lookup"><span data-stu-id="705af-324">Finland National ID</span></span> 
- <span data-ttu-id="705af-325">Numéro de passeport finlandais</span><span class="sxs-lookup"><span data-stu-id="705af-325">Finland Passport Number</span></span> 
- <span data-ttu-id="705af-326">Numéro de permis de conduire français</span><span class="sxs-lookup"><span data-stu-id="705af-326">France Driver's License Number</span></span> 
- <span data-ttu-id="705af-327">Numéro d’assurance maladie Français</span><span class="sxs-lookup"><span data-stu-id="705af-327">France Health Insurance Number</span></span> 
- <span data-ttu-id="705af-328">Carte nationale d'identité (CNI) française</span><span class="sxs-lookup"><span data-stu-id="705af-328">France National ID Card (CNI)</span></span> 
- <span data-ttu-id="705af-329">Numéro de passeport français</span><span class="sxs-lookup"><span data-stu-id="705af-329">France Passport Number</span></span> 
- <span data-ttu-id="705af-330">Numéro de sécurité sociale (INSEE) français</span><span class="sxs-lookup"><span data-stu-id="705af-330">France Social Security Number (INSEE)</span></span> 
- <span data-ttu-id="705af-331">Numéro d’identification fiscale français (numéro SPI.)</span><span class="sxs-lookup"><span data-stu-id="705af-331">France Tax Identification Number (numéro SPI.)</span></span> 
- <span data-ttu-id="705af-332">Numéro de taxe sur la valeur ajoutée en France</span><span class="sxs-lookup"><span data-stu-id="705af-332">France Value Added Tax Number</span></span> 
- <span data-ttu-id="705af-333">Numéro de permis de conduire allemand</span><span class="sxs-lookup"><span data-stu-id="705af-333">German Driver's License Number</span></span> 
- <span data-ttu-id="705af-334">Numéro de passeport allemand</span><span class="sxs-lookup"><span data-stu-id="705af-334">German Passport Number</span></span> 
- <span data-ttu-id="705af-335">Numéro de carte d’identité allemand</span><span class="sxs-lookup"><span data-stu-id="705af-335">Germany Identity Card Number</span></span> 
- <span data-ttu-id="705af-336">Numéro d’identification fiscale allemand</span><span class="sxs-lookup"><span data-stu-id="705af-336">Germany Tax Identification Number</span></span> 
- <span data-ttu-id="705af-337">Numéro de taxe sur la valeur ajoutée en Allemagne</span><span class="sxs-lookup"><span data-stu-id="705af-337">Germany Value Added Tax Number</span></span> 
- <span data-ttu-id="705af-338">Numéro de permis de conduire Grec</span><span class="sxs-lookup"><span data-stu-id="705af-338">Greece Driver's License Number</span></span> 
- <span data-ttu-id="705af-339">Carte d’identité nationale grecque</span><span class="sxs-lookup"><span data-stu-id="705af-339">Greece National ID Card</span></span> 
- <span data-ttu-id="705af-340">Numéro de passeport Grec</span><span class="sxs-lookup"><span data-stu-id="705af-340">Greece Passport Number</span></span> 
- <span data-ttu-id="705af-341">Numéro de sécurité sociale grec (AMKA)</span><span class="sxs-lookup"><span data-stu-id="705af-341">Greece Social Security Number (AMKA)</span></span> 
- <span data-ttu-id="705af-342">Numéro d’identification fiscale grec</span><span class="sxs-lookup"><span data-stu-id="705af-342">Greek Tax identification Number</span></span> 
- <span data-ttu-id="705af-343">Numéro de carte d’identité (HKID) Hong Kong</span><span class="sxs-lookup"><span data-stu-id="705af-343">Hong Kong Identity Card (HKID) Number</span></span> 
- <span data-ttu-id="705af-344">Numéro de sécurité sociale hongrois (TAJ)</span><span class="sxs-lookup"><span data-stu-id="705af-344">Hungarian Social Security Number (TAJ)</span></span> 
- <span data-ttu-id="705af-345">Numéro de taxe sur la valeur ajoutée hongrois</span><span class="sxs-lookup"><span data-stu-id="705af-345">Hungarian Value Added Tax Number</span></span> 
- <span data-ttu-id="705af-346">Numéro de permis de conduire hongrois</span><span class="sxs-lookup"><span data-stu-id="705af-346">Hungary Driver's License Number</span></span> 
- <span data-ttu-id="705af-347">Numéro de passeport hongrois</span><span class="sxs-lookup"><span data-stu-id="705af-347">Hungary Passport Number</span></span> 
- <span data-ttu-id="705af-348">Numéro d’identification personnel hongrie</span><span class="sxs-lookup"><span data-stu-id="705af-348">Hungary Personal Identification Number</span></span> 
- <span data-ttu-id="705af-349">Numéro d’identification fiscale hongrie</span><span class="sxs-lookup"><span data-stu-id="705af-349">Hungary Tax identification Number</span></span> 
- <span data-ttu-id="705af-350">Numéro de compte permanent Inde</span><span class="sxs-lookup"><span data-stu-id="705af-350">India Permanent Account Number (PAN)</span></span> 
- <span data-ttu-id="705af-351">Numéro d’identification unique (Aadhaar) Inde</span><span class="sxs-lookup"><span data-stu-id="705af-351">India Unique Identification (Aadhaar) Number</span></span> 
- <span data-ttu-id="705af-352">Numéro de carte d’identité (KTP) Indonésie</span><span class="sxs-lookup"><span data-stu-id="705af-352">Indonesia Identity Card (KTP) Number</span></span> 
- <span data-ttu-id="705af-353">Numéro de compte international (IBAN)</span><span class="sxs-lookup"><span data-stu-id="705af-353">International Banking Account Number (IBAN)</span></span> 
- <span data-ttu-id="705af-354">Classification internationale des maladie (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="705af-354">International Classification of Diseases (ICD-10-CM)</span></span> 
- <span data-ttu-id="705af-355">Classification internationale des maladie (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="705af-355">International Classification of Diseases (ICD-9-CM)</span></span> 
- <span data-ttu-id="705af-356">Adresse IP</span><span class="sxs-lookup"><span data-stu-id="705af-356">IP Address</span></span> 
- <span data-ttu-id="705af-357">Numéro de permis de conduire Irlande</span><span class="sxs-lookup"><span data-stu-id="705af-357">Ireland Driver's License Number</span></span> 
- <span data-ttu-id="705af-358">Numéro de passeport irlande</span><span class="sxs-lookup"><span data-stu-id="705af-358">Ireland Passport Number</span></span> 
- <span data-ttu-id="705af-359">Numéro personnel pour le service public irlandais (PPS)</span><span class="sxs-lookup"><span data-stu-id="705af-359">Ireland Personal Public Service (PPS) Number</span></span> 
- <span data-ttu-id="705af-360">Numéro de compte bancaire Israël</span><span class="sxs-lookup"><span data-stu-id="705af-360">Israel Bank Account Number</span></span> 
- <span data-ttu-id="705af-361">Carte nationale d’identité Israël</span><span class="sxs-lookup"><span data-stu-id="705af-361">Israel National ID</span></span> 
- <span data-ttu-id="705af-362">Numéro de permis de conduire Italie</span><span class="sxs-lookup"><span data-stu-id="705af-362">Italy Driver's License Number</span></span> 
- <span data-ttu-id="705af-363">Code fiscal italien</span><span class="sxs-lookup"><span data-stu-id="705af-363">Italy Fiscal Code</span></span> 
- <span data-ttu-id="705af-364">Numéro de passeport Italie</span><span class="sxs-lookup"><span data-stu-id="705af-364">Italy Passport Number</span></span> 
- <span data-ttu-id="705af-365">Numéro de taxe sur la valeur ajoutée italie</span><span class="sxs-lookup"><span data-stu-id="705af-365">Italy Value Added Tax Number</span></span> 
- <span data-ttu-id="705af-366">Numéro de compte bancaire Japon</span><span class="sxs-lookup"><span data-stu-id="705af-366">Japan Bank Account Number</span></span> 
- <span data-ttu-id="705af-367">Numéro de permis de conduire Japon</span><span class="sxs-lookup"><span data-stu-id="705af-367">Japan Driver's License Number</span></span> 
- <span data-ttu-id="705af-368">Numéro de passeport Japon</span><span class="sxs-lookup"><span data-stu-id="705af-368">Japan Passport Number</span></span> 
- <span data-ttu-id="705af-369">Matricule de résident Japon</span><span class="sxs-lookup"><span data-stu-id="705af-369">Japan Resident Registration Number</span></span> 
- <span data-ttu-id="705af-370">Numéro d’assurance sociale Japon</span><span class="sxs-lookup"><span data-stu-id="705af-370">Japan Social Insurance Number (SIN)</span></span> 
- <span data-ttu-id="705af-371">Japonais Mon numéro d’entreprise</span><span class="sxs-lookup"><span data-stu-id="705af-371">Japanese My Number Corporate</span></span> 
- <span data-ttu-id="705af-372">Japonais Mon numéro personnel</span><span class="sxs-lookup"><span data-stu-id="705af-372">Japanese My Number Personal</span></span> 
- <span data-ttu-id="705af-373">Numéro de carte de résidence (japonais)</span><span class="sxs-lookup"><span data-stu-id="705af-373">Japanese Residence Card Number</span></span> 
- <span data-ttu-id="705af-374">Numéro de permis de conduire letton</span><span class="sxs-lookup"><span data-stu-id="705af-374">Latvia Driver's License Number</span></span> 
- <span data-ttu-id="705af-375">Numéro de passeport letton</span><span class="sxs-lookup"><span data-stu-id="705af-375">Latvia Passport Number</span></span> 
- <span data-ttu-id="705af-376">Code personnel letton</span><span class="sxs-lookup"><span data-stu-id="705af-376">Latvia Personal Code</span></span> 
- <span data-ttu-id="705af-377">Numéro de permis de conduire lituanien</span><span class="sxs-lookup"><span data-stu-id="705af-377">Lithuania Driver's License Number</span></span> 
- <span data-ttu-id="705af-378">Numéro de passeport lituanien</span><span class="sxs-lookup"><span data-stu-id="705af-378">Lithuania Passport Number</span></span> 
- <span data-ttu-id="705af-379">Code personnel lituanien</span><span class="sxs-lookup"><span data-stu-id="705af-379">Lithuania Personal Code</span></span> 
- <span data-ttu-id="705af-380">Numéro de permis de conduire De Qu’est-ce que vous avez ?</span><span class="sxs-lookup"><span data-stu-id="705af-380">Luxemburg Driver's License Number</span></span> 
- <span data-ttu-id="705af-381">Numéro d’identification national (personnes physiques)</span><span class="sxs-lookup"><span data-stu-id="705af-381">Luxemburg National Identification Number (Natural persons)</span></span> 
- <span data-ttu-id="705af-382">Numéro d’identification national (personnes non physiques)</span><span class="sxs-lookup"><span data-stu-id="705af-382">Luxemburg National Identification Number (Non-natural persons)</span></span> 
- <span data-ttu-id="705af-383">Numéro de passeport de Contrôle</span><span class="sxs-lookup"><span data-stu-id="705af-383">Luxemburg Passport Number</span></span> 
- <span data-ttu-id="705af-384">Numéro de carte d’identité Malaisie</span><span class="sxs-lookup"><span data-stu-id="705af-384">Malaysia Identity Card Number</span></span> 
- <span data-ttu-id="705af-385">Numéro de permis de conduire de Malte</span><span class="sxs-lookup"><span data-stu-id="705af-385">Malta Driver's License Number</span></span> 
- <span data-ttu-id="705af-386">Numéro de carte d’identité Malte</span><span class="sxs-lookup"><span data-stu-id="705af-386">Malta Identity Card Number</span></span> 
- <span data-ttu-id="705af-387">Numéro de passeport de Malte</span><span class="sxs-lookup"><span data-stu-id="705af-387">Malta Passport Number</span></span> 
- <span data-ttu-id="705af-388">Numéro d’ID fiscal de Malte</span><span class="sxs-lookup"><span data-stu-id="705af-388">Malta Tax ID Number</span></span> 
- <span data-ttu-id="705af-389">Numéro de service du citoyen (BSN) néerlandais</span><span class="sxs-lookup"><span data-stu-id="705af-389">Netherlands Citizen's Service (BSN) Number</span></span> 
- <span data-ttu-id="705af-390">Numéro de permis de conduire néerlandais</span><span class="sxs-lookup"><span data-stu-id="705af-390">Netherlands Driver's License Number</span></span> 
- <span data-ttu-id="705af-391">Numéro de passeport néerlandais</span><span class="sxs-lookup"><span data-stu-id="705af-391">Netherlands Passport Number</span></span> 
- <span data-ttu-id="705af-392">Numéro d’identification fiscale pays-Bas</span><span class="sxs-lookup"><span data-stu-id="705af-392">Netherlands Tax Identification Number</span></span> 
- <span data-ttu-id="705af-393">Numéro de taxe sur la valeur ajoutée des Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="705af-393">Netherlands Value Added Tax Number</span></span> 
- <span data-ttu-id="705af-394">Numéro de compte bancaire nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="705af-394">New Zealand bank account number</span></span> 
- <span data-ttu-id="705af-395">Numéro de permis de conduire nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="705af-395">New Zealand Driver License Number</span></span> 
- <span data-ttu-id="705af-396">Numéro de revenu pour les Pays-Bas (Nouvelle-Zélande)</span><span class="sxs-lookup"><span data-stu-id="705af-396">New Zealand Inland Revenue number</span></span> 
- <span data-ttu-id="705af-397">Numéro du Ministère de la santé Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="705af-397">New Zealand Ministry of Health Number</span></span> 
- <span data-ttu-id="705af-398">Numéro de réseau social de La Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="705af-398">New Zealand Social Welfare Number</span></span> 
- <span data-ttu-id="705af-399">Numéro d’identité norvégien</span><span class="sxs-lookup"><span data-stu-id="705af-399">Norway Identity Number</span></span> 
- <span data-ttu-id="705af-400">Numéro d’identification multifonction unifié Philippines</span><span class="sxs-lookup"><span data-stu-id="705af-400">Philippines Unified Multi-Purpose ID Number</span></span> 
- <span data-ttu-id="705af-401">Numéro de permis de conduire polonais</span><span class="sxs-lookup"><span data-stu-id="705af-401">Poland Driver's License Number</span></span> 
- <span data-ttu-id="705af-402">Carte d'identité polonaise</span><span class="sxs-lookup"><span data-stu-id="705af-402">Poland Identity Card</span></span> 
- <span data-ttu-id="705af-403">Numéro d'identification national polonais (PESEL)</span><span class="sxs-lookup"><span data-stu-id="705af-403">Poland National ID (PESEL)</span></span> 
- <span data-ttu-id="705af-404">Numéro de passeport polonais</span><span class="sxs-lookup"><span data-stu-id="705af-404">Poland Passport</span></span> 
- <span data-ttu-id="705af-405">Numéro d’identification fiscale polonais</span><span class="sxs-lookup"><span data-stu-id="705af-405">Poland Tax Identification Number</span></span> 
- <span data-ttu-id="705af-406">Numéro POLONAIS REGON</span><span class="sxs-lookup"><span data-stu-id="705af-406">Polish REGON Number</span></span> 
- <span data-ttu-id="705af-407">Numéro de carte de citoyen portugais</span><span class="sxs-lookup"><span data-stu-id="705af-407">Portugal Citizen Card Number</span></span> 
- <span data-ttu-id="705af-408">Numéro de permis de conduire Portugal</span><span class="sxs-lookup"><span data-stu-id="705af-408">Portugal Driver's License Number</span></span> 
- <span data-ttu-id="705af-409">Numéro de passeport portugais</span><span class="sxs-lookup"><span data-stu-id="705af-409">Portugal Passport Number</span></span> 
- <span data-ttu-id="705af-410">Numéro d’identification fiscale portugais</span><span class="sxs-lookup"><span data-stu-id="705af-410">Portugal Tax Identification Number</span></span> 
- <span data-ttu-id="705af-411">Numéro de permis de conduire roumain</span><span class="sxs-lookup"><span data-stu-id="705af-411">Romania Driver's License Number</span></span> 
- <span data-ttu-id="705af-412">Numéro de passeport roumain</span><span class="sxs-lookup"><span data-stu-id="705af-412">Romania Passport Number</span></span> 
- <span data-ttu-id="705af-413">Code numérique personnel (CNP) roumain</span><span class="sxs-lookup"><span data-stu-id="705af-413">Romania Personal Numerical Code (CNP)</span></span> 
- <span data-ttu-id="705af-414">Numéro de passeport russe (national)</span><span class="sxs-lookup"><span data-stu-id="705af-414">Russian Passport Number (Domestic)</span></span> 
- <span data-ttu-id="705af-415">Numéro de passeport russe (international)</span><span class="sxs-lookup"><span data-stu-id="705af-415">Russian Passport Number (International)</span></span> 
- <span data-ttu-id="705af-416">ID national Arabie saoudite</span><span class="sxs-lookup"><span data-stu-id="705af-416">Saudi Arabia National ID</span></span> 
- <span data-ttu-id="705af-417">Numéro de carte d’identité d’enregistrement national (NRIC) Singapour</span><span class="sxs-lookup"><span data-stu-id="705af-417">Singapore National Registration Identity Card (NRIC) Number</span></span> 
- <span data-ttu-id="705af-418">Numéro de permis de conduire slovaque</span><span class="sxs-lookup"><span data-stu-id="705af-418">Slovakia Driver's License Number</span></span> 
- <span data-ttu-id="705af-419">Numéro de passeport slovaque</span><span class="sxs-lookup"><span data-stu-id="705af-419">Slovakia Passport Number</span></span> 
- <span data-ttu-id="705af-420">Numéro personnel slovaque</span><span class="sxs-lookup"><span data-stu-id="705af-420">Slovakia Personal Number</span></span> 
- <span data-ttu-id="705af-421">Numéro de permis de conduire slovène</span><span class="sxs-lookup"><span data-stu-id="705af-421">Slovenia Driver's License Number</span></span> 
- <span data-ttu-id="705af-422">Numéro de passeport slovène</span><span class="sxs-lookup"><span data-stu-id="705af-422">Slovenia Passport Number</span></span> 
- <span data-ttu-id="705af-423">Numéro d’identification fiscale slovénien</span><span class="sxs-lookup"><span data-stu-id="705af-423">Slovenia Tax Identification Number</span></span> 
- <span data-ttu-id="705af-424">Numéro de citoyen maître unique de Slovénie</span><span class="sxs-lookup"><span data-stu-id="705af-424">Slovenia Unique Master Citizen Number</span></span> 
- <span data-ttu-id="705af-425">Numéro d’identification Afrique du Sud</span><span class="sxs-lookup"><span data-stu-id="705af-425">South Africa Identification Number</span></span> 
- <span data-ttu-id="705af-426">Matricule de résident Corée du Sud</span><span class="sxs-lookup"><span data-stu-id="705af-426">South Korea Resident Registration Number</span></span> 
- <span data-ttu-id="705af-427">DNI (Espagne)</span><span class="sxs-lookup"><span data-stu-id="705af-427">Spain DNI</span></span> 
- <span data-ttu-id="705af-428">Numéro de permis de conduire Espagnol</span><span class="sxs-lookup"><span data-stu-id="705af-428">Spain Driver's License Number</span></span> 
- <span data-ttu-id="705af-429">Numéro de passeport Espagnol</span><span class="sxs-lookup"><span data-stu-id="705af-429">Spain Passport Number</span></span> 
- <span data-ttu-id="705af-430">Numéro de sécurité sociale (N° S.S.) espagnol</span><span class="sxs-lookup"><span data-stu-id="705af-430">Spain Social Security Number (SSN)</span></span> 
- <span data-ttu-id="705af-431">Numéro d’identification fiscale Espagnol</span><span class="sxs-lookup"><span data-stu-id="705af-431">Spain Tax Identification Number</span></span> 
- <span data-ttu-id="705af-432">SQL Server Connection String</span><span class="sxs-lookup"><span data-stu-id="705af-432">SQL Server Connection String</span></span> 
- <span data-ttu-id="705af-433">Numéro de permis de conduire suédois</span><span class="sxs-lookup"><span data-stu-id="705af-433">Sweden Driver's License Number</span></span> 
- <span data-ttu-id="705af-434">ID national suédois</span><span class="sxs-lookup"><span data-stu-id="705af-434">Sweden National ID</span></span> 
- <span data-ttu-id="705af-435">Numéro de passeport suédois</span><span class="sxs-lookup"><span data-stu-id="705af-435">Sweden Passport Number</span></span> 
- <span data-ttu-id="705af-436">Numéro d’identification fiscale suédois</span><span class="sxs-lookup"><span data-stu-id="705af-436">Sweden Tax Identification Number</span></span> 
- <span data-ttu-id="705af-437">Code SWIFT</span><span class="sxs-lookup"><span data-stu-id="705af-437">SWIFT Code</span></span> 
- <span data-ttu-id="705af-438">Numéro de sécurité sociale suisse AHV</span><span class="sxs-lookup"><span data-stu-id="705af-438">Swiss Social Security Number AHV</span></span> 
- <span data-ttu-id="705af-439">ID national à Taïwan</span><span class="sxs-lookup"><span data-stu-id="705af-439">Taiwan National ID</span></span> 
- <span data-ttu-id="705af-440">	Numéro de passeport Taïwan</span><span class="sxs-lookup"><span data-stu-id="705af-440">Taiwan Passport Number</span></span> 
- <span data-ttu-id="705af-441">Certificat de résident Taïwan (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="705af-441">Taiwan Resident Certificate (ARC/TARC)</span></span> 
- <span data-ttu-id="705af-442">Code d’identification de la population thaï</span><span class="sxs-lookup"><span data-stu-id="705af-442">Thai Population Identification Code</span></span> 
- <span data-ttu-id="705af-443">Numéro d’identification nationale turc</span><span class="sxs-lookup"><span data-stu-id="705af-443">Turkish National Identification number</span></span> 
- <span data-ttu-id="705af-p108">Numéro de permis de conduire du Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="705af-p108">U.K. Driver's License Number</span></span> 
- <span data-ttu-id="705af-p109">Numéro de liste électorale du Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="705af-p109">U.K. Electoral Roll Number</span></span> 
- <span data-ttu-id="705af-p110">Numéro du service de santé national (NHS) du Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="705af-p110">U.K. National Health Service Number</span></span> 
- <span data-ttu-id="705af-p111">Numéro d'assurance national (NINO) du Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="705af-p111">U.K. National Insurance Number (NINO)</span></span> 
- <span data-ttu-id="705af-452">Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="705af-452">U.K.</span></span> <span data-ttu-id="705af-453">Numéro de référence du contribuable unique</span><span class="sxs-lookup"><span data-stu-id="705af-453">Unique Taxpayer Reference Number</span></span> 
- <span data-ttu-id="705af-454">États-Unis/Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="705af-454">U.S. / U.K.</span></span> <span data-ttu-id="705af-455">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="705af-455">Passport Number</span></span> 
- <span data-ttu-id="705af-456">Numéro de compte bancaire États-Unis</span><span class="sxs-lookup"><span data-stu-id="705af-456">U.S. Bank Account Number</span></span> 
- <span data-ttu-id="705af-457">Numéro de permis de conduire États-Unis</span><span class="sxs-lookup"><span data-stu-id="705af-457">U.S. Driver's License Number</span></span> 
- <span data-ttu-id="705af-458">Numéro d’identification fiscale individuel (ITIN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="705af-458">U.S. Individual Taxpayer Identification Number (ITIN)</span></span> 
- <span data-ttu-id="705af-459">Numéro de sécurité sociale (SSN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="705af-459">U.S. Social Security Number (SSN)</span></span> 
- <span data-ttu-id="705af-460">Numéro de passeport Ukrainien (national)</span><span class="sxs-lookup"><span data-stu-id="705af-460">Ukraine Passport Number (Domestic)</span></span> 
- <span data-ttu-id="705af-461">Numéro de passeport ukrainien (international)</span><span class="sxs-lookup"><span data-stu-id="705af-461">Ukraine Passport Number (International)</span></span> 
 
<span data-ttu-id="705af-462">Notez que des types d'informations sensibles personnalisés seront également détectés en plus des types d'informations sensibles pré-personnalisés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="705af-462">Please note that custom sensitive information types will also be detected in addition to the above out-of-the-box sensitive information types</span></span>

## <a name="support-matrix-for-dlp-policy-tips-across-microsoft-apps"></a><span data-ttu-id="705af-463">Matrice de prise en charge des conseils de stratégie DLP dans les applications Microsoft</span><span class="sxs-lookup"><span data-stu-id="705af-463">Support Matrix for DLP policy tips across Microsoft apps</span></span>

|<span data-ttu-id="705af-464">**Application et plateforme**</span><span class="sxs-lookup"><span data-stu-id="705af-464">**App and platform**</span></span>|<span data-ttu-id="705af-465">**Prise en charge des conseils de stratégie DLP**</span><span class="sxs-lookup"><span data-stu-id="705af-465">**DLP policy tip support**</span></span>|<span data-ttu-id="705af-466">**Types d'informations sensibles pris en charge**</span><span class="sxs-lookup"><span data-stu-id="705af-466">**Sensitive information types supported**</span></span>|<span data-ttu-id="705af-467">**Prédicats et actions pris en charge**</span><span class="sxs-lookup"><span data-stu-id="705af-467">**Predicates and actions supported**</span></span>|<span data-ttu-id="705af-468">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="705af-468">**Comments**</span></span>|
|:--|:--|:--|:--|:--|
|<span data-ttu-id="705af-469">**Outlook Web Access**</span><span class="sxs-lookup"><span data-stu-id="705af-469">**Outlook Web Access**</span></span>|:::image type="icon" source="../media/rightmrk.png" border="false":::|<span data-ttu-id="705af-470">Tous</span><span class="sxs-lookup"><span data-stu-id="705af-470">All</span></span>|<span data-ttu-id="705af-471">Subset</span><span class="sxs-lookup"><span data-stu-id="705af-471">Subset</span></span>|<span data-ttu-id="705af-472">Voir la [référence des conseils de stratégie de protection contre la perte de données](#data-loss-prevention-policy-tips-reference)</span><span class="sxs-lookup"><span data-stu-id="705af-472">See [Data Loss Prevention policy tips reference](#data-loss-prevention-policy-tips-reference)</span></span>|
|<span data-ttu-id="705af-473">**Outlook Win32 (Outlook 2013 et au-delà)**</span><span class="sxs-lookup"><span data-stu-id="705af-473">**Outlook Win32 (Outlook 2013 and beyond)**</span></span>|:::image type="icon" source="../media/rightmrk.png" border="false":::|<span data-ttu-id="705af-474">Subset</span><span class="sxs-lookup"><span data-stu-id="705af-474">Subset</span></span>|<span data-ttu-id="705af-475">Subset</span><span class="sxs-lookup"><span data-stu-id="705af-475">Subset</span></span>|<span data-ttu-id="705af-476">Voir outlook [2013](#outlook-2013-and-later-supports-showing-policy-tips-for-only-some-conditions-and-exceptions) et ultérieur prend en charge l'affichage de conseils de stratégie uniquement pour certaines conditions et exceptions, et [Outlook 2013](#outlook-2013-and-later-supports-showing-policy-tips-for-only-some-sensitive-information-types) et ultérieur prend en charge l'affichage de conseils de stratégie pour certains types d'informations sensibles uniquement pour plus d'informations sur la prise en charge des types d'informations sensibles et des conditions et actions DLP prises en charge pour afficher les conseils de stratégie DLP sur Outlook Win32.</span><span class="sxs-lookup"><span data-stu-id="705af-476">See [Outlook 2013 and later supports showing policy tips for only some conditions and exceptions](#outlook-2013-and-later-supports-showing-policy-tips-for-only-some-conditions-and-exceptions) and [Outlook 2013 and later supports showing policy tips for only some sensitive information types](#outlook-2013-and-later-supports-showing-policy-tips-for-only-some-sensitive-information-types) for details on support for sensitive information types and DLP conditions and actions supported for showing DLP policy tips on Outlook Win32.</span></span>|
|<span data-ttu-id="705af-477">**Outlook Mobile (iOS, Android)/Outlook Mac**</span><span class="sxs-lookup"><span data-stu-id="705af-477">**Outlook Mobile (iOS, Android)/Outlook Mac**</span></span>|:::image type="icon" source="../media/crsmrk.png" border="false":::|<span data-ttu-id="705af-478">Aucun</span><span class="sxs-lookup"><span data-stu-id="705af-478">None</span></span>|<span data-ttu-id="705af-479">Aucun</span><span class="sxs-lookup"><span data-stu-id="705af-479">None</span></span>|<span data-ttu-id="705af-480">Les conseils de stratégie DLP ne sont pas pris en charge sur Outlook Mobile</span><span class="sxs-lookup"><span data-stu-id="705af-480">DLP policy tips are not supported on Outlook mobile</span></span>|
|<span data-ttu-id="705af-481">**Client Web Sharepoint Online/One Drive for Business**</span><span class="sxs-lookup"><span data-stu-id="705af-481">**Sharepoint Online/One Drive for Business Web client**</span></span>|:::image type="icon" source="../media/rightmrk.png" border="false":::|<span data-ttu-id="705af-482">Tous</span><span class="sxs-lookup"><span data-stu-id="705af-482">All</span></span>|<span data-ttu-id="705af-483">Tous les prédicats et actions SPO/ODB dans DLP</span><span class="sxs-lookup"><span data-stu-id="705af-483">All SPO/ODB predicates and actions in DLP</span></span>||
|<span data-ttu-id="705af-484">**Client Win32 Sharepoint Win32/ One Drive pour les entreprises**</span><span class="sxs-lookup"><span data-stu-id="705af-484">**Sharepoint Win32/ One Drive for Business Win32 client**</span></span>|:::image type="icon" source="../media/crsmrk.png" border="false":::|<span data-ttu-id="705af-485">Aucun</span><span class="sxs-lookup"><span data-stu-id="705af-485">None</span></span>|<span data-ttu-id="705af-486">Aucun</span><span class="sxs-lookup"><span data-stu-id="705af-486">None</span></span>|<span data-ttu-id="705af-487">Les conseils de stratégie DLP ne sont pas pris en charge sur les applications clientes de bureau SharePoint ou OneDrive</span><span class="sxs-lookup"><span data-stu-id="705af-487">DLP policy tips are not supported on Sharepoint or OneDrive desktop client apps</span></span>|
|<span data-ttu-id="705af-488">**Word, Excel, Powerpoint Web Client**</span><span class="sxs-lookup"><span data-stu-id="705af-488">**Word, Excel, Powerpoint Web Client**</span></span>|:::image type="icon" source="../media/rightmrk.png" border="false":::|<span data-ttu-id="705af-489">Tous</span><span class="sxs-lookup"><span data-stu-id="705af-489">All</span></span>|<span data-ttu-id="705af-490">Tous les prédicats et actions SPO/ODB dans DLP</span><span class="sxs-lookup"><span data-stu-id="705af-490">All SPO/ODB predicates and actions in DLP</span></span>|<span data-ttu-id="705af-491">Le conseil de stratégie DLP est pris en charge si le document est hébergé sur SPO ou l'application web ODB et que la stratégie DLP est déjà estampillée.</span><span class="sxs-lookup"><span data-stu-id="705af-491">DLP policy tip is supported if the document is hosted on SPO or ODB web app and the DLP policy is already stamped.</span></span>|
|<span data-ttu-id="705af-492">**Word, Excel, Powerpoint Mobile Client**</span><span class="sxs-lookup"><span data-stu-id="705af-492">**Word, Excel, Powerpoint Mobile Client**</span></span>|:::image type="icon" source="../media/crsmrk.png" border="false":::|<span data-ttu-id="705af-493">Aucun</span><span class="sxs-lookup"><span data-stu-id="705af-493">None</span></span>|<span data-ttu-id="705af-494">Aucun</span><span class="sxs-lookup"><span data-stu-id="705af-494">None</span></span>|<span data-ttu-id="705af-495">Les conseils de stratégie DLP ne sont pas pris en charge dans les applications mobiles pour Office.</span><span class="sxs-lookup"><span data-stu-id="705af-495">DLP policy tips are not supported in mobile apps for Office.</span></span>|
|<span data-ttu-id="705af-496">**Teams Web/ Teams Desktop/ Teams Mobile/ Teams Mac**</span><span class="sxs-lookup"><span data-stu-id="705af-496">**Teams Web/ Teams Desktop/ Teams Mobile/ Teams Mac**</span></span>|:::image type="icon" source="../media/rightmrk.png" border="false":::|<span data-ttu-id="705af-497">Tous</span><span class="sxs-lookup"><span data-stu-id="705af-497">All</span></span>|<span data-ttu-id="705af-498">Tous les prédicats Teams dans la stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="705af-498">All Teams predicates in DLP policy</span></span>|<span data-ttu-id="705af-499">Les conseils de stratégie s'afficheront lorsqu'un message est marqué comme « Ce message a été marqué.</span><span class="sxs-lookup"><span data-stu-id="705af-499">Policy tips will show when a message is flagged as “This message has been flagged.</span></span> <span data-ttu-id="705af-500">Que puis-je faire ?</span><span class="sxs-lookup"><span data-stu-id="705af-500">What can I do?”</span></span> <span data-ttu-id="705af-501">Lorsque vous cliquez sur le lien, l'utilisateur peut passer en revue les types d'informations sensibles détectés et remplacer ou signaler un problème si autorisé par l'administrateur. Notez qu'aucun conseil de stratégie n'est affiché pour les fichiers.</span><span class="sxs-lookup"><span data-stu-id="705af-501">When clicking the link, the user can review the sensitive info types detected and override or report an issue if allowed by the admin. Note that no policy tips are shown for files.</span></span> <span data-ttu-id="705af-502">Lorsque le destinataire tente d'accéder au document, il se peut qu'il obtienne un accès refusé s'il n'est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="705af-502">When the recipient tries to access the document, they might get access denied if not allowed.</span></span>|
|<span data-ttu-id="705af-503">**Appareils de point de terminaison Win32**</span><span class="sxs-lookup"><span data-stu-id="705af-503">**Win32 Endpoint Devices**</span></span>|:::image type="icon" source="../media/rightmrk.png" border="false":::|<span data-ttu-id="705af-504">Subset</span><span class="sxs-lookup"><span data-stu-id="705af-504">Subset</span></span>|<span data-ttu-id="705af-505">Tous les prédicats et actions DLP de point de terminaison dans la stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="705af-505">All Endpoint DLP predicates and actions in DLP policy</span></span>|<span data-ttu-id="705af-506">Voir Protection contre la perte de données sur le point de terminaison [prend en charge les conseils de stratégie pour certains types d'informations sensibles uniquement](#data-loss-prevention-on-endpoint-supports-policy-tips-for-only-some-sensitive-information-types)</span><span class="sxs-lookup"><span data-stu-id="705af-506">See [Data Loss Prevention on Endpoint supports policy tips for only some sensitive information types](#data-loss-prevention-on-endpoint-supports-policy-tips-for-only-some-sensitive-information-types)</span></span>|
|<span data-ttu-id="705af-507">**Appareils Mac**</span><span class="sxs-lookup"><span data-stu-id="705af-507">**Mac devices**</span></span>|:::image type="icon" source="../media/crsmrk.png" border="false":::|<span data-ttu-id="705af-508">Aucun</span><span class="sxs-lookup"><span data-stu-id="705af-508">None</span></span>|<span data-ttu-id="705af-509">Aucun</span><span class="sxs-lookup"><span data-stu-id="705af-509">None</span></span>|<span data-ttu-id="705af-510">La protection contre la perte de données n'est pas appliquée sur les appareils Mac aujourd'hui</span><span class="sxs-lookup"><span data-stu-id="705af-510">Data loss prevention are not enforceable on Mac devices today</span></span>|
|<span data-ttu-id="705af-511">**Applications cloud tierces**</span><span class="sxs-lookup"><span data-stu-id="705af-511">**3rd party cloud apps**</span></span>|:::image type="icon" source="../media/crsmrk.png" border="false":::|<span data-ttu-id="705af-512">Aucun</span><span class="sxs-lookup"><span data-stu-id="705af-512">None</span></span>|<span data-ttu-id="705af-513">Aucun</span><span class="sxs-lookup"><span data-stu-id="705af-513">None</span></span>|<span data-ttu-id="705af-514">Protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="705af-514">Data Loss Prevention</span></span>|
|<span data-ttu-id="705af-515">**Sur place**</span><span class="sxs-lookup"><span data-stu-id="705af-515">**On-prem**</span></span>|:::image type="icon" source="../media/crsmrk.png" border="false":::|<span data-ttu-id="705af-516">Aucun</span><span class="sxs-lookup"><span data-stu-id="705af-516">None</span></span>|<span data-ttu-id="705af-517">Aucun</span><span class="sxs-lookup"><span data-stu-id="705af-517">None</span></span>||
|<span data-ttu-id="705af-518">**Word, Excel, Powerpoint Win32 Client**</span><span class="sxs-lookup"><span data-stu-id="705af-518">**Word, Excel, Powerpoint Win32 Client**</span></span>|:::image type="icon" source="../media/crsmrk.png" border="false":::|<span data-ttu-id="705af-519">Subset</span><span class="sxs-lookup"><span data-stu-id="705af-519">Subset</span></span>|<span data-ttu-id="705af-520">Subset</span><span class="sxs-lookup"><span data-stu-id="705af-520">Subset</span></span>|<span data-ttu-id="705af-521">Les conseils de stratégie pour les applications clientes WXP fonctionnent pour les documents stockés sur Sharepoint Online ou one drive for Business Sites pour toutes les stratégies DLP qui ont exactement les conditions ou actions ci-dessous ou un sous-ensemble de conditions ou d'actions dans la stratégie DLP :</span><span class="sxs-lookup"><span data-stu-id="705af-521">Policy tips for WXP client apps will work for documents stored on Sharepoint Online or One Drive for Business Sites for all DLP policies which have exactly the below or a subset of conditions or actions in the DLP policy:</span></span></br> <ul><li><span data-ttu-id="705af-522">Le contenu contient des types d'informations sensibles</span><span class="sxs-lookup"><span data-stu-id="705af-522">Content contains sensitive information types</span></span></li><li><span data-ttu-id="705af-523">Étendue d'accès (le contenu est partagé en interne/en externe)</span><span class="sxs-lookup"><span data-stu-id="705af-523">Access Scope (Content is shared internally/externally)</span></span></li><li><span data-ttu-id="705af-524">Avertir l'utilisateur (conseils de stratégie/notifications utilisateur)</span><span class="sxs-lookup"><span data-stu-id="705af-524">Notify User (policy tips/user notifications)</span></span></li><li><span data-ttu-id="705af-525">Bloquer tout le monde</span><span class="sxs-lookup"><span data-stu-id="705af-525">Block everyone</span></span></li><li><span data-ttu-id="705af-526">Rapports d’incident</span><span class="sxs-lookup"><span data-stu-id="705af-526">Incident reports</span></span></li></ul></br> <span data-ttu-id="705af-527">Si une autre condition ou action est présente, le conseil de stratégie DLP pour cette stratégie n'apparaîtra pas dans les applications de bureau de Word, Excel ou PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="705af-527">If any other condition or action is present, the DLP policy tip for that policy will not appear in the desktop apps of Word, Excel or PowerPoint.</span></span>|
||||||
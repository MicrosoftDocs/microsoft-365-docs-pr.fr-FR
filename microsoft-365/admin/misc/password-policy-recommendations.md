---
title: Recommandations en matière de stratégie de mot de passe
f1.keywords:
- CSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection:
- Adm_O365
- Adm_NonTOC
ms.custom:
- AdminSurgePortfolio
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 9fa2539a-2211-41fd-85a0-bc37b9619ca4
description: Sécuriser votre organisation contre les attaques par mot de passe, et interdire les mots de passe courants et activer l’authentification multifacteur basée sur les risques.
ms.openlocfilehash: f580ed957b8231bc68c5f21ea9af990808478382
ms.sourcegitcommit: bbad1938b6661d4a6bca99f235c44e521b1fb662
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2021
ms.locfileid: "53006924"
---
# <a name="password-policy-recommendations"></a><span data-ttu-id="2b978-103">Recommandations en matière de stratégie de mot de passe</span><span class="sxs-lookup"><span data-stu-id="2b978-103">Password policy recommendations</span></span>

<span data-ttu-id="2b978-104">En tant qu’administrateur d’une organisation, vous êtes chargé de la configuration d'une stratégie de mot de passe pour les utilisateurs au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2b978-104">As the admin of an organization, you're responsible for setting the password policy for users in your organization.</span></span> <span data-ttu-id="2b978-105">La configuration d'une stratégie de mot de passe peut être complexe et déconcertante. Cet article vous fournit des recommandations pour renforcer la sécurité de votre organisation contre les attaques par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="2b978-105">Setting the password policy can be complicated and confusing, and this article provides recommendations to make your organization more secure against password attacks.</span></span>
  
<span data-ttu-id="2b978-106">Pour déterminer la fréquence d’expiration des mots de passe Microsoft 365 dans votre organisation, consultez la page [Définir une stratégie d’expiration de mot de passe pour Microsoft 365](../manage/set-password-expiration-policy.md).</span><span class="sxs-lookup"><span data-stu-id="2b978-106">To determine how often Microsoft 365 passwords expire in your organization, see [Set password expiration policy for Microsoft 365](../manage/set-password-expiration-policy.md).</span></span>

<span data-ttu-id="2b978-107">Pour obtenir plus d’informations sur les mots de passe Microsoft 365, consultez :</span><span class="sxs-lookup"><span data-stu-id="2b978-107">For more information about Microsoft 365 passwords, see:</span></span>

<span data-ttu-id="2b978-108">[Réinitialiser les mots de passe](../add-users/reset-passwords.md) (article)</span><span class="sxs-lookup"><span data-stu-id="2b978-108">[Reset passwords](../add-users/reset-passwords.md) (article)</span></span>

<span data-ttu-id="2b978-109">[Définir le mot de passe d’un utilisateur de façon à ce qu’il n’expire jamais](../add-users/set-password-to-never-expire.md) (article)</span><span class="sxs-lookup"><span data-stu-id="2b978-109">[Set an individual user's password to never expire](../add-users/set-password-to-never-expire.md) (article)</span></span>

<span data-ttu-id="2b978-110">[Autoriser les utilisateurs à réinitialiser leur mot de passe](../add-users/let-users-reset-passwords.md) (article)</span><span class="sxs-lookup"><span data-stu-id="2b978-110">[Let users reset their own passwords](../add-users/let-users-reset-passwords.md) (article)</span></span>

<span data-ttu-id="2b978-111">[Renvoyer le mot de passe d’un utilisateur – Aide de l’administrateur](../add-users/resend-user-password.md) (article)</span><span class="sxs-lookup"><span data-stu-id="2b978-111">[Resend a user's password - Admin Help](../add-users/resend-user-password.md) (article)</span></span>
  
## <a name="understanding-password-recommendations"></a><span data-ttu-id="2b978-112">Présentation des recommandations concernant les mots de passe</span><span class="sxs-lookup"><span data-stu-id="2b978-112">Understanding password recommendations</span></span>

<span data-ttu-id="2b978-113">Les pratiques pour mot de passe recommandées sont classées en plusieurs catégories :</span><span class="sxs-lookup"><span data-stu-id="2b978-113">Good password practices fall into a few broad categories:</span></span>
  
- <span data-ttu-id="2b978-114">**Résistance aux attaques courantes** il s’agit du choix de l’emplacement dans lequel les utilisateurs entrent les mots de passe (les appareils connus et fiables ayant une bonne détection de programmes malveillants, sites validés) et le choix du mot de passe à adopter (longueur et unicité).</span><span class="sxs-lookup"><span data-stu-id="2b978-114">**Resisting common attacks** This involves the choice of where users enter passwords (known and trusted devices with good malware detection, validated sites), and the choice of what password to choose (length and uniqueness).</span></span>

- <span data-ttu-id="2b978-115">**Contenir les attaques fructueuses** la résistance aux attaques réussies de pirates informatiques consiste à limiter l’exposition à un service précis ou à empêcher les dommages purs et simples, si le mot de passe d’un utilisateur est volé.</span><span class="sxs-lookup"><span data-stu-id="2b978-115">**Containing successful attacks** Containing successful hacker attacks is about limiting exposure to a specific service, or preventing that damage altogether, if a user's password gets stolen.</span></span> <span data-ttu-id="2b978-116">Par exemple, s’assurer qu’une violation de vos informations d’identification de réseaux sociaux ne rende pas votre compte bancaire vulnérable, ou ne pas laisser un compte peu protégé accepter des liens de réinitialisation pour un compte important.</span><span class="sxs-lookup"><span data-stu-id="2b978-116">For example, ensuring that a breach of your social networking credentials doesn't make your bank account vulnerable, or not letting a poorly guarded account accept reset links for an important account.</span></span>

- <span data-ttu-id="2b978-117">**Comprendre la nature humaine** de nombreuses pratiques valides en matière de mot de passe échouent face à des comportements humains naturels.</span><span class="sxs-lookup"><span data-stu-id="2b978-117">**Understanding human nature** Many valid password practices fail in the face of natural human behaviors.</span></span> <span data-ttu-id="2b978-118">Une compréhension de la nature humaine est essentielle, car les recherches démontrent que pratiquement toutes les règles que vous imposez à vos utilisateurs entraînent une fragilisation de la qualité des mots de passe.</span><span class="sxs-lookup"><span data-stu-id="2b978-118">Understanding human nature is critical because research shows that almost every rule you impose on your users will result in a weakening of password quality.</span></span> <span data-ttu-id="2b978-119">Les exigences de longueur, de caractères spéciaux et de modification du mot de passe entraînent une normalisation des mots de passe, ce qui permet aux pirates informatiques de deviner ou de déchiffrer les mots de passe plus facilement.</span><span class="sxs-lookup"><span data-stu-id="2b978-119">Length requirements, special character requirements, and password change requirements all result in normalization of passwords, which makes it easier for attackers to guess or crack passwords.</span></span>

## <a name="password-guidelines-for-administrators"></a><span data-ttu-id="2b978-120">Conseils relatifs aux mots de passe pour les administrateurs</span><span class="sxs-lookup"><span data-stu-id="2b978-120">Password guidelines for administrators</span></span>

<span data-ttu-id="2b978-121">La diversité des mots de passe représente l’objectif principal d’un système de mot de passe sécurisé.</span><span class="sxs-lookup"><span data-stu-id="2b978-121">The primary goal of a more secure password system is password diversity.</span></span> <span data-ttu-id="2b978-122">Votre stratégie de mot de doit contenir de nombreux mots de passe différents qui sont de plus difficiles à deviner.</span><span class="sxs-lookup"><span data-stu-id="2b978-122">You want your password policy to contain lots of different and hard to guess passwords.</span></span> <span data-ttu-id="2b978-123">Voici quelques recommandations pour garantir la sécurité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2b978-123">Here are a few recommendations for keeping your organization as secure as possible.</span></span>
  
- <span data-ttu-id="2b978-124">Conserver une exigence de longueur minimale de 8 caractères (une longueur supérieure n'est pas forcément recommandable)</span><span class="sxs-lookup"><span data-stu-id="2b978-124">Maintain an 8-character minimum length requirement (longer isn't necessarily better)</span></span>

- <span data-ttu-id="2b978-125">N'exigez pas de composition de caractères.</span><span class="sxs-lookup"><span data-stu-id="2b978-125">Don't require character composition requirements.</span></span> <span data-ttu-id="2b978-126">For exemple, \*&amp;(^%$</span><span class="sxs-lookup"><span data-stu-id="2b978-126">For example, \*&amp;(^%$</span></span>

- <span data-ttu-id="2b978-127">Ne demandez pas la réinitialisation de mot de passe régulière obligatoire pour les comptes utilisateur</span><span class="sxs-lookup"><span data-stu-id="2b978-127">Don't require mandatory periodic password resets for user accounts</span></span>

- <span data-ttu-id="2b978-128">Interdisez les mots de passe communs pour empêcher les mots de passe vulnérables d'envahir votre système</span><span class="sxs-lookup"><span data-stu-id="2b978-128">Ban common passwords, to keep the most vulnerable passwords out of your system</span></span>

- <span data-ttu-id="2b978-129">Informez vos utilisateurs pour qu'ils ne réutilisent pas leur mot de passe d'organisation à des fins autres que professionnelles</span><span class="sxs-lookup"><span data-stu-id="2b978-129">Educate your users to not re-use their organization passwords for non-work related purposes</span></span>

- <span data-ttu-id="2b978-130">Renforcer l'Inscription des utilisateurs au service d'[authentification multifacteur](../security-and-compliance/set-up-multi-factor-authentication.md)</span><span class="sxs-lookup"><span data-stu-id="2b978-130">Enforce registration for [multi-factor authentication](../security-and-compliance/set-up-multi-factor-authentication.md)</span></span>

- <span data-ttu-id="2b978-131">Autoriser les enjeux liés à l’authentification multifacteur basée sur le risque</span><span class="sxs-lookup"><span data-stu-id="2b978-131">Enable risk-based multi-factor authentication challenges</span></span>

### <a name="password-guidance-for-your-users"></a><span data-ttu-id="2b978-132">Conseils liés aux mots de passe pour vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="2b978-132">Password guidance for your users</span></span>

<span data-ttu-id="2b978-p106">Voici quelques conseils en matière de mots de passe destinés aux utilisateurs de votre organisation. Assurez-vous d'informer vos utilisateurs sur ces recommandations et d'appliquer les stratégies de mot de passe recommandées au niveau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="2b978-p106">Here's some password guidance for users in your organization. Make sure to let your users know about these recommendations and enforce the recommended password policies at the organizational level.</span></span>
  
- <span data-ttu-id="2b978-135">N’utilisez pas de mot de passe identique ou similaire à celui utilisé sur d’autres sites web</span><span class="sxs-lookup"><span data-stu-id="2b978-135">Don't use a password that is the same or similar to one you use on any other websites</span></span>

- <span data-ttu-id="2b978-136">N’utilisez pas de mot unique (par exemple, **code** ou une expression couramment utilisée de type **jetaime)**</span><span class="sxs-lookup"><span data-stu-id="2b978-136">Don't use a single word, for example, **password**, or a commonly-used phrase like **Iloveyou**</span></span>

- <span data-ttu-id="2b978-137">Veillez à ce que les mots de passe soient difficiles à deviner, même par des personnes qui vous connaissent bien, telles que les noms et les anniversaires de vos amis et de votre famille, vos groupes préférés et les phrases que vous aimez utiliser</span><span class="sxs-lookup"><span data-stu-id="2b978-137">Make passwords hard to guess, even by those who know a lot about you, such as the names and birthdays of your friends and family, your favorite bands, and phrases you like to use</span></span>

## <a name="some-common-approaches-and-their-negative-impacts"></a><span data-ttu-id="2b978-138">Approches courantes et leurs répercussions négatives</span><span class="sxs-lookup"><span data-stu-id="2b978-138">Some common approaches and their negative impacts</span></span>

<span data-ttu-id="2b978-139">Voici quelques-unes des pratiques les plus couramment utilisées en matière de gestion des mots de passe, bien que des recherches nous avertissent de leurs conséquences négatives.</span><span class="sxs-lookup"><span data-stu-id="2b978-139">These are some of the most commonly used password management practices, but research warns us about the negative impacts of them.</span></span>
  
### <a name="password-expiration-requirements-for-users"></a><span data-ttu-id="2b978-140">Exigences d’expiration du mot de passe pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="2b978-140">Password expiration requirements for users</span></span>

<span data-ttu-id="2b978-141">Les conditions d’expiration du mot de passe sont plus néfastes que bénéfiques, car elles permettent aux utilisateurs de sélectionner des mots de passe sans surprise, composés de mots et de chiffres à caractère séquentiel très liés entre eux.</span><span class="sxs-lookup"><span data-stu-id="2b978-141">Password expiration requirements do more harm than good, because these requirements make users select predictable passwords, composed of sequential words and numbers which are closely related to each other.</span></span> <span data-ttu-id="2b978-142">Dans ce cas, le mot de passe suivant peut être déterminé en se basant sur le mot de passe précédent.</span><span class="sxs-lookup"><span data-stu-id="2b978-142">In these cases, the next password can be predicted based on the previous password.</span></span> <span data-ttu-id="2b978-143">Les exigences en matière d’expiration de mot de passe ne présentent aucun avantage de confinement, car les cybercriminels utilisent pratiquement toujours les informations d’identification dès qu’ils les compromettent.</span><span class="sxs-lookup"><span data-stu-id="2b978-143">Password expiration requirements offer no containment benefits because cyber criminals almost always use credentials as soon as they compromise them.</span></span> <span data-ttu-id="2b978-144">Pour plus d’informations, consultez [Il est temps de reconsidérer les changements de mots de passe obligatoires](https://go.microsoft.com/fwlink/p/?linkid=861018).</span><span class="sxs-lookup"><span data-stu-id="2b978-144">Check out [Time to rethink mandatory password changes](https://go.microsoft.com/fwlink/p/?linkid=861018) for more info.</span></span>
  
### <a name="requiring-long-passwords"></a><span data-ttu-id="2b978-145">Exigence de mots de passe longs</span><span class="sxs-lookup"><span data-stu-id="2b978-145">Requiring long passwords</span></span>

<span data-ttu-id="2b978-146">Les exigences de longueur de mot de passe (plus de 10 caractères environ) peuvent entraîner un comportement utilisateur prévisible et non souhaitable.</span><span class="sxs-lookup"><span data-stu-id="2b978-146">Password length requirements (greater than about 10 characters) can result in user behavior that is predictable and undesirable.</span></span> <span data-ttu-id="2b978-147">Par exemple, il est possible que les utilisateurs devant utiliser un mot de passe de 16 caractères choisissent de répéter des modèles tels que **quatrequatrequatre** ou **motdepassemotdepasse** qui respectent les exigences de longueur de caractères, mais qui sont faciles à deviner.</span><span class="sxs-lookup"><span data-stu-id="2b978-147">For example, users who are required to have a 16-character password may choose repeating patterns like **fourfourfourfour** or **passwordpassword** that meet the character length requirement but aren't hard to guess.</span></span> <span data-ttu-id="2b978-148">De plus, les exigences de longueur augmentent les risques d’adoption par les utilisateurs d’autres méthodes non sécurisées, telles que l’écriture sur papier de leurs mots de passe, leur réutilisation ou leur stockage non chiffré dans leurs documents.</span><span class="sxs-lookup"><span data-stu-id="2b978-148">Additionally, length requirements increase the chances that users will adopt other insecure practices, such as writing their passwords down, re-using them, or storing them unencrypted in their documents.</span></span> <span data-ttu-id="2b978-149">Pour inciter les utilisateurs à considérer un mot de passe unique, nous vous recommandons de conserver une exigence raisonnable d'une longueur minimale de 8 caractères.</span><span class="sxs-lookup"><span data-stu-id="2b978-149">To encourage users to think about a unique password, we recommend keeping a reasonable 8-character minimum length requirement.</span></span>
  
### <a name="requiring-the-use-of-multiple-character-sets"></a><span data-ttu-id="2b978-150">Nécessité d’utiliser plusieurs jeux de caractères</span><span class="sxs-lookup"><span data-stu-id="2b978-150">Requiring the use of multiple character sets</span></span>

<span data-ttu-id="2b978-151">L'exigence de complexité de mots de passe permet de réduire l’espace de clé et d'amener les utilisateurs à agir de façon prévisible, faisant ainsi plus de mal que de bien.</span><span class="sxs-lookup"><span data-stu-id="2b978-151">Password complexity requirements reduce key space and cause users to act in predictable ways, doing more harm than good.</span></span> <span data-ttu-id="2b978-152">La plupart des systèmes appliquent des exigences de complexité des mots de passe d'un certain niveau.</span><span class="sxs-lookup"><span data-stu-id="2b978-152">Most systems enforce some level of password complexity requirements.</span></span> <span data-ttu-id="2b978-153">Par exemple, les mots de passe doivent contenir des caractères faisant partie des trois catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="2b978-153">For example, passwords need characters from all three of the following categories:</span></span>
  
- <span data-ttu-id="2b978-154">caractères majuscules</span><span class="sxs-lookup"><span data-stu-id="2b978-154">uppercase characters</span></span>

- <span data-ttu-id="2b978-155">caractères minuscules</span><span class="sxs-lookup"><span data-stu-id="2b978-155">lowercase characters</span></span>

- <span data-ttu-id="2b978-156">caractères non alphanumériques</span><span class="sxs-lookup"><span data-stu-id="2b978-156">non-alphanumeric characters</span></span>

<span data-ttu-id="2b978-157">Beaucoup de personnes utilisent des modèles similaires par exemple, une lettre majuscule en premier, un symbole en dernier et un nombre dans les deux derniers caractères.</span><span class="sxs-lookup"><span data-stu-id="2b978-157">Most people use similar patterns, for example, a capital letter in the first position, a symbol in the last, and a number in the last 2.</span></span> <span data-ttu-id="2b978-158">Les cybercriminels le savent, de sorte qu’ils exécutent leurs attaques de dictionnaire en utilisant les substitutions les plus courantes, « $ » pour « s », « @ » pour « a », « 1 » pour « l ».</span><span class="sxs-lookup"><span data-stu-id="2b978-158">Cyber criminals know this, so they run their dictionary attacks using the most common substitutions, "$" for "s", "@" for "a," "1" for "l".</span></span> <span data-ttu-id="2b978-159">Le fait de contraindre vos utilisateurs à choisir une combinaison de majuscules, minuscules et caractères spéciaux a une incidence négative.</span><span class="sxs-lookup"><span data-stu-id="2b978-159">Forcing your users to choose a combination of upper, lower, digits, special characters has a negative effect.</span></span> <span data-ttu-id="2b978-160">Certaines exigences de complexité empêchent également les utilisateurs d’utiliser des mots de passe sécurisés et mémorables, et de les contraint à faire usage de mots de passe moins sécurisés et moins marquants.</span><span class="sxs-lookup"><span data-stu-id="2b978-160">Some complexity requirements even prevent users from using secure and memorable passwords, and force them into coming up with less secure and less memorable passwords.</span></span>
  
## <a name="successful-patterns"></a><span data-ttu-id="2b978-161">Modèles performants</span><span class="sxs-lookup"><span data-stu-id="2b978-161">Successful Patterns</span></span>

<span data-ttu-id="2b978-162">En revanche, voici quelques recommandations favorisant une variété des mots de passe.</span><span class="sxs-lookup"><span data-stu-id="2b978-162">In contrast, here are some recommendations in encouraging password diversity.</span></span>
  
### <a name="ban-common-passwords"></a><span data-ttu-id="2b978-163">Interdire les mots de passe courants</span><span class="sxs-lookup"><span data-stu-id="2b978-163">Ban common passwords</span></span>

<span data-ttu-id="2b978-164">L’exigence de mot de passe la plus importante à imposer à vos utilisateurs lors de la création de mots de passe consiste à interdire l’utilisation de mots de passe communs afin de limiter la vulnérabilité de votre organisation aux attaques de mot de passe par force brute.</span><span class="sxs-lookup"><span data-stu-id="2b978-164">The most important password requirement you should put on your users when creating passwords is to ban the use of common passwords to reduce your organization's susceptibility to brute force password attacks.</span></span> <span data-ttu-id="2b978-165">Les mots de passe utilisateur courants incluent : **abcdefg**, **motdepasse** et **singe**.</span><span class="sxs-lookup"><span data-stu-id="2b978-165">Common user passwords include: **abcdefg**, **password**, **monkey**.</span></span>
  
### <a name="educate-users-to-not-re-use-organization-passwords-anywhere-else"></a><span data-ttu-id="2b978-166">Apprenez à vos utilisateurs à ne pas réutiliser ailleurs les mots de passe d’organisation</span><span class="sxs-lookup"><span data-stu-id="2b978-166">Educate users to not re-use organization passwords anywhere else</span></span>

<span data-ttu-id="2b978-167">L’un des plus importants messages à faire passer auprès des utilisateurs de votre organisation est de ne pas réutiliser autre part leur mot de passe d’organisation.</span><span class="sxs-lookup"><span data-stu-id="2b978-167">One of the most important messages to get across to users in your organization is to not re-use their organization password anywhere else.</span></span> <span data-ttu-id="2b978-168">L’utilisation de mots de passe d’organisation sur des sites web externes augmente considérablement la probabilité de compromission de ces mots de passe par des cybercriminels.</span><span class="sxs-lookup"><span data-stu-id="2b978-168">The use of organization passwords in external websites greatly increases the likelihood that cyber criminals will compromise these passwords.</span></span>
  
### <a name="enforce-multi-factor-authentication-registration"></a><span data-ttu-id="2b978-169">Imposer l'inscription avec service d'authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="2b978-169">Enforce Multi-Factor Authentication registration</span></span>

<span data-ttu-id="2b978-170">Veillez à ce que les utilisateurs mettent à jour leurs informations de sécurité et de contact, telles que l'adresse e-mail secondaire, le numéro de téléphone ou l'appareil enregistré pour les services de notifications Push afin qu'ils puissent répondre aux questions challenges et être informés des évènements de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2b978-170">Make sure your users update contact and security information, like an alternate email address, phone number, or a device registered for push notifications, so they can respond to security challenges and be notified of security events.</span></span> <span data-ttu-id="2b978-171">Les informations de contact et de sécurité mises à jour permettent aux utilisateurs de vérifier leur identité en cas d'oubli de leur mot de passe, ou si un autre utilisateur tente de prendre le contrôle de leur compte.</span><span class="sxs-lookup"><span data-stu-id="2b978-171">Updated contact and security information helps users verify their identity if they ever forget their password, or if someone else tries to take over their account.</span></span> <span data-ttu-id="2b978-172">Elles fournissent en outre un canal de notification de type hors plage en cas d'évènements de sécurité, tels que des tentatives de connexion ou des modifications de mots de passe.</span><span class="sxs-lookup"><span data-stu-id="2b978-172">It also provides an out of band notification channel in the case of security events such as login attempts or changed passwords.</span></span> 
  
<span data-ttu-id="2b978-173">Pour plus d'informations, voir [Configurer l'authentification multifacteur](../security-and-compliance/set-up-multi-factor-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="2b978-173">To learn more, see [Set up multi-factor authentication](../security-and-compliance/set-up-multi-factor-authentication.md).</span></span>
  
### <a name="enable-risk-based-multi-factor-authentication"></a><span data-ttu-id="2b978-174">Activer le service d'authentification multifacteur basé sur le risque</span><span class="sxs-lookup"><span data-stu-id="2b978-174">Enable risk-based multi-factor authentication</span></span>

<span data-ttu-id="2b978-175">L’authentification multifacteur basée sur le risque s'assure que, lorsque notre système détecte une activité suspecte, il peut défier l’utilisateur pour s’assurer qu’il s’agit bien du propriétaire du compte.</span><span class="sxs-lookup"><span data-stu-id="2b978-175">Risk-based multi-factor authentication ensures that when our system detects suspicious activity, it can challenge the user to ensure that they are the legitimate account owner.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="2b978-176">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="2b978-176">Next steps</span></span>

<span data-ttu-id="2b978-177">Vous voulez en savoir plus sur la gestion des mots de passe ?</span><span class="sxs-lookup"><span data-stu-id="2b978-177">Want to know more about managing passwords?</span></span> <span data-ttu-id="2b978-178">Voici quelques recommandations de lecture :</span><span class="sxs-lookup"><span data-stu-id="2b978-178">Here is some recommended reading:</span></span>

- [<span data-ttu-id="2b978-179">Conseils sur les mots de passe Microsoft</span><span class="sxs-lookup"><span data-stu-id="2b978-179">Microsoft Password Guidance</span></span>](https://www.microsoft.com/research/wp-content/uploads/2016/06/Microsoft_Password_Guidance-1.pdf)

- [<span data-ttu-id="2b978-180">Les mots de passe web sont-ils performants ?</span><span class="sxs-lookup"><span data-stu-id="2b978-180">Do Strong Web Passwords Accomplish Anything?</span></span>](https://go.microsoft.com/fwlink/p/?linkid=861008)

- [<span data-ttu-id="2b978-181">Portefeuilles de mots de passe et utilisateur à effort limité</span><span class="sxs-lookup"><span data-stu-id="2b978-181">Password Portfolios and the Finite-Effort User</span></span>](https://go.microsoft.com/fwlink/p/?linkid=861014)

- [<span data-ttu-id="2b978-182">Prévenir les mots de passe vulnérables en lisant dans les pensées de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="2b978-182">Preventing Weak Passwords by Reading Users' Minds</span></span>](https://go.microsoft.com/fwlink/p/?linkid=861015)

- [<span data-ttu-id="2b978-183">Choix de mots de passe sécurisés</span><span class="sxs-lookup"><span data-stu-id="2b978-183">Choosing Secure Passwords</span></span>](https://go.microsoft.com/fwlink/p/?linkid=861016)

- [<span data-ttu-id="2b978-184">L'heure est venue de reconsidérer les changement de mots de passe obligatoires</span><span class="sxs-lookup"><span data-stu-id="2b978-184">Time to rethink mandatory password changes</span></span>](https://go.microsoft.com/fwlink/p/?linkid=861018)

- [<span data-ttu-id="2b978-185">Plus mauvais mots de passe en 2015</span><span class="sxs-lookup"><span data-stu-id="2b978-185">Worst Passwords of 2015</span></span>](https://go.microsoft.com/fwlink/p/?linkid=861020)

## <a name="related-content"></a><span data-ttu-id="2b978-186">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="2b978-186">Related content</span></span>

<span data-ttu-id="2b978-187">[Réinitialiser les mots de passe](../add-users/reset-passwords.md) (article)</span><span class="sxs-lookup"><span data-stu-id="2b978-187">[Reset passwords](../add-users/reset-passwords.md) (article)</span></span>\
<span data-ttu-id="2b978-188">[Définir le mot de passe d’un utilisateur de façon à ce qu’il n’expire jamais](../add-users/set-password-to-never-expire.md) (article)</span><span class="sxs-lookup"><span data-stu-id="2b978-188">[Set an individual user's password to never expire](../add-users/set-password-to-never-expire.md) (article)</span></span>\
<span data-ttu-id="2b978-189">[Autoriser les utilisateurs à réinitialiser leur mot de passe](../add-users/let-users-reset-passwords.md) (article)</span><span class="sxs-lookup"><span data-stu-id="2b978-189">[Let users reset their own passwords](../add-users/let-users-reset-passwords.md) (article)</span></span>\
<span data-ttu-id="2b978-190">[Renvoyer le mot de passe d’un utilisateur – Aide de l’administrateur](../add-users/resend-user-password.md) (article)</span><span class="sxs-lookup"><span data-stu-id="2b978-190">[Resend a user's password - Admin Help](../add-users/resend-user-password.md) (article)</span></span>

---
title: RGPD pour Skype Entreprise Server
description: Découvrez comment satisfaire aux exigences du RGPD dans les environnements locaux Skype Entreprise Server et Lync Server.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.openlocfilehash: aa0d66bcf727b7dd3c545384ec3a4838667a9183
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41596401"
---
# <a name="gdpr-for-skype-for-business-server-and-lync-server"></a><span data-ttu-id="82553-103">RGPD pour Skype Entreprise Server et Lync Server</span><span class="sxs-lookup"><span data-stu-id="82553-103">GDPR for Skype for Business Server and Lync Server</span></span>

<span data-ttu-id="82553-p101">La plupart des données de Skype Entreprise Server et de Lync Server sont stockées dans Exchange Server. Ces données incluent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="82553-p101">Most Skype for Business Server and Lync Server data is stored in Exchange Server. This includes:</span></span>

-   <span data-ttu-id="82553-106">Historique des conversations</span><span class="sxs-lookup"><span data-stu-id="82553-106">Conversation history</span></span>

-   <span data-ttu-id="82553-107">Notifications de messagerie vocale et transcriptions</span><span class="sxs-lookup"><span data-stu-id="82553-107">Voicemail notifications and transcriptions</span></span>

-   <span data-ttu-id="82553-108">Invitations aux réunions</span><span class="sxs-lookup"><span data-stu-id="82553-108">Meeting invites</span></span>

<span data-ttu-id="82553-109">Reportez-vous aux procédures définies pour le [RGPD pour Exchange Server](gdpr-for-exchange-server.md) afin de rechercher, exporter ou supprimer ces types de données dans le cadre de demandes liées au RGPD.</span><span class="sxs-lookup"><span data-stu-id="82553-109">Use the procedures outlined for [GDPR for Exchange Server](gdpr-for-exchange-server.md) to find, export, or delete these types of data for GDPR requests.</span></span>

<span data-ttu-id="82553-p102">Les listes de contacts sont stockées dans la base de données SQL Server. Elles peuvent être exportées de plusieurs manières, décrites ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="82553-p102">Contact lists are stored in the SQL Server database. They can be exported in the following ways:</span></span>

-   <span data-ttu-id="82553-p103">Les utilisateurs finaux eux-mêmes peuvent exporter des contacts en cliquant avec le bouton droit de la souris sur l’en-tête du groupe et en sélectionnant Copier. Tous les contacts de ce groupe seront ainsi copiés dans le Presse-papiers et pourront ensuite être collés dans n’importe quelle application.</span><span class="sxs-lookup"><span data-stu-id="82553-p103">End users themselves can export the contacts by right clicking the group header and selecting Copy. This will copy all the contacts in that group into the clipboard, which can then be pasted into any app.</span></span>

-   <span data-ttu-id="82553-114">Vous pouvez utiliser la cmdlet [Export-CsUserData](https://docs.microsoft.com/powershell/module/skype/export-csuserdata) pour exporter ces données.</span><span class="sxs-lookup"><span data-stu-id="82553-114">You can use the [Export-CsUserData](https://docs.microsoft.com/powershell/module/skype/export-csuserdata) cmdlet to export this data.</span></span>

<span data-ttu-id="82553-p104">Le contenu chargé dans des réunions (comme des documents ou fichiers PowerPoint) ou le contenu généré lors d’une réunion (comme le tableau blanc, des sondages ou des questions et réponses) est stocké dans l’organisateur de fichiers. Il peut également être exporté si des utilisateurs finaux se reconnectent à une réunion qui n’a pas expiré et téléchargent un contenu qui y a été chargé ou prennent des captures d’écran dans le cas où le contenu a été généré.</span><span class="sxs-lookup"><span data-stu-id="82553-p104">Content uploaded into meetings (such as PowerPoint files or handouts) or content generated in a meeting (such as whiteboard, polls, or Q/A) is stored in the filer. This can also be exported if end users log back into any meeting that has not expired and download any uploaded content or take screenshots in the case of generated content.</span></span>

<span data-ttu-id="82553-p105">Les réunions MeetNow qui ne se trouvent pas dans le calendrier Exchange, tout comme la liste de contacts et les droits des contacts (famille, collègue, etc.) se trouvent dans la base de données utilisateur. Dans Lync Server 2013 et les versions ultérieures, vous pouvez utiliser la cmdlet [Export-CsUserData](https://docs.microsoft.com/powershell/module/skype/export-csuserdata) pour exporter ces données.</span><span class="sxs-lookup"><span data-stu-id="82553-p105">MeetNow meetings that are not in the Exchange Calendar and Contact List and contact rights (family, co-worker, etc.) are in the User Database. In Lync Server 2013 and later, you can use the [Export-CsUserData](https://docs.microsoft.com/powershell/module/skype/export-csuserdata) cmdlet to export this data.</span></span>

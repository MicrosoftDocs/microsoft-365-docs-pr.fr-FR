---
title: RGPD pour Office Online Server et Office Web Apps Server
description: Dans cet article, vous allez découvrir comment répondre aux exigences du RGPD pour Office Online Server et Office Web Apps Server.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.custom:
- seo-marvel-mar2020
titleSuffix: Microsoft GDPR
ms.openlocfilehash: 84ea370f513ade134df75b2ee4e0912d6a623227
ms.sourcegitcommit: 27daadad9ca0f02a833ff3cff8a574551b9581da
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2020
ms.locfileid: "47547340"
---
# <a name="gdpr-for-office-web-apps-server-and-office-online-server"></a><span data-ttu-id="81f4b-103">RGPD pour Office Web Apps Server et Office Online Server</span><span class="sxs-lookup"><span data-stu-id="81f4b-103">GDPR for Office Web Apps Server and Office Online Server</span></span>

<span data-ttu-id="81f4b-p101">Les données de télémétrie Office Online Server et Office Web Apps Server sont stockées sous forme de journaux ULS. Vous pouvez utiliser la [visionneuse ULS](https://www.microsoft.com/download/details.aspx?id=44020) pour afficher les journaux ULS depuis votre client local.</span><span class="sxs-lookup"><span data-stu-id="81f4b-p101">Office Online Server and Office Web Apps Server telemetry data is stored in the form of ULS logs. You can use [ULS Viewer](https://www.microsoft.com/download/details.aspx?id=44020) to view ULS logs from your on-premises tenant.</span></span>

<span data-ttu-id="81f4b-p102">Chaque ligne de journal contient un élément CorrelationID. Les lignes de journal connexes partagent le même CorrelationID. Chacun de ces éléments CorrelationID est lié à un seul élément SessionID, qui, lui, peut être associé à plusieurs éléments CorrelationID. Chaque SessionID peut être lié à un seul UserID, bien que certaines sessions puissent être anonymes et donc ne pas avoir d’élément UserID associé. Afin de déterminer les données qui sont associées à un utilisateur particulier, il est donc possible d’établir un mappage à partir d’un seul élément UserID vers les éléments SessionID associés à cet utilisateur, à partir de ces éléments SessionID vers les éléments CorrelationID associés et à partir de ces éléments CorrelationID vers tous les journaux de ces corrélations. Reportez-vous au diagramme ci-dessous pour voir la relation entre les différents ID.</span><span class="sxs-lookup"><span data-stu-id="81f4b-p102">Every log line contains a CorrelationID. Related log lines share the same CorrelationID. Each CorrelationID is tied to a single SessionID, and one SessionID may be related to many CorrelationIDs. Each SessionID may be related to a single UserID, although some sessions can be anonymous and therefore not have an associated UserID. In order to determine what data is associated with a particular user, it is therefore possible to map from a single UserID to the SessionIDs associated with that user, from those SessionIDs to the associated CorrelationIDs, and from those CorrelationIDs to all the logs in those correlations. See the below diagram for the relationship between the different IDs.</span></span>

![Organigramme montrant la relation entre SessionIDs et CorrelationIds](../media/gdpr-for-office-online-server-image1.jpg)

## <a name="gathering-logs"></a><span data-ttu-id="81f4b-113">Collecte de journaux</span><span class="sxs-lookup"><span data-stu-id="81f4b-113">Gathering Logs</span></span>

<span data-ttu-id="81f4b-p103">Afin de collecter tous les journaux associés à l’élément UserID 1, par exemple, la première étape consisterait à collecter toutes les sessions associées à cet élément UserID 1 (c'est-à-dire, les éléments SessionID 1 et SessionID 2). L’étape suivante consisterait à collecter toutes les corrélations associées aux éléments SessionID 1 (c'est-à-dire, les éléments CorrelationID 1, 2 et 3) et SessionID 2 (c'est-à-dire, l’élément CorrelationID 4). Enfin, il faudrait collecter tous les journaux associés à chacune des corrélations de la liste.</span><span class="sxs-lookup"><span data-stu-id="81f4b-p103">In order to gather all logs associated with UserID 1, for example, the first step would be to gather all sessions associated with UserID 1 (i.e. SessionID 1 and SessionID2). The next step would be to gather all correlations associated with SessionID 1 (i.e. CorrelationIDs 1, 2, and 3) and with SessionID 2 (i.e. CorrelationID 4). Finally, gather all logs associated with each of the correlations in the list.</span></span>

1. <span data-ttu-id="81f4b-117">Lancez ULSViewer.</span><span class="sxs-lookup"><span data-stu-id="81f4b-117">Launch UlsViewer</span></span>

2. <span data-ttu-id="81f4b-118">Ouvrez le journal ULS correspondant à la période souhaitée ; les journaux ULS sont stockés dans %PROGRAMDATA%\\Microsoft\\OfficeWebApps\\Data\\Logs\\ULS.</span><span class="sxs-lookup"><span data-stu-id="81f4b-118">Open up the uls log corresponding to the intended timeframe; ULS logs are stored in %PROGRAMDATA%\\Microsoft\\OfficeWebApps\\Data\\Logs\\ULS</span></span>

3. <span data-ttu-id="81f4b-119">Éditez | Modifiez le filtre.</span><span class="sxs-lookup"><span data-stu-id="81f4b-119">Edit | Modify Filter</span></span>

4. <span data-ttu-id="81f4b-120">Appliquez le filtre suivant :</span><span class="sxs-lookup"><span data-stu-id="81f4b-120">Apply a filter that is:</span></span>

    - <span data-ttu-id="81f4b-121">EventID est égal à apr3y</span><span class="sxs-lookup"><span data-stu-id="81f4b-121">EventID equals apr3y</span></span>

      <span data-ttu-id="81f4b-122">Ou</span><span class="sxs-lookup"><span data-stu-id="81f4b-122">Or</span></span>

    - <span data-ttu-id="81f4b-123">EventID est égal à bp2d6</span><span class="sxs-lookup"><span data-stu-id="81f4b-123">EventID equals bp2d6</span></span>

5. <span data-ttu-id="81f4b-124">Les éléments UserID hachés sont stockés dans le message de l’un de ces deux événements.</span><span class="sxs-lookup"><span data-stu-id="81f4b-124">Hashed UserIds will be in the Message of either one of these two events</span></span>

6. <span data-ttu-id="81f4b-125">Pour apr3y, le message contient une valeur UserID et une valeur PUID.</span><span class="sxs-lookup"><span data-stu-id="81f4b-125">For apr3y, the Message will contain a UserID value and a PUID value</span></span>

7. <span data-ttu-id="81f4b-p104">Pour bp2d6, le message contient d’autres informations. Le champ de la valeur LoggableUserId est l’élément UserID haché.</span><span class="sxs-lookup"><span data-stu-id="81f4b-p104">For bp2d6, the Message will contain quite a bit of information. The LoggableUserId Value field is the hashed UserID.</span></span>

8. <span data-ttu-id="81f4b-128">Une fois que vous avez récupéré l’élément UserID haché à partir de l’un de ces deux événements, la valeur WacSessionId de cette ligne dans ULSViewer contient l’élément WacSessionId associé à cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="81f4b-128">Once the hashed UserId is obtained from either of these two tags, the WacSessionId value of that row in ULSViewer will contain the WacSessionId associated with that user</span></span>

9. <span data-ttu-id="81f4b-129">Collectez toutes les valeurs WacSessionId associées à l’utilisateur en question.</span><span class="sxs-lookup"><span data-stu-id="81f4b-129">Collect all of the WacSessionId values associated with the user in question</span></span>

10. <span data-ttu-id="81f4b-130">Filtrez tous les éléments EventID dont la valeur est « xmnv », le message obtenu sera « UserSessionId=\<WacSessionId\>WacSessionId » pour le premier élément WacSessionId de la liste (en remplaçant l’élément \<WacSessionId\> du filtre par votre élément WacSessionId).</span><span class="sxs-lookup"><span data-stu-id="81f4b-130">Filter for all EventId equals "xmnv", Message equals "UserSessionId=\<WacSessionId\>" for the first WacSessionId in the list (replacing the \<WacSessionId\> part of the filter with your WacSessionId)</span></span>

11. <span data-ttu-id="81f4b-131">Collectez toutes les valeurs de corrélation qui correspondent à cet élément WacSessionId.</span><span class="sxs-lookup"><span data-stu-id="81f4b-131">Collect all values of Correlation that match that WacSessionId</span></span>

12. <span data-ttu-id="81f4b-132">Répétez les étapes 10 et 11 pour toutes les valeurs de WacSessionId dans votre liste pour l’utilisateur en question.</span><span class="sxs-lookup"><span data-stu-id="81f4b-132">Repeat steps 10-11 for all values of WacSessionId in your list for the user in question</span></span>

13. <span data-ttu-id="81f4b-133">Filtrez toutes les corrélations qui correspondent à la première corrélation de votre liste.</span><span class="sxs-lookup"><span data-stu-id="81f4b-133">Filter for all Correlation equals the first Correlation in your list</span></span>

14. <span data-ttu-id="81f4b-134">Collectez tous les journaux correspondant à cette corrélation.</span><span class="sxs-lookup"><span data-stu-id="81f4b-134">Collect all logs matching that Correlation</span></span>

15. <span data-ttu-id="81f4b-135">Répétez les étapes 13 et 14 pour toutes les valeurs de la corrélation de votre liste pour l’utilisateur en question.</span><span class="sxs-lookup"><span data-stu-id="81f4b-135">Repeat steps 13-14 for all values of Correlation in your list for the user in question</span></span>

## <a name="types-of-data"></a><span data-ttu-id="81f4b-136">Types de données</span><span class="sxs-lookup"><span data-stu-id="81f4b-136">Types of Data</span></span>

<span data-ttu-id="81f4b-p105">Les journaux Office contiennent de nombreux types de données différents. Voici quelques exemples de données que contiennent les journaux ULS :</span><span class="sxs-lookup"><span data-stu-id="81f4b-p105">Office logs contain a variety of different types of data. The following are examples of the data that ULS logs may contain:</span></span>

- <span data-ttu-id="81f4b-139">Des codes d’erreur pour les problèmes rencontrés lors de l’utilisation du produit</span><span class="sxs-lookup"><span data-stu-id="81f4b-139">Error codes for issues encountered during use of the product</span></span>

- <span data-ttu-id="81f4b-140">Des clics et autres données sur l’utilisation de l’application</span><span class="sxs-lookup"><span data-stu-id="81f4b-140">Button clicks and other pieces of data about app usage</span></span>

- <span data-ttu-id="81f4b-141">Des données sur les performances de l’application et/ou des fonctionnalités particulières au sein de l’application</span><span class="sxs-lookup"><span data-stu-id="81f4b-141">Performance data about the app and/or particular features within the app</span></span>

- <span data-ttu-id="81f4b-142">Des informations générales sur l’emplacement de l’ordinateur de l’utilisateur (par exemple, le pays/la région, le département et la ville, issus de l’adresse IP), mais pas une géolocalisation précise.</span><span class="sxs-lookup"><span data-stu-id="81f4b-142">General location information about where the user’s computer is (e.g. country / region, state, and city, derived from the IP address), but not precise geo location.</span></span>

- <span data-ttu-id="81f4b-143">Des métadonnées de base sur le navigateur, par exemple, le nom et la version du navigateur, et sur l’ordinateur, par exemple, son type de système d’exploitation et sa version</span><span class="sxs-lookup"><span data-stu-id="81f4b-143">Basic metadata about the browser, e.g. browser name and version, and the computer, e.g. OS type and version</span></span>

- <span data-ttu-id="81f4b-144">Des messages d’erreur de l’hôte du document (par exemple, OneDrive, SharePoint, Exchange)</span><span class="sxs-lookup"><span data-stu-id="81f4b-144">Error messages from the document host (e.g. OneDrive, SharePoint, Exchange)</span></span>

- <span data-ttu-id="81f4b-145">Des informations sur les processus internes de l’application, non liés aux actions entreprises par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="81f4b-145">Information about processes internal to the app, unrelated to any action the user has taken</span></span>

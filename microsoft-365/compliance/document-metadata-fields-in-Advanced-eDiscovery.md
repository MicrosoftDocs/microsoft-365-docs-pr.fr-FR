---
title: Champs de métadonnées des documents dans l'Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Cet article définit les champs de métadonnées pour les documents d’un jeu à réviser dans un cas Advanced eDiscovery dans Microsoft 365.
ms.openlocfilehash: 42f349bf01d5a777535dd04096b860a0165f1edf
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52769568"
---
# <a name="document-metadata-fields-in-advanced-ediscovery"></a>Champs de métadonnées des documents dans l'Advanced eDiscovery

Le tableau suivant répertorie les champs de métadonnées pour les documents d’un jeu à réviser dans un cas Advanced eDiscovery. Le tableau fournit les informations suivantes :

- **Nom** du  champ et nom du champ d’affichage : nom du champ de métadonnées et nom du champ affiché lors de l’affichage des métadonnées de fichier d’un document sélectionné dans un jeu à réviser. Certains champs de métadonnées ne sont pas inclus lors de l’affichage des métadonnées de fichier d’un document. Ces champs sont mis en surbrill plan avec un astérisque (*).

- **Nom du champ utilisable dans une recherche :** Nom de la propriété que vous pouvez rechercher lors de l’exécution d’une requête [de jeu à réviser.](review-set-search.md) Une cellule vide signifie que vous ne pouvez pas rechercher le champ dans une requête de jeu à réviser.

- **Nom du champ exporté :** Nom du champ de métadonnées inclus lors de l’exportation des documents.  Une cellule vide signifie que le champ n’est pas inclus avec les métadonnées exportées.

- **Description :** Description du champ de métadonnées.

> [!NOTE]
> Le **champ Mots clés dans** la recherche de jeu à [réviser](./review-set-search.md) utilise le langage KQL (Keyword Query Language). Les champs répertoriés  dans la colonne Nom de  champ utilisable dans une recherche peuvent être utilisés dans le champ Mots clés d’une recherche de jeu à réviser pour former des requêtes complexes sans que vous n’avez à utiliser le générateur de requêtes. Pour plus d’informations sur KQL, consultez la référence [de la syntaxe du langage](/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)de requête de mot clé.

|**Nom du champ** et **nom du champ d’affichage**|**Nom du champ utilisable dans une recherche**|**Nom du champ exporté**|**Description**|
|:-----|:-----|:-----|:-----|
|ID de contenu de pièce jointe|AttachmentContentId||ID de contenu de pièce jointe de l’élément.|
|Score de privilège client avocat|AttorneyClientPrivilegeScore||Score de contenu du modèle de privilège client-avocat.|
|Auteur|Auteur|Doc_authors|Auteur à partir des métadonnées du document.|
|Cci|Cci|Email_bcc|Champ Bcc pour les types de messages. Le format **est \<SMTPAddress> DisplayName**.|
|Cc|Cc|Email_cc|Champ Cc pour les types de messages. Le format **est \<SMTPAddress> DisplayName**.|
|Étiquettes de conformité|ComplianceLabels|Compliance_labels|[Étiquettes de rétention](retention.md) appliquées au contenu Office 365.|
|Chemin composé|CompoundPath|Compound_path|Chemin lisible par l’homme qui décrit la source de l’élément.|
|Content*|Contenu||Texte extrait de l’élément.|
|Corps de la conversation|Corps de la conversation||Corps de conversation de l’élément.|
|Conversation Topic|Conversation Topic||Rubrique de conversation de l’élément.|
|Conversation ID|ConversationId|Conversation_ID|ID de conversation du message.|
|Conversation Index||Conversation_index|Index de conversation du message.|
|Heure pdf de la conversation|ConversationPdfTime||Date de création de la version PDF de la conversation.|
|Temps de redéaction de conversation|ConversationRedaction PleinTime||Date à laquelle la version PDF de la conversation a été créée pour la conversation.|
|||Converted_file_path|Chemin d’accès du fichier d’exportation converti. Pour une utilisation interne à Microsoft uniquement.|
|Date de création du document|CreatedTime|Doc_date_created|Créer une date à partir des métadonnées du document.|
|Consignataire|Consignataire|Consignataire|Nom du dépositaire à qui l’élément a été associé.|
|Date|Date|Date|Date est un champ calculé qui dépend du type de fichier.<br /><br />Courrier électronique : date d’envoi<br />Pièces jointes : date de dernière modification du document ; si elle n’est pas disponible, date d’envoi du parent<br />Documents incorporés : date de la dernière modification du document ; si elle n’est pas disponible, date de la dernière modification du parent<br />Documents SPO (pièces jointes modernes) : SharePoint date de dernière modification ; si non disponible, date de la dernière modification des documents<br />Documents non Office 365 : Date de la dernière modification<br />Réunions : date de début de la réunion<br />Messagerie vocale : date d’envoi<br />Messagerie instantanée : date d’envoi|
|Autres chemins d’accès|Dedupedcompoundpath|Deduped_compound_path|Liste des chemins d’accès composés de documents qui sont des doublons exacts (e-mail : en fonction du contenu, documents : en fonction du hachage).|
|Autres dépositaires|DedupedCustodians|Deduped_custodians|Liste des dépositaires de documents qui sont des doublons exacts (pour le courrier électronique, en fonction du contenu ; pour les documents, en fonction du hachage).|
|Autres ID de fichier|DedupedFileIds|Deduped_file_IDs|Liste des ID de fichiers des documents qui sont des doublons exacts (pour le courrier électronique, en fonction du contenu ; pour les documents, en fonction du hachage).|
|Commentaires sur le document|DocComments|Doc_comments|Commentaires des métadonnées du document.|
|Société de documents||Doc_company|Société à partir des métadonnées du document.|
|DocIndex*|||Index de la famille. **-1 ou** **0 signifie** qu’il s’agit de la racine.|
|Mots clés de document||Doc_keywords|Mots clés des métadonnées du document.|
|Document modifié par||Doc_modified_by|Date de la dernière modification à partir des métadonnées du document.|
|Révision du document|Doc_Version|Doc_Version|Révision à partir des métadonnées du document.|
|Objet du document||Doc_subject|Objet des métadonnées du document.|
|Modèle de document||Doc_template|Modèle à partir des métadonnées du document.|
|DocLastSavedBy||Doc_last_saved_by|Nom de l’utilisateur qui a enregistré le document pour la dernière fois.|
|Thème dominant|DominantTheme|Dominant_theme|Thème dominant tel que calculé pour l’analyse.|
|Sous-ensemble en double||Duplicate_subset|ID de groupe pour les doublons exacts.|
|EmailAction*||Email_action|Les valeurs **sont None,** **Reply** ou **Forward**; basé sur la ligne d’objet d’un message.|
|Accusé de réception du courrier électronique demandé||Email_delivery_receipt|Adresse de messagerie fournie dans les en-têtes Internet pour l’accusé de réception.|
|Importance|EmailImportance|Email_importance|Importance du message : **0** - Faible ; **1** - Normal ; **2** - Élevé|
|Erreurs de traitement ignorées|ErrorIgnored|Error_Ignored|L’erreur a été ignorée et n’a pas été corrigé.|
|EmailInternetHeaders|EmailInternetHeaders|Email_internet_headers|Ensemble complet d’en-têtes de courrier à partir du message électronique|
|EmailLevel*||Email_level|Indique le niveau d’un message dans le thread de messagerie à qui il appartient ; les pièces jointes héritent de la valeur de son message parent.|
|ID de message électronique||Email_message_ID|ID de message Internet du message.|
|EmailReadReceiptRequested||Email_read_receipt|Adresse de messagerie fournie dans les en-têtes Internet pour la réception de la lecture.|
|Sécurité du courrier électronique|EmailSecurity|Email_security|Paramètre de sécurité du message : **0** - Aucun ; **1** - Signé ; **2** : chiffré ; **3** : chiffré et signé.|
|Sensibilité de l’e-mail|EmailSensitivity|email_sensitivity|Paramètre de sensibilité du message : **0** - Aucun ; **1** Personnel ; **2** - Privé ; **3** - CompanyConfidential.|
|Ensemble de messages électroniques|EmailSet|Email_set|ID de groupe pour tous les messages dans le même ensemble de messages électroniques.|
|EmailThread*||Email_thread|Position du message dans l’ensemble de messages électroniques ; se compose d’ID de nœud de la racine au message actuel et est séparé par des point (.).|
|||Export_native_path|Chemin d’accès du fichier exporté.|
|Type de contenu extrait||Native_type|Type de contenu extrait, sous la forme de type mime ; par exemple, **image/jpeg**|
|||Extracted_text_path|Chemin d’accès au fichier texte extrait dans l’exportation.|
|ExtractedTextLength*||Extracted_text_length|Nombre de caractères dans le texte extrait.|
|FamilyDuplicateSet*||Family_duplicate_set|Identificateur numérique pour les familles qui sont des doublons exacts les uns des autres (même contenu et toutes les mêmes pièces jointes).|
|ID de famille|FamilyId|Family_ID|Rassemble tous les éléments pour le courrier électronique. Cela inclut le message, ainsi que toutes les pièces jointes et éléments extraits.|
|Taille de la famille||Family_size|Nombre de documents de la famille.|
|Classe de fichier|FileClass|File_class|Pour le contenu de SharePoint et OneDrive : **Document**; pour le contenu de Exchange : **e-mail** ou **pièce jointe**.|
|ID de fichier|FileId|File_ID|Identificateur de document unique dans le cas.|
|Date de création du système de fichiers||File_system_date_created|Date de création à partir du système de fichiers (s’applique uniquement aux données non Office 365 données).|
|Date de modification du système de fichiers||File_system_date_modified|Date de modification à partir du système de fichiers (s’applique uniquement aux données Office 365 non modifiées).|
|Type de fichier|FileType||Type de fichier de l’élément en fonction de l’extension de fichier.|
|ID de groupe|ID de groupe|Group_ID|Rassemble tous les éléments pour les e-mails et les documents. Pour le courrier électronique, cela inclut le message, ainsi que toutes les pièces jointes et éléments extraits. Pour les documents, cela inclut le document et tous les éléments incorporés.|
|A une pièce jointe|HasAttachment|Email_has_attachment|Indique si le message a des pièces jointes.|
|A un avocat|HasAttorney||**True** lorsqu’au moins l’un des participants est trouvé dans la liste des avocats ; Sinon, la valeur est **False**.|
|HasText*||Has_text|Indique si l’élément possède du texte ; les valeurs possibles **sont True** et **False**.|
|ID non modifiable||Immutable_ID|Cet ID est utilisé pour identifier de manière unique un document au sein d’un jeu à réviser. Ce champ ne peut pas être utilisé dans une recherche de jeu à réviser et l’ID ne peut pas être utilisé pour accéder à un document à son emplacement natif.|
|Type d’inclusion|InclusiveType|Inclusive_type|Type d’inclusion calculé pour **l’analyse : 0** - non inclus ; **1** - inclus ; **2** - inclus moins ; **3** : copie incluse.|
|In Reply To Id||In_reply_to_ID|En réponse à l’ID du message.|
|InputFileExtension||Original_file_extension|Extension de fichier d’origine du fichier.|
|InputFileID||Input_file_ID|ID de fichier de l’élément de niveau supérieur dans le jeu à réviser. Pour une pièce jointe, cet ID sera l’ID du parent. Cela peut être utilisé pour grouper des familles.|
|Pièce jointe moderne| IsModernAttachment|  |Ce fichier est une pièce jointe moderne ou un fichier lié.|
|Est à partir de la version du document | IsFromDocumentVersion |  |Le document actuel est issu d’une version différente d’un autre document.|
|Est-ce que la pièce jointe est un e- | IsEmailAttachment|  |Cet élément est issu d’une pièce jointe à un e-mail qui apparaît comme un élément joint au message.|
|Pièce jointe inline| IsInlineAttachment|  |Cette ligne a été jointe et apparaît dans le corps du message.|
|Est représentatif|IsRepresentative|Is_representative|Un document dans chaque ensemble de doublons exacts est marqué comme représentant.|
|Classe de l’élément|ItemClass|Item_class|Classe d’élément fournie par le serveur Exchange ; par exemple, **IPM. Remarque**|
|Dernière modification|LastModifiedDate|Doc_date_modified|Date de la dernière modification à partir des métadonnées du document.|
|ID de chargement|LoadId|Load_ID|ID du jeu de chargement dans lequel l’élément a été ajouté à un jeu à réviser.|
|Emplacement|Emplacement|Emplacement|Chaîne qui indique le type d’emplacement d’origine des documents.<br /><br />**Données importées** : données non Office 365 données<br />**Teams** - Microsoft Teams<br />**Exchange** - boîtes aux lettres Exchange boîtes aux lettres<br />**SharePoint** - SharePoint sites<br />**OneDrive** - OneDrive comptes|
|Nom de l’emplacement|LocationName|Location_name|Chaîne qui identifie la source de l’élément. Pour exchange, il s’adressera à l’adresse SMTP de la boîte aux lettres . pour SharePoint et OneDrive, l’URL de la collection de sites.|
|||Marked_as_pivot|Ce fichier est le tableau croisé dynamique d’un jeu quasiment en double.|
|Marqué comme représentant|MarkAsRepresentative||Un document de chaque ensemble de doublons exacts est marqué comme représentant.|
|Date de fin de réunion|MeetingEndDate|Meeting_end_date|Date de fin de réunion pour les réunions.|
|Date de début de la réunion|MeetingStartDate|Meeting_start_date|Date de début de réunion pour les réunions.|
|Type de message|MessageKind|Message_kind|Type de message à rechercher. Valeurs possibles : documents de contacts e-mail **<br /> <br /> <br /> <br /> <br /> externaldata <br /> faxes <br /> im <br /> journals <br /> meetings <br /> microsoftteams** (returns items from chats, meetings, and calls in Microsoft Teams) **<br /> notes posts <br /> <br /> rssfeeds <br /> tasks <br /> voicemail**| 
|ID parent de pièce jointe moderne||ModernAttachment_ParentId|ID non permutable du parent du document.|
|Native Extension|NativeExtension|Native_extension|Extension native de l’élément.|
|Nom de fichier natif|NativeFileName|Native_file_name|Nom de fichier natif de l’élément.|
|NativeMD5||Native_MD5|Hachage MD5 (valeur de hachage 128 bits) du flux de fichier.|
|NativeSHA256||Native_SHA_256|Hachage SHA256 (valeur de hachage 256 bits) du flux de fichier.|
|Tri ND/ET : exclusion des pièces jointes|NdEtSortExclAttach|ND_ET_sort_excl_attach|Concaténation de l’ensemble de threads de messagerie (ET) et du jeu de quasi-doublons (ND). Ce champ est utilisé pour un tri efficace au moment de la révision. Un **D** est préfixé de jeux de ND et un **E** est précédé de jeux ET.|
|Tri ND/ET : y compris les pièces jointes|NdEtSortInclAttach|ND_ET_sort_incl_attach|Concaténation d’un ensemble de threads de messagerie (ET) et d’un jeu de threads quasi-dupliqués (ND). Ce champ est utilisé pour un tri efficace au moment de la révision. Un **D** est préfixé de jeux de ND et un **E** est précédé de jeux ET. Chaque élément de courrier électronique d’un ensemble ET est suivi de ses pièces jointes appropriées.|
|Jeu de quasi-doublons||ND_set|Les éléments similaires au document pivot partagent la même ND_set.|
|Auteurs O365||O365_authors|Auteur à partir SharePoint.|
|O365 créé par||O365_created_by|Créé à partir de SharePoint.|
|Date de création d’O365||O365_date_created|Date de création à partir SharePoint.|
|Date O365 modifiée||O365_date_modified|Date de la dernière modification SharePoint.|
|O365 modifié par||O365_modified_by|Modifié à partir de SharePoint.|
|Parent ID|ParentId|Parent_ID|ID du parent de l’élément.|
|ParentNode||Parent_node|Message électronique précédent le plus proche dans le thread de messagerie.|
|Domaines des participants|ParticipantDomains|Email_participant_domains|Liste de tous les domaines des participants d’un message.|
|Participants|Participants|Email_participants|Liste de tous les participants d’un message ; par exemple, Sender, To, Cc, Bcc.|
|ID de tableau croisé dynamique|PivotId|Pivot_ID|ID d’un tableau croisé dynamique.|
|Potentiellement privilégié|Potentiellement privilégié|Potentially_privileged|True si le modèle de détection des privilèges client-avocat considère le document comme potentiellement privilégié|
|État du traitement|ProcessingStatus|Error_code|État du traitement après l’ajout de l’élément à un jeu à réviser.|
|Lire le centile|ReadPercentile||Lire le centile du document en fonction de la pertinence.|
|Received|Received|Email_date_received|Date et heure de réception de l’e-mail au UTC.|
|Nombre de destinataires||Recipient_count|Nombre de destinataires dans le message.|
|Domaines des destinataires|RecipientDomains|Email_recipient_domains|Liste de tous les domaines des destinataires d’un message.|
|Destinataires|Destinataires|Email_recipients|Liste de tous les destinataires d’un message (À, Cc, Cci).|
|||Redacted_file_path|Chemin d’accès du fichier de remplacement rédigé dans l’exportation.|
|||Redacted_text_path|Chemin d’accès du remplacement de fichier texte rédigé dans l’exportation. Pour une utilisation interne à Microsoft uniquement.|
|Problème de cas de balise de pertinence 1||Relevance_tag_case_issue_1|Problème case de balise de pertinence 1 à partir de la pertinence.|
|Score de pertinence|RelevanceScore||Score de pertinence d’un document en fonction de la pertinence.|
|Balise de pertinence|RelevanceTag||Score de pertinence d’un document en fonction de la pertinence.|
|ID représentant|RepresentativeId||Identificateur numérique de chaque ensemble de doublons exacts.|
|||Row_number|Numéro de ligne de l’élément dans le fichier de chargement.|
|Expéditeur|Expéditeur|Email_sender|Champ Expéditeur (De) pour les types de messages. Le format **est \<SmtpAddress> DisplayName**.|
|Sender/Author|SenderAuthor||Champ calculé composé de l’expéditeur ou de l’auteur de l’élément.|
|Domaine de l’expéditeur|SenderDomain|Email_sender_domain|Domaine de l’expéditeur.|
|Sent|Sent|Email_date_sent|Date d’envoi du message.|
|Définir l’ordre : premier inclus|SetOrderInclusivesFirst|Set_order_inclusives_first|Champ tri - courrier électronique et pièces jointes : contre-chronologique ; documents : s’pivoter d’abord en descendant le score de similarité.|
|Définir l’ID||Set_ID|Les documents de contenu similaire (ND_set) ou de courrier électronique dans le même thread de messagerie (Email_set) partagent le même Set_ID.|
|SimilarityPercent||Similarity_percent|Indique à quel point un document est similaire au tableau croisé dynamique du jeu en double proche.|
|Taille de fichier native|Size|Native_size|Nombre d’octets de l’élément natif.|
|Sujet|Sujet|Email_subject|Objet du message.|
|Objet/Titre|SubjectTitle||Champ calculé composé de l’objet ou du titre de l’élément.|
|Balises|Balises|Balises|Balises appliquées dans un jeu à réviser.|
|Liste des thèmes|ThemesList|Themes_list|Liste des thèmes telle que calculée pour l’analyse.|
|Titre|Titre|Doc_title|Titre des métadonnées du document.|
|À|À|Email_to|Champ pour les types de messages. Format : **DisplayName \<SmtpAddress>**|
|Unique dans l’ensemble de courriers électroniques|UniqueInEmailSet||**False** s’il existe un doublon de la pièce jointe dans son ensemble de courriers électroniques.|
|ID de groupe de version||Version_Group_Id|Rassemble les différentes versions du même document.|
|A été corrigé|WasRemediated|Was_Remediated|**True** si l’élément a été corrigé, sinon **False**.|
|Statistiques|WordCount|Word_count|Nombre de mots dans l’élément.|
|||||

> [!NOTE]
> Pour plus d’informations sur les propriétés utilisables dans une recherche lors de la recherche d’emplacements de contenu Office 365 lorsque vous collectez des données pour un cas Advanced eDiscovery, voir Requêtes par mot clé et conditions de recherche pour la recherche de [contenu.](keyword-queries-and-search-conditions.md)

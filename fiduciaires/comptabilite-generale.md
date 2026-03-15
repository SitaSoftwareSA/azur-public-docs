# Comptabilité Générale

### Les données clients et fournisseurs <a href="#les-donnees-clients-et-fournisseurs" id="les-donnees-clients-et-fournisseurs"></a>

Avant de commencer avec l'encodage des données clients et fournisseurs, il est important de connaître les fonctionnalités des masques d'encodage.

### Le “Masque” <a href="#le-masque-masque" id="le-masque-masque"></a>

Le principe est simple, l'enregistrement "Masque" est un type d'enregistrement spécial, il contient les valeurs qui sont remplies automatiquement lors de la création d'un nouvel enregistrement.

![](<../.gitbook/assets/image (153).png>)

Vous pouvez accéder à cet enregistrement en cliquant sur le bouton " Masque " qui se trouve sur la barre de contrôle de l'écran d'encodage.

Après avoir cliqué sur ce bouton vous pouvez consulter les valeurs des champs de l'enregistrement "Masque". S'il y a des valeurs qui restent les mêmes pour la plupart des enregistrements, comme par exemple le code TVA des articles, vous pouvez les insérer dans cet enregistrement. Si vous avez terminé il faut encore cliquer sur "Valider" pour enregistrer vos modifications. Si vous créez par après un nouvel article, la valeur du code TVA sera déjà pré remplie. Les modifications que vous effectuez ici ne sont pas définitives, elles pourront à chaque moment être révisées.

### L’organisation en familles, groupes et sous-groupes <a href="#lorganisation-en-familles-groupes-et-sous-groupes" id="lorganisation-en-familles-groupes-et-sous-groupes"></a>

(à des fins organisationnelles et statistiques)

azur vous permet d'organiser vos clients et fournisseurs selon un modèle hiérarchique. C'est également possible pour les articles qui seront traités dans le 3ème chapitre « La gestion d'entreprise ». Cela veut dire que chaque enregistrement peut être associé à une famille qui elle‐même peut être subdivisée en groupes et en sous-groupes. Vous pouvez ainsi attribuer des propriétés spécifiques (prix/code TVA/conditions de payement/…) à une famille, un groupe ou un sous‐groupe d'enregistrement au lieu d'attribuer ces propriétés à chaque enregistrement. Vous pouvez de même effectuer des opérations de recherche, faire afficher des statistiques (vente/achat/chiffre d'affaires/…).&#x20;

### Les clients <a href="#les-clients" id="les-clients"></a>

Pour gérer les **données des clients** (ajout, modification, suppression, consultation) il faut lancer le programme **321. Données clients** qui se trouve dans le menu 3.

![](<../.gitbook/assets/image (99).png>)

Dans le même menu vous trouvez les tables auxiliaires qui sont utilisées lors de l'encodage des données clients. Celles‐ci sont décrites ci‐dessous. Encodage des données clients. **Les données sont organisées sur 5 pages d'onglet et regroupées par catégories:**   \* **Page 1 signalétique**: informations qui servent à identifier client

![](<../.gitbook/assets/image (26).png>)

|**Options**|**Description**| |----|----| |Numéro du client | À la création d'un nouveau client le programme vous propose automatiquement un numéro client. Vous pouvez accepter celui‐ci ou vous pouvez le changer s'il ne convient pas.

_Le numéro du client est un champ obligatoire, vous ne pouvez pas continuer l'encodage sans avoir entré un numéro et appuyé sur Enter pour confirmer!_

|Code alphanumérique | Vous avez la possibilité d'attribuer un code alphanumérique aux clients. Ce code est destiné à l'usage interne et peut faciliter la recherche si vous utilisez toujours la même méthode pour générer ce code.| |Titre | Dans ce champ vous pouvez entrer l'abréviation du titre d'une personne physique ou morale. Le titre complet sera affiché à droite de ce champ. Par exemple : écrivez "M" pour Monsieur, "BQ" pour Banque, …. Vous pouvez ajouter vous‐même des couples abréviation/titre complet dans la table des personnalisations. _Ceci est expliqué plus en détail dans le chapitre II.1.c. Données comptables._| |Nom et raison sociale du client | Il est conseillé d'entrer le nom et le prénom des personnes physiques dans le champ 4.| |Numéro de TV | Ce champ est requis pour les sociétés luxembourgeoises, il sera repris par d'autres modules d'**azur**. | |No d'identification Intracommunautair | Ce champ est requis pour les sociétés qui opèrent sur le plan européen. D'autres modules d'**azur** ont recours à ce numéro. | |Langue Il suffit d'entrer le code Langue du client, appuyez sur F3 pour avoir une liste des codes disponibles. Le code langue est utilisé pour les correspondances avec le client. Si les textes pour la correspondance dans la table des textes existent dans la langue du client, le programme les choisira automatiquement. |Informations complémentaires | Ces champs sont facultatifs, ils vous permettent de stocker des informations complémentaires sur le client| |Client divers | **azur** permet de regrouper les opérations de vente comptant afin de ne pas surcharger le dossier comptable. Ceci permet aussi au client de ne pas laisser ses coordonnées lors d'une telle opération. Pour ce faire il faut créer un client (que vous pouvez appeler "Client Divers") et vous cochez la case "Client divers". Lors de la création de la facture vous pourrez indiquer un nom et une adresse de facturation si c'est nécessaire. Ceci sera expliqué plus en détail dans le chapitre IV.1.a.| |17‐26. Adresse et Boîte Postale | Les données que vous entrez pour les champs "Adresse" seront utilisées comme adresses de livraison et de facturation si vous ne l'indiquez pas autrement lors de la facturation. | |27-33 Communication | L'encodage de ces données est facultatif. Ces champs vous permettent de compléter les informations sur le client.|

**Page 2 Compta** : Contient les informations comptables du client

![](<../.gitbook/assets/image (52).png>)

|**Options**|**Description**| |----|----| |Type | Ils permettent d'identifier les clients, s'ils sont soumis ou non à la TVA … Cela se répercute sur les documents de vente, les déclarations intracommunautaires, etc. Pour changer les types du client, cliquez sur le bouton "Types du client". L'écran suivant apparaîtra alors.Pour associer un type avec le client cochez la case qui se trouve à gauche du type. Parmi les types sélectionnés il faut spécifier un et un seul type par défaut. Pour ce faire cliquez sur la case qui se trouve à droite du type. Si vous avez terminé cliquez sur le bouton "Valider" pour enregistrer les modifications.| |Devise| Choisissez la devise dans laquelle se font les échanges directs avec le client en question. En appuyant sur F3 vous aurez une liste avec les devises les plus courantes et leurs codes ISO respectifs. Sélectionnez une devise et cliquez sur le bouton valider.| |Code T.V.A.| Il s'agit du code T.V.A. qui sera appliqué aux transactions avec le client pour le calcul des documents de vente.Pour ajouter des valeurs pour la T.V.A. veuillez consulter le chapitre II.1.c...| |Comptes généraux| Un seul compte ou un choix entre plusieurs comptes centralisateurs identifie le client avec un n° de contrepartie des articles les plus vendus. Le centre de frais et le compte analytique sont des champs plus spécifiques à utiliser dans le cadre d'une comptabilité analytique|  



* **Page 3 Facturation** : Traite les informations sur la facturation des clients.

![](<../.gitbook/assets/image (37).png>)

|**Options**|**Description**| |----|----| |1-3. No famille, groupe et sous‐groupe | Entrez le numéro de famille, de groupe et de sous‐groupe du client ou appuyez sur F3 pour le sélectionner dans une liste. _Pour avoir plus d'informations sur l'organisation hiérarchique des clients veuillez consulter le chapitre II.2.d._| |4. Type prix | Pour choisir un type de prix entrez son numéro correspondant. Les numéros (de 1 à 6) se réfèrent aux prix des articles pour le numéro en question. Pour plus d'informations veuillez consulter le chapitre II.2.c.| |5. Article par défaut | Vous pouvez spécifier un article par défaut pour les clients qui achètent généralement le même article. Lors de la création d'une facture pour ce client l'article par défaut sera automatiquement proposé et vous n'avez plus qu'à indiquer la quantité. Remise par quantité Suivi rappel : Cochez la case pour générer automatiquement les rappels | |9-10. Texte accueil début/fin | Le texte accueil début sera affiché au-dessus des titres des colonnes, le texte accueil fin sera affiché en dessous des lignes de la facture. Vous avez aussi la possibilité de définir des textes accueil début/fin dans les paramètres du dossier, ceux‐là sont affichés dans tous les documents de vente indépendamment pour les textes définis pour un client. Pour choisir les textes appuyez sur F3 et sélectionnez‐le dans la liste. Vous pouvez ajouter et éditer vous‐même ces textes à afficher. _Pour ce faire veuillez consulter le chapitre II.1.c._| |16. Conditions de payement | Pour changer les conditions de payement appuyez sur F3 et sélectionnez les conditions appropriées dans la liste. Pour ajouter de nouvelles conditions de payement à la liste veuillez consulter le chapitre II.1.c. La valeur que vous entrez ici sera reprise comme proposition de la date d'échéance lors de la création de documents de vente.| |17. Mode de payement | Entrez le code du mode de payement ou appuyez F3 sur pour sélectionner un mode de payement dans la liste. _Type de facturation du client: 23,24 et 25 Entrez ici le code pour le paramétrage du type de facturation._|



* **Page 4 Intrastat** Ces données permettent au programme de compléter automatiquement les formulaires pour l'Intrastat. Voir 3ème partie de ce chapitre: Option déclarations intracommunautaires.



* **Page 5 Relations commerciales** Cette page d'onglet vous permet d'entrer les informations sur la personne de contact auprès d'une entreprise cliente.

![](<../.gitbook/assets/image (8).png>)

* **Page 9 Liste** Affiche en mode consultation la liste de tous les clients enregistrés. Si vous vous trouvez en mode recherche la liste contient uniquement les clients répondant à vos critères de recherche.

### Les fournisseurs

Pour gérer les données des fournisseurs (ajout, modification, suppression, consultation) il faut lancer le programme 331. (Données fournisseurs). Les champs à remplir pour les fournisseurs ont généralement la même signification que pour les clients. Le programme 331. (Données fournisseurs) s'utilise par conséquent de la même façon que le programme 321. (Données clients). Ce chapitre traite uniquement les particularités pour les fournisseurs. Afin d’obtenir des explications sur les autres champs veuillez consulter le chapitre précédent « Les clients ».



* **Page 1 Signalétique** - Informations qui servent à identifier le fournisseur.

![](<../.gitbook/assets/image (168).png>)



* **Page 2 Compta** : informations comptables du fournisseur

![](<../.gitbook/assets/image (154).png>)

Comme pour la page "Signalétique" les champs sont similaires Il faut seulement veiller à indiquer les comptes généraux adéquats pour les fournisseurs. En cliquant sur le bouton "Types du fournisseur" vous aurez l'écran suivant.

![](<../.gitbook/assets/image (169).png>)



* **Page 3 Facturation** : modes de payement et correspondance avec le fournisseur.

Cette page contient les champs à remplir pour les modes de payement, l'organisation hiérarchique et la correspondance personnalisée des fournisseurs. _Pour avoir plus d'informations sur les données à entrer veuillez consulter la partie sur la facturation du chapitre précédent «Les clients »._



* **Page 4 Intrastat** Ces données permettent au programme de compléter automatiquement les formulaires pour l'Intrastat _Voir 3ème partie de ce chapitre: Option déclarations intracommunautaires._



* **Page 5 Relations commerciales** Cette page d'onglet vous permet d'entrer les informations sur la personne de contact auprès du fournisseur.



* **Page 6 Liste** Affiche en mode consultation la liste de tous les clients enregistrés. Si vous vous trouvez en mode recherche la liste contient uniquement les clients répondant à vos critères de recherche.

### Les écritures et éditions comptables <a href="#les-ecritures-et-editions-comptables" id="les-ecritures-et-editions-comptables"></a>

#### **Les écritures de ventes et d’achats**

La manipulation des écrans d'encodage des écritures de vente et d'achat est identique, c’est la raison pour laquelle les écrans sont décrits ensemble dans ce manuel. Les écritures sont générées automatiquement lors de la création de factures, de bons d'achat/vente ou de notes de crédit. L'encodage manuel des écritures se fait dans les écrans des écritures décrits plus haut. Lorsque vous encodez manuellement une écriture pour laquelle il n'existe pas de facture correspondante, une facture est créée automatiquement avec le même montant, mais sans lignes d'articles.

#### **Encodage des écritures**

L'encodage des écritures de vente comprend l'entête de l'écriture et les lignes. Pour chaque écriture il faut d'abord remplir les champs de l'entête et valider ces données en appuyant sur le bouton

![](<../.gitbook/assets/image (10).png>)

Une fois l'entête validé il faut encoder les lignes dans la zone d'encodage des lignes et valider

![](<../.gitbook/assets/image (109).png>)

chaque ligne en cliquant sur le bouton. Pour valider le document vous devez cliquer sur le bouton qui se trouve en bas de l'écran des écritures de vente

![](<../.gitbook/assets/image (78).png>)

1. **Entête écriture** Après avoir lancé le programme cliquez sur le bouton "Ajouter/Chercher document" ou appuyez sur Enter. La zone d'encodage de l'entête devient active (voir image ci‐dessous) <img src="../.gitbook/assets/image (58).png" alt="" data-size="original">.
2. Le type de journal des ventes et le type de document doivent être choisis en appuyant sur **F3**.
3. Maintenant il faut choisir un journal des **ventes (No 1 en général)** et un type de document **(1 pour Facture, 2 pour Note de crédit, etc…).**
4. Dans le champ **No document** vous pouvez indiquer vous‐même le numéro du document en entrant le numéro et en appuyant sur **Enter** ou bien vous laissez le programme attribuer un numéro au document. **azur** se charge de créer la facture qui correspond à l'écriture de vente que vous êtes en train de faire. Celle‐ci sera enregistrée sous le numéro de document qui se trouve dans le champ **No document.**
5. Ensuite vous devez encore choisir un client à l’aide de la touche F3. Les valeurs par défaut qui se trouvent dans les enregistrements des clients vont être remplies dans les champs **Devise, Type client, Date document et Date échéance.**
6. Il faut entrer le montant TTC du document de vente dans le champ "Total document".
7. Le champ **Libellé** est facultatif, il sert à ajouter une remarque ou une référence à l'écriture comptable.
8. Après avoir vérifié les valeurs de l'entête vous pouvez cliquer sur le bouton Entête **OK** pour valider l'entête et pour passer à l'encodage des lignes du document.
9. **Encodage des lignes**

![](<../.gitbook/assets/image (55).png>)

![](<../.gitbook/assets/image (50).png>)

10\. Pour encoder une ligne des écritures de ventes, commencez par sélectionner le numéro du compte. En appuyant sur **F3** sur les champs **No compte** ou **Libellé** compte vous aurez une liste pour rechercher les comptes généraux.

11\. Après cela il faut indiquer le montant à comptabiliser sur ce compte. Par défaut le montant est traité comme montant HTVA. Si vous voulez entrer le montant TTC il faut ajouter le signe **"+"** à la fin du montant. (voir figure ci‐dessous)

12\. Pour gagner du temps il est possible d'entrer le signe **"+"** dans le champ **Montant**, dans ce cas le montant qui reste à comptabiliser sera attribué à la ligne en cours.

13\. Le champ **D/C** sert à indiquer si le montant doit être débité ou crédité.

14\. Le champ **Type client** contient toujours le type par défaut du client. Si le client admet plusieurs types, vous pouvez les choisir dans ce champ.

15\. Le champ **Libellé** sert à rajouter un commentaire pour la ligne que vous êtes en train d'encoder.

16\. Après avoir rempli tous les champs, vous devez cliquer sur le bouton **Ligne OK** pour passer à la ligne suivante. Au-dessus de la zone d'encodage des lignes se trouve le champ « **Reste à comptabiliser** » ![](<../.gitbook/assets/image (43).png>)Celui‐ci affiche à tout moment le montant qui n'a pas encore été comptabilisé ainsi que le **signe** du montant. Vous ne pouvez pas valider un document tant que la valeur de ce champ ne soit pas à 0 (zéro).

Les lignes que vous avez validées pour un document apparaissent dans la zone d'affichage des lignes du document (voir image ci‐dessous). Vous ne pouvez pas modifier directement ces lignes dans le tableau.

En dessous de ce tableau se trouve un autre tableau qui affiche la répartition des montants pour les codes TVA utilisés dans ce document. Ce tableau est affiché à titre indicatif et vous ne pouvez pas faire de modifications dans ces lignes.

![](<../.gitbook/assets/image (97).png>)

Répétez l'étape précédente pour toutes les lignes à encoder. Quand vous avez terminé l'encodage des lignes, cliquez sur le bouton **Valider document** qui se trouve dans la barre en bas de l'écran pour enregistrer l'écriture.<br>

![](<../.gitbook/assets/image (49).png>)

Pour annuler le document en cours, cliquez sur **Annuler document**.

Pour fermer l'écran des écritures d'achat, cliquez sur le bouton **Fin**.

### Consultation / modification d’écritures <a href="#consultation-modification-decritures" id="consultation-modification-decritures"></a>

Les étapes à suivre pour consulter une écriture comptable sont les suivantes: \* Cliquer sur le bouton **Ajouter/Chercher document** \* Entrer le numéro du journal dans le champ **No journal** et appuyer sur **Enter** \* Entrer le type du document dans le champ **Type** et appuyer sur **Enter** \* Entrer le numéro du document dans le champ **No document** et appuyer sur **Enter**, ou bien appuyer sur **F3** sur le champ "No document" et sélectionner le document dans l'écran de recherche.

Après cela le document sera affiché à l'écran.

Pour enlever toutes les lignes de l'écriture cliquez sur le bouton **Vider document** en bas de l’écran. Maintenant vous pouvez recommencer l'encodage des lignes de l'écriture.

![](<../.gitbook/assets/image (22).png>)

Pour modifier seulement quelques lignes, sélectionnez la ligne à modifier dans le tableau d'affichage des lignes et puis cliquez sur le bouton avec la fonction désirée (**Ajouter ‐, Modifier‐ ou Supprimer ligne**). (Voir image ci‐dessous).

![](<../.gitbook/assets/image (118).png>)

_Après cela vous procédez de la même façon que pour l'encodage des lignes. Pour terminer n'oubliez pas de valider la ou les lignes et de valider le document._

#### **Paramètres d’impression des documents de vente**

#### Après avoir ouvert un document existant, les boutons **Options, Aperçu et Imprimer** qui se trouvent en haut à droite de l'écran sont activés.

Le bouton **Options** vous permet de modifier les paramètres d'impression.

_Les paramètres que vous modifiez dans cet écran ne seront pas stockés, si vous fermez l'écran de facturation les paramètres par défaut seront rechargés. Les paramètres par défaut peuvent être définis dans l'écran **Paramètres du dossier**._

### Les opérations financières

![](<../.gitbook/assets/image (156).png>)

Afin d'encoder des opérations financières vous devez vérifier que les journaux financiers correspondent à vos comptes en banque existants. Dans le sous‐menu Table des journaux du menu Fichiers de base vous trouvez l'écran "Journaux des opérations financières". Dans cet écran vous pouvez consulter la liste des journaux financiers existants. Vous pouvez ajouter des journaux financiers dans cet écran.

![](<../.gitbook/assets/image (167).png>)

#### **Encodage des écritures**

L'encodage des écritures financières comprend deux étapes. L'encodage de l'entête nécessite le numéro du compte financier à utiliser, le numéro et la date de l'extrait ainsi que les soldes début et fin de l'extrait. Une fois remplies, les données de l'entête peuvent être encodées dans la zone d'encodage des lignes. Une fois terminé, et après que le montant restant à comptabiliser est de valeur nulle, vous pouvez valider l'enregistrement en cliquant sur le bouton situé en bas de l'écran.

![](<../.gitbook/assets/image (15).png>)

#### **Entête écriture**

* Après avoir cliqué sur le bouton **DMS**  , la zone d'encodage de l'entête devient active. (Voir image ci‐dessous).

![](<../.gitbook/assets/image (138).png>)

* Tout d'abord, veuillez entrer le numéro du journal financier. Si vous ne savez plus de quel numéro il s'agit, appuyez sur F3 pour sélectionner le journal dans la liste.
* Après cela le curseur se positionne sur le champ du numéro de l'extrait. Le numéro début est attribué automatiquement, en général il suffit d'appuyer sur Enter pour continuer. S'il s'agit d'un compte du type BCEE vous pouvez indiquer le numéro de la partie de l'extrait. Pour continuer vous devez indiquer le numéro de l'extrait fin.
* La date valeur de l'extrait est proposée en fonction des paramètres indiqués dans les données de base du journal financier (→ voir page XX ‐ programme: 3D3)
* Le solde début correspond au solde fin de l'extrait précédent, il est proposé par le programme. Dans le champ Solde fin vous devez entrer le solde fin du dernier extrait à encoder.
* Le champ Libellé est facultatif, il sert à faciliter l'identification de l'opération en cours.
* Après avoir rempli toutes les valeurs de l'entête il faut cliquer sur le bouton Entête Ok pour valider l'entête et pour passer à l'encodage des lignes de l'extrait.

#### **Encodage des lignes**

![](<../.gitbook/assets/image (38).png>)

![](<../.gitbook/assets/image (45).png>)

#### Opération de payement client/fournisseur: Indiquez le type (**"c"** ou **"f"**) dans le champ (a). Choisissez le client ou fournisseur dans les champs (b). À ce moment vous pouvez choisir le n° du document à traiter en cliquant sur la ligne correspondante dans la zone d'affichage des lignes. (→ voir image ci‐**dessous).**<br>

![](<../.gitbook/assets/image (47).png>)

Après avoir choisi le document vous pouvez encore ajuster le montant si nécessaire et pour valider la ligne vous devez cliquer sur le bouton **Détail**. En alternative vous pouvez choisir plusieurs documents en même temps et faire générer les lignes correspondantes par **azur**. Pour ce faire vous devez cliquer sur le bouton **Sélection**. Ceci vous affiche l'écran de sélection des documents.

![](<../.gitbook/assets/image (100).png>)

Dans cet écran vous devez cliquer sur les lignes pour sélectionner ou désélectionner les documents. Pour valider votre choix, cliquez sur le bouton **Valider sélection**. Ceci engendre la génération automatique des lignes d'extraits. Pour encoder un acompte, cliquez sur le bouton **Acompte**. Vous pouvez alors indiquer le montant de l'acompte et choisir la méthode à utiliser pour distribuer ce montant sur les documents ouverts.

![](<../.gitbook/assets/image (65).png>)

Quand vous avez terminé l'encodage de l'extrait, vous devez encore cliquer sur le bouton "Valider extrait" pour valider les données encodées. Si le montant "Reste à comptabiliser" n'est pas soldé, le programme vous propose les options suivantes: ![alt](https://docs.sitasoftware.lu/fiduciaires/fr/images/image105.png) Choisissez parmi les options et cliquez sur "OK" pour continuer.

* Opérations sur des comptes généraux:

Entrez "**g**" dans le champ (**a**). Choisissez le compte en cliquant sur **F3** dans le champ (b). Entrez le montant dans le champ (**d**) et indiquez s'il faut débiter ou créditer le compte. Pour valider la ligne, cliquez sur le bouton **Détail**.

### Les opérations diverses

![](<../.gitbook/assets/image (2).png>)

Avant de pouvoir encoder des opérations diverses il faut avoir créé un journal des opérations diverses dans l'écran 3D4. L'encodage des données est identique aux opérations financières. Seules changent les données qu'il faut indiquer dans l'entête. Cette partie du chapitre décrit donc uniquement l'encodage de l'entête des opérations diverses. _Pour avoir des détails sur l'encodage des lignes, veuillez-vous référer à la partie **encodage des lignes des opérations financières.**_ Entête écriture Pour commencer avec l'encodage des opérations diverses vous devez cliquer sur le bouton qui se trouve en bas à gauche.

![](<../.gitbook/assets/image (102).png>)

<br>

![](<../.gitbook/assets/image (98).png>)

Vous commencez par entrer le numéro du journal dans le champ prévu (**F3** pour avoir la liste des journaux) et vous confirmez avec la touche **Enter**. Par après il vous sera demandé d'entrer une valeur pour le numéro de l'opération diverse. En appuyant sur "Enter" le programme va attribuer automatiquement ce numéro. Pour continuer vous pouvez encore préciser la date de traitement et un libellé. Après avoir vérifié les données de l'entête il faut cliquer sur le bouton pour commencer avec l'encodage des lignes...

![](<../.gitbook/assets/image (5).png>)

### Les éditions comptables <a href="#les-editions-comptables" id="les-editions-comptables"></a>

Les écrans des éditions comptables possèdent une barre supplémentaire qui s'appelle **Barre des fonctions**, celle‐ci possède une série de boutons qui servent à lancer l'aperçu des rapports sélectionnés ainsi que la gestion des paramètres de l'écran.

![](<../.gitbook/assets/image (54).png>)

Les boutons **Aperçu** et **Imprimer** génèrent, en fonction de vos paramètres, le rapport pour la page d'onglet sélectionnée. Le bouton "Aperçu" affiche d'abord le rapport tel qu'il sera imprimé tandis que le bouton **Imprimer** lance directement l'impression. ‐ Si vous sauvegardez des paramètres en utilisant le bouton **Mes paramètres**, ils seront uniquement accessibles pour l'utilisateur qui les a créés. ‐ Si vous sauvegardez des paramètres en utilisant le bouton "Paramètres par défaut", ceux‐ci seront disponibles pour tous les utilisateurs. ‐ Les "Paramètres par défaut" sont les paramètres qui sont déjà en place au démarrage de l'écran. Si vous voulez changer les paramètres par défaut il faut d'abord effectuer les changements du paramétrage, ensuite vous devez cliquer sur le bouton "Paramètres par défaut". La prochaine fois que vous lancerez cet écran les nouveaux paramètres seront en place.

### Les écritures clients <a href="#les-ecritures-clients" id="les-ecritures-clients"></a>

![](<../.gitbook/assets/image (44).png>)

![](<../.gitbook/assets/image (150).png>)

### Informations générales <a href="#informations-generales" id="informations-generales"></a>

Cet écran se compose de trois zones distinctes, la zone de sélection des **clients, la barre des fonctions et les pages d'onglet.**

![](<../.gitbook/assets/image (170).png>)

Dans la zone de sélection des **clients**, vous pouvez indiquer le(s) client(s) à traiter. Cette sélection restera valable jusqu'à ce que vous la changiez ou bien que vous fermiez l'écran.

La zone des pages d'onglets contient les paramètres des rapports disponibles. Ceux-ci sont regroupés par type de rapport et se trouvent sur des pages d'onglet différents. Avant de lancer un rapport, il faut vérifier que vous avez bien sélectionné la page du rapport que vous voulez avoir. Pour sélectionner une page d'onglet, il faut cliquer sur l'onglet qui contient la désignation de la page.

Après cela, vérifier si les paramètres affichés correspondent bien à vos besoins. Si ce n'est pas le cas, modifiez-les. Afin de lancer le rapport, veuillez cliquer sur le bouton **Aperçu** ou **Imprimer**.

_Les boutons "Aperçu" et "Imprimer" lancent le rapport pour la page d'onglet sélectionnée ainsi qu'en fonction des paramètres spécifiés pour cette page._

Par la suite nous allons voir en détail les pages d'onglet contenus dans l'écran d'édition des écritures comptables.

#### **EXTRAIT DES COMPTES / HISTORIQUE**

![](<../.gitbook/assets/image (60).png>)

Ci‐dessus vous voyez la page d'onglet Extrait des **comptes / Historique**. En haut à gauche vous pouvez indiquer le ou les documents à traiter aussi bien par numéro de document/opération que par **date document** ou par **date de paiement**. Ceci est à utiliser au cas où vous cherchez des informations précises sur un certain nombre de documents. De même le temps de calcul est largement réduit par rapport au traitement de tous les documents. Comme paramètres vous disposez de plusieurs encadrés qui vous permettent d'adapter le traitement des documents à vos besoins spécifiques. Parmi ceux‐là il y a la sélection par échéance, la sélection par type et la sélection par solde. Echéance: Par défaut la sélection se fait sur tous les documents, dans ce cas vous voyez tous les postes ouverts des clients sélectionnés. L'option **Seulement les documents échus** vous permet de voir quel client est en retard avec ses payements. Solde documents: Par défaut seulement les documents non soldés sont affichés dans le rapport. En cochant l'option **Seulement les documents soldés**, vous pouvez voir quels documents ont été payés par les clients sélectionnés. **Tri de documents**: Ceci concerne l'ordre d'affichage des documents dans le rapport. Par défaut, le tri se fait d'après la **date** du document, puis par son **numéro d'opération**.

#### **RAPPEL**

La génération des rappels peut être entièrement automatisée dans **azur**. Pour avoir l'écran des rappels, lancez le programme **21 Ecritures clients** et cliquez sur l'onglet **Rappel**.

![](<../.gitbook/assets/image (174).png>)

Si vous lancez cet écran pour la première fois, il faut d'abord vérifier les options qui se trouvent dans la zone de paramétrage des rappels.

![](<../.gitbook/assets/image (84).png>)

Pour que les lettres de rappel sortent avec l'entête correspondant au numéro de rappel, il faut encore spécifier des entêtes et bas de page pour les 1er, 2ème, 3ème et Nième rappels. Pour ce faire, cliquez dans le champ qui se trouve à droite du nom **Entête** ou **Fin**, et appuyez sur la touche **F3** pour sélectionner le texte adéquat. Si vous n'avez pas encore de texte pour les entêtes ou les pieds-de-page, se reporter à la création des textes dans prog. **3K Tables de textes**. Une fois que vous avez bien paramétré l'écran des rappels il faut sauvegarder ces paramètres. Pour ce faire il faut cliquer sur le bouton qui se trouve dans la **barre de contrôle** à droite de l'écran.

#### **CHOIX DU MODE RAPPEL**

![](<../.gitbook/assets/image (117).png>)

**Une lettre par code rappel**: Pour un client donné, tous les documents qui correspondent au même code rappel seront regroupés dans la même lettre de rappel. Ainsi, le client recevra autant de lettres qu'il y a de codes rappel différents à son compte. **Une seule lettre avec le plus petit code rappel**: Tous les documents non soldés d'un client sont regroupés dans une même lettre avec l'entête du plus petit code rappel. **Une seule lettre avec le plus grand code rappel**: Tous les documents non soldés d'un client sont regroupés dans une même lettre avec l'entête du plus grand code rappel.

Après avoir fait les réglages pour la sélection des documents et des entêtes, il est conseillé de sauvegarder ces paramètres pour ne plus avoir à les encoder ultérieuremen&#x74;**.**

#### **GÉNÉRER LES LETTRES DE RAPPEL**

Après avoir paramétré les rappels, vous pouvez visualiser les lettres de rappel en cliquant sur le bouton aperçu.

![](<../.gitbook/assets/image (87).png>)

Le programme vous demandera ensuite de confirmer ou non la mise à jour des codes rappel. Si vous cliquez sur Oui, le nombre de rappels des documents sélectionnés seront incrémenté, le solde et la date du rappel seront mémorisés.

#### **GESTION DES CODES RAPPEL**

Vous pouvez consulter la liste des documents qui sont à échéance et ajuster manuellement le nombre et la date des rappels déjà envoyés pour ces documents. Ceci se fait dans l'écran de gestion des rappels. Pour ouvrir cet écran, cliquez sur le bouton **Initialiser, Modifier, Consulter les nombres et dates de rappels** qui se trouvent en bas de la page **Rappel**.

![](<../.gitbook/assets/image (12).png>)

gestion des rappels se présente de la façon suivante:

![](<../.gitbook/assets/image (157).png>)

La zone "Détail Document" affiche par défaut tous les documents qui sont arrivés à échéance et qui ne sont pas encore soldés. Pour limiter l'affichage à un nombre réduit de documents, vous pouvez inclure les numéros client et les dates document dans la sélection. Pour ce faire, entrez les numéros début et fin de la gamme des clients dont vous voulez afficher les documents. Procédez de la même façon pour la gamme des dates document.

Chaque ligne de la zone **Détail Document** représente un document.

![](<../.gitbook/assets/image (93).png>)

Les informations affichées par document sont les suivantes: **N° et nom client, N° Journal, Type document, N° et Date document, Date échéance, Montant, Solde, Devise document, Nombre de rappels** antérieurs ainsi que le solde et la date des rappels antérieurs. Comme la place disponible sur l'écran est limitée, vous devez utiliser la barre de défilement pour voir toutes les informations qui se trouvent dans une ligne.



1. **Initialisation et modification manuelle des codes rappel** Si vous voulez modifier manuellement le nombre de rappels d'un document, il faut d'abord sélectionner le ou les documents concernés dans la zone "Détail document" et puis il faut indiquer le nombre de rappels effectifs pour le ou les documents sélectionnés. La sélection des documents se fait en cliquant une fois avec le bouton gauche de la souris sur le document en question. La ligne concernée sera mise en évidence par un fond bleu. ![alt](https://docs.sitasoftware.lu/fiduciaires/fr/images/image122.png) Pour désélectionner un document, cliquez à nouveau sur la ligne bleue. Pour modifier le nombre de rappels des documents sélectionnés, vous devez utiliser le groupe de boutons qui se trouve à droite de la zone de "Détail document". Il suffit de cliquer sur un des boutons pour mettre à jour les codes rappel des documents sélectionnés. Attention: Cette mise à jour manuelle est prévue pour l'initialisation des codes rappel des documents. Par exemple si vous avez déjà envoyé des rappels pour certains documents sans passer par le module "Rappel" d'**azur** et vous voulez que le programme envoie par la suite les lettres de rappel avec les bons codes rappel pour les documents en question. Vous pouvez aussi modifier manuellement les codes rappel pour les autres documents, mais à ce moment vous devez être conscient du fait que les dates des rappels pour ces documents ne seront pas mises à jour.
2. **Annulation de la dernière mise à jour automatique des codes rappel** Si pour quelque raison vous deviez annuler en bloc la dernière mise à jour automatique des codes rappel, vous pouvez le faire dans la page d'onglet Annuler de l'écran de gestion des codes rappel. Pour avoir cette page il faut cliquer sur l'onglet "Annuler" qui se trouve en haut à gauche de l'écran de gestion des rappels.

![](<../.gitbook/assets/image (111).png>)

La page d'annulation comprend deux éléments, un champ qui affiche la date à laquelle a été effectuée la dernière mise à jour automatique des rappels et un bouton qui actionne l'annulation de cette mise à jour. L'annulation concerne tous les rappels que vous avez créés à cette date et heure.

## LES OPTIONS _Azur_ COMPTABILITÉ <a href="#les-options-azur-comptabilite" id="les-options-azur-comptabilite"></a>

### La gestion automatique des virements <a href="#la-gestion-automatique-des-virements" id="la-gestion-automatique-des-virements"></a>

![](<../.gitbook/assets/image (149).png>)

![](<../.gitbook/assets/image (80).png>)

Le module « Virements » d'**azur** a été conçu pour préparer les ordres de virement qui vont être envoyés à travers le programme « Multiline » de l'ABBL. azur vous propose, selon vos critères de sélection, les paiements à effectuer. Après avoir validé cette sélection, **azur** crée un fichier texte dans le format prévu par **Multiline**.

#### **Le paramétrage du dossier**

Avant tout, il faut encoder les comptes en banque de votre société dans **azur**. Ceux-ci doivent être enregistrés dans trois endroits différents. À savoir, dans les programmes respectifs: 1. **341 Table des comptes généraux** en tant que compte financier 2. **31 Paramètres dossier** : dont les données doivent être définies accordement comprenant limite de crédit, nom du détenteur du compte etc...). 3. **3D3 – Journal des opérations financières** : dans lequel il faut créer un journal financier correspondant et lier le compte financier et le compte en banque dossier à ce journal. Si vous encodez déjà vos opérations financières dans le programme **13. Opérations financières** vous n'avez plus besoin de créer les comptes financiers, ni les journaux financiers correspondants. Vous pouvez donc sauter l'étape n°1.

#### **Création d’un compte financier**

Le plan comptable fourni avec **azur** contient plusieurs comptes financiers qui contiennent comme libellé français le texte 'C/C BANQUAIRE'. Ces comptes peuvent servir de base pour vos propres comptes financiers. Vous n'avez plus qu'à remplacer le libellé par celui de votre compte en banque et à vérifier que la devise correspond bien à celle de votre compte.

![](<../.gitbook/assets/image (62).png>)

#### **Création d’un compte en banque pour votre dossier**

Pour commencer allez dans le programme **31. Paramètres du dossier**, puis dans la partie supérieure droite vous cliquez sur le bouton **Comptes en banque** pour avoir l'écran d'encodage des comptes en banque du dossier.

![](<../.gitbook/assets/image (136).png>)

1. Une fois l'écran de traitement des comptes dossier affiché, vous cliquez sur **Ajouter** et vous entrez un code pour identifier votre compte en banque et vous appuyez sur **Enter**.
2. Choisissez une banque (avec **F3**) et remplissez les autres champs (si vous connaissez le numéro de compte IBAN, vous n'avez plus besoin de remplir le champ **N° de compte banque**).
3. L'indication de la **limite de crédit** est facultative et peut être prise en compte lors des opérations de paiement.
4. Le champ **Ordre pour les virements** sert à modifier l'ordre d'affichage des comptes dans l'écran de création des virements.
5. Le champ **Etat** vous permet de préciser le type d'utilisation du compte. Par défaut la valeur est '0', si le compte doit seulement être utilisé pour les paiements client ou fournisseur, vous mettez les valeurs '1', respectivement '2'. Si le compte en banque n'existe plus ou ne doit plus être utilisé, vous ne devez pas le supprimer mais mettre l'état sur la valeur '9' (Supprimé). Dans les champs de l'adresse vous devez rentrer les coordonnées du titulaire du compte.
6. Quand vous avez terminé, l'écran devrait se présenter tel que sur l'image ci-contre.
7. **Fermez** à présent cet écran et validez l'écran des paramètres de dossier.

![](<../.gitbook/assets/image (108).png>)

Création du journal financier / lire les comptes à partir d'un journal Pour achever cette partie, nous avons encore besoin d'un journal financier par compte. Veuillez démarrer le programme **3D3. Journal des opérations financières**. _Pour ceux qui n'ont pas encore de journal financier, veuillez-vous référer à la partie Création de journal financier de ce manuel._

![](<../.gitbook/assets/image (151).png>)

Il s'agit ici de s'assurer que le champ **5. Numéro de compte financier** contienne le compte correct par rapport au journal. Il faut rajouter dans le champ **16. Code banque dossier** le code banque dossier. Il ne manque plus qu'à compléter le paramétrage de l'écran des virements: Démarrez le programme **42. Création virements** et cliquez sur l'onglet **Paramètres virements**.

![](<../.gitbook/assets/image (129).png>)

**azur** peut générer automatiquement les textes qui seront affichés dans les lignes de la communication du virement. **azur** reprend des informations concernant la facture, comme par exemple, la date ou le numéro. Comme il n'y a que 4 lignes à 35 caractères (par virement par bénéficiaire), il faudra indiquer au programme le nombre de factures pour lesquelles les informations détaillées seront affichées dans la communication. S'il y a plus de factures pour un même bénéficiaire, un autre texte (que vous pourrez spécifier à un autre endroit) sera affiché dans le champ **Communication du virement**. Le paramétrage de ces textes sera expliqué plus loin dans cette documentation. Par défaut ce nombre est fixé à 3, il reste alors une ligne de la référence pour afficher des informations comme par exemple le numéro d'ordre de virement. Les codes frais pour les virements (LUP) : \* **BEN =Bénéficiaire**\
&#xNAN;_**OUR = Donneur d'ordre** \* **SHA = Partagés** Les codes frais pour les domiciliations (LSL): \* **DEB = Débiteur**_\
**CRE = Créditeur**   Les textes figurant dans les champs **Identification pour virements** seront envoyés à la banque (fichier LUP) respectivement à la CETREL (fichier LSL) avec les fichiers Multiline. L'identification pour les banques doit contenir un nom court (16 caractères) pour votre société. Si vous faites des domiciliations avec **azur**, vous devez mettre le code à 10 chiffres qui vous a été donné par la Cetrel. Après avoir modifié des paramètres vous devez cliquer sur le bouton **Sauvegarder** dans la partie inférieure gauche de l'écran.

Pour configurer les textes générés pour les lignes de la communication vous devez cliquer sur l'onglet Textes par défaut.

![](<../.gitbook/assets/image (70).png>)

En cliquant sur le bouton **Recherche**, le programme va afficher les textes existant pour la combinaison de paramètres (Code langue, client ou fournisseur, type fichier, etc.) que vous avez choisie. Pour modifier par exemple le texte qui sera affiché dans la première ligne de la communication d'un ordre de virement, vous devez double-cliquer sur **Ligne référence no.1**

![](<../.gitbook/assets/image (57).png>)

Il s'agit ici d'un évaluateur de fonctions, c'est-à-dire un assistant qui vous permet de construire des chaînes de texte et de les formater selon certains critères. Exemple: Si vous voulez que le programme prenne le texte se trouvant dans la référence de la facture, qu'il mette ce texte en lettres majuscules en rajoutant le texte 'Réf.:' devant, qu'il rajoute des espaces derrière pour arriver à une longueur totale de 20 caractères et enfin qu'il découpe si le texte résultant dépasserait les 20 caractères. La formule résultante sera la suivante: **AjouteCharDevDer('Réf.:'+{REFERENCE},' ',20,True)** _L'élaboration de ces formules dépasse le cadre de ce chapitre et sera expliquée ailleurs en détail._

#### La préparation des comptes clients/ fournisseurs pour les virements <a href="#la-preparation-des-comptes-clients-fournisseurs-pour-les-virements" id="la-preparation-des-comptes-clients-fournisseurs-pour-les-virements"></a>

Pour pouvoir préparer les virements, le programme doit encore connaître le ou les comptes en banque de vos clients et de vos fournisseurs. Etant donné que le paramétrage pour les fournisseurs et les clients est identique, nous allons décrire uniquement la partie « Fournisseurs » dans ce manuel. Pour préparer les virements, démarrez le programme **331. Encodage des données fournisseurs**, ouvrez l'enregistrement du fournisseur pour lequel vous voulez rajouter un compte en banque et allez sur l'onglet **3. Facturation**

![](<../.gitbook/assets/image (110).png>)

Les champs 7 à 12 accueillent les données financières du fournisseur, les champs 10 et 11 sont là pour des raisons de compatibilité avec d'anciens programmes et ne seront pas pris en compte pour les virements automatiques. Assurez-vous que le champ **8. Mode de paiement** contient le code 'VIR' pour indiquer le mode de paiement par virement. Le champ **12. Escompte** est lié aux conditions de paiement du fournisseur, c'est-à-dire que le module virement va proposer automatiquement de déduire le montant de l'escompte si la facture est payée avant son échéance. Le champ **9. Code du compte** permet de gérer les comptes en banque des fournisseurs. Vous pouvez vous-même définir le code du compte, d'une longueur maximale de 6 caractères. En règle générale vous pouvez mettre le code de la banque, mais il n'y a pas de lien direct entre le code que vous mettez dans ce champ et la banque du fournisseur. Il est d'ailleurs possible que le fournisseur possède plusieurs comptes auprès de la même banque, que vous distinguerez alors avec des chiffres (p.ex. BGLL1 et BGLL2). Si vous devez rajouter un nouveau compte en banque pour un fournisseur, **entrez le code** dans ce champ et **confirmez** la création du compte. Vous aurez alors l'écran suivant:

![](<../.gitbook/assets/image (33).png>)

Dans le champ **3. Code banque**, insérez le code de la banque. S'il s'agit d'une banque luxembourgeoise, vous pouvez la sélectionner dans la liste qui s'affiche avec **F3**. Pour les banques étrangères, il est nécessaire de les créer une après l'autre. La création d'une banque sera expliquée plus loin.

_La création d'une banque est expliquée page 72._

* Après, indiquez le numéro de compte IBAN ou le numéro de compte normal.
* Dans le champ 6. Code paiement, mettez le code 'VIR'.
* Finalement, pour activer le compte, mettez un '0' dans le champ 7. Etat. (si le compte n'est plus utilisé par la suite, remplacez le 0 par un 9). Les champs sous **Adresse** ne sont qu'à rentrer si l'adresse du détenteur du compte diffère de celle du fournisseur. Au cas où vous devez créer une banque étrangère dans **azur**, vous devez vous assurer que vous disposez soit du code:
* SWIFT code
* d'un code banque tel que Code RIB, AT, BLZ, etc.
* ainsi que du nom et de l'adresse de la filiale

_En visitant le site http://www.swift.com vous pouvez éventuellement compléter les informations manquantes_ Par exemple pour BNP-Paribas à Metz, vous devez trouver un descriptif à 4 caractères (ex. BPMZ) pour cette succursale, puis appuyez sur **Enter** et le programme vous propose de créer et d'enregistrer cette banque. Dans l'écran suivant, vous devez rentrer le nom de la banque, ainsi que, si possible, son adresse. Le champ **12. Code Cetrel** sert uniquement pour les domiciliations et vous permet de regrouper les banques pour lesquelles les domiciliations se font à travers la Cetrel.

![](<../.gitbook/assets/image (152).png>)

L'encodage du code SWIFT est subdivisé dans ses 4 parties, à savoir: 1. 4 caractères pour le code banque 2. 2 caractères pour le code pays 3. 2 caractères pour le code ville 4. 3 caractères pour l'agence Une fois l'encodage des données de la banque terminé et validé; vous pouvez continuer avec le reste de l'encodage du compte en banque fournisseur. La banque créée est désormais connue par **azur**. Au prochain encodage de compte pour cette banque, vous pourrez la choisir parmi les autres banques dans la base de données d'**azur**.  

### La création du fichier virement

Une fois que vous avez paramétré votre dossier pour les virements, vous pouvez passer à la création des virements via le programme **42. Création virements**.

![](<../.gitbook/assets/image (143).png>)

Le programme fait la distinction entre deux catégories de bénéficiaires qui sont les clients et les fournisseurs.

Pour les fournisseurs, vous ne disposez que du type fichier 'LUP' pour les virements, tandis que pour les clients, il est autant possible de réaliser des virements (fichier LUP) que des ordres de domiciliations (fichier LSL).\
<br>

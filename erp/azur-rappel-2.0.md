# Azur rappel 2.0

## Présentation <a href="#presentation" id="presentation"></a>

Azur Rappel 2.0 est conçu pour vous permettre:

* De gérer vos rappels au jour le jour.
* Une gestion simplifiée du traitement des documents.
* D'"automatiser" la génération des rappels.

### Ecran Azur Rappel 2.0 <a href="#ecran-azur-rappel-20" id="ecran-azur-rappel-20"></a>

L'écran d'Azur Rappel 2.0 se compose de 4 onglets:

1. Paramètres.
2. Propositions.
3. Historique.
4. Service.

#### Paramètres <a href="#parametres" id="parametres"></a>

L'onglet Paramètres vous permets de:

* Gérer les paramètres de sélections des clients et des documents.
* Réaliser une proposition de rappel sur base des paramètres.

#### Propositions <a href="#propositions" id="propositions"></a>

L'onglet Proposition vous permets de:



* Visualiser les propositions en cours.
* Sélectionner /désélectionner un/des clients(s) de la proposition.
* Sélectionner /désélectionner un/des document(s) de la proposition.
* Lancer la génération des rappels sur base de la proposition.

#### Historique <a href="#historique" id="historique"></a>

L'onglet Historique vous permet de visualiser et de traiter les rappels.

#### Service <a href="#service" id="service"></a>

L'onglet Service permet de configurer un service pour qu'il génère automatiquement une proposition de rappel sur base des paramètes préalablement enregistrés.

### Paramètres <a href="#parametres_1" id="parametres_1"></a>

L'onglet paramètres permet de choisir les paramètres:

* De sélection client (Parite suppérieure de l'écran)
* De sélection des documents (Partie inférieure de l'écran)

![](<../.gitbook/assets/image (177).png>)

#### Sélection client <a href="#selection-client" id="selection-client"></a>

La partie Sélection client permet de choisir les clients qui ferront partie de la proposition.

![](<../.gitbook/assets/image (222).png>)



| Paramètre                                      | Descriptions                                                                            |
| ---------------------------------------------- | --------------------------------------------------------------------------------------- |
| N° client de ... à                             | Permet de spécifier le/les clients.                                                     |
| Nom client de ... à                            | Permet de spécifier le/les clients.                                                     |
| Adr fact. de ... à                             | Permet de spécifier une plage d'adresse de facturation.                                 |
| Adr livr. de ... à                             | Permet de spécifier une plage d'adresse de livraison.                                   |
| Tri des clients                                | Ordre dans lequel appartaitront les clients dans la proposition et les rappels générés. |
| Rupture de page suivant adresse de facturation | Si coché, un document de rappel sera généré par adresse de facturation.                 |
| Rupture de page suivant adresse de livraison   | Si coché, un document de rappel sera généré par adresse de livraison.                   |
| Sélection client                               | Permet de spécifier une sélection de client.                                            |
| Rétablir                                       | Réinitialiser les différents champs de saisie.                                          |

{% hint style="info" %}
Info

* Laisser vide pour ne pas utiliser.
* La liste des paramètres peut évoluer.
{% endhint %}

#### Sélection document <a href="#selection-document" id="selection-document"></a>

La partie Sélection document permet d'affiner la rechercher des documents à inclure dans la proposition.

![](<../.gitbook/assets/image (200).png>)



| Paramètre                                              | Descriptions                                                                                                                                                                                                                                                                         |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Date traitement                                        | Est la date qui va servir de référence pour le calcul des documents échux.                                                                                                                                                                                                           |
| N° document de ... à                                   | Permet de spécifier le/les documents.                                                                                                                                                                                                                                                |
| Date document de ... à                                 | Permet de spécifier une plage de date de document.                                                                                                                                                                                                                                   |
| Date de paiement de ... à                              | Permet de spécifier une plage de date de paiement.                                                                                                                                                                                                                                   |
| <p><strong>Délais avant</strong><br>1er Rappel</p>     | Nombre de jour entre la date d'échéance et le 1er Rappel.                                                                                                                                                                                                                            |
| <p><strong>Délais avant</strong><br>2ième Rappel</p>   | Nombre de jour entre le 1er et le 2ième Rappel.                                                                                                                                                                                                                                      |
| <p><strong>Délais avant</strong><br>3ième Rappel</p>   | Nombre de jour enre le 2ième et le 3ième Rappel.                                                                                                                                                                                                                                     |
| <p><strong>Délais avant</strong><br>4ème Rappel</p>    | Nombre de jour entre le 3ième et le 4ième Rappel.                                                                                                                                                                                                                                    |
| <p><strong>Délais avant</strong><br>Rappel suivant</p> | <p>Nombre de jour entre le 4ième et le Xième.<br>Rappel Nombre de jour entre le X et Xième +1 Rappel.</p>                                                                                                                                                                            |
| <p><strong>Délais avant</strong><br>Recouvrement:</p>  | Nombre de jour entre le rappel Max et le Recouvrement.                                                                                                                                                                                                                               |
| Montant Minimum:                                       | Est le montant Minimum que doit atteindre le rappel pour être dans la proposition.                                                                                                                                                                                                   |
| Recouvrement après X Rappel:                           | Défini le nombre maximum de rappel avant Recouvrement.                                                                                                                                                                                                                               |
| N° de reppport                                         | Permet de spécifier le report Azur à utiliser pour la génération des Rappels.                                                                                                                                                                                                        |
| Nb jour avant annulation auto                          | Est le nombre de jour qui défini la validité d'une proposition de rappel précédement crée.                                                                                                                                                                                           |
| **Sélection/ clients**                                 | Seulemenet ceux avec un total échu positif.                                                                                                                                                                                                                                          |
| **Sélection/ clients**                                 | Seulemenet ceux avec un total général positif.                                                                                                                                                                                                                                       |
| **Sélection/ clients**                                 | Ajouter documents non échus.                                                                                                                                                                                                                                                         |
| **Mode rappel**                                        | <p><strong>Une lettre par code rappel</strong><br>Pour un "client" donné, tous les documents qui correspondent au même code rappel seront regroupés dans la même lettre de rappel. Ainsi, le client recevra autant de lettres qu'il y a de codes rappel différents à son compte.</p> |
| **Mode rappel**                                        | <p><strong>Une seule lettre avec le plus petit code rappel</strong><br>Tous les documents d'un "client" sont regroupés dans une même lettre avec l'entête du plus petit code rappel.</p>                                                                                             |
| **Mode rappel**                                        | <p><strong>Une seule lettre avec le plus grand code rappel</strong><br>Tous les documents d'un "client" sont regroupés dans une même lettre avec l'entête du plus grand code rappel.</p>                                                                                             |
| Tri des documents                                      | Ordre dans lequel appartaitront les documents dans la proposition et les rappels générés.                                                                                                                                                                                            |

{% hint style="success" %}
Tip

Pour plus d'information concernant le **recouvrement client**, vous pouvez consulter le site de [justice.public.lu](https://justice.public.lu/fr/creances/recouvrement-creances.html) .
{% endhint %}

{% hint style="info" %}
Info

* Nous utilisons _client_ entre " car il ne s'agit pas toujours du client proprement parlé mais cela peut varier suivant le regroupage effectué dans la partie [Sélection client](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#selection-client).
* Laisser vide pour ne pas utiliser.
* La liste des paramètres peut évoluer.
{% endhint %}

#### Actions <a href="#actions" id="actions"></a>

Dans la partie de droite, vous avez les différentes actions.



| Actions                                                                                                                      | Descriptions                                                                                                |
| ---------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| ![image bouton Load Mes paramètres](https://docs.sitasoftware.lu/erp/fr/images/btn_load_mes_parametres.png)                  | [Mes paramètres (charger)](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#mes-parametres-charger)           |
| ![image boutn  Load paramètres standard](https://docs.sitasoftware.lu/erp/fr/images/btn_load_parametres_standard.png)        | [Paramètres standard (charger)](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#parametres-standard-charger) |
| ![image boutn  Load paramètres service](https://docs.sitasoftware.lu/erp/fr/images/btn_load_parametres_service.png)          | [Paramètres service (charger)](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#parametres-service-charger)   |
| ![image bouton Enregistrer mes paramètres](https://docs.sitasoftware.lu/erp/fr/images/btn_save_mes_parametres.png)           | [Mes paramètres (sauver)](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#mes-parametres-sauver)             |
| ![image bouton Enregistrer paramètres standard](https://docs.sitasoftware.lu/erp/fr/images/btn_save_parametres_standard.png) | [Paramètres standard (sauver)](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#parametres-standard-sauver)   |
| ![image bouton Enregistrer paramètres défaut](https://docs.sitasoftware.lu/erp/fr/images/btn_save_parametres_defaut.png)     | [Paramètres défaut (sauver)](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#parametre-defaut-sauver)        |
| ![image bouton Enregistrer paramètres service](https://docs.sitasoftware.lu/erp/fr/images/btn_save_parametres_service.png)   | [Paramètres service (sauver)](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#parametres-service-sauver)     |
| ![image bouton Générer proposition](https://docs.sitasoftware.lu/erp/fr/images/btn_proposition.png)                          | [Générer proposition](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#generer-proposition)                   |

{% hint style="success" %}
Tip

La liste des actions est susceptible d'évoluer au fil du temps.
{% endhint %}

**Mes paramètres (charger)**

Permet de charger mes paramètres préalablement enregistrés.

**Paramètres standard (charger)**

Permet de charger les pramètres standard préalablement enregistrés.

**Paramètres service (charger)**

Permet de charger les paramètres "service" préalablement enregistrés.

**Mes paramètres (sauver)**

Permet d'enregistrer mes paramètres.

**Paramètres standard (sauver)**

Permet d'enregistrer les paramètres comme paramètres "standard".

**Paramètres défaut (sauver)**

Permet d'enregistrer les paramètres comme paramètres "par défaut".

**Paramètres service (sauver)**

Permet d'enregistrer les paramètres comme paramètres pour une génération par service.

{% hint style="success" %}
Tip

Azur Rappel 2.0 permet aux utilisateurs d'enregistrer des jeux de paramètres et de les planifier pour une exécution automatique. Dès lors, il est possible d'automatiser des proposition de rappel. Exemple: Il sera possible de demander à Azur de générer une proposition de Rappel tous les jours à 7H30 pour les clients qui sont dans une sélection et qui ont un document échu.
{% endhint %}

[Plus d'infos](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#service_1)

**Générer proposition**

Permet de générer une proposition manuellement sur base des paramètres.

{% hint style="info" %}
Info

Une fois la proposition générée, l'utilisateur sera dirigé vers l'onglet "Propositions".
{% endhint %}

### Propositions <a href="#propositions_1" id="propositions_1"></a>

![](<../.gitbook/assets/image (269).png>)

#### Proposition en cours <a href="#proposition-en-cours" id="proposition-en-cours"></a>

Dans la partie de gauche, vous retrouvez la liste des propositions qui sont toujours "En cours" dans le système.

#### Liste des clients <a href="#liste-des-clients" id="liste-des-clients"></a>

Dans la partie supérieure du milieu de l'écran, vous avez la liste des clients (triés et regroupés suivant les paramètres utilisés pour générer la proposition).

#### Liste des documents <a href="#liste-des-documents" id="liste-des-documents"></a>

Dans la partie inférieure du milieu de l'écran, vous avez la liste des documents pour le client actif dans la "Liste des clients".

#### Actions <a href="#actions_1" id="actions_1"></a>

Dans la partie de droite, vous avez les différentes actions.



| Actions                                                                                                             | Descriptions                                                                                        |
| ------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![image bouton Report](https://docs.sitasoftware.lu/erp/fr/images/btn_report.png)                                   | [Report](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#report)                                     |
| ![image boutn Annuler propostion](https://docs.sitasoftware.lu/erp/fr/images/btn_annuler_propostion.png)            | [Annuler proposition](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#report)                        |
| ![image bouton Message client](https://docs.sitasoftware.lu/erp/fr/images/btn_message_client.png)                   | [Message client](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#message-client)                     |
| ![image bouton Gestion liasse](https://docs.sitasoftware.lu/erp/fr/images/btn_gestion_liasse.png)                   | [Gestion liasse](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#gestion-liasse)                     |
| ![image bouton Plus de rappel client](https://docs.sitasoftware.lu/erp/fr/images/btn_plus_de_rappel_client.png)     | [Plus de rappel (client)](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#plus-de-rappel-client)     |
| ![image bouton Générer Rappels](https://docs.sitasoftware.lu/erp/fr/images/btn_generer_rappels.png)                 | [Générer Rappels](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#generer-rappels)                   |
| ![image bouton Plus de rappel document](https://docs.sitasoftware.lu/erp/fr/images/btn_plus_de_rappel_document.png) | [Plus de rappel (document)](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#plus-de-rappel-document) |

{% hint style="success" %}
Tip

La liste des actions est susceptible d'évoluer au fil du temps.
{% endhint %}

**Report**

Permet de visualiser un report avec l'ensemble de la proposition avant de générer les rappels

{% hint style="info" %}
Info

Un exemplaire de ce report sera automatiquement généré et enregistré dans le DMS lors de la validation de la propostion. Cet exemplaire sera consultable via l'onglet "Historique".
{% endhint %}

**Annuler proposition**

Permet simplement d'annuler une proposition

**Message client**

![](<../.gitbook/assets/image (275).png>)

Permet à l'utilisateur de saisir un message qui sera transmis au client si le rappel est envoyé par email.

{% hint style="info" %}
Info

Le texte sera ajouté dans la section "TEXTE\_LIBRE" de l'email envoyé au client.
{% endhint %}

{% hint style="info" %}
Info

Cette action est aussi réalisable dans l'onglet historique.
{% endhint %}

**Gestion liasse**

Permet à l'utilisateur de constituer une liasse de documents à inclure en pièce jointe lors de l'envoi du rappel par email. [Plus d'infos](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#gestion-liasse_2)

**Plus de rappel (client)**

Permet de configurer le **client** pour qu'il ne reçoive plus de rappel. Il sera toujours possible de chager cette modification via le programme 321. Le client sera toujours visible dans la propostion, les rappels ne seront pas générés pour lui.

**Générer Rappels**

Permet de générer les rappels sur base de la propostion.

{% hint style="warning" %}
Warning

Cette action modifiera le status de la propostion. Un service va prendre le relais et générer les rappels. Une fois que celui-ci aura terminé, l'utilisateur sera redirigé vers l'onglet Historique. De plus, le service envera une notification à chaques étapes. Cette notification sera visible dans le volet "Log" de l'écran.

Le service génèrera les rappels dans le DMS du/des client(s). Le traitement des documents qui sont générés par le service se fait dans la partie [Historique](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#historique_1)
{% endhint %}

![Illustration du volet "Log"](<../.gitbook/assets/image (183).png>)

**Plus de rappel (document)**

Permet de configurer le **document** pour qu'il ne reçoive plus de rappel. Le document sera toujours visible dans la propostion, les rappels ne seront pas générés pour lui.

#### Sélection - Désélection <a href="#selection-deselection" id="selection-deselection"></a>

![](<../.gitbook/assets/image (240).png>)

Permet de sélectionner - désélectionner **automatiquement** tous les "clients" de la proposition.

#### Légende <a href="#legende" id="legende"></a>

![](<../.gitbook/assets/image (296).png>)



* Sélectionné: en vert, les "clients" **sélectionné** dans la proposition pour la génération des rappels.
* Non sélectionné: en jaune, les "clients" **non sélectionné** dans la proposition pour la génération des rappels.
* Pas de rappel: en rouge, les "clients" qui sont **enlevés** de la proposition. (Le client ou le document est taggé "plus de rappel").

### Historique <a href="#historique_1" id="historique_1"></a>

![](<../.gitbook/assets/image (348).png>)

#### Liste des propositions <a href="#liste-des-propositions" id="liste-des-propositions"></a>

Dans la partie de gauche de l'écran, vous trouverez la liste des propositions validées

* Ok: reprend les propositions validées corretement traitées par le service, c'est à dire les propositions qui ont générés les rappels
* En cours: reprend les propositions qui doivent être traitées par le service de génération des rappels
* En erreur: reprend les propositions qui ont eu un soucis dans le service de génération des rappels
* Annulé: reprend les protpositions qui ont été annulées

#### Détail - client <a href="#detail-client" id="detail-client"></a>

Dans la partie centrale supérieur, vous trouverez une ligne par client / groupement.

Une ligne correspond à un document "Rappel".

{% hint style="warning" %}
Warning

Il se peut qu'il y ait plusieurs ligne par client. En effet, cela dépendra des paramètres qui ont été utilisés pour générer la proposition de rappel.
{% endhint %}

#### Liste des documents / clients <a href="#liste-des-documents-clients" id="liste-des-documents-clients"></a>

Dans la partie inférieure du milieu de l'écran, vous avez la liste des documents pour le client actif dans la partie "Détail - client".

Il s'agit de la liste des documents qui figureront dans le document "Rappel".

#### Actions <a href="#actions_2" id="actions_2"></a>

Dans la partie de droite, vous avez les différentes actions.



| Actions                                                                                                   | Descriptions                                                                                     |
| --------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| ![image bouton voir proposition](https://docs.sitasoftware.lu/erp/fr/images/btn_voir_proposition.png)     | [Voir proposition](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#voir-proposition)              |
| ![image bouton voir rappel](https://docs.sitasoftware.lu/erp/fr/images/btn_voir_rappel.png)               | [Voir rappel](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#voir-rappel)                        |
| ![image bouton Message client](https://docs.sitasoftware.lu/erp/fr/images/btn_message_client.png)         | [Message client](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#message-client_1)                |
| ![image bouton Gestion liasse](https://docs.sitasoftware.lu/erp/fr/images/btn_gestion_liasse.png)         | [Gestion liasse](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#gestion-liasse_1)                |
| ![image bouton Imprimer](https://docs.sitasoftware.lu/erp/fr/images/btn_imprimer.png)                     | [Imprimer](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#imprimer-imprimer-selection)           |
| ![image bouton Imprimer sélection](https://docs.sitasoftware.lu/erp/fr/images/btn_imprimer_selection.png) | [Imprimer sélection](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#imprimer-imprimer-selection) |
| ![image bouton Email](https://docs.sitasoftware.lu/erp/fr/images/btn_email.png)                           | [Email](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#email-email-selection)                    |
| ![image bouton Email sélection](https://docs.sitasoftware.lu/erp/fr/images/btn_email_selection.png)       | [Email sélection](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#email-email-selection)          |
| ![image bouton Edition email](https://docs.sitasoftware.lu/erp/fr/images/btn_email_edition.png)           | [Edition email](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#edition-email)                    |
| ![image bouton eInvoicing](https://docs.sitasoftware.lu/erp/fr/images/btn_einvoicing.png)                 | [eInvoicing](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#einvoicing)                          |
| ![image bouton Regénérer Rappels](https://docs.sitasoftware.lu/erp/fr/images/btn_regenerer_rappel.png)    | [Regénérer Rappels](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#regenerer-rappels)            |

{% hint style="success" %}
Tip

La liste des actions est susceptible d'évoluer au fil du temps.
{% endhint %}

**Voir proposition**

Permet de visualiser la proposition validée via un pdf enregistré dans le DMS.

**Voir rappel**

Permet de visualiser le document "Rappel" pour la ligne active dans "Détail - client".

**Message client**

![](<../.gitbook/assets/image (311).png>)

Permet à l'utilisateur de saisir un message qui sera transmis au client si le rappel est envoyé par email.

{% hint style="info" %}
**Info**

Le texte sera ajouté dans la section "TEXTE\_LIBRE" de l'email envoyé au client.
{% endhint %}

**Gestion liasse**

Permet à l'utilisateur de constituer une liasse de documents à inclure en pièce jointe lors de l'envoi du rappel par email. [Plus d'infos](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#gestion-liasse_2)

**Imprimer - Imprimer sélection**

Pour l'impression, deux possibilités s'offrent à vous:

1. Sélectionnez l'imprimante souhaitée et cliquer sur imprimer ou imprimer sélection.
2. Cocher exportation, définir l'emplassement et clique sur imprimer ou imprimer sélection.

Si vous cliquez sur imprimer sélection, la liste des clients sélectionnés (CTRL + CLICK) dans la liste "Détail - client" seront traités.

**Email - Email sélection**

Pour l'envoi des rappels par email, le programme d'eInvoicing sera démarré en **arrière plan**. Toute la configuration du programme d'eInvoincing sera utilisés pour envoyer l'email:

* L'adresse email d'expédition
* Le contenu de l'email
* Les informations du serveur mail
* ...

**Edition email**

Cette action va vous permettre d'éditer la/les adresses emails du client actif dans la liste "Détail - client".

{% hint style="info" %}
**Info**



Le programme eInvoicing va être chargé automatiqument, l'utilisateur va arriver sur la page de gestion de l'annuaire simplie, le client sera déja chargé.&#x20;

Vous pourrez définir cet écran:

* L'adresse email du client
* L'adresse email du client spécifique pour les documents (Factures, Bon de livraison,...)
* L'adresse email du client pour l'envoi des rappels
{% endhint %}

![](https://docs.sitasoftware.lu/erp/fr/images/annuaire_simple.png)

**eInvoicing**

Cette action va charger l'écran eInvoincing en mode Rappel 2.0 et chargera automatiquement la proposition de rappel.

![](<../.gitbook/assets/image (304).png>)

**Regénérer Rappels**

Cette action vous permet, en cas de soucis, de regénérer les rappels de la proposition active dans la liste "Historique".

### Gestion liasse <a href="#gestion-liasse_2" id="gestion-liasse_2"></a>

La gestion liasse permet à l'utilisateur de regrouper un ensemble de document qui seront ajouté à l'email envoyé au client avec le rappel.

![](<../.gitbook/assets/image (326).png>)

#### Desctription <a href="#desctription" id="desctription"></a>

Dans la grille de gauche de l'écran, vous pouvez voir la liste des documents qui seront joint à l'email de rappel (en plus du PDF de rappel). Dans la grille de droite, vous pouvez voir la liste des documents DMS du client.

#### Actions <a href="#actions_3" id="actions_3"></a>

Dans la partie de droite, vous avez les différentes actions.



| Actions                                                                                                | Descriptions                                                                  |
| ------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------- |
| ![image bouton Fichier Local](https://docs.sitasoftware.lu/erp/fr/images/btn_liasse_fichier_local.png) | [Fichier Local](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#fichier-local) |
| ![image bouton Visaliser Ligne](https://docs.sitasoftware.lu/erp/fr/images/btn_liasse_visualiser.png)  | [Visualiser Ligne](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#voir-ligne) |
| ![image bouton Factures / Nc](https://docs.sitasoftware.lu/erp/fr/images/btn_liasse_facture.png)       | [Factures / Nc](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#factures-nc)   |
| ![image bouton Supprimer](https://docs.sitasoftware.lu/erp/fr/images/btn_liasse_supprimer.png)         | [Supprimer](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#supprimer)         |
| ![image bouton Annuler](https://docs.sitasoftware.lu/erp/fr/images/btn_liasse_annuler.png)             | [Annuler](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#annuler)             |
| ![image bouton Valider](https://docs.sitasoftware.lu/erp/fr/images/btn_liasse_valider.png)             | [Valider](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#valider)             |

{% hint style="success" %}
**Tip**

La liste des actions est susceptible d'évoluer au fil du temps.
{% endhint %}

### Service <a href="#service_1" id="service_1"></a>

Dans l'onglet service, vous avez la possibilité de configurer vos jeux de paramètres préalablement enregistrés

![](<../.gitbook/assets/image (307).png>)

#### Liste des services <a href="#liste-des-services" id="liste-des-services"></a>

Dans la partie centrale, vous trouvez:

* La liste des parametètres enregsitrés ainsi que leur status (Actif).
* La planification prévue
* L'email de la/les personne(s) qui seront notifiées par email.

#### Actions <a href="#actions_4" id="actions_4"></a>

Dans la partie de droite, vous avez les différentes actions.

#### &#x20;<a href="#liste-des-services" id="liste-des-services"></a>

| Actions                                                                                               | Descriptions                                                                              |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| ![image bouton Planifier](https://docs.sitasoftware.lu/erp/fr/images/btn_service_planifier.png)       | [Planifier](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#planifier)                     |
| ![image bouton Activer](https://docs.sitasoftware.lu/erp/fr/images/btn_service_activer.png)           | [Activer / Désactiver](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#activer-descativer) |
| ![image bouton Destinataire](https://docs.sitasoftware.lu/erp/fr/images/btn_service_destinataire.png) | [Destinataire](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#destinataire)               |
| ![image bouton Supprimer](https://docs.sitasoftware.lu/erp/fr/images/btn_service_renommer.png)        | [Renommer](https://docs.sitasoftware.lu/erp/fr/rappel.fr/#Renommer)                       |

{% hint style="success" %}
Tip

La liste des actions est susceptible d'évoluer au fil du temps.
{% endhint %}

**Planifier**

Permet de planifier à quel moment le service devra exécuter le jeu de paramètres pour générer une proposition de rappel.

![](<../.gitbook/assets/image (336).png>)

{% hint style="warning" %}
Warning

Azur adaptera automatiquement les secondes avec \*.
{% endhint %}

**Activer / Désactiver**

Permet d'activer ou de désactier un jeu de paramètres.

**Destinataire**

Permet de saisir une adresse email à notifer lorsque la proposition de rappel aura été générée par le service

{% hint style="success" %}
Tip

Pour notifier plusieurs adresses email, vous pouvez les séparer par un point-virgule.

Exemple: adresse1@sitasoftware.lu;adresse2@sitasoftware.lu
{% endhint %}

**Renommer**

Permet de renomer le jeu de paramètres.

![Vidéo](<../.gitbook/assets/image (292).png>)

### Les données ne seront enregistrés que lorsque l'utilisateur cliquera sur valider!Release note <a href="#release-note" id="release-note"></a>

* Version 1, mai 2021 MFI

# Introduction

## Les écritures et éditions comptables

### Les écritures de vente et d'achats

La manipulation des écrans d'encodage des écritures de vente et d'achat est identique, c’est la raison pour laquelle les écrans sont décrits ensemble dans ce manuel.



![](<../.gitbook/assets/image (42).png>)

Les écritures sont générées automatiquement lors de la création de factures, de bons d'achat/vente ou de notes de crédit. L'encodage manuel des écritures se fait dans les écrans des écritures décrits plus haut. Lorsque vous encodez manuellement une écriture pour laquelle il n'existe pas de facture correspondante, une facture est créée automatiquement avec le même montant, mais sans lignes d'articles.

### Encodage des écritures

\
Après avoir lancé le programme cliquez sur le bouton _Ajouter/Chercher_ document ou appuyez sur Enter. La zone d'encodage de l'entête devient active (voir image ci‐dessous).<br>

![](<../.gitbook/assets/image (133).png>)



* Le type de journal des ventes et le type de document doivent être choisis en appuyant sur F3.
* Maintenant il faut choisir un journal des ventes (No 1 en général) et un type de document (1 pour Facture, 2 pour Note de crédit, etc…).
* Dans le champ No document vous pouvez indiquer vous‐même le numéro du document en entrant le numéro et en appuyant sur Enter ou bien vous laissez le programme attribuer un numéro au document. azur se charge de créer la facture qui correspond à l'écriture de vente que vous êtes en train de faire. Celle‐ci sera enregistrée sous le numéro de document qui se trouve dans le champ No document.
* Ensuite vous devez encore choisir un client à l’aide de la touche F3. Les valeurs par défaut qui se trouvent dans les enregistrements des clients vont être remplies dans les champs Devise, Type client, Date document et Date échéance.
* Il faut entrer le montant TTC du document de vente dans le champ "Total document".
* Le champ Libellé est facultatif, il sert à ajouter une remarque ou une référence à l'écriture comptable.
* Après avoir vérifié les valeurs de l'entête vous pouvez cliquer sur le bouton Entête OK pour valider l'entête et pour passer à l'encodage des lignes du document.

### Encodage des lignes <a href="#encodage-des-lignes" id="encodage-des-lignes"></a>

![](<../.gitbook/assets/image (175).png>)

Pour encoder une ligne des écritures de ventes, commencez par sélectionner le numéro du compte. En appuyant sur F3 sur les champs No compte ou Libellé compte vous aurez une liste pour rechercher les comptes généraux. • Après cela il faut indiquer le montant à comptabiliser sur ce compte. Par défaut le montant est traité comme montant HTVA. Si vous voulez entrer le montant TTC il faut ajouter le signe "+" à la fin du montant. (voir figure ci‐dessous) • Pour gagner du temps il est possible d'entrer le signe "+" dans le champ Montant, dans ce cas le montant qui reste à comptabiliser sera attribué à la ligne en cours. • Le champ D/C sert à indiquer si le montant doit être débité ou crédité. • Le champ Type client contient toujours le type par défaut du client. Si le client admet plusieurs types, vous pouvez les choisir dans ce champ. • Le champ Libellé sert à rajouter un commentaire pour la ligne que vous êtes en train d'encoder. • Après avoir rempli tous les champs, vous devez cliquer sur le bouton Ligne OK pour passer à la ligne suivante. Au-dessus de la zone d'encodage des lignes se trouve le champ _Reste à comptabiliser_

![](<../.gitbook/assets/image (162).png>)

Celui‐ci affiche à tout moment le montant qui n'a pas encore été comptabilisé ainsi que le signe du montant. Vous ne pouvez pas valider un document tant que la valeur de ce champ ne soit pas à 0 (zéro). Les lignes que vous avez validées pour un document apparaissent dans la zone d'affichage des lignes du document (voir image ci‐dessous). Vous ne pouvez pas modifier directement ces lignes dans le tableau. En dessous de ce tableau se trouve un autre tableau qui affiche la répartition des montants pour les codes TVA utilisés dans ce document. Ce tableau est affiché à titre indicatif et vous ne pouvez pas faire de modifications dans ces lignes. Répétez l'étape précédente pour toutes les lignes à encoder. Quand vous avez terminé l'encodage des lignes, cliquez sur le bouton Valider document qui se trouve dans la barre en bas de l'écran pour enregistrer l'écriture.

![](<../.gitbook/assets/image (161).png>)

Pour annuler le document en cours, cliquez sur Annuler document.

Pour fermer l'écran des écritures d'achat, cliquez sur le bouton Fin.

### _Les éditions compatbles_

Les écrans des éditions comptables possèdent une barre supplémentaire qui s'appelle Barre des fonctions, celle‐ci possède une série de boutons qui servent à lancer l'aperçu des rapports sélectionnés ainsi que la gestion des paramètres de l'écran.

![](<../.gitbook/assets/image (6).png>)

_-_ Les boutons _Aperçu et Imprimer_ génèrent, en fonction de vos paramètres, le rapport pour la page d'onglet sélectionnée. Le bouton _Aperçu_ affiche d'abord le rapport tel qu'il sera imprimé tandis que le bouton _Imprimer_ lance directement l'impression.

‐ Si vous sauvegardez des paramètres en utilisant le bouton _Mes paramètres_, ils seront uniquement accessibles pour l'utilisateur qui les a créés.

‐ Si vous sauvegardez des paramètres en utilisant le bouton _Paramètres par défaut_, ceux‐ci seront disponibles pour tous les utilisateurs.

‐ Les _Paramètres par défaut_ sont les paramètres qui sont déjà en place au démarrage de l'écran. Si vous voulez changer les paramètres par défaut il faut d'abord effectuer les changements du paramétrage, ensuite vous devez cliquer sur le bouton "Paramètres par défaut". La prochaine fois que vous lancerez cet écran les nouveaux paramètres seront en place.

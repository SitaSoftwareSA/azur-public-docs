# Inventaire

### Release note <a href="#release-note" id="release-note"></a>



| Date         | Note                                                       |
| ------------ | ---------------------------------------------------------- |
| Octobre 2020 | MFI, Terminer, clôturer et valider des inventaires en lots |

### Préparation de l'inventaire <a href="#preparation-de-linventaire" id="preparation-de-linventaire"></a>

Pour préparer votre inventaire vous pouvez sortir une liste d’inventaire par emplacement (avec ou sans code-barres). _L’avantage d’utiliser la version avec code-barres est de pouvoir faire le relevé de l’inventaire dans des zones hors connexion comme par exemple des frigos ou des congélateurs. Vous pourrez utiliser les codes-barres pour encoder les quantités depuis un bureau ou une zone de travail plus confortable._

![](<../.gitbook/assets/image (239).png>)

{% hint style="warning" %}
_Warning_

Uniquement disponible en utilisant les emplacements.
{% endhint %}

Exemple d’étiquette de produit dans le stock. Grâce à cette étiquette qui peut être disposée dans votre stock vous gagnerez du temps pour le rangement, l’expédition et l’inventaire.

![](<../.gitbook/assets/image (271).png>)

{% hint style="warning" %}
_Warning_

Uniquement disponible en utilisant les emplacements.


{% endhint %}

### Créer un inventaire <a href="#creer-un-inventaire" id="creer-un-inventaire"></a>

Avant de créer un inventaire vous devez choisir l’emplacement dans lequel vous aller faire votre inventaire. Pour choisir un emplacement, vous pouvez utiliser la méthode manuelle ou utiliser le mode graphique. Pour utiliser le mode graphique, cliquez sur le bouton bleu.

![](<../.gitbook/assets/image (186).png>)

![](<../.gitbook/assets/image (253).png>)

![](<../.gitbook/assets/image (192).png>)

{% hint style="info" %}
_Info_



Si vous n’utilisez pas les emplacements dans votre stock

* vous pouvez faire votre inventaire en choisissant code emplacement -1.
* L’inventaire ne vous proposera pas les quantités attendues par produit/emplacement
{% endhint %}

![](<../.gitbook/assets/image (248).png>)

Lors de la création d’un inventaire, le programme va générer des mouvements par rapport à l’emplacement de l’inventaire choisi. _Pour rappel si vous n’utilisez pas les emplacements, le programme ne vous génèrera pas de données._

### Inventaire <a href="#inventaire_1" id="inventaire_1"></a>

Lors de la création d’un inventaire, l’utilisateur sera automatiquement redirigé vers la page « inventaire encours ». Pour rentrer dans un inventaire / changer de zone, allée,; positionnez-vous dessus et cliquer sur « Continuer inventaire ». Pour se positionner dessu&#x73;_:_

![](<../.gitbook/assets/image (214).png>)

![](<../.gitbook/assets/image (266).png>)

![](<../.gitbook/assets/image (236).png>)

Une fois dans l’inventaire encours, vous visualisez:

* le nombre de produit à scanner / nombre de produit attendus ainsi que le pourcentage d’avancement (0/52) 0.00%
* Les derniers enregistrements.

Si vous utilisez les emplacements, vous devez spécifier l’emplacement dans lequel vous êtes. Cette opération permettra de vérifier que l’association produit – emplacement est correcte (Scannez l’emplacement ou cliquez sur le bouton bleu ciel). L’emplacement devient Vert, cela veut dire que vous êtes bien dans un « enfant » de l’emplacement général de votre inventaire encours. À nouveau ici 0/1, cela veut dire que le programme s’attend à un produit dans cet emplacement. Si vous cliquez sur détail, vous pouvez consulter les produits attendus dans l’emplacement scanné

![](<../.gitbook/assets/image (259).png>)

![](<../.gitbook/assets/image (180).png>)

#### Sacnning Article <a href="#sacnning-article" id="sacnning-article"></a>

![](<../.gitbook/assets/image (228).png>)

Une fois le produit scanné (ou recherché via F3) et trouvé dans le système le programme vous montre : - le code-barres scanné / N° de série - l’article et son libellé - la quantité attendue - la valeur (prix de revient \* quantité) Si vous utilisez les articles unités conversions (1Carton = 20 pièces), vous pouvez saisir: - soit encoder un nombre de carton - soit un nombre de pièce - soit une quantité totale Dans le cas contraire, vous pouvez saisir: - Une quantité totale

![](<../.gitbook/assets/image (260).png>)

#### Nombre de produit <a href="#nombre-de-produit" id="nombre-de-produit"></a>

Vous pouvez saisir le nombre de produit ou scanner plusieurs fois le produit pour cumuler les quantités. Une fois que le nombre est correctement saisi, cliquez sur « Valider »

![](<../.gitbook/assets/image (202).png>)

**Produit à poids variable**

![](<../.gitbook/assets/image (264).png>)

Pour un produit à poids variable, vous pouvez saisir le poids cumulé ou cliquez sur la calculatrice. Si le produit est correctement configuré, la calculatrice sera automatiquement visible. Dans le cas contraire, pour visualiser la calculatrice, cliquez sur le bouton « Poids variable ».

<br>

![](<../.gitbook/assets/image (263).png>)

Si vous cliquez sur la calculatrice, vous pourrez scanner des étiquettes, le programme décodera le poids. Cliquez sur « valider » pour retourner les valeurs.

![](<../.gitbook/assets/image (270).png>)

#### Importation d'un fichier pour inventaire <a href="#importation-dun-fichier-pour-inventaire" id="importation-dun-fichier-pour-inventaire"></a>

Vous avez la possibilité d’importer un fichier pour alimenter votre inventaire. Pour importer un fichier, il faut:

![](<../.gitbook/assets/image (189).png>)

Sur la droite de l’écran, vous pouvez voir un bouton «Import fichier».

![](<../.gitbook/assets/image (215).png>)

Cliquer sur le bouton « Charger fichier » pour l’ajouter dans la liste des fichiers à importer. L’extension du fichier doit être .Xls La structure du fichier doit être la suivante : A=N° article B=Libelle C=Qte carton D=Qte pc E=Poids Kg F=Emplacement Cette structure est susceptible de changer, veuillez-vous référez à la structure indiquée dans le programme. Elle sera mise à jour. Une fois que vous avez sélectionné vos fichiers, cliquer sur « importer fichier(s) »

![](<../.gitbook/assets/image (256).png>)

Le fichier importé, vous visualisez ce qui sera importé. Le bouton contrôle avant import permet de vérifier si l’emplacement mentionné dans le fichier existe bien dans la base de donnée. Si les données affichées vous conviennent, vous pouvez cliquer sur « valider l’importation », le programme va générer les mouvements de stock.

#### Association produit emplacement ne correspond pas <a href="#association-produit-emplacement-ne-correspond-pas" id="association-produit-emplacement-ne-correspond-pas"></a>

![](<../.gitbook/assets/image (254).png>)

Si le programme constate que l’emplacement du produit ne correspond pas à l’emplacement encours, le programme affiche un message « Attention l’emplacement de l’article ne correspond pas ! Cliquez pour pouvoir valider ». Il faut cliquer sur le message pour pouvoir valider.

{% hint style="info" %}
Info

Ce contrôle est réaliser que si vous travaillez avec un n° de série dans votre stock.
{% endhint %}

#### Voir inventaire en cours <a href="#voir-inventaire-en-cours" id="voir-inventaire-en-cours"></a>

Cette partie permet de visualiser les dernières opérations de l’inventaire encours.

#### Scan encours / Modif <a href="#scann-encours-modif" id="scann-encours-modif"></a>

Permet de voir les dernières opérations faites par un utilisateur ou par soi-même et de corriger un encodage précédemment fait.

#### Validation de l'inventaire <a href="#validation-de-linventaire" id="validation-de-linventaire"></a>

![](<../.gitbook/assets/image (226).png>)

Vous pouvez terminer un inventaire sans pour autant le valider. Cette opération vous permet de figer l’inventaire sans pour autant avoir des conséquences sur votre stock. Vous pouvez également en profiter pour visualiser votre inventaire via les statistiques.

![](<../.gitbook/assets/image (209).png>)

**Terminer inventaire**

C'est uniquement pour qu'un utilisateur puisse dire au système qu'il a fini sa partie. L'inventaire poura toujours être édité.

**Valider inventaire**

Cette action est pour un responsable, l'inventaire sera validé, il ne pourra plus être édité.

**Cloturer inventaire**

Enfin Clôturer votre inventaire. Pour pouvoir clôturer votre inventaire vous serez invité à saisir : - Le stock sera recalculé après cette opération - Un mot de passe - Une référence

{% hint style="info" %}
**Info**

Cette référence est important, elle vous servira plus tard pour

* Visualiser un inventaire validé
* Si vous attribuez la même référence à deux inventaires, ils seront cumulés dans les statistiques. Si vous faite un inventaire par zone mais que vous voulez avoir un total pour tout l’inventaire, vous pouvez mettre comme référence la date du jour.
{% endhint %}

![](<../.gitbook/assets/image (258).png>)

**Comparere 2 inventaires**

![](<../.gitbook/assets/image (232).png>)

**Statistiques**



* Préparation d’inventaire
* Liste des articles à scanner trié par emplacement
* Liste des articles à scanner trié par emplacement avec code-barres
* Visualisation d’inventaire
* Par rapport à un n° d’inventaire vous pouvez visualiser les quantités introduites par emplacement ainsi que la quantité attendue
* Comparaison d’inventaire
* Par rapport à une référence donnée lors de la clôture d’inventaire, vous pourrez comparer 2 inventaires.

**Export**

Azur vous permet d’exporter votre inventaire vers Excel. Ci-dessous le contenu disponible de l’export.

![](<../.gitbook/assets/image (193).png>)

* N° article et désignation
* Emplacement, emplacement produit
* Quantité physique, poids physique, unité
* Poids - pièce Valeur
* Quantité parent, unité parent, quantité supplémentaire et conversion \*

{% hint style="info" %}
**Info**

* Ces données sont exploitables uniquement en utilisant les articles unités conversions.
{% endhint %}

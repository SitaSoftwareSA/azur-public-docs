# Azur Toolkit



### Release note <a href="#release-note" id="release-note"></a>

* Version 1, aout 2021 MFI
* Version 2, septembre 2021, correction pour initialiser une grille [correction](https://docs.sitasoftware.lu/formation/fr/toolkit.fr/#pour-initialiser-une-grille)
* Version 3, septembre 2021 ajout création Intervention [plus d'info](https://docs.sitasoftware.lu/formation/fr/toolkit.fr/#creation-dune-intervention)
* Version 4, novembre 2021 ajout de la maps [plus d'info](https://docs.sitasoftware.lu/formation/fr/toolkit.fr/#Azur-Maps)
* Version 5, janvier 2022 ajout création document Azur [plus d'info](https://docs.sitasoftware.lu/formation/fr/toolkit.fr/#creation-dun-document)

### Présentation <a href="#presentation" id="presentation"></a>

Bienvenue dans la partie Formation dédiée à Azur Toolkit, autrement appelé Azur Scripteur

Le scripteur d'azur permet de faire des programmes sur mesures. Ces programmes sont intégrés dans la base de donnée et ne demande pas une recompilation d'Azur pour fonctionner!

### Azur Toolkit <a href="#azut-toolkit" id="azut-toolkit"></a>

Pour créer un scripteur, rendez-vous dans le programme 3S1 d'Azur

![](.gitbook/assets/toolkit_premier_script.gif)

Azur ToolKit se présente comme ceci

![](<.gitbook/assets/image (337).png>)



| Légende |                                                       |
| ------- | ----------------------------------------------------- |
| 1       | Fenêtre principale du programme                       |
| 2       | Palette des outils (palette des composants)           |
| 3       | Permet de switcher entre le design et le code (F12)   |
| 4       | Proriétés de l'oblet "actif" dans la forme            |
| 5       | Liste de évenenments de l'oblet "actif" dans la forme |
| 6       | Permet d'enregistrer (CTRL + s)                       |
| 7       | Pour exécuter le script                               |

{% hint style="success" %}
Tip

Lorsque vous êtes dans le code, vous pouvez faire appel à l'auto completion avec le raccourci CTRL + espace.
{% endhint %}

#### Import / export un script <a href="#import-export-un-script" id="import-export-un-script"></a>

Pour importer, exporter un script d'une DB vers une autre, veuillez faire l'opération suivante

![](.gitbook/assets/toolkit_import_export.gif)



**Exporter**

* Dans le 3S1 cliquer droit sur le script à exporter
* Export to Zip for release
* Répondre **NON** à la question

**Importer**

* Dans le 3S1 cliquer droit sur le script à exporter
* Importer Zip from Release
* Répondre **OUI** à la question

{% hint style="info" %}
Info

Si lors de votre import, vous avez le message d'erreur suivant, veuillez simplement choisir un répertoire temporaire plus proche de la racine de votre disque dur
{% endhint %}

![](<.gitbook/assets/image (295).png>)

#### Les bases de la programmation <a href="#les-bases-de-la-programmation" id="les-bases-de-la-programmation"></a>

**Convention**

Ci-dessous les conventions de programmation que nous avons fixé et que nous nous efforçons tant que possible de respecter.

{% hint style="info" %}
Info

Nous utilisons le camCase pour écrire le code, le nom des variables, le nom des fonctions et le nom des procédures.
{% endhint %}



| Variable Type              | Prefix | Exemple  |
| -------------------------- | ------ | -------- |
| globales                   | gl     | glUser   |
| private                    | pv     | pvUser   |
| protected                  | pt     | ptUser   |
| public                     | pb     | pbUser   |
| published                  | ps     | psUser   |
| local                      | lc     | lcUser   |
| local within method        | lclc   | lclcUser |
| constant                   | co     | coUser   |
|                            |        |          |
| variable d'entrée          | e      | eUser    |
| variable d'entrée éditable | o      | oUser    |

Exemple code Blocks

```
function GetUserName(const eUserNbr:Integer; var oDateTime:TDateTime):String
var 
  lcx:Integer;

  function GetDummy:String;
    var 
      lclcX:Integer; 
    begin
      result:='Dummy';
    end;

begin
  oDateTime:=now;
  for lcx:=0 to self.componentcount -1 do            
    begin
      If lcx=0
      then begin

           end
      else If lcx=1
           then begin
                  If GetDummy='Dummy'
                  then showmessage('OK');
                end
           else Beep;                        
    end;
end; 
```

**La condition Si**

Pour exécuter une portion de code qui doit réaliser une opération selon qu’une condition soit remplie, il faut écrire un bloc IF – THEN. SI lcNom est blanc alors on affiche vide

```
var
  lcNom:String;
begin
  lcNom := '';
  if (lcNom='')  
  then begin
         ShowMessage('Vide');
       end;
end;              
```

{% hint style="info" %}
Info

Ces deux codes donnent le même résultat

```
if (lcNom='')  
then begin
        ShowMessage('Vide');
    end;       
    
    
if (lcNom='')  
then ShowMessage('Vide');
```
{% endhint %}

**La condition Si - sinon**

Pour exécuter une portion de code qui doit réaliser une opération selon qu’une condition soit remplie ou non, il faut écrire un bloc IF – THEN-ELSE.

```
var
  lcNom:String;
begin
  lcNom := '';
  if (lcNom='')  
  then begin
         ShowMessage('Vide');
       end
  else begin
         ShowMessage(lcNom);
       end;     
end;              
```

Une procédure exécute une portion de code et ne retourne aucune valeur. Elle peut prendre en paramètre une ou plusieurs variables.

**SANS PARAMÈTRES**

```
procedure HelloWorld;
begin
  ShowMessage('Hello world!');
end;              
```

**AVEC PARAMÈTRES**

```
procedure AfficherMessage(eMessage:string);
begin
  ShowMessage(eMessage);
end;              
```

**Les fonctions**

Une fonction exécute une portion de code et renvoie un résultat une fois celle-ci terminée. Elle peut prendre en paramètre une ou plusieurs variables

```
function NombrePlusUn(eNombre:Integer):Integer;
begin
  result := eNombre +1;
end;              
```

#### Les variables Azur <a href="#les-variables-azur" id="les-variables-azur"></a>

Ci-dessous la liste des variables Azur les plus souvent utilisées



| Variable                      | Description                                                       |
| ----------------------------- | ----------------------------------------------------------------- |
| dossierAzur                   | Objet Dossier Azur                                                |
| dossierAzur.NoDossier         | Contient le n° de dossier encours dans Azur                       |
| periodeAzur                   | Objet Périore Azur                                                |
| periodeAzur.NoPeriode         | Contient le n° de la période encours dans Azur                    |
| utilisateurAzur               | Objet Utilisateur Azur                                            |
| utilisateurAzur.NoUtil        | Contient le n° de l'utilisateur connecté dans Azur                |
| utilisateurAzur.NomUtil       | Contient le nom de l'utilisateur connecté dans Azur               |
| utilisateurAzur.CodeLangue    | Contient le code de la langue de l'utilisateur connecté dans Azur |
| utilisateurAzur.NoRole        | Contient le n° du role de l'utilisateur connecté dans Azur        |
| utilisateurAzur.NoFamille     | Contient le n° de la famille de l'utilisateur connecté dans Azur  |
| utilisateurAzur.NoGroupe      | Contient le n° de groupe de l'utilisateur connecté dans Azur      |
| utilisateurAzur.NoSousGroupe  | Contient le n° du sous groupe de l'utilisateur connecté dans Azur |
| utilisateurAzur.InterbaseName | Contient le nom Firebird de l'utilisateur connecté dans Azur      |
| idDatabase                    | N° de l'id database (SOCIETE.ID\_DATABASE)                        |

{% hint style="danger" %}
**Warning**

À utiliser avec précaution!
{% endhint %}

#### La liste des procédures et fonctions <a href="#la-liste-des-procedures-et-fonctions" id="la-liste-des-procedures-et-fonctions"></a>

Pour visualiser la liste des procédures et fonctions "Système", vous pouvez, dans le code, faire le raccourci clavier ALT + F1.

![](<.gitbook/assets/image (320).png>)

Grâce à cette aide, vous pouvez connaitre

* les fonctions/procédures disponibles
* les paramètres d'entrées
* l'unité (uses) à éventuellement déclarer pour pouvoir les utiliser

#### Les F3s <a href="#les-f3s" id="les-f3s"></a>

Pour utiliser un F3 dans le scripteur

Utiliser un composant de type TSitaAllInOneEdit, le TSitaAllInOneEdit est un dérivé du composant TEdit.

```
Uses
  /*
  ...
  */
  unitSitaAllInOneEdit;

  /*
  Dans l'initialisation du programme (en général dans le OnShow ou OnCreate de la forme, on fait appel à une procédure initCompo)
  */
procedure initCompo;
begin
  //Permet d'utilise les SitaAllInOneEdit
  InitialiserSitaValidEdit(self, ['moEnter','moUp','moDn'], False, True, False, FormMenu.FocusComponent1,-1,F3DynAzur,True,False,False ); 

  monSitaAllInOneEdit.F3NoCode := 667;
  monSitaAllInOneEdit.F3NomTable := 'CODE_PAYS';
  monSitaAllInOneEdit.F3ButtonEnabled := True;   //--> Affiche la petite loupe

  //Si on veut passer des paramètres à notre F3
  monSitaAllInOneEdit.F3queryParams := 'NOM_DU_PARAMETRE_1='+LaValeur1EnString +#10+ 'NOM_DU_PARAMETRE_2='+LaValeur2EnString;

end;
```

#### Messages <a href="#messages" id="messages"></a>

Pour une facilité de traduction, nous avons développé les SitaMessages ci-dessous un exemple de sitaMessage

**Messages de validation**

```
uses UnitSitaDialogs;

procedure AfficherMessage(eParametre,eParametreDeux:String);
begin
  SitaMessageDlg(3084201,Utilisateur.CodeLangue,IB_Connection,'"'+eParametre+'","'+eParametresDeux+'"','Mon message avec le parametre 1 %s et le parametre 2 %s ', mtInformation, [mbOk], 0);
end;
```

{% hint style="info" %}
**Info**


{% endhint %}

| Type           | Illustration                                                                                          |
| -------------- | ----------------------------------------------------------------------------------------------------- |
| mtInformation  | ![ecran dyn 2.0](https://docs.sitasoftware.lu/formation/fr/images/toolkit_message_mtInformation.png)  |
| mtConfirmation | ![ecran dyn 2.0](https://docs.sitasoftware.lu/formation/fr/images/toolkit_message_mtConfirmation.png) |
| mtError        | ![ecran dyn 2.0](https://docs.sitasoftware.lu/formation/fr/images/toolkit_message_mtError.png)        |
| mtWarning      | ![ecran dyn 2.0](https://docs.sitasoftware.lu/formation/fr/images/toolkit_message_mtWarning.png)      |

**Messages de choix**

```
uses UnitSitaDialogs;

procedure AfficherMessage(eParametre,eParametreDeux:String);
begin
  if SitaMessageDlg(3085201,UtilisateurAzur.CodeLangue, IBTransactionScript.IB_Connection ,nil,'Voulez-vous continuer?',mtconfirmation,[mbyes,mbno],0)=mryes
  then begin
         ShowMessage('L''utilisateur a cliqué sur oui');
       end
  else begin
         ShowMessage('L''utilisateur a cliqué sur non');
       end;     
end;
```

Dans cet exemple 3084201 est un identifiant unique qui permet de d'enregistrer le message dans la base de donné.

{% hint style="info" %}
**Info**



* Les messages sont enregistrés automatiquement dans la base lors du premier appel ! Si vous modifiez un message par la suite dans le code, il ne sera pas changé dans DB!
* La table est ECRAN\_MESSAGE
{% endhint %}

**Get Message - GetMsgFromDb**

```
uses UnitSitaDialogs;

GetMsgFromDb(3205201,UtilisateurAzur.CodeLangue,IB_Connection,'Ceci est un message enregistré dans la base ');
```

#### Report du 2A dans le scripteur <a href="#report-du-2a-dans-le-scripteur" id="report-du-2a-dans-le-scripteur"></a>

```
uses UnitFonctionString, UnitSitaReports; 

procedure VoirReport(eGuid:string); 
var       
  lcString:TSTrings;   
begin
 try  
   lcString := TStringList.Create;    
   //Paramètres du report dans le 2A
   lcString.Values['Z_NO_DOSSIER'] := DossierAzur.NoDossier;
   lcString.Values['NO_UTIL']      := intToStr(UtilisateurAzur.NoUtil);                                                                        
   FormatList4Fastreport(lcString);                     
   SitaReportingGuid(IBTransactionScript.IB_Connection ,
                     StrToInt(DossierAzur.NoDossier),                                                                                                                                   
                     eGuid,
                     'Droits',
                     UtilisateurAzur.NoUtil,                                                                                                                  
                     '-1',          
                     UtilisateurAzur.Codelangue,                                      
                     '' ,                       
                     lcString,              
                     False,      
                     1,  //1 pour voir, 0 pour impression directe
                     1,
                     -1,
                     -1,
                     False); 
  finally
   lcString.Free;                                                                                                                          
  end;    
end;                                                         

procedure Button1Click(Sender: TObject);
begin
  VoirReport('CB7E686C-7ADC-4E1B-86F9-A5BA52F96CE7');  //Guid du report
end;
```

{% hint style="info" %}
**Info**



* Nous utilisons un Guid pour être certain de pointer vers le bon report. Cela nous permet d'avoir le report n° 10 chez le client A qui est complètement différent du report n° 10 chez le client B
*   Pour trouver le GUID à utiliser, vous pouvez exécuter la requête suivante

    ```
       SELECT GUID FROM REPORTING WHERE NO_REPORT=:NO_REPORT_FROM_2A; 
    ```
{% endhint %}

#### Les écrans dynamique 2.0 dans le scripteur <a href="#les-ecrans-dynamique-20-dans-le-scripteur" id="les-ecrans-dynamique-20-dans-le-scripteur"></a>

Dans cette rubrique, nous allons voir comment faire un appel à un écran dynamique

**Écran dynamique simple**

```
uses UnitFormDyn;

procedure LancerEcranDynamique(eGuid:string);               
begin      
  EcranDynamiqueGuid( nil ,F3DynAzur.IB_Connection,nil,eGuid,UtilisateurAzur.NoRole,UtilisateurAzur.NoUtil,nil,False).ShowModal;                                                                                                                             
end;          

procedure Button1Click(Sender: TObject);
begin
  LancerEcranDynamique('BC2F2290-1AB6-4845-9C44-9B3260010B83'); 
end;  
```

**Écran dynamique avec paramètre**

```
uses UnitFormDyn;

procedure RunOptions(eGuid:String);                         
var
  lcEcranDynParams:TFormDyn2; 
  lcParams:TStringList;               
begin      
  lcEcranDynParams:=EcranDynamiqueGuid( nil ,F3DynAzur.IB_Connection,nil,eGuid,UtilisateurAzur.NoRole,UtilisateurAzur.NoUtil,nil,False);   
  lcEcranDynParams.Height:=Self.Height;
  lcEcranDynParams.Width :=Self.Width;                                                                                    
  lcEcranDynParams.Left:=0;
  lcEcranDynParams.Top:=0;      
  if Assigned(lcEcranDynParams)
  then begin 
         lcParams:=TStringList.Create;                    
         try                                                           
           lcParams.Values['NO_DOSSIER']                  :=DossierAzur.NoDossier;                      
           lcParams.Values['NO_ROLE']                     :=UtilisateurAzur.NoRole;
           lcParams.Values['NO_UTILISATEUR']              :=UtilisateurAzur.NoUtil;
           lcParams.Values['NO_PERIODE']                  :=PeriodeAzur.NoPeriode;  
           lcParams.Values['NO_FAMILLE_UTILISATEUR']      :=UtilisateurAzur.NoFamille; 
           lcParams.Values['NO_GROUPE_UTILISATEUR']       :=UtilisateurAzur.NoGroupe; 
           lcParams.Values['NO_SOUS_GROUPE_UTILISATEUR']  :=UtilisateurAzur.NoSousGroupe;                                                                                          
           lcEcranDynParams.OpenDataset(lcParams);                                     
           lcEcranDynParams.ShowModal;                                                                                                                           
         finally 
            lcParams.Free;
            lcParams:=Nil;
         end;                                                          
       end;                                                                                                                          
end;      
```

{% hint style="info" %}
**Info**



* Nous utilisons un Guid pour être certain de pointer vers le bon écran. Cela nous permet d'avoir l'écran n° 10 chez le client A qui est complètement différent de l'écran n° 10 chez le client B
*   Pour trouver le GUID à utiliser, vous pouvez exécuter la requête suivante

    ```
       BC2F2290-1AB6-4845-9C44-9B3260010B83; 
    ```
{% endhint %}

#### Les grilles <a href="#les-grilles" id="les-grilles"></a>

Pour ajouter une grille facilement, utilisez le composant TSitaIbGridPanel. Azur va automatiquement vous ajouter 3 composants



| Composant           | Type             | Description                                                |
| ------------------- | ---------------- | ---------------------------------------------------------- |
| DssSitaIbGridPanel1 | TIB\_DataSource  | C'est lui qui va faire le lien entre le query et la grille |
| QSitaIbGridPanel1   | TSitaIbQuery     | C'est le query                                             |
| SitaIbGridPanel1    | TSitaIbGridPanel | La grille                                                  |

![](.gitbook/assets/toolkit_add_grille.gif)

**Format d'affichage pour un nombre**

```
#,###,###,###,##0.00
```

**Pour initialiser une grille**

Pour résumé c'est le design de la grille. Personnelement j'utilise toujours 3 procédures dans mes scripts

```
InitGp
InitGpPetit
InitGpGrand
```

Un exemple d'InitGP

```
procedure InitGp(eGp:TSitaIbGridPanel);                                                                                          
begin                                                                             
  eGp.IB_Grid.DefaultRowHeight     := 25;                                                      
  eGp.IB_Grid.DefaultColWidth      := 100;                                                                                                                                           
  eGp.IB_Grid.Font.Size            := 13;                               
  eGp.IB_Grid.ReadOnly             := True;                                 
  eGp.IB_Grid.CurrentRowFont.Size  := 12;               
  eGp.IB_Grid.CurrentRowFont.Style := fsBold;                                                
  eGp.IB_Grid.CurrentRowFont.Color := clBlack;                                                                
  eGp.IB_GRID.FixedFont.Size       := 12;   
  eGp.Titre_Font.Size              := 14;                               
  eGp.Initialiser;        
end;
```

Enfin, pour initialiser ma grille

{% hint style="danger" %}
**Warning**



Release note, ce test est facultatif

```
if not SitaIBGridPanel1.Initialized
then initGp(SitaIBGridPanel1);

//autre méthode 
if not SitaIBGridPanel1.Initialized
then SitaIBGridPanel1.Initialiser      
```

Pour initaliser la grille

```
   initGp(SitaIBGridPanel1);

   //autre méthode 
   SitaIBGridPanel1.Initialiser      
```
{% endhint %}



**Pour mettre un checkBox dans un champ**

Généralement nous utilisons ceci pour le champ ACTIF

```
QSitaIbGridPanel1.ColumnAttributes.Clear;
QSitaIbGridPanel1.ColumnAttributes.Add('ACTIF=BOOLEAN=T,F');  
```



**Pour mettre une image dans une colone**

Préalablement, ajouter un composant TImageList sur la forme.

```
SitaIBGridPanel1.GRID_ImageList := ImageList1;
SitaIBGridPanel1.GRID_ImageListParams.Clear;
SitaIBGridPanel1.GRID_ImageListParams.Add('MON_CHAMP=VALUE=0;IMAGEINDEX=0;REPLACE=1'); 
SitaIBGridPanel1.GRID_ImageListParams.Add('MON_CHAMP=VALUE=1;IMAGEINDEX=1;REPLACE=1');
SitaIBGridPanel1.GRID_ImageListParams.Add('MON_CHAMP=VALUE=2;IMAGEINDEX=2;REPLACE=1');
SitaIBGridPanel1.GRID_ImageListParams.Add('MON_CHAMP=VALUE=3;IMAGEINDEX=3;REPLACE=1'); 
```

**Pour mettre de la couleur dans une ligne**

```
SitaIbGridPanel1.FieldColorRulesEnabled := True;           
SitaIbGridPanel1.FieldColorRules.Clear;
SitaIbGridPanel1.FieldColorRules.Add('MON_CHAMP=VALUE=0;LINECOLOR=$00ADCF48'); //-->Vert;
SitaIbGridPanel1.FieldColorRules.Add('MON_CHAMP=VALUE=1;LINECOLOR=$006555ED'); //-->Rouge;
SitaIbGridPanel1.FieldColorRules.Add('MON_CHAMP=VALUE=2;LINECOLOR=$00516EFC'); //-->Orange;
```

**Pour mettre de la couleur dans une colone et dans le texte**

```
SitaIbGridPanel1.FieldColorRules.Clear;
SitaIbGridPanel1.FieldColorRules.Add('TOTAL=EVAL='#39'<<TOTAL_ABS>>'#39'='#39'<<SOLDE_A_PAYER>>'#39';FONTCOLOR=$00245715;');
SitaIbGridPanel1.FieldColorRules.Add('TOTAL=EVAL='#39'<<TOTAL_ABS>>'#39'='#39'<<SOLDE_A_PAYER>>'#39';FONTCOLOR='+ColorToString( coCouleurOK ));
SitaIbGridPanel1.FieldColorRules.Add('TOTAL=EVAL='#39'<<TOTAL_ABS>>'#39'='#39'<<SOLDE_A_PAYER>>'#39';CELLCOLOR=$00DAEDD4;');              
SitaIbGridPanel1.FieldColorRules.Add('TOTAL=EVAL='#39'<<TOTAL_ABS>>'#39'<>'#39'<<SOLDE_A_PAYER>>'#39';FONTCOLOR=$006555ED');                        
SitaIbGridPanel1.FieldColorRules.Add('TOTAL=EVAL='#39'<<TOTAL_ABS>>'#39'<>'#39'<<SOLDE_A_PAYER>>'#39';CELLCOLOR=$00B3AEFF;');               
```

**Pour cacher le nom des colonnes**

```
SitaIbGridPanel1.IB_GRID.IndicateTitles := False;
```

**Pour cacher l'indication de la ligne en cours**

```
SitaIbGridPanel1.ib_grid.IndicateCurrentRow := False; 
```

**Pour récupérer les records sélectionnés dans une grille**

Ci-dessous une fonction qui renvoi la valeur d'un champ d'un query pour les records sélectionnés

```
function GetSelectedRecord(eSourceQuery:TSitaIbQuery;eChamp:String):String;
var
 lcBookMarks:TStringList;
 lcI:Integer;
begin
  result := '';
  if (
            (Assigned(eSourceQuery))
        and (eSourceQuery.Active)  
        and (not eSourceQuery.IsEmpty)        
     )
  then begin
         try
           lcBookMarks := TStringList.Create;
           eSourceQuery.SelectedBookmarks(lcBookMarks);

           //Facultatif, pour sélectionner la ligne en cours
           if lcBookmarks.Count = 0
           then begin
                 eSourceQuery.Selected[eSourceQuery.RowNum] := True;
                 eSourceQuery.SelectedBookmarks(lcBookmarks);
                end;                                              


           if lcBookMarks.Count > 0
           then begin
                  for lcI := 0 to lcBookMarks.Count -1 do
                  begin
                    eSourceQuery.BufferBookmark := lcBookMarks[lcI]
                    result := result + eSourceQuery.BufferFieldByName(eChamp).AsString + #10;  
                  end;                  
                end;
         finally
           lcBookMarks.free;
           lcBookMarks := nil;
         end;
       end;
end; 
```

**Résultat**

Voici le résultat de la démo&#x20;

![](https://docs.sitasoftware.lu/formation/fr/images/toolkit_grille_exemple.png)

#### Communication entre 2 scripts <a href="#communication-entre-2-scripts" id="communication-entre-2-scripts"></a>

Pour communiquer entre deux scripts, vous pouvez consulter les 2 scripts qui sont déja dans votre base

| Description     | lien                                                                         |
| --------------- | ---------------------------------------------------------------------------- |
| ScriptEventCom1 | [lien](https://docs.sitasoftware.lu/formation/fr/images/SCRIPTEVENTCOM1.zip) |
| ScriptEventCom2 | [lien](https://docs.sitasoftware.lu/formation/fr/images/SCRIPTEVENTCOM2.zip) |

Dans cet exemple, lorsque le programme 1 appel le programme 2, il va lui passer un bouton en paramètre.

Le programme 2 va "cliquer" sur le bouton.

Le code "Onclick" du bouton sera exécuté dans le programme 1

**script 1**

```
var
  glCtrl:TButton; //-->Un bouton

procedure UnitMainFormScriptEventCom1Create(Sender: TObject);
begin
  //--> Création du bouton
  glCtrl:=TButton.create(self);
  glCtrl.OnClick:='EventFromOtherScripter';
end;

procedure OnFormClose(Sender: TObject; var Action: TCloseAction);
begin
  Action:=caFree;
end;

procedure Button1Click(Sender: TObject);
var
  lcParams:TStringlist;
begin
  lcParams:=TStringlist.create;                            
  lcParams.AddObject('BtnCom',glCtrl); //--> le bouton est ajouté comme objet dans le stringList paramètres passé au programme 2
  lcParams.add('MYVAR=VIVA');
  RunScriptApp(UtilisateurAzur,F3DynAzur.IB_Connection,'4B8B3F3E-6FF7-4D7C-BB12-1AE2F0D8623F',nil,5,lcParams);
end;  

procedure EventFromOtherScripter(Sender: TObject);
begin
  showmessage('Viva Message on Script 1 called from Script 2');
end; 
```

**script 2**

```
procedure Button1Click(Sender: TObject);
var
  lcIDX:Integer;
begin 
  lcIDX:=PublishedComponents.IndexOf('BtnCom'); //-->On recherche l'objet BtnCom PublishedComponents contient entrautre les paramètres venant du programme 1
  If lcIDX<>-1 //--> si l'objet est trouvé
  then TButton(PublishedComponents.Objects[lcIDX]).Click; //--> On fait le click qui sera "interprété" dans le script 1
end; 
```

#### Création d'un document <a href="#creation-dun-document" id="creation-dun-document"></a>

**Remarques**

{% hint style="success" %}
**Tip**

N'hésitez pas à tester dans le 711 vos données si vous rencotrez une erreur depuis le scripteur.
{% endhint %}

**Création d'un document de vente**

Pour créer un document Azur depuis le scripteur, nous allons utiliser un objet généralement nous nommons l'objet glFactureVente de type TFactureScript.

```
uses UnitFonctionFactureScript

var glFactureVente:TFactureScript;
```

**INITIALISATION DE L'OBJET**

La première étape est d'initialiser l'objet glFactureVente. Cette initialisation est à faire une seule fois dans votre script

{% hint style="danger" %}
**Warning**

Si vous devez faire des documents qui seront dans des périodes comptables différentes, il faudra: - Libérer l'objet - Changer la période - Réinitialiser l'objet En effet, lorsque l'objet glFactureVente est initialisé, il est lié à la période en cours.
{% endhint %}



Dans l'exemple ci-dessous, nous tennons compte de ce possible changement de période

```
procedure initFactureVente(eDateDocument:string;var oNoPeriode:String);
var lcNoPeriode:String;
begin                 
   lcNoPeriode := getPeriodeDate(eDateDocument);                                                                                                        
   if lcNoPeriode <> glNoPeriodeAzur                                                                                      
   then begin                                   
          if Assigned(glFactureVente)
          then begin                               
                 glFactureVente.free;                                                                                 
                 glFactureVente := nil;
               end; 
          FormCom.OuvrirDossier(DossierAzur.NoDossier,lcNoPeriode,True); //Pour eventuellement changer la période
          Application.ProcessMessages;
          glNoPeriodeAzur := lcNoPeriode;     
        end;
   if not Assigned(glFactureVente)
   then begin
          glFactureVente :=  TFactureScript.Create;
          glFactureVente.DocumentVenteWithTransaction(IBTransactionScript, 'AUTOCOMMITROLLBACK=F');     //-->'AUTOCOMMITROLLBACK=F' Permet au script la gestion du commit de la transaction.
          //Comme ici on est succeptible de générer N documents, on va nous gérer la transaction et committer à la fin si tout est ok 
          glFactureVente.SetSMAutomatique(True);                                                                       
          glFactureVente.SetSMIntrastat(False);     
        end;                                
  oNoPeriode := lcNoPeriode;   
end;    
```

{% hint style="success" %}
**Tip**

La différence entre glFactureVente.DocumentVenteWithTransaction(IBTransactionScript, '');

et

glFactureVente.DocumentVenteWithTransaction(IBTransactionScript, 'AUTOCOMMITROLLBACK=F');

C'est que dans le deuxième exemple, c'est le scripteur qui va gérer la transaction. Lorsque la validation du document se ferra, le document ne sera pas commité. Cet initialisation peut s'averer utile si vous êtes amené à devoir créer plusieurs documents ou à devoir faire un traitement post création.
{% endhint %}



**CRÉATION DE L'ENTÊTE DU DOCUMENT**

L'entête du document contient les informations d'identification du document.

* Le client
* La date du document
* La date d'échéance
* Les adresses de livraisons et facturations
* ...

```
function CreerEntete(eSourceQuery:TSitaIbQuery;var oNoDocument:String; var oCodeUniqueDocument:String):Boolean;
var 
  lcNoJournal, 
  lcTypeDocument, 
  lcNoDocument,                              
  lcNoClient, 
  lcAdrFact,
  lcAdrLiv,   
  lcReference,
  lcDateDocument,
  lcNoPeriode:String;
  lcCreationDoc:Boolean;
begin
  try
    initFactureVente(eSourceQuery.BufferFieldByName('DATE_DOCUMENT').AsString , lcNoPeriode)  

    result := False;
    lcNoJournal := eSourceQuery.BufferFieldByName('NO_JOURNAL').AsString;
    lcTypeDocument := eSourceQuery.BufferFieldByName('TYPE_DOCUMENT').AsString;
    lcNoDocument := oNoDocument;
    lcDateDocument := eSourceQuery.BufferFieldByName('DATE_DOCUMENT').AsString;
    lcNoClient := eSourceQuery.BufferFieldByName('NO_CLIENT').AsString;
    lcAdrFact := eSourceQuery.BufferFieldByName('ADRESSE_FACT').AsString;
    lcAdrLiv := eSourceQuery.BufferFieldByName('ADRESSE_LIVR').AsString;    

    lcReference := '';
    if CBReprendreReference.Checked
    then lcReference := eSourceQuery.BufferFieldByName('REFERENCE').AsString;
    lcCreationDoc := True;

    if not glFactureVente.AjoutEnteteAutomatique(                           
                                                 lcNoJournal,     //ANoJournal String;
                                                 lcTypeDocument,  //ANoTypeDocument String;
                                                 lcNoDocument,    //ANoDocument var String;                   
                                                 lcNoClient,      //ANoClient String;       
                                                 lcDateDocument,  //ADateDocument String;
                                                 '',              //ANoCondPaiement String;                                                                                                                
                                                 lcAdrFact,       //ANoAdrFac String; 
                                                 lcAdrLiv,        //ANoAdrLiv String; 
                                                 lcCreationDoc,   //ACreation var Boolean; 
                                                 lcReference,     //Reference String;
                                                 '',              //AReleve String;   
                                                 '',              //AMajcompta String;
                                                 lcNoPeriode,     //ANoPeriode String;
                                                 0,               //AAcompte Extended;              
                                                 '',              //ANoMagasin String;    
                                                 '',              //ANoCaisse String; 
                                                 '',              //ANoFamilleContrat String;
                                                 '',              //ANoGroupeContrat String;                                                                                     
                                                 '',              //ANoSGroupeContrat String;    
                                                 '',              //ANoCompteCentralisateur String;                      
                                                 False,           //ASM_AjoutTexteDebutFin Boolean; 
                                                 '',              //Parametres String;                                                                                         
                                                 '',
                                                 ''           
                                                 )            
    then Result := False; 
    else begin                                            
           glFactureVente.ModifieEntete ('CODE_UNIQUE_SOURCE=' + eSourceQuery.BufferFieldByName('CODE_UNIQUE_SOURCE').AsString ,'');
           glFactureVente.ModifieEntete ('CODE_TOURNEE=' + eSourceQuery.BufferFieldByName('CODE_TOURNEE').AsString ,'');
           glFactureVente.ModifieEntete ('DATE_LIVRAISON=' + eSourceQuery.BufferFieldByName('DATE_LIVRAISON').AsString,'');                                                                                                                   
           glFactureVente.ModifieEntete ('CODE_OPERAION=' + '725','');
           oCodeUniqueDocument := glFactureVente.JounalVenteByName('CODE_UNIQUE','');
           oNoDocument := lcNoDocument;
           Result := True;                    
         end;          
  except
    result := False;
    SitaMessageDlg(3243201,Utilisateur.CodeLangue,IB_Connection,nil,'Une erreur s''est produite lors de la création d''un nouveau document', mtError, [mbOk], 0);    
  end;  
end;  
```

**AJOUT DES ARTICLES AU DOCUMENT**

```
function AjoutArticle(eSourceQuery:TSitaIbQuery;var oCodeUnique:String):Boolean;
var
  lcNoArticle,lcLibelle,lcUniteEmballage:String;
  lcQuantite,lcUniteDeVente:Extended;
  lcPrix:Extended; 
  lcRemiseLigne:Extended;
  lcModifFields:TStringList;
begin
  result := False;
  try
    lcModifFields := TStringList.create;
    try
      lcNoArticle := eSourceQuery.BufferFieldByName('NO_ARTICLE').AsString;
      lcLibelle := eSourceQuery.BufferFieldByName('LIBELLE').AsString;
      lcQuantite := StrToFloatDef(eSourceQuery.BufferFieldByName('QUANTITE_LIGNE').AsString,1);
      lcUniteDeVente := StrToFloatDef(eSourceQuery.BufferFieldByName('UNITE_DE_VENTE').AsString,1);
      lcUniteEmballage := eSourceQuery.BufferFieldByName('UNITE_EMBALLAGE').AsString;
      lcPrix := eSourceQuery.BufferFieldByName('PRIX').AsExtended;
      lcRemiseLigne := eSourceQuery.BufferFieldByName('REMISE').AsExtended; 

      lcModifFields.Add('CODE_UNITE_LIGNE=' + lcUniteEmballage ); 
      lcModifFields.Add('CODE_UNIQUE_SOURCE=' + eSourcequery.BufferFieldByName('CODE_UNIQUE_IE').AsString);

      if glFactureVente.AjoutArticleAutomatiqueDebut (lcNoArticle,     //ANoArticle: String;
                                                      '',              //lcNoCompteGen,                                              //ANoCompteGen: String; 
                                                      '',              //ANoCodeTva: String;
                                                      '0',             //ANoCentreFrais: String;
                                                      '0',             //ANoNatureFrais: String; 
                                                      lcQuantite ,     //AQteLigne: Extended;                               
                                                      lcUniteDeVente,  //AUniteLigne: Extended;
                                                      lcPrix,          //APrixUnitaire: Extended; 
                                                      lcRemiseLigne,   //ARemiseLigne: Extended;
                                                      '1',             //AModeCalcul, //: Char;
                                                      False,           //: Boolean; 
                                                      '',              //: String;              
                                                      True,            //: Boolean;                
                                                      lcLibelle,       //IB_CArticle.FieldByName('LIBELLE1').AsString, //: String; 
                                                      False,           //,                          
                                                      False,           //: Boolean         
                                                      '',                                    
                                                      '',                          
                                                      lcModifFields.Text)                                              
      then begin                                                                                                                                                            
             if not glFactureVente.AjoutArticleAutomatiqueFin('') 
             then begin                                                          
                    Result := False;
                    SitaMessageDlg(3245201,Utilisateur.CodeLangue,IB_Connection,nil,'Une erreur s''est produite lors de la validation de l''ajout d''article au document', mtError, [mbOk], 0);
                  end                 
             else begin
                     result := True;
                     oCodeUnique := glFactureVente.FactureLigneByName('CODE_UNIQUE','');
                  end;  
           end                   
      else begin
             Result := False;
             SitaMessageDlg(3245201,Utilisateur.CodeLangue,IB_Connection,nil,'Une erreur s''est produite lors de la validation de l''ajout d''article au document', mtError, [mbOk], 0);
           end;
    except
      result := False;  
      SitaMessageDlg(3244201,Utilisateur.CodeLangue,IB_Connection,nil,'Une erreur s''est produite lors de l''ajout d''article au document', mtError, [mbOk], 0);
    end;
  finally
    lcModifFields.free;
    lcModifFields := nil;
  end;  
end; 
```

**VALIDATION DU DOCUMENT**

```
function ValiderEntete:Boolean;
begin                           
  try
    result := False;
    glFactureVente.ValiderDocumentVente(0,0,'');    
    Result := True;             
  except
    result := False;    
    SitaMessageDlg(3246201,Utilisateur.CodeLangue,IB_Connection,nil,'Une erreur s''est produite lors de la validation du document', mtError, [mbOk], 0);
  end;  
end;
```

#### Création d'une Intervention <a href="#creation-dune-intervention" id="creation-dune-intervention"></a>

```
uses UnitFormIntervention
...
function AjouterUneIntervention(eTypeIntervention:Integer; var oNoIntervention:Integer;eAutoCommit:Boolean):Boolean;
var
  lcInterventionParams:TInterventionParams; 
  lcResultIntervention:Boolean;
begin                    
  try                                                                                                                                                
    try
      result := False;
      lcInterventionParams:=TInterventionParams.create;
      with TInterventionParams(lcInterventionParams) do
      begin                                    
        IBConnection:=IBTransactionScript.IB_Connection;
        IBTransaction:=IBTransactionScript;             
        UtilisateurIntervention:=UtilisateurAzur;                                                                                                   
        Description:='';                                  //Description
        TypeIntervention:=eTypeIntervention;
        NoIntervention:=-1;                                  
        NoDossierIntervention  :=DossierAzur.NoDossier;
        SMAutomatique:=true;                                                      
        HideForm:=True;    
        Libelle:='';                                      //Libelle            
      end;   
      lcResultIntervention := Intervention(lcInterventionParams);
      if ((lcResultIntervention) and (TInterventionParams(lcInterventionParams).NoIntervention>0))
      then begin                                                                               
             oNoIntervention := IntToStr(TInterventionParams(lcInterventionParams).NoIntervention);
             if eAutoCommit
             then IbTransactionScript.CommitRetaining;             
             Result := True;
           end;
    except
      IBTransactionScript.RollbackRetaining;
    end;
  finally
    try
      TInterventionParams(lcInterventionParams).FormIntervention.Free;
    except
    end;     
  end;
end;  
```

#### Azur Maps <a href="#azur-maps" id="azur-maps"></a>

![](<.gitbook/assets/image (350).png>)



**Introduction**

Grâce au scripteur Azur Maps, vous allez être capable

* D'afficher des points sur la carte.
* De calculer la distance entre 2 points.
* D'afficher une route entre plusieurs points.

{% hint style="success" %}
**Tip**

Un point sur la carte s'appel aussi marker.
{% endhint %}

{% hint style="info" %}
**Info**

Si vous rencontrez un souci avec Edge Chromium: "Could not initialize Edge Chromium! ..." [Tms Software Edge Chromium](https://www.tmssoftware.com/site/edgechromium.asp) .
{% endhint %}

**Marker**

Ci dessous une petite descriptions d'un marker:

* Lorsqu'un marker est créé, nous récupérons un **id** unique qui l'identifie.
* Un marker peut avoir un **titre** (élément visible au survol de la souris).
* Un marker peut avoir un **popup** (élément visible lors du click).
* Un marker peut avoir une image personalisée.

![](<.gitbook/assets/image (338).png>)



**Utilisation depuis un autre script**

Ci-dessous la liste des objets à passer à Azur Maps

* BtnRetourVersScriptAppel
* QueryFromScriptAppel
* BtnActionFromScriptAppel
* ParamsFromScriptAppel
* ParamsAssociationIdPopup
* ParamsAssociationIdCuAzur
* ParamsPopupStr

**BTNRETOURVERSSCRIPTAPPEL**

Bouton qui permet le retour vers le script "Source". Tag:

* 3 Distance calculée, réponse dans ParamsFromScriptAppel.Values\['KM'] et ParamsFromScriptAppel.Values\['TIME'].
* 4 Un clic a été effectué dans un marker sur la carte, dans le Hint du bouton, on a l'id du marker
* 5 Disance calculée en vol d'oiseau, réponse dans ParamsFromScriptAppel.Values\['KM'].
* 6 Si l'action n''a pas de retour spécifique, on force un clique pour pouvoir signifier que l'action est terminée.

**QUERYFROMSCRIPTAPPEL**

Est un query qui contient des adresses à affciher sur la carte, les champs utilisés sont:

* ADRESSE, Rue de la Baronne Lemonnier 4A
* CODE\_POSTAL, 5580
* LOCALITE, Rochefort
* NO\_CODE\_PAYSE, BE
* NOM, Nom ou NOM\_CLI ou NOM\_FOU
* POPUP, Texte du popup si l'utilisateur clique sur le marker
* GUID\_IMAGE, guid de TREEVIEW\_PICTURE qui contient le guid de l'image à afficher pour représenter le marker
* CODE\_UNIQUE ou ITEM\_DBKEY, sera le code unique auquel sera associé l'id du marker
* LATITUDE \*
* LONGITUDE \*

{% hint style="info" %}
**Info**

Si la latitude et la longitude sont remplies, l'adresse ne sera pas pris en compte, le programme utilisera une autre fonction.
{% endhint %}



**BTNACTIONFROMSCRIPTAPPEL**

C'est l'élément déclancheur des actions du script. Les différentes actions possibles sont (BtnActionFromScriptAppel.tag):

**Afficher sur la carte un marker par record du query**

Action 0, avec l'utilisation de QueryFromScriptAppel, Pour chaque record du Query, un marker sera placé sur la carte.

**Afficher sur la carte un marker par record du query**

Action 1, avec l'utilisation de QueryFromScriptAppel, Pour le record actif du Query, un marker sera placé sur la carte.

**Réinitialiser la carte**

Action 2

**Calculer une distance**

Action 3, avec l'utilisation de ParamsFromScriptAppel

**Afficher un popup**

Action 4

**Placer un maker**

Action 5 avec l'utilisation de ParamsFromscriptAppel.

**Voir une route**

Action 6 avec l'utilisation de QueryFromScriptAppel.

**Calcul distance (vol d'oiseau)**

Action 9 avec l'utilisation de ParamsFromscriptAppel.

Avant d'appeler BtnActionFromScriptAppel.Click dans le scripteur source

* ParamsFromScriptAppel.Values\['LATITUDE\_DE'] = Latitude point A
* ParamsFromScriptAppel.Values\['LONGITUDE\_DE'] = Longitude point A
* ParamsFromScriptAppel.Values\['LATITUDE\_A'] = Latitude point B
* ParamsFromScriptAppel.Values\['LONGITUDE\_A'] = Longitude point B

Une fois la distance calculée, dans le scripteur source, la réponse se trouvera dans

* ParamsFromScriptAppel.Values\['KM']

**Placer un cercle sur la carte**

Action 10 avec l'utilisation de ParamsFromscriptAppel.

Avant d'appeler BtnActionFromScriptAppel.Click dans le scripteur source

* ParamsFromScriptAppel.Values\['LATITUDE'] = Latitude du centre du cercle
* ParamsFromScriptAppel.Values\['LONGITUDE'] = Longitude du centre du cercle

ou

* ParamsFromScriptAppel.Values\['ADRESSE'] = Adresse
* ParamsFromScriptAppel.Values\['DIAMETRE'] = Diamètre du cercle en Km
* ParamsFromScriptAppel.Values\['CENTRE'] = Si T, alors la carte sera centrée sur le cercle

**Afficher sur la carte un marker par record sélectionné du query**

Action 11, avec l'utilisation de QueryFromScriptAppel, Pour les records sélectionnés du Query, un marker sera placé sur la carte .

**PARAMSFROMSCRIPTAPPEL**

Est un StringList qui va nous permettre de passer des informations entre les deux scripts.

**Pour calculer une distance**

Avant d'appeler BtnActionFromScriptAppel.Click dans le scripteur source

* ParamsFromScriptAppel.Values\['FROM'] = Adresse source
* ParamsFromScriptAppel.Values\['TO'] = Adresse destination

OU

* ParamsFromScriptAppel.Values\['LATITUDE\_DE'] =Latitude Adresse source
* ParamsFromScriptAppel.Values\['LONGITUDE\_DE'] =Latitude Adresse source
* ParamsFromScriptAppel.Values\['LATITUDE\_A'] =Latitude Adresse Destination
* ParamsFromScriptAppel.Values\['LONGITUDE\_A'] =Longitude Adresse Destination

{% hint style="info" %}
**Info**

Comme paramètre supplémentaire, vous avez aussi ParamsFromScriptAppel.Values\['ROUTE'] = T, alors la route sera affichée sur la carte. ParamsFromScriptAppel.Values\['ETAPES'] = T, alors les étapes seront affichées sur la carte.
{% endhint %}



Une fois la distance calculée, dans le scripteur source, la réponse se trouvera dans

* ParamsFromScriptAppel.Values\['KM']
* ParamsFromScriptAppel.Values\['TIME']

**Pour placer un marker sur la carte**

Pour placer un marker sur la carte, vous devez remplir ParamsFromscriptAppel avec au moins les values suivantes:

* ParamsFromscriptAppel.Values\['ADRESSE'], contient toute l'adresse Rue + localite + code postal + pays
* ParamsFromscriptAppel.Values\['TITRE'], contient le titre du marker
* ParamsFromscriptAppel.Values\['GUID\_IMAGE'], guid de TREEVIEW\_PICTURE qui contient le guid de l'image à afficher pour représenter le marker
* ParamsFromscriptAppel.Values\['LATITUDE'], contient la latitude de l'adresse\*.
* ParamsFromscriptAppel.Values\['LONGITUDE'], contient la longitude de l'adresse\*.

{% hint style="info" %}
**Info**

Si la latitude et la longitude sont remplies, l'adresse ne sera pas pris en compte, le programme utilisera une autre fonction.
{% endhint %}

**PARAMSASSOCIATIONIDPOPUP**

Ce StringList contiendra une section par marker avec le contentu du popup pour ce marker

```
[213213-5561-56651]
Popup à afficher
```

**PARAMSASSOCIATIONIDCUAZUR**

Ce StringList contiendra une section par marker avec le code\_unique associé à ce marker

```
[213213-5561-56651]
123456
```

il contiendra aussi éventuellement, une section par code\_unique avec comme value disponible

* LATITUDE
* LONGITUDE
* ID

**PARAMSPOPUPSTR**

Ce StringList contiendra le contenu d'un popop, utilisé uniquement lors du placement d'un marker via Action 5

### Démos <a href="#demos" id="demos"></a>



| Description                                       | lien                                                                                      |
| ------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| Programme vierge de base                          | [lien](https://docs.sitasoftware.lu/formation/fr/images/TESTFROMSCRATC1.zip)              |
| Programme vierge reporting                        | [lien](https://docs.sitasoftware.lu/formation/fr/images/PROGRAMMESCRIPTDEMOREPORTING.zip) |
| Programme vierge ecran dynamique                  | [lien](https://docs.sitasoftware.lu/formation/fr/images/PROGRAMMESCRIPTDEMOECRANDYN.zip)  |
| Programme virege grille                           | [lien](https://docs.sitasoftware.lu/formation/fr/images/PROGRAMMESCRIPTDEMOGRILLE.zip)    |
| Programme sélection dans une grille               | [lien](https://docs.sitasoftware.lu/formation/fr/images/DEMOSELECTIONDANSGRILLE.zip)      |
| Programme de création d'un document de vente Azur | [lien](https://docs.sitasoftware.lu/formation/fr/images/DEMOCREATIONDOCUMENTVENTE.ZIP)    |
| Programme Azur Maps                               | [lien](https://docs.sitasoftware.lu/formation/fr/images/AZURMAPS.zip)                     |
| Programme demo appel Azur Maps                    | [lien](https://docs.sitasoftware.lu/formation/fr/images/DEMOAPPELMAPS.zip)                |

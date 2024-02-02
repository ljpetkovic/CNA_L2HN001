---
marp: true
theme: default
markdown.marp.enableHtml: true
paginate: true
extra: true
footer: "Cultures numériques avancées, mineure HN (L2HN001), 02/02/2024, Ljudmila PETKOVIC"
html: true

---

  <style>
  section {
    background-color: white;
    color: black;
    font-family: system-ui !important;
  }



  h1 {
    color: DarkBlue;
  }

  

  h2 {
    color: DarkBlue;
  }

  h3 {
    color: DarkBlue;
  }

  h4 {
    color: DarkBlue;
  }

  h5 {
    color: DarkBlue;
  }

  h6 {
    color: DarkBlue;
    font-size: 30px;
    font-weight:normal;
  }

  blockquote {
    background: #ffedcc;
    border-left: 10px solid #d1bf9d;
    margin: 1.5em 10px;
    padding: 0.5em 10px;
  }
  blockquote:before{
    content: unset;
  }

  blockquote:after{
    content: unset;
  }

  small-text {
      font-size: 0.7rem;
    }

  smaller-text {
      font-size: 0.5rem;
    }

  .center {
   display: block;
     margin-left: auto;
   margin-right: auto;
     width: 50%;
  }

.container {
  display: grid;
  grid-template-columns: 0.68fr 1fr;
}

    .container-side {
      display: inline-flex;
      text-align: center;
    }



    #content {
          position: relative;
      }
      #content img {
          position: absolute;
          top: -600px;
          right: 0px;
      }

  </style>

</div> 

  <div class="column">
    <img src="https://htl.cnrs.fr/wp-content/uploads/2021/05/sorbonne_nouvelle-devise-trapezes_bleu-e1622639412877.png" alt="Sorbonne_Nouvelle" style="width:10%; position:relative; top:-40px; left:-795px; margin-left:790px; margin-right:0px;">
  </div>
 <div class="row">
  <div class="column">
      <figure>
    <img src="https://kinsta.com/wp-content/uploads/2021/08/old-date.png" alt="Bash" style="width:30%; float:right">
      </figure>
  </div>






  <!-- _class: lead -->

  ## Cultures numériques avancées

  #### Structure des répertoires. Commandes. Variables.

  ###### Ljudmila PETKOVIC

<small-text><a href="mailto:ljudmila.petkovic@sorbonne-nouvelle.fr">`ljudmila.petkovic@sorbonne-nouvelle.fr`</a></small-text>

  <br>

  

  <small-text> 

Cultures numériques avancées (L2HN001)
Mineure « Humanités numériques », licence Lettres 
Paris, le 2 février 2024, année 2023-2024

  </small-text>

<smaller-text>*Diapositives adaptées de [Simon Gabay](https://github.com/gabays/Fondamentaux/blob/main/Lignes_de_commandes/DistRead_1_2.pdf), [Simone Rebora](https://github.com/ABC-DH/EnExDi2022/tree/main/materials/1_KnowYourComputer/slides) et [Élisabeth Brunet et Gaël Thomas](http://www-inf.telecom-sudparis.eu/cours/CSC3102/Supports/ci1-bash/ci-bash.pptx.pdf)*.</smaller-text>

<!--<smaller-text>*Diapositives adaptées de [Simon Gabay](https://github.com/gabays/Fondamentaux/blob/main/Lignes_de_commandes/DistRead_1_2.pdf) et de [Simone Rebora](https://github.com/ABC-DH/EnExDi2022/tree/main/materials/1_KnowYourComputer/slides)*.</smaller-text>-->

<div style="position:relative; top:-220px; left:0px; margin-left:860px; margin-right:0px; font-size:14px;">
  Source :  <a href="https://kinsta.com/fr/blog/commandes-linux/">Diaz, 2023.</a>
</div>



---

## Structure des répertoires

* façon dont un système d'exploitation organise les fichiers / répertoires accessibles à l'utilisateur 
* les fichiers sont généralement affichés dans une arborescence hiérarchique
* angl. *Filesystem Hierarchy Standard* : « norme de la hiérarchie des systèmes de fichiers » 
  * GNU/Linux et la plupart des systèmes Unix

---

## Structure des répertoires

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

![bg width:500pt height:350pt](/home/ljudmila/Dropbox/Bureau/SN/archive/2022-23/CNA_L2HN001/1_Ligne_de_commande/img/arborescence.jpg)

*<p align="center">Filesystem Hierarchy Standard.</p>*

---

## Fonctions des répertoires

* `/bin/` : commandes de base nécessaires au démarrage et à l'utilisation d'un système minimaliste
* `/etc/` : *editable text configurations* ou fichiers de configuration
* `/lib/` : bibliothèques (*librairies*) logicielles nécessaires pour les exécutables
* `/home/` : répertoire des utilisateurs
* ...

Les répertoires de chaque utilisateur sont eux connus (fichiers de système cachés)

* `Bureau`
* `Documents`
* `Téléchargements`
* ...

---

## `root`

Les répertoires sont organisés comme un arbre : 



![bg width:350pt height:250pt](/home/ljudmila/Dropbox/Bureau/SN/archive/2022-23/CNA_L2HN001/1_Ligne_de_commande/img/arborescence.jpg)

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

<br>

* le premier répertoire (ici `Ordinateur`) est appelé le répertoire *racine* (`root`) 
* il contient tous les autres, organisés comme des branches partant de ce tronc

---

## Chemin absolu

L'adresse du répertoire racine est `/`. Celle d'un répertoire ou d'un fichier précis est ainsi la liste des répertoires depuis `root` pour accéder à celui voulu, chaque nom étant séparé avec un `/`. Ainsi, pour atteindre le fichier `bash` dans le dossier `bin` , je suis le chemin **absolu** : `/bin/bash`.

## Chemin relatif

Le chemin que nous venons de voir est dit *absolu*, car il part de l'élément racine, mais il existe aussi des chemins **relatifs** si nous partons d'un autre endroit (normalement celui où nous sommes déjà) : `ljudmila/home/bin/bash`.

---

## Chemin relatif

Parfois il est impossible de savoir quel est le nom du fichier précédent dans l'arborescence, il est possible d'utiliser un raccourci : `..` signifie ainsi « remonter d'un dossier » :

```bash
ljudmila/home/bin/bash
```

est ainsi l'équivalent de

```bash
ljudmila/../bin/bash
```

---

## Conventions de nommage

1. Il est fortement déconseillé d'utiliser des espaces
2. Des stratégies alternatives existent comme:
   2.1 Le camelCase (par exemple : `nomDeFichier.extension`)
   2.2 Avoir recours à des tirets (`nom-de-Fichier.extension`) ou
   des tirets bas (`nom_de_Fichier.extension`)
   2.3 Tentez d'être cohérent dans cette stratégie
3. Versionnez les documents (`nom-de-Fichier-v1.extension`) ou
   datez‐les en commençant par l'année (`nom-de-Fichier-AAA-MM-JJ.extension`)
4. L'extension doit être choisie avec attention : un `.txt` n'est pas un `.xml`

---

## Fonctionnement de Bash

* Bash exécute les instructions ligne par ligne : la fin de ligne est la fin de commande
* une commande doit être complète, sinon elle ne s'execute pas
* une commande est appelée par son nom (par exemple `pwd`), qui permet de retrouver la fonction (angl. *builtin*), le programme associé
  * une fonction est un bloc de commandes qui s'exécute lorsque la fonction est appelée
  * un *builtin* (« préconstruit », comprendre « prédéfini ») est une mini‐opération pré‐construite en bash (dont `pwd`)
  * un programme est un groupe d'instructions

---

## Localisation

Certaines commandes prédéfinies sont enregistrées dans la machine (comme `pwd` ou `ls`) : leur nom suffit pour les appeler.

```bash
pwd
```

```bash
ls
```

Dans d'autres cas, comme celui de scripts ou de programmes, il faut spécifier le chemin ou le fichier se trouve. Pour cela on utilise le chemin absolu ou (ici) relatif :

```bash
commandes/commande_1.sh
```

---

## Affichage des fichiers / répertoires

`ls` : lister les noms des fichiers et des répertoires *visibles* dans le répertoire courant

`ls -l` : utiliser un format de liste longue (avec les indications des permissions pour chaque fichier)

* `-l` est une *option*

---

## Argument

Certaines commandes vont nécessiter des précisions : copier *ceci*, aller *là‐bas*. Pour donner ces précisions, on va ajouter à la commande des arguments.

Prenons l'exemple de la commande `cd` (*change directory*) qui permet de se déplacer. On pourrait la traduire par `« aller à » [commande] + lieu [argument]`. Le lieu où l'on se dirige prend la forme du répertoire‐destination placé juste après la commande.

```bash
cd commandes
```

---

## Changer le répertoire

```bash
cd Documents # aller dans le répertoire 'Documents'
```

```bash
cd ../.. # remonter de deux dossiers
```

```bash
cd . # rester dans le même répertoire
```

---

## Arguments

Parfois on peut avoir besoin de plusieurs arguments. On les ajoute ainsi les uns après les autres.

* commande `cp` (*copy*), que l'on peut traduire par `« copier » [commande] + tel chose [argument 1] + à tel endroit [argument 2]` :

  ```bash
  cp commandes/test.sh ..
  ```

* commande `rm` (*remove*) qui permet d'effacer un fichier :

  ```bash
  rm test.sh
  ```

---

## Astuces pour naviguer dans le système des répertoires

* Faire glisser des éléments dans une fenêtre Terminal afin d’entrer le chemin absolu d’un fichier / répertoire

* Ouvrir le terminal à partir du répertoire souhaité
  * clique droite sur le répertoire > `Ouvrir dans un terminal`

* Flèche haut `↑` et bas `↓` pour se déplacer dans l'historique du terminal

* Tabulation (`↹`) pour l'auto-complétion

---

## Options

* une option modifie le comportement d'une commande
* elle est placée après la commande et est précédée d'un (`-`) ou de deux tirets (`--`)
  * `ls -a` (ou `ls -Force` sous Windows) : lister les noms des fichiers et des répertoires *cachés* dans le répertoire courant, commençant par un point, p. ex. `.fichier_cache.txt`
    * <small-text>raccourci pour afficher les fichiers cachés : `Ctrl + H` (Linux) ou `(fn) + Cmd + Shift + point` (Mac)
  * `git --version` : vérifier si Git avait été bien installé et si oui, quelle version a été installée

---

## Copier le fichier

La commande `mkdir` (*make directory*) permet de créer un répertoire :

```bash
mkdir test
```

La commande `cp` (*copy*) permet de copier un fichier :

```bash
cp mon_script.sh test
```

Déplacer une multitude de fichiers en les mettant à la suite :

```bash
cp FICHIER_1 FICHIER_2 RÉPERTOIRE_CIBLE
```

Copier un fichier dans le même répertoire en lui attribuant un nouveau nom :

```bash
cp test/mon_script.sh test/mon_script_2.sh
```

---

## Déplacer le fichier

Un alternative à la commande `cp` est la commande commande `mv` (*move*) qui permet de déplacer (et non copier) un fichier :

```bash
mv mon_script.sh test
```

Son fonctionnement est proche de `cp` :

```bash
mv FICHIER_1 FICHIER_2 RÉPERTOIRE_CIBLE
```

Si tous les fichiers ont la même extension, il est possible d'utiliser un joker (`*`) :

```bash
mv *.sh RÉPERTOIRE_CIBLE
```

---

## Effacer

La commande `rm` (*remove*) permet d'effacer un fichier, avec l'option `-f` pour forcer l'exécution si besoin :

```bash
rm mon_script.sh
```

Pour effacer un répertoire contenant des fichiers, il faut utiliser :

* l'option `-r` (*recursively*) qui permet d'effacer tous les fichiers contenus l'un après l'autre
* l'option `-f` (*force*) pour éviter d'avoir à valider pour chaque fichier

```bash
rm -rf test
```

---

## Rechercher

Faire des recherches dans un fichier : `grep` (`Select-String` pour Windows) :

```bash
grep "ordinateur" fichier_test.txt
```

Nous pouvons faire des requêtes en utilisant les expressions régulières (*regex*).

Trouvons tous les mots commençant par la lettre « m », en majuscule ou en minuscule.

```bash
grep -Eoi "\bm\w+" fichier_test.txt
```

<smaller-text>`-E` : expression rationnelle étendue (≠ expression rationnelle simple `-G`)
<smaller-text>`-o` : n'afficher que l'occurrence en question (*match*)</smaller-text>
<smaller-text>`-i` : trouver le mot en majuscule ou en minuscule</smaller-text>
<smaller-text>`\b` : limite de mot, c'est-à-dire le début d'un mot<smaller-text>
<smaller-text>`\w+` : un ou plusieurs caractères alphabétiques<smaller-text>

---

## Variables

Comme tout langage de programmation, Bash permet aux programmeurs de stocker de l'information dans des objets appelés **variables** (on déclare les variables).

Exemple d'une variable :

```bash
nom="Michel"
```

Les variables se caractérisent par :

* leur nom : 
  * chaque variable à un nom et ce nom est unique (il n'existe pas deux variables ayant le même nom dans un même programme)
  * ce nom permet de savoir de quelle variable on parle.
* leur type : nombre, chaîne de caractères, liste...

---

## Créer une variable 

Dans la séquence *Coucou* + *nom* si *nom* doit pouvoir changer il s'agit d'une variable. Cette dernière est stockée sous un nom arbitraire :

```bash
nom="Michel" # ne pas séparer la variable du signe « égal à » (nom = "Michel")
```

et appelée avec son nom précédée de `$` :

```bash
echo "Coucou $nom"
```

---

  ## Références

<ul style="font-size: 20px">
    <li><b>Brunet, É. & Thomas, G.</b> (<i>s. d.</i>). « Le shell bash » [<i>diapositives</i>]. Télécom SudParis. <a href="http://www-inf.telecom-sudparis.eu/cours/CSC3102/Supports/ci1-bash/ci-bash.pptx.pdf">http://www-inf.telecom-sudparis.eu/cours/CSC3102/Supports/ci1-bash/ci-bash.pptx.pdf</a></li>
    <li><b>Combeau, M.</b> (2022). « La différence entre le terminal, la console et le shell ». <a href="https://www.codequoi.com/difference-entre-terminal-console-et-shell/">https://www.codequoi.com/difference-entre-terminal-console-et-shell/</a></li>
    <li><b>Rebora, S.</b> (2022). « Connaître son propre ordinateur » [<i>dépôt GitHub</i>]. EnExDi2022. <a href="https://github.com/ABC-DH/EnExDi2022/tree/main/materials/1_KnowYourComputer/slides">https://github.com/ABC-DH/EnExDi2022/tree/main/materials/1_KnowYourComputer/slides</a>
  </li>
    <li><b>Gabay, S.</b> (2022). « Les lignes de commandes et Bash » [<i>dépôt GitHub</i>]. Université de Genève, Chaire des humanités numériques, Faculté des Lettres. <a href="https://github.com/gabays/Fondamentaux/blob/main/Lignes_de_commandes/DistRead_1_2.pdf">https://github.com/gabays/Fondamentaux/blob/main/Lignes_de_commandes/DistRead_1_2.pdf</a>
    </li>
    <li><b>Diaz, D.</b> (2023). « Les 40 commandes Linux les plus utilisées que vous devez connaître ». Kinsta. <a href="https://kinsta.com/fr/blog/commandes-linux/">https://kinsta.com/fr/blog/commandes-linux/</a>
    </li>
    <li><b>Xyoos</b> (<i>s.d.</i>). « Interface graphique ». <a href="https://cours-informatique-gratuit.fr/dictionnaire/interface-graphique/">https://cours-informatique-gratuit.fr/dictionnaire/interface-graphique/</a></li>
</ul>

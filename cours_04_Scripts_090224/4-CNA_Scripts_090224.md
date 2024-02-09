---
marp: true
theme: default
markdown.marp.enableHtml: true
paginate: true
extra: true
footer: "Cultures numériques avancées, mineure HN (L2HN001), 09/02/2024, Ljudmila PETKOVIC"
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

  #### Exécution des scripts en ligne de commande.

  ###### Ljudmila PETKOVIC

<small-text><a href="mailto:ljudmila.petkovic@sorbonne-nouvelle.fr">`ljudmila.petkovic@sorbonne-nouvelle.fr`</a></small-text>

  <br>

  

  <small-text> 

Cultures numériques avancées (L2HN001)
Mineure « Humanités numériques », licence Lettres
Paris, le 9 février 2024, année 2023-2024

  </small-text>

<smaller-text>*Diapositives adaptées de [Simon Gabay](https://github.com/gabays/Fondamentaux/blob/main/Lignes_de_commandes/DistRead_1_2.pdf), [Simone Rebora](https://github.com/ABC-DH/EnExDi2022/tree/main/materials/1_KnowYourComputer/slides) et [Élisabeth Brunet et Gaël Thomas](http://www-inf.telecom-sudparis.eu/cours/CSC3102/Supports/ci1-bash/ci-bash.pptx.pdf)*.</smaller-text>

<!--<smaller-text>*Diapositives adaptées de [Simon Gabay](https://github.com/gabays/Fondamentaux/blob/main/Lignes_de_commandes/DistRead_1_2.pdf) et de [Simone Rebora](https://github.com/ABC-DH/EnExDi2022/tree/main/materials/1_KnowYourComputer/slides)*.</smaller-text>-->

<div style="position:relative; top:-220px; left:0px; margin-left:860px; margin-right:0px; font-size:14px;">
  Source :  <a href="https://kinsta.com/fr/blog/commandes-linux/">Diaz, 2023.</a>
</div>


---

## Créer un fichier en ligne de commande

* il existe plusieurs manières de créer un fichier en ligne de commande
* alternative aux éditeurs de texte basés sur une interface graphique
  * Notepad, TextEdit, Gedit...

---

## `touch`

* commande `touch` suivi du nom du fichier que l'on veut créer :

  ```bash
  touch mon_fichier.txt
  ```

  <p align="center" alt="drawing">
      <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_04_Scripts_090224/img/touch.png" width="850" height="100"><br>
  </p>

  <p align="center" alt="drawing">
      <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_04_Scripts_090224/img/touch_cree.png" width="850" height="200"><br>
  </p>

---

## `nano`

* éditer les fichiers en ligne de commande avec l'éditeur `nano`

  ```bash
  nano mon_fichier.txt
  ```

  <p align="center" alt="drawing">
      <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_04_Scripts_090224/img/nano.png" width="1000" height="100"><br>
  </p>

  * la fenêtre ci-contre apparaîtra, où nous pouvons écrire du texte :

    <p align="center" alt="drawing">
        <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_04_Scripts_090224/img/nano_ouvert.png" width="900" height="250"><br>
    </p>

---

## `nano`

* pour sortir et enregistrer le fichier, taper successivement `Ctrl + X` puis `O` (oui)

* pour finir, valider avec la touche Entrée

* les instructions sont toujours affichées en bas de l'écran

  <div class="container-side">
    <figure>
      <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_04_Scripts_090224/img/nano_ouvert.png" width="720" height="190" alt="">
      <figcaption>
        Sortir : <tt>Ctrl + X</tt>
      </figcaption>
    </figure>
      <figure>
  <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_04_Scripts_090224/img/nano_sauvegarde.png" width="720" height="190" alt="">
              <figcaption>
        Enregistrer le fichier : <tt>O</tt>, Entrée
      </figcaption>
  </figure>

---

## Exercice 1 : créer un fichier `.txt`

1. créer un nouveau fichier `test.txt`
2. y écrire le contenu suivant : *Bonjour le monde*.
3. sortir de l'éditeur de texte et enregistrer le fichier
4. vérifier la présence du fichier dans le répertoire courant 
   1. utiliser la commande déjà abordée aux cours précédents

---

## Solution de l'exercice 1

1. `nano test.txt`
2. saisie du texte *Bonjour le monde*. 
3. `Ctrl + X`, `O`
4. `ls`

---

## Lecture du fichier : `cat`

* la commande `cat` permet de lire le contenu du fichier

  ```bash
  cat mon_fichier.txt
  ```

  <p align="center" alt="drawing">
      <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_04_Scripts_090224/img/cat.png" width="850" height="200"><br>
  </p>

---

## Redirection du contenu : `>` et `>>`

* créer le fichier `source.txt` et y écrire le message « Ceci est un autre fichier.

* pour rediriger le contenu du fichier `source` vers le fichier `destination`,  utiliser l’option `>` 

  ```bash
  cat source.txt > destination.txt
  ```

* pour **ajouter** le contenu dans le fichier de destination, utiliser l'option `>>`

  ```bash
  cat source.txt >> destination.txt
  ```

  <div style="padding: 15px; border: 1px solid transparent; border-color: transparent; margin-bottom: 20px; border-radius: 4px; color: #8a6d3b;; background-color: #fcf8e3; border-color: #faebcc;">
  Le <tt>></tt> est l'opérateur de redirection de sortie utilisé pour <b>écraser</b> les fichiers qui existent déjà dans le répertoire. Bien que le <tt>>></tt> soit également un opérateur de sortie, il <b>ajoute</b> les données d'un fichier existant.
  </div>

---

## Recherche du texte : `grep`

* pour faire des recherches du texte dans un fichier, utiliser la commande `grep` :

  ```bash
  grep "Ceci" source.txt
  ```

* on peut faire des requêtes en utilisant les expressions régulières (*regex*).

  * trouver tous les mots commençant par la lettre « C » en majuscule

    ```bash
    grep -Eo "C\w+" source.txt
    ```

    <small-text>`-E` : expression rationnelle étendue (≠ expression rationnelle simple `-G`)</small-text>

    <small-text>`-o` : n'afficher que l'occurrence en question (*match*)</small-text>

    <small-text>`C` : le caractère littéral « C »</small-text>

    <small-text>`\w+` : un ou plusieurs caractères alphabétiques<small-text>

---

## Créer un script

* on peut créer des scripts *shell* pour automatiser certaines tâches 
  * traitement des données, la manipulation de fichiers, etc.

* on crée un script shell avec la commande `nano mon_script.sh`

  * on utilise l'extension `.sh` pour nommer les scripts (fichier *shell*)

  <p align="center" alt="drawing">
      <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_04_Scripts_090224/img/nano_script.png" width="1000" height="100"><br>
  </p>

---

## Créer un script

* on déclare le type de document avec un appel de script (***shebang***) 

  ```bash
  #!/bin/bash
  ```

  * <small-text>cela indique que le fichier n'est pas un fichier binaire mais un script</small-text>

* on écrit le texte suivant dans l'éditeur de texte `nano` :

  ```bash
  echo "Bonjour le monde"
  ```

* on sort de l'éditeur et on enregistre le fichier (*cf.* p. 5) 

  <p align="center" alt="drawing">
      <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_04_Scripts_090224/img/nano_bonjour.png" width="550" height="180"><br>
  </p>

---

## Fichier créé

* le fichier `mon_script.sh` est enregistré dans le répertoire courant
* quand on l'ouvre, on voit qu'il contient du texte saisi lors de l'étape précédente
  * commande qui permet d'afficher le texte « Bonjour le monde »

<p align="center" alt="drawing">
    <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_04_Scripts_090224/img/resultat_bonjour.png" width="1300" height="100"><br>
</p>

---

## Exécution du script 

* avant de lancer le script, le `mon_script.sh` doit être **exécutable** 

  * pour lancer le script, taper `sh mon_script.sh` ou `bash mon_script.sh`

  * le message « Bonjour le monde » s'affiche

    <div class="container-side">
      <figure>
        <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_04_Scripts_090224/img/execution_sh.png" width="550" height="100" alt="">
        <figcaption>
          <tt>sh mon_script.sh</tt>
        </figcaption>
      </figure>
        <figure>
    <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_04_Scripts_090224/img/execution_bash.png" width="550" height="100" alt="">
                <figcaption>
          <tt>bash mon_script.sh</tt>
        </figcaption>
    </figure>

---

## Exécution du script (Windows)

* autre manière d'exécuter le script :

  ```bash
  ./mon_script.sh
  ```

  * <small-text>si vous obtenez le message d'erreur : `bash: ./mon_script.sh: Permission non accordée`, il faut rendre le fichier exécutable en tapant `chmod +x mon_script.sh` et puis relancer le script `./mon_script.sh`</small-text>

    <p align="center" alt="drawing">
        <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_04_Scripts_090224/img/chmod.png" width="1000" height="300"><br>
    </p>

---

## Exercice 2 : créer un script `.sh`

1. créer un script `list.sh`
2. y écrire le *shebang*, puis la commande `ls`
3. sortir de l'éditeur de texte et enregistrer le fichier
4. vérifier la présence du fichier dans le répertoire courant 
5. lancer le script et expliquer le résultat
   1. si besoin, rendre le fichier exécutable
6. créer une copie de ce script (`list_copie.sh`) dans le répertoire courant
7. supprimer la copie créée

---

## Solution de l'exercice 2

<ol style="line-height: 40px">
    <li><tt>nano list.sh</tt></li>
    ou <tt>touch list.sh</tt>, puis <tt>nano list.sh</tt>
    <li><tt>!#/bin/bash</tt></li>
    <tt>ls</tt>
    <li><tt>Ctrl + X</tt>, puis <tt>O</tt></li>
    <li><tt>ls</tt></li>
    <li><tt>sh list.sh</tt></li>
    ou <tt>bash list.sh</tt>
    <br>ou <tt>chmod +x list.sh</tt>, puis <tt>./list.sh</tt>
    <br>Ce script affiche le contenu du répertoire courant.
    <li><tt>cp list.sh list_copie.sh</tt></li>
    <li><tt>rm list_copie.sh</tt></li>

</ol>

---

## Commentaires

* un commentaire sert à améliorer la lisibilité du script

* il est placé en le faisant précéder du caractère **dièse** (ou croisillon, « **#** »)

* tout ce qui suit la dièse est ignoré (non exécuté) jusqu'à la fin de la ligne  

* cela permet de mettre un commentaire sur une ligne d'instructions

* l'espace sépare la fin de l'instruction et le début du commentaire

  ```bash
  #!/bin/bash 
  # Ceci est un commentaire dans mon script shell qui ne va pas être exécuté.
  ls # Cette ligne indique la commande qui affiche le contenu du répertoire courant.
  ```

---

## Exercice 3 : créer un script avec un commentaire

1. créer un script `date.sh` 
2. y écrire 
   1. le *shebang*
   2. le commentaire « Ce programme affiche la date »
   3. la commande `date` suivi du commentaire « Cette ligne affiche la date »

3. sortir de l'éditeur de texte et sauvegarder le script créé
4. lancer le script et expliquer le résultat

---

## Solution de l'exercice 3

<ol>
    <li><tt>nano date.sh</tt></li>
    ou <tt>touch date.sh</tt>, puis <tt>nano date.sh</tt>

</ol>

2. ```bash
   #!/bin/bash 
   # Ce programme affiche la date 
   date # Cette ligne affiche la date
   ```

3. `Ctrl + X`, puis `o`

4. `sh date.sh`

   `bash date.sh`

   `chmod +x date.sh`, puis `./date.sh`

   Ce script affiche et définit la date et l'heure du système.

---

## Variables

Le shell permet de définir et réutiliser des variables :

```bash
message="qui suis-je ?"
echo $message
qui suis-je ?
```

<div style="padding: 15px; border: 1px solid transparent; border-color: transparent; margin-bottom: 20px; border-radius: 4px; color: #8a6d3b;; background-color: #fcf8e3; border-color: #faebcc;">
Il ne faut <b>pas</b> d'espace autour du signe <tt>=</tt>.
</div>

<div style="padding: 15px; border: 1px solid transparent; border-color: transparent; margin-bottom: 20px; border-radius: 4px; color: #31708f; background-color: #d9edf7; border-color: #bce8f1;">
Les guillemets sont nécessaires si la valeur de la variable contient des espaces.
</div>

Le méta-caractère dollar (`$`), suivi d'un nom de variable (`message`), est remplacé par la valeur de la variable en question (`qui suis-je ?`).

<span style="float:right; font-size: 18px">([Champin, 2020](https://perso.liris.cnrs.fr/pierre-antoine.champin/enseignement/linux/s5.html))

---

## Variables : méta-caractère `$`

* le méta-caractère `$` n'est pas inhibié par les guillemets doubles (`""`)

  ```bash
  $ echo "J'ai une question : $message"
  J'ai une question : qui suis-je ?
  ```

* en revanche, il l'est par les guillemets simples (`'`)

  ```bash
  $ echo 'J'ai une question $message'
  > # la commande ne s'exécute pas
  ```

  <span style="float:right; font-size: 18px">Adapté de [Champin (2020)](https://perso.liris.cnrs.fr/pierre-antoine.champin/enseignement/linux/s5.html)

---

## Exercice 4 : créer un script contenant une variable

1. créer un script `coucou.sh`
2. y écrire le *shebang*
3. affecter la valeur `Michel` à la variable `nom`
4. formuler la commande d'affichage du message « Coucou [nom] »
   1. on récupère la valeur de `nom` à partir de la variable déclarée à l'étape 3.
5. ajouter le commentaire « Cette ligne affiche le nom 'Michel' »
6. sortir de l'éditeur de texte et enregistrer le script
7. lancer le script et expliquer le résultat

---

## Solution de l'exercice 4 

1. `nano coucou.sh`

   ou `touch coucou.sh`, puis `nano coucou.sh`

2. `#!/bin/bash`

3. `nom="Michel"`

4. `echo "Coucou $nom"`

5. `# Cette ligne affiche le nom 'Michel'`

6. `Ctrl + X`, puis `O`

7. `sh coucou.sh`

   `bash coucou.sh`

   `chmod+x coucou.sh`, puis `./coucou.sh`

---

## Affecter le résultat d'une commande à une variable

Introduisons une nouvelle variable `date_actuelle`.

Pour stocker le résultat d'une commande dans cette variable :

* mettre la commande entre parenthèses, précédées par un `$`

  ```bash
  date_actuelle=$(date)
  ```

* ou mettre la commande entre les accents graves ``

  ```bash
  date_actuelle=`date`
  ```

---

## Exercice 5 : créer un script contenant une variable II

1. créer un script `variable.sh` 

2. ajouter le *shebang*
3. stocker la commande `date` dans la variable `date_actuelle`
4. formuler la commande d'affichage du message « Aujourd'hui on est `date` »
   1. on récupère la valeur de `date` à partir de la variable déclarée à l'étape 3.
5. ajouter le commentaire « Cette ligne affiche la date »
6. sortir de l'éditeur du texte et enregistrer le script
7. lancer le script et expliquer le résultat

---

## Solution de l'exercice 5

<ol style="line-height: 40px">
    <li><tt>nano variable.sh</tt></li>
    ou <tt>touch variable.sh</tt>, puis <tt>nano variable.sh</tt>
    <li><tt>#!/bin/bash</tt></li>
    <li><tt>date_actuelle=$(date)</tt></li>
    <li><tt>echo "Aujourd'hui on est $date_actuelle"</tt></li>
    <li><tt># Cette ligne affiche la date</tt></li>
    <li><tt>Ctrl + X</tt>, puis <tt>O</tt></li>
    <li><tt>sh variable.sh</tt></li>
    <tt>bash variable.sh</tt>
    <br><tt>chmod +x variable.sh</tt>, puis <tt>./variable.sh</tt>
</ol>



---

## Avantages de l'utilisation de la ligne de commande

* **Flexibilité** : combiner les commandes et obtenir une palette pratiquement infinie de fonctions nouvelles
* **Fiabilité** : tendance à s'exécuter de la même manière sur différents SE (« couteau suisse »)
* **Rapidité** : automatisation des tâches à grande échelle (p. ex. renommer un ensemble des fichiers d'un seul coup)
* **Expérience** : communiquer avec l'ordinateur plus directement qu'avec les interfaces graphiques, en apprenant ainsi énormément sur son fonctionnement interne
* **Économisation des ressources** : utilise les ressources de l'ordinateur beaucoup plus parcimonieusement que les programmes graphiques

<small-text>Source : [Floss Manuals](https://fr.flossmanuals.net/introduction-a-la-ligne-de-commande/introduction/)</small-text>

---

  ## Références

<ul style="font-size: 20px">
    <li><b>Brunet, É. & Thomas, G.</b> (<i>s. d.</i>). « Le shell bash » [<i>diapositives</i>]. Télécom SudParis. <a href="http://www-inf.telecom-sudparis.eu/cours/CSC3102/Supports/ci1-bash/ci-bash.pptx.pdf">http://www-inf.telecom-sudparis.eu/cours/CSC3102/Supports/ci1-bash/ci-bash.pptx.pdf</a></li>
    <li><b>Combeau, M.</b> (2022). « La différence entre le terminal, la console et le shell ». <a href="https://www.codequoi.com/difference-entre-terminal-console-et-shell/">https://www.codequoi.com/difference-entre-terminal-console-et-shell/</a></li>
    <li><b>Champin, P.-A.</b> (2020). Séance 5 : Automatisation et scripts. Département Informatique (IUT Lyon 1). <a href="https://perso.liris.cnrs.fr/pierre-antoine.champin/enseignement/linux/s5.html">https://perso.liris.cnrs.fr/pierre-antoine.champin/enseignement/linux/s5.html</a></li>
    <li><b>Rebora, S.</b> (2022). « Connaître son propre ordinateur » [<i>dépôt GitHub</i>]. EnExDi2022. <a href="https://github.com/ABC-DH/EnExDi2022/tree/main/materials/1_KnowYourComputer/slides">https://github.com/ABC-DH/EnExDi2022/tree/main/materials/1_KnowYourComputer/slides</a>
  </li>
    <li><b>Gabay, S.</b> (2022). « Les lignes de commandes et Bash » [<i>dépôt GitHub</i>]. Université de Genève, Chaire des humanités numériques, Faculté des Lettres. <a href="https://github.com/gabays/Fondamentaux/blob/main/Lignes_de_commandes/DistRead_1_2.pdf">https://github.com/gabays/Fondamentaux/blob/main/Lignes_de_commandes/DistRead_1_2.pdf</a>
    </li>
    <li><b>Diaz, D.</b> (2023). « Les 40 commandes Linux les plus utilisées que vous devez connaître ». Kinsta. <a href="https://kinsta.com/fr/blog/commandes-linux/">https://kinsta.com/fr/blog/commandes-linux/</a>
    </li>
    <li><b>Xyoos</b> (<i>s.d.</i>). « Interface graphique ». <a href="https://cours-informatique-gratuit.fr/dictionnaire/interface-graphique/">https://cours-informatique-gratuit.fr/dictionnaire/interface-graphique/</a></li>
</ul>


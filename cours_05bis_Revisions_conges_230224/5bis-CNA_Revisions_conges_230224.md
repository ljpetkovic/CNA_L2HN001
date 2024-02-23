---
marp: true
theme: default
markdown.marp.enableHtml: true
paginate: true
extra: true
footer: "Cultures numériques avancées, licence <i>Sciences du langage</i>, mineure HN (L2HN001), 23/02/2024, Ljudmila PETKOVIC"
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

  #### Récapitulatif : Bash et commandes essentielles

  ###### Ljudmila PETKOVIC

<small-text><a href="mailto:ljudmila.petkovic@sorbonne-nouvelle.fr">`ljudmila.petkovic@sorbonne-nouvelle.fr`</a></small-text>

  <br>

  

  <small-text> 

Cultures numériques avancées (L2HN001)
Licence *Sciences du langage*, mineure « Humanités numériques »
Paris, le 23 février 2024, année 2023-2024

  </small-text>

<smaller-text>*Diapositives adaptées de [Simon Gabay](https://github.com/gabays/Fondamentaux/blob/main/Lignes_de_commandes/DistRead_1_2.pdf), [Simone Rebora](https://github.com/ABC-DH/EnExDi2022/tree/main/materials/1_KnowYourComputer/slides) et [Élisabeth Brunet et Gaël Thomas](http://www-inf.telecom-sudparis.eu/cours/CSC3102/Supports/ci1-bash/ci-bash.pptx.pdf)*.</smaller-text>

<!--<smaller-text>*Diapositives adaptées de [Simon Gabay](https://github.com/gabays/Fondamentaux/blob/main/Lignes_de_commandes/DistRead_1_2.pdf) et de [Simone Rebora](https://github.com/ABC-DH/EnExDi2022/tree/main/materials/1_KnowYourComputer/slides)*.</smaller-text>-->

<div style="position:relative; top:-220px; left:0px; margin-left:860px; margin-right:0px; font-size:14px;">
  Source :  <a href="https://kinsta.com/fr/blog/commandes-linux/">Diaz, 2023.</a>
</div>


---

# Utilisation de la ligne de commande

---

## Ouvrir le terminal

Pour **Linux** : 

* appuyer simultanément sur les touches `Ctrl` + `Alt` + `T` 

* ouvrez la barre de recherche, tapez `terminal` et appuyez sur Entrée

  <p align="center" alt="drawing">
      <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_02_Bash_260124/img/terminal_linux.png" width="500" height="330"><br>
  </p>

---

## Ouvrir le terminal

Pour **Mac** :

* ouvrez la barre de recherche, tapez `terminal` et appuyez sur Entrée

* ou cliquer sur `Terminal.app`  dans `Applications` > `Utilitaires`

  <p align="center" alt="drawing">
      <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_02_Bash_260124/img/terminal_mac.png" width="500" height="330"><br>
  </p>

---

## Ouvrir le terminal

Pour **Windows** : 

⚠️ Windows dispose de deux *shells* – `Command Prompt` et `PowerShell` qui ne fonctionnent pas de la même manière que ceux sur Linux ou Mac.

<div style="padding: 15px; border: 1px solid transparent; border-color: transparent; margin-bottom: 20px; border-radius: 4px; color: #a94442; background-color: #f2dede; border-color: #ebccd1;">
Ce n'est pas possible d'exécuter toutes les commandes Bash sur Windows, sauf si l'on n'utilise pas certaines commandes équivalentes, adaptées à Windows.
</div>


<div style="padding: 15px; border: 1px solid transparent; border-color: transparent; margin-bottom: 20px; border-radius: 4px; color: #8a6d3b;; background-color: #fcf8e3; border-color: #faebcc;">
Pour contourner ce problème, les utilisateurs de Windows peuvent télécharger <a href="https://git-scm.com/download/win">Git Bash</a> (émulateur de terminal Bash sur Windows).
</div>


---

## Git Bash pour Windows

* Téléchargez Git Bash depuis le site officiel de Git ([lien](https://git-scm.com/download/win))

* Suivez les étapes d'installation indiquées dans ce [tutoriel](https://adamtheautomator.com/git-bash/) + [tutoriel vidéo](https://www.youtube.com/watch?v=USZqL4QDXjU)

  * Pour l'étape 4., choisir l'option `Use Vim (the ubiquitous text editor) as Git's default editor`

* Suite à l'installation du Git Bash, assurez-vous de son bon fonctionnement en l'ouvrant et en tapant :

  ```bash
  git --version
  ```

---

## Raccourcis pour copier-coller (facultatif)

À priori, les raccourcis pour *copier* et coller sont les suivants :

* copier : `Ctrl + Shift + C`
* coller : `Ctrl + Insert` ou `Shift + Insert`

<small-text>Pour activer le raccourci `Ctrl + Shift + V` pour coller :</small-text>

<small-text>1. Clic droit > `Options...`</small-text>
<small-text>2. Dans l'onglet Keys, cochez `Ctrl + Shift + letter shortcuts`</small-text>

<p align="center" alt="drawing">
    <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_05bis_Revisions_conges_230224/img/git_raccourci_copier_coller.png" width="300" height="230"><br>
</p>


---

## Les commandes abordées jusqu'à présent

Pour chaque commande, vous trouverez :

* sa description
* ses options courantes (si elles nous sont pertinentes)
* quelques exemples de son utilisation 

<div style="padding: 15px; border: 1px solid transparent; border-color: transparent; margin-bottom: 20px; border-radius: 4px; color: #8a6d3b;; background-color: #fcf8e3; border-color: #faebcc;">
L'objectif est de mémoriser ces commandes basiques et de comprendre la logique de leurs fonctionnements.
</div>

<div style="padding: 15px; border: 1px solid transparent; border-color: transparent; margin-bottom: 20px; border-radius: 4px; color: #31708f; background-color: white; border-color: #bce8f1;">
Pour tous les autres détails, référez-vous aux diapositives des <a href="https://icampus.univ-paris3.fr/course/view.php?id=44401">séances 1-5</a>.
</div>

---

##### `pwd` 

* angl. ***p**rint **w**orking **d**irectory*

* affiche le répertoire courant

* montre où nous sommes dans le système des fichiers et des répertoires

  ```bash
  pwd
  ```

---

##### `ls`

* angl. _**l**i**s**t_

* liste le contenu du répertoire courant :

  ```bash
  ls
  ```

* liste le contenu d'un autre répertoire donné en paramètre :

  ```bash
  ls mon_dossier
  ```

* options courantes : `-a` (pour afficher les fichiers cachés dont le nom commence par un point `.`, p. ex. `.fichier_cache.txt`)

  ```bash
  ls -a
  ```


---

##### `cd`

* angl. ***c**hange **d**irectory*

* change le répertoire courant

  ```bash
  cd # se placer dans le répertoire personnel ('home')
  ```

---

##### `cd` + chemin absolu / relatif

* chemin absolu (chemin à partir du répertoire-racine `/`)

  ```bash
  cd /home/Utilisateur/Documents/
  ```

* chemin relatif

  ```bash
  cd .. # remonter d'un répertoire (aller à son 'parent')
  ```

  ```bash
  cd ../.. # remonter de deux dossiers (aller à son 'grand-parent')
  ```

  ```bash
  cd Documents # accéder au répertoire 'Documents' depuis le répertoire actuel
  ```

  ```bash
  cd Utilisateur/Documents # accéder au répertoire 'Documents' via le répertoire 'Utilisateur'
  ```

---

##### `cp`

* **c**o**p**ie un fichier 

  ```bash
  cp fichier_original.txt fichier_copie.txt
  ```

* options courantes : `-r`

  * copie un répertoire, si l'option `-r` est utilisée)

    ```bash
    cp -r repertoire_original repertoire_copie
    ```


---

##### `mv`

* angl. _**m**o**v**e_

* **déplace** un fichier dans un répertoire

  ```bash
  mv fichier.txt Documents
  ```

* déplace un répertoire dans un répertoire

  ```bash
  mv mon_dossier Documents
  ```

* **renomme** un fichier

  ```bash
  mv fichier.txt fichier_renomme.txt
  ```

* renomme un répertoire

  ```bash
  mv repertoire repertoire_renomme
  ```

---

##### `rm`

* angl. _**r**e**m**ove_

* supprime un fichier 

  ```bash
  rm fichier_a_supprimer.txt
  ```

* options courantes : `-r`

  * supprime un répertoire, si l'option `-r` est utilisée

    ```bash
    rm -r repertoire_a_supprimer
    ```


---

##### `touch`

* crée un fichier

  ```bash
  touch mon_script.sh
  ```

---

##### `nano`

* éditeur de texte en ligne de commande (*suivez les instructions de l'éditeur en bas de l'écran*.)

  ```bash
  nano mon_script.sh
  ```

* ajouter un appel de script (*shebang*) suivi par votre script (p. ex. une commande)

  ```bash
  #!/bin/bash
  echo "Coucou"
  ```

  <small-text>Pour quitter : `Ctrl + X` → *Sauver l'espace modifié ?* `O` (ou `Y`, si votre Terminal est configuré en anglais) → *Nom du fichier à écrire :* `mon_script.sh` (valider par Entrée)</small-text>

---

##### `echo`

* affiche un message (ou les résultats d'autres commandes), ici une **chaîne de caractères**

  ```bash
  echo "Coucou René"
  ```

  * une chaîne de caractère peut être stockée dans une **variable** (p. ex. `nom`) 

    ```bash
    nom="Michel"
    ```

  * quand on appelle une variable, on ajoute le signe du dollar `$` avant son nom

    ```bash
    echo "Coucou $nom"
    ```

---

##### `grep`

* angl. _**g**lobal **r**egular **e**xpression **p**rint_

* recherche une chaîne de caractères dans des fichiers 

  * recherche simple 

    ```bash
    grep "Ceci" fichier_test.txt
    ```

  * recherche avancée

    * options courantes : `-E` (regex), `-o`, `-i`

    * recherche en utilisant les expressions régulières (**regex**), p. ex. « trouver tous les mots commençant par la lettre « C » en majuscule »

      ```bash
      grep -E "C\w+" fichier_test.txt
      ```


---

##### `bash` ou `sh`

* exécute un script *shell* (avec l'extension `.sh`)

  ```bash
  bash mon_script.sh
  ```

  ```bash
  sh mon_script.sh
  ```

* la commande `bash` peut être enlevée :

  ```bash
  ./mon_script.sh
  ```

  <small-text>Si vous obtenez un message d'erreur : `bash: ./mon_script.sh: Permission non accordée`, il faut donner au fichier la permission d'exécution (le rendre exécutable) en tapant `chmod +x mon_script.sh`, et ensuite relancer la commande ci-dessus.</small-text>

---

##### `mkdir`

* angl. _**m**a**k**e **dir**ectory_

* crée un répertoire

  ```bash
  mkdir repertoire
  ```

---

##### `cat`

* angl. _con**cat**enate_

* lire le contenu du fichier

  ```bash
  cat mon_fichier.txt
  ```


---

## Redirection du contenu : `>` et `>>`

* pour **rediriger** le contenu du fichier `source.txt` vers le fichier `destination.txt`,  utiliser l’option `>` :

  <div style="padding: 15px; border: 1px solid transparent; border-color: transparent; margin-bottom: 20px; border-radius: 4px; color: #8a6d3b;; background-color: #fcf8e3; border-color: #faebcc;">
  Une redirection avec <tt>></tt> sur un fichier qui existe déjà efface le contenu du fichier avant d'y placer le résultat de la commande.
  </div>

  ```bash
  cat source.txt > destination.txt
  ```

* pour **ajouter** le contenu dans le fichier de destination, utiliser l'option `>>`

  ```bash
  cat source.txt >> destination.txt
  ```


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

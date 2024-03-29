---
marp: true
theme: default
markdown.marp.enableHtml: true
paginate: true
extra: true
footer: "Cultures numériques avancées, licence <i>Sciences du langage</i>, mineure HN (L2HN001), 29/03/2024, Ljudmila PETKOVIC"
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

li li { font-size: 90%; }   

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

  #### GitHub et GitHub Desktop

  ###### Ljudmila PETKOVIC

<small-text><a href="mailto:ljudmila.petkovic@sorbonne-nouvelle.fr">`ljudmila.petkovic@sorbonne-nouvelle.fr`</a></small-text>

  <br>

  

  <small-text> 

Cultures numériques avancées (L2HN001)
Licence *Sciences du langage*, mineure « Humanités numériques »
Paris, le 29 mars 2024, année 2023-2024

  </small-text>

<!--<smaller-text>*Diapositives adaptées de l'[IUT Lyon 1](https://perso.liris.cnrs.fr/pierre-antoine.champin/enseignement/intro-git/)* *et de [Thibault Clérice](https://github.com/PonteIneptique/cours-git)*</smaller-text>-->

<smaller-text>*Diapositives adaptées de [O'clock](https://oclock.io/tuto-github-lutiliser) et de [GitHub, Inc.](https://docs.github.com/fr/desktop/overview/getting-started-with-github-desktop)*</smaller-text>

<div style="position:relative; top:-220px; left:0px; margin-left:860px; margin-right:0px; font-size:14px;">
  Source :  <a href="https://kinsta.com/fr/blog/commandes-linux/">Diaz, 2023.</a>
</div>




---

## [Git](https://git-scm.com/) : un outil de versionnage (rappel)

- plusieurs applications :

  - gestion de code source<sup>1</sup> pour les projets logiciels 

    <span style="font-size: 50%; line-height: 20px; display:block"><sup>1</sup> texte qui présente les instructions composant un programme sous une forme lisible, telles qu'elles ont été écrites dans un langage de programmation.</span>

  - rédaction de la documentation

  - création d'un site web

- permet un travail collaboratif, grâce à la :

  - facilité d’échange
  - traçabilité
  - gestion des conflits

---

## Git

* Git fonctionne en créant une copie locale (angl. *clone*) du projet sur un ordinateur
* on peut apporter des modifications à ces fichiers 
* on peut enregistrer chaque modification sous forme de  « commit »
  * les commits servent de points de contrôle dans l’historique du projet
  * un commit est accompagné d’un message expliquant les changements effectués
  * ces messages permettent de comprendre ce qui a été modifié à chaque étape
    * un bel avantage pour le suivi de projet

---

## GitHub

* plateforme de développement collaboratif basée sur Git
* permet aux développeurs de partager, gérer et collaborer sur des projets
* facilite la gestion du code source et la collaboration entre les membres
* fonctionnalités avancées pour suivre les problèmes / demandes de modifications
* référence dans le domaine
* transparence, productivité et collaboration dans le développement logiciel
* peut fusionner les modifications, ce qui facilite le travail en collaboration

---

## 1️⃣ Inscription sur GitHub

1. Accédez à https://github.com/.

2. Cliquez sur **Sign Up** (« s'inscrire »).

3. Suivez les invites pour créer votre compte personnel.

   <p align="center">
     <img width="800" height="350" style="margin-right:10px; vertical-align:bottom" src="img/signup.png">
   </p>

---

### GitHub – côté utilisateur·trice

<p align="center">
  <img width="1000" height="530" style="margin-right:10px; vertical-align:bottom" src="img/github.png">
</p>

---

### GitHub Desktop

* application *open source*<sup>1</sup> gratuite qui permet d’utiliser du code hébergé sur GitHub ou sur d’autres services d’hébergement Git (p. ex. [GitLab](https://about.gitlab.com/))

  <span style="font-size: 50%; line-height: 20px; display:block"><sup>1</sup> code source que l'on rend disponible gratuitement pour qu'il puisse être modifié et redistribué, dans un contexte de développement communautaire ([Office québécois de la langue française, 2002](https://archive.wikiwix.com/cache/index2.php?url=https%3A%2F%2Fvitrinelinguistique.oqlf.gouv.qc.ca%2Fredirection%2Fficheuid%2F8362923#federation=archive.wikiwix.com&tab=url)).</span>

* effectue des commandes Git : 

  * validation / spécification (angl. *commit*) des modifications
  * envoi (angl. *push*) de modifications, dans une GUI

* alternative à l'utilisation de la ligne de commande

---

## 2️⃣ Télécharger et installer GitHub Desktop (Windows)

* [tutoriel](https://docs.github.com/en/desktop/installing-and-authenticating-to-github-desktop/installing-github-desktop?platform=windows)

  <p align="left">  <img width="480" height="400" style="margin-left:10px; vertical-align:left" src="img/github_desktop.png">      <img width="500" height="400" style="margin-right:10px; vertical-align:right" src="img/github_desktop_telecharger.png"></p>

---

##  2️⃣ Télécharger et installer GitHub Desktop (Mac)

* [tutoriel](https://docs.github.com/en/desktop/installing-and-authenticating-to-github-desktop/installing-github-desktop?platform=mac)

  <p align="left">  <img width="480" height="400" style="margin-left:10px; vertical-align:left" src="img/github_desktop_mac.png">      <img width="500" height="400" style="margin-right:10px; vertical-align:right" src="img/github_desktop_telecharger_mac.png"></p>

---

## 2️⃣ Télécharger et installer GitHub Desktop

1. Visitez la [page](https://desktop.github.com/) de téléchargement de GitHub Desktop.     
2. Cliquez sur **Télécharger** (Windows ou Mac).
3. Dans le dossier `Téléchargements` de votre ordinateur, double-cliquez sur le fichier d'installation, p. ex. :
   1. `GitHubDesktopSetup-x64.exe` pour Windows 
   2. `GitHubDesktop-x64.zip` pour Mac.     
4. Lancer GitHub Desktop une fois l'installation terminée.

---

### GitHub Desktop – interface graphique

<p align="center">
  <img width="700" height="500" style="margin-right:10px; vertical-align:bottom" src="img/github_desktop_gui.png">
</p>

---

##  3️⃣ Authentification

* une fois GitHub Desktop installé, authentifiez-vous avec votre compte GitHub

* permet de vous connecter à des dépôts distants sur GitHub

  <p align="center">
    <img width="700" height="400" style="margin-right:10px; vertical-align:bottom" src="img/github_desktop_auth.png">
  </p>

---

## 4️⃣ Configuration et personnalisation de GitHub Desktop

* vous pouvez configurer l'application pour l'adapter au mieux à vos besoins

  * connecter / supprimer des comptes GitHub, choisir un éditeur de texte ou un interpréteur de commandes par défaut...

  <p align="center">
    <img width="700" height="400" style="margin-right:10px; vertical-align:bottom" src="img/github_desktop_config.png">
  </p>



---

## :five: Créer un dépôt

* sélectionner `File` dans la barre de menus > `New repository...`

* nommez le dépôt, donnez-lui une description est cliquez sur `Create repository`

* le dépôt est créé sur votre ordinateur dans le répertoire indiqué dans le champ `Local path` (p. ex. `/home/ljudmila/Documents/GitHub`)

  <p align="center">
    <img width="350" height="300" style="margin-right:10px; vertical-align:bottom" src="img/repo.png">
  </p>

---

### Retrouver le dépôt créé en local

* après avoir créé le dépôt, trouvez le répôt sur votre ordinateur en suivant le chemin correspondant

  <p align="center">
    <img width="1000" height="200" style="margin-right:10px; vertical-align:bottom" src="img/github_desktop_test.png">
  </p>

---

## :six: Ajouter un fichier : créer une documentation en Markdown

* ouvrez un fichier Markdown (`.md`) avec un éditeur Markdown (p. ex. [Typora](https://typora.io/))
* utilisez l'en-tête 1 pour écrire « Ma première documentation en Markdown », suivi d'un paragraphe contenant le mot « Coucou »
* sauvegarder le fichier sous le nom `README.md` (pour que son contenu soit visible sur la page d'accueil du dépôt créé)

<p align="center">
  <img width="550" height="300" style="margin-right:10px; vertical-align:bottom" src="img/README.png">
</p>

---

### Observer les modifications effectuées dans GitHub Desktop

* revenez sur GitHub Desktop et observer les modifications effectuées dans le fichier `README.md`

<p align="center">
  <img width="750" height="450" style="margin-right:10px; vertical-align:bottom" src="img/modifs.png">
</p>

---

## :seven: *Commiter* vos modifications

* dans le champ dédié à l'écriture des commits, écrivez : « créé une documentation » et cliquez sur le bouton `Commit to main`

  <p align="center">
    <img width="750" height="450" style="margin-right:10px; vertical-align:bottom" src="img/commit.png">
  </p>

---

## :eight: *Pusher* vos modifications

* pour publier vos modifications sur GitHub, cliquez sur `Push origin` ou `Repository > Push`

<p align="center">
  <img width="750" height="450" style="margin-right:10px; vertical-align:bottom" src="img/push.png">
</p>

---

### Votre dépôt distant sur GitHub

* retrouvez votre dépôt créé dans la liste des dépôts dans votre compte GitHub

<p align="left">  <img width="520" height="300" style="margin-left:10px; vertical-align:left" src="img/depot_distant.png">      <img width="530" height="300" style="margin-right:10px; vertical-align:right" src="img/depot_distant_2.png"></p>

---

## Cloner un dépôt distant

* cliquez sur `File` > `Clone repository`

* dans l'onglet `URL` `Repository URL or GitHub username and repository` saisissez le lien URL suivant `https://github.com/ljpetkovic/depot_CNA` 

* le `Local path` spécifie l'adresse où `depot_CNA` sera hébergé (ne pas changer)

  <p align="center">
    <img width="650" height="350" style="margin-right:10px; vertical-align:bottom" src="img/clone.png">
  </p>

---

## État du dépôt cloné

* vous avez désormais accès au dépôt que vous venez de cloner

<p align="center">
  <img width="750" height="450" style="margin-right:10px; vertical-align:bottom" src="img/depot_clone.png">
</p>

---

  ## Références

<ul style="font-size: 20px">
        <li><b>GitHub, Inc.</b>. (2024). <a href="https://docs.github.com/fr/desktop/overview/getting-started-with-github-desktop"><i>Bien démarrer avec GitHub Desktop</a></i>. Documentation GitHub.</li>
    <li><b>O'clock.</b> (2023, juillet 13). <a href="https://oclock.io/tuto-github-lutiliser">Tuto GitHub : comment l’utiliser ?</a>.</li>
    <li><b>Office québécois de la langue française</b>. (2002). <a href="https://archive.wikiwix.com/cache/index2.php?url=https%3A%2F%2Fvitrinelinguistique.oqlf.gouv.qc.ca%2Fredirection%2Fficheuid%2F8362923#federation=archive.wikiwix.com&tab=url">code source libre</a>. Dans <i>Office québécois de la langue française</i>. Consulté le 28 mars 2024.</li>

</ul>


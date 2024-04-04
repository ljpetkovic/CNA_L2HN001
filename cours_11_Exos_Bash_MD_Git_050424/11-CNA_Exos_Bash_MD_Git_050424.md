---
marp: true
theme: default
markdown.marp.enableHtml: true
paginate: true
extra: true
footer: "Cultures numériques avancées, licence <i>Sciences du langage</i>, mineure HN (L2HN001), 05/04/2024, Ljudmila PETKOVIC"
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

  #### Exercices Bash, Markdown et Git

  ###### Ljudmila PETKOVIC

<small-text><a href="mailto:ljudmila.petkovic@sorbonne-nouvelle.fr">`ljudmila.petkovic@sorbonne-nouvelle.fr`</a></small-text>

  <br>

  

  <small-text> 

Cultures numériques avancées (L2HN001)
Licence *Sciences du langage*, mineure « Humanités numériques »
Paris, le 5 avril 2024, année 2023-2024

  </small-text>

<!--<smaller-text>*Diapositives adaptées de l'[IUT Lyon 1](https://perso.liris.cnrs.fr/pierre-antoine.champin/enseignement/intro-git/)* *et de [Thibault Clérice](https://github.com/PonteIneptique/cours-git)*</smaller-text>-->



<div style="position:relative; top:-160px; left:0px; margin-left:860px; margin-right:0px; font-size:14px;">
  Source :  <a href="https://kinsta.com/fr/blog/commandes-linux/">Diaz, 2023.</a>
</div>



---

# Bash

---

## [Terminal Tutor](https://www.terminaltutor.com/)

<p align="center">
  <img width="1000" height="500" style="margin-right:10px; vertical-align:bottom" src="img/terminal_tutor.png">
</p>

<p align="center">Aperçu de l'interface en ligne de commande sur le site Terminal Tutor.</p>

---

# Markdown

---

## [Tutoriel Markdown](https://www.arthurperret.fr/tutomd/) (Perret, 2020)

<p align="center">
  <img width="1000" height="500" style="margin-right:10px; vertical-align:bottom" src="img/markdown_accueil.png">
</p>

<p align="center">Page d'accueil du tutoriel Markdown.</p>

---

## [Tutoriel Markdown](https://www.arthurperret.fr/tutomd/tutorial/tutorial.html) (Perret, 2020)

<p align="center">
  <img width="1000" height="500" style="margin-right:10px; vertical-align:bottom" src="img/markdown_tuto.png">
</p>

<p align="center">Introduction au tutoriel Markdown.</p>

---

# Git

---

## [Tutoriel Git](https://www.w3schools.com/git/default.asp?remote=github) 

<p align="center">
  <img width="1000" height="450" style="margin-right:10px; vertical-align:bottom" src="img/git_tuto.png">
</p>

<p align="center">Page d'accueil du tutoriel Git.</p>

---

## [Exercices Git](https://www.w3schools.com/git/exercise.asp?filename=exercise_getstarted1) 

Exercices indispensables pour ce cours :

* *Git Get Started* : exercices 1-2
* *Git New Files* : exercice 1
* *Git Staging Environment* : exercice 1
* *Git Commit* : exercices 1, 4
* *Git Branch* : exercices 1-4
* *Git Remote Get Started* : exercice 1
* *Git Push to Remote* : exercice 1
* *Git Clone* : exercice 1-2
* *Git Reset* : exercice 1

---

## [Quiz sur Git](https://www.w3schools.com/quiztest/quiztest.asp?qtest=GIT)

* questions indispensables pour ce cours : 1-3, 7-13, 15-18, 22, 24
* questions avancées : 4-6, 14, 19-21, 23, 25

<p align="center">
  <img width="800" height="400" style="margin-right:10px; vertical-align:bottom" src="img/git_quiz.png">
</p>

<p align="center">Début du quiz sur Git.</p>

---

## [Récapitulatif des commandes utiles pour Bash et Git](https://christopheducamp.com/2013/12/09/anti-seche-ligne-de-commande/) (Ducamp, 2013)

<p align="center">
  <img width="400" height="400" style="margin-right:10px; vertical-align:bottom" src="img/antiseche.png">
</p>

<p align="center">Page d'accueil du récapitulatif des commandes utiles pour Bash et Git.</p>

---

## [Tutoriel Git pratique](https://www.hostinger.fr/tutoriels/tuto-git) (Anonyme, 2023)

Utiliser Git en ligne de commande.

<p align="center">
  <img width="800" height="400" style="margin-right:10px; vertical-align:bottom" src="img/git_pratique.png">
</p>

<p align="center">Page d'accueil du tutoriel pour la prise en main de Git.</p>

---

  ## Références

<ul style="font-size: 20px">
        <li><b>Anonyme.</b> Tuto GIT Guide Complet Pour une Prise en Main Rapide !. Hostinger tutoriels. <a href="https://www.hostinger.fr/tutoriels/tuto-git">https://www.hostinger.fr/tutoriels/tuto-git</a></li>
    <li><b>Ducamp, C.</b> (2013). Antisèche Ligne de commande pour Démarrer sur GitHub ! <a href="https://www.christopheducamp.com/2013/12/09/anti-seche-ligne-de-commande/">https://www.christopheducamp.com/2013/12/09/anti-seche-ligne-de-commande/</a></li>
    <li><b>Perret, A.</b> (2020). Tutoriel Markdown. <a href="https://www.arthurperret.fr/tutomd/">https://www.arthurperret.fr/tutomd/</a></li>
    <li><b>Terminal Tutor.</b> (<i>s. d.</i>). Terminal Tutor – learn the Command Line interactively. <a href="https://www.terminaltutor.com/">https://www.terminaltutor.com/</a></li>
    <li><b>W3Cschools.</b> (2023). Git Tutorial. <a href="https://www.w3schools.com/git/">https://www.w3schools.com/git/</a></li>



</ul>


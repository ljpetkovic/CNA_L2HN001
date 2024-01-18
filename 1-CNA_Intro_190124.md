---
marp: true
theme: default
markdown.marp.enableHtml: true
paginate: true
extra: true
footer: "Cultures numériques avancées, mineure HN (L2HN001), 19/01/2024, Ljudmila PETKOVIC"
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
    <img src="https://kinsta.com/wp-content/uploads/2021/08/old-date.png" alt="Bash" style="width:40%; float:right">
      </figure>
  </div>





  <!-- _class: lead -->

  ## Cultures numériques avancées

  ###### Ljudmila PETKOVIC

<small-text><a href="mailto:ljudmila.petkovic@sorbonne-nouvelle.fr">`ljudmila.petkovic@sorbonne-nouvelle.fr`</a></small-text>

  <br>

  


  <small-text>

  Cultures numériques avancées (L2HN001)
  Mineure « Humanités numériques », licence Lettres 
  Paris, le 19 janvier 2024, année 2023-2024

  </small-text>

<smaller-text>*Diapositives adaptées de [Simon Gabay](https://github.com/gabays/Fondamentaux/blob/main/Lignes_de_commandes/DistRead_1_2.pdf) et de [Simone Rebora](https://github.com/ABC-DH/EnExDi2022/tree/main/materials/1_KnowYourComputer/slides)*.</smaller-text>

<div style="position:relative; top:-80px; left:0px; margin-left:790px; margin-right:0px; font-size:14px;">
  Source :  <a href="https://kinsta.com/fr/blog/commandes-linux/">Diaz, 2023.</a>
</div>

---

# Questions administratives

---

## Informations pratiques

<table align="center" style="font-size: 27.5px;">
    <tr>
        <td align="left"><b>Formation</b></td>
        <td align="left">mineure Humanités numériques, licence Lettres (L1)</td>
    </tr>
    <tr style="background-color: white;">
        <td align="left"><b>Modalité</b></td>
        <td align="left">présentiel</td>
    </tr>
    <tr style="background-color: white;">
        <td align="left"><b>Enseignante</b></td>
        <td align="left">Ljudmila PETKOVIC</td>
    </tr>
    <tr style="background-color: white;">
        <td align="left"><b>Semestre</b></td>
        <td align="left">printemps (S2)</td>
    </tr>
    <tr>
        <td align="left"><b>Salle</b></td>
        <td align="left">B307, campus Nation</td>
    </tr>
    <tr style="background-color: white;">
        <td align="left"><b>Horaire</b></td>
        <td align="left">vendredi 08h-10h</td>
    </tr>
    <tr>
        <td align="left"><b>Langue</b></td>
        <td align="left">français</td>
     <tr style="background-color: white;">
        <td align="left"><b>ECTS</b></td>
        <td align="left">3</td>
    </tr>
    <tr>
        <td align="left"><b>Matériel</b></td>
        <td align="left"><a href="https://icampus.univ-paris3.fr/course/view.php?id=44401">iCampus</a></td>
    </tr>
    </tr>
</table>

---

## Emploi du temps · [calendrier](http://www.univ-paris3.fr/medias/fichier/calendrier-2023-2024-sorbonne-nouvelle-e-769-tudiant_1685096240005.pdf)

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:'Open Sans', sans-serif;font-size:26px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:'Open Sans', sans-serif;font-size:26px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-c4ww{background-color:#cbcefb;border-color:black;text-align:center;vertical-align:top}
.tg .tg-j4xs{background-color:#cbcefb;border-color:black;text-align:center;vertical-align:middle}
.tg .tg-3iz3{background-color:#ffffff;border-color:#000000;color:#fe0000;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-07kb{background-color:#fffc9e;border-color:#000000;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-mums{background-color:#ffffff;border-color:#000000;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-oorc{background-color:#cbcefb;border-color:#000000;text-align:center;vertical-align:middle}
.tg .tg-jbyd{background-color:#ffffff;border-color:#000000;text-align:center;vertical-align:top}
.tg .tg-7g6k{background-color:#ffffff;border-color:black;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-vhtn{background-color:#ffffff;border-color:#000000;text-align:center;vertical-align:middle}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-07kb" colspan="2">Séances 1-5</th>
    <th class="tg-07kb" colspan="2">Séances 6-11</th>
    <th class="tg-07kb" colspan="2">Séances 12-13</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-mums">1</td>
    <td class="tg-oorc">19 janvier</td>
    <td class="tg-mums">6</td>
    <td class="tg-oorc">1 mars</td>
    <td class="tg-mums">12</td>
    <td class="tg-c4ww">19 avril</td>
  </tr>
  <tr>
    <td class="tg-mums">2</td>
    <td class="tg-oorc">26 janvier</td>
    <td class="tg-mums">7</td>
    <td class="tg-oorc">8 mars</td>
    <td class="tg-mums">13</td>
    <td class="tg-c4ww">26 avril</td>
  </tr>
  <tr>
    <td class="tg-mums">3</td>
    <td class="tg-oorc">2 février</td>
    <td class="tg-mums">8</td>
    <td class="tg-oorc">15 mars</td>
    <td class="tg-jbyd" colspan="2" rowspan="5" style="border:none;"></td>
  </tr>
  <tr>
    <td class="tg-7g6k">4</td>
    <td class="tg-oorc">9 février</td>
    <td class="tg-7g6k">9</td>
    <td class="tg-j4xs">22 mars</td>
  </tr>
  <tr>
    <td class="tg-7g6k">5</td>
    <td class="tg-oorc">16 février</td>
    <td class="tg-7g6k">10</td>
    <td class="tg-j4xs">29 mars</td>
  </tr>
  <tr>
    <td class="tg-3iz3">congés</td>
    <td class="tg-oorc">23 février</td>
    <td class="tg-mums">11</td>
    <td class="tg-j4xs">5 avril</td>
  </tr>
  <tr>
    <td class="tg-vhtn" colspan="2" style="border:none;"></td>
    <td class="tg-3iz3">congés</td>
    <td class="tg-j4xs">12 avril</td>
  </tr>
</tbody>
</table>

---

## Évaluation

* <span style="color:darkblue"><b>Contrôle continu</b></span>

  <table align="left" style="font-size: 28px";>
      <tr>
          <td align="center"><b>Type d'évaluation</b></td>
          <td align="center"><b>Date</b></td>
          <td align="center"><b>Durée</b></td>
          <td align="center"><b>% de la note</b></td>
      </tr>
      <tr style="background-color: white;">
          <td align="center">évaluation de la pratique numérique</td>
          <td align="center">1 mars</td>
          <td align="center">1h</td>
          <td align="center">50%</td>
      </tr>
      <tr>
          <td align="center">évaluation de la pratique numérique</td>
          <td align="center">26 avril</td>
          <td align="center">1h</td>
          <td align="center">50%</td>
      </tr>
  </table><br><br><br><br>
  
  
  



* <span style="color:darkblue"><b>Contrôle terminal intégré (CTI)</b></span>

  <table align="left" style="font-size: 28px";>
      <tr>
          <td align="center">évaluation de la pratique numérique</td>
          <td align="center">26 avril</td>
          <td align="center">2h</td>
          <td align="center">100%</td>
      </tr>
  </table><br><br> 

* <span style="color:darkblue"><b>Rattrapage</b></span>

  <table align="left" style="font-size: 28px";>
      <tr>
          <td align="center">évaluation de la pratique numérique</td>
          <td align="center">18-29 juin</td>
          <td align="center">2h</td>
          <td align="center">100%</td>
      </tr>
  </table> 

---

## Absences

* L’**absence non justifiée** à un DST ou la non-participation à l’une des épreuves du contrôle continu (y compris la non-remise d’un travail à la date fixée par l’enseignant·e) entraîne la note de 0 sur 20 pour l’exercice concerné.
* En cas d’**absence justifiée**, deux aménagements sont possibles :
  * calcul de la moyenne uniquement à partir des autres épreuves auxquelles l’étudiant·e a participé ;
  * organisation d’une nouvelle épreuve pour les étudiant·e·s concerné·e·s.


---

## Réponses à toutes les questions administratives

<div style="padding: 15px; border: 1px solid transparent; border-color: transparent; margin-bottom: 20px; border-radius: 4px; color: #31708f; background-color: white; border-color: #bce8f1;">
Pour toutes les questions administratives, voir la <a href="http://www.univ-paris3.fr/medias/fichier/charte-de-l-evaluation-et-du-controle-des-connaissances-licence-et-master-2023-2024-cfvu-10-nov-2023_1700764504893.pdf">Charte de l'évaluation et du contrôle des connaissances</a>.
</div>


 ou contacter :

* le secrétariat : <a href="mailto:patricia.hernandez-munoz@sorbonne-nouvelle.fr">Mme Patricia HERNANDEZ-MUNOZ</a>
* le directeur du département : <a href="mailto:james.costa@sorbonne-nouvelle.fr">M. James COSTA</a>

---

  ## Plan du cours

 <ol style="font-size: 26px";>
  <li>Introduction au cours. Connaître son propre ordinateur.</li>
  <li>La ligne de commande comme alternative à l'interface graphique : langage de script Bash.</li>
  <li>Structure des répertoires. Variables.</li>
  <li>Exécution des scripts en ligne de commande.</li>
  <li>Examen blanc 1.</li>
  <li>Contrôle continu. Premier partiel.</li>
  <li>Langage de balisage Markdown : notions de base.</li>
  <li>Markdown : rédaction d’une documentation.</li>
  <li>Git : outil de versionnement du code. Notions de base.</li>
  <li>Git : commandes de base.</li>
  <li>Examen blanc 2.</li>
  <li>Contrôle continu. Deuxième partiel.</li>
  <li> ???? </li>
</ol> 

---

# Connaître son propre ordinateur


---

  ## Références

  * Diaz, D. (2023). « Les 40 commandes Linux les plus utilisées que vous devez connaître ». Kinsta. https://kinsta.com/fr/blog/commandes-linux/

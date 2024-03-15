---
marp: true
theme: default
markdown.marp.enableHtml: true
paginate: true
extra: true
footer: "Cultures numériques avancées, licence <i>Sciences du langage</i>, mineure HN (L2HN001), 15/03/2024, Ljudmila PETKOVIC"
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

  #### Markdown : rédaction d'une documentation

  ###### Ljudmila PETKOVIC

<small-text><a href="mailto:ljudmila.petkovic@sorbonne-nouvelle.fr">`ljudmila.petkovic@sorbonne-nouvelle.fr`</a></small-text>

  <br>

  

  <small-text> 

Cultures numériques avancées (L2HN001)
Licence *Sciences du langage*, mineure « Humanités numériques »
Paris, le 15 mars 2024, année 2023-2024

  </small-text>

<smaller-text>_Diapositives adaptées de la [documentation Typora](https://support.typora.io/media/export/Markdown-Reference.pdf)_.</smaller-text>

<!--<smaller-text>*Diapositives adaptées de [Simon Gabay](https://github.com/gabays/Fondamentaux/blob/main/Lignes_de_commandes/DistRead_1_2.pdf) et de [Simone Rebora](https://github.com/ABC-DH/EnExDi2022/tree/main/materials/1_KnowYourComputer/slides)*.</smaller-text>-->

<div style="position:relative; top:-220px; left:0px; margin-left:860px; margin-right:0px; font-size:14px;">
  Source :  <a href="https://kinsta.com/fr/blog/commandes-linux/">Diaz, 2023.</a>
</div>


---

## Typora

* éditeur du texte écrit en langage Markdown
* interface graphique de l'utilisateur (angl. *GUI*) minimaliste
* l'écriture inclut les balises utilisées : visualisation des modifications en temps réel
* plus de fonctionnalités en comparaison avec les éditeurs Markdown en ligne 
  * p. ex. StackEdit ne supporte pas de cases à cocher, de surlignage etc. 
* permet d'exporter les résultats en différents formats (HTML, PDF...) 

---

## Télécharger Typora

* ouvrir le lien https://typora.io/ > se diriger en bas de la page > télécharger Typora pour votre système d'exploitation (macOS, Windows ou Linux)

<p align="center" alt="drawing"> 
    <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_08_Markdown_doc_150324/img/typora.png" width="500" height="450"><br>
</p>

---

## Interface Typora

<p align="center" alt="drawing"> 
    <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_08_Markdown_doc_150324/img/gui_typora.png" width="600" height="550"><br>
</p>


---

## Fonctionnalités

Vous pouvez explorer les fonctionnalités de Typora dans la barre d'outils en haut.

<p align="center" alt="drawing"> 
    <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_08_Markdown_doc_150324/img/fonctionnalites.png" width="900" height="80"><br>
</p>

* `Fichier` : nouveau, ouvrir, exporter...
* `Éditer` : annuler, copier / coller, trouver et remplacer...

* `Paragraphe` : en-têtes, citations, listes...
* `Format` : gras, italique, souligné...
* `Présentation` : plan, arborescence, rechercher...
* `Thèmes` : Github, Newsprint, Night...

---

## Liste des tâches

Syntaxe : 

* `- [ ]` 
* `- [x]` 
  * ou cocher manuellement la case dans le fichier Markdown

```markdown
- [ ] cette tâche n'est pas complète
- [x] cette tâche est complète 
```

➡️

☐ cette tâche n'est pas complète

☑ cette tâche est complète

---

## Tableaux

Syntaxe :

```
| Colonne 1 | Colonne 2 |
| --------- | --------- |
|  Ligne 1  |  Ligne 1  |
|  Ligne 2  |  Ligne 2  |
```

➡️

| Colonne 1 | Colonne 2 |
| --------- | --------- |
| Ligne 1   | Ligne 1   |
| Ligne 2   | Ligne 2   |

---

## Commentaire

Syntaxe : `<!-- mon commentaire -->`

* les commentaires sont visibles dans le fichier Markdown, mais pas dans le rendu

  ```
  <!-- mon commentaire qui sert comme une note pour moi-même mais qui 
  ne sera pas visible dans le rendu final -->
  
  Mon texte.
  ```

  ➡️ <!-- mon commentaire -->

  Mon texte.

---

## Notes de bas de page

Syntaxe : 

* indiquer la note de bas de page après un mot : `[^fn1]` + `Entrée`
* écrire `[^fn1]:` suivi du texte de la note de bas de page

```
On peut créer des notes de bas de page[^fn1].

[^fn1] : Voici le texte de notre note de bas de page.
```

➡️

<p align="center" alt="drawing"> 
    <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_08_Markdown_doc_150324/img/footnote.png" width="1700" height="200"><br>
</p>

---

## Emojis :smiley_cat:

Syntaxe `:emoji:`

<div style="padding: 15px; border: 1px solid transparent; border-color: transparent; margin-bottom: 20px; border-radius: 4px; color: #31708f; background-color: #d9edf7; border-color: #bce8f1;">
Une aide à la saisie semi-automatique apparaîtra après avoir tapé <tt>:</tt> et le début d'un nom emoji.
</div>

`:white_check_mark:`

➡️

:white_check_mark:

---

## Fonctionnalités supplémentaires

<div style="padding: 15px; border: 1px solid transparent; border-color: transparent; margin-bottom: 20px; border-radius: 4px; color: #8a6d3b;; background-color: #fcf8e3; border-color: #faebcc;">
Pour utiliser les fonctionnalités supplémentaires, il faut les activer dans l'onglet <tt>Fichier > Préférences > Markdown</tt>.
</div>

<p align="center" alt="drawing"> 
    <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_08_Markdown_doc_150324/img/indices_exposants.png" width="400" height="400"><br>
</p>

---

## Indice

Syntaxe : `texte~indice`

* `H~2~O`

  ➡️

  H~2~O

## Exposant

Syntaxe : `texte^exposant` 

* `X^2` 

  ➡️

  X<sup>2</sup>

---

## Surlignage

Syntaxe : `==texte à surligner==`

* `Voici comment on peut ==surligner== le texte.`  

  ➡️ Voici comment on peut <span style="background-color: #FFFF00">surligner</span> le texte.

---

## Table des matières

Syntaxe : `[toc]`

➡️

<p align="center" alt="drawing"> 
    <img src="/home/ljudmila/Dropbox/SN/CNA_L2HN001/cours_08_Markdown_doc_150324/img/toc.png" width="250" height="450"><br>
</p>

---

# Exercice

Création d'une documentation en Markdown et export sous format HTML et PDF.

☐ Reproduire la documentation à partir du document `doc.pdf` en utilisant le langage Markdown.

---

  ## Références

<ul style="font-size: 20px">
    <li><b>Documentation Typora</b> (<i>s. d.</i>). <a href="https://support.typora.io/media/export/Markdown-Reference.pdf">https://support.typora.io/media/export/Markdown-Reference.pdf</a></li>
</ul>

---
marp: true
theme: default
markdown.marp.enableHtml: true
paginate: true
extra: true
footer: "Cultures numériques avancées, licence <i>Sciences du langage</i>, mineure HN (L2HN001), 07/03/2024, Ljudmila PETKOVIC"
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

  #### Langage de balisage Markdown : notions de base

  ###### Ljudmila PETKOVIC

<small-text><a href="mailto:ljudmila.petkovic@sorbonne-nouvelle.fr">`ljudmila.petkovic@sorbonne-nouvelle.fr`</a></small-text>

  <br>

  

  <small-text> 

Cultures numériques avancées (L2HN001)
Licence *Sciences du langage*, mineure « Humanités numériques »
Paris, le 08 mars 2024, année 2023-2024

  </small-text>

<smaller-text>_Diapositives adaptées de [Torikian,](https://www.markdowntutorial.com/fr/)_</smaller-text>

<!--<smaller-text>*Diapositives adaptées de [Simon Gabay](https://github.com/gabays/Fondamentaux/blob/main/Lignes_de_commandes/DistRead_1_2.pdf) et de [Simone Rebora](https://github.com/ABC-DH/EnExDi2022/tree/main/materials/1_KnowYourComputer/slides)*.</smaller-text>-->

<div style="position:relative; top:-220px; left:0px; margin-left:860px; margin-right:0px; font-size:14px;">
  Source :  <a href="https://kinsta.com/fr/blog/commandes-linux/">Diaz, 2023.</a>
</div>


---

## Markdown

* langage de balisage (angl. _mark-up language_) et moyen d'écrire du contenu web 
  * d'autres langages de balisage : HTML, XML, LaTeX

* écrit en <span style="color:darkblue">**texte brut**</span> (angl. _plain text_)
  * contenu basique, échangeable et inter-opérable du texte
  * représente seulement les caractères contenus, sans leur apparence
  * seule une numérotation des caractères est utilisée, la police de caractères étant fournie par un mécanisme indépendant 

* Markdown utilise un alphabet normal, avec quelques symboles familiers, comme l'astérisques ( `*` ) et accents graves (<tt>`</tt> )


---

## Avantages de l'utilisation de Markdown

* Le texte écrit dans Markdown peut être facilement partagé entre les ordinateurs, les téléphones mobiles et les personnes. → intéropérabilité (≠ applications de traitement de texte encombrantes, p. ex. Word)
* Il devient rapidement la norme d'écriture pour les universitaires, les scientifiques, les écrivains et bien d'autres.
  * des sites Web comme [GitHub](https://github.com/ljpetkovic/IHN_L1HN001), [Stack Overflow](https://stackoverflow.com/), [Reddit](https://www.reddit.com/) etc. utilisent Markdown pour styliser leurs commentaires
* Le formatage de texte dans Markdown est facilement manipulable : 
  * son rôle n'est pas de changer la taille, la couleur ou le type de police du texte (≠ CSS : langage descriptif de la mise en forme du document HTML ou XML) 
  * tout ce que vous contrôlez est l'affichage du texte, comme la mise en gras, la création d'en-têtes et l'organisation de listes.
  

---

## Plateformes d'utilisation de Markdown

Pour écrire un document en utilisant le langage Markdown, vous pouvez soit :

* télécharger un logiciel sur votre ordinateur, en fonction de votre système d'exploitation (p. ex. [Typora](https://typora.io/), [MacDown](https://macdown.uranusjr.com/) etc.)
* utiliser un logiciel en ligne (p. ex. [StackEdit](https://stackedit.io/app#))

---

# Notions de base

* italique / gras
* en-têtes
* liens
* images
* citations bloc
* listes
* paragraphes
* autres

---

## Italique

Pour mettre un élément (mot, symbole...) en italique dans Markdown, il faut l'entourer d'un trait de soulignement (`_`) ou d'un asterisque (`*`). 

Par exemple, le mot `_italique_`  ou `*italique*` devient _italique_. 

```markdown
Voici comment écrire en _italique_. Ceci est également écrit en *italique*.
```

Résultat :

➡️ Voici comment écrire en _italique_. Ceci est également écrit en *italique*. 

---

## Gras

Entourer un élément de deux traits de soulignement ou de deux astérisques :

```markdown
Voici comment écrire en **gras**. Et voici encore un mot en __gras__.
```

➡️ Voici comment écrire en **gras**. Et voici encore un mot en __gras__.

---

## Italique ET gras

Placer les astérisques à l'extérieur et le trait de soulignement à l'intérieur, pour raison de lisibilité :

```markdown
Voici comment écrire en **_italique et gras_**.
```

➡️ Voici comment écrire à la fois en **_italique et gras_**.

---

## En-têtes

* fréquemment utilisés sur les sites Web, les articles de magazines et les bulletins, pour attirer l'attention sur une section 
* agissent comme des titres ou des sous-titres au-dessus des sections

---

## Types d'en-têtes

6 types d'en-têtes, par tailles décroissantes :

* # En-tête 1

* ## En-tête 2

* ### En-tête 3

* #### En-tête 4

* ##### En-tête 5

* ###### En-tête 6 

---

## En-têtes

* faire précéder un élément d'un signe dièse (`#`)

* placer le même nombre de dièses que la taille de l'en-tête souhaitée
  * par exemple, pour un en-tête 1, vous utiliserez un signe dièse : `# En-tête 1`
    # ➡️ En-tête 1
    
  * pour un en-tête 2, vous en utiliserez deux : `## En-tête 2`
    ## ➡️ En-tête 2
    
  * et ainsi de suite.

---

## En-têtes

C'est à vous de décider quand il convient d'utiliser quel en-tête. 

En général, les en-têtes un et six doivent être utilisés avec parcimonie. 

Vous ne pouvez pas vraiment mettre un en-tête en gras, mais vous pouvez mettre certains mots en italique. 

```markdown
### Mon en-tête 3 _italicisé_
```

### ➡️ Mon en-tête 3 _italicisé_

---

## Liens

* créer des hyperliens vers d'autres sites Web dans Markdown

* deux types de liens différents qui s'affichent exactement de la même manière :
  1. lien *in line* ou lien « dans la ligne » (angl. *inline link*)
  1. lien « référence » (angl. *reference link*)


---

### *Inline link*

* placer le <u>texte du lien</u> entre crochets (`[ ]`), puis le <u>lien</u> entre parenthèses (`( )`) 

Par exemple, pour créer un lien hypertexte vers https://github.com/ avec un texte de lien qui dit, « Cliquer ici », écrire : `[Cliquer ici](https://github.com/)`.

➡️ [Cliquer ici](https://github.com/)

---

### Formatage des liens

* Lien en gras :

  ```markdown
  Vous devez **[vraiment](https://github.com/)** cliquer ici
  ```

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;➡️ Vous devez **[vraiment](https://github.com/)** cliquer ici

* Lien en italique

  ```markdown
  Vous devez _[vraiment](https://github.com/)_ cliquer ici
  ```

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;➡️ Vous devez _[vraiment](https://github.com/)_ cliquer ici

* Lien dans le titre

  #### ➡️ Mon [titre](https://github.com/)

---

### *Reference link*

Le lien est en fait une référence à un autre endroit du document.

* syntaxe : `[texte du lien web]` + `[lien web effectif]`

```markdown
     Ceci est [un lien web][premier site web].
     Ceci est [un autre lien web][deuxième site web].
     Et maintenant nous revenons au [premier lien web][premier site web].

     [premier site web]: www.github.com
     [deuxième site web]: www.google.com
```

➡️ Ceci est [un lien web][premier site web].

➡️ Ceci est [un autre lien web][deuxième site web].

➡️ Et maintenant nous revenons au [premier lien web][premier site web].

[premier site web]: https://github.com/
[deuxième site web]: https://github.com/ljpetkovic/L2HN001

---

### *Reference link*

* les « références » sont indiquées dans le 2<sup>e</sup> ensemble de crochets : `[texte du lien web]` et <span style="color:darkblue"><b>`[lien web effectif]`</b></span>

* au bas d'un document Markdown, ces crochets sont définis comme des liens appropriés vers des sites web externes

  <div style="padding: 15px; border: 1px solid transparent; border-color: transparent; margin-bottom: 20px; border-radius: 4px; color: #3c763d; background-color: #dff0d8; border-color: #d6e9c6;">
      Plusieurs liens vers le même site web ne doivent être mis à jour qu'une seule fois. Par exemple, si nous décidons de rediriger tous les liens du <tt>[premier site web]</tt> vers un autre site web, nous n'avons qu'à changer le lien de <span style="color:red"><b>référence unique</b></span>.
  </div> 

  <div style="padding: 15px; border: 1px solid transparent; border-color: transparent; margin-bottom: 20px; border-radius: 4px; color: #8a6d3b;; background-color: #fcf8e3; border-color: #faebcc;">
      Les liens de référence n'apparaissent pas dans le Markdown <span style="color:darkblue"><b>rendu</b></span>. Vous les définissez en fournissant le même nom de balise entouré de crochets, suivi de deux-points, suivi du lien. <tt>[premier site web]: https://github.com/</tt>
  </div>

---

## Images

Les images ont également deux styles, tout comme les liens, et les deux s'affichent exactement de la même manière. 

1. « image dans la ligne » (angl. *inline image link*)
2. « image de référence » (angl. *reference image link*)

<div style="padding: 15px; border: 1px solid transparent; border-color: transparent; margin-bottom: 20px; border-radius: 4px; color: #8a6d3b;; background-color: #fcf8e3; border-color: #faebcc;">
La différence entre les liens et les images est que les images sont précédées d'un point d'exclamation (<tt>!</tt>). 
</div>

Pour créer un *inline image link*, tapez un point d'exclamation (`!`), placez le « texte alternatif » entre crochets (`[ ]`), puis placez le lien entre parenthèses (`( )`). 

<small-text>*NB* : Le « texte alternatif » est une expression ou une phrase qui décrit l'image pour les personnes malvoyantes, utilisant des lecteurs d'écran ou ne disposant pas de connexions Internet haut débit.</small-text>

---

### *Inline image link*

Par exemple, pour créer un *inline image link* vers https://www.digitalocean.com/_next/static/media/intro-to-cloud.d49bc5f7.jpeg, avec un texte alternatif indiquant « Shell », écrire :

```markdown
![Shell](https://www.digitalocean.com/_next/static/media/intro-to-cloud.d49bc5f7.jpeg)
```

 ![Benjamin Bannekat](https://www.digitalocean.com/_next/static/media/intro-to-cloud.d49bc5f7.jpeg)

---

### *Reference image link*

Faire précéder le Markdown d'un point d'exclamation, puis fournir deux crochets pour le texte alternatif, puis deux autres pour la balise d'image, comme ceci : 

```markdown
![En-tête][markdown]
```

Au bas de la page Markdown, définir une image pour le tag : 

`[markdown]: https://raw.githubusercontent.com/sanity-io/sanity-plugin-markdown/HEAD/assets/example.png`

---

### *Reference image link*

```markdown
![En-tête][markdown]
```

`[markdown]: https://raw.githubusercontent.com/sanity-io/sanity-plugin-markdown/HEAD/assets/example.png`

![Prise de notes avec markdown][markdown] 

[markdown]: https://raw.githubusercontent.com/sanity-io/sanity-plugin-markdown/HEAD/assets/example.png

---

nouvelle page

---

## Citations bloc

* une citation bloc est une phrase ou un paragraphe qui a été spécialement formaté pour attirer l'attention du lecteur

* pour attirer une attention particulière sur une citation d'une autre source ou pour concevoir une citation tirée d'un article de magazine, faites précéder la ligne du signe « supérieur à » (`>`), par exemple :

  ```markdown
  > « Je pense, donc je suis ».
  ```

  [➡️](https://emojiterra.com/fr/fleche-droite/)

  > « Je pense, donc je suis ».
  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(René Descartes)

---

### Formatage des citations bloc

* italique, gras et hyperlien

  ```markdown
  > « Etre libre, ce n'est pas pouvoir faire ce que l'on _veut_, 
  > mais c'est vouloir ce que l'on **peut**. » 
  ([source](https://citations.ouest-france.fr/citation-jean-paul-sartre/etre-libre-pouvoir-faire-veut-19476.html))
  ```
  
  [➡️](https://emojiterra.com/fr/fleche-droite/)
  
  > « Etre libre, ce n'est pas pouvoir faire ce que l'on _veut_, 
  > mais c'est vouloir ce que l'on **peut**. » ([source](https://citations.ouest-france.fr/citation-jean-paul-sartre/etre-libre-pouvoir-faire-veut-19476.html))

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(Jean-Paul Sartre)

---

## Listes

Deux types de listes : 

1. non ordonnée (avec des puces)
2. ordonnée (avec des chiffres)

---

### Liste non ordonnée

* faire précéder chaque élément de la liste d'un astérisque (`*`)

* chaque élément de la liste obtient également sa propre ligne
  * p. ex., une liste de courses dans Markdown pourrait ressembler à ceci :

```markdown
* Asperges
* Roquefort
* Gruyère
```

[➡️](https://emojiterra.com/fr/fleche-droite/)

* Asperges
* Roquefort
* Gruyère

---

### Liste ordonnée

* une liste ordonnée est précédée de chiffres au lieu d'astérisques. 
  * p. ex. : recette

```markdown
1. Bien égoutter les asperges et les disposer dans un petit plat à gratin.
2. Emietter le roquefort et le mélanger à la crème fraîche. Poivrer et saler.
3. Verser le mélange sur les asperges et répartir du gruyère pour faire gratiner.
4. Mettre l'ensemble au four à 180°C (thermostat 6) pendant 15 min environ.
```

[➡️](https://emojiterra.com/fr/fleche-droite/)

1. Bien égoutter les asperges et les disposer dans un petit plat à gratin.
2. Emietter le roquefort et le mélanger à la crème fraîche. Poivrer et saler.
3. Verser le mélange sur les asperges et répartir du gruyère pour faire gratiner.
4. Mettre l'ensemble au four à 180°C (thermostat 6) pendant 15 min environ.

---

### Formatage des listes

Vous pouvez choisir d'ajouter des italiques, du gras ou des liens dans les listes.

Par exemple, mettons les noms latins des plantes en italique.

```markdown
* Azalea (_Ericaceae Rhododendron_)
* Chrysanthemum (_Anthemideae Chrysanthemum_)
* Dahlia (_Coreopsideae Dahlia_)
```

[➡️](https://emojiterra.com/fr/fleche-droite/)

* Azalea (_Ericaceae Rhododendron_)
* Chrysanthemum (_Anthemideae Chrysanthemum_)
* Dahlia (_Coreopsideae Dahlia_)

---

### Listes imbriquées

Pour créer une liste plus approfondie, nous pouvons imbriquer une liste dans une autre. 

Indenter<sup>1</sup> chaque astérisque d'un espace de plus que l'élément précédent (certains éditeurs, comme Typora, permettent de faire une tabulation). 

<small-text><sup>1</sup> insérer une tabulations ou plusieurs espaces au début d'une ligne de texte</small-text>

---

### Exemple des listes imbriquées

Dans la liste suivante, nous ajoutons une sous-liste au 1<sup>e</sup> et au 2<sup>e</sup> élément de la liste, ainsi qu'un autre élément imbriqué dans le 2<sup>e</sup> élément imbriqué :

```markdown
* Mon premier élément de la liste
  * Un élément imbriqué dans le premier élément
* Mon deuxième élément de ma liste
  * Un élément imbriqué dans le deuxième élément
    * Un autre élément imbriqué dans le deuxième élément imbriqué
```

[➡️](https://emojiterra.com/fr/fleche-droite/)

* Mon premier élément de la liste
  * Un élément imbriqué dans le premier élément
* Mon deuxième élément de ma liste
  * Un élément imbriqué dans le deuxième élément
    * Un autre élément imbriqué dans le deuxième élément imbriqué

---

### Listes avec des paragraphes

On n'ajoute pas de sous-listes après trois niveaux pour raison de lisibilité.

Pour créer une liste nécessitant un contexte supplémentaire (mais pas une autre liste), le paragraphe doit commencer sur une ligne toute seuls sous la puce ou le chiffre, et il doit être indenté d'au moins un espace (ou alors, il faut faire un retour à la ligne et supprimer la nouvelle puce ou le nouveau chiffre) :

```markdown
1. Cassez trois œufs au-dessus d'un bol.   

 Maintenant, vous allez vouloir casser les œufs de manière à ne pas faire de dégâts. 
```

[➡️](https://emojiterra.com/fr/fleche-droite/)

1. Cassez trois œufs au-dessus d'un bol.   

   Maintenant, vous allez vouloir casser les œufs de manière à ne pas faire de dégâts.  

---

### Convertir les puces en leurs propres paragraphes

```markdown
1. Couper le fromage   
   * Assurez-vous que le fromage est coupé en petits triangles.
2.  Trancher les tomates
   * Soyez prudent lorsque vous tenez le couteau.
```

[➡️](https://emojiterra.com/fr/fleche-droite/)

1. Couper le fromage   
   * Assurez-vous que le fromage est coupé en petits triangles.
2. Trancher les tomates
   * Soyez prudent lorsque vous tenez le couteau.

---

## Paragraphes

* pour créer une nouvelle ligne sans créer un nouveau paragraphe ou casser la liste qui le précède, utiliser les « pauses douces » (angl. *soft breaks*, `Shift + Entrée`) ou en insérant deux espaces après chaque nouvelle ligne, selon l'éditeur).

  > Ceci est mon`..`
  > joli poème 
  
* ≠ « grosses coupures » (angl. _hard breaks_, `Entrée/Retour`)

  > Ceci est mon
  >
  > Joli poème

---

### Plusieurs paragraphes dans une liste

Rappelez-vous que nous avons inséré une nouvelle ligne (`Entrée`) pour plusieurs paragraphes dans une liste.

Au lieu d'utiliser des *hard breaks*, nous pouvons resserrer les sous-paragraphes avec des *soft breaks* :

```markdown
1. Cassez trois œufs au-dessus d'un bol.
 Maintenant, vous allez vouloir casser les œufs de manière à ne pas faire de dégâts. 
```

➡️

1. Cassez trois œufs au-dessus d'un bol.
   Maintenant, vous allez vouloir casser les œufs de manière à ne pas faire de dégâts.  

---

## D'autres types de formatage du texte

* insérer trois tirets `---` pour séparer les diapositives ou les sections du texte

* texte barré : `~~barré~~` : Ceci est mon texte ~~barré~~

* texte souligné : `<ins>souligné</ins>` : Ceci est mon texte <ins>souligné</ins>

* texte à l'intérieur de deux accents graves : `git add` (idéal pour des commandes simples) 

* texte à l'intérieur de trois accents graves, suivi par un retour à la ligne (idéal pour les bouts de code)

  ```
  git add README.md
  git commit -m "Mon README"
  git push
  ```

---

# Exercices

[Tutoriel Markdown](https://www.markdowntutorial.com)

---

  ## Références

<ul style="font-size: 20px">
    <li><b>Torikian, G.</b> (<i>s. d.</i>). « Markdown Tutorial ». [<i>tutoriel</i>]. <a href="https://www.markdowntutorial.com/fr/">https://www.markdowntutorial.com/fr/</a> (consulté le 7 mars 2024).</li>
</ul>

# Développement web

**Instructions**
Vous allez créer un CV interactif. Celui-ci devra contenir vos informations et changer de format lorsqu'on cliquera sur un bouton.

**Objectifs**
1. Apprendre les bases du HTML, structure et balises courantes
2. Découvrir le CSS
3. Introduire un peu de javascript pour intéragir avec les éléments de la page

![image](https://github.maif.io/guilde-dev/numerique-pour-toutes-2025/blob/feature/numerique-pour-toutes-2026-front/assets/exercice-html-css.png)

<h2>
    <a href="https://codepen.io/Marion-Pougnard/pen/KwMMBwv" target="_blank" rel="noopener noreferrer">
        Accès à l'exercice sur CodePen
    </a>    
</h2>
---

### **Étapes à suivre**

#### **Étape 1 : Comprendre la structure HTML**
> ##### **C'est quoi le HTML ?**
> C'est le langage de balisage qui permet de structurer le contenu d'une page web.  
> C'est le principe d'une armoire à tiroirs :
> on a des éléments qui contiennent d'autres éléments, et ainsi de suite.  
> On peut également mettre des étiquettes sur ces tiroirs pour identifier leur contenu.
>
> ![structure-html.jpg](assets/structure-html.jpg)
>
> Lien vers la documentation HTML : <a href="https://developer.mozilla.org/fr/docs/Web/HTML" target="_blank" rel="noopener noreferrer">MDN HTML</a>


1. Commencez avec le squelette fourni ci-dessus.
2. Remplacez le texte par vos propres informations :
    - Dans `<h1>` (balise de titre), ajoutez vos prénom et nom.
    - Dans `<p>` (balise paragraphe), écrivez une phrase qui vous décrit.
3. Ajoutez des sections pour décrire vos compétences :
    - Créez une balise `<section>` avec un attribut "class" :
      <a href="https://developer.mozilla.org/fr/docs/Web/HTML/Element/section" target="_blank" rel="noopener noreferrer">
      documentation de la balise section
      </a>
    - Ajoutez un titre à la section `<h2>` : "Compétences techniques".
    - Ajoutez une liste de compétences avec les balises `<ul>` et `<li>` :
      <a href="https://developer.mozilla.org/fr/docs/Web/HTML/Element/li" target="_blank" rel="noopener noreferrer">
      documentation des balises de liste
      </a>.  
      Exemple de compétences découvertes dans cet atelier : CSS, HTML, JavaScript
    - Dupliquez cette section deux fois pour : "Compétences humaines" et "hobbies"


<details>
  <summary>Proposition de correction</summary>

```html
<section class="competences">
    <h2>Compétences techniques</h2>
    <ul id="techniques">
        <li>CSS</li>
        <li>HTML</li>
        <li>JavaScript</li>
    </ul>
</section>
<section class="competences">
    <h2>Compétences humaines</h2>
    <ul id="humaines">
        <li>Curiosité</li>
        <li>Adaptabilité</li>
        <li>Esprit d'équipe</li>
    </ul>
</section>
<section class="competences">
    <h2>Hobbies</h2>
    <ul id="hobbies">
        <li>patisserie</li>
        <li>jeux de société</li>
    </ul>
</section>
```
</details>


---

#### **Étape 2 : Ajouter du style avec CSS**

> ##### **C'est quoi le CSS ?**
> C'est le langage qui permet de styliser les pages web.
> c'est comme la décoration d'une maison :
> on peut changer les couleurs, les tailles, les polices, etc.
>
> Lien vers la documentation CSS :
<a href="https://developer.mozilla.org/fr/docs/Web/CSS" target="_blank" rel="noopener noreferrer">
Documentation CSS
</a>


Nous allons maintenant travailler dans la partie CSS de codepen.

1. **Commençons par ajouter une touche de couleur et le choix d'une police de caractères**
    - Pour ajouter du contenu sur notre CV, il faut d'abord cibler les éléments HTML avec des sélecteurs CSS.
    - Nous allons donc écrire dans la partie CSS `.cv {}`
    - À l'intérieur des accolades, nous allons ajouter :
        - les propriétés `border`, `background-color` et `font-family` pour ajouter une bordure, changer la couleur de fond et changer la police de caractères
        - les valeurs associées que vous pouvez rechercher dans la documentation (<a href="https://developer.mozilla.org/fr/docs/Web/CSS/Reference/Properties/border" target="_blank" rel="noopener noreferrer">
          border
          </a>, <a href="https://developer.mozilla.org/fr/docs/Web/CSS/Reference/Properties/background-color" target="_blank" rel="noopener noreferrer">
          background-color
          </a>, <a href="https://developer.mozilla.org/fr/docs/Web/CSS/Reference/Properties/font-family" target="_blank" rel="noopener noreferrer">
          font-family
          </a>)
2. **Maintenant, nous allons faire un peu de mise en forme**
    - Ajoutez un peu d'espace au sein du CV avec la propriété `padding` (<a href="https://developer.mozilla.org/fr/docs/Web/CSS/Reference/Properties/padding" target="_blank" rel="noopener noreferrer">
      padding
      </a>).
    - Centrez le texte avec `text-align` (<a href="https://developer.mozilla.org/fr/docs/Web/CSS/Reference/Properties/text-align" target="_blank" rel="noopener noreferrer">
      text-align
      </a>).
    - Arrondissez les coins du CV avec `border-radius` (<a href="https://developer.mozilla.org/fr/docs/Web/CSS/Reference/Properties/border-radius" target="_blank" rel="noopener noreferrer">
      border-radius
      </a>).
    - Ajustez la taille de la CV avec `width` (<a href="https://developer.mozilla.org/fr/docs/Web/CSS/Reference/Properties/width" target="_blank" rel="noopener noreferrer">
      width
      </a>).

<details>
<summary>Proposition de correction</summary>

```css
.cv {
  background-color: gold;
  font-family: Arial, sans-serif;
  padding: 20px;
  text-align: center;
  border-radius: 8px;
  width: 400px;
}
```
</details>

3. **Approfondir la mise en forme :**
    - Ajouter une ombre au CV avec la propriété `box-shadow` (<a href="https://developer.mozilla.org/fr/docs/Web/CSS/Reference/Properties/box-shadow)" target="_blank" rel="noopener noreferrer">
      box-shadow
      </a>).
    - Ajoutez un sélecteur CSS sur les sections de votre CV avec `.competences {}`.
        - Ajoutez-y la propriété `border-top` en y précisant le style, l'épaisseur et la couleur pour séparer chaque section (<a href="https://developer.mozilla.org/fr/docs/Web/CSS/Reference/Properties/border-top" target="_blank" rel="noopener noreferrer">
          border-top
          </a>).
    - Ajoutez un sélecteur CSS sur les listes de votre CV avec `ul {}`.
        - Cachez les puces des listes en utilisant la bonne valeur de la propriété `list-style` (<a href="https://developer.mozilla.org/fr/docs/Web/CSS/Reference/Properties/list-style" target="_blank" rel="noopener noreferrer">
          list-style
          </a>).
        - Corrigez l'alignement des listes en y précisant un `padding` de 0px.


4. **Pour aller plus loin avec le CSS, découvrons les `flexbox` (<a href="https://css-tricks.com/snippets/css/a-guide-to-flexbox/" target="_blank" rel="noopener noreferrer">
   flexbox
   </a>).**
    - Pour que l'utilisation des flexbox soit plus parlante, copiez votre code HTML et collez-le une ou plusieurs fois en dessous. Vous aurez ainsi plusieurs CV.
    - Ajoutez un sélecteur CSS sur le corps de la page avec `body {}`.
    - Ajoutez la propriété `display : flex;`.
    - Que remarquez-vous ? Les CV sont-elles alignées horizontalement ou verticalement ? Savez-vous pourquoi ?
    - Ajoutez les propriétés `justify-content` et `gap` et leurs valeurs (<a href="https://developer.mozilla.org/fr/docs/Web/CSS/Reference/Properties/justify-content" target="_blank" rel="noopener noreferrer">
      justify-content
      </a>, <a href="https://developer.mozilla.org/fr/docs/Web/CSS/Reference/Properties/gap" target="_blank" rel="noopener noreferrer">
      gap
      </a>).


<details>
  <summary>Proposition de correction</summary>

```css
.cv {
  background-color: gold;
  font-family: Arial, sans-serif;
  padding: 20px;
  text-align: center;
  border-radius: 8px;
  width: 400px;
  box-shadow: 5px 5px 20px -5px rgba(0, 0, 0, 0.70);
}

.competences {
  border-top: solid 1px orange;
}

ul {
  list-style: none;
  padding: 0px;
}

body {
  display: flex;
  justify-content: center;
  gap: 10px;
}
```
</details>

---
####  Étape 3 : Ajouter un peu d’interactivité avec JavaScript
> ##### **C'est quoi le Javascript ?**
> C'est le langage de programmation qui permet d'ajouter de l'interactivité aux pages web.
> Plus précisément, il pourrait permettre, dans notre cas, d'ajouter de l'interactivité pour modifier notre CV en écoutant un évènement utilisateur "click"
>
> Lien vers la <a href="https://developer.mozilla.org/fr/docs/Web/JavaScript" target="_blank" rel="noopener noreferrer">documentation JavaScript</a>

Pour tester l'interactivité nous allons ajouter un "toggle" bouton pour changer la couleur du titre :
1. **Tout d'abord en HTML nous allons ajouter une balise `button` avec un id="ToggleBtn"**

Documentation sur les <a href="https://developer.mozilla.org/fr/docs/Web/HTML/Reference/Elements/button" target="_blank" rel="noopener noreferrer">
boutons
</a>
<details>
  <summary>Proposition de correction</summary>

```html
<div style="display: flex; height: 30px;">
    <span style="align-self: center;">Changez la couleur du titre</span>
    <button id="toggleBtn" class="switch">
        <span class="slider"></span>
    </button>
</div>
```
</details>

2. **Dans la partie javascript nous allons définir des sélecteurs qui agiront sur le bouton, par son id, et sur la titre du CV**
   Utilisez `document.getElementById` sur l'ID du bouton et du titre afin de récupérer leurs emplacements et la stocker dans une `const` : documentation <a href="https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById" target="_blank" rel="noopener noreferrer">getElementById()</a> et <a href="https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Statements/const" target="_blank" rel="noopener noreferrer">const</a>
<details>
  <summary>Proposition de correction</summary>

```javascript
const button = document.getElementById('toggleBtn')
const titre = document.getElementById('name')
```
</details>

3. **Puis nous allons écrire une méthode qui ajoutera un attribut `active` class aux deux balises sélectionnées afin d'en modifier la mise en forme**

<details>
    <summary>Proposition de correction</summary>

```javascript
button.addEventListener('click', ()=>{
    titre.classList.toggle('active')
    button.classList.toggle('active')
})
```
</details>

4. **Pour pouvoir visualiser les changements, ajoutez du CSS qui modifiera l'apparence du titre lorsqu'il sera actif**

<details>
    <summary>Proposition de correction</summary>

```css
h1.active {
    color: red;
}
```
</details>

---
#### **Étape Bonus : Ajouter un formulaire avec JavaScript**

Maintenant que notre CV est fait, on veut pouvoir l'actualiser de façon interactive ! Pour cela, nous allons mettre en place un formulaire qui permet d'ajouter une nouvelle compétence dans la section de notre choix :

1. **D'abord un peu de HTML : Ajoutez la liste déroulante permettant de lister les sections (balise `select` contenant une liste de `option`), un champ texte qui va vous permettre d'écrire la nouvelle compétence et un bouton pour valider** :
   <a href="https://developer.mozilla.org/fr/docs/Web/HTML/Reference/Elements/select" target="_blank" rel="noopener noreferrer">
   documentation listes déroulantes
   </a>

<details>
  <summary>Proposition de correction</summary>

```html
<div class="ajout">
    <h1>Ajouter une compétence</h1>
    <select id="selectionRubrique">
        <option value="humaines">Compétences humaines</option>
        <option value="techniques">Compétences techniques</option>
        <option value="hobbies">Hobbies</option>
    </select>
    <br/>
    <input type="text" id="nouvelleCompetence" placeholder="Nouvelle compétence"/>
    <br/>
    <button>Ajouter une compétence</button>
</div>
```
</details>

2. **Déclenchez une action Javascript au click sur le bouton**
    - Dans le code Javascript, écrivez une fonction "ajout" <a href="https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Function" target="_blank" rel="noopener noreferrer">syntaxe fonction</a> qui va afficher à l'écran une `alert` indiquant "J'ai cliqué !" <a href="https://developer.mozilla.org/fr/docs/Web/API/Window/alert" target="_blank" rel="noopener noreferrer">syntaxe alert</a>
    - Dans le HTML, ajoutez un attribut "onclick" sur le bouton qui va appeler cette fonction
<details>
  <summary>Proposition de correction</summary>

```html
  <button onclick="ajout()">Ajouter une compétence</button>
```
```javascript
  function ajout() {
    alert("J'ai cliqué !!")
  }
```
</details>

3. **Lisez le contenu de votre formulaire lors du click sur le bouton**
    - Dans la fonction "ajout", utilisez `document.getElementById` sur l'ID de la liste déroulante pour récupérer sa valeur et la stocker dans une `const` : documentation <a href="https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById" target="_blank" rel="noopener noreferrer">getElementById()</a> et <a href="https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Statements/const" target="_blank" rel="noopener noreferrer">const</a>
    - Faites de même pour lire la compétence saisie dans le formulaire
    - Affichez le résultat dans la fenêtre d'alerte à la place du "J'ai cliqué"


<details>
  <summary>Proposition de correction</summary>

```javascript
function ajout() {
    const sectionSelected = document.getElementById('selectionRubrique').value
    const nouvelleCompetence = document.getElementById('nouvelleCompetence').value
    alert(sectionSelected + " " + nouvelleCompetence)
}
```
</details>

4. **Ajoutez cette nouvelle compétence à votre CV**
    - Utilisez à nouveau `document.getElementById` pour récupérer la section HTML correspondant à la valeur stockée dans `sectionSelected`
    - Utilisez `document.createElement` pour créer un nouvel élément `<li>` puis `document.createTextNode` pour créer l'élément texte de ce `<li>`: documentation <a href="https://developer.mozilla.org/fr/docs/Web/API/Document/createElement" target="_blank" rel="noopener noreferrer">document.createElement</a> et <a href="https://developer.mozilla.org/fr/docs/Web/API/Document/createTextNode" target="_blank" rel="noopener noreferrer">document.createTextNode</a>
    - Ajoutez l'élément texte au `<li>` avec `appendChild`, et le `<li>` à la section HTML de la même façon : documentation <a href="https://developer.mozilla.org/fr/docs/Web/API/Node/appendChild" target="_blank" rel="noopener noreferrer">appendChild</a>

<details>
  <summary>Proposition de correction</summary>

```javascript
function ajout() {
    const sectionSelected = document.getElementById('selectionRubrique').value
    const section = document.getElementById(sectionSelected)
    const nouvelElement = document.createElement("li")
    const textNouvelElement = document.createTextNode(document.getElementById('nouvelleCompetence').value)
    nouvelElement.appendChild(textNouvelElement)
    section.appendChild(nouvelElement)
}
```
</details>

5. **Testez !!**

<a href="https://codepen.io/Marion-Pougnard/pen/NPNQzqJ" target="_blank" rel="noopener noreferrer">
    Proposition finale
</a>


### **Résumé**
À la fin de l'atelier, chaque participante aura :
1. Une page web basique avec HTML.
2. Un CV stylisé avec CSS.
3. Une interaction grâce à JavaScript.
